<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>سوق العتبة — كل سوق العتبة في تطبيق واحد</title>
<meta name="description" content="تطبيق سوق العتبة: ملابس حريمي، رجالي، أطفالي، عطور وإكسسوارات بأسعار الجملة من موردين موثوقين." />
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Changa:wght@500;600;700;800&family=Cairo:wght@400;500;600;700;800&family=Tajawal:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --navy: #0B1B42;
    --navy-deep: #071230;
    --maroon: #6E1029;
    --amber: #FF7A29;
    --gold: #E8B33D;
    --cream: #F7F1E6;
    --cream-2: #EFE6D4;
    --ink: #181522;
    --paper: #FFFDF9;
    --line: rgba(11,27,66,0.12);
  }

  *{ box-sizing: border-box; margin:0; padding:0; }

  html{ scroll-behavior: smooth; }

  body{
    font-family: 'Cairo', sans-serif;
    background: var(--paper);
    color: var(--ink);
    overflow-x: hidden;
    -webkit-font-smoothing: antialiased;
  }

  img{ max-width:100%; display:block; }

  .display{
    font-family: 'Changa', sans-serif;
    font-weight: 700;
    letter-spacing: 0.5px;
  }

  .eyebrow{
    font-family: 'Tajawal', sans-serif;
    font-weight: 500;
    font-size: 0.78rem;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    color: var(--gold);
    display:flex;
    align-items:center;
    gap:10px;
  }
  .eyebrow::before{
    content:"";
    width:22px; height:2px;
    background: var(--gold);
    display:inline-block;
  }

  .wrap{
    max-width: 1220px;
    margin: 0 auto;
    padding: 0 28px;
  }

  a{ color:inherit; text-decoration:none; }

  /* ===== Header ===== */
  header{
    position: sticky;
    top:0;
    z-index: 50;
    background: var(--navy);
    border-bottom: 1px solid rgba(255,255,255,0.08);
  }
  .nav{
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding: 16px 28px;
    max-width:1220px;
    margin:0 auto;
  }
  .logo{
    display:flex;
    align-items:center;
    gap:10px;
    font-family:'Changa', sans-serif;
    font-weight:700;
    font-size:1.35rem;
    color:#fff;
  }
  .logo .dot{
    width:10px; height:10px;
    border-radius:50%;
    background: var(--amber);
    box-shadow: 0 0 10px var(--amber);
  }
  .nav-links{
    display:flex;
    gap:30px;
    font-family:'Tajawal',sans-serif;
    font-size:0.95rem;
    color: rgba(255,255,255,0.75);
  }
  .nav-links a:hover{ color: var(--gold); }
  .nav-cta{
    background: var(--amber);
    color:#1a0d00;
    font-family:'Cairo',sans-serif;
    font-weight:700;
    font-size:0.9rem;
    padding: 10px 22px;
    border-radius: 30px;
    white-space:nowrap;
  }
  .nav-cta:hover{ filter:brightness(1.08); }

  @media (max-width: 760px){
    .nav-links{ display:none; }
  }

  /* ===== Hero ===== */
  .hero{
    background: radial-gradient(120% 100% at 80% 0%, #142a63 0%, var(--navy) 45%, var(--navy-deep) 100%);
    color:#fff;
    padding: 86px 0 0;
    position:relative;
    overflow:hidden;
  }
  .hero::after{
    content:"";
    position:absolute;
    inset:0;
    background:
      radial-gradient(circle at 12% 20%, rgba(232,179,61,0.10), transparent 40%),
      radial-gradient(circle at 90% 60%, rgba(255,122,41,0.12), transparent 45%);
    pointer-events:none;
  }
  .hero-grid{
    display:grid;
    grid-template-columns: 1.05fr 0.95fr;
    gap: 40px;
    align-items:center;
    position:relative;
    z-index:2;
  }
  @media (max-width: 940px){
    .hero-grid{ grid-template-columns: 1fr; text-align:center; }
    .hero-copy{ order:1; }
    .hero-art{ order:2; }
  }

  .hero h1{
    font-size: clamp(2.6rem, 5.6vw, 4.4rem);
    line-height: 1.05;
    color:#fff;
    text-shadow: 0 0 26px rgba(232,179,61,0.35);
  }
  .hero h1 span{
    color: var(--gold);
    text-shadow: 0 0 18px rgba(232,179,61,0.65), 0 0 40px rgba(232,179,61,0.35);
  }
  .hero p.lead{
    margin-top: 22px;
    font-size: 1.12rem;
    line-height: 1.9;
    color: rgba(255,255,255,0.78);
    max-width: 540px;
  }
  @media (max-width: 940px){ .hero p.lead{ margin-inline:auto; } }

  .hero-actions{
    display:flex;
    gap:16px;
    margin-top: 34px;
    flex-wrap:wrap;
  }
  @media (max-width: 940px){ .hero-actions{ justify-content:center; } }

  .btn-primary{
    background: var(--amber);
    color:#1a0d00;
    font-weight:800;
    padding: 15px 34px;
    border-radius: 14px;
    font-size:1.02rem;
    box-shadow: 0 14px 30px -10px rgba(255,122,41,0.55);
  }
  .btn-primary:hover{ filter:brightness(1.06); transform: translateY(-1px); }

  .btn-ghost{
    border: 1.5px solid rgba(255,255,255,0.35);
    color:#fff;
    padding: 15px 30px;
    border-radius: 14px;
    font-weight:700;
    font-size:1.02rem;
  }
  .btn-ghost:hover{ background: rgba(255,255,255,0.08); }

  .hero-stats{
    display:flex;
    gap:34px;
    margin-top: 46px;
    flex-wrap:wrap;
  }
  @media (max-width: 940px){ .hero-stats{ justify-content:center; } }
  .hero-stats div b{
    display:block;
    font-family:'Changa',sans-serif;
    font-size:1.7rem;
    color: var(--gold);
  }
  .hero-stats div span{
    font-family:'Tajawal',sans-serif;
    font-size:0.85rem;
    color: rgba(255,255,255,0.65);
  }

  /* phone frame for hero */
  .hero-art{
    display:flex;
    justify-content:center;
    position:relative;
  }
  .phone-frame{
    width: 270px;
    border-radius: 38px;
    background: #050b1f;
    padding: 10px;
    box-shadow:
      0 30px 70px -20px rgba(0,0,0,0.6),
      0 0 0 1px rgba(255,255,255,0.06),
      0 0 60px rgba(232,179,61,0.18);
    position:relative;
  }
  .phone-frame img{
    border-radius: 28px;
    width:100%;
    display:block;
  }
  .phone-frame .notch{
    position:absolute;
    top:18px; left:50%;
    transform:translateX(-50%);
    width: 90px; height:18px;
    background:#050b1f;
    border-radius: 12px;
    z-index:3;
  }
  .glow-ring{
    position:absolute;
    width:380px; height:380px;
    border-radius:50%;
    border: 1px dashed rgba(232,179,61,0.28);
    top:50%; left:50%;
    transform:translate(-50%,-50%);
    animation: spin 26s linear infinite;
  }
  @keyframes spin{ to{ transform:translate(-50%,-50%) rotate(360deg); } }

  /* ===== Marquee ===== */
  .marquee-band{
    background: var(--navy-deep);
    border-top: 1px solid rgba(255,255,255,0.06);
    border-bottom: 1px solid rgba(255,255,255,0.06);
    overflow:hidden;
    padding: 16px 0;
    position:relative;
    z-index:2;
  }
  .marquee-track{
    display:flex;
    width: max-content;
    animation: scroll-rtl 28s linear infinite;
  }
  .marquee-track span{
    font-family:'Changa',sans-serif;
    font-size:1.05rem;
    color: var(--gold);
    padding: 0 26px;
    white-space:nowrap;
    text-shadow: 0 0 12px rgba(232,179,61,0.45);
    display:flex;
    align-items:center;
    gap:26px;
  }
  .marquee-track span::after{ content:"✦"; color: rgba(255,122,41,0.7); }
  @keyframes scroll-rtl{
    from{ transform: translateX(0); }
    to{ transform: translateX(-50%); }
  }
  @media (prefers-reduced-motion: reduce){
    .marquee-track{ animation: none; }
    .glow-ring{ animation: none; }
  }

  /* ===== Section generic ===== */
  section{ padding: 96px 0; }
  .section-head{
    max-width: 680px;
    margin-bottom: 56px;
  }
  .section-head h2{
    font-size: clamp(1.9rem, 3.4vw, 2.6rem);
    margin-top: 14px;
    color: var(--navy);
  }
  .section-head p{
    margin-top: 16px;
    color: #585369;
    font-size: 1.05rem;
    line-height:1.9;
  }

  /* ===== Features ===== */
  .features{ background: var(--cream); }
  .feature-grid{
    display:grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 22px;
  }
  @media (max-width: 980px){ .feature-grid{ grid-template-columns: repeat(2,1fr); } }
  @media (max-width: 600px){ .feature-grid{ grid-template-columns: 1fr; } }

  .feature-card{
    background: var(--paper);
    border: 1px solid var(--line);
    border-radius: 18px;
    padding: 30px 26px;
    position:relative;
    transition: transform .25s ease, box-shadow .25s ease;
  }
  .feature-card:hover{
    transform: translateY(-4px);
    box-shadow: 0 18px 30px -18px rgba(11,27,66,0.25);
  }
  .feature-card .icon{
    width:46px; height:46px;
    border-radius: 12px;
    background: var(--navy);
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:1.3rem;
    margin-bottom:18px;
    color: var(--gold);
  }
  .feature-card h3{
    font-family:'Changa',sans-serif;
    font-size:1.2rem;
    color: var(--navy);
    margin-bottom:10px;
  }
  .feature-card p{
    font-size:0.96rem;
    line-height:1.8;
    color:#5a5468;
  }

  /* ===== Screens gallery ===== */
  .screens{ background: var(--paper); }
  .screen-grid{
    display:grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 38px 28px;
  }
  @media (max-width: 940px){ .screen-grid{ grid-template-columns: repeat(2,1fr); } }
  @media (max-width: 600px){ .screen-grid{ grid-template-columns: 1fr; max-width:320px; margin:0 auto; } }

  .screen-card{ text-align:center; }
  .screen-shell{
    background: #050b1f;
    border-radius: 30px;
    padding: 9px;
    box-shadow: 0 22px 40px -18px rgba(11,27,66,0.35);
    position:relative;
  }
  .screen-shell .notch{
    position:absolute;
    top:14px; left:50%; transform:translateX(-50%);
    width:70px; height:14px;
    background:#050b1f; border-radius:10px; z-index:3;
  }
  .screen-shell img{ border-radius: 22px; }
  .screen-tag{
    display:inline-block;
    margin-top: 18px;
    font-family:'Tajawal',sans-serif;
    font-size:0.82rem;
    color: var(--navy);
    background: var(--cream-2);
    padding: 6px 16px;
    border-radius: 20px;
    border: 1px solid var(--line);
  }

  /* ===== Category signage band ===== */
  .signage{
    background: linear-gradient(160deg, var(--maroon) 0%, #4d0c1c 100%);
    color:#fff;
  }
  .signage .section-head h2{ color:#fff; }
  .signage .section-head p{ color: rgba(255,255,255,0.75); }
  .signage .eyebrow{ color: var(--gold); }

  .sign-grid{
    display:flex;
    flex-wrap:wrap;
    gap: 14px;
  }
  .sign-tile{
    font-family:'Changa',sans-serif;
    font-size: 1.02rem;
    padding: 14px 24px;
    border-radius: 12px;
    border: 1.5px solid rgba(232,179,61,0.55);
    color: var(--gold);
    text-shadow: 0 0 10px rgba(232,179,61,0.45);
    background: rgba(255,255,255,0.03);
    transition: all .2s ease;
  }
  .sign-tile:hover{
    background: rgba(232,179,61,0.12);
    box-shadow: 0 0 24px rgba(232,179,61,0.25);
    transform: translateY(-2px);
  }

  /* ===== CTA ===== */
  .cta{
    background: var(--navy);
    color:#fff;
    text-align:center;
  }
  .cta h2{
    font-size: clamp(2rem, 4vw, 3rem);
    color:#fff;
  }
  .cta h2 span{ color: var(--gold); }
  .cta p{
    margin: 18px auto 36px;
    color: rgba(255,255,255,0.75);
    max-width: 560px;
    font-size: 1.05rem;
    line-height:1.85;
  }
  .cta-actions{
    display:flex;
    gap:16px;
    justify-content:center;
    flex-wrap:wrap;
  }

  /* ===== Footer ===== */
  footer{
    background: var(--navy-deep);
    color: rgba(255,255,255,0.55);
    padding: 34px 0;
    font-family:'Tajawal',sans-serif;
    font-size: 0.88rem;
  }
  .foot-row{
    display:flex;
    justify-content:space-between;
    align-items:center;
    flex-wrap:wrap;
    gap:14px;
  }
  footer a:hover{ color: var(--gold); }
</style>
</head>
<body>

<header>
  <div class="nav">
    <div class="logo"><span class="dot"></span> سوق العتبة</div>
    <nav class="nav-links">
      <a href="#features">المميزات</a>
      <a href="#screens">الشاشات</a>
      <a href="#categories">الأقسام</a>
    </nav>
    <a class="nav-cta" href="#cta">حمّل التطبيق</a>
  </div>
</header>

<section class="hero">
  <div class="wrap hero-grid">
    <div class="hero-copy">
      <div class="eyebrow">تطبيق تسوق بسعر الجملة</div>
      <h1 class="display">كل سوق العتبة<br><span>في تطبيق واحد</span></h1>
      <p class="lead">
        ملابس حريمي، رجالي وأطفالي، عطور، مستحضرات تجميل، حقائب وإكسسوارات — كل ده من موردين حقيقيين، بالكود والسعر واضحين قدامك، وزرار حجز واحد يقرّبك من البضاعة بدل ما تلف على المحلات.
      </p>
      <div class="hero-actions">
        <a class="btn-primary" href="#cta">حمّل التطبيق الآن</a>
        <a class="btn-ghost" href="#screens">شاهد لقطات الشاشة</a>
      </div>
      <div class="hero-stats">
        <div><b>8+</b><span>أقسام رئيسية</span></div>
        <div><b>فلترة</b><span>بالقسم واللون والمقاس والسعر</span></div>
        <div><b>حجز</b><span>بضغطة واحدة لكل منتج</span></div>
      </div>
    </div>
    <div class="hero-art">
      <div class="glow-ring"></div>
      <div class="phone-frame">
        <div class="notch"></div>
        <img src="screenshots/01-home.jpg" alt="الشاشة الرئيسية لتطبيق سوق العتبة">
      </div>
    </div>
  </div>

  <div class="marquee-band">
    <div class="marquee-track">
      <span>ملابس حريمي</span><span>ملابس رجالي</span><span>ملابس الاطفالي</span><span>عطور</span><span>مستحضرات التجميل</span><span>الحقائب</span><span>أحذية</span><span>الإكسسوارات</span>
      <span>ملابس حريمي</span><span>ملابس رجالي</span><span>ملابس الاطفالي</span><span>عطور</span><span>مستحضرات التجميل</span><span>الحقائب</span><span>أحذية</span><span>الإكسسوارات</span>
    </div>
  </div>
</section>

<section class="features" id="features">
  <div class="wrap">
    <div class="section-head">
      <div class="eyebrow">ليه سوق العتبة</div>
      <h2 class="display">تسوق منظّم بروح السوق الحقيقي</h2>
      <p>نفس دفعة العتبة وتنوّعها، لكن من غير زحمة ولا لفّ. كل ميزة في التطبيق مبنية على اللي يحصل بالفعل وقت الشراء بالجملة.</p>
    </div>
    <div class="feature-grid">
      <div class="feature-card">
        <div class="icon">⌕</div>
        <h3 class="display">فلترة دقيقة</h3>
        <p>فلتر بالقسم، اللون، المقاس، ونطاق السعر من جنيه واحد لحد 10000 جنيه، علشان توصل لقطعتك في ثواني.</p>
      </div>
      <div class="feature-card">
        <div class="icon">▣</div>
        <h3 class="display">أقسام واضحة</h3>
        <p>من الملابس الحريمي والرجالي للعطور والحقائب والإكسسوارات، كل قسم له واجهته وصوره الخاصة.</p>
      </div>
      <div class="feature-card">
        <div class="icon">🛍</div>
        <h3 class="display">حجز بضغطة</h3>
        <p>زرار "حجز" واحد تحت كل منتج، مع السعر والكود ظاهرين قبل ما تقرر، بلا مفاوضة ولا تخمين.</p>
      </div>
      <div class="feature-card">
        <div class="icon">⚙</div>
        <h3 class="display">حسابك في إيدك</h3>
        <p>الطلبات، المرتجعات، المفضلة، والموردين المفضلين في قائمة واحدة سهلة الوصول من أي شاشة.</p>
      </div>
    </div>
  </div>
</section>

<section class="screens" id="screens">
  <div class="wrap">
    <div class="section-head">
      <div class="eyebrow">جولة في التطبيق</div>
      <h2 class="display">تجوّل في السوق من شاشتك</h2>
      <p>ست شاشات حقيقية من التطبيق، من أول ما تفتحه لحد ما تحجز أول قطعة.</p>
    </div>
    <div class="screen-grid">
      <div class="screen-card">
        <div class="screen-shell"><div class="notch"></div><img src="screenshots/01-home.jpg" alt="الشاشة الرئيسية"></div>
        <span class="screen-tag">الواجهة الرئيسية</span>
      </div>
      <div class="screen-card">
        <div class="screen-shell"><div class="notch"></div><img src="screenshots/02-categories.jpg" alt="شاشة الأقسام"></div>
        <span class="screen-tag">الأقسام</span>
      </div>
      <div class="screen-card">
        <div class="screen-shell"><div class="notch"></div><img src="screenshots/03-category-detail.jpg" alt="قسم ملابس حريمي"></div>
        <span class="screen-tag">ملابس حريمي</span>
      </div>
      <div class="screen-card">
        <div class="screen-shell"><div class="notch"></div><img src="screenshots/04-search-results.jpg" alt="نتائج البحث والمنتجات"></div>
        <span class="screen-tag">نتائج البحث</span>
      </div>
      <div class="screen-card">
        <div class="screen-shell"><div class="notch"></div><img src="screenshots/05-filter.jpg" alt="شاشة الفلتر"></div>
        <span class="screen-tag">الفلتر</span>
      </div>
      <div class="screen-card">
        <div class="screen-shell"><div class="notch"></div><img src="screenshots/06-account.jpg" alt="شاشة الحساب والقائمة"></div>
        <span class="screen-tag">حسابي</span>
      </div>
    </div>
  </div>
</section>

<section class="signage" id="categories">
  <div class="wrap">
    <div class="section-head">
      <div class="eyebrow">واجهات السوق</div>
      <h2 class="display">أقسام بتلمع زي يافطات العتبة</h2>
      <p>كل قسم في التطبيق له يافطته الخاصة، بنفس روح اللافتات النيون اللي تميّز شوارع العتبة.</p>
    </div>
    <div class="sign-grid">
      <span class="sign-tile">ملابس حريمي</span>
      <span class="sign-tile">ملابس رجالي</span>
      <span class="sign-tile">ملابس الاطفالي</span>
      <span class="sign-tile">عطور</span>
      <span class="sign-tile">مستحضرات التجميل</span>
      <span class="sign-tile">الحقائب</span>
      <span class="sign-tile">أحذية</span>
      <span class="sign-tile">الإكسسوارات</span>
      <span class="sign-tile">بناطيل وجينزات</span>
      <span class="sign-tile">عبايات خليجي</span>
      <span class="sign-tile">لانجري</span>
      <span class="sign-tile">زي شرعي</span>
    </div>
  </div>
</section>

<section class="cta" id="cta">
  <div class="wrap">
    <h2 class="display">جاهز تتسوق <span>زي أهل العتبة؟</span></h2>
    <p>حمّل تطبيق سوق العتبة وابدأ تتفرج على المنتجات، تفلتر براحتك، وتحجز اللي يعجبك بسعر واضح.</p>
    <div class="cta-actions">
      <a class="btn-primary" href="#">حمّل التطبيق</a>
      <a class="btn-ghost" href="https://github.com/" target="_blank" rel="noopener">مشروع GitHub</a>
    </div>
  </div>
</section>

<footer>
  <div class="wrap foot-row">
    <span>© سوق العتبة — صفحة عرض للتطبيق</span>
    <span><a href="#screens">الشاشات</a> · <a href="#features">المميزات</a> · <a href="#categories">الأقسام</a></span>
  </div>
</footer>

</body>
</html>
