---
layout: post
title: 🖥️ 네이버 투표 사이트 분석
date: 2015-06-15 11:21:32 +0900
description: 네이버는 생각만큼 허술하지 않았다 # Add post description (optional)
img: /report/http-referer-allstar.jpg # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [개발일지]
---

## 네이버 투표 분석하기 
- K리그 올스타전 자동 투표 프로그램을 만들기 위해 네이버 서비스를 분석했다.
-[2015년 K리그 올스타전 투표](http://m.sports.naver.com/event/soccer/allstar/result.nhn?side=classic) 는 전체 후보 44명중에서 20명을 투표하는 방식이다.

## 1. 분석
- 내가 원하는 20명을 강제 or 임의 지정하고, 자동으로 전송하는게 최종 목표
- 후보 선수들마다 숫자로 된 고유(UNIQUE)의 ID가 존재 하는데, 투표 페이지에서 [소스보기] 하면 알아낼 수 있다. (YYYYMMDD 형식인데, 연맹에 선수등록 시점? 입단날짜?)
- 투표를 전송하는 모듈은  [m.sports.naver.com/js/source/event/allstar/kleague_allstar_2015.js?v=201506040000](http://m.sports.naver.com/js/source/event/allstar/kleague_allstar_2015.js?v=201506040000)  에 정의되어 있는데, 스크립트 파일이 다운사이징 되어 있는 상태라서 알아보기 힘들다.  [js code fomatter](https://www.google.co.kr/search?q=js+code+fomatter&oq=js+code+fomatter&aqs=chrome..69i57j0l4.207j0j7&sourceid=chrome&es_sm=93&ie=UTF-8),  [beautiful code](https://www.google.co.kr/search?q=beautiful+code&oq=beautiful+code&aqs=chrome..69i57j0l5.103j0j7&sourceid=chrome&es_sm=93&ie=UTF-8#newwindow=1&q=beautiful+code+js)  구글에서 검색하면 많이 나오니, 도움 받으면 코드를 예쁘게 들여쓰기까지 적용변환 시켜준다. 

- 아래는 스크립트에 선언된, 실제로 투표를 전송하는 vote() 함수.
~~~javascript
function vote(side) {
  if (checkTotalCount("C")) {
  if (!confirm("투표하시겠습니까?")) {
    return
  }
  var param = {};
  param.CGK1 = selectedPlayerObj.CGK[0].playerId;
  param.CGK2 = selectedPlayerObj.CGK[1].playerId;
  param.CDFL1 = selectedPlayerObj.CDFL[0].playerId;
  param.CDFL2 = selectedPlayerObj.CDFL[1].playerId;
  param.CDFC1 = selectedPlayerObj.CDFC[0].playerId;
  param.CDFC2 = selectedPlayerObj.CDFC[1].playerId;
  param.CDFC3 = selectedPlayerObj.CDFC[2].playerId;
  param.CDFC4 = selectedPlayerObj.CDFC[3].playerId;
  param.CDFR1 = selectedPlayerObj.CDFR[0].playerId;
  param.CDFR2 = selectedPlayerObj.CDFR[1].playerId;
  param.CMFL1 = selectedPlayerObj.CMFL[0].playerId;
  param.CMFL2 = selectedPlayerObj.CMFL[1].playerId;
  param.CMFC1 = selectedPlayerObj.CMFC[0].playerId;
  param.CMFC2 = selectedPlayerObj.CMFC[1].playerId;
  param.CMFC3 = selectedPlayerObj.CMFC[2].playerId;
  param.CMFC4 = selectedPlayerObj.CMFC[3].playerId;
  param.CMFR1 = selectedPlayerObj.CMFR[0].playerId;
  param.CMFR2 = selectedPlayerObj.CMFR[1].playerId;
  param.CFW1 = selectedPlayerObj.CFW[0].playerId;
  param.CFW2 = selectedPlayerObj.CFW[1].playerId;
  param.CFW3 = selectedPlayerObj.CFW[2].playerId;
  param.CFW4 = selectedPlayerObj.CFW[3].playerId;
  ajaxVote = jindo.$Ajax("/event/soccer/allstar/vote.nhn", {
    type: "xhr",
    method: "post",
    onload: function(res) {
      var resMessage = statusCodetoMessage[res.text()] == null ? statusCodetoMessage.systemError : statusCodetoMessage[res.text()];
      alert(resMessage);
      document.location = "/event/soccer/allstar/index.nhn"
    }
  }).request(param)
  } 
  else {
    alert("각 팀별/포지션별로 필요한 후보수를 채워주세요.")
  }
} 
~~~
- 네이버의 Jindo 라이브러리를 이용해서 20명의 선수ID 전송하면 끝? 어랏 간단하네..어떤 유효성 체크하는 코드도 없기 때문에, 쾌재를 부르면서 내가 원하는 선수ID를 강제로 json 형태로 만들어서 전송!

## 2. 시도

**invalidReferer**

- 그렇다. 나처럼 이상한 BOT을 만들어서 시도하는 사람들을 차단하기 위해서, HTTP헤더에 있는 REFERER 유효성을 검사하고 있었다.
- 즉, 네이버 투표 페이지를 통해서만 (정상적인 접근) 투표결과를 집계할 수 있도록 체크하고 있다. 

- 그렇다면 HTTP 헤더를 변조시켜서, 투표페이지에서 진행하는 것처럼 속여서 다시 전송을 시도해본다면? 
REFERER는 이전의 사이트 위치정보를 가지고 있기 때문에, 올스타전의 전송값을 체크하는 [http://m.sports.naver.com/event/soccer/allstar/vote.nhn](http://m.sports.naver.com/event/soccer/allstar/vote.nhn)  입장에서 REFERER 체크하는 위치는
[http://m.sports.naver.com/event/soccer/allstar/voteMain.nhn?order=nameside=classic](http://m.sports.naver.com/event/soccer/allstar/voteMain.nhn?order=nameside=classic)  올스타 투표를 선택하는 페이지URL이 된다.

~~~php
<?php
$allstar2015 = 1;
if($_GET["allstar2015"]){
	phpinfo();
}
else {
	$header = 'Host:'.$_SERVER["HTTP_HOST"]."\r\n".'Referer:[http://m.sports.naver.com/event/soccer/allstar/voteMain.nhn?order=nameside=classic](http://m.sports.naver.com/event/soccer/allstar/voteMain.nhn?order=nameside=classic)';
	$socket = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);
	if(socket_connect($socket, $_SERVER["HTTP_HOST"], 80)) {
		socket_write($socket, 'GET '.$_SERVER["REQUEST_URI"].'?allstar2015=1 HTTP/1.0'."\r\n".$header."\r\n\r\n");
		while($strRecv = socket_read($socket, 1024)) {
			echo $strRecv;
		}
		socket_close($socket);
	}
}
?>
~~~
- REFERER 를 출력하면 아래와 같이 조작에 성공하였는데, 투표결과를 전송하면  
**invalidReferer**  

![http-referer-allstar.jpg](/img/in-post/http-referer-allstar.jpg)


## 3. 결론
- 안된다ㅎㅎㅎ 
- 기본적인 유효성 처리를 하고 있기 때문에, 단순한 투표 시스템일지라도 네이버처럼 REFERE체크뿐 아니라, 중복 체크, IP체크 등… 여러가지 신경을 많이 써야함에도 카운트 처리만 하는 방식은 꽤나 위험함에도, 일반적인 웹사이트에서 이런 방식을 시도하면 잘 되는 곳도 있다.
- 참고로 에스토니아라는 국가정부에서는 전자투표를 하는데, 정치적인 특성상 제기되는 의혹과 시스템의 불안함에 대한 가능성을 줄이고, 투명성을 높이고자, 투표시스템의 소스코드를 공개! [기사](http://www.betanews.net/article/580781)
- 네이버 ID당 1일 1회 투표이므로, 매일 5분씩만 투자해서, 수동으로 하자.
- 안될 거란 것을 알면서도, 도전해봤지만 실패. 나도 버그에서는 자유로울 수 없는 개발자이고, 누군가의 대상(!)인데, 나부터 잘하자.ㅠ