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
      --red-dim: #9a0012;
      --black: #060606;
      --card: #0e0e0e;
      --border: #1e1e1e;
      --white: #FFFFFF;
      --dim: #888;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }

    html { scroll-behavior: smooth; }

    body {
      background-color: var(--black);
      color: var(--white);
      font-family: 'Cairo', sans-serif;
      overflow-x: hidden;
    }

    /* ── NOISE OVERLAY ── */
    body::before {
      content: '';
      position: fixed;
      inset: 0;
      background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.03'/%3E%3C/svg%3E");
      pointer-events: none;
      z-index: 9999;
      opacity: 0.4;
    }

    /* ── HEADER ── */
    header {
      padding: 0 6%;
      height: 70px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: rgba(6,6,6,0.92);
      backdrop-filter: blur(12px);
      position: sticky;
      top: 0;
      z-index: 100;
      border-bottom: 1px solid var(--border);
    }

    .logo-area {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .logo-ring {
      position: relative;
      width: 44px; height: 44px;
    }
    .logo-ring svg {
      position: absolute; top: 0; left: 0;
      width: 100%; height: 100%;
      animation: spin 8s linear infinite;
    }
    @keyframes spin { to { transform: rotate(360deg); } }

    .logo-ring img {
      position: absolute;
      top: 5px; left: 5px;
      width: 34px; height: 34px;
      border-radius: 50%;
      object-fit: cover;
    }

    .brand-name {
      font-family: 'Tajawal', sans-serif;
      font-size: 1.25rem;
      font-weight: 900;
      letter-spacing: 1px;
      color: var(--white);
    }
    .brand-name span { color: var(--red); }

    .nav-link {
      color: var(--dim);
      text-decoration: none;
      font-size: 0.88rem;
      font-weight: 600;
      letter-spacing: 0.5px;
      transition: color 0.2s;
      border-bottom: 2px solid transparent;
      padding-bottom: 2px;
    }
    .nav-link:hover { color: var(--white); border-bottom-color: var(--red); }

    /* ── HERO ── */
    .hero {
      min-height: 520px;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      text-align: center;
      padding: 80px 8% 60px;
      position: relative;
      overflow: hidden;
    }

    .hero-bg {
      position: absolute; inset: 0;
      background:
        radial-gradient(ellipse 80% 60% at 50% -10%, rgba(232,0,29,0.18) 0%, transparent 70%),
        radial-gradient(ellipse 40% 40% at 80% 80%, rgba(232,0,29,0.05) 0%, transparent 60%);
    }

    .hero-grid {
      position: absolute; inset: 0;
      background-image:
        linear-gradient(rgba(232,0,29,0.04) 1px, transparent 1px),
        linear-gradient(90deg, rgba(232,0,29,0.04) 1px, transparent 1px);
      background-size: 60px 60px;
      mask-image: radial-gradient(ellipse 80% 80% at 50% 50%, black 20%, transparent 100%);
    }

    .hero-badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: rgba(232,0,29,0.1);
      border: 1px solid rgba(232,0,29,0.3);
      color: var(--red);
      padding: 6px 18px;
      border-radius: 50px;
      font-size: 0.82rem;
      font-weight: 700;
      margin-bottom: 28px;
      letter-spacing: 0.5px;
      position: relative;
      animation: fadeUp 0.6s ease both;
    }
    .hero-badge::before {
      content: '';
      width: 8px; height: 8px;
      background: var(--red);
      border-radius: 50%;
      animation: pulse 1.5s ease infinite;
    }
    @keyframes pulse {
      0%, 100% { opacity: 1; transform: scale(1); }
      50% { opacity: 0.4; transform: scale(0.7); }
    }

    .hero h1 {
      font-family: 'Tajawal', sans-serif;
      font-size: clamp(2rem, 5vw, 3.4rem);
      font-weight: 900;
      line-height: 1.2;
      margin-bottom: 18px;
      position: relative;
      animation: fadeUp 0.7s 0.1s ease both;
    }
    .hero h1 em {
      font-style: normal;
      color: var(--red);
    }

    .hero p {
      color: var(--dim);
      font-size: 1.05rem;
      max-width: 520px;
      margin: 0 auto 36px;
      position: relative;
      animation: fadeUp 0.7s 0.2s ease both;
    }

    .hero-cta {
      display: flex;
      gap: 14px;
      justify-content: center;
      flex-wrap: wrap;
      position: relative;
      animation: fadeUp 0.7s 0.3s ease both;
    }

    .btn-primary {
      padding: 13px 30px;
      background: var(--red);
      color: white;
      text-decoration: none;
      border-radius: 10px;
      font-weight: 700;
      font-size: 0.95rem;
      transition: all 0.25s;
      box-shadow: 0 4px 20px rgba(232,0,29,0.3);
    }
    .btn-primary:hover {
      background: #ff1a35;
      transform: translateY(-2px);
      box-shadow: 0 8px 28px rgba(232,0,29,0.45);
    }

    .btn-secondary {
      padding: 13px 30px;
      background: transparent;
      color: var(--white);
      text-decoration: none;
      border-radius: 10px;
      font-weight: 600;
      font-size: 0.95rem;
      border: 1px solid var(--border);
      transition: all 0.25s;
    }
    .btn-secondary:hover { border-color: rgba(232,0,29,0.5); background: rgba(232,0,29,0.06); }

    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(20px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    /* ── STATS ── */
    .stats {
      display: flex;
      justify-content: center;
      gap: 0;
      border-top: 1px solid var(--border);
      border-bottom: 1px solid var(--border);
      margin: 0 6% 50px;
      border-radius: 12px;
      overflow: hidden;
    }
    .stat {
      flex: 1;
      padding: 24px 20px;
      text-align: center;
      border-left: 1px solid var(--border);
    }
    .stat:last-child { border-left: none; }
    .stat-num {
      font-family: 'Tajawal', sans-serif;
      font-size: 1.7rem;
      font-weight: 900;
      color: var(--red);
      display: block;
    }
    .stat-label { font-size: 0.78rem; color: var(--dim); }

    /* ── TELEGRAM BANNER ── */
    .telegram-wrap { padding: 0 6% 50px; }
    .telegram-banner {
      background: linear-gradient(135deg, #006fa8 0%, #0088cc 50%, #00a8e8 100%);
      color: white;
      padding: 20px 30px;
      text-align: center;
      border-radius: 14px;
      text-decoration: none;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 12px;
      font-weight: 700;
      font-size: 1rem;
      transition: 0.3s;
      box-shadow: 0 4px 24px rgba(0,136,204,0.25);
    }
    .telegram-banner:hover { transform: translateY(-3px); box-shadow: 0 8px 32px rgba(0,136,204,0.4); }
    .telegram-banner .tg-icon {
      width: 36px; height: 36px;
      background: rgba(255,255,255,0.2);
      border-radius: 50%;
      display: flex; align-items: center; justify-content: center;
      font-size: 1.2rem;
      flex-shrink: 0;
    }

    /* ── SECTION ── */
    .section-header {
      padding: 10px 6% 28px;
      display: flex;
      align-items: center;
      gap: 16px;
    }
    .section-header h2 {
      font-family: 'Tajawal', sans-serif;
      font-size: 1.7rem;
      font-weight: 900;
    }
    .section-line {
      flex: 1;
      height: 1px;
      background: linear-gradient(to left, var(--red), transparent);
    }
    .section-bar {
      width: 5px; height: 30px;
      background: var(--red);
      border-radius: 3px;
      flex-shrink: 0;
    }

    /* ── VIDEOS GRID ── */
    .videos-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(290px, 1fr));
      gap: 20px;
      padding: 0 6% 60px;
    }

    .video-card {
      background: var(--card);
      border-radius: 14px;
      overflow: hidden;
      border: 1px solid var(--border);
      transition: border-color 0.3s, transform 0.3s;
      animation: fadeUp 0.5s ease both;
    }
    .video-card:hover {
      border-color: rgba(232,0,29,0.5);
      transform: translateY(-6px);
    }
    .video-card:hover .play-overlay { opacity: 1; }

    .thumbnail-container {
      position: relative;
      width: 100%;
      padding-top: 56.25%;
      overflow: hidden;
    }
    .thumbnail-container img {
      position: absolute; top: 0; left: 0;
      width: 100%; height: 100%;
      object-fit: cover;
      transition: transform 0.4s ease;
    }
    .video-card:hover .thumbnail-container img { transform: scale(1.05); }

    .play-overlay {
      position: absolute; inset: 0;
      display: flex; align-items: center; justify-content: center;
      background: rgba(0,0,0,0.45);
      opacity: 0;
      transition: opacity 0.3s;
    }
    .play-btn {
      width: 52px; height: 52px;
      background: var(--red);
      border-radius: 50%;
      display: flex; align-items: center; justify-content: center;
      box-shadow: 0 4px 20px rgba(232,0,29,0.5);
    }
    .play-btn svg { width: 20px; height: 20px; fill: white; margin-right: -2px; }

    .duration-badge {
      position: absolute;
      bottom: 8px; left: 8px;
      background: rgba(0,0,0,0.8);
      color: white;
      font-size: 0.72rem;
      font-weight: 700;
      padding: 3px 8px;
      border-radius: 5px;
    }

    .video-info { padding: 15px; }
    .video-title {
      font-size: 0.93rem;
      font-weight: 700;
      margin-bottom: 14px;
      color: #e8e8e8;
      line-height: 1.5;
      display: -webkit-box;
      -webkit-line-clamp: 2;
      -webkit-box-orient: vertical;
      overflow: hidden;
    }

    .btn-watch {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      width: 100%;
      padding: 11px;
      background: rgba(232,0,29,0.08);
      color: var(--red);
      text-align: center;
      text-decoration: none;
      border: 1px solid rgba(232,0,29,0.25);
      border-radius: 9px;
      font-size: 0.88rem;
      font-weight: 700;
      transition: 0.25s;
    }
    .btn-watch:hover { background: var(--red); color: white; border-color: var(--red); }
    .btn-watch svg { width: 16px; height: 16px; fill: currentColor; }

    /* ── FOOTER ── */
    footer {
      padding: 36px 6%;
      text-align: center;
      color: #3a3a3a;
      border-top: 1px solid var(--border);
      font-size: 0.85rem;
    }
    footer a { color: var(--red); text-decoration: none; }

    /* ── SCROLLBAR ── */
    ::-webkit-scrollbar { width: 6px; }
    ::-webkit-scrollbar-track { background: var(--black); }
    ::-webkit-scrollbar-thumb { background: var(--red-dim); border-radius: 3px; }

    @media (max-width: 600px) {
      .stats { flex-direction: column; }
      .stat { border-left: none; border-bottom: 1px solid var(--border); }
      .stat:last-child { border-bottom: none; }
    }
  </style>
</head>
<body>

  <!-- HEADER -->
  <header>
    <div class="logo-area">
      <div class="logo-ring">
        <svg viewBox="0 0 44 44" fill="none">
          <circle cx="22" cy="22" r="20" stroke="#E8001D" stroke-width="1.5" stroke-dasharray="4 3"/>
        </svg>
        <img src="https://yt3.googleusercontent.com/6XzWsh-u0E1v73R8t0C9R-x_6L5uS_SjX4J-8V8kX_n7uC-Zq5H8fG-z1W5G-W5G-W5G-W5G=s176-c-k-c0x00ffffff-no-rj" alt="Logo" onerror="this.style.background='#E8001D';this.alt='I'">
      </div>
      <span class="brand-name">islam<span>_3LN</span></span>
    </div>
    <a href="https://youtube.com/@luxx_islam_pro" target="_blank" class="nav-link">قناتي الرسمية ↗</a>
  </header>

  <!-- HERO -->
  <section class="hero">
    <div class="hero-bg"></div>
    <div class="hero-grid"></div>

    <div class="hero-badge">🎬 &nbsp;بوابة الاحتراف في المونتاج</div>

    <h1>احترف المونتاج و<em>صناعة المحتوى</em></h1>
    <p>تعلّم أسرار Alight Motion و InShot و CapCut من الصفر حتى الاحتراف مع أفضل الشروحات بالعربي.</p>

    <div class="hero-cta">
      <a href="https://youtube.com/@luxx_islam_pro" target="_blank" class="btn-primary">تابع القناة</a>
      <a href="https://t.me/islam3ln" target="_blank" class="btn-secondary">📥 قناة التلغرام</a>
    </div>
  </section>

  <!-- STATS -->
  <div class="stats">
    <div class="stat">
      <span class="stat-num">10+</span>
      <span class="stat-label">شروحات مختارة</span>
    </div>
    <div class="stat">
      <span class="stat-num">3</span>
      <span class="stat-label">تطبيقات محترفة</span>
    </div>
    <div class="stat">
      <span class="stat-num">100%</span>
      <span class="stat-label">محتوى مجاني</span>
    </div>
    <div class="stat">
      <span class="stat-num">🔥</span>
      <span class="stat-label">كورسات ريلز</span>
    </div>
  </div>

  <!-- TELEGRAM BANNER -->
  <div class="telegram-wrap">
    <a href="https://t.me/islam3ln" class="telegram-banner" target="_blank">
      <div class="tg-icon">📥</div>
      <span>اضغط هنا لتحميل ملحقات المونتاج المجانية من قناة التلغرام</span>
    </a>
  </div>

  <!-- VIDEOS -->
  <div class="section-header">
    <div class="section-bar"></div>
    <h2>شروحات يوتيوب المختارة</h2>
    <div class="section-line"></div>
  </div>

  <div class="videos-grid">

    <div class="video-card" style="animation-delay:0.05s">
      <div class="thumbnail-container">
        <img src="https://i.ytimg.com/vi/wwkB8KWByPQ/sddefault.jpg" alt="thumbnail" loading="lazy">
        <div class="play-overlay"><div class="play-btn"><svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg></div></div>
      </div>
      <div class="video-info">
        <p class="video-title">كيف تصمم مقدمة احترافية بالهاتف باستخدام Alight Motion</p>
        <a href="https://youtu.be/wwkB8KWByPQ" class="btn-watch" target="_blank">
          <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg> مشاهدة الشرح
        </a>
      </div>
    </div>

    <div class="video-card" style="animation-delay:0.1s">
      <div class="thumbnail-container">
        <img src="https://i.ytimg.com/vi/TZhNJqZbDwI/sddefault.jpg" alt="thumbnail" loading="lazy">
        <div class="play-overlay"><div class="play-btn"><svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg></div></div>
      </div>
      <div class="video-info">
        <p class="video-title">كيف تصنع إعلان 3D احترافي على لايت موشن</p>
        <a href="https://youtu.be/TZhNJqZbDwI" class="btn-watch" target="_blank">
          <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg> مشاهدة الشرح
        </a>
      </div>
    </div>

    <div class="video-card" style="animation-delay:0.15s">
      <div class="thumbnail-container">
        <img src="https://i.ytimg.com/vi/PahY-vvDYwE/maxresdefault.jpg" alt="thumbnail" loading="lazy">
        <div class="play-overlay"><div class="play-btn"><svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg></div></div>
      </div>
      <div class="video-info">
        <p class="video-title">أسرار في تطبيق inshot يخفيها عنك المحترفون</p>
        <a href="https://youtu.be/PahY-vvDYwE" class="btn-watch" target="_blank">
          <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg> مشاهدة الشرح
        </a>
      </div>
    </div>

    <div class="video-card" style="animation-delay:0.2s">
      <div class="thumbnail-container">
        <img src="https://i.ytimg.com/vi/-iDrVYWBXNo/sddefault.jpg" alt="thumbnail" loading="lazy">
        <div class="play-overlay"><div class="play-btn"><svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg></div></div>
      </div>
      <div class="video-info">
        <p class="video-title">كيفية عمل انترو احترافي في Alight Motion (شرح كامل)</p>
        <a href="https://youtu.be/-iDrVYWBXNo" class="btn-watch" target="_blank">
          <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg> مشاهدة الشرح
        </a>
      </div>
    </div>

    <div class="video-card" style="animation-delay:0.25s">
      <div class="thumbnail-container">
        <img src="https://i.ytimg.com/vi/timNK3PEAdI/sddefault.jpg" alt="thumbnail" loading="lazy">
        <div class="play-overlay"><div class="play-btn"><svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg></div></div>
      </div>
      <div class="video-info">
        <p class="video-title">شرح مونتاج مقدمة احترافية بتطبيق inshot (أساسيات)</p>
        <a href="https://youtu.be/timNK3PEAdI" class="btn-watch" target="_blank">
          <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg> مشاهدة الشرح
        </a>
      </div>
    </div>

    <div class="video-card" style="animation-delay:0.3s">
      <div class="thumbnail-container">
        <img src="https://i.ytimg.com/vi/6Rz5AcXRIh4/maxresdefault.jpg" alt="thumbnail" loading="lazy">
        <div class="play-overlay"><div class="play-btn"><svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg></div></div>
      </div>
      <div class="video-info">
        <p class="video-title">شرح كيفية مونتاج ريلز احترافي بالهاتف (كورس مجاني)</p>
        <a href="https://youtu.be/6Rz5AcXRIh4" class="btn-watch" target="_blank">
          <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg> مشاهدة الشرح
        </a>
      </div>
    </div>

    <div class="video-card" style="animation-delay:0.35s">
      <div class="thumbnail-container">
        <img src="https://i.ytimg.com/vi/cvNhaYeQe6Q/sddefault.jpg" alt="thumbnail" loading="lazy">
        <div class="play-overlay"><div class="play-btn"><svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg></div></div>
      </div>
      <div class="video-info">
        <p class="video-title">شرح تأثير الكاميرا 3D على لايت موشن</p>
        <a href="https://youtu.be/cvNhaYeQe6Q" class="btn-watch" target="_blank">
          <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg> مشاهدة الشرح
        </a>
      </div>
    </div>

    <div class="video-card" style="animation-delay:0.4s">
      <div class="thumbnail-container">
        <img src="https://i.ytimg.com/vi/4UGT0JR-RiU/maxresdefault.jpg" alt="thumbnail" loading="lazy">
        <div class="play-overlay"><div class="play-btn"><svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg></div></div>
      </div>
      <div class="video-info">
        <p class="video-title">5 خطوات لتسريع المونتاج وإنجاز الفيديو بسرعة ⚡</p>
        <a href="https://youtu.be/4UGT0JR-RiU" class="btn-watch" target="_blank">
          <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg> مشاهدة الشرح
        </a>
      </div>
    </div>

    <div class="video-card" style="animation-delay:0.45s">
      <div class="thumbnail-container">
        <img src="https://i.ytimg.com/vi/qjg4Eh3MAvg/sddefault.jpg" alt="thumbnail" loading="lazy">
        <div class="play-overlay"><div class="play-btn"><svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg></div></div>
      </div>
      <div class="video-info">
        <p class="video-title">تصميم صورة مصغرة احترافية بالهاتف فقط 🔥</p>
        <a href="https://youtu.be/qjg4Eh3MAvg" class="btn-watch" target="_blank">
          <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg> مشاهدة الشرح
        </a>
      </div>
    </div>

    <div class="video-card" style="animation-delay:0.5s">
      <div class="thumbnail-container">
        <img src="https://i.ytimg.com/vi/Iri6wMX0Tr0/sddefault.jpg" alt="thumbnail" loading="lazy">
        <div class="play-overlay"><div class="play-btn"><svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg></div></div>
      </div>
      <div class="video-info">
        <p class="video-title">أفضل طريقة لعمل ريلز احترافي باستخدام إنشوت</p>
        <a href="https://youtu.be/Iri6wMX0Tr0" class="btn-watch" target="_blank">
          <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg> مشاهدة الشرح
        </a>
      </div>
    </div>

  </div>

  <!-- FOOTER -->
  <footer>
    <p>© 2026 جميع الحقوق محفوظة &nbsp;·&nbsp; <a href="https://youtube.com/@luxx_islam_pro" target="_blank">islam_3LN</a> &nbsp;·&nbsp; بوابة المونتاج الاحترافي</p>
  </footer>

</body>
</html>

