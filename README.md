# bakevibe.
bakevibe is a online   bakery website which gives you fresh bakery items
#codes
#HTML used in fronted page
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Bakevibe — Fresh Daily</title>u

  <!-- Google fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

  <!-- Font Awesome -->
  <link rel="stylesheet"
        href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/7.0.1/css/all.min.css"
        integrity="sha512-2SwdPD6INVrV/lHTZbO2nodKhrnDdJK9/kg2XD1r9uGqPo1cUbujc+IYdlYdEErWNu69gVcYgdxlmVmzTWnetw=="
        crossorigin="anonymous" referrerpolicy="no-referrer" />

  <!-- Main stylesheet -->
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header class="site-header">
    <div class="container navbar">
      <a class="logo" href="#"><span class="logo-txt">Bake</span><span class="logo-sub">vibe</span></a>

      <nav class="nav">
        <ul class="navlist">
          <li><a href="#home" class="navlinks active">Home</a></li>
          <li><a href="#about" class="navlinks">About</a></li>
          <li><a href="#menu" class="navlinks">Menu</a></li>
          <li><a href="#gallery" class="navlinks">Gallery</a></li>
          <li><a href="#contact" class="navlinks">Contact</a></li>
        </ul>

        <div class="nav-icon">
          <button id="cart-toggle" class="icon-btn" aria-label="Open cart"><i class="fa-solid fa-cart-shopping"></i><span id="cart-count">0</span></button>
          <a href="#" class="icon-btn" aria-label="Profile"><i class="fa-solid fa-user"></i></a>
        </div>

        <button class="hamburger" aria-label="Toggle menu">
          <span class="bar"></span>
          <span class="bar"></span>
          <span class="bar"></span>
        </button>
      </nav>
    </div>
  </header>

  <main>
    <!-- HERO -->
    <section id="home" class="hero-section">
      <div class="container hero-grid">
        <div class="hero-text">
          <h1>Fresh Bakery Delights — Straight From Our Oven</h1>
          <p>Handmade breads, pastries, and cakes crafted daily using the finest ingredients. Order online for pickup or delivery.</p>
          <div class="hero-ctas">
            <a class="btn" href="#menu">View Menu</a>
            <a class="btn ghost" href="#contact">Contact Us</a>
          </div>
        </div>
        <div class="hero-image">
          <img src="https://images.unsplash.com/photo-1542831371-d531d36971e6?w=1200&q=80&auto=format&fit=crop" alt="Assorted bakery items">
        </div>
      </div>
    </section>

    <!-- ABOUT -->
    <section id="about" class="section container about">
      <h2>About Bakevibe</h2>
      <p>WLast Updated: [20/06/2024]
Welcome to [Bakevibe]. By placing an order with us or using our services, you agree to the following Terms & Conditions. Please read them carefully.

1. Orders
1.1 All orders are subject to availability and confirmation.
1.2 Custom orders must be placed at least [X days] in advance.
1.3 We reserve the right to decline orders that cannot be reasonably fulfilled.
1.4 Order details (design, flavor, size, pickup/delivery date) must be confirmed in writing.</p>
    </section>

    <!-- MENU -->
    <section id="menu" class="section container menu">
      <h2>Menu</h2>
      <div class="menu-grid">
        <!-- Each card includes data used by JS to add to cart -->
        <article class="card">
          <img src="https://images.unsplash.com/photo-1542831371-d531d36971e6?w=800&q=80&auto=format&fit=crop" alt="Sourdough loaf" />
          <div class="card-body">
            <h3 class="item-title">Sourdough Loaf</h3>
            <p class="item-desc">Crispy crust, open crumb — naturally leavened.</p>
            <div class="card-footer">
              <div class="price">₹150</div>
              <button class="btn add-to-cart" data-id="sourdough" data-title="Sourdough Loaf" data-price="150">Add</button>
            </div>
          </div>
        </article>
      </div>
    </section>

    <!-- GALLERY -->
    <section id="gallery" class="section container gallery">
      <h2>Gallery</h2>
      <div class="gallery-grid">
        <img class="gallery-img" src="https://images.unsplash.com/photo-1452195100486-9cc805987862?w=800&q=80&auto=format&fit=crop" alt="Baked muffins">
        <img class="gallery-img" src="https://images.unsplash.com/photo-1494438639946-1ebd1d20bf85?w=800&q=80&auto=format&fit=crop" alt="Loaves on shelf">
        <img class="gallery-img" src="https://images.unsplash.com/photo-1512058564366-c9e3d1f9f3f0?w=800&q=80&auto=format&fit=crop" alt="Pastries close up">
        <img class="gallery-img" src="https://images.unsplash.com/photo-1544025162-d76694265947?w=800&q=80&auto=format&fit=crop" alt="Decorated cakes">
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" class="section container contact">
      <h2>Contact & Orders</h2>
      <div class="contact-grid">
        <div>
          <p><strong>Address:</strong> shop no 24, Bakevibe, sector 38 gurugram </p>
          <p><strong>Phone:</strong> +91 8890338669, 9457196657</p>
          <p><strong>owner:</strong> Hemant and Himanshu</p>
          <p><strong>Opening:</strong> Mon–Sun, 7:00 AM – 8:00 PM</p>
        </div>

        <form id="contact-form" class="contact-form" action="#" onsubmit="return false;">
          <input type="text" id="name" placeholder="Your name" required>
          <input type="email" id="email" placeholder="Email" required>
          <textarea id="message" rows="4" placeholder="Message / order details"></textarea>
          <button class="btn" id="send-msg">Send Message</button>
        </form>
      </div>
    </section>
  </main>

  <!-- CART MODAL (hidden) -->
  <div id="cart-modal" class="cart-modal" aria-hidden="true">
    <div class="cart-panel">
      <header class="cart-header">
        <h3>Your Cart</h3>
        <button id="close-cart" class="btn ghost">Close</button>
      </header>
      <div id="cart-items" class="cart-items"></div>
      <footer class="cart-footer">
        <div class="cart-total">Total: <span id="cart-total">₹0</span></div>
        <div class="cart-actions">
          <button id="clear-cart" class="btn ghost">Clear</button>
          <button id="checkout" class="btn">Checkout</button>
        </div>
      </footer>
    </div>
  </div>

  <!-- Lightbox -->
  <div id="lightbox" class="lightbox" aria-hidden="true">
    <div class="lightbox-inner">
      <img id="lightbox-img" src="" alt="">
      <p id="lightbox-caption"></p>
      <div class="lightbox-actions">
        <button id="lb-add" class="btn">Add to cart</button>
        <button id="lb-close" class="btn ghost">Close</button>
      </div>
    </div>
  </div>

  <footer class="site-footer">
    <div class="container">
      <p>&copy; <span id="year"></span> Bakevibe. All rights reserved.</p>
    </div>
  </footer>

  <!-- JS -->
  <script src="main.js"></script>
</body>
</html>

#style.css used in styling
/* Base / variables */
:root{
  --pink: #FF006E;
  --white: #fff;
  --black: #111;
  --muted: #6b6b6b;
  --accent: #8381D9;
  --bg: #FAE7E5;
  --card: #fff;
  --shadow: 0 8px 24px rgba(0,0,0,0.08);
  --radius: 12px;
}

*{ box-sizing: border-box; margin:0; padding:0; font-family: 'Poppins', sans-serif; }
img{ display:block; max-width:100%; height:auto; }

.container{ width:90%; max-width:1200px; margin:0 auto; }

/* header */
.site-header{ background:#3b3b3b; color:var(--white); }
.navbar{ display:flex; align-items:center; justify-content:space-between; padding:1rem 0; gap:1rem; }
.logo{ display:flex; align-items:baseline; gap:0.6rem; text-decoration:none; color:inherit; }
.logo-txt{ font-size:1.6rem; font-weight:700; color:var(--accent); }
.logo-sub{ color:#fff; font-weight:600; font-size:0.95rem; opacity:0.9; }

.nav{ display:flex; align-items:center; gap:1rem; width:100%; }
.navlist{ display:flex; gap:1.4rem; list-style:none; align-items:center; margin-left:1rem; }
.navlinks{ color:#fff; text-decoration:none; font-weight:600; transition:color .2s; }
.navlinks:hover, .navlinks.active{ color:var(--pink); }

.icon-btn{ background:transparent; border:none; color:#fff; cursor:pointer; font-size:1rem; position:relative; padding:0.3rem 0.6rem; border-radius:8px; }
.icon-btn i{ font-size:1.1rem; }
#cart-count{ background:var(--pink); color:#fff; border-radius:999px; padding:2px 6px; font-size:0.75rem; margin-left:8px; }

/* hamburger (mobile) */
.hamburger{ display:none; background:transparent; border:none; flex-direction:column; gap:6px; padding:0.25rem; }
.hamburger .bar{ width:22px; height:2px; background:#fff; display:block; border-radius:2px; }

/* hero */
.hero-section{ background:var(--bg); padding:3.2rem 0; }
.hero-grid{ display:grid; grid-template-columns: 1fr 1fr; gap:2rem; align-items:center; }
.hero-text h1{ font-size:2.4rem; margin-bottom:0.6rem; color:var(--black); }
.hero-text p{ color:var(--muted); margin-bottom:1rem; max-width:60ch; }
.hero-ctas .btn{ margin-right:0.6rem; }

/* buttons */
.btn{ background:var(--pink); color:#fff; border:none; padding:0.7rem 1rem; border-radius:8px; cursor:pointer; font-weight:600; }
.btn.ghost{ background:transparent; border:1px solid #ddd; color:var(--black); }
.btn.small{ padding:0.35rem 0.6rem; font-size:0.95rem; }

/* sections */
.section{ padding:2.2rem 0; }
.section h2{ font-size:1.6rem; margin-bottom:0.6rem; color:var(--black); }

/* menu grid */
.menu-grid{ display:grid; grid-template-columns: repeat(2, 1fr); gap:1rem; }
.card{ background:var(--card); border-radius:12px; box-shadow:var(--shadow); overflow:hidden; display:flex; flex-direction:column; }
.card img{ height:160px; object-fit:cover; }
.card-body{ padding:0.9rem; display:flex; flex-direction:column; gap:0.6rem; flex:1; }
.card-footer{ display:flex; justify-content:space-between; align-items:center; margin-top:auto; }

/* gallery */
.gallery-grid{ display:grid; grid-template-columns: repeat(4, 1fr); gap:0.6rem; margin-top:1rem; }
.gallery-img{ width:100%; height:160px; object-fit:cover; border-radius:8px; cursor:zoom-in; }

/* contact */
.contact-grid{ display:grid; grid-template-columns: 1fr 1fr; gap:1rem; align-items:start; }
.contact-form input, .contact-form textarea{ width:100%; padding:0.7rem; border-radius:8px; border:1px solid #eee; margin-bottom:0.6rem; }

/* footer */
.site-footer{ background:#111; color:#fff; padding:1rem 0; text-align:center; }

/* cart modal */
.cart-modal{ position:fixed; inset:0; display:none; align-items:center; justify-content:center; background:rgba(0,0,0,0.45); z-index:2000; }
.cart-panel{ width:90%; max-width:520px; background:#fff; border-radius:12px; padding:1rem; box-shadow:var(--shadow); }
.cart-header{ display:flex; justify-content:space-between; align-items:center; }
.cart-items{ max-height:320px; overflow:auto; margin:0.8rem 0; }
.cart-footer{ display:flex; justify-content:space-between; align-items:center; gap:1rem; }

/* lightbox */
.lightbox{ position:fixed; inset:0; display:none; align-items:center; justify-content:center; background:rgba(0,0,0,0.7); z-index:3000; }
.lightbox-inner{ max-width:900px; width:90%; background:#fff; padding:1rem; border-radius:10px; text-align:center; }
.lightbox-inner img{ max-height:60vh; object-fit:contain; margin-bottom:0.6rem; }

/* responsive */
@media (max-width:900px){
  .hero-grid{ grid-template-columns: 1fr; }
  .menu-grid{ grid-template-columns: 1fr; }
  .gallery-grid{ grid-template-columns: repeat(2, 1fr); }
  .contact-grid{ grid-template-columns: 1fr; used}
  .navlist{ display:none; position:absolute; right:1rem; top:68px; background:#3b3b3b; padding:0.8rem 1rem; border-radius:8px; flex-direction:column; gap:0.6rem; }
  .hamburger{ display:flex; }
  .nav.open .navlist{ display:flex; }
}

/* small screens */
@media (max-width:480px){
  .navbar{ gap:.5rem; }
  .logo-txt{ font-size:1.25rem; }
  .hero-text h1{ font-size:1.4rem; }
  .gallery-img{ height:120px; }
}
#java script used in backend

// main.js - adds interactivity: hamburger, smooth scroll, gallery lightbox, cart with localStorage, simple contact action

/* -------------------------
   Utilities & DOM helpers
   ------------------------- */
const $ = (sel) => document.querySelector(sel);
const $$ = (sel) => Array.from(document.querySelectorAll(sel));

/* -------------------------
   DOM Ready
   ------------------------- */
document.addEventListener('DOMContentLoaded', () => {
  document.getElementById('year').textContent = new Date().getFullYear();
  initHamburger();
  initSmoothScroll();
  initGalleryLightbox();
  initMenuAddToCart();
  initCartModal();
  initContactForm();
});

/* -------------------------
   Hamburger menu (mobile)
   ------------------------- */
function initHamburger() {
  const ham = $('.hamburger');
  const nav = $('.nav');
  if (!ham || !nav) return;
  ham.addEventListener('click', () => {
    nav.classList.toggle('open');
  });
}

/* -------------------------
   Smooth scroll for anchors
   ------------------------- */
function initSmoothScroll(){
  $$('a[href^="#"]').forEach(a => {
    a.addEventListener('click', (e) => {
      const href = a.getAttribute('href');
      if (href.length > 1) {
        const target = document.querySelector(href);
        if (target) {
          e.preventDefault();
          target.scrollIntoView({ behavior: 'smooth', block: 'start' });
          // close mobile menu
          const nav = $('.nav');
          if (nav && nav.classList.contains('open')) nav.classList.remove('open');
        }
      }
    });
  });
}

/* -------------------------
   Lightbox for gallery images
   ------------------------- */
function initGalleryLightbox(){
  const imgs = $$('.gallery-img');
  const lb = $('#lightbox');
  const lbImg = $('#lightbox-img');
  const lbCap = $('#lightbox-caption');
  const lbClose = $('#lb-close');
  const lbAdd = $('#lb-add');

  if (!lb) return;

  imgs.forEach((img, idx) => {
    img.addEventListener('click', () => {
      lbImg.src = img.src;
      lbImg.alt = img.alt || '';
      lbCap.textContent = img.alt || '';
      lb.dataset.current = idx;
      lb.style.display = 'flex';
      lb.setAttribute('aria-hidden', 'false');
    });
  });

  lbClose.addEventListener('click', closeLb);
  lb.addEventListener('click', (e) => { if (e.target === lb) closeLb(); });

  // Add to cart from lightbox - uses deterministic id & price
  lbAdd.addEventListener('click', () => {
    const title = lbImg.alt || `Gallery Item`;
    const id = `gallery-${lb.dataset.current || 0}`;
    const price = generatePrice(title);
    addToCart({ id, title, price, qty: 1 });
    showToast(`${title} added to cart`);
    closeLb();
  });

  function closeLb() { lb.style.display = 'none'; lb.setAttribute('aria-hidden', 'true'); }

  function generatePrice(name) {
    let sum = 0;
    for (let i = 0; i < name.length; i++) sum += name.charCodeAt(i);
    return Math.round((sum % 500) + 50);
  }
}

/* -------------------------
   Menu add-to-cart buttons
   ------------------------- */
function initMenuAddToCart(){
  $$('.add-to-cart').forEach(btn => {
    btn.addEventListener('click', () => {
      const id = btn.dataset.id;
      const title = btn.dataset.title;
      const price = Number(btn.dataset.price);
      addToCart({ id, title, price, qty: 1 });
      showToast(`${title} added to cart`);
    });
  });
}

/* -------------------------
   Shopping cart (localStorage)
   ------------------------- */
const CART_KEY = 'pepsu_bakery_cart_v1';
let cart = loadCart();
updateCartUI();

function loadCart(){
  try { return JSON.parse(localStorage.getItem(CART_KEY)) || []; } catch (e) { return []; }
}
function saveCart(){ localStorage.setItem(CART_KEY, JSON.stringify(cart)); updateCartUI(); }

function addToCart(item){
  const found = cart.find(i => i.id === item.id);
  if (found) found.qty += item.qty; else cart.push(item);
  saveCart();
}
function clearCart(){ cart = []; saveCart(); }

function updateCartUI(){
  const count = cart.reduce((s,i)=>s+i.qty,0);
  const cartCountEl = $('#cart-count');
  if (cartCountEl) cartCountEl.textContent = count;
  renderCartItems();
}

function renderCartItems(){
  const list = $('#cart-items');
  const totalEl = $('#cart-total');
  if (!list || !totalEl) return;
  list.innerHTML = '';
  if (cart.length === 0){
    list.innerHTML = `<p style="color:#666">Your cart is empty.</p>`;
    totalEl.textContent = '₹0';
    return;
  }
  let total = 0;
  cart.forEach((item, idx) => {
    total += item.price * item.qty;
    const row = document.createElement('div');
    row.className = 'cart-row';
    row.style.display = 'flex';
    row.style.justifyContent = 'space-between';
    row.style.alignItems = 'center';
    row.style.padding = '0.5rem 0';
    row.innerHTML = `
      <div>
        <div style="font-weight:600">${item.title}</div>
        <div style="font-size:0.9rem;color:#666">₹${item.price} x ${item.qty}</div>
      </div>
      <div style="display:flex;gap:0.4rem;align-items:center">
        <button class="btn small" data-action="dec" data-idx="${idx}">-</button>
        <button class="btn small" data-action="inc" data-idx="${idx}">+</button>
        <button class="btn small" data-action="remove" data-idx="${idx}">Remove</button>
      </div>
    `;
    list.appendChild(row);
  });
  totalEl.textContent = `₹${total}`;

  // attach actions
  list.querySelectorAll('button').forEach(b => {
    const idx = Number(b.dataset.idx);
    const act = b.dataset.action;
    b.addEventListener('click', () => {
      if (act === 'inc') cart[idx].qty += 1;
      if (act === 'dec') { cart[idx].qty = Math.max(1, cart[idx].qty - 1); }
      if (act === 'remove') cart.splice(idx,1);
      saveCart();
    });
  });
}

/* -------------------------
   Cart modal & actions
   ------------------------- */
function initCartModal(){
  const modal = $('#cart-modal');
  const toggle = $('#cart-toggle');
  const close = $('#close-cart');
  const clearBtn = $('#clear-cart');
  const checkout = $('#checkout');

  if (!modal || !toggle) return;

  toggle.addEventListener('click', () => { modal.style.display = 'flex'; modal.setAttribute('aria-hidden','false'); renderCartItems(); });
  close.addEventListener('click', () => { modal.style.display = 'none'; modal.setAttribute('aria-hidden','true'); });
  modal.addEventListener('click', (e) => { if (e.target === modal) { modal.style.display='none'; modal.setAttribute('aria-hidden','true'); } });

  clearBtn.addEventListener('click', () => { clearCart(); showToast('Cart cleared'); modal.style.display = 'none'; });
  checkout.addEventListener('click', () => {
    if (cart.length === 0) { showToast('Cart is empty'); return; }
    // demo checkout: clear cart and show thank you
    clearCart();
    modal.style.display = 'none';
    showToast('Thanks! Your order was received (demo)');
  });
}

/* -------------------------
   Toast helper
   ------------------------- */
let toastTimer = null;
function showToast(msg, duration = 2200) {
  let toast = $('#site-toast');
  if (!toast) {
    toast = document.createElement('div');
    toast.id = 'site-toast';
    toast.style.cssText = 'position:fixed;left:50%;transform:translateX(-50%);bottom:80px;background:rgba(0,0,0,0.8);color:#fff;padding:0.6rem 1rem;border-radius:8px;display:none;z-index:4000;';
    document.body.appendChild(toast);
  }
  toast.textContent = msg;
  toast.style.display = 'block';
  if (toastTimer) clearTimeout(toastTimer);
  toastTimer = setTimeout(()=>{ toast.style.display = 'none'; }, duration);
}

/* -------------------------
   Contact form (demo)
   ------------------------- */
function initContactForm(){
  const form = $('#contact-form');
  if (!form) return;
  form.addEventListener('submit', (e) => {
    e.preventDefault();
    const name = $('#name').value.trim();
    const email = $('#email').value.trim();
    const message = $('#message').value.trim();
    if (!name || !email) { showToast('Please enter name & email'); return; }
    // demo behavior: clear and show toast
    $('#name').value = ''; $('#email').value = ''; $('#message').value = '';
    showToast('Message sent — we will contact you soon');
  });
}

