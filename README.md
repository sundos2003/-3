<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>حيواناتي | موسوعة وعالم الحيوانات</title>
  <meta name="description" content="موقع عربي احترافي عن الحيوانات: مقالات وصور وفيديوهات وفئات مرتبة مع وسائل تواصل مباشرة عبر إنستغرام وواتساب وتليجرام والبريد." />
  <meta name="theme-color" content="#0ea5e9" />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;800&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#0b1220;          /* خلفية داكنة أنيقة */
      --panel:#111a2b;
      --muted:#7aa2c9;
      --accent:#22d3ee;      /* سماوي */
      --accent-2:#38bdf8;    /* أزرق فاتح */
      --text:#eaf2fb;
      --shadow:0 10px 25px rgba(0,0,0,.35);
      --radius:18px;
    }
    *{box-sizing:border-box}
    html,body{margin:0;height:100%;background:radial-gradient(1200px 800px at 90% -10%, rgba(56,189,248,.20), transparent), var(--bg);color:var(--text);font-family:"Cairo", system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif}
    a{color:inherit;text-decoration:none}
    img{max-width:100%;display:block}

    /* شريط علوي */
    .nav{position:sticky;top:0;z-index:50;backdrop-filter:saturate(1.2) blur(8px);background:linear-gradient(180deg, rgba(11,18,32,.85), rgba(11,18,32,.55));border-bottom:1px solid rgba(255,255,255,.06)}
    .container{max-width:1200px;margin:auto;padding:0 20px}
    .nav-inner{display:flex;align-items:center;justify-content:space-between;height:68px}
    .brand{display:flex;align-items:center;gap:10px;font-weight:800;letter-spacing:.2px}
    .brand .logo{width:40px;height:40px;border-radius:50%;display:grid;place-items:center;background:linear-gradient(135deg,var(--accent),var(--accent-2));box-shadow:var(--shadow)}
    .nav-links{display:flex;gap:18px}
    .nav-links a{opacity:.9;padding:8px 12px;border-radius:12px}
    .nav-links a:hover{background:rgba(255,255,255,.06);opacity:1}
    .cta{display:flex;gap:10px}
    .btn{display:inline-flex;align-items:center;gap:8px;padding:10px 16px;border-radius:14px;font-weight:700;border:1px solid rgba(255,255,255,.12);background:rgba(255,255,255,.04);box-shadow:var(--shadow);transition:.25s}
    .btn:hover{transform:translateY(-2px);background:rgba(255,255,255,.08)}
    .btn.primary{background:linear-gradient(135deg,var(--accent),var(--accent-2));color:#07263a;border:none}

    /* البطل */
    .hero{position:relative;overflow:hidden}
    .hero .wrap{display:grid;grid-template-columns:1.1fr .9fr;gap:24px;align-items:center;padding:56px 0 36px}
    .hero h1{font-size:clamp(28px,5vw,44px);margin:0 0 12px;line-height:1.2}
    .hero p{margin:0 0 20px;color:var(--muted)}
    .hero .actions{display:flex;gap:12px;flex-wrap:wrap}
    .hero-visual{position:relative;border-radius:var(--radius);overflow:hidden;min-height:320px;background:#06101f;border:1px solid rgba(255,255,255,.06);box-shadow:var(--shadow)}
    .hero-visual img{width:100%;height:100%;object-fit:cover;opacity:.9}
    .glass{position:absolute;inset:auto 16px 16px 16px;background:rgba(6,16,31,.6);border:1px solid rgba(255,255,255,.08);border-radius:16px;padding:12px;display:flex;gap:10px;flex-wrap:wrap}

    /* أقسام */
    section{padding:52px 0}
    .section-title{display:flex;align-items:center;justify-content:space-between;margin-bottom:22px}
    .section-title h2{margin:0;font-size:clamp(22px,3.4vw,32px)}
    .muted{color:var(--muted)}

    /* بطاقات الفئات */
    .grid{display:grid;gap:16px}
    .grid.cols-5{grid-template-columns:repeat(5,1fr)}
    @media (max-width:1100px){.grid.cols-5{grid-template-columns:repeat(3,1fr)}}
    @media (max-width:700px){.hero .wrap{grid-template-columns:1fr}.grid.cols-5{grid-template-columns:repeat(2,1fr)}}
    @media (max-width:460px){.grid.cols-5{grid-template-columns:1fr}}

    .card{position:relative;overflow:hidden;border-radius:20px;background:linear-gradient(180deg, rgba(255,255,255,.04), rgba(255,255,255,.02));border:1px solid rgba(255,255,255,.06);box-shadow:var(--shadow);min-height:180px}
    .card img{position:absolute;inset:0;object-fit:cover;filter:saturate(1.05) contrast(1.05) brightness(.92)}
    .card .label{position:absolute;inset:auto 12px 12px 12px;background:rgba(0,0,0,.45);backdrop-filter:blur(6px);padding:10px 12px;border-radius:14px;border:1px solid rgba(255,255,255,.08);display:flex;align-items:center;justify-content:space-between;gap:10px}
    .chip{font-size:13px;opacity:.9}

    /* المعرض */
    .gallery{display:grid;grid-template-columns:repeat(12,1fr);gap:12px}
    .gallery .g{border-radius:16px;overflow:hidden;border:1px solid rgba(255,255,255,.06);box-shadow:var(--shadow)}
    .gallery .g img{height:100%;width:100%;object-fit:cover}
    .gallery .g.big{grid-column:span 6;min-height:260px}
    .gallery .g.sm{grid-column:span 3;min-height:180px}
    @media (max-width:900px){.gallery .g.big{grid-column:span 12}.gallery .g.sm{grid-column:span 6}}
    @media (max-width:520px){.gallery .g.sm{grid-column:span 12}}

    /* تواصل */
    .contact{display:grid;grid-template-columns:1fr 1fr;gap:18px}
    @media (max-width:900px){.contact{grid-template-columns:1fr}}
    .panel{background:linear-gradient(180deg, rgba(255,255,255,.04), rgba(255,255,255,.02));border:1px solid rgba(255,255,255,.06);border-radius:20px;padding:18px;box-shadow:var(--shadow)}
    .socials{display:grid;grid-template-columns:repeat(2,1fr);gap:12px}
    .social{display:flex;align-items:center;gap:10px;padding:12px;border-radius:14px;background:rgba(255,255,255,.04);border:1px solid rgba(255,255,255,.06)}
    .social:hover{background:rgba(255,255,255,.07)}
    .social svg{width:22px;height:22px}

    /* نموذج */
    .form{display:grid;gap:10px}
    .input{width:100%;padding:12px 14px;border-radius:12px;background:#0a1323;color:var(--text);border:1px solid rgba(255,255,255,.08)}
    textarea.input{min-height:120px;resize:vertical}
    .footer{padding:32px 0;color:#8fb4d3;border-top:1px solid rgba(255,255,255,.06)}
  </style>
</head>
<body>
  <!-- شريط علوي -->
  <header class="nav">
    <div class="container nav-inner">
      <a class="brand" href="#top">
        <span class="logo" aria-hidden="true">🐾</span>
        <span>حيواناتي</span>
      </a>
      <nav class="nav-links">
        <a href="#about">عن الموقع</a>
        <a href="#categories">الفئات</a>
        <a href="#gallery">المعرض</a>
        <a href="#contact">تواصل</a>
      </nav>
      <div class="cta">
        <a class="btn" href="https://wa.me/782667989" target="_blank" rel="noopener">واتساب</a>
        <a class="btn primary" href="https://www.instagram.com/sndsalbhyry0?igsh=MWc2ZWRyNDcydm1wNg==" target="_blank" rel="noopener">إنستغرام</a>
      </div>
    </div>
  </header>

  <!-- البطل -->
  <section class="hero" id="top">
    <div class="container wrap">
      <div>
        <h1>عالم الحيوانات — موسوعة مبسطة، صور مبهرة، ومعلومات دقيقة</h1>
        <p>اكتشف تنوع المملكة الحيوانية: من الثدييات المفترسة إلى الكائنات البحرية العميقة. محتوى مُنظم، صور عالية الجودة، وروابط مباشرة للتواصل.</p>
        <div class="actions">
          <a class="btn primary" href="#categories">استكشف الفئات</a>
          <a class="btn" href="#gallery">تصفح المعرض</a>
        </div>
      </div>
      <div class="hero-visual">
        <img alt="لقطة فنية لحيوانات متنوعة" src="https://images.unsplash.com/photo-1546182990-dffeafbe841d?q=80&w=1600&auto=format&fit=crop"/>
        <div class="glass">
          <span class="chip">مئات الصور</span>
          <span class="chip">معلومات موثوقة</span>
          <span class="chip">تصفح سريع</span>
        </div>
      </div>
    </div>
  </section>

  <!-- عن -->
  <section id="about">
    <div class="container">
      <div class="section-title">
        <h2>عن الموقع</h2>
        <span class="muted">نسخة أولية قابلة للتوسع</span>
      </div>
      <div class="panel">
        <p>هذا الموقع يهدف لتقديم محتوى عربي مختصر وموثوق عن الحيوانات. التصميم <strong>متجاوب</strong> ويعمل على الجوال والكمبيوتر، مع تركيز على السرعة والبساطة البصرية. يمكنك ربطه بسهولة بحسابات التواصل التالية: إنستغرام، واتساب، تليجرام، والبريد.</p>
      </div>
    </div>
  </section>

  <!-- الفئات -->
  <section id="categories">
    <div class="container">
      <div class="section-title">
        <h2>فئات الحيوانات</h2>
        <a class="btn" href="#gallery">عرض الصور</a>
      </div>
      <div class="grid cols-5">
        <a class="card" href="#gallery" title="ثدييات">
          <img src="https://images.unsplash.com/photo-1501706362039-c06b2d715385?q=80&w=1200&auto=format&fit=crop" alt="ثدييات"/>
          <div class="label"><strong>ثدييات</strong><span class="muted">120 نوع</span></div>
        </a>
        <a class="card" href="#gallery" title="طيور">
          <img src="https://images.unsplash.com/photo-1501706362039-c06b2d715385?q=80&w=1200&auto=format&fit=crop&sat=120" alt="طيور"/>
          <div class="label"><strong>طيور</strong><span class="muted">90 نوع</span></div>
        </a>
        <a class="card" href="#gallery" title="زواحف">
          <img src="https://images.unsplash.com/photo-1548095115-45697e51374e?q=80&w=1200&auto=format&fit=crop" alt="زواحف"/>
          <div class="label"><strong>زواحف</strong><span class="muted">60 نوع</span></div>
        </a>
        <a class="card" href="#gallery" title="بحرية">
          <img src="https://images.unsplash.com/photo-1507525428034-b723cf961d3e?q=80&w=1200&auto=format&fit=crop" alt="بحرية"/>
          <div class="label"><strong>بحرية</strong><span class="muted">85 نوع</span></div>
        </a>
        <a class="card" href="#gallery" title="حشرات">
          <img src="https://images.unsplash.com/photo-1498928715928-5f9f7e66e86c?q=80&w=1200&auto=format&fit=crop" alt="حشرات"/>
          <div class="label"><strong>حشرات</strong><span class="muted">150 نوع</span></div>
        </a>
      </div>
    </div>
  </section>

  <!-- المعرض -->
  <section id="gallery">
    <div class="container">
      <div class="section-title">
        <h2>معرض الصور</h2>
        <span class="muted">نماذج توضيحية قابلة للتبديل</span>
      </div>
      <div class="gallery">
        <div class="g big"><img alt="أسد" src="https://images.unsplash.com/photo-1546182990-dffeafbe841d?q=80&w=1600&auto=format&fit=crop"/></div>
        <div class="g sm"><img alt="بومة" src="https://images.unsplash.com/photo-1501706362039-c06b2d715385?q=80&w=1200&auto=format&fit=crop"/></div>
        <div class="g sm"><img alt="سحلية" src="https://images.unsplash.com/photo-1548095115-45697e51374e?q=80&w=1200&auto=format&fit=crop"/></div>
        <div class="g sm"><img alt="دولفين" src="https://images.unsplash.com/photo-1507525428034-b723cf961d3e?q=80&w=1200&auto=format&fit=crop"/></div>
        <div class="g sm"><img alt="فراشة" src="https://images.unsplash.com/photo-1498928715928-5f9f7e66e86c?q=80&w=1200&auto=format&fit=crop"/></div>
        <div class="g big"><img alt="فيل" src="https://images.unsplash.com/photo-1546182990-dffeafbe841d?q=80&w=1600&auto=format&fit=crop&sat=110"/></div>
      </div>
    </div>
  </section>

  <!-- تواصل -->
  <section id="contact">
    <div class="container">
      <div class="section-title">
        <h2>تواصل معنا</h2>
        <span class="muted">روابط مباشرة ورسالة سريعة</span>
      </div>
      <div class="contact">
        <div class="panel">
          <div class="socials">
            <a class="social" href="https://www.instagram.com/sndsalbhyry0?igsh=MWc2ZWRyNDcydm1wNg==" target="_blank" rel="noopener" aria-label="Instagram">
              <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true"><path d="M7 2h10a5 5 0 0 1 5 5v10a5 5 0 0 1-5 5H7a5 5 0 0 1-5-5V7a5 5 0 0 1 5-5zm5 5a5 5 0 1 0 0 10 5 5 0 0 0 0-10zm6-1.25a1.25 1.25 0 1 0 0 2.5 1.25 1.25 0 0 0 0-2.5zM12 9a3 3 0 1 1 0 6 3 3 0 0 1 0-6z"/></svg>
              <span>إنستغرام</span>
            </a>
            <a class="social" href="https://wa.me/782667989" target="_blank" rel="noopener" aria-label="WhatsApp">
              <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true"><path d="M20.52 3.48A11.86 11.86 0 0 0 12 0C5.37 0 0 5.37 0 12c0 2.1.54 4.08 1.49 5.81L0 24l6.34-1.66A11.95 11.95 0 0 0 12 24c6.63 0 12-5.37 12-12 0-3.19-1.25-6.19-3.48-8.52zM12 21.5c-1.93 0-3.76-.53-5.34-1.45l-.38-.22-3.76.98.99-3.66-.25-.39A9.45 9.45 0 1 1 21.5 12 9.49 9.49 0 0 1 12 21.5zm5.43-6.58c-.3-.15-1.76-.86-2.04-.96-.27-.1-.47-.15-.67.15-.2.29-.77.96-.94 1.16-.17.19-.35.22-.64.07-.29-.15-1.22-.45-2.33-1.44a8.75 8.75 0 0 1-1.62-2c-.17-.29-.02-.45.13-.6.13-.13.3-.34.45-.51.15-.17.2-.29.3-.49.1-.2.05-.37-.02-.52-.07-.15-.67-1.62-.91-2.22-.24-.58-.49-.5-.67-.5h-.57c-.2 0-.52.07-.79.37-.27.3-1.04 1.02-1.04 2.49 0 1.46 1.07 2.88 1.22 3.08.15.19 2.1 3.2 5.09 4.49 3 .28 3.6.27 4.24.17.65-.1 2.04-.83 2.34-1.65.3-.82.3-1.53.21-1.68-.08-.15-.27-.24-.57-.39z"/></svg>
              <span>واتساب</span>
            </a>
            <a class="social" href="https://t.me/+967782667989" target="_blank" rel="noopener" aria-label="Telegram">
              <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true"><path d="M9.97 15.6 9.8 19.5c.34 0 .48-.15.65-.33l3.1-2.97 4.62 3.39c.85.47 1.46.22 1.68-.79l3.05-14.28c.27-1.27-.46-1.78-1.27-1.47L2.3 9.37C1.07 9.86 1.08 10.55 2.08 10.86l6.06 1.89 14.09-8.87-12.26 11.72z"/></svg>
              <span>تليجرام</span>
            </a>
            <a class="social" href="mailto:sondosalbohyry@gmail.com" aria-label="Email">
              <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true"><path d="M20 4H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h16a2 2 0 0 0 2-2V6a2 2 0 0 0-2-2zm0 4-8 5L4 8V6l8 5 8-5v2z"/></svg>
              <span>البريد</span>
            </a>
          </div>
        </div>
        <div class="panel">
          <form class="form" onsubmit="return sendMail(event)">
            <input class="input" id="name" placeholder="الاسم" required>
            <input class="input" id="email" placeholder="البريد الإلكتروني" type="email" required>
            <textarea class="input" id="message" placeholder="رسالتك" required></textarea>
            <button class="btn primary" type="submit">إرسال رسالة</button>
          </form>
        </div>
      </div>
    </div>
  </section>

  <footer class="footer">
    <div class="container" style="display:flex;align-items:center;justify-content:space-between;gap:12px;flex-wrap:wrap">
      <small>© <span id="year"></span> حيواناتي — صنع بالـ HTML/CSS/JS</small>
      <div style="display:flex;gap:10px">
        <a class="btn" href="#top">رجوع للأعلى</a>
      </div>
    </div>
  </footer>

  <script>
    // سنة ديناميكية
    document.getElementById('year').textContent = new Date().getFullYear();

    // إرسال عبر البريد الافتراضي
    function sendMail(e){
      e.preventDefault();
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const msg = document.getElementById('message').value.trim();
      const body = encodeURIComponent(`مرحباً،\nالاسم: ${name}\nالبريد: ${email}\n\n${msg}`);
      window.location.href = `mailto:sondosalbohyry@gmail.com?subject=رسالة من موقع الحيوانات&body=${body}`;
      return false;
    }

    // تمرير ناعم للروابط الداخلية
    document.querySelectorAll('a[href^="#"]').forEach(a=>{
      a.addEventListener('click', (ev)=>{
        const id = a.getAttribute('href');
        if(id.length>1){ ev.preventDefault(); document.querySelector(id).scrollIntoView({behavior:'smooth'}); }
      });
    });
  </script>
</body>
</html>
