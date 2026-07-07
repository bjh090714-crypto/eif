<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>🍢 분식이네 키오스크</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@400;500;700;900&display=swap');

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --red: #D92B2B;
      --red-dark: #B02020;
      --red-light: #FDEAEA;
      --yellow: #F5C300;
      --yellow-light: #FFFBEA;
      --bg: #FFF8F0;
      --white: #FFFFFF;
      --gray-100: #F5F5F5;
      --gray-200: #E8E8E8;
      --gray-400: #AAAAAA;
      --gray-700: #444444;
      --text: #1A1A1A;
      --shadow: 0 2px 12px rgba(0,0,0,0.10);
      --shadow-lg: 0 6px 28px rgba(0,0,0,0.13);
    }

    body {
      font-family: 'Noto Sans KR', sans-serif;
      background: var(--bg);
      color: var(--text);
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }

    /* ── 헤더 ── */
    header {
      background: var(--red);
      color: white;
      padding: 18px 32px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      box-shadow: var(--shadow);
      position: sticky;
      top: 0;
      z-index: 100;
    }
    .header-logo { font-size: 24px; font-weight: 900; letter-spacing: -0.5px; }
    .header-logo span { color: var(--yellow); }
    .header-time { font-size: 13px; opacity: 0.85; }

    /* ── 카테고리 탭 ── */
    .category-bar {
      background: var(--white);
      border-bottom: 2px solid var(--gray-200);
      display: flex;
      gap: 4px;
      padding: 0 24px;
      overflow-x: auto;
    }
    .cat-btn {
      padding: 14px 20px;
      font-size: 14px;
      font-weight: 700;
      font-family: inherit;
      border: none;
      background: none;
      cursor: pointer;
      color: var(--gray-400);
      border-bottom: 3px solid transparent;
      margin-bottom: -2px;
      transition: color 0.15s, border-color 0.15s;
      white-space: nowrap;
    }
    .cat-btn.active { color: var(--red); border-color: var(--red); }
    .cat-btn:hover:not(.active) { color: var(--gray-700); }

    /* ── 메인 레이아웃 ── */
    .main {
      display: flex;
      flex: 1;
      gap: 0;
      max-width: 1100px;
      width: 100%;
      margin: 0 auto;
      padding: 24px 16px;
      gap: 20px;
      align-items: flex-start;
    }

    /* ── 메뉴 그리드 ── */
    .menu-section { flex: 1; min-width: 0; }
    .menu-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(175px, 1fr));
      gap: 14px;
    }
    .menu-card {
      background: var(--white);
      border-radius: 14px;
      box-shadow: var(--shadow);
      overflow: hidden;
      cursor: pointer;
      transition: transform 0.15s, box-shadow 0.15s;
      border: 2px solid transparent;
      position: relative;
    }
    .menu-card:hover { transform: translateY(-3px); box-shadow: var(--shadow-lg); }
    .menu-card.selected { border-color: var(--red); }
    .menu-card.sold-out { opacity: 0.5; pointer-events: none; }

    .menu-img {
      width: 100%;
      aspect-ratio: 1/1;
      object-fit: cover;
      font-size: 52px;
      display: flex;
      align-items: center;
      justify-content: center;
      background: var(--gray-100);
    }
    .menu-info { padding: 10px 12px 12px; }
    .menu-name { font-size: 14px; font-weight: 700; margin-bottom: 4px; }
    .menu-desc { font-size: 11px; color: var(--gray-400); margin-bottom: 8px; line-height: 1.5; }
    .menu-price { font-size: 15px; font-weight: 900; color: var(--red); }
    .sold-out-badge {
      position: absolute; top: 10px; right: 10px;
      background: rgba(0,0,0,0.55); color: white;
      font-size: 11px; font-weight: 700;
      padding: 3px 8px; border-radius: 20px;
    }
    .badge-best {
      position: absolute; top: 10px; left: 10px;
      background: var(--yellow); color: #7A5800;
      font-size: 11px; font-weight: 700;
      padding: 3px 8px; border-radius: 20px;
    }

    /* ── 주문 사이드바 ── */
    .order-panel {
      width: 300px;
      flex-shrink: 0;
      background: var(--white);
      border-radius: 16px;
      box-shadow: var(--shadow-lg);
      display: flex;
      flex-direction: column;
      position: sticky;
      top: 80px;
      max-height: calc(100vh - 100px);
    }
    .order-header {
      background: var(--red);
      color: white;
      padding: 16px 20px;
      border-radius: 14px 14px 0 0;
      font-size: 16px;
      font-weight: 900;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .order-count {
      background: var(--yellow);
      color: #7A5800;
      font-size: 12px;
      font-weight: 900;
      padding: 3px 9px;
      border-radius: 20px;
    }
    .order-list {
      flex: 1;
      overflow-y: auto;
      padding: 12px 16px;
      min-height: 120px;
    }
    .order-empty {
      text-align: center;
      color: var(--gray-400);
      font-size: 13px;
      padding: 32px 0;
      line-height: 1.8;
    }
    .order-item {
      display: flex;
      align-items: center;
      gap: 10px;
      padding: 10px 0;
      border-bottom: 1px solid var(--gray-200);
    }
    .order-item:last-child { border-bottom: none; }
    .order-item-emoji { font-size: 24px; width: 36px; text-align: center; }
    .order-item-info { flex: 1; min-width: 0; }
    .order-item-name { font-size: 13px; font-weight: 700; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
    .order-item-price { font-size: 12px; color: var(--red); font-weight: 700; }
    .qty-controls { display: flex; align-items: center; gap: 6px; }
    .qty-btn {
      width: 26px; height: 26px;
      border-radius: 50%;
      border: 1.5px solid var(--gray-200);
      background: none;
      font-size: 16px;
      font-weight: 700;
      cursor: pointer;
      display: flex; align-items: center; justify-content: center;
      color: var(--gray-700);
      transition: background 0.1s;
    }
    .qty-btn:hover { background: var(--gray-100); }
    .qty-btn.minus:hover { border-color: var(--red); color: var(--red); }
    .qty-num { font-size: 14px; font-weight: 700; min-width: 18px; text-align: center; }

    .order-footer { padding: 14px 16px; border-top: 2px solid var(--gray-200); }
    .order-total {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 12px;
    }
    .total-label { font-size: 13px; color: var(--gray-700); font-weight: 500; }
    .total-price { font-size: 22px; font-weight: 900; color: var(--red); }

    .btn-order {
      width: 100%;
      padding: 15px;
      background: var(--red);
      color: white;
      border: none;
      border-radius: 10px;
      font-size: 16px;
      font-weight: 900;
      font-family: inherit;
      cursor: pointer;
      transition: background 0.15s, transform 0.1s;
    }
    .btn-order:hover:not(:disabled) { background: var(--red-dark); transform: translateY(-1px); }
    .btn-order:disabled { background: var(--gray-200); color: var(--gray-400); cursor: not-allowed; transform: none; }
    .btn-clear {
      width: 100%;
      padding: 9px;
      margin-top: 8px;
      background: none;
      border: 1.5px solid var(--gray-200);
      border-radius: 8px;
      font-size: 13px;
      font-weight: 500;
      font-family: inherit;
      cursor: pointer;
      color: var(--gray-700);
      transition: border-color 0.1s;
    }
    .btn-clear:hover { border-color: var(--red); color: var(--red); }

    /* ── 모달 ── */
    .modal-overlay {
      display: none;
      position: fixed; inset: 0;
      background: rgba(0,0,0,0.5);
      z-index: 999;
      align-items: center;
      justify-content: center;
    }
    .modal-overlay.open { display: flex; }
    .modal {
      background: white;
      border-radius: 20px;
      padding: 36px 32px;
      max-width: 380px;
      width: 90%;
      text-align: center;
      box-shadow: var(--shadow-lg);
      animation: pop 0.2s ease;
    }
    @keyframes pop { from { transform: scale(0.85); opacity: 0; } to { transform: scale(1); opacity: 1; } }
    .modal-emoji { font-size: 56px; margin-bottom: 16px; }
    .modal-title { font-size: 22px; font-weight: 900; margin-bottom: 8px; }
    .modal-desc { font-size: 14px; color: var(--gray-700); line-height: 1.7; margin-bottom: 24px; }
    .modal-btn {
      padding: 13px 36px;
      background: var(--red);
      color: white;
      border: none;
      border-radius: 10px;
      font-size: 15px;
      font-weight: 700;
      font-family: inherit;
      cursor: pointer;
    }
    .modal-btn:hover { background: var(--red-dark); }

    @media (max-width: 700px) {
      .main { flex-direction: column; padding: 16px 10px; }
      .order-panel { width: 100%; position: static; max-height: none; }
    }
  </style>
</head>
<body>

<header>
  <div class="header-logo">🍢 <span>분식이네</span></div>
  <div class="header-time" id="clock"></div>
</header>

<div class="category-bar" id="categoryBar"></div>

<div class="main">
  <section class="menu-section">
    <div class="menu-grid" id="menuGrid"></div>
  </section>

  <aside class="order-panel">
    <div class="order-header">
      🛒 주문 내역
      <span class="order-count" id="orderCount">0개</span>
    </div>
    <div class="order-list" id="orderList">
      <div class="order-empty">아직 선택한 메뉴가 없어요<br>🍽️ 메뉴를 골라보세요!</div>
    </div>
    <div class="order-footer">
      <div class="order-total">
        <span class="total-label">합계</span>
        <span class="total-price" id="totalPrice">0원</span>
      </div>
      <button class="btn-order" id="orderBtn" disabled onclick="placeOrder()">주문하기</button>
      <button class="btn-clear" onclick="clearOrder()">전체 취소</button>
    </div>
  </aside>
</div>

<div class="modal-overlay" id="modalOverlay">
  <div class="modal">
    <div class="modal-emoji">🎉</div>
    <div class="modal-title">주문이 완료됐어요!</div>
    <div class="modal-desc" id="modalDesc"></div>
    <button class="modal-btn" onclick="closeModal()">확인</button>
  </div>
</div>

<script>
  // ── 메뉴 데이터 ──
  const menus = [
    { id:1, cat:'떡볶이', name:'국물 떡볶이', price:4000, emoji:'🍢', desc:'매콤달콤 국물이 자박한 정통 떡볶이', best:true },
    { id:2, cat:'떡볶이', name:'로제 떡볶이', price:5000, emoji:'🍝', desc:'크리미한 로제 소스로 부드럽게', best:false },
    { id:3, cat:'떡볶이', name:'치즈 떡볶이', price:5500, emoji:'🧀', desc:'녹진한 치즈가 듬뿍 올라간 떡볶이', best:false },
    { id:4, cat:'순대', name:'순대 한 접시', price:4000, emoji:'🌭', desc:'탱글탱글 쫄깃한 당면 순대', best:true },
    { id:5, cat:'순대', name:'순대국밥', price:7000, emoji:'🍲', desc:'진한 국물의 든든한 순대국밥', best:false },
    { id:6, cat:'튀김', name:'튀김 모둠', price:3000, emoji:'🍤', desc:'오징어·야채·새우 튀김 모둠', best:true },
    { id:7, cat:'튀김', name:'고구마 튀김', price:2500, emoji:'🍠', desc:'달콤한 고구마 튀김 5개', best:false },
    { id:8, cat:'튀김', name:'꽈배기', price:2000, emoji:'🥨', desc:'바삭 달콤한 설탕 꽈배기', best:false },
    { id:9, cat:'라면', name:'라볶이', price:5500, emoji:'🍜', desc:'라면+떡볶이 최강 조합', best:true },
    { id:10, cat:'라면', name:'짜파구리', price:6000, emoji:'🍝', desc:'짜파게티+너구리 프리미엄 조합', best:false },
    { id:11, cat:'김밥', name:'참치 김밥', price:3500, emoji:'🍱', desc:'고소한 참치마요 김밥', best:true },
    { id:12, cat:'김밥', name:'치즈 김밥', price:3500, emoji:'🧀', desc:'쭉 늘어나는 치즈가 가득', best:false },
    { id:13, cat:'김밥', name:'꼬마 김밥', price:2500, emoji:'🍙', desc:'한입에 쏙! 작고 귀여운 꼬마김밥', best:false },
    { id:14, cat:'어묵', name:'어묵탕', price:2000, emoji:'🍡', desc:'따뜻한 국물이 있는 꼬치 어묵', best:true },
    { id:15, cat:'어묵', name:'어묵볶음', price:4000, emoji:'🥘', desc:'매콤하게 볶은 어묵 볶음', best:false },
    { id:16, cat:'음료', name:'달달 식혜', price:1500, emoji:'🥤', desc:'시원하고 달콤한 전통 식혜', best:false },
    { id:17, cat:'음료', name:'매실 음료', price:1500, emoji:'🍵', desc:'새콤달콤 매실 원액 음료', best:false },
  ];

  const categories = ['전체', ...new Set(menus.map(m => m.cat))];
  let currentCat = '전체';
  let cart = {}; // { id: qty }

  // ── 시계 ──
  function updateClock() {
    const now = new Date();
    document.getElementById('clock').textContent =
      now.toLocaleTimeString('ko-KR', { hour: '2-digit', minute: '2-digit' });
  }
  updateClock();
  setInterval(updateClock, 1000);

  // ── 카테고리 렌더 ──
  function renderCategories() {
    const bar = document.getElementById('categoryBar');
    bar.innerHTML = categories.map(cat =>
      `<button class="cat-btn ${cat === currentCat ? 'active' : ''}" onclick="selectCat('${cat}')">${cat}</button>`
    ).join('');
  }

  function selectCat(cat) {
    currentCat = cat;
    renderCategories();
    renderMenus();
  }

  // ── 메뉴 렌더 ──
  function renderMenus() {
    const filtered = currentCat === '전체' ? menus : menus.filter(m => m.cat === currentCat);
    const grid = document.getElementById('menuGrid');
    grid.innerHTML = filtered.map(menu => `
      <div class="menu-card ${cart[menu.id] ? 'selected' : ''}" onclick="addToCart(${menu.id})">
        ${menu.best ? '<span class="badge-best">⭐ BEST</span>' : ''}
        <div class="menu-img">${menu.emoji}</div>
        <div class="menu-info">
          <div class="menu-name">${menu.name}</div>
          <div class="menu-desc">${menu.desc}</div>
          <div class="menu-price">${menu.price.toLocaleString()}원</div>
        </div>
      </div>
    `).join('');
  }

  // ── 장바구니 ──
  function addToCart(id) {
    cart[id] = (cart[id] || 0) + 1;
    renderMenus();
    renderCart();
  }

  function changeQty(id, delta) {
    cart[id] = (cart[id] || 0) + delta;
    if (cart[id] <= 0) delete cart[id];
    renderMenus();
    renderCart();
  }

  function clearOrder() {
    cart = {};
    renderMenus();
    renderCart();
  }

  function renderCart() {
    const list = document.getElementById('orderList');
    const ids = Object.keys(cart);

    if (ids.length === 0) {
      list.innerHTML = '<div class="order-empty">아직 선택한 메뉴가 없어요<br>🍽️ 메뉴를 골라보세요!</div>';
      document.getElementById('totalPrice').textContent = '0원';
      document.getElementById('orderCount').textContent = '0개';
      document.getElementById('orderBtn').disabled = true;
      return;
    }

    let total = 0;
    let totalQty = 0;
    list.innerHTML = ids.map(id => {
      const menu = menus.find(m => m.id == id);
      const qty = cart[id];
      total += menu.price * qty;
      totalQty += qty;
      return `
        <div class="order-item">
          <div class="order-item-emoji">${menu.emoji}</div>
          <div class="order-item-info">
            <div class="order-item-name">${menu.name}</div>
            <div class="order-item-price">${(menu.price * qty).toLocaleString()}원</div>
          </div>
          <div class="qty-controls">
            <button class="qty-btn minus" onclick="changeQty(${id}, -1)">−</button>
            <span class="qty-num">${qty}</span>
            <button class="qty-btn" onclick="changeQty(${id}, 1)">+</button>
          </div>
        </div>
      `;
    }).join('');

    document.getElementById('totalPrice').textContent = total.toLocaleString() + '원';
    document.getElementById('orderCount').textContent = totalQty + '개';
    document.getElementById('orderBtn').disabled = false;
  }

  // ── 주문 완료 ──
  function placeOrder() {
    const ids = Object.keys(cart);
    const itemNames = ids.map(id => {
      const menu = menus.find(m => m.id == id);
      return `${menu.name} ${cart[id]}개`;
    }).join(', ');
    const total = ids.reduce((s, id) => s + menus.find(m => m.id == id).price * cart[id], 0);

    document.getElementById('modalDesc').innerHTML =
      `<b>${itemNames}</b><br><br>합계 <b style="color:#D92B2B">${total.toLocaleString()}원</b><br><br>잠시 후 나옵니다 😊`;

    document.getElementById('modalOverlay').classList.add('open');
    cart = {};
    renderMenus();
    renderCart();
  }

  function closeModal() {
    document.getElementById('modalOverlay').classList.remove('open');
  }

  // ── 초기화 ──
  renderCategories();
  renderMenus();
</script>
</body>
</html>
