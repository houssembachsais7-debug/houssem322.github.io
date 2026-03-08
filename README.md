<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>متجر البريق | اطلب الآن</title>
<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700;900&family=Tajawal:wght@300;400;500;700&display=swap" rel="stylesheet">
<style>
  :root {
    --gold: #C9A84C;
    --gold-light: #E8C97A;
    --dark: #0D0D0D;
    --dark-2: #1A1A1A;
    --dark-3: #252525;
    --cream: #F5F0E8;
    --text-muted: #888;
    --red: #E74C3C;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'Cairo', sans-serif;
    background: var(--dark);
    color: var(--cream);
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* ===== HEADER ===== */
  header {
    background: var(--dark-2);
    border-bottom: 1px solid #2a2a2a;
    padding: 18px 40px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: sticky;
    top: 0;
    z-index: 100;
  }

  .logo {
    font-size: 24px;
    font-weight: 900;
    letter-spacing: 1px;
    color: var(--gold);
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .logo span { color: var(--cream); }

  .nav-links {
    display: flex;
    gap: 30px;
    list-style: none;
  }
  .nav-links a {
    color: var(--text-muted);
    text-decoration: none;
    font-size: 14px;
    transition: color 0.3s;
    font-weight: 500;
  }
  .nav-links a:hover { color: var(--gold); }

  .cart-btn {
    background: transparent;
    border: 1px solid var(--gold);
    color: var(--gold);
    padding: 8px 20px;
    border-radius: 30px;
    cursor: pointer;
    font-family: 'Cairo', sans-serif;
    font-size: 14px;
    transition: all 0.3s;
  }
  .cart-btn:hover { background: var(--gold); color: var(--dark); }

  /* ===== HERO SECTION ===== */
  .hero {
    text-align: center;
    padding: 60px 20px 30px;
    position: relative;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    top: -100px;
    left: 50%;
    transform: translateX(-50%);
    width: 600px;
    height: 600px;
    background: radial-gradient(circle, rgba(201,168,76,0.08) 0%, transparent 70%);
    pointer-events: none;
  }

  .hero-label {
    display: inline-block;
    background: rgba(201,168,76,0.1);
    border: 1px solid rgba(201,168,76,0.3);
    color: var(--gold);
    padding: 6px 20px;
    border-radius: 30px;
    font-size: 13px;
    font-weight: 600;
    letter-spacing: 2px;
    margin-bottom: 20px;
    animation: fadeDown 0.6s ease both;
  }

  .hero h1 {
    font-size: clamp(32px, 5vw, 56px);
    font-weight: 900;
    line-height: 1.2;
    margin-bottom: 15px;
    animation: fadeDown 0.7s ease 0.1s both;
  }
  .hero h1 em {
    font-style: normal;
    background: linear-gradient(135deg, var(--gold), var(--gold-light));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .hero p {
    color: var(--text-muted);
    font-size: 16px;
    max-width: 500px;
    margin: 0 auto 40px;
    line-height: 1.7;
    animation: fadeDown 0.7s ease 0.2s both;
  }

  /* ===== PRODUCTS GRID ===== */
  .section-title {
    text-align: center;
    font-size: 28px;
    font-weight: 700;
    margin-bottom: 10px;
    color: var(--cream);
  }
  .section-sub {
    text-align: center;
    color: var(--text-muted);
    font-size: 14px;
    margin-bottom: 40px;
  }

  .products-section {
    max-width: 1100px;
    margin: 0 auto;
    padding: 20px 20px 60px;
  }

  .products-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 20px;
    margin-bottom: 60px;
  }

  .product-card {
    background: var(--dark-2);
    border-radius: 16px;
    overflow: hidden;
    border: 1px solid #2a2a2a;
    cursor: pointer;
    transition: all 0.35s ease;
    position: relative;
    animation: fadeUp 0.5s ease both;
  }
  .product-card:nth-child(1) { animation-delay: 0.1s; }
  .product-card:nth-child(2) { animation-delay: 0.2s; }
  .product-card:nth-child(3) { animation-delay: 0.3s; }
  .product-card:nth-child(4) { animation-delay: 0.4s; }

  .product-card:hover {
    transform: translateY(-6px);
    border-color: var(--gold);
    box-shadow: 0 20px 40px rgba(0,0,0,0.5), 0 0 0 1px rgba(201,168,76,0.2);
  }

  .product-card.selected {
    border-color: var(--gold);
    box-shadow: 0 0 0 2px var(--gold), 0 20px 40px rgba(201,168,76,0.1);
  }

  .product-badge {
    position: absolute;
    top: 12px;
    right: 12px;
    background: var(--red);
    color: white;
    font-size: 11px;
    font-weight: 700;
    padding: 4px 10px;
    border-radius: 20px;
    z-index: 2;
  }

  .product-badge.new { background: #27AE60; }

  .product-img-wrap {
    width: 100%;
    height: 200px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 80px;
    position: relative;
    overflow: hidden;
  }

  /* Stylized SVG product backgrounds */
  .product-img-wrap.p1 { background: linear-gradient(135deg, #1a1230, #2d1b69); }
  .product-img-wrap.p2 { background: linear-gradient(135deg, #0d2137, #1a4a6b); }
  .product-img-wrap.p3 { background: linear-gradient(135deg, #1a0d0d, #6b1a1a); }
  .product-img-wrap.p4 { background: linear-gradient(135deg, #0d1a0d, #1a5c1a); }

  .product-img-wrap svg {
    width: 100px;
    height: 100px;
    filter: drop-shadow(0 10px 20px rgba(0,0,0,0.5));
    transition: transform 0.3s ease;
  }
  .product-card:hover .product-img-wrap svg {
    transform: scale(1.08) rotate(-3deg);
  }

  .selected-check {
    position: absolute;
    top: 12px;
    left: 12px;
    width: 28px;
    height: 28px;
    background: var(--gold);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    opacity: 0;
    transform: scale(0);
    transition: all 0.3s;
    z-index: 2;
  }
  .product-card.selected .selected-check {
    opacity: 1;
    transform: scale(1);
  }
  .selected-check svg { width: 14px; height: 14px; }

  .product-info {
    padding: 16px;
  }
  .product-name {
    font-size: 15px;
    font-weight: 700;
    margin-bottom: 5px;
    color: var(--cream);
  }
  .product-desc {
    font-size: 12px;
    color: var(--text-muted);
    margin-bottom: 12px;
    line-height: 1.5;
  }
  .product-footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .product-price {
    font-size: 18px;
    font-weight: 900;
    color: var(--gold);
  }
  .product-price span {
    font-size: 12px;
    color: var(--text-muted);
    font-weight: 400;
  }
  .stars { color: var(--gold); font-size: 12px; }

  /* ===== ORDER FORM ===== */
  .order-section {
    max-width: 700px;
    margin: 0 auto;
    padding: 0 20px 80px;
  }

  .form-card {
    background: var(--dark-2);
    border: 1px solid #2a2a2a;
    border-radius: 24px;
    padding: 40px;
    position: relative;
    overflow: hidden;
  }
  .form-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 3px;
    background: linear-gradient(90deg, var(--gold), var(--gold-light), var(--gold));
  }

  .form-header {
    margin-bottom: 30px;
  }
  .form-header h2 {
    font-size: 24px;
    font-weight: 700;
    margin-bottom: 6px;
  }
  .form-header p {
    color: var(--text-muted);
    font-size: 14px;
  }

  .selected-product-preview {
    background: var(--dark-3);
    border: 1px solid rgba(201,168,76,0.2);
    border-radius: 12px;
    padding: 16px;
    margin-bottom: 28px;
    display: flex;
    align-items: center;
    gap: 16px;
  }
  .preview-icon {
    width: 60px;
    height: 60px;
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
  }
  .preview-icon.p1 { background: linear-gradient(135deg, #1a1230, #2d1b69); }
  .preview-icon.p2 { background: linear-gradient(135deg, #0d2137, #1a4a6b); }
  .preview-icon.p3 { background: linear-gradient(135deg, #1a0d0d, #6b1a1a); }
  .preview-icon.p4 { background: linear-gradient(135deg, #0d1a0d, #1a5c1a); }
  .preview-icon svg { width: 32px; height: 32px; }
  .preview-text h4 { font-size: 14px; font-weight: 700; margin-bottom: 3px; }
  .preview-text p { font-size: 13px; color: var(--text-muted); }
  .preview-price {
    margin-right: auto;
    font-size: 20px;
    font-weight: 900;
    color: var(--gold);
  }

  .form-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 18px;
  }
  .form-grid .full { grid-column: 1 / -1; }

  .form-group {
    display: flex;
    flex-direction: column;
    gap: 8px;
  }
  .form-group label {
    font-size: 13px;
    font-weight: 600;
    color: var(--text-muted);
    letter-spacing: 0.5px;
  }
  .form-group input,
  .form-group select {
    background: var(--dark-3);
    border: 1px solid #333;
    border-radius: 10px;
    padding: 13px 16px;
    color: var(--cream);
    font-family: 'Cairo', sans-serif;
    font-size: 14px;
    outline: none;
    transition: all 0.3s;
    width: 100%;
    appearance: none;
    -webkit-appearance: none;
  }
  .form-group input::placeholder { color: #555; }
  .form-group input:focus,
  .form-group select:focus {
    border-color: var(--gold);
    box-shadow: 0 0 0 3px rgba(201,168,76,0.1);
  }

  .select-wrapper {
    position: relative;
  }
  .select-wrapper::after {
    content: '▾';
    position: absolute;
    left: 14px;
    top: 50%;
    transform: translateY(-50%);
    color: var(--gold);
    pointer-events: none;
    font-size: 14px;
  }

  .qty-control {
    display: flex;
    align-items: center;
    gap: 0;
    background: var(--dark-3);
    border: 1px solid #333;
    border-radius: 10px;
    overflow: hidden;
  }
  .qty-btn {
    width: 44px;
    height: 44px;
    background: transparent;
    border: none;
    color: var(--gold);
    font-size: 20px;
    cursor: pointer;
    transition: background 0.2s;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Cairo', sans-serif;
  }
  .qty-btn:hover { background: rgba(201,168,76,0.1); }
  .qty-value {
    flex: 1;
    text-align: center;
    font-size: 16px;
    font-weight: 700;
    color: var(--cream);
  }

  .summary-box {
    background: var(--dark-3);
    border-radius: 12px;
    padding: 18px;
    margin: 24px 0;
  }
  .summary-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 6px 0;
    font-size: 14px;
    color: var(--text-muted);
  }
  .summary-row.total {
    color: var(--cream);
    font-size: 18px;
    font-weight: 700;
    border-top: 1px solid #333;
    margin-top: 8px;
    padding-top: 14px;
  }
  .summary-row.total .amount { color: var(--gold); }

  .submit-btn {
    width: 100%;
    padding: 18px;
    background: linear-gradient(135deg, var(--gold), var(--gold-light));
    border: none;
    border-radius: 12px;
    color: var(--dark);
    font-family: 'Cairo', sans-serif;
    font-size: 17px;
    font-weight: 700;
    cursor: pointer;
    transition: all 0.3s;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
    position: relative;
    overflow: hidden;
  }
  .submit-btn::before {
    content: '';
    position: absolute;
    top: 0; left: -100%;
    width: 100%; height: 100%;
    background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
    transition: left 0.5s;
  }
  .submit-btn:hover::before { left: 100%; }
  .submit-btn:hover { transform: translateY(-2px); box-shadow: 0 10px 30px rgba(201,168,76,0.3); }
  .submit-btn:active { transform: translateY(0); }

  .trust-badges {
    display: flex;
    justify-content: center;
    gap: 24px;
    margin-top: 20px;
  }
  .trust-badge {
    display: flex;
    align-items: center;
    gap: 6px;
    font-size: 12px;
    color: var(--text-muted);
  }
  .trust-badge svg { width: 16px; height: 16px; color: var(--gold); }

  /* ===== SUCCESS MODAL ===== */
  .modal-overlay {
    display: none;
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,0.8);
    z-index: 999;
    align-items: center;
    justify-content: center;
    backdrop-filter: blur(6px);
  }
  .modal-overlay.show { display: flex; }
  .modal {
    background: var(--dark-2);
    border: 1px solid rgba(201,168,76,0.3);
    border-radius: 24px;
    padding: 50px 40px;
    max-width: 440px;
    width: 90%;
    text-align: center;
    animation: popIn 0.4s cubic-bezier(0.34, 1.56, 0.64, 1) both;
  }
  .modal-icon {
    width: 80px;
    height: 80px;
    background: linear-gradient(135deg, var(--gold), var(--gold-light));
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto 24px;
  }
  .modal-icon svg { width: 40px; height: 40px; color: var(--dark); }
  .modal h2 { font-size: 26px; font-weight: 800; margin-bottom: 12px; }
  .modal p { color: var(--text-muted); font-size: 15px; line-height: 1.6; margin-bottom: 28px; }
  .modal-close {
    background: var(--gold);
    border: none;
    border-radius: 10px;
    padding: 14px 40px;
    color: var(--dark);
    font-family: 'Cairo', sans-serif;
    font-size: 15px;
    font-weight: 700;
    cursor: pointer;
  }

  /* ===== ANIMATIONS ===== */
  @keyframes fadeDown {
    from { opacity: 0; transform: translateY(-20px); }
    to { opacity: 1; transform: translateY(0); }
  }
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }
  @keyframes popIn {
    from { opacity: 0; transform: scale(0.8); }
    to { opacity: 1; transform: scale(1); }
  }

  /* ===== RESPONSIVE ===== */
  @media (max-width: 600px) {
    header { padding: 14px 20px; }
    .nav-links { display: none; }
    .form-card { padding: 24px 20px; }
    .form-grid { grid-template-columns: 1fr; }
    .form-grid .full { grid-column: 1; }
    .trust-badges { flex-wrap: wrap; gap: 12px; }
  }
</style>
</head>
<body>

<!-- HEADER -->
<header>
  <div class="logo">✦ <span>البريق</span> STORE</div>
  <ul class="nav-links">
    <li><a href="#">الرئيسية</a></li>
    <li><a href="#">المنتجات</a></li>
    <li><a href="#">التوصيل</a></li>
    <li><a href="#">اتصل بنا</a></li>
  </ul>
  <button class="cart-btn">🛒 السلة</button>
</header>

<!-- HERO -->
<section class="hero">
  <div class="hero-label">🔥 عروض حصرية - توصيل لكل ولايات الجزائر</div>
  <h1>اختر منتجك <em>المميز</em><br>واطلبه الآن</h1>
  <p>تشكيلة راقية من أفضل المنتجات بأسعار لا تُنافَس، مع ضمان التوصيل السريع لباب منزلك</p>
</section>

<!-- PRODUCTS -->
<section class="products-section">
  <p class="section-title">منتجاتنا المميزة</p>
  <p class="section-sub">اضغط على المنتج لاختياره</p>

  <div class="products-grid" id="productsGrid">

    <!-- PRODUCT 1: Watch -->
    <div class="product-card" onclick="selectProduct(this, 0)" data-price="4500" data-name="ساعة كلاسيك فاخرة" data-class="p1">
      <div class="product-badge">-30%</div>
      <div class="selected-check">
        <svg viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="3"><polyline points="20 6 9 17 4 12"/></svg>
      </div>
      <div class="product-img-wrap p1">
        <svg viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
          <rect x="35" y="10" width="30" height="8" rx="3" fill="#C9A84C"/>
          <rect x="35" y="82" width="30" height="8" rx="3" fill="#C9A84C"/>
          <circle cx="50" cy="50" r="28" fill="#1a1230" stroke="#C9A84C" stroke-width="3"/>
          <circle cx="50" cy="50" r="22" fill="#0d0a20"/>
          <circle cx="50" cy="50" r="3" fill="#C9A84C"/>
          <line x1="50" y1="50" x2="50" y2="34" stroke="#C9A84C" stroke-width="2" stroke-linecap="round"/>
          <line x1="50" y1="50" x2="62" y2="55" stroke="#E8C97A" stroke-width="1.5" stroke-linecap="round"/>
          <circle cx="50" cy="30" r="2" fill="#C9A84C" opacity="0.6"/>
          <circle cx="50" cy="70" r="2" fill="#C9A84C" opacity="0.6"/>
          <circle cx="30" cy="50" r="2" fill="#C9A84C" opacity="0.6"/>
          <circle cx="70" cy="50" r="2" fill="#C9A84C" opacity="0.6"/>
        </svg>
      </div>
      <div class="product-info">
        <div class="product-name">ساعة كلاسيك فاخرة</div>
        <div class="product-desc">ساعة يد أنيقة بإطار ذهبي وزجاج كريستال مقاوم للخدش</div>
        <div class="product-footer">
          <div class="product-price">4,500 <span>دج</span></div>
          <div class="stars">★★★★★</div>
        </div>
      </div>
    </div>

    <!-- PRODUCT 2: Perfume -->
    <div class="product-card" onclick="selectProduct(this, 1)" data-price="2800" data-name="عطر أوريانت" data-class="p2">
      <div class="product-badge new">جديد</div>
      <div class="selected-check">
        <svg viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="3"><polyline points="20 6 9 17 4 12"/></svg>
      </div>
      <div class="product-img-wrap p2">
        <svg viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
          <rect x="42" y="15" width="16" height="8" rx="2" fill="#C9A84C"/>
          <rect x="46" y="10" width="8" height="8" rx="1" fill="#E8C97A"/>
          <rect x="30" y="38" width="40" height="50" rx="8" fill="#0d2137" stroke="#C9A84C" stroke-width="1.5"/>
          <rect x="34" y="23" width="32" height="16" rx="4" fill="#1a4a6b" stroke="#C9A84C" stroke-width="1"/>
          <rect x="36" y="50" width="28" height="2" rx="1" fill="#C9A84C" opacity="0.3"/>
          <text x="50" y="72" text-anchor="middle" fill="#C9A84C" font-size="7" font-family="serif" font-style="italic">Orient</text>
          <ellipse cx="50" cy="80" rx="10" ry="3" fill="#C9A84C" opacity="0.2"/>
          <circle cx="50" cy="30" r="3" fill="#E8C97A"/>
        </svg>
      </div>
      <div class="product-info">
        <div class="product-name">عطر أوريانت الملكي</div>
        <div class="product-desc">عطر شرقي فاخر بمزيج من العود والمسك يدوم طوال اليوم</div>
        <div class="product-footer">
          <div class="product-price">2,800 <span>دج</span></div>
          <div class="stars">★★★★☆</div>
        </div>
      </div>
    </div>

    <!-- PRODUCT 3: Bag -->
    <div class="product-card" onclick="selectProduct(this, 2)" data-price="5200" data-name="حقيبة جلد طبيعي" data-class="p3">
      <div class="selected-check">
        <svg viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="3"><polyline points="20 6 9 17 4 12"/></svg>
      </div>
      <div class="product-img-wrap p3">
        <svg viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M36 35 Q36 24 50 24 Q64 24 64 35" stroke="#C9A84C" stroke-width="3" fill="none" stroke-linecap="round"/>
          <rect x="22" y="35" width="56" height="45" rx="8" fill="#6b1a1a" stroke="#C9A84C" stroke-width="1.5"/>
          <rect x="22" y="35" width="56" height="12" rx="6" fill="#5a1515" stroke="#C9A84C" stroke-width="1"/>
          <rect x="38" y="53" width="24" height="16" rx="4" fill="#3a0f0f" stroke="#C9A84C" stroke-width="1"/>
          <circle cx="50" cy="61" r="3" fill="#C9A84C"/>
          <line x1="44" y1="41" x2="56" y2="41" stroke="#C9A84C" stroke-width="1.5" stroke-linecap="round"/>
        </svg>
      </div>
      <div class="product-info">
        <div class="product-name">حقيبة جلد طبيعي</div>
        <div class="product-desc">حقيبة يد نسائية من الجلد الأصلي بتصميم عصري وأنيق</div>
        <div class="product-footer">
          <div class="product-price">5,200 <span>دج</span></div>
          <div class="stars">★★★★★</div>
        </div>
      </div>
    </div>

    <!-- PRODUCT 4: Glasses -->
    <div class="product-card" onclick="selectProduct(this, 3)" data-price="1900" data-name="نظارة شمسية برميوم" data-class="p4">
      <div class="product-badge">-20%</div>
      <div class="selected-check">
        <svg viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="3"><polyline points="20 6 9 17 4 12"/></svg>
      </div>
      <div class="product-img-wrap p4">
        <svg viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
          <line x1="10" y1="50" x2="22" y2="50" stroke="#C9A84C" stroke-width="3" stroke-linecap="round"/>
          <line x1="78" y1="50" x2="90" y2="50" stroke="#C9A84C" stroke-width="3" stroke-linecap="round"/>
          <circle cx="32" cy="50" r="16" fill="#0d1a0d" stroke="#C9A84C" stroke-width="2.5"/>
          <circle cx="68" cy="50" r="16" fill="#0d1a0d" stroke="#C9A84C" stroke-width="2.5"/>
          <line x1="48" y1="50" x2="52" y2="50" stroke="#C9A84C" stroke-width="2" stroke-linecap="round"/>
          <circle cx="32" cy="50" r="10" fill="rgba(26,92,26,0.4)"/>
          <circle cx="68" cy="50" r="10" fill="rgba(26,92,26,0.4)"/>
          <circle cx="27" cy="45" r="3" fill="rgba(255,255,255,0.15)"/>
          <circle cx="63" cy="45" r="3" fill="rgba(255,255,255,0.15)"/>
        </svg>
      </div>
      <div class="product-info">
        <div class="product-name">نظارة شمسية برميوم</div>
        <div class="product-desc">نظارة شمسية بعدسات مستقطبة UV400 وإطار معدني خفيف</div>
        <div class="product-footer">
          <div class="product-price">1,900 <span>دج</span></div>
          <div class="stars">★★★★☆</div>
        </div>
      </div>
    </div>

  </div>

  <!-- ORDER FORM -->
  <div class="order-section">
    <div class="form-card">
      <div class="form-header">
        <h2>🛒 أكمل طلبك</h2>
        <p>أدخل بياناتك وسنتصل بك لتأكيد الطلب خلال 24 ساعة</p>
      </div>

      <!-- Selected Product Preview -->
      <div class="selected-product-preview" id="productPreview">
        <div class="preview-icon p1" id="previewIcon">
          <svg viewBox="0 0 100 100" fill="none">
            <circle cx="50" cy="50" r="28" fill="#1a1230" stroke="#C9A84C" stroke-width="3"/>
            <circle cx="50" cy="50" r="22" fill="#0d0a20"/>
            <circle cx="50" cy="50" r="3" fill="#C9A84C"/>
            <line x1="50" y1="50" x2="50" y2="34" stroke="#C9A84C" stroke-width="2" stroke-linecap="round"/>
          </svg>
        </div>
        <div class="preview-text">
          <h4 id="previewName">ساعة كلاسيك فاخرة</h4>
          <p>✅ متوفر - توصيل 3-5 أيام</p>
        </div>
        <div class="preview-price" id="previewPrice">4,500 دج</div>
      </div>

      <div class="form-grid">
        <div class="form-group">
          <label>الاسم الكامل</label>
          <input type="text" id="nameInput" placeholder="مثال: أحمد بن علي">
        </div>
        <div class="form-group">
          <label>رقم الهاتف</label>
          <input type="tel" id="phoneInput" placeholder="0550 123 456">
        </div>
        <div class="form-group full">
          <label>الولاية</label>
          <div class="select-wrapper">
            <select id="stateSelect">
              <option value="">اختر ولايتك</option>
              <option>الجزائر</option><option>البليدة</option><option>وهران</option>
              <option>قسنطينة</option><option>سطيف</option><option>عنابة</option>
              <option>باتنة</option><option>تلمسان</option><option>بجاية</option>
              <option>تيزي وزو</option><option>مستغانم</option><option>سكيكدة</option>
              <option>الشلف</option><option>تبسة</option><option>بسكرة</option>
              <option>ورقلة</option><option>أدرار</option><option>تمنراست</option>
              <option>إليزي</option><option>أم البواقي</option><option>خنشلة</option>
              <option>سوق أهراس</option><option>جيجل</option><option>ميلة</option>
              <option>برج بوعريريج</option><option>المسيلة</option><option>المدية</option>
              <option>تيسمسيلت</option><option>البويرة</option><option>بومرداس</option>
              <option>بوعلام</option><option>النعامة</option><option>سعيدة</option>
              <option>معسكر</option><option>البيض</option><option>تيارت</option>
              <option>غليزان</option><option>الأغواط</option><option>الجلفة</option>
              <option>غرداية</option><option>الوادي</option><option>توقرت</option>
              <option>بريكة</option><option>عين الدفلى</option><option>عين تموشنت</option>
              <option>خميستي</option><option>عين ولمان</option><option>برج باجي مختار</option>
              <option>أولاد جلال</option><option>تيميمون</option><option>ورقلة</option>
              <option>إن صالح</option><option>إن قزام</option><option>توقرت</option>
              <option>جانت</option><option>المغير</option><option>المنيعة</option>
              <option>تندوف</option>
            </select>
          </div>
        </div>
        <div class="form-group full">
          <label>العنوان التفصيلي</label>
          <input type="text" id="addressInput" placeholder="الحي، الشارع، رقم المبنى...">
        </div>
        <div class="form-group">
          <label>الكمية</label>
          <div class="qty-control">
            <button class="qty-btn" onclick="changeQty(-1)">−</button>
            <div class="qty-value" id="qtyDisplay">1</div>
            <button class="qty-btn" onclick="changeQty(1)">+</button>
          </div>
        </div>
        <div class="form-group">
          <label>طريقة الدفع</label>
          <div class="select-wrapper">
            <select>
              <option>💵 الدفع عند الاستلام</option>
              <option>🏦 تحويل بنكي</option>
              <option>📱 بريدي موب</option>
            </select>
          </div>
        </div>
      </div>

      <div class="summary-box">
        <div class="summary-row"><span>سعر المنتج</span><span id="summaryPrice">4,500 دج</span></div>
        <div class="summary-row"><span>الكمية</span><span id="summaryQty">× 1</span></div>
        <div class="summary-row"><span>رسوم التوصيل</span><span>مجاني 🎉</span></div>
        <div class="summary-row total"><span>المجموع</span><span class="amount" id="summaryTotal">4,500 دج</span></div>
      </div>

      <button class="submit-btn" onclick="submitOrder()">
        <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="20 6 9 17 4 12"/></svg>
        تأكيد الطلب الآن
      </button>

      <div class="trust-badges">
        <div class="trust-badge">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>
          دفع آمن
        </div>
        <div class="trust-badge">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>
          توصيل سريع
        </div>
        <div class="trust-badge">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M22 16.92v3a2 2 0 0 1-2.18 2A19.79 19.79 0 0 1 4.28 4.18 2 2 0 0 1 6.27 2h3a2 2 0 0 1 2 1.72c.127.96.361 1.903.7 2.81a2 2 0 0 1-.45 2.11L10.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0 1 24 16.92z"/></svg>
          دعم 24/7
        </div>
        <div class="trust-badge">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="1 4 1 10 7 10"/><path d="M3.51 15a9 9 0 1 0 .49-4.02"/></svg>
          إرجاع مجاني
        </div>
      </div>
    </div>
  </div>
</section>

<!-- SUCCESS MODAL -->
<div class="modal-overlay" id="successModal">
  <div class="modal">
    <div class="modal-icon">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="20 6 9 17 4 12"/></svg>
    </div>
    <h2>تم تأكيد طلبك! 🎉</h2>
    <p>شكراً لك! سيتصل بك أحد موظفينا خلال ساعات قليلة لتأكيد طلبك وتحديد موعد التوصيل.</p>
    <button class="modal-close" onclick="closeModal()">عودة للمتجر</button>
  </div>
</div>

<script>
  const products = [
    { name: "ساعة كلاسيك فاخرة", price: 4500, cls: "p1", svg: `<svg viewBox="0 0 100 100" fill="none"><circle cx="50" cy="50" r="28" fill="#1a1230" stroke="#C9A84C" stroke-width="3"/><circle cx="50" cy="50" r="22" fill="#0d0a20"/><circle cx="50" cy="50" r="3" fill="#C9A84C"/><line x1="50" y1="50" x2="50" y2="34" stroke="#C9A84C" stroke-width="2" stroke-linecap="round"/><line x1="50" y1="50" x2="62" y2="55" stroke="#E8C97A" stroke-width="1.5" stroke-linecap="round"/></svg>` },
    { name: "عطر أوريانت الملكي", price: 2800, cls: "p2", svg: `<svg viewBox="0 0 100 100" fill="none"><rect x="30" y="38" width="40" height="50" rx="8" fill="#0d2137" stroke="#C9A84C" stroke-width="1.5"/><circle cx="50" cy="30" r="3" fill="#E8C97A"/></svg>` },
    { name: "حقيبة جلد طبيعي", price: 5200, cls: "p3", svg: `<svg viewBox="0 0 100 100" fill="none"><rect x="22" y="35" width="56" height="45" rx="8" fill="#6b1a1a" stroke="#C9A84C" stroke-width="1.5"/><path d="M36 35 Q36 24 50 24 Q64 24 64 35" stroke="#C9A84C" stroke-width="3" fill="none" stroke-linecap="round"/><circle cx="50" cy="61" r="3" fill="#C9A84C"/></svg>` },
    { name: "نظارة شمسية برميوم", price: 1900, cls: "p4", svg: `<svg viewBox="0 0 100 100" fill="none"><circle cx="32" cy="50" r="16" fill="#0d1a0d" stroke="#C9A84C" stroke-width="2.5"/><circle cx="68" cy="50" r="16" fill="#0d1a0d" stroke="#C9A84C" stroke-width="2.5"/><line x1="48" y1="50" x2="52" y2="50" stroke="#C9A84C" stroke-width="2"/><line x1="10" y1="50" x2="22" y2="50" stroke="#C9A84C" stroke-width="3" stroke-linecap="round"/><line x1="78" y1="50" x2="90" y2="50" stroke="#C9A84C" stroke-width="3" stroke-linecap="round"/></svg>` }
  ];

  let selectedIndex = 0;
  let qty = 1;

  function selectProduct(card, index) {
    document.querySelectorAll('.product-card').forEach(c => c.classList.remove('selected'));
    card.classList.add('selected');
    selectedIndex = index;
    const p = products[index];
    document.getElementById('previewName').textContent = p.name;
    document.getElementById('previewPrice').textContent = p.price.toLocaleString() + ' دج';
    const icon = document.getElementById('previewIcon');
    icon.className = 'preview-icon ' + p.cls;
    icon.innerHTML = p.svg;
    updateSummary();
  }

  function changeQty(delta) {
    qty = Math.max(1, Math.min(10, qty + delta));
    document.getElementById('qtyDisplay').textContent = qty;
    updateSummary();
  }

  function updateSummary() {
    const p = products[selectedIndex];
    document.getElementById('summaryPrice').textContent = p.price.toLocaleString() + ' دج';
    document.getElementById('summaryQty').textContent = '× ' + qty;
    document.getElementById('summaryTotal').textContent = (p.price * qty).toLocaleString() + ' دج';
  }

  function submitOrder() {
    const name = document.getElementById('nameInput').value.trim();
    const phone = document.getElementById('phoneInput').value.trim();
    const state = document.getElementById('stateSelect').value;
    const address = document.getElementById('addressInput').value.trim();
    if (!name || !phone || !state || !address) {
      alert('⚠️ يرجى ملء جميع الحقول المطلوبة');
      return;
    }
    document.getElementById('successModal').classList.add('show');
  }

  function closeModal() {
    document.getElementById('successModal').classList.remove('show');
    document.getElementById('nameInput').value = '';
    document.getElementById('phoneInput').value = '';
    document.getElementById('stateSelect').value = '';
    document.getElementById('addressInput').value = '';
    qty = 1;
    document.getElementById('qtyDisplay').textContent = '1';
    updateSummary();
  }

  // Select first product by default
  document.querySelector('.product-card').classList.add('selected');
</script>

</body>
</html>
