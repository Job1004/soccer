[index.html](https://github.com/user-attachments/files/29154937/index.html)
<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>출판 제안서 — 그라운드 밖의 리더십 · 황명구</title>
<style>
/* ── RESET & BASE ── */
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; font-size: 16px; }
body {
  font-family: 'Apple SD Gothic Neo', 'Noto Sans KR', 'Malgun Gothic', sans-serif;
  color: #1a1a1a; background: #fff; line-height: 1.7;
}
img { display: block; width: 100%; height: 100%; object-fit: cover; }

/* ── COLORS ── */
:root {
  --green: #1D9E75;
  --green-d: #0F6E56;
  --green-l: #E1F5EE;
  --navy: #111827;
  --navy-m: #1e2d4d;
  --gray: #64748b;
  --gray-l: #f1f5f9;
  --gold: #b45309;
  --gold-l: #fef3c7;
  --border: rgba(0,0,0,0.09);
  --red: #dc2626;
}

/* ── NAV ── */
nav {
  position: fixed; top: 0; left: 0; right: 0; z-index: 200;
  height: 58px; display: flex; align-items: center;
  justify-content: space-between; padding: 0 52px;
  background: rgba(255,255,255,0.96); backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--border);
}
.nav-brand { font-size: 14px; font-weight: 700; letter-spacing: 0.03em; }
.nav-brand em { color: var(--green); font-style: normal; }
.nav-links { display: flex; gap: 28px; list-style: none; }
.nav-links a { font-size: 13px; color: var(--gray); text-decoration: none; transition: color .2s; }
.nav-links a:hover { color: var(--green); }
.nav-badge {
  font-size: 12px; font-weight: 600; padding: 6px 18px;
  border-radius: 20px; background: var(--navy); color: #fff;
  letter-spacing: 0.04em;
}

/* ── COVER ── */
#cover {
  min-height: 100vh; padding-top: 58px;
  display: grid; grid-template-columns: 1fr 1fr;
}
.cover-left {
  background: var(--navy);
  display: flex; flex-direction: column; justify-content: center;
  padding: 80px 64px;
  position: relative; overflow: hidden;
}
.cover-left::before {
  content: '';
  position: absolute; inset: 0;
  background: url('images/01_profile_main.jpg') center/cover no-repeat;
  opacity: 0.18;
}
.cover-left-inner { position: relative; z-index: 1; }
.cover-proposal-tag {
  display: inline-flex; align-items: center; gap: 8px;
  font-size: 11px; letter-spacing: 0.16em; font-weight: 700;
  color: var(--green); background: rgba(29,158,117,0.15);
  padding: 6px 14px; border-radius: 4px; margin-bottom: 32px;
  border: 1px solid rgba(29,158,117,0.3);
}
.cover-book-title {
  font-size: clamp(36px, 4vw, 52px); font-weight: 900;
  color: #fff; line-height: 1.15; letter-spacing: -0.02em;
  margin-bottom: 16px;
}
.cover-book-title .accent { color: #5DCAA5; }
.cover-book-sub {
  font-size: 15px; color: rgba(255,255,255,0.55);
  line-height: 1.7; margin-bottom: 40px;
}
.cover-divider { height: 1px; background: rgba(255,255,255,0.12); margin-bottom: 32px; }
.cover-author-name { font-size: 22px; font-weight: 700; color: #fff; margin-bottom: 6px; }
.cover-author-roles { font-size: 13px; color: rgba(255,255,255,0.45); line-height: 1.7; }
.cover-dots {
  position: absolute; bottom: 40px; left: 64px; right: 64px;
  display: flex; gap: 8px; z-index: 1;
}
.dot { width: 6px; height: 6px; border-radius: 50%; background: rgba(255,255,255,0.2); }
.dot.active { background: var(--green); width: 20px; border-radius: 3px; }

.cover-right {
  position: relative; overflow: hidden;
  background: linear-gradient(145deg, #1D9E75 0%, #0d6b4e 100%);
}
.cover-photo {
  position: absolute; inset: 0;
  background: url('images/01_profile_main.jpg') center top/cover no-repeat;
}
.cover-photo-overlay {
  position: absolute; inset: 0;
  background: linear-gradient(to right, rgba(17,24,39,0.6) 0%, transparent 50%);
}
.cover-photo-label {
  position: absolute; bottom: 40px; right: 32px;
  text-align: right; z-index: 2;
}
.cover-photo-label .lname { font-size: 28px; font-weight: 900; color: #fff; }
.cover-photo-label .ltag { font-size: 12px; color: rgba(255,255,255,0.6); margin-top: 4px; letter-spacing: 0.08em; }

/* ── DUAL PHOTO ROW ── */
.photo-duo {
  display: grid; grid-template-columns: 1fr 1fr; gap: 14px;
  max-width: 520px; margin-top: 20px;
}
.photo-duo .tl-photo { margin-top: 0; }

/* ── SHARED SECTION ── */
.section { padding: 96px 0; }
.container { max-width: 1080px; margin: 0 auto; padding: 0 48px; }
.sec-label {
  font-size: 11px; letter-spacing: 0.16em; font-weight: 700;
  color: var(--green); margin-bottom: 12px; text-transform: uppercase;
}
.sec-title {
  font-size: clamp(26px, 3vw, 38px); font-weight: 800;
  color: var(--navy); letter-spacing: -0.02em; line-height: 1.2;
  margin-bottom: 14px;
}
.sec-body { font-size: 16px; color: var(--gray); line-height: 1.85; max-width: 620px; }

/* ── AUTHOR PROFILE ── */
#author { background: var(--gray-l); }
.author-layout {
  display: grid; grid-template-columns: 300px 1fr; gap: 72px; align-items: start;
}
.author-photo-wrap {
  border-radius: 20px; overflow: hidden; aspect-ratio: 3/4;
  background: linear-gradient(145deg, var(--green-l), var(--green));
  position: relative; box-shadow: 0 20px 60px rgba(0,0,0,0.15);
}
.author-photo-wrap img { position: absolute; inset: 0; z-index: 1; }
.author-photo-fallback {
  position: absolute; inset: 0;
  display: flex; align-items: center; justify-content: center;
  font-size: 80px; font-weight: 900; color: rgba(255,255,255,0.9);
}
.author-right { padding-top: 8px; }
.author-headline {
  font-size: 22px; font-weight: 800; color: var(--navy);
  line-height: 1.35; margin-bottom: 20px;
}
.author-desc { font-size: 15px; color: var(--gray); line-height: 1.85; margin-bottom: 16px; }
.author-cred-grid {
  display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-top: 28px;
}
.cred { background: #fff; border-radius: 10px; padding: 14px 16px; border: 1px solid var(--border); }
.cred-label { font-size: 10px; letter-spacing: 0.1em; color: #94a3b8; font-weight: 700; margin-bottom: 5px; }
.cred-val { font-size: 13px; color: var(--navy); font-weight: 600; line-height: 1.5; }

/* ── JOURNEY (TIMELINE WITH PHOTOS) ── */
#journey { background: #fff; }
.tl-wrap { position: relative; padding-left: 48px; }
.tl-wrap::before {
  content: ''; position: absolute; left: 15px; top: 8px; bottom: 8px;
  width: 2px; background: linear-gradient(to bottom, var(--green), rgba(29,158,117,0.1));
}
.tl-item { position: relative; padding-bottom: 64px; }
.tl-item:last-child { padding-bottom: 0; }
.tl-dot {
  position: absolute; left: -48px; top: 6px;
  width: 18px; height: 18px; border-radius: 50%;
  background: var(--green); border: 3px solid #fff;
  box-shadow: 0 0 0 2px var(--green);
}
.tl-period { font-size: 11px; color: var(--green); font-weight: 700; letter-spacing: 0.1em; margin-bottom: 6px; }
.tl-head { font-size: 22px; font-weight: 800; color: var(--navy); margin-bottom: 12px; }
.tl-body { font-size: 15px; color: var(--gray); line-height: 1.8; max-width: 600px; margin-bottom: 20px; }
.tl-photo {
  border-radius: 16px; overflow: hidden;
  height: 260px; max-width: 520px;
  background: linear-gradient(135deg, #e2e8f0, #cbd5e1);
  position: relative;
}
.tl-photo-fallback {
  position: absolute; inset: 0;
  display: flex; flex-direction: column;
  align-items: center; justify-content: center;
  gap: 8px; color: #94a3b8; font-size: 13px;
}
.tl-photo-fallback span { font-size: 36px; }
.tl-quote {
  margin-top: 16px; padding: 14px 20px;
  border-left: 3px solid var(--green); background: var(--green-l);
  border-radius: 0 8px 8px 0; font-size: 14px; color: var(--green-d);
  font-style: italic; line-height: 1.75; max-width: 560px;
}

/* ── BOOK PROPOSAL ── */
#book-proposal { background: var(--navy); color: #fff; }
#book-proposal .sec-label { color: #5DCAA5; }
#book-proposal .sec-title { color: #fff; }
.bp-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 48px; align-items: start; margin-top: 56px; }
.book-mockup {
  border-radius: 20px; overflow: hidden;
  box-shadow: 0 32px 80px rgba(0,0,0,0.5);
  aspect-ratio: 3/4;
  background: linear-gradient(145deg, #1e2d4d, #0d1520);
  padding: 44px 36px;
  display: flex; flex-direction: column; justify-content: space-between;
  position: relative;
}
.book-mockup::before {
  content: ''; position: absolute; inset: 0;
  background: repeating-linear-gradient(0deg, transparent, transparent 56px, rgba(255,255,255,0.02) 56px, rgba(255,255,255,0.02) 57px);
}
.bm-label { font-size: 10px; letter-spacing: 0.2em; color: rgba(255,255,255,0.35); position: relative; z-index:1; }
.bm-title { font-size: 30px; font-weight: 900; color: #fff; line-height: 1.15; letter-spacing: -0.01em; position: relative; z-index:1; }
.bm-title .ba { color: #5DCAA5; }
.bm-sub { font-size: 12px; color: rgba(255,255,255,0.4); margin-top: 10px; line-height: 1.6; position: relative; z-index:1; }
.bm-bar { height: 1px; background: rgba(255,255,255,0.12); position: relative; z-index:1; }
.bm-author { font-size: 18px; font-weight: 700; color: rgba(255,255,255,0.85); position: relative; z-index:1; }
.bm-author-sub { font-size: 11px; color: rgba(255,255,255,0.35); margin-top: 4px; line-height: 1.5; position: relative; z-index:1; }

.bp-details { display: flex; flex-direction: column; gap: 24px; }
.bp-block {
  border: 1px solid rgba(255,255,255,0.08);
  border-radius: 14px; padding: 24px;
  background: rgba(255,255,255,0.04);
}
.bp-block-title { font-size: 13px; font-weight: 700; color: #5DCAA5; margin-bottom: 12px; letter-spacing: 0.06em; }
.bp-block-text { font-size: 14px; color: rgba(255,255,255,0.65); line-height: 1.8; }
.bp-quote {
  font-size: 16px; color: rgba(255,255,255,0.85);
  font-style: italic; line-height: 1.75;
  border-left: 3px solid #5DCAA5; padding-left: 20px;
}

/* ── CHAPTERS ── */
#chapters { background: var(--gray-l); }
.ch-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 16px; }
.ch-card {
  background: #fff; border-radius: 14px; padding: 24px;
  border: 1px solid var(--border);
  transition: box-shadow .2s, transform .2s;
}
.ch-card:hover { box-shadow: 0 8px 32px rgba(0,0,0,0.08); transform: translateY(-2px); }
.ch-part { font-size: 10px; letter-spacing: 0.12em; font-weight: 700; color: var(--green); margin-bottom: 8px; }
.ch-name { font-size: 15px; font-weight: 700; color: var(--navy); margin-bottom: 6px; line-height: 1.35; }
.ch-sub { font-size: 13px; color: var(--gray); margin-bottom: 12px; }
.ch-items { display: flex; flex-direction: column; gap: 5px; }
.ch-item { font-size: 12px; color: #94a3b8; display: flex; align-items: flex-start; gap: 6px; line-height: 1.4; }
.ch-item::before { content: ''; display: block; width: 4px; height: 4px; border-radius: 50%; background: var(--green); flex-shrink: 0; margin-top: 6px; }
.ch-status { display: inline-flex; align-items: center; gap: 4px; font-size: 11px; font-weight: 600; padding: 3px 10px; border-radius: 20px; margin-top: 14px; }
.st-done { background: #dcfce7; color: #15803d; }
.st-wip { background: #fef3c7; color: #92400e; }
.st-plan { background: #f1f5f9; color: #64748b; }

/* ── MEDIA ── */
#media { background: #fff; }
.media-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; }
.media-card {
  border-radius: 14px; overflow: hidden; border: 1px solid var(--border);
}
.media-photo {
  height: 200px;
  background: linear-gradient(135deg, #e2e8f0, #cbd5e1);
  position: relative;
}
.media-photo-fallback {
  position: absolute; inset: 0;
  display: flex; flex-direction: column;
  align-items: center; justify-content: center;
  gap: 6px; color: #94a3b8; font-size: 12px;
}
.media-photo-fallback span { font-size: 28px; }
.media-label { background: #fff; padding: 16px 20px; }
.media-cat { font-size: 10px; letter-spacing: 0.1em; font-weight: 700; color: var(--green); margin-bottom: 4px; }
.media-name { font-size: 14px; font-weight: 700; color: var(--navy); margin-bottom: 4px; line-height: 1.35; }
.media-desc { font-size: 12px; color: var(--gray); line-height: 1.5; }

/* ── VALUES ── */
#values { background: var(--green); }
.val-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; }
.val-card { background: rgba(255,255,255,0.1); border-radius: 16px; padding: 32px; border: 1px solid rgba(255,255,255,0.15); }
.val-icon { font-size: 28px; margin-bottom: 16px; }
.val-title { font-size: 18px; font-weight: 800; color: #fff; margin-bottom: 10px; }
.val-body { font-size: 14px; color: rgba(255,255,255,0.75); line-height: 1.8; }
#values .sec-label { color: rgba(255,255,255,0.7); }
#values .sec-title { color: #fff; }

/* ── VISION ── */
#vision { background: var(--gray-l); }
.vis-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; }
.vis-card {
  background: #fff; border-radius: 16px; padding: 32px;
  border: 1px solid var(--border); position: relative; overflow: hidden;
}
.vis-bar { position: absolute; top: 0; left: 0; right: 0; height: 4px; }
.v1 .vis-bar { background: var(--green); }
.v2 .vis-bar { background: #2563eb; }
.v3 .vis-bar { background: var(--gold); }
.vis-num { font-size: 11px; font-weight: 700; letter-spacing: 0.12em; margin-bottom: 14px; }
.v1 .vis-num { color: var(--green); }
.v2 .vis-num { color: #2563eb; }
.v3 .vis-num { color: var(--gold); }
.vis-icon { font-size: 28px; margin-bottom: 14px; }
.vis-title { font-size: 17px; font-weight: 700; color: var(--navy); line-height: 1.35; margin-bottom: 10px; }
.vis-body { font-size: 14px; color: var(--gray); line-height: 1.8; }

/* ── AUDIENCE ── */
#audience { background: #fff; }
.aud-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 16px; }
.aud-card { background: var(--gray-l); border-radius: 14px; padding: 24px; text-align: center; }
.aud-icon { font-size: 32px; margin-bottom: 14px; }
.aud-title { font-size: 14px; font-weight: 700; color: var(--navy); margin-bottom: 8px; }
.aud-body { font-size: 13px; color: var(--gray); line-height: 1.65; }

/* ── PUBLISHING PITCH ── */
#pitch { background: var(--navy); color: #fff; }
#pitch .sec-label { color: #5DCAA5; }
#pitch .sec-title { color: #fff; }
.pitch-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin-top: 48px; }
.pitch-card {
  border: 1px solid rgba(255,255,255,0.08);
  border-radius: 14px; padding: 28px;
  background: rgba(255,255,255,0.04);
}
.pitch-card-num { font-size: 32px; font-weight: 900; color: rgba(29,158,117,0.25); line-height: 1; margin-bottom: 12px; }
.pitch-card-title { font-size: 16px; font-weight: 700; color: #fff; margin-bottom: 10px; }
.pitch-card-body { font-size: 14px; color: rgba(255,255,255,0.6); line-height: 1.8; }
.pitch-cta {
  margin-top: 48px; text-align: center;
  padding: 40px; border: 1px dashed rgba(255,255,255,0.15);
  border-radius: 20px;
}
.pitch-cta-title { font-size: 22px; font-weight: 800; color: #fff; margin-bottom: 12px; }
.pitch-cta-body { font-size: 15px; color: rgba(255,255,255,0.55); line-height: 1.8; }

/* ── FOOTER ── */
footer { background: #0d1520; padding: 56px 0 40px; text-align: center; }
.footer-logo { font-size: 18px; font-weight: 900; color: #fff; margin-bottom: 6px; }
.footer-logo em { color: #5DCAA5; font-style: normal; }
.footer-sub { font-size: 13px; color: rgba(255,255,255,0.3); margin-bottom: 32px; line-height: 1.7; }
.footer-contact { font-size: 13px; color: rgba(255,255,255,0.25); }
.footer-copy { font-size: 12px; color: rgba(255,255,255,0.15); margin-top: 28px; }

/* ── ANIMATIONS ── */
.reveal { opacity: 0; transform: translateY(28px); transition: opacity .7s ease, transform .7s ease; }
.reveal.in { opacity: 1; transform: none; }
.reveal-d1 { transition-delay: .1s; }
.reveal-d2 { transition-delay: .2s; }
.reveal-d3 { transition-delay: .3s; }

/* ── RESPONSIVE ── */
@media (max-width: 900px) {
  #cover { grid-template-columns: 1fr; }
  .cover-right { height: 50vw; }
  .author-layout, .bp-grid, .ch-grid, .media-grid, .val-grid, .vis-grid, .aud-grid, .pitch-grid { grid-template-columns: 1fr; }
  .cover-left { padding: 60px 32px; }
  nav { padding: 0 24px; }
  .nav-links { display: none; }
  .container { padding: 0 24px; }
}
</style>
</head>
<body>

<!-- ── NAV ── -->
<nav>
  <div class="nav-brand">황명구 <em>·</em> HMG</div>
  <ul class="nav-links">
    <li><a href="#author">저자 소개</a></li>
    <li><a href="#journey">삶의 여정</a></li>
    <li><a href="#book-proposal">책 소개</a></li>
    <li><a href="#chapters">목차</a></li>
    <li><a href="#media">미디어</a></li>
    <li><a href="#vision">비전</a></li>
    <li><a href="#pitch">출판 제안</a></li>
  </ul>
  <div class="nav-badge">출판사 제안서</div>
</nav>

<!-- ── COVER ── -->
<section id="cover">
  <div class="cover-left">
    <div class="cover-left-inner">
      <div class="cover-proposal-tag">
        ✦ BOOK PROPOSAL &nbsp;·&nbsp; 출판 제안서
      </div>
      <h1 class="cover-book-title">
        그라운드<br>밖의<br><span class="accent">리더십</span>
      </h1>
      <p class="cover-book-sub">
        축구선수에서 정책전문가까지,<br>한 사람의 전환과 확장의 기록
      </p>
      <div class="cover-divider"></div>
      <div class="cover-author-name">황명구 지음</div>
      <div class="cover-author-roles">
        프로축구선수 · 축구지도자 · 대학 행정가<br>
        정책전문가 · 전략전문가 · 이학박사
      </div>
    </div>
    <div class="cover-dots">
      <div class="dot active"></div>
      <div class="dot"></div>
      <div class="dot"></div>
      <div class="dot"></div>
      <div class="dot"></div>
    </div>
  </div>
  <div class="cover-right">
    <div class="cover-photo">
      <!-- 이미지: images/01_profile_main.jpg -->
      <img src="images/01_profile_main.jpg" alt="황명구 프로필" onerror="this.style.display='none'">
    </div>
    <div class="cover-photo-overlay"></div>
    <div class="cover-photo-label">
      <div class="lname">황명구</div>
      <div class="ltag">HWANG MYOUNG GOO</div>
    </div>
  </div>
</section>

<!-- ── AUTHOR PROFILE ── -->
<section id="author" class="section">
  <div class="container">
    <div class="sec-label reveal">저자 소개</div>
    <div class="author-layout">
      <div class="reveal reveal-d1">
        <div class="author-photo-wrap">
          <!-- 이미지: images/02_profile_smile.jpg -->
          <img src="images/02_profile_smile.jpg" alt="황명구 프로필 사진" onerror="this.style.display='none'">
          <div class="author-photo-fallback">황</div>
        </div>
      </div>
      <div class="author-right">
        <div class="sec-label reveal">황명구 — Hwang Myung-gu</div>
        <h2 class="sec-title reveal">현장성과 학문성,<br>실행력과 전략을 겸비한<br>융합형 전문 리더</h2>
        <p class="author-desc reveal">
          황명구는 프로축구선수 출신의 현장형 리더이자, 선수와 지도자 경험을 바탕으로
          대학 행정, 정책, 전략, 지역협력, ESG 분야로 전문성을 확장해 온 융합형 실천 전문가이다.
        </p>
        <p class="author-desc reveal">
          경북 울진에서 출생하여 서울 도림초·영도중학교, 충북 청주상업고등학교를 거쳐 충남대학교에 진학하였다.
          부산 대우로얄즈 프로축구단에서 선수 생활 후 대전 봉산중학교 신생팀 지도자를 맡아
          대전 대표로 소년체전에 참가하는 성과를 거두었다.
          이후 충남대학교에서 27년간 학생지도, 취업지원, 창업지원, 지역협력, ESG 업무를 수행하였다.
        </p>
        <p class="author-desc reveal">
          한남대학교 교육학 석사, 충남대학교 이학박사를 취득하고 카이스트 지식재산전략 최고위과정을 수료하였으며,
          행정사 및 스포츠전문지도사 자격을 갖추어 학문적 기반과 제도적 전문성을 함께 완성하였다.
        </p>
        <div class="author-cred-grid">
          <div class="cred reveal reveal-d1">
            <div class="cred-label">학위</div>
            <div class="cred-val">이학박사 (충남대)<br>교육학 석사 (한남대)</div>
          </div>
          <div class="cred reveal reveal-d2">
            <div class="cred-label">자격</div>
            <div class="cred-val">행정사<br>스포츠전문지도사</div>
          </div>
          <div class="cred reveal reveal-d1">
            <div class="cred-label">선수 경력</div>
            <div class="cred-val">대우로얄즈 프로축구단</div>
          </div>
          <div class="cred reveal reveal-d2">
            <div class="cred-label">행정 경력</div>
            <div class="cred-val">충남대학교 27년 재직<br>ESG센터 · 취업·창업지원</div>
          </div>
          <div class="cred reveal reveal-d1">
            <div class="cred-label">연수 과정</div>
            <div class="cred-val">카이스트 지식재산전략<br>최고위과정</div>
          </div>
          <div class="cred reveal reveal-d2">
            <div class="cred-label">대외 활동</div>
            <div class="cred-val">대전교도소 교정위원<br>ESG·지역협력 전문가</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ── JOURNEY ── -->
<section id="journey" class="section">
  <div class="container">
    <div class="sec-label reveal">삶의 여정</div>
    <h2 class="sec-title reveal">내 삶은 왜 늘<br>새로운 운동장을 향해 갔는가</h2>
    <p class="sec-body reveal" style="margin-bottom: 60px;">
      멈춤은 끝이 아니라 전환이었다. 운동장에서 시작된 여정은 지도자의 현장으로,
      대학과 지역의 현장으로, 그리고 학문과 전략의 영역으로 끊임없이 확장되어 왔다.
    </p>

    <div class="tl-wrap">

      <div class="tl-item reveal">
        <div class="tl-dot"></div>
        <div class="tl-period">프로선수 시절 · 부산 대우로얄즈</div>
        <div class="tl-head">축구, 첫 번째 인생의 무대</div>
        <p class="tl-body">
          충남대학교 졸업 후 부산 대우로얄즈 프로축구단에 입단, 선수의 길을 걸었다.
          팀을 위한 헌신과 경쟁 속에서 버티는 힘을 온몸으로 익혔다.
          뜻하지 않은 부상이 선수 생활을 멈추게 하였고, 인생의 첫 번째 전환점이 찾아왔다.
        </p>
        <div class="photo-duo">
          <div class="tl-photo" style="height:200px">
            <!-- 이미지: images/08_ball_front.jpg (대우로얄즈 사인 공 앞면) -->
            <img src="images/08_ball_front.jpg" alt="대우로얄즈 사인 축구공" onerror="this.style.display='none'">
            <div class="tl-photo-fallback"><span>⚽</span>팀 사인 기념 축구공</div>
          </div>
          <div class="tl-photo" style="height:200px">
            <!-- 이미지: images/09_ball_back.jpg (사인 공 뒷면 — 황명구 서명) -->
            <img src="images/09_ball_back.jpg" alt="황명구 서명이 담긴 대우로얄즈 공" onerror="this.style.display='none'">
            <div class="tl-photo-fallback"><span>✍️</span>황명구 친필 사인 — 대우로얄즈 기념구</div>
          </div>
        </div>
        <div class="tl-quote">
          "많은 사람은 멈춤을 실패라고 여긴다. 하지만 내게 멈춤은 끝이 아니라 전환이었다."
        </div>
      </div>

      <div class="tl-item reveal">
        <div class="tl-dot"></div>
        <div class="tl-period">지도자 시절 · 대전 봉산중학교</div>
        <div class="tl-head">사람을 키우는 사람</div>
        <p class="tl-body">
          선수에서 지도자로 전환하여 대전 봉산중학교 신생 축구팀을 맡았다.
          대전 대표로 소년체전에 참가하는 성과를 거두며 지도자로서 역량을 인정받았다.
          직접 뛰는 것보다 누군가가 더 잘 뛸 수 있도록 돕는 일이 더 깊은 책임임을 처음 깨달은 시기였다.
        </p>
        <div class="tl-photo">
          <!-- 이미지: images/04_coaching.JPG (봉산중 헹가래 사진) -->
          <img src="images/04_coaching.JPG" alt="봉산중학교 축구팀 헹가래 사진" onerror="this.style.display='none'">
          <div class="tl-photo-fallback">
            <span>🏃</span>
            봉산중학교 축구팀 · 소년체전 대전 대표
          </div>
        </div>
        <div class="tl-quote">
          "선수로 뛸 때는 나 자신을 훈련했다. 지도자가 된 뒤에는 사람을 키우는 법을 배웠다."
        </div>
      </div>

      <div class="tl-item reveal">
        <div class="tl-dot"></div>
        <div class="tl-period">대학 행정 · 충남대학교 27년</div>
        <div class="tl-head">대학과 지역을 잇다 — 27년의 현장</div>
        <p class="tl-body">
          충남대학교 교직원으로 이직한 뒤 학생지도, 취업·창업지원, 지역협력, ESG 업무에 이르기까지
          대학 행정의 전 영역에서 27년간 실무 경험을 축적하였다.
          정부 재정지원사업, 청년 인재양성 사업, 지자체 협력사업, 공공가치 기반 프로젝트를 기획·운영하였다.
        </p>
        <div class="tl-quote">
          "진짜 변화는 현장을 모르는 사람이 아니라, 현장에서 사람을 만나고 문제를 이해한 사람이 만들 수 있다."
        </div>
      </div>

      <div class="tl-item reveal">
        <div class="tl-dot"></div>
        <div class="tl-period">학문 · 석사 → 박사 취득</div>
        <div class="tl-head">현장 위에 학문을 쌓다</div>
        <p class="tl-body">
          현장 경험에 머물지 않고 한남대학교 교육학 석사, 충남대학교 이학박사를 취득하고
          카이스트 지식재산전략 최고위과정을 수료하였다.
          행정사·스포츠전문지도사 자격도 갖추며 학문적 기반과 제도적 전문성을 함께 완성하였다.
        </p>
        <div class="tl-photo" style="height:280px; max-width:220px; border-radius:16px; overflow:hidden; margin-top:20px; position:relative; background:linear-gradient(135deg,#e2e8f0,#cbd5e1)">
          <!-- 이미지: images/10_graduation.PNG (박사 학위 수여식) -->
          <img src="images/10_graduation.PNG" alt="박사 학위 수여식" onerror="this.style.display='none'" style="width:100%;height:100%;object-fit:cover;object-position:center top">
          <div style="position:absolute;inset:0;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:8px;color:#94a3b8;font-size:13px">
            <span style="font-size:36px">🎓</span>박사 학위 수여식
          </div>
        </div>
        <div class="tl-quote" style="margin-top:20px">
          "그것은 스펙을 쌓기 위한 과정이 아니었다. 현장을 더 정확히 이해하고 사람과 조직, 정책과 지역을 더 효과적으로 연결하기 위한 또 하나의 훈련이었다."
        </div>
      </div>

    </div>
  </div>
</section>

<!-- ── BOOK PROPOSAL ── -->
<section id="book-proposal" class="section">
  <div class="container">
    <div class="sec-label reveal">출판 제안 도서</div>
    <h2 class="sec-title reveal">그라운드 밖의 리더십</h2>
    <div class="bp-grid">
      <div class="reveal reveal-d1">
        <div class="book-mockup">
          <div>
            <div class="bm-label">HWANG MYOUNG GOO · 황명구</div>
          </div>
          <div>
            <div class="bm-title">그라운드<br>밖의<br><span class="ba">리더십</span></div>
            <div class="bm-sub">축구선수에서 정책전문가까지,<br>한 사람의 전환과 확장의 기록</div>
          </div>
          <div>
            <div class="bm-bar"></div>
            <div style="height:16px"></div>
            <div class="bm-author">황명구 지음</div>
            <div class="bm-author-sub">현장 리더십 · 학문적 리더십 · 공공적 실행력<br>융합형 전문 리더</div>
          </div>
        </div>
      </div>
      <div class="bp-details">
        <div class="bp-block reveal">
          <div class="bp-block-title">✦ 책의 핵심 메시지</div>
          <div class="bp-quote">
            "운동장에서 배운 실행력, 사람을 키우며 익힌 리더십, 학문과 자격으로 완성한 전문성.
            한 사람의 삶은 결국 사람과 조직, 대학과 지역을 연결하는 길이 되었다."
          </div>
        </div>
        <div class="bp-block reveal reveal-d1">
          <div class="bp-block-title">📖 책의 성격</div>
          <div class="bp-block-text">
            이 책은 한 사람의 경력을 나열한 기록이 아니다.
            현장과 학문, 실천과 성찰, 개인의 도전과 공동체의 책임이 만나
            하나의 삶을 이루어 온 과정에 대한 이야기이다.
            전환은 끝이 아니라 확장임을 보여주는 실천형 리더의 성장 서사.
          </div>
        </div>
        <div class="bp-block reveal reveal-d2">
          <div class="bp-block-title">📊 도서 정보</div>
          <div class="bp-block-text">
            분류: 자서전 · 에세이 · 리더십<br>
            구성: 프롤로그 + 5부 16장 + 에필로그<br>
            예상 분량: 약 280~320페이지<br>
            상태: 집필 및 편집 진행중
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ── CHAPTERS ── -->
<section id="chapters" class="section">
  <div class="container">
    <div class="sec-label reveal">목차 구성</div>
    <h2 class="sec-title reveal">5부 16장의 여정</h2>
    <p class="sec-body reveal" style="margin-bottom: 48px;">
      프롤로그부터 에필로그까지 — 한 사람의 전환과 확장의 이야기를 시간의 흐름과 주제의 깊이로 구성하였다.
    </p>
    <div class="ch-grid">
      <div class="ch-card reveal">
        <div class="ch-part">프롤로그</div>
        <div class="ch-name">내 삶은 왜 늘 새로운 운동장을 향해 갔는가</div>
        <div class="ch-sub">삶의 방향성과 핵심 메시지</div>
        <span class="ch-status st-done">✓ 완료</span>
      </div>
      <div class="ch-card reveal reveal-d1">
        <div class="ch-part">제1부 · 1~3장</div>
        <div class="ch-name">뿌리와 꿈</div>
        <div class="ch-sub">울진, 서울, 청주, 대전으로 이어진 성장기</div>
        <div class="ch-items">
          <span class="ch-item">1장. 울진, 삶의 기초를 배우다</span>
          <span class="ch-item">2장. 서울에서 세상을 넓히다</span>
          <span class="ch-item">3장. 청주에서 현실을, 대전에서 꿈을</span>
        </div>
        <span class="ch-status st-wip">✏ 집필중</span>
      </div>
      <div class="ch-card reveal reveal-d2">
        <div class="ch-part">제2부 · 4~6장</div>
        <div class="ch-name">축구, 첫 번째 인생의 무대</div>
        <div class="ch-sub">대우로얄즈 입단부터 전환점까지</div>
        <div class="ch-items">
          <span class="ch-item">4장. 선수의 길, 충남대에서 대우로얄즈까지</span>
          <span class="ch-item">5장. 프로의 세계 — 부산에서 배운 것들</span>
          <span class="ch-item">6장. 멈춤이 전환이 되다</span>
        </div>
        <span class="ch-status st-wip">✏ 집필중</span>
      </div>
      <div class="ch-card reveal">
        <div class="ch-part">제3부 · 7~9장</div>
        <div class="ch-name">사람을 키우는 사람</div>
        <div class="ch-sub">봉산중학교 지도자 시절과 현장 리더십</div>
        <div class="ch-items">
          <span class="ch-item">7장. 지도자의 길로 들어서다</span>
          <span class="ch-item">8장. 봉산중, 0에서 시작한 팀 만들기</span>
          <span class="ch-item">9장. 직접 뛰는 것보다 어려운 것</span>
        </div>
        <span class="ch-status st-plan">○ 예정</span>
      </div>
      <div class="ch-card reveal reveal-d1">
        <div class="ch-part">제4부 · 10~13장</div>
        <div class="ch-name">대학과 지역을 잇다</div>
        <div class="ch-sub">충남대 27년, ESG, 정책, 지역협력</div>
        <div class="ch-items">
          <span class="ch-item">10장. 충남대, 새로운 운동장</span>
          <span class="ch-item">11장. 학생을 키우고 지역을 연결하다</span>
          <span class="ch-item">12장. ESG와 공공가치의 실행</span>
          <span class="ch-item">13장. 정책을 현장으로 가져오다</span>
        </div>
        <span class="ch-status st-plan">○ 예정</span>
      </div>
      <div class="ch-card reveal reveal-d2">
        <div class="ch-part">제5부 · 14~16장 + 에필로그</div>
        <div class="ch-name">그라운드 밖에서도 나는 뛰었다</div>
        <div class="ch-sub">학문적 심화, 미래 비전, 다음 장으로</div>
        <div class="ch-items">
          <span class="ch-item">14장. 석박사, 현장을 학문으로 다듬다</span>
          <span class="ch-item">15장. 융합형 리더의 완성</span>
          <span class="ch-item">16장. 사람·지역·대학·미래를 잇다</span>
          <span class="ch-item">에필로그. 내 삶의 다음 장</span>
        </div>
        <span class="ch-status st-plan">○ 예정</span>
      </div>
    </div>
  </div>
</section>

<!-- ── MEDIA ── -->
<section id="media" class="section">
  <div class="container">
    <div class="sec-label reveal">미디어 · 활동 · 강연</div>
    <h2 class="sec-title reveal">현장이 검증한<br>전문가의 기록</h2>
    <p class="sec-body reveal" style="margin-bottom: 48px;">
      MBC 방송 출연부터 대전 ESG 포럼 발표까지 — 황명구의 전문성은 이미 공공의 장에서 검증되어 왔다.
    </p>
    <div class="media-grid">
      <div class="media-card reveal">
        <div class="media-photo">
          <!-- 이미지: images/07_mbc.JPG (MBC 방송 출연) -->
          <img src="images/07_mbc.JPG" alt="MBC 방송 출연 — 황명구 취업지원팀장 충남대학교" onerror="this.style.display='none'">
          <div class="media-photo-fallback">
            <span>📺</span>
            MBC 방송 출연
          </div>
        </div>
        <div class="media-label">
          <div class="media-cat">TV 출연 · MBC</div>
          <div class="media-name">MBC 뉴스 — 취업지원 전문가 패널</div>
          <div class="media-desc">충남대학교 취업지원팀장으로 청년 취업 문제를 논한 MBC 방송 패널 출연</div>
        </div>
      </div>
      <div class="media-card reveal reveal-d1">
        <div class="media-photo">
          <!-- 이미지: images/05_esg_speech.jpg (ESG 포럼 발표) -->
          <img src="images/05_esg_speech.jpg" alt="2025 대전 SDGs-ESG 경영포럼 발표" onerror="this.style.display='none'">
          <div class="media-photo-fallback">
            <span>🎤</span>
            ESG 포럼 발표
          </div>
        </div>
        <div class="media-label">
          <div class="media-cat">강연 · 2025 대전 ESG 포럼</div>
          <div class="media-name">2025 대전 SDGs-ESG 경영포럼 발표</div>
          <div class="media-desc">대전컨벤션센터(DCC) — 지속가능한 지역발전 전략 주제 발표</div>
        </div>
      </div>
      <div class="media-card reveal reveal-d2">
        <div class="media-photo">
          <!-- 이미지: images/06_esg_panel.jpg (ESG 패널 토론) -->
          <img src="images/06_esg_panel.jpg" alt="ESG 포럼 패널 토론" onerror="this.style.display='none'">
          <div class="media-photo-fallback">
            <span>💬</span>
            ESG 패널 토론
          </div>
        </div>
        <div class="media-label">
          <div class="media-cat">토론 · 2025 대전 ESG 포럼</div>
          <div class="media-name">ESG 실천과 혁신을 잇다 — 패널 토론</div>
          <div class="media-desc">대학·지역협력·공공성 기반 ESG 전략을 주제로 한 패널 토론 참여</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ── VALUES ── -->
<section id="values" class="section">
  <div class="container">
    <div class="sec-label reveal">핵심 가치와 철학</div>
    <h2 class="sec-title reveal" style="color:#fff">현장 · 사람 · 연결<br>세 가지 기둥</h2>
    <p class="sec-body reveal" style="margin-bottom: 48px; color:rgba(255,255,255,0.7)">
      황명구의 삶 전반에 흐르는 세 가지 원칙. 이 세 가지는 분리되지 않고 하나로 연결되어 가치를 만들어 낸다.
    </p>
    <div class="val-grid">
      <div class="val-card reveal">
        <div class="val-icon">🏟</div>
        <div class="val-title">현장이 먼저다</div>
        <div class="val-body">
          책상 위 전략보다 실제 현장에서의 검증과 소통이 최우선이다.
          선수 시절부터 체득한 실행 중심의 가치관이 모든 의사결정의 기초가 되었다.
          현장을 모르면 전략은 공허하고, 실행을 모르면 정책은 멈춘다.
        </div>
      </div>
      <div class="val-card reveal reveal-d1">
        <div class="val-icon">🤝</div>
        <div class="val-title">사람이 전략이다</div>
        <div class="val-body">
          신뢰와 공감을 바탕으로 한 인간관계가 모든 실행의 출발점이다.
          진짜 변화는 현장에서 사람을 만나고 문제를 이해한 사람이 만들 수 있다.
          그것이 선수에서 지도자로, 행정가에서 전략가로 이어진 이유이다.
        </div>
      </div>
      <div class="val-card reveal reveal-d2">
        <div class="val-icon">🔗</div>
        <div class="val-title">연결이 가치다</div>
        <div class="val-body">
          개별 전문성이 서로 연결되고 융합될 때 비로소 가치가 완성된다.
          스포츠와 행정, 학문과 정책, 대학과 지역 — 이 모든 경계를 넘나드는
          연결이 황명구의 가장 독보적인 역량이다.
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ── VISION ── -->
<section id="vision" class="section">
  <div class="container">
    <div class="sec-label reveal">3대 미래 비전</div>
    <h2 class="sec-title reveal">사람 · 플랫폼 · 리더십<br>다음 운동장을 향해</h2>
    <p class="sec-body reveal" style="margin-bottom: 48px;">
      황명구의 미래는 세 가지 방향을 향해 있다. 이 비전들은 이 책에서 그 씨앗을 찾을 수 있다.
    </p>
    <div class="vis-grid">
      <div class="vis-card v1 reveal">
        <div class="vis-bar"></div>
        <div class="vis-num">비전 01</div>
        <div class="vis-icon">🌱</div>
        <div class="vis-title">사람을 키우는 생태계 설계</div>
        <div class="vis-body">청년들이 지역 내에서 기회를 발견하고 성장할 수 있는 구조를 설계한다. 대학·지역·청년이 연결되는 생태계.</div>
      </div>
      <div class="vis-card v2 reveal reveal-d1">
        <div class="vis-bar"></div>
        <div class="vis-num">비전 02</div>
        <div class="vis-icon">🏛</div>
        <div class="vis-title">대학–지역 협력 플랫폼 구축</div>
        <div class="vis-body">현장과 정책을 유기적으로 잇는 지속가능한 연결망을 구축한다. 대학과 지역의 상생 모델을 실천한다.</div>
      </div>
      <div class="vis-card v3 reveal reveal-d2">
        <div class="vis-bar"></div>
        <div class="vis-num">비전 03</div>
        <div class="vis-icon">⚖️</div>
        <div class="vis-title">공공성 기반 전략 리더십 (ESG)</div>
        <div class="vis-body">ESG와 정책이 현장에서 실제로 실행되는 전략을 리드한다. 공공적 가치와 지속가능성이 핵심이다.</div>
      </div>
    </div>
  </div>
</section>

<!-- ── AUDIENCE ── -->
<section id="audience" class="section">
  <div class="container">
    <div class="sec-label reveal">독자 대상</div>
    <h2 class="sec-title reveal">이 책이 닿아야 할<br>네 가지 독자층</h2>
    <div class="aud-grid" style="margin-top:48px">
      <div class="aud-card reveal">
        <div class="aud-icon">🧑‍💼</div>
        <div class="aud-title">전직·전환을 고민하는<br>직장인·전문가</div>
        <div class="aud-body">경력 전환과 재도전을 앞두고 방향을 찾는 모든 이들에게 실제적 나침반이 되는 책</div>
      </div>
      <div class="aud-card reveal reveal-d1">
        <div class="aud-icon">🎓</div>
        <div class="aud-title">대학·지역협력·공공행정<br>분야 관계자</div>
        <div class="aud-body">대학 행정, ESG, 지역 거버넌스, 청년정책 실무자에게 실전 인사이트를 제공</div>
      </div>
      <div class="aud-card reveal reveal-d2">
        <div class="aud-icon">🌱</div>
        <div class="aud-title">성장과 가능성을<br>찾는 청년·학생</div>
        <div class="aud-body">스포츠에서 시작해 다양한 영역으로 확장한 삶에서 자신의 가능성을 발견하는 독자</div>
      </div>
      <div class="aud-card reveal reveal-d3">
        <div class="aud-icon">📋</div>
        <div class="aud-title">리더십·조직·전략에<br>관심 있는 독자</div>
        <div class="aud-body">현장 중심 리더십과 융합형 전문성이 어떻게 완성되는지 배우고자 하는 독자</div>
      </div>
    </div>
  </div>
</section>

<!-- ── PITCH ── -->
<section id="pitch" class="section">
  <div class="container">
    <div class="sec-label reveal">출판사 제안 포인트</div>
    <h2 class="sec-title reveal">왜 지금, 왜 이 책인가</h2>
    <p class="sec-body reveal" style="margin-bottom: 0; color: rgba(255,255,255,0.6)">
      이 책은 시대가 요구하는 융합형 리더십의 실제 사례이자, 전환의 시대를 사는 독자들에게 가장 실천적인 메시지를 전달하는 자서전이다.
    </p>
    <div class="pitch-grid">
      <div class="pitch-card reveal">
        <div class="pitch-card-num">01</div>
        <div class="pitch-card-title">독보적인 스토리라인</div>
        <div class="pitch-card-body">
          프로축구선수 → 지도자 → 대학 행정가 → 박사 → ESG·전략전문가로 이어지는 전환의 여정은
          어떤 자서전에서도 볼 수 없는 독창적인 서사다. 스포츠 독자와 경영·행정 독자를 동시에 포괄한다.
        </div>
      </div>
      <div class="pitch-card reveal reveal-d1">
        <div class="pitch-card-num">02</div>
        <div class="pitch-card-title">검증된 저자 공신력</div>
        <div class="pitch-card-body">
          MBC 방송 패널 출연, 대전 ESG 포럼 발표, 충남대 27년 재직, 이학박사 학위, 카이스트 최고위과정 수료 —
          이미 공공의 장에서 전문성이 검증된 저자이다.
        </div>
      </div>
      <div class="pitch-card reveal">
        <div class="pitch-card-num">03</div>
        <div class="pitch-card-title">전환의 시대에 맞는 메시지</div>
        <div class="pitch-card-body">
          경력 전환, 평생학습, 융합형 인재에 대한 사회적 수요가 급증하는 시대에
          실제 삶으로 이를 실천한 인물의 이야기는 강력한 공감대를 형성한다.
        </div>
      </div>
      <div class="pitch-card reveal reveal-d1">
        <div class="pitch-card-num">04</div>
        <div class="pitch-card-title">지역·대학·ESG 시장 연계</div>
        <div class="pitch-card-body">
          대학 행정, 지역협력, ESG 경영이라는 현재 가장 주목받는 세 분야를 모두 아우르며
          강연·워크숍·정책 분야와의 연계 마케팅이 용이하다.
        </div>
      </div>
    </div>
    <div class="pitch-cta reveal">
      <div class="pitch-cta-title">현장을 아는 사람만이 실행 가능한 전략을 만든다</div>
      <div class="pitch-cta-body">
        축구선수에서 정책전문가까지 — 이 책은 한 사람의 경력이 아니라,<br>
        사람과 조직, 대학과 지역, 정책과 실행을 연결해 온 삶의 실천적 기록이다.
      </div>
    </div>
  </div>
</section>

<!-- ── FOOTER ── -->
<footer>
  <div class="container">
    <div class="footer-logo">황명구 <em>·</em> HMG</div>
    <div class="footer-sub">
      그라운드 밖의 리더십 — 출판 제안서<br>
      현장 리더십 · 학문적 리더십 · 공공적 실행력
    </div>
    <div class="footer-contact">출판 문의 · 강연 요청 · 저작권 관련 연락처 추후 업데이트</div>
    <div class="footer-copy">© 2025 황명구. All rights reserved.</div>
  </div>
</footer>

<script>
// Scroll reveal
const revealObserver = new IntersectionObserver((entries) => {
  entries.forEach((entry) => {
    if (entry.isIntersecting) {
      entry.target.classList.add('in');
      revealObserver.unobserve(entry.target);
    }
  });
}, { threshold: 0.12 });
document.querySelectorAll('.reveal').forEach(el => revealObserver.observe(el));

// Nav highlight
const sections = document.querySelectorAll('section[id]');
const navAs = document.querySelectorAll('.nav-links a');
window.addEventListener('scroll', () => {
  let cur = '';
  sections.forEach(s => { if (window.scrollY >= s.offsetTop - 80) cur = s.id; });
  navAs.forEach(a => {
    const active = a.getAttribute('href') === '#' + cur;
    a.style.color = active ? '#1D9E75' : '';
    a.style.fontWeight = active ? '600' : '';
  });
}, { passive: true });
</script>
</body>
</html>
