---
layout: post
title: 🖥️ 카카오톡 메신저에 OGP 연동하기
date: 2015-06-19 23:33:10 +0900
description: 카카오톡 메신저에 OGP 연동하기 # Add post description (optional)
img: report/kakao-meta-ogp-1.jpg # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [개발일지]
---
## 카카오톡 메신저에 OGP 연동
- [카카오톡 앱 안드로이드](https://play.google.com/store/apps/details?id=com.kakao.talk)  버전이 2015년 6월 16일 기준으로 5.0.0으로 업데이트 되었는데,  **URL 미리보기 기능**이 눈에 띈다.

![kakao-meta-ogp-0.jpg](/img/in-post/kakao-meta-ogp-0.jpg)

- URL을 클릭하기 전에는 어떤 컨텐츠인지 알 수 없는데, 업데이트된 카카오톡 메신저의 URL 미리보기 기능은 내용에 포함된 섬네일 이미지, 제목, 요약정보를 함께 표시해주고 있다. 정보를 받는 입장에서는 데이터(3G/LTE) 낭비, 피싱(스팸)에 노출되는 확률을 줄일 수 있으려나? 
- 사이트 이동을 쉽게 유도할 수 있는 순기능? 낚시기능? 양날의 검이 될 거 같은 OGP기능

- 모두 카카오톡에서 아래와 같은 경험 한 번씩 해봤을 것이다.**
 뉴스/블로그/동영상 친구에게 전송하거나  
 원문과 다른 낚시성 내용을 친구에게 전송

![kakao-meta-ogp-1.jpg](/img/in-post/kakao-meta-ogp-1.jpg)

## OGP 적용하기1
- 미리보기 기능은 공유되는 URL 에 설정된 [Open Graph Protocol (이하  **OG**)](http://ogp.me/) 정보를 기반으로 표시해 주고 있는데, 정보 제공, 물건 판매, 블로거 서비스에서는 괜찮은 기능같다.  **OG**는 meta tag 로 정의되어 있으며, 카카오톡에서 사용하는  **OG**는 아래 3개이다. 더 많은 종류는 [Open Graph Protocol 사이트](http://ogp.me/) 에서 볼 수 있다! ㅋ
~~~ html
<meta property="og:image" content="섬네일 이미지" />
<meta property="og:title" content="여기다 제목" />
<meta property="og:description" content="간단한 요약 내용" />
~~~
- 물론, 아직 사이트 대부분은 **OG**가 정의되어 있지 않으며, **OG**가 없어도 <body> 내의 컨텐츠에서 첫 번째 이미지와 HTML TAG를 제외한 텍스트를 파싱해서 요약정보를 보여주고 있지만, 정보의 신뢰도를 높이고, 효율적으로 공유하는 데 있어서, 앞으로 **OG**는 필수라고 볼 수 있다.

![kakao-meta-ogp-2.jpg](/img/in-post/kakao-meta-ogp-2.jpg)

## OGP 적용하기2
위에는 스크린 샷은 내가 선택한 섬네일 이미지, 링크제목, 링크 요약내용이 포함되어 URL을 공유하는 화면이며, 소스는 아래와 같이 간단하다.  **OG**  정보가 포함된 4, 5, 6 line만 있으면 된다.  

~~~ html
<!DOCTYPE html>
<html lang="ko-KR">
<head>
<meta property="og:image" content="[http://www.incheonutd.com/images/club/club_emblem_1.jpg](http://www.incheonutd.com/images/club/club_emblem_1.jpg)" />
<meta property="og:title" content="여기다 제목" />
<meta property="og:description" content="간단한 요약 내용" />
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>내 이야기좀 들어볼래? | @real21c</title>
<script type='text/javascript' src='[http://real21c.com/admin/wp-includes/js/jquery/jquery.js?ver=1.11.2](http://real21c.com/admin/wp-includes/js/jquery/jquery.js?ver=1.11.2)'></script>
</head>
<body>
<p>
인천 유나이티드(Incheon United Football Club)는 인천광역시를 연고로 하는 대한민국 K리그 클래식 소속의 프로축구단이다. 법적으로는 주식회사인데, 상당수 주식을 시민들이 보유하는, 즉 시민들이 주주로 참여하고 있는 소위 시민구단이다. 2003년에 팀이 창단되어 2004시즌부터 리그에 참가했으며,[1] 인천광역시와 인천광역시민이 중심이 되어 창단한 시민구단이다. 인천 유나이티드의 애칭이자 약칭인 '인유' 혹은 '유나이티드'로 불리고 있다. 홈 경기장은 인천광역시 남구 문학동에 있는 인천문학경기장을 사용했으며, 2012년부터 새로 완공된 인천축구전용경기장을 홈 경기장으로 사용하고 있다.
</p>
내용출처: <a href="[https://ko.wikipedia.org/wiki/%EC%9D%B8%EC%B2%9C_%EC%9C%A0%EB%82%98%EC%9D%B4%ED%8B%B0%EB%93%9C_FC](https://ko.wikipedia.org/wiki/%EC%9D%B8%EC%B2%9C_%EC%9C%A0%EB%82%98%EC%9D%B4%ED%8B%B0%EB%93%9C_FC)" target="_blank">위키트리</a><br/>
사진출처: <a href="[http://incheonutd.com/](http://incheonutd.com/)" target="_blank">인천유나이티드 홈페이지</a>
</pre>
</body>
</html>
~~~




## 적용 후기
- 현재 facebook, daum 뉴스, naver 뉴스/블로그, 인스타그램 등… 많은 소셜 서비스에서 **OG**가 적용이 되어 있는데, 내가 만드는 웹 서비스의 분류가 정보공유, 커뮤니케이션 분류에 해당할 경우에는, 소셜 연동이라던가 앞으로 여러 가지 확장성을 고려해서 **OG** 정보는 필수로 포함시키는 게 좋을 듯싶다.

- 요즘 기사도 로봇이 작성해주는 것이 트렌드인데,  기사/블로그/카페 등.. 에 적용할 수 있는 **OG**정보를 자동으로 생성해주는 플러그인을 만들어도 괜찮을 거 같다.