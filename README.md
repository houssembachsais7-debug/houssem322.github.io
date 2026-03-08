<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>قميص المنتخب الجزائري 🇩🇿</title>
<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700;900&display=swap" rel="stylesheet">
<style>
  :root {
    --green: #006233;
    --green-dark: #004a26;
    --green-light: #00853F;
    --red: #D21034;
    --white: #FFFFFF;
    --off-white: #F5F5F5;
    --dark: #0a1a0f;
    --dark-2: #0f2015;
    --dark-3: #162b1c;
    --gold: #C9A84C;
    --text-muted: #7a9e85;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'Cairo', sans-serif;
    background: var(--dark);
    color: var(--white);
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* === PITCH PATTERN BG === */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      repeating-linear-gradient(
        0deg,
        transparent,
        transparent 60px,
        rgba(0,98,51,0.07) 60px,
        rgba(0,98,51,0.07) 120px
      );
    pointer-events: none;
    z-index: 0;
  }

  /* === HEADER === */
  header {
    background: rgba(0,74,38,0.95);
    backdrop-filter: blur(10px);
    border-bottom: 3px solid var(--red);
    padding: 14px 30px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: sticky;
    top: 0;
    z-index: 100;
  }

  .logo {
    display: flex;
    align-items: center;
    gap: 12px;
  }
  .logo-flag {
    display: flex;
    width: 40px;
    height: 28px;
    border-radius: 4px;
    overflow: hidden;
    box-shadow: 0 2px 8px rgba(0,0,0,0.4);
  }
  .flag-green { background: var(--green); flex: 1; }
  .flag-white { background: white; flex: 1; position: relative; display: flex; align-items: center; justify-content: center; }
  .flag-white::before {
    content: '☪';
    color: var(--red);
    font-size: 14px;
    position: absolute;
  }
  .logo-text {
    font-size: 18px;
    font-weight: 900;
    color: white;
    letter-spacing: 1px;
  }
  .logo-text span { color: var(--gold); }

  .header-badge {
    background: var(--red);
    color: white;
    padding: 6px 16px;
    border-radius: 20px;
    font-size: 13px;
    font-weight: 700;
    animation: pulse 2s infinite;
  }
  @keyframes pulse {
    0%,100% { box-shadow: 0 0 0 0 rgba(210,16,52,0.4); }
    50% { box-shadow: 0 0 0 8px rgba(210,16,52,0); }
  }

  /* === HERO === */
  .hero {
    position: relative;
    z-index: 1;
    text-align: center;
    padding: 50px 20px 30px;
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute;
    top: -50%;
    left: 50%;
    transform: translateX(-50%);
    width: 700px;
    height: 700px;
    background: radial-gradient(circle, rgba(0,133,63,0.15) 0%, transparent 65%);
    pointer-events: none;
  }

  .hero-tag {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: rgba(210,16,52,0.15);
    border: 1px solid rgba(210,16,52,0.4);
    color: #ff6b6b;
    padding: 6px 18px;
    border-radius: 30px;
    font-size: 13px;
    font-weight: 600;
    margin-bottom: 20px;
    animation: fadeDown 0.5s ease both;
  }

  .hero h1 {
    font-size: clamp(28px, 5vw, 52px);
    font-weight: 900;
    line-height: 1.2;
    margin-bottom: 12px;
    animation: fadeDown 0.6s ease 0.1s both;
  }
  .hero h1 .dz { color: var(--gold); }
  .hero p {
    color: var(--text-muted);
    font-size: 15px;
    animation: fadeDown 0.6s ease 0.2s both;
  }

  /* === MAIN LAYOUT === */
  .main-layout {
    position: relative;
    z-index: 1;
    max-width: 1100px;
    margin: 0 auto;
    padding: 20px 20px 80px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 30px;
    align-items: start;
  }

  /* === PRODUCT GALLERY === */
  .gallery-section {
    position: sticky;
    top: 90px;
  }

  .main-img-wrap {
    position: relative;
    border-radius: 20px;
    overflow: hidden;
    background: linear-gradient(135deg, #0f2a18, #1a4a28);
    border: 2px solid rgba(0,133,63,0.3);
    box-shadow: 0 30px 60px rgba(0,0,0,0.5);
    margin-bottom: 12px;
    aspect-ratio: 3/4;
    cursor: zoom-in;
  }
  .main-img-wrap img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.5s ease;
  }
  .main-img-wrap:hover img { transform: scale(1.04); }

  .img-overlay {
    position: absolute;
    inset: 0;
    background: linear-gradient(to top, rgba(0,0,0,0.4) 0%, transparent 50%);
    pointer-events: none;
  }

  .img-badges {
    position: absolute;
    top: 14px;
    right: 14px;
    display: flex;
    flex-direction: column;
    gap: 6px;
  }
  .img-badge {
    background: var(--red);
    color: white;
    font-size: 11px;
    font-weight: 800;
    padding: 5px 12px;
    border-radius: 20px;
    text-align: center;
  }
  .img-badge.green { background: var(--green); }

  .thumb-row {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 8px;
  }
  .thumb {
    border-radius: 12px;
    overflow: hidden;
    border: 2px solid transparent;
    cursor: pointer;
    transition: all 0.3s;
    aspect-ratio: 1;
    background: var(--dark-3);
  }
  .thumb img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.3s;
  }
  .thumb:hover img { transform: scale(1.08); }
  .thumb.active { border-color: var(--gold); box-shadow: 0 0 0 1px var(--gold); }

  /* PRODUCT INFO CARD */
  .product-info-card {
    background: rgba(15,32,21,0.8);
    border: 1px solid rgba(0,133,63,0.25);
    border-radius: 16px;
    padding: 12px 16px;
    margin-top: 14px;
  }
  .rating-row {
    display: flex;
    align-items: center;
    gap: 8px;
    margin-bottom: 6px;
  }
  .stars { color: var(--gold); font-size: 14px; letter-spacing: 1px; }
  .rating-count { color: var(--text-muted); font-size: 12px; }
  .product-title { font-size: 18px; font-weight: 800; margin-bottom: 4px; }
  .product-sub { color: var(--text-muted); font-size: 13px; }

  /* === ORDER FORM === */
  .order-card {
    background: rgba(15,32,21,0.9);
    border: 1px solid rgba(0,133,63,0.25);
    border-radius: 24px;
    padding: 32px;
    position: relative;
    overflow: hidden;
    animation: fadeUp 0.6s ease 0.3s both;
  }
  .order-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 4px;
    background: linear-gradient(90deg, var(--green), var(--white), var(--red));
  }

  /* Price Block */
  .price-block {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: var(--dark-3);
    border-radius: 14px;
    padding: 16px 20px;
    margin-bottom: 24px;
    border: 1px solid rgba(0,133,63,0.2);
  }
  .price-main {
    font-size: 32px;
    font-weight: 900;
    color: var(--gold);
  }
  .price-main span { font-size: 16px; color: var(--text-muted); font-weight: 400; }
  .price-old {
    font-size: 16px;
    color: var(--text-muted);
    text-decoration: line-through;
    margin-bottom: 2px;
  }
  .price-save {
    font-size: 12px;
    color: #4ade80;
    font-weight: 700;
  }

  /* Size Selector */
  .section-label {
    font-size: 13px;
    font-weight: 700;
    color: var(--text-muted);
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 10px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .size-guide {
    color: var(--gold);
    font-size: 12px;
    cursor: pointer;
    text-decoration: underline;
    text-decoration-style: dotted;
  }
  .size-grid {
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    gap: 8px;
    margin-bottom: 22px;
  }
  .size-btn {
    background: var(--dark-3);
    border: 1.5px solid rgba(0,133,63,0.3);
    border-radius: 8px;
    padding: 10px 4px;
    color: var(--white);
    font-family: 'Cairo', sans-serif;
    font-size: 14px;
    font-weight: 700;
    cursor: pointer;
    transition: all 0.25s;
    text-align: center;
  }
  .size-btn:hover { border-color: var(--green-light); background: rgba(0,133,63,0.15); }
  .size-btn.selected {
    background: var(--green);
    border-color: var(--green);
    color: white;
    box-shadow: 0 4px 14px rgba(0,133,63,0.4);
  }

  /* Form Fields */
  .form-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 14px;
    margin-bottom: 16px;
  }
  .form-grid .full { grid-column: 1 / -1; }

  .fgroup {
    display: flex;
    flex-direction: column;
    gap: 7px;
  }
  .fgroup label {
    font-size: 12px;
    font-weight: 700;
    color: var(--text-muted);
    letter-spacing: 0.5px;
  }
  .fgroup input,
  .fgroup select {
    background: var(--dark-3);
    border: 1.5px solid rgba(0,133,63,0.25);
    border-radius: 10px;
    padding: 12px 14px;
    color: var(--white);
    font-family: 'Cairo', sans-serif;
    font-size: 14px;
    outline: none;
    transition: all 0.3s;
    width: 100%;
    appearance: none;
    -webkit-appearance: none;
  }
  .fgroup input::placeholder { color: #3a6a4a; }
  .fgroup input:focus,
  .fgroup select:focus {
    border-color: var(--green-light);
    box-shadow: 0 0 0 3px rgba(0,133,63,0.15);
  }
  .select-wrap { position: relative; }
  .select-wrap::after {
    content: '▾';
    position: absolute;
    left: 12px;
    top: 50%;
    transform: translateY(-50%);
    color: var(--green-light);
    pointer-events: none;
  }

  /* Quantity */
  .qty-row {
    display: flex;
    align-items: center;
    gap: 0;
    background: var(--dark-3);
    border: 1.5px solid rgba(0,133,63,0.25);
    border-radius: 10px;
    overflow: hidden;
    height: 46px;
  }
  .qty-btn {
    width: 46px;
    height: 100%;
    background: rgba(0,133,63,0.15);
    border: none;
    color: var(--green-light);
    font-size: 22px;
    cursor: pointer;
    transition: background 0.2s;
    font-family: 'Cairo', sans-serif;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .qty-btn:hover { background: rgba(0,133,63,0.3); }
  .qty-val {
    flex: 1;
    text-align: center;
    font-size: 16px;
    font-weight: 800;
    color: white;
  }

  /* Summary */
  .summary {
    background: var(--dark-3);
    border-radius: 12px;
    padding: 16px;
    margin: 20px 0;
    border: 1px solid rgba(0,133,63,0.15);
  }
  .sum-row {
    display: flex;
    justify-content: space-between;
    font-size: 13px;
    color: var(--text-muted);
    padding: 5px 0;
  }
  .sum-row.total {
    color: white;
    font-size: 17px;
    font-weight: 800;
    border-top: 1px solid rgba(0,133,63,0.2);
    margin-top: 8px;
    padding-top: 12px;
  }
  .sum-row.total .tot-val { color: var(--gold); }

  /* Submit Button */
  .submit-btn {
    width: 100%;
    padding: 17px;
    background: linear-gradient(135deg, var(--green), var(--green-light));
    border: none;
    border-radius: 12px;
    color: white;
    font-family: 'Cairo', sans-serif;
    font-size: 17px;
    font-weight: 800;
    cursor: pointer;
    transition: all 0.3s;
    position: relative;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
    letter-spacing: 0.5px;
  }
  .submit-btn::before {
    content: '';
    position: absolute;
    top: 0; left: -100%;
    width: 100%; height: 100%;
    background: linear-gradient(90deg, transparent, rgba(255,255,255,0.15), transparent);
    transition: left 0.5s;
  }
  .submit-btn:hover::before { left: 100%; }
  .submit-btn:hover { transform: translateY(-2px); box-shadow: 0 12px 30px rgba(0,133,63,0.4); }
  .submit-btn.loading { opacity: 0.7; cursor: not-allowed; }

  /* Trust */
  .trust-row {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin-top: 18px;
    flex-wrap: wrap;
  }
  .trust-item {
    display: flex;
    align-items: center;
    gap: 5px;
    font-size: 11px;
    color: var(--text-muted);
  }
  .trust-dot { width: 6px; height: 6px; border-radius: 50%; background: var(--green-light); }

  /* === MODAL === */
  .modal-bg {
    display: none;
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,0.85);
    z-index: 999;
    align-items: center;
    justify-content: center;
    backdrop-filter: blur(8px);
  }
  .modal-bg.open { display: flex; }
  .modal {
    background: var(--dark-2);
    border: 1px solid rgba(0,133,63,0.4);
    border-top: 4px solid var(--green);
    border-radius: 24px;
    padding: 48px 36px;
    max-width: 420px;
    width: 90%;
    text-align: center;
    animation: popIn 0.4s cubic-bezier(0.34,1.56,0.64,1) both;
  }
  .modal-icon {
    width: 80px;
    height: 80px;
    background: linear-gradient(135deg, var(--green), var(--green-light));
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto 22px;
    font-size: 36px;
  }
  .modal h2 { font-size: 24px; font-weight: 900; margin-bottom: 10px; }
  .modal p { color: var(--text-muted); line-height: 1.7; font-size: 14px; margin-bottom: 26px; }
  .modal-close {
    background: var(--green);
    border: none;
    border-radius: 10px;
    padding: 13px 36px;
    color: white;
    font-family: 'Cairo', sans-serif;
    font-size: 15px;
    font-weight: 700;
    cursor: pointer;
    transition: all 0.3s;
  }
  .modal-close:hover { background: var(--green-light); transform: translateY(-1px); }

  /* Error toast */
  .toast {
    position: fixed;
    bottom: 30px;
    left: 50%;
    transform: translateX(-50%) translateY(100px);
    background: var(--red);
    color: white;
    padding: 14px 28px;
    border-radius: 30px;
    font-size: 14px;
    font-weight: 600;
    z-index: 999;
    transition: transform 0.4s cubic-bezier(0.34,1.56,0.64,1);
    white-space: nowrap;
  }
  .toast.show { transform: translateX(-50%) translateY(0); }

  /* ANIMATIONS */
  @keyframes fadeDown { from{opacity:0;transform:translateY(-20px)} to{opacity:1;transform:translateY(0)} }
  @keyframes fadeUp { from{opacity:0;transform:translateY(30px)} to{opacity:1;transform:translateY(0)} }
  @keyframes popIn { from{opacity:0;transform:scale(0.85)} to{opacity:1;transform:scale(1)} }

  /* RESPONSIVE */
  @media(max-width:768px){
    .main-layout { grid-template-columns:1fr; }
    .gallery-section { position:static; }
    .order-card { padding:24px 18px; }
    .form-grid { grid-template-columns:1fr; }
    .form-grid .full { grid-column:1; }
    .logo-text { font-size:15px; }
  }
</style>
</head>
<body>

<!-- HEADER -->
<header>
  <div class="logo">
    <div class="logo-flag">
      <div class="flag-green"></div>
      <div class="flag-white"></div>
      <div class="flag-green"></div>
    </div>
    <div class="logo-text">الخضر <span>STORE</span></div>
  </div>
  <div class="header-badge">🔴 متوفر الآن</div>
</header>

<!-- HERO -->
<section class="hero">
  <div class="hero-tag">🏆 المنتخب الوطني الجزائري 🇩🇿</div>
  <h1>قميص <span class="dz">الخضر</span> الرسمي<br>الإصدار الجديد 2025</h1>
  <p>ارتدِ ألوان الجزائر — قميص أصلي عالي الجودة مع توصيل لجميع الولايات</p>
</section>

<!-- MAIN LAYOUT -->
<div class="main-layout">

  <!-- LEFT: GALLERY -->
  <div class="gallery-section" style="animation: fadeUp 0.5s ease 0.1s both;">
    <div class="main-img-wrap" id="mainImgWrap">
      <img src="36906.png" alt="قميص المنتخب الجزائري" id="mainImg">
      <div class="img-overlay"></div>
      <div class="img-badges">
        <div class="img-badge">🔥 إصدار 2025</div>
        <div class="img-badge green">✓ أصلي 100%</div>
      </div>
    </div>

    <div class="thumb-row">
      <div class="thumb active" onclick="switchImg('36906.png', this)">
        <img src="36906.png" alt="الواجهة الأمامية">
      </div>
      <div class="thumb" onclick="switchImg('36902.jpg', this)">
        <img src="36902.jpg" alt="الواجهة الخلفية">
      </div>
      <div class="thumb" onclick="switchImg('36939.jpg', this)">
        <img src="36939.jpg" alt="طريقة اللبس">
      </div>
    </div>

    <div class="product-info-card">
      <div class="rating-row">
        <div class="stars">★★★★★</div>
        <div class="rating-count">(248 تقييم)</div>
      </div>
      <div class="product-title">قميص المنتخب الجزائري الرسمي</div>
      <div class="product-sub">Adidas ClimaCool — نسيج تنفسي فائق الجودة</div>
    </div>
  </div>

  <!-- RIGHT: ORDER FORM -->
  <div class="order-card">

    <!-- Price -->
    <div class="price-block">
      <div>
        <div class="price-old">3,500 دج</div>
        <div class="price-save">💚 وفّر 700 دج</div>
      </div>
      <div class="price-main">2,800 <span>دج</span></div>
    </div>

    <!-- Size -->
    <div class="section-label">
      <span>المقاس</span>
      <span class="size-guide">جدول المقاسات ↗</span>
    </div>
    <div class="size-grid" id="sizeGrid">
      <button class="size-btn" onclick="selectSize(this)">S</button>
      <button class="size-btn" onclick="selectSize(this)">M</button>
      <button class="size-btn selected" onclick="selectSize(this)">L</button>
      <button class="size-btn" onclick="selectSize(this)">XL</button>
      <button class="size-btn" onclick="selectSize(this)">XXL</button>
    </div>

    <!-- Form -->
    <div class="form-grid">
      <div class="fgroup">
        <label>الاسم الكامل</label>
        <input type="text" id="name" placeholder="مثال: أحمد بن علي">
      </div>
      <div class="fgroup">
        <label>رقم الهاتف</label>
        <input type="tel" id="phone" placeholder="0550 123 456">
      </div>

      <div class="fgroup full">
        <label>الولاية</label>
        <div class="select-wrap">
          <select id="wilaya" onchange="loadCommunes()">
            <option value="">اختر الولاية</option>
            <option value="الجزائر">الجزائر</option>
            <option value="البليدة">البليدة</option>
            <option value="وهران">وهران</option>
            <option value="قسنطينة">قسنطينة</option>
            <option value="سطيف">سطيف</option>
            <option value="عنابة">عنابة</option>
            <option value="باتنة">باتنة</option>
            <option value="تلمسان">تلمسان</option>
            <option value="بجاية">بجاية</option>
            <option value="تيزي وزو">تيزي وزو</option>
            <option value="مستغانم">مستغانم</option>
            <option value="سكيكدة">سكيكدة</option>
            <option value="الشلف">الشلف</option>
            <option value="تبسة">تبسة</option>
            <option value="بسكرة">بسكرة</option>
            <option value="ورقلة">ورقلة</option>
            <option value="أدرار">أدرار</option>
            <option value="تمنراست">تمنراست</option>
            <option value="أم البواقي">أم البواقي</option>
            <option value="خنشلة">خنشلة</option>
            <option value="سوق أهراس">سوق أهراس</option>
            <option value="جيجل">جيجل</option>
            <option value="ميلة">ميلة</option>
            <option value="برج بوعريريج">برج بوعريريج</option>
            <option value="المسيلة">المسيلة</option>
            <option value="المدية">المدية</option>
            <option value="تيسمسيلت">تيسمسيلت</option>
            <option value="البويرة">البويرة</option>
            <option value="بومرداس">بومرداس</option>
            <option value="تيبازة">تيبازة</option>
            <option value="عين الدفلى">عين الدفلى</option>
            <option value="عين تموشنت">عين تموشنت</option>
            <option value="تيارت">تيارت</option>
            <option value="معسكر">معسكر</option>
            <option value="سعيدة">سعيدة</option>
            <option value="غليزان">غليزان</option>
            <option value="الأغواط">الأغواط</option>
            <option value="الجلفة">الجلفة</option>
            <option value="غرداية">غرداية</option>
            <option value="الوادي">الوادي</option>
            <option value="النعامة">النعامة</option>
            <option value="البيض">البيض</option>
            <option value="إليزي">إليزي</option>
            <option value="تندوف">تندوف</option>
            <option value="بشار">بشار</option>
            <option value="خميستي">خميستي</option>
            <option value="تيبيازة">تيبيازة</option>
            <option value="برج باجي مختار">برج باجي مختار</option>
            <option value="أولاد جلال">أولاد جلال</option>
            <option value="تيميمون">تيميمون</option>
            <option value="توقرت">توقرت</option>
            <option value="إن صالح">إن صالح</option>
            <option value="إن قزام">إن قزام</option>
            <option value="جانت">جانت</option>
            <option value="المغير">المغير</option>
            <option value="المنيعة">المنيعة</option>
            <option value="بني عباس">بني عباس</option>
            <option value="عين قزام">عين قزام</option>
            <option value="بريكة">بريكة</option>
          </select>
        </div>
      </div>

      <div class="fgroup full">
        <label>البلدية</label>
        <div class="select-wrap">
          <select id="commune">
            <option value="">اختر الولاية أولاً</option>
          </select>
        </div>
      </div>

      <div class="fgroup full">
        <label>العنوان التفصيلي</label>
        <input type="text" id="address" placeholder="الحي، الشارع، رقم المبنى...">
      </div>

      <div class="fgroup">
        <label>الكمية</label>
        <div class="qty-row">
          <button class="qty-btn" onclick="chQty(-1)">−</button>
          <div class="qty-val" id="qtyVal">1</div>
          <button class="qty-btn" onclick="chQty(1)">+</button>
        </div>
      </div>

      <div class="fgroup">
        <label>طريقة الدفع</label>
        <div class="select-wrap">
          <select>
            <option>💵 عند الاستلام</option>
            <option>📱 بريدي موب</option>
            <option>🏦 تحويل بنكي</option>
          </select>
        </div>
      </div>
    </div>

    <!-- Summary -->
    <div class="summary">
      <div class="sum-row"><span>سعر القميص</span><span>2,800 دج</span></div>
      <div class="sum-row"><span>الكمية</span><span id="sumQty">× 1</span></div>
      <div class="sum-row"><span>رسوم التوصيل</span><span style="color:#4ade80">مجاني 🎉</span></div>
      <div class="sum-row total"><span>المجموع</span><span class="tot-val" id="sumTotal">2,800 دج</span></div>
    </div>

    <!-- Submit -->
    <button class="submit-btn" id="submitBtn" onclick="submitOrder()">
      <span>🛒</span>
      <span id="btnText">تأكيد الطلب الآن</span>
    </button>

    <div class="trust-row">
      <div class="trust-item"><div class="trust-dot"></div> توصيل لكل الجزائر</div>
      <div class="trust-item"><div class="trust-dot"></div> ضمان الجودة</div>
      <div class="trust-item"><div class="trust-dot"></div> دفع آمن عند الاستلام</div>
    </div>
  </div>

</div>

<!-- SUCCESS MODAL -->
<div class="modal-bg" id="modal">
  <div class="modal">
    <div class="modal-icon">✅</div>
    <h2>تم استلام طلبك! 🇩🇿</h2>
    <p>شكراً لك على ثقتك! سيتصل بك أحد موظفينا خلال 24 ساعة لتأكيد الطلب وتحديد موعد التوصيل.</p>
    <button class="modal-close" onclick="closeModal()">العودة للمتجر</button>
  </div>
</div>

<!-- TOAST -->
<div class="toast" id="toast"></div>

<script>
  // ==================== CONFIG ====================
  const BOT_TOKEN = "YOUR_BOT_TOKEN_HERE"; // ← ضع توكن البوت هنا
  const CHAT_ID   = "672218833";
  const PRICE     = 2800;
  // ================================================

  // Communes data
  const communesData = {
    "الجزائر": ["الجزائر الوسطى","باب الواد","بولوغين","حسين داي","الحراش","برج البحري","القبة","بئر مراد رايس","بن عكنون","المحمدية","الرايس حميدو","بابا حسن","الدويرة","برج الكيفان","الرويبة","رغاية","الشراقة","الدرارية","سيدي موسى","الأرقان","خرايسية","سيدي عبد الله","حمامات الأنف","أولاد فايت","تيجلابين","سيدي يحيى","زرالدة","الساحل","الأبيار","قوبة","عين بنيان","بئر توتة"],
    "البليدة": ["البليدة","بوفاريك","لرباط","الأربعاء","موزاية","بني تامو","شرشل","أولاد يعيش","شفاعة","قرواو","الشريعة","بن خليل","بوعرفة","مصطفى بن إبراهيم","بني مراد","العفرون","الصومعة","بوينان","أحمد دراية","بن آرو","القليعة","أقبو"],
    "وهران": ["وهران","عين البيضاء","بطيوة","بئر الجير","السانية","مرسى الحجاج","عرزيو","بوسفر","حاسي بن عقة","طفراوي","مداغ","وادي تليلات","سيدي الشحمي","خرزوز","بوغراشة","الكرمة","عين الكرمة","حمام بوحجر","برحال","حاسي مفسوخ","مسرغين","سيدي مبارك"],
    "قسنطينة": ["قسنطينة","الخروب","عين عبيد","ديدوش مراد","عين سمارة","حامة بوزيان","إبن زياد","زيغود يوسف","أولاد رحمون","بني حميدان","مسعود بوجريو"],
    "سطيف": ["سطيف","العلمة","أقجدال","عين أرنات","قجال","بوقاعة","بئر العرش","باتنة","عين لقراح","بني عزيز","أولاد تبان","مزلوق","بابور","عين رويلة"],
    "عنابة": ["عنابة","الحجار","سرايدي","برحال","الشط","عين الباردة","المنارة","تيسدت"],
    "باتنة": ["باتنة","مروانة","نقاوس","بريكة","عين توتة","أريس","تكوت","سرج الغول","أولاد سلام","الشمرة","بيطام","حيدوسة","معافة"],
    "تلمسان": ["تلمسان","مغنية","غزوات","بني صاف","رمشي","سبدو","أولاد ميمون","بني سنوس","سيدي بوجنان","عين يوسف","ندرومة","بني بوسعيد"],
    "بجاية": ["بجاية","أميزور","الكريفات","خربة","أقبو","سيدي عيش","ببريشن","إيغيل علي","أوقاس","تيشي","أوزلاقن"],
    "تيزي وزو": ["تيزي وزو","عزازقة","لربعاء ناث إيراثن","بني يني","فريحة","أيت خليلي","أقبيل","معاتقة","أيت أيسي","بوغني","تابودت"],
    "مستغانم": ["مستغانم","عين تادلس","صيادة","عشعاشة","خضرا","سيدي علي","منصورة","حجاج"],
    "سكيكدة": ["سكيكدة","عزابة","فلفلة","حمادي كرومة","رمضان جمال","كركرة","بن عزوز"],
    "الشلف": ["الشلف","تنس","أم الدروع","بوقادير","عين مران","أولاد فارس","بني حواء"],
    "تبسة": ["تبسة","بئر العاتر","الونزة","النقرين","مرسط","تليجان","بكاريا"],
    "بسكرة": ["بسكرة","طولقة","أولاد جلال","سيدي عقبة","القنطرة","مشونش","أورلال","زريبة الوادي"],
    "ورقلة": ["ورقلة","حاسي مسعود","النقوسة","تقرت","سيدي خويلد","رأس المائدة","الرويسات","المنقر"],
    "المسيلة": ["المسيلة","بوسعادة","مجانة","سيدي عيسى","أولاد دراج","محمد بوضياف","بنهار","بريبة"],
    "برج بوعريريج": ["برج بوعريريج","رأس الوادي","برج زمورة","تاشتة","حمادة","قصر البخاري"],
    "المدية": ["المدية","بنيية","البرواقية","كاف لخضر","ثنية الحد","أزيز","شنيفة"],
    "البويرة": ["البويرة","لقصر","عين بسام","أقبو","سور الغزلان","راس الوادي"],
    "بومرداس": ["بومرداس","برج منايل","خميس الخشنة","دلس","بودواو","زموري","بلاية"],
    "تيبازة": ["تيبازة","شرشل","أقبو","حجوط","مراد","بوهارون","خميستي"],
    "عين الدفلى": ["عين الدفلى","خميس مليانة","عين البنيان","بورحيل","حمام ريغة","المخاطرية"],
    "عين تموشنت": ["عين تموشنت","بني صاف","حمام بوحجر","أولاد كيحل","شعبة اسحاق"],
    "تيارت": ["تيارت","فرندة","مهيانة","سوق أهراس","تاخمارت","السوقر"],
    "معسكر": ["معسكر","السيق","غريس","محمد بن علي","أولاد مامية","بوهني"],
    "سعيدة": ["سعيدة","عين الحجر","أولاد إبراهيم","تيرسين","دوي ثابت"],
    "غليزان": ["غليزان","رليزان","جمعة أولاد الشيخ","وادي الرهيو","بلعسل"],
    "الأغواط": ["الأغواط","آفلو","قصر الحيران","برج خنفيس","سيدي مخلوف"],
    "الجلفة": ["الجلفة","مسعد","حاسي بحبح","عين وسارة","بيرين","سلمانة"],
    "غرداية": ["غرداية","بريان","الغرارة","ذهب","القرارة","بونورة","العطف","بني يزقن","مليكة"],
    "الوادي": ["الوادي","بسباس","الرباح","ورماس","كوينين","المقرن","حساني عبد الكريم"],
    "النعامة": ["النعامة","المشرية","عسلة","صفيصفة","تيوت","مقرر"],
    "البيض": ["البيض","بوعلام","العبادلة","الشقيق","سيدي امحمد بن بوزيان"],
    "إليزي": ["إليزي","عين أمناس","جانت","برج عمر إدريس"],
    "تندوف": ["تندوف"],
    "بشار": ["بشار","أبادلة","بني ونيف","القنادسة","تاغيت","كرزاز"],
    "أدرار": ["أدرار","رقان","تيميمون","تيط","أولاد سعيد","أوقروت","أولف"],
    "تمنراست": ["تمنراست","عين صالح","عين قزام","إدلس"],
    "أم البواقي": ["أم البواقي","عين بيضاء","عين مليلة","عين الفكرون","عين الزيتونة"],
    "خنشلة": ["خنشلة","بغاي","أولاد رشاش","مستورة","الرميلة"],
    "سوق أهراس": ["سوق أهراس","سدراتة","معلمة","الحنانشة","أم العظائم"],
    "جيجل": ["جيجل","الميلية","الطاهر","تاهر","إيمي أومروان","الشقفة"],
    "ميلة": ["ميلة","الشلالة الكبرى","فرجيوة","عين مليلة","أحمد راشدي"],
    "توقرت": ["توقرت","الطيبات","تماسين","بلدة عمر"],
    "إن صالح": ["إن صالح","فقارة الزوا"],
    "إن قزام": ["إن قزام"],
    "جانت": ["جانت"],
    "المغير": ["المغير","جامعة","سيدي خليل"],
    "المنيعة": ["المنيعة","حاسي الفحل","بريانة"],
    "بني عباس": ["بني عباس","إقلي","ثاورير","بودة"],
    "عين قزام": ["عين قزام"],
    "بريكة": ["بريكة","رأس العيون","أولاد فاضل"],
    "أولاد جلال": ["أولاد جلال","سيدي خالد","الدوسن"],
    "تيميمون": ["تيميمون","تاليمون","عين سالح","شروين"],
    "برج باجي مختار": ["برج باجي مختار"],
    "خميستي": ["خميستي","سيدي سليمان","صوامع"],
    "تيبيازة": ["تيبازة","حاجوت","شرشل"],
    "تيسمسيلت": ["تيسمسيلت","ثنية الحد","عازيز","برج بونعامة"],
  };

  let qty = 1;
  let selectedSize = "L";

  function switchImg(src, thumb) {
    document.getElementById('mainImg').src = src;
    document.querySelectorAll('.thumb').forEach(t => t.classList.remove('active'));
    thumb.classList.add('active');
  }

  function selectSize(btn) {
    document.querySelectorAll('.size-btn').forEach(b => b.classList.remove('selected'));
    btn.classList.add('selected');
    selectedSize = btn.textContent;
  }

  function chQty(d) {
    qty = Math.max(1, Math.min(10, qty + d));
    document.getElementById('qtyVal').textContent = qty;
    document.getElementById('sumQty').textContent = '× ' + qty;
    document.getElementById('sumTotal').textContent = (PRICE * qty).toLocaleString('ar-DZ') + ' دج';
  }

  function loadCommunes() {
    const wilaya = document.getElementById('wilaya').value;
    const sel = document.getElementById('commune');
    sel.innerHTML = '';
    if (!wilaya) { sel.innerHTML = '<option value="">اختر الولاية أولاً</option>'; return; }
    const list = communesData[wilaya] || [wilaya];
    list.forEach(c => {
      const opt = document.createElement('option');
      opt.value = c; opt.textContent = c;
      sel.appendChild(opt);
    });
  }

  function showToast(msg) {
    const t = document.getElementById('toast');
    t.textContent = msg;
    t.classList.add('show');
    setTimeout(() => t.classList.remove('show'), 3000);
  }

  async function submitOrder() {
    const name    = document.getElementById('name').value.trim();
    const phone   = document.getElementById('phone').value.trim();
    const wilaya  = document.getElementById('wilaya').value;
    const commune = document.getElementById('commune').value;
    const address = document.getElementById('address').value.trim();

    if (!name)    { showToast('⚠️ أدخل اسمك الكامل'); return; }
    if (!phone)   { showToast('⚠️ أدخل رقم هاتفك'); return; }
    if (!wilaya)  { showToast('⚠️ اختر ولايتك'); return; }
    if (!commune) { showToast('⚠️ اختر بلديتك'); return; }
    if (!address) { showToast('⚠️ أدخل عنوانك التفصيلي'); return; }

    const btn = document.getElementById('submitBtn');
    const txt = document.getElementById('btnText');
    btn.classList.add('loading');
    txt.textContent = '⏳ جارٍ الإرسال...';

    const msg = `
🇩🇿 *طلب جديد — قميص الخضر*
━━━━━━━━━━━━━━
👤 الاسم: ${name}
📞 الهاتف: ${phone}
📍 الولاية: ${wilaya}
🏘️ البلدية: ${commune}
🏠 العنوان: ${address}
👕 المقاس: ${selectedSize}
🔢 الكمية: ${qty}
💰 المجموع: ${(PRICE * qty).toLocaleString()} دج
━━━━━━━━━━━━━━
🕐 ${new Date().toLocaleString('ar-DZ')}
    `.trim();

    try {
      const res = await fetch(`https://api.telegram.org/bot${BOT_TOKEN}/sendMessage`, {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ chat_id: CHAT_ID, text: msg, parse_mode: 'Markdown' })
      });
      const data = await res.json();
      if (data.ok) {
        document.getElementById('modal').classList.add('open');
      } else {
        showToast('❌ خطأ في الإرسال، حاول مجدداً');
      }
    } catch(e) {
      showToast('❌ تحقق من اتصالك بالإنترنت');
    }

    btn.classList.remove('loading');
    txt.textContent = 'تأكيد الطلب الآن';
  }

  function closeModal() {
    document.getElementById('modal').classList.remove('open');
    document.getElementById('name').value = '';
    document.getElementById('phone').value = '';
    document.getElementById('wilaya').value = '';
    document.getElementById('commune').innerHTML = '<option value="">اختر الولاية أولاً</option>';
    document.getElementById('address').value = '';
    qty = 1;
    document.getElementById('qtyVal').textContent = '1';
    document.getElementById('sumQty').textContent = '× 1';
    document.getElementById('sumTotal').textContent = '2,800 دج';
  }
</script>
</body>
</html>
