<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>islam_3LN | ملحقات المونتاج المجانية</title>
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
      min-height: 460px;
      display: flex; align-items: center; justify-content: center;
      flex-direction: column; text-align: center;
      padding: 90px 8% 60px;
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
      max-width: 520px; margin: 0 auto 36px;
      position: relative; animation: fadeUp 0.6s 0.16s ease both;
    }
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

    /* ── ASSET CARDS ── */
    .assets-grid {
      display: grid; grid-template-columns: repeat(auto-fill, minmax(260px,1fr));
      gap: 18px; padding: 0 5% 70px;
    }
    .asset-card {
      background: var(--card); border-radius: 14px; overflow: hidden;
      border: 1px solid var(--border-soft);
      transition: border-color 0.28s, transform 0.28s, background 0.28s;
      animation: fadeUp 0.55s ease both;
      padding: 26px 22px;
      display: flex; flex-direction: column; gap: 16px;
    }
    .asset-card:hover { border-color: rgba(232,0,29,0.4); transform: translateY(-5px); background: var(--card-hover); }

    .asset-icon {
      width: 54px; height: 54px;
      background: var(--red-soft); border: 1px solid rgba(232,0,29,0.22);
      border-radius: 12px; display: flex; align-items: center; justify-content: center;
      font-size: 1.6rem;
    }
    .asset-title {
      font-family: 'Tajawal', sans-serif;
      font-size: 1.15rem; font-weight: 900; color: var(--white);
    }
    .asset-desc {
      font-size: 0.85rem; color: var(--dim); line-height: 1.7;
    }
    .btn-download {
      display: flex; align-items: center; justify-content: center; gap: 7px;
      width: 100%; padding: 12px; background: var(--red-soft); color: var(--red);
      text-decoration: none; border: 1px solid rgba(232,0,29,0.22);
      border-radius: 9px; font-size: 0.88rem; font-weight: 700; transition: 0.22s;
      margin-top: auto;
    }
    .btn-download:hover { background: var(--red); color: white; border-color: var(--red); }

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
      <span class="brand-sub">ملحقات المونتاج المجانية</span>
    </div>
  </a>
  <nav class="header-nav">
    <a href="https://t.me/islam3ln" class="nav-link" target="_blank" rel="noopener">تلغرام</a>
    <a href="https://youtube.com/@luxx_islam_pro?si=4i3i4HmhJvfJzRyz" class="nav-btn" target="_blank" rel="noopener">
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
    ملحقات مونتاج مجانية 100%
  </div>
  <h1>كل ما يحتاجه <em>مونتاجك</em><br>في مكان واحد</h1>
  <p>صور متحركة، خلفيات، إنتقالات ومؤثرات صوتية جاهزة للتحميل المباشر — استخدمها بحرية في مشاريعك.</p>
  <div class="hero-cta">
    <a href="https://youtube.com/@luxx_islam_pro?si=4i3i4HmhJvfJzRyz" target="_blank" rel="noopener" class="btn-primary">
      <svg width="15" height="15" viewBox="0 0 24 24" fill="white"><path d="M8 5v14l11-7z"/></svg>
      تابع القناة
    </a>
    <a href="https://t.me/islam3ln" target="_blank" rel="noopener" class="btn-secondary">
      📥 انضم للتلغرام
    </a>
  </div>
</section>


<!-- ══ STATS ══ -->
<div class="stats-band">
  <div class="stat-item"><span class="stat-num">4</span><span class="stat-label">فئات ملحقات</span></div>
  <div class="stat-item"><span class="stat-num">100%</span><span class="stat-label">مجاني</span></div>
  <div class="stat-item"><span class="stat-num">🔥</span><span class="stat-label">تحديث مستمر</span></div>
  <div class="stat-item"><span class="stat-num">⚡</span><span class="stat-label">تحميل مباشر</span></div>
</div>


<!-- ══ TELEGRAM ══ -->
<div class="tg-wrap">
  <a href="https://t.me/islam3ln" class="tg-banner" target="_blank" rel="noopener">
    <div class="tg-icon-wrap">📥</div>
    <div class="tg-text">
      <strong>قناة التلغرام الرسمية</strong>
      <p>تابع كل جديد وملحقات حصرية أول بأول</p>
    </div>
    <div class="tg-arrow">←</div>
  </a>
</div>


<!-- ══ ASSETS ══ -->
<div class="section-hd">
  <div class="section-bar"></div>
  <h2>الملحقات</h2>
  <span class="count-badge">4 مجلدات</span>
  <div class="section-line"></div>
</div>

<div class="assets-grid">

  <div class="asset-card" style="animation-delay:0.04s">
    <div class="asset-icon">🔥</div>
    <div class="asset-title">صور متحركة</div>
    <div class="asset-desc">مجموعة فيديوهات وعناصر متحركة جاهزة لاستخدامها في مشاريعك.</div>
    <a href="https://drive.google.com/drive/folders/1JF64naxpsknVwsXvsbvp0qa630lOCzaP" class="btn-download" target="_blank" rel="noopener">
      📁 فتح المجلد
    </a>
  </div>

  <div class="asset-card" style="animation-delay:0.08s">
    <div class="asset-icon">🖼️</div>
    <div class="asset-title">خلفيات</div>
    <div class="asset-desc">خلفيات متنوعة بجودة عالية لتصاميمك ومقاطعك.</div>
    <a href="https://drive.google.com/drive/folders/1Dv1bkmusgY2OWPC6MpR1x_VKRk-mSvJo" class="btn-download" target="_blank" rel="noopener">
      📁 فتح المجلد
    </a>
  </div>

  <div class="asset-card" style="animation-delay:0.12s">
    <div class="asset-icon">🔀</div>
    <div class="asset-title">إنتقالات</div>
    <div class="asset-desc">إنتقالات احترافية تضيف لمسة سلسة بين مشاهد الفيديو.</div>
    <a href="https://drive.google.com/drive/folders/1HgfME_77qlhHr4gSkf7sf_rTWA37oqlV" class="btn-download" target="_blank" rel="noopener">
      📁 فتح المجلد
    </a>
  </div>

  <div class="asset-card" style="animation-delay:0.16s">
    <div class="asset-icon">🔊</div>
    <div class="asset-title">مؤثرات صوتية</div>
    <div class="asset-desc">مكتبة مؤثرات صوتية (SFX) لإضافة الحيوية على مونتاجك.</div>
    <a href="https://drive.google.com/drive/folders/1BTJoCEi2QQhCCzaulXvIVDIe5OZMAEnx" class="btn-download" target="_blank" rel="noopener">
      📁 فتح المجلد
    </a>
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
    <a href="https://youtube.com/@luxx_islam_pro?si=4i3i4HmhJvfJzRyz" target="_blank" rel="noopener">يوتيوب</a> &nbsp;·&nbsp;
    <a href="https://t.me/islam3ln" target="_blank" rel="noopener">تلغرام</a>
  </p>
</footer>

</body>
</html>
