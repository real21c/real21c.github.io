<style type="text/css">
/*-- GENERAL STYLES ------------------------------*/
.timeline {
line-height: 1.4em;
list-style: none;
margin: 0;
padding: 0;
width: 100%;
}

.timeline h1,
.timeline h2,
.timeline h3,
.timeline h4,
.timeline h5,
.timeline h6 {
line-height: inherit;
}

/*----- TIMELINE ITEM -----*/
.timeline-item {
padding-left: 40px;
position: relative;
}

.timeline-item:last-child {
padding-bottom: 0;
}

/*----- TIMELINE INFO -----*/
.timeline-info {
font-size: 12px;
font-weight: 700;
letter-spacing: 3px;
margin: 0 0 .5em 0;
text-transform: uppercase;
white-space: nowrap;
}

/*----- TIMELINE MARKER -----*/
.timeline-marker {
position: absolute;
top: 0;
bottom: 0;
left: 0;
width: 15px;
}

.timeline-marker:before {
background: tomato; /* $primary-color */
border: 2px solid transparent;
border-radius: 100%;
content: "";
display: block;
height: 12px;
position: absolute;
top: 4px;
left: 0;
width: 12px;
transition: background 0.3s ease-in-out,
border 0.3s ease-in-out;
}

.timeline-marker:after {
content: "";
width: 3px;
background: #CCD5DB;
display: block;
position: absolute;
top: 24px;
bottom: 0;
left: 6px;
}

.timeline-item:last-child .timeline-marker:after {
content: none;
}


/*----- TIMELINE CONTENT -----*/
.timeline-content {
padding-bottom: 40px;
}

.timeline-content p:last-child {
margin-bottom: 0;
}

/*----- TIMELINE PERIOD -----*/
.period {
padding: 0;
}

.period .timeline-info {
display: none;
}

.period .timeline-marker:before {
background: transparent;
content: "";
width: 15px;
height: auto;
border: none;
border-radius: 0;
top: 0;
bottom: 30px;
position: absolute;
border-top: 3px solid #CCD5DB;
border-bottom: 3px solid #CCD5DB;
}

.period .timeline-marker:after {
content: "";
height: 32px;
top: auto;
}

.period .timeline-content {
padding: 40px 0 70px;
}

.period .timeline-title {
margin: 0;
}

/*----------------------------------------------
MOD: TIMELINE SPLIT
----------------------------------------------*/
@media (min-width: 768px) {
.timeline-split .timeline {
display: table;
}

.timeline-split .timeline-item {
display: table-row;
padding: 0;
}

.timeline-split .timeline-info,
.timeline-split .timeline-marker,
.timeline-split .timeline-content,
.timeline-split .period .timeline-info {
display: table-cell;
vertical-align: top;
}

.timeline-split .timeline-marker {
position: relative;
}

.timeline-split .timeline-content {
padding-left: 30px;
}

.timeline-split .timeline-info {
padding-right: 30px;
}

.timeline-split .period .timeline-title {
position: relative;
left: -45px;
}
}

/*----------------------------------------------
MOD: MARKER OUTLINE
----------------------------------------------*/
.marker-outline .timeline-marker:before {
background: transparent;
border-color: #3498db;
}

.marker-outline .timeline-item:hover .timeline-marker:before {
background: #3498db;
}

.timeline-container:before {
background:initial;
}

.timeline-content{
padding:0 0 30px 0;
}
.timeline-info{
color:#aaa;
}

.timeline-company{
color:#aaa;
font-weight: normal;
}

.post-content ol, .post-content ul {
padding-left: 0rem;
}

</style>

<div class="profile">
<article class="single-post">                
	<section class="post-content">           
		<div class="md-card no-border">
			<p>일상과 업무에 새로운 가치를 더하는 데 깊은 관심을 가지고 있으며, 생활 속 불편한 문제를 IT 기술로 개선하고 해결하는 것을 즐기는 개발자입니다. <br/>자세한 경력과 프로젝트는 LinkedIn 프로필에서 확인하실 수 있습니다.</p>
		</div>
		<div class="timeline-container" style="padding: 0 0; margin-top:0;">
			<div class="container-fluid">
				<div class="row example-basic">
					<div class="col-xs-10 col-xs-offset-1 col-sm-8 col-sm-offset-2">
						<ul class="timeline">
							<li class="timeline-item period">
								<div class="timeline-info"></div>
								<div class="timeline-marker"></div>
								<div class="timeline-content">
								<h2 class="timeline-title">현재</h2>
								</div>
							</li>
							<li class="timeline-item">
								<div class="timeline-info">
								<span>Dec,2020 ~ Now</span>
								</div>
								<div class="timeline-marker"></div>
								<div class="timeline-content" style="font-size:1.5rem;">
								<h4 class="timeline-title">Software Engineer (Full-Stack)</h4>
								<p>- XR 기반 3D 공간 디지털화 및 커스텀 뷰어 서비스 개발</p>
								<p>- 교육기관용 디지털 사이니지 콘텐츠 재생 엔진 및 관리 플랫폼 개발</p>
								<p>- 온라인 증명서 발급 솔루션 개발</p>
								<p>- 교육기관 학사 운영 관리 웹서비스 개발</p>
								</div>
							</li>
							<li class="timeline-item">
								<div class="timeline-info">
								<span>Dec,2020 ~ Now</span>
								</div>
								<div class="timeline-marker"></div>
								<div class="timeline-content" style="font-size:1.5rem;">
								<h4 class="timeline-title">Mobile Developer (Android / iOS)</h4>
								<p>- 150여 개 이상 고객사 모바일 앱 End-to-End 개발 및 배포 수행</p>
								</div>
							</li>
							<li class="timeline-item">
								<div class="timeline-info">
								<span>Dec,2020 ~ Now</span>
								</div>
								<div class="timeline-marker"></div>
								<div class="timeline-content" style="font-size:1.5rem;">
								<h4 class="timeline-title">DevOps Engineer</h4>
								<p>- FDS 기반 시스템 이상 탐지 모니터링 솔루션 개발 (사내 적용)</p>
								</div>
							</li>
							<li class="timeline-item period">
								<div class="timeline-info"></div>
								<div class="timeline-marker"></div>
								<div class="timeline-content">
								<h2 class="timeline-title">과거</h2>
								</div>
							</li>
							<li class="timeline-item">
								<div class="timeline-info">
								<span>Feb,2019 ~ Dec,2020</span>
								</div>
								<div class="timeline-marker"></div>
								<div class="timeline-content" style="font-size:1.5rem;">
								<h4 class="timeline-title">Founder / CTO<br/><span class="timeline-company" style="font-weight:400;">언성데이터</span></h4>
								<p>- K-Startup 중소벤처기업부 지원사업 선정</p>
								<p>- 헬스케어 솔루션 기획 및 Web/Android 서비스 개발/출시</p>
								</div>
							</li>
							<li class="timeline-item">
								<div class="timeline-info">
								<span>Mar,2013 ~ Jan,2019</span>
								</div>
								<div class="timeline-marker"></div>
								<div class="timeline-content" style="font-size:1.5rem;">
								<h4 class="timeline-title">Software Engineer<br/><span class="timeline-company" style="font-weight:400;">Webchon</span></h4>
								<p>- 매장 음악 편성 및 실시간 스트리밍 웹서비스 개발</p>
								<p>- 익명성 공익제보 및 청탁금지법 위반 신고 솔루션 개발</p>
								<p>- 고위공직자 부패 위험성 진단 설문 솔루션 개발</p>
								</div>
							</li>
							<li class="timeline-item">
								<div class="timeline-info">
								<span>Mar,2011 ~ Dec,2012</span>
								</div>
								<div class="timeline-marker"></div>
								<div class="timeline-content" style="font-size:1.5rem;">
								<h4 class="timeline-title">Web Developer<br/><span class="timeline-company" style="font-weight:400;">Cansplex</span></h4>
								<p>- 병원/의원 홈페이지 솔루션 개발</p>
								</div>
							</li>
							<li class="timeline-item">
								<div class="timeline-info">
								<span>Jun,2010 ~ Mar,2011</span>
								</div>
								<div class="timeline-marker"></div>
								<div class="timeline-content" style="font-size:1.5rem;">
								<h4 class="timeline-title">Web Developer<br/><span class="timeline-company" style="font-weight:400;">프리챌</span></h4>
								<p>- 프리챌 뉴스 포털 사이트 개발</p>
								<p>- 프리챌 모바일 서비스 연동/개발 (KTF Freezone)</p>
								<p>- 트위터 실시간 노출 서비스 TweetShow 개발</p>
								</div>
							</li>
							<li class="timeline-item">
								<div class="timeline-info">
								<span>Feb,2009 ~ Apr,2010</span>
								</div>
								<div class="timeline-marker"></div>
								<div class="timeline-content" style="font-size:1.5rem;">
								<h4 class="timeline-title">Web Application Developer<br/><span class="timeline-company" style="font-weight:400;">Webchon</span></h4>
								<p>-홈페이지 솔루션 빌더 개발</p>
								</div>
							</li>
							<li class="timeline-item">
								<div class="timeline-info">
								<span>Feb,2007 ~ Feb,2009</span>
								</div>
								<div class="timeline-marker"></div>
								<div class="timeline-content" style="font-size:1.5rem;">
								<h4 class="timeline-title">Web Developer<br/><span class="timeline-company" style="font-weight:400;">SM온라인</span></h4>
								<p>- SM엔터테인먼트 스타 커뮤니티 포털 개발</p>
								<p>- 엠엔캐스트 동영상 스트리밍 인코딩 시스템 마이그레이션 (VP6 → H.264)</p>
								<p>- 동창 찾기 서비스 ‘다모임’ 개발 참여</p>
								</div>
							</li>
							<li class="timeline-item">
								<div class="timeline-info">
								<span>Apr,2001 ~ Jul,2007</span>
								</div>
								<div class="timeline-marker"></div>
								<div class="timeline-content" style="font-size:1.5rem;">
								<h4 class="timeline-title">Web Application Developer<br/><span class="timeline-company" style="font-weight:400;">(주)도움</span></h4>
								<p>- 사내 커뮤니티 웹서비스 개발 (인트라넷, 전자결제)</p>
								<p>- 사내 생산성 향상 기여 업무 지원 시스템 개발 (ERP, BOM, 금형현황판)</p>
								<p>- 사내 업무 자동화 및 정보 공유 시스템 개발 (워크플로우 엔진, 지식관리)</p>
								</div>
							</li>
							<li class="timeline-item">
							</li>
						</ul>
					</div>
				</div>
			</div>
		</div>
	</section>
</article>
</div>