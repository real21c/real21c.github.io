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
	font-size:16px;
}

.post-content ol, .post-content ul {
	padding-left: 0rem;
}

.mobile-only {
	display: none;
}

.desktop-only{
	display: block;
}

@media (max-width: 400px) {
	.mobile-only {
		display: block;
	}

	.desktop-only{
		display: none;
	}
}

.post-container li h4{
	line-height:initial;
}

.author-info {
    margin: 20px auto 40px;
}

.author-title {
    font-size: 4rem;
}

.author-meta {
    color: #9EABB3;
    font-size: 1.6rem;
}

.author-meta a {
    margin-top: 10px;
    color: #9EABB3;
}

a.icon-linkedin{
    color: #0a66c2;
}
</style>

<div class="profile">
<article class="single-post">                
	<section class="post-content">           
		<div class="md-card no-border"><p>
		Hello.<br/>
		I'm constantly striving to solve daily and work-related problems with IT technology and become a better developer.<br/>
		You can find details about my projects and awards on my <a href="https://linkedin.com/in/real21c/"
		   target="_blank"
		   rel="me"
		   itemprop="sameAs"
		   aria-label="LinkedIn"
		   style="display:inline-flex; align-items:center; gap:4px; vertical-align:middle; text-decoration:none;">
			<svg width="24" height="24"
			     viewBox="0 0 16 16"
			     xmlns="http://www.w3.org/2000/svg"
			     style="display:block;">
				<path fill="#0A66C2"
				      d="M12.225 12.225h-1.778V9.44c0-.664-.012-1.519-.925-1.519-.926 0-1.068.724-1.068 1.47v2.834H6.676V6.498h1.707v.783h.024c.348-.594.996-.95 1.684-.925 1.802 0 2.135 1.185 2.135 2.728l-.001 3.14zM4.67 5.715a1.037 1.037 0 01-1.032-1.031c0-.566.466-1.032 1.032-1.032.566 0 1.031.466 1.032 1.032 0 .566-.466 1.032-1.032 1.032zm.889 6.51h-1.78V6.498h1.78v5.727zM13.11 2H2.885A.88.88 0 002 2.866v10.268a.88.88 0 00.885.866h10.226a.882.882 0 00.889-.866V2.865a.88.88 0 00-.889-.864z"/>
			</svg>
			LinkedIn
		</a> profile.<br/>
		Thank you.</p></div>

		<div class="timeline-container" style="padding: 0 0; margin-top:0;">
			<div class="container-fluid">
				<div class="row example-basic">
					<ul class="timeline">
						<li class="timeline-item period">
							<div class="timeline-info"></div>
							<div class="timeline-content" style="padding-top:0px;"><h2 class="timeline-title" style="line-height:0;">Present</h2></div>
						</li>
						<li class="timeline-item">
							<div class="timeline-info">
								<span>Dec,2020~Now</span>
								<span class="calc_my" style="color:#fbceb1;"></span>
							</div>
							<div class="timeline-marker"></div>
							<div class="timeline-content" style="font-size:1.5rem;">
								<h4 class="timeline-title">Software Engineer (Full-Stack)</h4>
								<p>- Development of XR-based 3D spatial digitization and custom viewer services</p>
								<p>- Development of a digital signage content playback engine and management platform for educational institutions</p>
								<p>- Development of an online certificate issuance solution</p>
								<p>- Development of a web service for academic affairs management in educational institutions</p>
							</div>
						</li>
						<li class="timeline-item">
							<div class="timeline-info">
								<span>Dec,2020~Now</span>
								<span class="calc_my" style="color:#fbceb1;"></span>
							</div>
							<div class="timeline-marker"></div>
							<div class="timeline-content" style="font-size:1.5rem;">
								<h4 class="timeline-title">Mobile Developer (Android / iOS)</h4>
								<p>- End-to-end development and deployment of mobile apps for over 150 clients.</p>
							</div>
						</li>
						<li class="timeline-item">
							<div class="timeline-info">
								<span>Dec,2020~Now</span>
								<span class="calc_my" style="color:#fbceb1;"></span>
							</div>
							<div class="timeline-marker"></div>
							<div class="timeline-content" style="font-size:1.5rem;">
								<h4 class="timeline-title">DevOps Engineer</h4>
								<p>- Development of an FDS-based system anomaly detection monitoring solution (for in-house application)</p>
							</div>
						</li>
						<li class="timeline-item period">
							<div class="timeline-info"></div>
							<div class="timeline-marker"></div>
							<div class="timeline-content" style="padding-top:0px;"><h2 class="timeline-title" style="line-height:0;">Past</h2></div>
						</li>
						<li class="timeline-item">
							<div class="timeline-info">
								<span>Feb,2019~Dec,2020</span>
								<span style="color:#fbceb1;"><strong>(1</strong> yr <strong>11</strong> mos)</span>
							</div>
							<div class="timeline-marker"></div>
							<div class="timeline-content" style="font-size:1.5rem;">
								<h4 class="timeline-title">Founder / CTO<br/><span class="timeline-company" style="font-weight:400;">Unsung Data</span></h4>
								<p>- K-Startup Selected for Support from the Ministry of SMEs and Startups</p>
								<p>- Healthcare Solution Planning and Web/Android Service Development/Launch</p>
							</div>
						</li>
						<li class="timeline-item">
							<div class="timeline-info">
								<span>Mar,2013~Jan,2019 Jan</span>
								<span style="color:#fbceb1;"><strong>(6</strong> yrs)</span>
							</div>
							<div class="timeline-marker"></div>
							<div class="timeline-content" style="font-size:1.5rem;">
								<h4 class="timeline-title">Software Engineer<br/><span class="timeline-company" style="font-weight:400;">Webchon</span></h4>
								<p>- Development of in-store music programming and real-time streaming web services</p>
								<p>- Development of a solution for anonymous public interest reporting and reporting violations of the Anti-Corruption and Bribery Act</p>
								<p>- Development of a survey solution for assessing the risk of corruption among high-ranking public officials</p>
							</div>
						</li>
						<li class="timeline-item">
							<div class="timeline-info">
								<span>Mar,2011~Dec,2012</span>
								<span style="color:#fbceb1;"><strong>(1</strong> yr <strong>10</strong> mos)</span>
							</div>
							<div class="timeline-marker"></div>
							<div class="timeline-content" style="font-size:1.5rem;">
								<h4 class="timeline-title">Web Developer<br/><span class="timeline-company" style="font-weight:400;">Cansplex</span></h4>
								<p>- Development of hospital/clinic website solution</p>
							</div>
						</li>
						<li class="timeline-item">
							<div class="timeline-info">
								<span>Jun,2010~Mar,2011</span>
								<span style="color:#fbceb1;">(<strong>11</strong> mos)</span>
							</div>
							<div class="timeline-marker"></div>
							<div class="timeline-content" style="font-size:1.5rem;">
								<h4 class="timeline-title">Web Developer<br/><span class="timeline-company" style="font-weight:400;">Freechal</span></h4>
								<p>- Development of Freechal News Portal Site</p>
								<p>- Freechal Mobile Service Telecom Integration/Development (KTF Freezone)</p>
								<p>- Development of TweetShow, a real-time Twitter exposure service</p>
							</div>
						</li>
						<li class="timeline-item">
							<div class="timeline-info">
								<span>Feb,2009~Apr,2010</span>
								<span style="color:#fbceb1;"><strong>(1</strong> yr <strong>3</strong> mos)</span>
							</div>
							<div class="timeline-marker"></div>
							<div class="timeline-content" style="font-size:1.5rem;">
								<h4 class="timeline-title">Web Application Developer<br/><span class="timeline-company" style="font-weight:400;">Webchon</span></h4>
								<p>-Homepage solution builder development</p>
							</div>
						</li>
						<li class="timeline-item">
							<div class="timeline-info">
								<span>Feb,2007~Feb,2009</span>
								<span style="color:#fbceb1;"><strong>(2</strong> yrs <strong>1</strong> mo)</span>
							</div>
							<div class="timeline-marker"></div>
							<div class="timeline-content" style="font-size:1.5rem;">
								<h4 class="timeline-title">Web Developer<br/><span class="timeline-company" style="font-weight:400;">SM ONLINE</span></h4>
								<p>- Development of SM Entertainment's Star Community Portal</p>
								<p>- Migration of MNcast video streaming encoding processor (VP6 → H.264)</p>
								<p>- Participation in the development of the alumni search service "Damoim"</p>
							</div>
						</li>
						<li class="timeline-item">
							<div class="timeline-info">
								<span>Apr,2001~Jul,2007</span>
								<span style="color:#fbceb1;"><strong>(5</strong> yrs <strong>11</strong> mos)</span>
							</div>
							<div class="timeline-marker"></div>
							<div class="timeline-content" style="font-size:1.5rem;">
								<h4 class="timeline-title">Web Application Developer<br/><span class="timeline-company" style="font-weight:400;">DOM Co., Ltd.</span></h4>
								<p>- Designed and developed an electronic approval web service and internal community platform</p>
								<p>- Led the full lifecycle (planning, design, development, and operation) of an ERP-based integrated resource management system for manufacturing</p>
								<p>- Designed and developed a knowledge-sharing system and workflow engine</p>
							</div>
						</li>
					</ul>
				</div>
			</div>
		</div>
	</section>
</article>
</div>
<script type="text/javascript">
function durationFromStartToNowHTML(startYear, startMonth) {
	const now = new Date();
	const endYear = now.getFullYear();
	const endMonth = now.getMonth() + 1; // 0-based → 1-based

	const totalMonths =
	(endYear - startYear) * 12 +
	(endMonth - startMonth) + 1; // inclusive

	const years = Math.floor(totalMonths / 12);
	const months = totalMonths % 12;

	let html = '(';

	if (years > 0) {
		html += `<strong>${years}</strong> yr${years !== 1 ? 's' : ''}`;
	}

	if (months > 0) {
		if (years > 0) html += ' ';
		html += `<strong>${months}</strong> mo${months !== 1 ? 's' : ''}`;
	}

	html += ')';

	return html;
}

document.querySelectorAll('.calc_my').forEach(el => {
	el.innerHTML = durationFromStartToNowHTML(2020, 12);
});
</script>