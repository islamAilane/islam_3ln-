<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>islam_3LN | بوابة المونتاج والدروس الاحترافية</title>
  <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;900&family=Tajawal:wght@400;700;900&display=swap" rel="stylesheet">
  <style>
    :root {
      --red: #E8001D;
      --red-glow: rgba(232,0,29,0.35);
      --red-soft: rgba(232,0,29,0.08);
      --black: #060606;
      --card: #101010;
      --card-hover: #151515;
      --border: #1f1f1f;
      --border-soft: #181818;
      --white: #FFFFFF;
      --dim: #777;
      --dim2: #444;
    }

    *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }
    html { scroll-behavior: smooth; }

    body {
      background: var(--black);
      color: var(--white);
      font-family: 'Cairo', sans-serif;
      overflow-x: hidden;
      min-height: 100vh;
    }

    body::after {
      content: '';
      position: fixed; inset: 0;
      background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 512 512' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='g'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.75' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23g)' opacity='0.035'/%3E%3C/svg%3E");
      pointer-events: none;
      z-index: 9000;
    }

    /* ── HEADER ── */
    header {
      padding: 0 5%;
      height: 68px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: rgba(6,6,6,0.94);
      backdrop-filter: blur(16px);
      -webkit-backdrop-filter: blur(16px);
      position: sticky;
      top: 0;
      z-index: 500;
      border-bottom: 1px solid var(--border);
    }

    .logo-area {
      display: flex;
      align-items: center;
      gap: 13px;
      text-decoration: none;
    }

    /* SVG logo mark */
    .logo-mark {
      position: relative;
      width: 46px; height: 46px;
      flex-shrink: 0;
    }
    .logo-mark .ring {
      position: absolute; inset: 0;
      animation: spin 10s linear infinite;
    }
    .logo-inner {
      position: absolute;
      inset: 5px;
      background: #ffffff;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .logo-inner span {
      font-family: 'Tajawal', sans-serif;
      font-size: 0.7rem;
      font-weight: 900;
      color: #000;
      letter-spacing: 0.5px;
      line-height: 1;
      user-select: none;
    }
    @keyframes spin { to { transform: rotate(360deg); } }

    .brand-text { display: flex; flex-direction: column; line-height: 1.1; }
    .brand-main {
      font-family: 'Tajawal', sans-serif;
      font-size: 1.18rem; font-weight: 900;
      color: var(--white); letter-spacing: 0.5px;
    }
    .brand-main em { font-style: normal; color: var(--red); }
    .brand-sub { font-size: 0.67rem; color: var(--dim); font-weight: 400; }

    .header-nav { display: flex; align-items: center; gap: 20px; }
    .nav-link {
      color: var(--dim); text-decoration: none;
      font-size: 0.85rem; font-weight: 600;
      transition: color 0.2s; position: relative;
    }
    .nav-link::after {
      content: ''; position: absolute;
      bottom: -3px; right: 0;
      width: 0; height: 2px;
      background: var(--red); transition: width 0.25s;
    }
    .nav-link:hover { color: var(--white); }
    .nav-link:hover::after { width: 100%; }
    .nav-btn {
      padding: 8px 18px;
      background: var(--red); color: white;
      text-decoration: none; border-radius: 8px;
      font-size: 0.82rem; font-weight: 700;
      transition: 0.2s; display: inline-flex; align-items: center; gap: 6px;
    }
    .nav-btn:hover { background: #ff1a35; transform: translateY(-1px); }

    /* ── HERO ── */
    .hero {
      min-height: 540px;
      display: flex; align-items: center; justify-content: center;
      flex-direction: column; text-align: center;
      padding: 90px 8% 70px;
      position: relative; overflow: hidden;
    }
    .hero-bg {
      position: absolute; inset: 0;
      background:
        radial-gradient(ellipse 90% 55% at 50% -5%, rgba(232,0,29,0.16) 0%, transparent 65%),
        radial-gradient(ellipse 50% 50% at 85% 90%, rgba(232,0,29,0.04) 0%, transparent 55%);
    }
    .hero-grid {
      position: absolute; inset: 0;
      background-image:
        linear-gradient(rgba(255,255,255,0.022) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,0.022) 1px, transparent 1px);
      background-size: 55px 55px;
      -webkit-mask-image: radial-gradient(ellipse 85% 85% at 50% 50%, black 10%, transparent 100%);
      mask-image: radial-gradient(ellipse 85% 85% at 50% 50%, black 10%, transparent 100%);
    }
    .hero-badge {
      display: inline-flex; align-items: center; gap: 9px;
      background: var(--red-soft);
      border: 1px solid rgba(232,0,29,0.28);
      color: #ff6070; padding: 7px 20px; border-radius: 50px;
      font-size: 0.8rem; font-weight: 700; margin-bottom: 30px;
      position: relative; animation: fadeUp 0.5s ease both;
    }
    .live-dot {
      width: 7px; height: 7px;
      background: var(--red); border-radius: 50%;
      animation: blink 1.4s ease infinite; flex-shrink: 0;
    }
    @keyframes blink {
      0%,100% { opacity: 1; box-shadow: 0 0 0 0 var(--red-glow); }
      50% { opacity: 0.45; box-shadow: 0 0 0 4px transparent; }
    }
    .hero h1 {
      font-family: 'Tajawal', sans-serif;
      font-size: clamp(1.9rem, 5.5vw, 3.5rem);
      font-weight: 900; line-height: 1.2;
      margin-bottom: 20px; position: relative;
      animation: fadeUp 0.6s 0.08s ease both;
    }
    .hero h1 em { font-style: normal; color: var(--red); }
    .hero p {
      color: var(--dim); font-size: 1rem; line-height: 1.8;
      max-width: 500px; margin: 0 auto 36px;
      position: relative; animation: fadeUp 0.6s 0.16s ease both;
    }
    .hero-apps {
      display: flex; align-items: center; justify-content: center;
      gap: 9px; margin-bottom: 36px; flex-wrap: wrap;
      position: relative; animation: fadeUp 0.6s 0.22s ease both;
    }
    .app-chip {
      display: inline-flex; align-items: center; gap: 6px;
      background: #111; border: 1px solid var(--border);
      padding: 5px 13px; border-radius: 8px;
      font-size: 0.77rem; font-weight: 700; color: #bbb;
    }
    .app-chip .dot { width: 6px; height: 6px; border-radius: 50%; }
    .hero-cta {
      display: flex; gap: 12px; justify-content: center; flex-wrap: wrap;
      position: relative; animation: fadeUp 0.6s 0.28s ease both;
    }
    .btn-primary {
      padding: 13px 32px; background: var(--red); color: white;
      text-decoration: none; border-radius: 10px; font-weight: 700; font-size: 0.93rem;
      transition: 0.22s; box-shadow: 0 4px 22px var(--red-glow);
      display: inline-flex; align-items: center; gap: 8px;
    }
    .btn-primary:hover { background: #ff1a35; transform: translateY(-2px); box-shadow: 0 8px 30px var(--red-glow); }
    .btn-secondary {
      padding: 13px 28px; background: transparent; color: var(--white);
      text-decoration: none; border-radius: 10px; font-weight: 600; font-size: 0.93rem;
      border: 1px solid var(--border); transition: 0.22s;
      display: inline-flex; align-items: center; gap: 8px;
    }
    .btn-secondary:hover { border-color: rgba(232,0,29,0.4); background: var(--red-soft); }

    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(22px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    /* ── STATS BAND ── */
    .stats-band {
      display: grid; grid-template-columns: repeat(4,1fr);
      border-top: 1px solid var(--border); border-bottom: 1px solid var(--border);
      margin: 0 5% 50px; border-radius: 14px; overflow: hidden; background: #0b0b0b;
    }
    .stat-item {
      padding: 22px 16px; text-align: center;
      border-left: 1px solid var(--border); transition: background 0.25s;
    }
    .stat-item:last-child { border-left: none; }
    .stat-item:hover { background: #111; }
    .stat-num {
      display: block; font-family: 'Tajawal', sans-serif;
      font-size: 1.65rem; font-weight: 900; color: var(--red);
      line-height: 1; margin-bottom: 5px;
    }
    .stat-label { font-size: 0.75rem; color: var(--dim); }

    /* ── CHANNEL STATS ── */
    .ch-stats-wrap { padding: 0 5% 46px; }
    .ch-stats-bar {
      background: #0b0b0b; border: 1px solid var(--border);
      border-radius: 14px; padding: 18px 26px;
      display: flex; align-items: center; gap: 8px;
      flex-wrap: wrap; justify-content: space-between;
    }
    .ch-stat-group { display: flex; align-items: center; gap: 26px; flex-wrap: wrap; }
    .ch-stat { display: flex; align-items: center; gap: 10px; }
    .ch-stat-icon {
      width: 36px; height: 36px;
      background: var(--red-soft); border: 1px solid rgba(232,0,29,0.18);
      border-radius: 9px; display: flex; align-items: center; justify-content: center;
      font-size: 1rem; flex-shrink: 0;
    }
    .ch-stat-text strong {
      display: block; font-family: 'Tajawal', sans-serif;
      font-size: 1.05rem; font-weight: 900; color: var(--white); line-height: 1.1;
    }
    .ch-stat-text span { font-size: 0.71rem; color: var(--dim); }
    .live-badge {
      display: inline-flex; align-items: center; gap: 6px;
      background: var(--red-soft); border: 1px solid rgba(232,0,29,0.25);
      color: #ff6070; padding: 5px 12px; border-radius: 20px;
      font-size: 0.72rem; font-weight: 700;
    }

    /* shimmer */
    .skel {
      background: linear-gradient(90deg, #1a1a1a 25%, #222 50%, #1a1a1a 75%);
      background-size: 400% 100%; animation: shimmer 1.4s ease infinite; border-radius: 5px;
    }
    @keyframes shimmer { 0% { background-position: 100% 0; } 100% { background-position: -100% 0; } }

    /* ── TELEGRAM ── */
    .tg-wrap { padding: 0 5% 50px; }
    .tg-banner {
      background: linear-gradient(130deg, #006ba3, #0088cc 55%, #009de0);
      color: white; padding: 18px 28px; border-radius: 14px;
      text-decoration: none; display: flex; align-items: center; gap: 16px;
      font-weight: 700; font-size: 0.97rem; transition: 0.25s;
      box-shadow: 0 4px 26px rgba(0,136,204,0.2);
    }
    .tg-banner:hover { transform: translateY(-3px); box-shadow: 0 10px 36px rgba(0,136,204,0.38); }
    .tg-icon-wrap {
      width: 44px; height: 44px; background: rgba(255,255,255,0.18);
      border-radius: 12px; display: flex; align-items: center; justify-content: center;
      font-size: 1.4rem; flex-shrink: 0;
    }
    .tg-text { flex: 1; }
    .tg-text p { font-size: 0.78rem; opacity: 0.8; font-weight: 400; margin-top: 2px; }
    .tg-arrow {
      width: 30px; height: 30px; background: rgba(255,255,255,0.18);
      border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 1rem;
    }

    /* ── SECTION HEADER ── */
    .section-hd { padding: 6px 5% 24px; display: flex; align-items: center; gap: 14px; }
    .section-bar { width: 4px; height: 28px; background: var(--red); border-radius: 2px; flex-shrink: 0; }
    .section-hd h2 { font-family: 'Tajawal', sans-serif; font-size: 1.55rem; font-weight: 900; }
    .count-badge {
      background: var(--red-soft); border: 1px solid rgba(232,0,29,0.2);
      color: var(--red); padding: 3px 10px; border-radius: 20px;
      font-size: 0.75rem; font-weight: 700;
    }
    .section-line { flex: 1; height: 1px; background: linear-gradient(to left, var(--border), transparent); }

    /* ── FILTER TABS ── */
    .filter-tabs { display: flex; gap: 8px; padding: 0 5% 22px; flex-wrap: wrap; }
    .tab {
      padding: 7px 18px; background: #0e0e0e;
      border: 1px solid var(--border); border-radius: 8px;
      color: var(--dim); font-size: 0.8rem; font-weight: 700;
      cursor: pointer; transition: 0.2s; font-family: 'Cairo', sans-serif;
    }
    .tab:hover, .tab.active {
      background: var(--red-soft); border-color: rgba(232,0,29,0.35); color: var(--red);
    }

    /* ── VIDEOS GRID ── */
    .videos-grid {
      display: grid; grid-template-columns: repeat(auto-fill, minmax(295px,1fr));
      gap: 18px; padding: 0 5% 70px;
    }
    .video-card {
      background: var(--card); border-radius: 14px; overflow: hidden;
      border: 1px solid var(--border-soft);
      transition: border-color 0.28s, transform 0.28s, background 0.28s;
      animation: fadeUp 0.55s ease both;
    }
    .video-card:hover { border-color: rgba(232,0,29,0.4); transform: translateY(-5px); background: var(--card-hover); }

    .thumb-wrap {
      position: relative; width: 100%; padding-top: 56.25%;
      overflow: hidden; background: #0d0d0d;
    }
    .thumb-wrap img {
      position: absolute; top: 0; left: 0; width: 100%; height: 100%;
      object-fit: cover; transition: transform 0.4s ease;
    }
    .video-card:hover .thumb-wrap img { transform: scale(1.06); }

    .play-overlay {
      position: absolute; inset: 0;
      display: flex; align-items: center; justify-content: center;
      background: rgba(0,0,0,0.42); opacity: 0; transition: opacity 0.28s;
    }
    .video-card:hover .play-overlay { opacity: 1; }
    .play-circle {
      width: 54px; height: 54px; background: var(--red); border-radius: 50%;
      display: flex; align-items: center; justify-content: center;
      box-shadow: 0 4px 22px rgba(232,0,29,0.55); transition: transform 0.2s;
    }
    .play-circle:hover { transform: scale(1.1); }
    .play-circle svg { width: 22px; height: 22px; fill: white; margin-right: -2px; }

    .app-tag {
      position: absolute; top: 9px; right: 9px;
      background: rgba(0,0,0,0.72); backdrop-filter: blur(4px);
      border: 1px solid rgba(255,255,255,0.08);
      font-size: 0.68rem; font-weight: 700;
      padding: 3px 9px; border-radius: 5px; color: #ccc;
    }
    .video-card[data-app="alight"] .app-tag { color: #a78bfa; }
    .video-card[data-app="inshot"] .app-tag { color: #34d399; }
    .video-card[data-app="general"] .app-tag { color: #fb923c; }

    .video-info { padding: 14px 15px 15px; }
    .video-title {
      font-size: 0.9rem; font-weight: 700; color: #ddd; line-height: 1.55;
      margin-bottom: 12px;
      display: -webkit-box; -webkit-line-clamp: 2; -webkit-box-orient: vertical; overflow: hidden;
    }
    .video-stats { display: flex; gap: 7px; margin-bottom: 13px; flex-wrap: wrap; min-height: 26px; }
    .s-pill {
      display: inline-flex; align-items: center; gap: 5px;
      background: #131313; border: 1px solid var(--border);
      border-radius: 16px; padding: 3px 10px;
      font-size: 0.72rem; font-weight: 700; color: var(--dim);
    }
    .s-pill.views { color: #60b4f8; border-color: rgba(96,180,248,0.2); background: rgba(96,180,248,0.05); }
    .s-pill.likes { color: #f87585; border-color: rgba(248,117,133,0.2); background: rgba(248,117,133,0.05); }
    .s-pill.skel {
      min-width: 72px; height: 24px; border-color: var(--border);
      background: linear-gradient(90deg, #1a1a1a 25%, #222 50%, #1a1a1a 75%);
      background-size: 400% 100%; animation: shimmer 1.4s ease infinite;
      color: transparent;
    }
    .btn-watch {
      display: flex; align-items: center; justify-content: center; gap: 7px;
      width: 100%; padding: 10px; background: var(--red-soft); color: var(--red);
      text-decoration: none; border: 1px solid rgba(232,0,29,0.22);
      border-radius: 9px; font-size: 0.86rem; font-weight: 700; transition: 0.22s;
    }
    .btn-watch:hover { background: var(--red); color: white; border-color: var(--red); }
    .btn-watch svg { width: 15px; height: 15px; fill: currentColor; }

    /* ── FOOTER ── */
    footer {
      padding: 32px 5%; text-align: center; color: var(--dim2);
      border-top: 1px solid var(--border); font-size: 0.82rem;
      display: flex; flex-direction: column; gap: 10px; align-items: center;
    }
    .footer-logo { display: flex; align-items: center; gap: 9px; text-decoration: none; }
    .footer-brand { font-family: 'Tajawal', sans-serif; font-weight: 900; font-size: 1rem; color: #333; }
    .footer-brand em { font-style: normal; color: var(--red); }
    footer a { color: var(--red); text-decoration: none; }
    footer a:hover { text-decoration: underline; }

    ::-webkit-scrollbar { width: 5px; }
    ::-webkit-scrollbar-track { background: var(--black); }
    ::-webkit-scrollbar-thumb { background: #2a0008; border-radius: 3px; }
    ::-webkit-scrollbar-thumb:hover { background: var(--red); }

    @media (max-width: 700px) {
      .stats-band { grid-template-columns: repeat(2,1fr); }
      .stat-item:nth-child(2) { border-left: none; }
      .stat-item:nth-child(3), .stat-item:nth-child(4) { border-top: 1px solid var(--border); }
      .stat-item:nth-child(4) { border-left: none; }
      .nav-link { display: none; }
      header { padding: 0 4%; }
    }
  </style>
</head>
<body>

<!-- ══ HEADER ══ -->
<header>
  <a href="#" class="logo-area">
    <div class="logo-mark">
      <svg class="ring" viewBox="0 0 46 46" fill="none" xmlns="http://www.w3.org/2000/svg">
        <circle cx="23" cy="23" r="21" stroke="#E8001D" stroke-width="1.4" stroke-dasharray="5 3.5" stroke-linecap="round"/>
      </svg>
      <div class="logo-inner">
        <span>3LN</span>
      </div>
    </div>
    <div class="brand-text">
      <span class="brand-main">islam<em>_3LN</em></span>
      <span class="brand-sub">بوابة المونتاج الاحترافي</span>
    </div>
  </a>
  <nav class="header-nav">
    <a href="https://t.me/islam3ln" class="nav-link" target="_blank" rel="noopener">تلغرام</a>
    <a href="https://youtube.com/@luxx_islam_pro" class="nav-btn" target="_blank" rel="noopener">
      <svg width="14" height="14" viewBox="0 0 24 24" fill="white"><path d="M8 5v14l11-7z"/></svg>
      القناة
    </a>
  </nav>
</header>


<!-- ══ HERO ══ -->
<section class="hero">
  <div class="hero-bg"></div>
  <div class="hero-grid"></div>
  <div class="hero-badge">
    <span class="live-dot"></span>
    بوابة المونتاج والدروس الاحترافية
  </div>
  <h1>احترف المونتاج و<em>صناعة المحتوى</em><br>من الصفر</h1>
  <p>تعلّم أسرار تطبيقات المونتاج على الهاتف مع أوضح الشروحات بالعربي — مجاناً وبدون تعقيد.</p>
  <div class="hero-apps">
    <div class="app-chip"><span class="dot" style="background:#a78bfa"></span> Alight Motion</div>
    <div class="app-chip"><span class="dot" style="background:#34d399"></span> InShot</div>
    <div class="app-chip"><span class="dot" style="background:#fb923c"></span> CapCut</div>
    <div class="app-chip"><span class="dot" style="background:#60b4f8"></span> Reels</div>
  </div>
  <div class="hero-cta">
    <a href="https://youtube.com/@luxx_islam_pro" target="_blank" rel="noopener" class="btn-primary">
      <svg width="15" height="15" viewBox="0 0 24 24" fill="white"><path d="M8 5v14l11-7z"/></svg>
      تابع القناة
    </a>
    <a href="https://t.me/islam3ln" target="_blank" rel="noopener" class="btn-secondary">
      📥 ملحقات مجانية
    </a>
  </div>
</section>


<!-- ══ STATS ══ -->
<div class="stats-band">
  <div class="stat-item"><span class="stat-num">10+</span><span class="stat-label">شرح مختار</span></div>
  <div class="stat-item"><span class="stat-num">3</span><span class="stat-label">تطبيقات</span></div>
  <div class="stat-item"><span class="stat-num">100%</span><span class="stat-label">مجاني</span></div>
  <div class="stat-item"><span class="stat-num">🔥</span><span class="stat-label">كورس ريلز</span></div>
</div>


<!-- ══ CHANNEL STATS ══ -->
<div class="ch-stats-wrap">
  <div class="ch-stats-bar" id="chBar">
    <div class="ch-stat-group">
      <div class="ch-stat">
        <div class="ch-stat-icon">👥</div>
        <div class="ch-stat-text">
          <strong><span class="skel" style="display:inline-block;width:55px;height:17px;"></span></strong>
          <span>مشترك</span>
        </div>
      </div>
      <div class="ch-stat">
        <div class="ch-stat-icon">👁</div>
        <div class="ch-stat-text">
          <strong><span class="skel" style="display:inline-block;width:65px;height:17px;"></span></strong>
          <span>مشاهدة</span>
        </div>
      </div>
      <div class="ch-stat">
        <div class="ch-stat-icon">🎬</div>
        <div class="ch-stat-text">
          <strong><span class="skel" style="display:inline-block;width:40px;height:17px;"></span></strong>
          <span>فيديو</span>
        </div>
      </div>
    </div>
    <div class="live-badge"><span class="live-dot" style="width:6px;height:6px;"></span> بيانات مباشرة</div>
  </div>
</div>


<!-- ══ TELEGRAM ══ -->
<div class="tg-wrap">
  <a href="https://t.me/islam3ln" class="tg-banner" target="_blank" rel="noopener">
    <div class="tg-icon-wrap">📥</div>
    <div class="tg-text">
      <strong>قناة التلغرام الرسمية</strong>
      <p>حمّل ملحقات المونتاج والقوالب المجانية مباشرة</p>
    </div>
    <div class="tg-arrow">←</div>
  </a>
</div>


<!-- ══ VIDEOS ══ -->
<div class="section-hd">
  <div class="section-bar"></div>
  <h2>شروحات مختارة</h2>
  <span class="count-badge">10 فيديو</span>
  <div class="section-line"></div>
</div>

<div class="filter-tabs">
  <button class="tab active" data-filter="all">الكل</button>
  <button class="tab" data-filter="alight">Alight Motion</button>
  <button class="tab" data-filter="inshot">InShot</button>
  <button class="tab" data-filter="general">عام</button>
</div>

<div class="videos-grid" id="videosGrid">

  <div class="video-card" style="animation-delay:0.04s" data-vid="wwkB8KWByPQ" data-app="alight">
    <div class="thumb-wrap">
      <img src="https://i.ytimg.com/vi/wwkB8KWByPQ/sddefault.jpg" alt="مقدمة احترافية - Alight Motion" loading="lazy">
      <div class="play-overlay"><div class="play-circle"><svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg></div></div>
      <span class="app-tag">Alight Motion</span>
    </div>
    <div class="video-info">
      <p class="video-title">كيف تصمم مقدمة احترافية بالهاتف باستخدام Alight Motion</p>
      <div class="video-stats"><span class="s-pill skel"></span></div>
      <a href="https://youtu.be/wwkB8KWByPQ" class="btn-watch" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg> مشاهدة الشرح
      </a>
    </div>
  </div>

  <div class="video-card" style="animation-delay:0.08s" data-vid="TZhNJqZbDwI" data-app="alight">
    <div class="thumb-wrap">
      <img src="https://i.ytimg.com/vi/TZhNJqZbDwI/sddefault.jpg" alt="إعلان 3D - Alight Motion" loading="lazy">
      <div class="play-overlay"><div class="play-circle"><svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg></div></div>
      <span class="app-tag">Alight Motion</span>
    </div>
    <div class="video-info">
      <p class="video-title">كيف تصنع إعلان 3D احترافي على لايت موشن</p>
      <div class="video-stats"><span class="s-pill skel"></span></div>
      <a href="https://youtu.be/TZhNJqZbDwI" class="btn-watch" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg> مشاهدة الشرح
      </a>
    </div>
  </div>

  <div class="video-card" style="animation-delay:0.12s" data-vid="PahY-vvDYwE" data-app="inshot">
    <div class="thumb-wrap">
      <img src="https://i.ytimg.com/vi/PahY-vvDYwE/maxresdefault.jpg" alt="أسرار InShot" loading="lazy">
      <div class="play-overlay"><div class="play-circle"><svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg></div></div>
      <span class="app-tag">InShot</span>
    </div>
    <div class="video-info">
      <p class="video-title">أسرار في تطبيق InShot يخفيها عنك المحترفون</p>
      <div class="video-stats"><span class="s-pill skel"></span></div>
      <a href="https://youtu.be/PahY-vvDYwE" class="btn-watch" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg> مشاهدة الشرح
      </a>
    </div>
  </div>

  <div class="video-card" style="animation-delay:0.16s" data-vid="-iDrVYWBXNo" data-app="alight">
    <div class="thumb-wrap">
      <img src="https://i.ytimg.com/vi/-iDrVYWBXNo/sddefault.jpg" alt="انترو احترافي - Alight Motion" loading="lazy">
      <div class="play-overlay"><div class="play-circle"><svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg></div></div>
      <span class="app-tag">Alight Motion</span>
    </div>
    <div class="video-info">
      <p class="video-title">كيفية عمل انترو احترافي في Alight Motion — شرح كامل</p>
      <div class="video-stats"><span class="s-pill skel"></span></div>
      <a href="https://youtu.be/-iDrVYWBXNo" class="btn-watch" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg> مشاهدة الشرح
      </a>
    </div>
  </div>

  <div class="video-card" style="animation-delay:0.2s" data-vid="timNK3PEAdI" data-app="inshot">
    <div class="thumb-wrap">
      <img src="https://i.ytimg.com/vi/timNK3PEAdI/sddefault.jpg" alt="مقدمة InShot" loading="lazy">
      <div class="play-overlay"><div class="play-circle"><svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg></div></div>
      <span class="app-tag">InShot</span>
    </div>
    <div class="video-info">
      <p class="video-title">شرح مونتاج مقدمة احترافية بتطبيق InShot — أساسيات</p>
      <div class="video-stats"><span class="s-pill skel"></span></div>
      <a href="https://youtu.be/timNK3PEAdI" class="btn-watch" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg> مشاهدة الشرح
      </a>
    </div>
  </div>

  <div class="video-card" style="animation-delay:0.24s" data-vid="6Rz5AcXRIh4" data-app="general">
    <div class="thumb-wrap">
      <img src="https://i.ytimg.com/vi/6Rz5AcXRIh4/maxresdefault.jpg" alt="ريلز احترافي" loading="lazy">
      <div class="play-overlay"><div class="play-circle"><svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg></div></div>
      <span class="app-tag">Reels</span>
    </div>
    <div class="video-info">
      <p class="video-title">شرح كيفية مونتاج ريلز احترافي بالهاتف — كورس مجاني</p>
      <div class="video-stats"><span class="s-pill skel"></span></div>
      <a href="https://youtu.be/6Rz5AcXRIh4" class="btn-watch" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg> مشاهدة الشرح
      </a>
    </div>
  </div>

  <div class="video-card" style="animation-delay:0.28s" data-vid="cvNhaYeQe6Q" data-app="alight">
    <div class="thumb-wrap">
      <img src="https://i.ytimg.com/vi/cvNhaYeQe6Q/sddefault.jpg" alt="كاميرا 3D - Alight Motion" loading="lazy">
      <div class="play-overlay"><div class="play-circle"><svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg></div></div>
      <span class="app-tag">Alight Motion</span>
    </div>
    <div class="video-info">
      <p class="video-title">شرح تأثير الكاميرا 3D على لايت موشن</p>
      <div class="video-stats"><span class="s-pill skel"></span></div>
      <a href="https://youtu.be/cvNhaYeQe6Q" class="btn-watch" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg> مشاهدة الشرح
      </a>
    </div>
  </div>

  <div class="video-card" style="animation-delay:0.32s" data-vid="4UGT0JR-RiU" data-app="general">
    <div class="thumb-wrap">
      <img src="https://i.ytimg.com/vi/4UGT0JR-RiU/maxresdefault.jpg" alt="تسريع المونتاج" loading="lazy">
      <div class="play-overlay"><div class="play-circle"><svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg></div></div>
      <span class="app-tag">نصائح</span>
    </div>
    <div class="video-info">
      <p class="video-title">5 خطوات لتسريع المونتاج وإنجاز الفيديو بسرعة ⚡</p>
      <div class="video-stats"><span class="s-pill skel"></span></div>
      <a href="https://youtu.be/4UGT0JR-RiU" class="btn-watch" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg> مشاهدة الشرح
      </a>
    </div>
  </div>

  <div class="video-card" style="animation-delay:0.36s" data-vid="qjg4Eh3MAvg" data-app="general">
    <div class="thumb-wrap">
      <img src="https://i.ytimg.com/vi/qjg4Eh3MAvg/sddefault.jpg" alt="صورة مصغرة" loading="lazy">
      <div class="play-overlay"><div class="play-circle"><svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg></div></div>
      <span class="app-tag">ثمبنيل</span>
    </div>
    <div class="video-info">
      <p class="video-title">تصميم صورة مصغرة احترافية بالهاتف فقط 🔥</p>
      <div class="video-stats"><span class="s-pill skel"></span></div>
      <a href="https://youtu.be/qjg4Eh3MAvg" class="btn-watch" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg> مشاهدة الشرح
      </a>
    </div>
  </div>

  <div class="video-card" style="animation-delay:0.40s" data-vid="Iri6wMX0Tr0" data-app="inshot">
    <div class="thumb-wrap">
      <img src="https://i.ytimg.com/vi/Iri6wMX0Tr0/sddefault.jpg" alt="ريلز InShot" loading="lazy">
      <div class="play-overlay"><div class="play-circle"><svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg></div></div>
      <span class="app-tag">InShot</span>
    </div>
    <div class="video-info">
      <p class="video-title">أفضل طريقة لعمل ريلز احترافي باستخدام InShot</p>
      <div class="video-stats"><span class="s-pill skel"></span></div>
      <a href="https://youtu.be/Iri6wMX0Tr0" class="btn-watch" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg> مشاهدة الشرح
      </a>
    </div>
  </div>

</div>


<!-- ══ FOOTER ══ -->
<footer>
  <a href="#" class="footer-logo">
    <div class="logo-mark" style="width:32px;height:32px;">
      <svg class="ring" viewBox="0 0 46 46" fill="none">
        <circle cx="23" cy="23" r="21" stroke="#E8001D" stroke-width="1.4" stroke-dasharray="5 3.5" stroke-linecap="round"/>
      </svg>
      <div class="logo-inner" style="inset:4px;">
        <span style="font-size:0.54rem;">3LN</span>
      </div>
    </div>
    <span class="footer-brand">islam<em>_3LN</em></span>
  </a>
  <p>© 2026 جميع الحقوق محفوظة &nbsp;·&nbsp;
    <a href="https://youtube.com/@luxx_islam_pro" target="_blank" rel="noopener">يوتيوب</a> &nbsp;·&nbsp;
    <a href="https://t.me/islam3ln" target="_blank" rel="noopener">تلغرام</a>
  </p>
</footer>


<script>
  /* ── FORMAT ── */
  function fmt(n) {
    if (!n || isNaN(n)) return '—';
    if (n >= 1e6) return (n/1e6).toFixed(1).replace('.0','') + 'M';
    if (n >= 1e3) return (n/1e3).toFixed(1).replace('.0','') + 'K';
    return String(n);
  }

  /* ── COUNT UP ── */
  function countUp(el, target) {
    if (!el || !target) return;
    const dur = 1100, t0 = performance.now();
    (function tick(now) {
      const p = Math.min((now - t0) / dur, 1);
      const e = 1 - Math.pow(1 - p, 3);
      el.textContent = fmt(Math.floor(e * target));
      if (p < 1) requestAnimationFrame(tick);
    })(t0);
  }

  /* ── API (multiple instances for reliability) ── */
  const INSTANCES = [
    'https://inv.tux.pizza',
    'https://invidious.privacydev.net',
    'https://yt.cdaut.de'
  ];
  async function apiFetch(path) {
    for (const base of INSTANCES) {
      try {
        const r = await fetch(base + path, { signal: AbortSignal.timeout(5500) });
        if (r.ok) return await r.json();
      } catch { /* try next */ }
    }
    throw new Error('all failed');
  }

  /* ── VIDEO STATS ── */
  async function loadVideoStats(card) {
    const vid = card.dataset.vid;
    const div = card.querySelector('.video-stats');
    try {
      const d = await apiFetch('/api/v1/videos/' + vid + '?fields=viewCount,likeCount');
      div.innerHTML = '';
      if (d.viewCount) {
        const vp = document.createElement('span');
        vp.className = 's-pill views';
        const vs = document.createElement('span');
        vp.textContent = '👁 ';
        vp.appendChild(vs);
        div.appendChild(vp);
        countUp(vs, d.viewCount);
        vs.textContent = fmt(d.viewCount) + ' مشاهدة';
        countUp({ set textContent(v){ vs.textContent = v + ' مشاهدة'; } }, d.viewCount);
      }
      if (d.likeCount) {
        const lp = document.createElement('span');
        lp.className = 's-pill likes';
        const ls = document.createElement('span');
        lp.textContent = '👍 ';
        lp.appendChild(ls);
        div.appendChild(lp);
        ls.textContent = fmt(d.likeCount) + ' إعجاب';
        (function animLike(t0) {
          const dur = 1100;
          requestAnimationFrame(function tick(now) {
            const p = Math.min((now - t0) / dur, 1);
            const e = 1 - Math.pow(1 - p, 3);
            ls.textContent = fmt(Math.floor(e * d.likeCount)) + ' إعجاب';
            if (p < 1) requestAnimationFrame(tick);
          });
        })(performance.now());
        (function animView(t0) {
          if (!d.viewCount) return;
          const dur = 1100;
          const vs2 = div.querySelector('.views span');
          if (!vs2) return;
          requestAnimationFrame(function tick(now) {
            const p = Math.min((now - t0) / dur, 1);
            const e = 1 - Math.pow(1 - p, 3);
            vs2.textContent = fmt(Math.floor(e * d.viewCount)) + ' مشاهدة';
            if (p < 1) requestAnimationFrame(tick);
          });
        })(performance.now());
      }
    } catch {
      div.innerHTML = '<span class="s-pill" style="color:#3a3a3a;">📺 يوتيوب</span>';
    }
  }

  /* ── CHANNEL STATS ── */
  async function loadChannelStats() {
    const bar = document.getElementById('chBar');
    try {
      const d = await apiFetch('/api/v1/channels/luxx_islam_pro?fields=subCount,totalViews,videoCount');
      bar.innerHTML = `
        <div class="ch-stat-group">
          <div class="ch-stat">
            <div class="ch-stat-icon">👥</div>
            <div class="ch-stat-text"><strong id="cS">0</strong><span>مشترك</span></div>
          </div>
          <div class="ch-stat">
            <div class="ch-stat-icon">👁</div>
            <div class="ch-stat-text"><strong id="cV">0</strong><span>إجمالي المشاهدات</span></div>
          </div>
          <div class="ch-stat">
            <div class="ch-stat-icon">🎬</div>
            <div class="ch-stat-text"><strong id="cVid">0</strong><span>فيديو</span></div>
          </div>
        </div>
        <div class="live-badge"><span class="live-dot" style="width:6px;height:6px;"></span> بيانات مباشرة</div>
      `;
      const animate = (id, val) => {
        const el = document.getElementById(id);
        if (!el || !val) return;
        const dur = 1200, t0 = performance.now();
        (function tick(now) {
          const p = Math.min((now - t0)/dur, 1);
          const e = 1 - Math.pow(1-p, 3);
          el.textContent = fmt(Math.floor(e * val));
          if (p < 1) requestAnimationFrame(tick);
        })(t0);
      };
      animate('cS', d.subCount);
      animate('cV', d.totalViews);
      animate('cVid', d.videoCount);
    } catch {
      bar.innerHTML = `
        <div class="ch-stat-group">
          <div class="ch-stat">
            <div class="ch-stat-icon">📺</div>
            <div class="ch-stat-text">
              <strong style="color:#ccc;">@luxx_islam_pro</strong>
              <span>تعذّر تحميل الإحصائيات</span>
            </div>
          </div>
        </div>
        <a href="https://youtube.com/@luxx_islam_pro" target="_blank" rel="noopener" class="nav-btn" style="font-size:0.8rem;padding:7px 16px;">فتح القناة</a>
      `;
    }
  }

  /* ── FILTER TABS ── */
  document.querySelectorAll('.tab').forEach(btn => {
    btn.addEventListener('click', () => {
      document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
      btn.classList.add('active');
      const f = btn.dataset.filter;
      document.querySelectorAll('.video-card').forEach(card => {
        card.style.display = (f === 'all' || card.dataset.app === f) ? '' : 'none';
      });
    });
  });

  /* ── INIT ── */
  document.addEventListener('DOMContentLoaded', () => {
    loadChannelStats();
    document.querySelectorAll('.video-card[data-vid]').forEach((card, i) => {
      setTimeout(() => loadVideoStats(card), i * 280);
    });
  });
</script>
</body>
</html>

