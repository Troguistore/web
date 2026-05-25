<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TROGÜI - Tienda Online Colombia 🇨🇴</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700;800;900&family=Nunito:wght@400;600;700;800;900&display=swap" rel="stylesheet">
<style>
:root{
  --orange:#FF5200;
  --orange-light:#FF7A3D;
  --dark:#1a1a2e;
  --white:#fff;
  --light:#f5f5f5;
  --green:#00b050;
  --red:#e00;
  --gray:#666;
  --border:#e8e8e8;
  --shadow:0 4px 24px rgba(0,0,0,.10);
  --shadow-hover:0 12px 40px rgba(255,82,0,.18);
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{font-family:'Nunito',sans-serif;background:#f2f2f2;color:var(--dark);overflow-x:hidden}
a{text-decoration:none;color:inherit}
img{max-width:100%}
button{font-family:'Nunito',sans-serif}

/* TOPBAR */
.topbar{background:var(--dark);color:#fff;text-align:center;padding:8px 12px;font-size:13px;font-weight:700;letter-spacing:.3px;position:relative;overflow:hidden}
.topbar span{color:var(--orange)}
.topbar-scroll{display:inline-block;white-space:nowrap;animation:marquee 30s linear infinite}
@keyframes marquee{0%{transform:translateX(100vw)}100%{transform:translateX(-100%)}}

/* HEADER */
header{background:#fff;box-shadow:0 2px 16px rgba(0,0,0,.1);position:sticky;top:0;z-index:900}
.header-inner{max-width:1320px;margin:0 auto;display:flex;align-items:center;gap:14px;padding:10px 16px;flex-wrap:wrap}
.logo-area{min-width:150px}
.logo-img{height:50px;width:auto;object-fit:contain}
.search-bar{flex:1;min-width:200px;position:relative}
.search-bar input{width:100%;padding:11px 48px 11px 18px;border:2.5px solid var(--border);border-radius:30px;font-size:15px;font-family:'Nunito',sans-serif;outline:none;transition:.25s;background:#fafafa}
.search-bar input:focus{border-color:var(--orange);background:#fff;box-shadow:0 0 0 4px rgba(255,82,0,.08)}
.search-bar button{position:absolute;right:6px;top:50%;transform:translateY(-50%);background:var(--orange);border:none;border-radius:50%;width:36px;height:36px;color:#fff;cursor:pointer;font-size:16px;display:flex;align-items:center;justify-content:center;transition:.2s}
.search-bar button:hover{background:#e04800;transform:translateY(-50%) scale(1.08)}
.header-actions{display:flex;align-items:center;gap:10px;flex-wrap:wrap}
.wa-btn{display:flex;align-items:center;gap:6px;background:#25D366;color:#fff;padding:9px 16px;border-radius:22px;font-weight:800;font-size:13px;transition:.2s;white-space:nowrap}
.wa-btn:hover{background:#128C7E;transform:scale(1.04)}
.cart-btn{position:relative;background:var(--orange);color:#fff;border:none;border-radius:22px;padding:9px 18px;font-weight:800;font-size:14px;cursor:pointer;display:flex;align-items:center;gap:7px;transition:.2s}
.cart-btn:hover{background:#e04800;transform:scale(1.04)}
.cart-count{background:#fff;color:var(--orange);border-radius:50%;min-width:22px;height:22px;font-size:12px;font-weight:900;display:flex;align-items:center;justify-content:center;padding:0 4px}
.socials{display:flex;gap:6px}
.socials a{width:36px;height:36px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:18px;transition:.2s}
.socials a:hover{transform:scale(1.15)}
.socials a.ig{background:linear-gradient(45deg,#f09433,#e6683c,#dc2743,#cc2366,#bc1888);color:#fff}
.socials a.tk{background:#010101;color:#fff}
.socials a.wa{background:#25D366;color:#fff}

/* NAV */
nav{background:var(--orange);position:sticky;top:70px;z-index:800}
.nav-inner{max-width:1320px;margin:0 auto;display:flex;gap:0;overflow-x:auto;scrollbar-width:none}
.nav-inner::-webkit-scrollbar{display:none}
.nav-inner a{color:#fff;padding:13px 20px;font-weight:800;font-size:13.5px;white-space:nowrap;border-bottom:3px solid transparent;transition:.2s;display:flex;align-items:center;gap:5px}
.nav-inner a:hover,.nav-inner a.active{border-bottom-color:#fff;background:rgba(255,255,255,.15)}

/* SLIDER */
.slider-section{background:#fff}
.slider-wrap{position:relative;overflow:hidden;height:280px}
.slider-track{display:flex;transition:transform .6s cubic-bezier(.4,0,.2,1);height:100%}
.slide{min-width:100%;height:100%;display:flex;align-items:center;position:relative;overflow:hidden}
.slide-1{background:linear-gradient(135deg,#1a1a2e 55%,#FF5200 100%)}
.slide-2{background:linear-gradient(135deg,#0d3b2e 55%,#00b050 100%)}
.slide-3{background:linear-gradient(135deg,#16213e 55%,#e94560 100%)}
.slide-content{color:#fff;padding:40px;z-index:2;max-width:600px}
.slide-content h2{font-size:clamp(22px,4vw,44px);font-weight:900;line-height:1.15;font-family:'Poppins',sans-serif}
.slide-content h2 span{color:var(--orange)}
.slide-content p{font-size:15px;margin:10px 0 20px;opacity:.9;line-height:1.5}
.slide-btn{background:var(--orange);color:#fff;padding:13px 30px;border-radius:30px;font-weight:900;font-size:15px;display:inline-block;transition:.25s;border:2px solid transparent}
.slide-btn:hover{background:transparent;border-color:#fff;transform:scale(1.05)}
.slide-deco{position:absolute;right:0;top:0;height:100%;width:45%;opacity:.08;background:radial-gradient(circle at center,#fff 0%,transparent 70%)}
.slider-arrow{position:absolute;top:50%;transform:translateY(-50%);background:rgba(255,255,255,.15);backdrop-filter:blur(4px);color:#fff;border:none;font-size:24px;width:46px;height:46px;border-radius:50%;cursor:pointer;z-index:10;transition:.2s;border:1px solid rgba(255,255,255,.2)}
.slider-arrow:hover{background:rgba(255,255,255,.3)}
.slider-arrow.prev{left:14px}
.slider-arrow.next{right:14px}
.slider-dots{display:flex;justify-content:center;gap:8px;padding:12px;background:#fff}
.dot{width:10px;height:10px;border-radius:50%;background:#ddd;cursor:pointer;transition:.3s}
.dot.active{background:var(--orange);width:28px;border-radius:5px}

/* BADGES */
.badges-strip{background:#fff;border-top:1px solid var(--border);border-bottom:3px solid var(--orange)}
.badges-inner{max-width:1320px;margin:0 auto;display:flex;justify-content:center;flex-wrap:wrap}
.badge-item{display:flex;align-items:center;gap:8px;padding:14px 22px;font-weight:800;font-size:13px;border-right:1px solid var(--border);color:var(--dark)}
.badge-item:last-child{border-right:none}
.badge-item em{color:var(--orange);font-style:normal}

/* SECTION TITLES */
.section-title{text-align:center;padding:32px 16px 6px;font-size:clamp(22px,3vw,30px);font-weight:900;font-family:'Poppins',sans-serif;color:var(--dark)}
.section-title span{color:var(--orange)}
.section-sub{text-align:center;color:var(--gray);margin-bottom:22px;font-size:14px;padding:0 16px}

/* PRODUCTS */
.products-section{max-width:1320px;margin:0 auto;padding:0 14px 50px}
.products-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(210px,1fr));gap:18px}

/* PRODUCT CARD */
.product-card{background:#fff;border-radius:18px;overflow:hidden;box-shadow:var(--shadow);transition:.28s;position:relative;display:flex;flex-direction:column}
.product-card:hover{transform:translateY(-5px);box-shadow:var(--shadow-hover)}
.product-img-wrap{position:relative;background:#f8f8f8;height:210px;overflow:hidden;display:flex;align-items:center;justify-content:center;cursor:pointer}
.product-img-wrap img{height:100%;width:100%;object-fit:cover;transition:.4s}
.product-card:hover .product-img-wrap img{transform:scale(1.07)}
.badge-off{position:absolute;top:10px;left:10px;background:var(--orange);color:#fff;font-size:11px;font-weight:900;padding:4px 10px;border-radius:20px;z-index:2}
.badge-sold-c{position:absolute;top:10px;right:10px;background:rgba(26,26,46,.85);color:#fff;font-size:10px;font-weight:700;padding:3px 8px;border-radius:10px;z-index:2}
.badge-last{position:absolute;bottom:10px;left:10px;background:var(--red);color:#fff;font-size:10px;font-weight:900;padding:3px 9px;border-radius:10px;z-index:2;animation:pulse 1.3s infinite}
@keyframes pulse{0%,100%{opacity:1}50%{opacity:.55}}
.product-info{padding:13px 13px 0;flex:1;cursor:pointer}
.product-name{font-weight:800;font-size:14px;line-height:1.35;margin-bottom:6px;font-family:'Poppins',sans-serif;display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden}
.stars{color:#f5c518;font-size:14px;margin-bottom:5px}
.stars span{color:var(--gray);font-size:12px;margin-left:4px}
.price-wrap{display:flex;align-items:center;gap:8px;flex-wrap:wrap;margin-bottom:5px}
.price-old{color:#aaa;font-size:13px;text-decoration:line-through}
.price-new{color:var(--orange);font-size:22px;font-weight:900}
.timer-badge{background:#fff5ee;border:1px solid #ffccaa;border-radius:8px;padding:4px 9px;font-size:11px;font-weight:800;color:var(--orange);display:flex;align-items:center;gap:4px;margin-bottom:6px}
.free-ship{font-size:11.5px;color:var(--green);font-weight:800;display:flex;align-items:center;gap:3px;margin-bottom:3px}
.contra-e{font-size:11px;color:var(--gray);margin-bottom:10px}
.card-btns{display:grid;grid-template-columns:1fr 1fr;gap:8px;padding:0 13px 13px;margin-top:auto}
.btn-add{background:var(--dark);color:#fff;border:none;padding:10px 6px;border-radius:12px;font-weight:800;font-size:13px;cursor:pointer;transition:.2s;width:100%}
.btn-add:hover{background:#0f0f25}
.btn-pedir{background:var(--orange);color:#fff;border:none;padding:10px 6px;border-radius:12px;font-weight:900;font-size:13px;cursor:pointer;width:100%;position:relative;overflow:hidden;transition:.2s}
.btn-pedir:hover{background:#e04800}
@keyframes shake{
  0%{transform:translateX(0) rotate(0)}
  15%{transform:translateX(-5px) rotate(-1.5deg)}
  30%{transform:translateX(5px) rotate(1.5deg)}
  45%{transform:translateX(-4px) rotate(-1deg)}
  60%{transform:translateX(4px) rotate(1deg)}
  75%{transform:translateX(-2px)}
  90%{transform:translateX(2px)}
  100%{transform:translateX(0)}
}
.btn-pedir.shaking{animation:shake .65s ease-in-out}

/* MODAL */
.modal-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.6);z-index:1100;align-items:center;justify-content:center;padding:16px}
.modal-overlay.active{display:flex}
.modal-box{background:#fff;border-radius:22px;max-width:720px;width:100%;max-height:92vh;overflow-y:auto;position:relative}
.modal-close{position:absolute;top:14px;right:14px;background:var(--dark);color:#fff;border:none;border-radius:50%;width:34px;height:34px;font-size:18px;cursor:pointer;z-index:10;display:flex;align-items:center;justify-content:center}
.modal-content{padding:26px}
.modal-gallery{display:grid;grid-template-columns:repeat(auto-fill,minmax(180px,1fr));gap:8px;margin-bottom:16px}
.modal-gallery img{border-radius:12px;height:190px;width:100%;object-fit:cover;cursor:pointer;transition:.2s;border:2px solid transparent}
.modal-gallery img:hover,.modal-gallery img.active-img{border-color:var(--orange)}
.modal-title{font-size:21px;font-weight:900;font-family:'Poppins',sans-serif;margin-bottom:8px}
.modal-price-wrap{display:flex;align-items:center;gap:14px;margin:10px 0;flex-wrap:wrap}
.modal-price-old{font-size:16px;text-decoration:line-through;color:#aaa}
.modal-price-new{font-size:30px;font-weight:900;color:var(--orange)}
.modal-desc{font-size:14px;color:#555;line-height:1.65;margin:12px 0}
.modal-delivery{background:#f0fff4;border:1px solid var(--green);border-radius:12px;padding:14px;margin:14px 0;font-size:13.5px}
.modal-delivery strong{color:var(--green)}
.btn-order{width:100%;background:var(--orange);color:#fff;border:none;padding:15px;border-radius:14px;font-weight:900;font-size:16px;cursor:pointer;margin-top:12px;transition:.2s}
.btn-order:hover{background:#e04800;transform:scale(1.02)}
.review-list{margin-top:22px}
.review-item{border:1px solid var(--border);border-radius:13px;padding:14px;margin-bottom:11px;background:#fafafa}
.review-top{display:flex;align-items:center;gap:10px;margin-bottom:6px}
.review-avatar{width:38px;height:38px;border-radius:50%;background:var(--orange);color:#fff;display:flex;align-items:center;justify-content:center;font-weight:900;font-size:16px;flex-shrink:0}
.review-name{font-weight:800;font-size:14px}
.review-stars{color:#f5c518;font-size:13px}
.review-text{font-size:13px;color:#444;line-height:1.55}

/* ORDER FORM */
.order-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.65);z-index:1200;align-items:center;justify-content:center;padding:16px}
.order-overlay.active{display:flex}
.order-form-box{background:#fff;border-radius:22px;max-width:540px;width:100%;max-height:92vh;overflow-y:auto;padding:28px;position:relative}
.form-title{font-size:21px;font-weight:900;font-family:'Poppins',sans-serif;margin-bottom:6px}
.form-prod{font-size:14px;color:var(--gray);margin-bottom:14px}
.form-price-show{background:#fff8f0;border:2.5px solid var(--orange);border-radius:13px;padding:14px;margin-bottom:18px;display:flex;justify-content:space-between;align-items:center}
.form-price-show .fprice{font-size:24px;font-weight:900;color:var(--orange)}
.form-price-show .fold{font-size:13px;text-decoration:line-through;color:#aaa}
.form-group{margin-bottom:14px}
.form-group label{font-weight:800;font-size:14px;display:block;margin-bottom:5px}
.req{color:var(--red)}
.form-group input,.form-group textarea,.form-group select{width:100%;padding:12px 14px;border:2px solid var(--border);border-radius:11px;font-size:14px;font-family:'Nunito',sans-serif;outline:none;transition:.2s;color:var(--dark);background:#fafafa}
.form-group input:focus,.form-group textarea:focus,.form-group select:focus{border-color:var(--orange);background:#fff}
.form-group textarea{resize:vertical;min-height:72px}
.btn-confirm{width:100%;background:var(--green);color:#fff;border:none;padding:15px;border-radius:14px;font-weight:900;font-size:16px;cursor:pointer;margin-top:10px;transition:.2s}
.btn-confirm:hover{background:#009040}
.btn-cancel-f{width:100%;background:#eee;color:var(--dark);border:none;padding:12px;border-radius:14px;font-weight:700;font-size:14px;cursor:pointer;margin-top:8px}

/* CART DRAWER */
.cart-drawer{position:fixed;right:-420px;top:0;height:100vh;width:390px;background:#fff;box-shadow:-6px 0 40px rgba(0,0,0,.18);z-index:1300;transition:.35s cubic-bezier(.4,0,.2,1);overflow-y:auto;padding:22px}
.cart-drawer.open{right:0}
.cart-title{font-size:21px;font-weight:900;font-family:'Poppins',sans-serif;margin-bottom:18px;display:flex;justify-content:space-between;align-items:center}
.cart-item{display:flex;gap:12px;border-bottom:1px solid var(--border);padding:13px 0;align-items:center}
.cart-item img{width:72px;height:72px;object-fit:cover;border-radius:10px;background:#f4f4f4;flex-shrink:0}
.cart-item-info{flex:1}
.cart-item-name{font-weight:800;font-size:14px;line-height:1.3;margin-bottom:3px}
.cart-item-price{color:var(--orange);font-weight:900;font-size:15px}
.cart-qty{display:flex;align-items:center;gap:8px;margin-top:5px}
.qty-btn{background:var(--border);border:none;border-radius:6px;width:26px;height:26px;font-weight:900;cursor:pointer;font-size:14px}
.qty-val{font-weight:800;font-size:14px;min-width:20px;text-align:center}
.cart-remove{color:var(--red);background:none;border:none;font-size:20px;cursor:pointer;flex-shrink:0;padding:0 4px}
.cart-total-row{font-size:18px;font-weight:900;color:var(--orange);text-align:right;margin:18px 0;padding-top:4px}
.btn-checkout{width:100%;background:var(--orange);color:#fff;border:none;padding:15px;border-radius:14px;font-weight:900;font-size:16px;cursor:pointer;transition:.2s}
.btn-checkout:hover{background:#e04800}
.empty-cart{text-align:center;color:var(--gray);padding:48px 0;font-size:15px}

/* DELIVERY CALC */
.delivery-wrap{max-width:520px;margin:0 auto 36px;background:#fff;border-radius:18px;padding:22px;box-shadow:var(--shadow)}
.delivery-wrap h3{font-size:18px;font-weight:900;margin-bottom:12px;font-family:'Poppins',sans-serif}
.delivery-result{background:#f0fff4;border:1px solid var(--green);border-radius:11px;padding:13px;font-size:14px;font-weight:700;color:#006630;margin-top:12px;display:none}

/* NOTIFICATION */
.notif{position:fixed;bottom:90px;left:16px;background:var(--dark);color:#fff;padding:12px 18px;border-radius:14px;font-size:13px;font-weight:700;z-index:1200;display:none;max-width:300px;box-shadow:0 6px 24px rgba(0,0,0,.35);animation:slideUp .4s}
@keyframes slideUp{from{opacity:0;transform:translateY(20px)}to{opacity:1;transform:translateY(0)}}
.notif .nn{color:var(--orange)}

/* ROULETTE MODAL */
.roulette-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.75);z-index:2000;align-items:center;justify-content:center;padding:16px}
.roulette-overlay.active{display:flex}
.roulette-box{background:#fff;border-radius:26px;max-width:500px;width:100%;padding:32px;text-align:center;position:relative;overflow:hidden}
.roulette-box::before{content:'';position:absolute;top:0;left:0;right:0;height:5px;background:linear-gradient(90deg,var(--orange),#ff9a5c,var(--orange))}
.roulette-title{font-size:26px;font-weight:900;font-family:'Poppins',sans-serif;margin-bottom:6px;color:var(--dark)}
.roulette-title span{color:var(--orange)}
.roulette-sub{font-size:14px;color:var(--gray);margin-bottom:22px}
.roulette-canvas-wrap{position:relative;width:280px;height:280px;margin:0 auto 20px}
.roulette-canvas-wrap canvas{border-radius:50%;box-shadow:0 8px 32px rgba(255,82,0,.25)}
.roulette-pointer{position:absolute;top:-18px;left:50%;transform:translateX(-50%);font-size:36px;filter:drop-shadow(0 2px 4px rgba(0,0,0,.3))}
.roulette-btn{background:var(--orange);color:#fff;border:none;padding:14px 36px;border-radius:30px;font-weight:900;font-size:17px;cursor:pointer;transition:.2s;margin-top:8px}
.roulette-btn:hover{background:#e04800;transform:scale(1.05)}
.roulette-btn:disabled{background:#ccc;cursor:not-allowed;transform:none}
.roulette-result{margin-top:18px;font-size:18px;font-weight:900;color:var(--orange);display:none;animation:slideUp .4s}
.roulette-close{position:absolute;top:14px;right:14px;background:var(--dark);color:#fff;border:none;border-radius:50%;width:32px;height:32px;font-size:17px;cursor:pointer;display:flex;align-items:center;justify-content:center}
.roulette-close:hover{background:#333}

/* ADMIN */
.admin-btns{position:fixed;bottom:16px;right:16px;display:flex;gap:8px;z-index:1100}
.admin-btn{width:38px;height:38px;border-radius:50%;border:none;font-weight:900;font-size:13px;cursor:pointer;opacity:.55;transition:.2s;box-shadow:0 2px 10px rgba(0,0,0,.25)}
.admin-btn:hover{opacity:1;transform:scale(1.12)}
.admin-btn.r-btn{background:var(--orange);color:#fff}
.admin-btn.c-btn{background:var(--dark);color:#fff}
.admin-btn.e-btn{background:#0f3460;color:#fff}

.admin-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.65);z-index:2000;align-items:flex-start;justify-content:center;padding:16px;overflow-y:auto}
.admin-overlay.active{display:flex}
.admin-panel{background:#fff;border-radius:22px;max-width:980px;width:100%;margin:20px auto;padding:26px;position:relative;max-height:90vh;overflow-y:auto}
.admin-panel h2{font-size:22px;font-weight:900;font-family:'Poppins',sans-serif;color:var(--orange);margin-bottom:20px}
.admin-product-item{border:2px solid var(--border);border-radius:14px;padding:18px;margin-bottom:14px}
.admin-product-item label{font-weight:800;font-size:13px;display:block;margin-bottom:3px;margin-top:10px}
.admin-product-item input,.admin-product-item textarea,.admin-product-item select{width:100%;padding:8px 12px;border:1.5px solid var(--border);border-radius:9px;font-size:13px;font-family:'Nunito',sans-serif}
.admin-row2{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.btn-save-admin{background:var(--green);color:#fff;border:none;padding:10px 20px;border-radius:10px;font-weight:800;cursor:pointer;margin-top:10px}
.btn-del-admin{background:var(--red);color:#fff;border:none;padding:6px 12px;border-radius:8px;font-weight:700;cursor:pointer;font-size:12px}
.btn-add-prod{background:var(--orange);color:#fff;border:none;padding:12px 24px;border-radius:12px;font-weight:900;cursor:pointer;font-size:15px;margin-bottom:20px}
.img-preview{width:80px;height:80px;object-fit:cover;border-radius:10px;border:2px solid var(--border);margin-top:6px;cursor:pointer}

.orders-stats{display:grid;grid-template-columns:repeat(auto-fit,minmax(120px,1fr));gap:10px;margin-bottom:18px}
.stat-card{background:#fff;border:2px solid var(--border);border-radius:13px;padding:14px;text-align:center}
.stat-card .sv{font-size:24px;font-weight:900;color:var(--orange)}
.stat-card .sl{font-size:12px;color:var(--gray);font-weight:700;margin-top:2px}
.orders-toolbar{display:flex;gap:10px;flex-wrap:wrap;margin-bottom:16px;padding:14px;background:#f8f8f8;border-radius:13px;align-items:center}
.orders-toolbar input{flex:1;min-width:160px;padding:9px 13px;border:1.5px solid var(--border);border-radius:9px;font-size:13px;font-family:'Nunito',sans-serif;outline:none}
.orders-toolbar input:focus{border-color:var(--orange)}
.order-card{border:2px solid var(--border);border-radius:15px;padding:16px;margin-bottom:12px;background:#fff;transition:.2s}
.order-card:hover{border-color:var(--orange);box-shadow:0 4px 18px rgba(255,82,0,.1)}
.order-product-name{font-size:15px;font-weight:900;color:var(--dark);font-family:'Poppins',sans-serif;margin-bottom:8px}
.order-grid{display:grid;grid-template-columns:1fr 1fr;gap:6px;font-size:13px}
.order-field .of-label{font-size:11px;font-weight:800;color:var(--gray);text-transform:uppercase;letter-spacing:.5px;display:block}
.order-field .of-value{font-weight:700;color:var(--dark)}
.order-price-row{display:flex;align-items:center;gap:10px;margin-top:10px;padding-top:10px;border-top:1px solid var(--border);flex-wrap:wrap}
.order-price-new{font-size:20px;font-weight:900;color:var(--orange)}
.order-price-old{font-size:13px;text-decoration:line-through;color:#aaa}
.order-wa-btn{margin-left:auto;background:#25D366;color:#fff;border:none;border-radius:10px;padding:8px 16px;font-weight:800;font-size:12px;cursor:pointer}
.order-nota{background:#fffbe6;border:1px solid #ffe082;border-radius:9px;padding:8px 12px;font-size:12px;color:#7a6000;margin-top:8px;font-weight:700}
.no-orders{text-align:center;padding:40px;color:var(--gray);font-size:15px}
.visitors-badge{background:var(--dark);color:#fff;border-radius:11px;padding:10px 16px;font-size:13px;font-weight:700;margin-bottom:16px;display:flex;align-items:center;gap:8px}
.visitors-dot{width:10px;height:10px;border-radius:50%;background:var(--green);animation:blink 1.1s infinite}
@keyframes blink{0%,100%{opacity:1}50%{opacity:.15}}

/* SEARCH DROPDOWN */
.search-dropdown{position:absolute;top:108%;left:0;right:0;background:#fff;border-radius:14px;box-shadow:0 10px 32px rgba(0,0,0,.14);z-index:600;display:none;max-height:300px;overflow-y:auto}
.search-dropdown.open{display:block}
.search-dd-item{padding:11px 16px;cursor:pointer;font-size:14px;border-bottom:1px solid var(--border);display:flex;align-items:center;gap:10px;transition:.15s}
.search-dd-item:hover{background:#fff8f0}
.search-dd-item img{width:40px;height:40px;object-fit:cover;border-radius:8px}
.search-dd-item .sdi-name{font-weight:800;font-size:14px}
.search-dd-item .sdi-price{color:var(--orange);font-weight:900;font-size:13px}

/* WA FLOAT */
.wa-float{position:fixed;bottom:90px;right:20px;background:#25D366;color:#fff;width:58px;height:58px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:28px;box-shadow:0 4px 20px rgba(0,0,0,.3);z-index:1000;transition:.2s}
.wa-float:hover{transform:scale(1.12);background:#128C7E}

/* FLOAT MSG */
.float-msg{position:fixed;bottom:160px;left:50%;transform:translateX(-50%);background:var(--dark);color:#fff;padding:11px 22px;border-radius:22px;font-weight:700;font-size:14px;z-index:9999;animation:slideUp .4s;white-space:nowrap}

/* PAGE EDITOR */
.page-editor-group{border:1.5px solid var(--border);border-radius:13px;padding:16px;margin-bottom:14px}
.page-editor-group label{font-weight:800;font-size:14px;display:block;margin-bottom:6px;color:var(--dark)}
.page-editor-group input,.page-editor-group textarea{width:100%;padding:9px 13px;border:1.5px solid var(--border);border-radius:9px;font-size:13px;font-family:'Nunito',sans-serif}
.page-editor-group textarea{min-height:64px;resize:vertical}
.admin-review-item{border:1.5px solid var(--border);border-radius:11px;padding:13px;margin-bottom:10px;display:grid;gap:6px}
.admin-review-item input,.admin-review-item textarea,.admin-review-item select{width:100%;padding:8px 11px;border:1.5px solid var(--border);border-radius:8px;font-size:13px;font-family:'Nunito',sans-serif}

/* RESPONSIVE */
@media(max-width:700px){
  .products-grid{grid-template-columns:repeat(2,1fr);gap:12px}
  .modal-gallery{grid-template-columns:1fr 1fr}
  .cart-drawer{width:100%;right:-110%}
  .slide-content{padding:24px}
  .admin-row2{grid-template-columns:1fr}
  .order-grid{grid-template-columns:1fr}
  .orders-stats{grid-template-columns:1fr 1fr}
  .card-btns{grid-template-columns:1fr 1fr}
  .badge-item{padding:9px 12px;font-size:12px}
}
@media(max-width:380px){
  .products-grid{grid-template-columns:1fr}
}

/* GIF/VIDEO in modal */
.modal-media-item{border-radius:12px;overflow:hidden;height:190px;object-fit:cover;width:100%}
</style>
</head>
<body>

<!-- TOPBAR -->
<div class="topbar">
  <div class="topbar-scroll" id="topbar-text">
    🇨🇴 Envíos a TODA Colombia &nbsp;|&nbsp; 💵 PAGO CONTRA ENTREGA &nbsp;|&nbsp; 📦 Interrapidísimo · Coordinadora · Envia &nbsp;|&nbsp; ⭐ +500 clientes felices &nbsp;|&nbsp; 🔒 Compra 100% segura &nbsp;|&nbsp; 🚚 Envío GRATIS en todos los productos
  </div>
</div>

<!-- HEADER -->
<header>
  <div class="header-inner">
    <div class="logo-area">
      <img src="https://i.imgur.com/7QZqKhP.png" alt="TROGÜI" class="logo-img" onerror="this.outerHTML='<svg width=\'140\' height=\'50\' viewBox=\'0 0 140 50\' xmlns=\'http://www.w3.org/2000/svg\'><rect width=\'140\' height=\'50\' rx=\'8\' fill=\'#FF5200\'/><text x=\'10\' y=\'36\' font-family=\'Poppins,sans-serif\' font-weight=\'900\' font-size=\'28\' fill=\'#1a1a2e\'>TROGÜI</text></svg>'">
    </div>
    <div class="search-bar" style="position:relative">
      <input type="text" id="search-input" placeholder="🔍  Buscar productos..." autocomplete="off" oninput="searchProducts(this.value)" onfocus="searchProducts(this.value)">
      <button onclick="doSearch()">🔍</button>
      <div class="search-dropdown" id="search-dropdown"></div>
    </div>
    <div class="header-actions">
      <a href="https://wa.link/lhneng" target="_blank" class="wa-btn">📱 320 657 2598</a>
      <div class="socials">
        <a href="https://www.instagram.com/store_trog" target="_blank" class="ig" title="Instagram">📸</a>
        <a href="https://www.tiktok.com/@trogui_store" target="_blank" class="tk" title="TikTok">🎵</a>
        <a href="https://wa.link/lhneng" target="_blank" class="wa" title="WhatsApp">💬</a>
      </div>
      <button class="cart-btn" onclick="toggleCart()">🛒 Carrito <span class="cart-count" id="cart-count">0</span></button>
    </div>
  </div>
</header>

<!-- NAV -->
<nav>
  <div class="nav-inner">
    <a href="#products" class="active" onclick="filterCat('all',this)">🏠 Todo</a>
    <a href="#products" onclick="filterCat('hogar',this)">🏡 Hogar</a>
    <a href="#products" onclick="filterCat('tecnologia',this)">📱 Tecnología</a>
    <a href="#products" onclick="filterCat('salud',this)">💊 Salud</a>
    <a href="#products" onclick="filterCat('belleza',this)">💄 Belleza</a>
    <a href="#products" onclick="filterCat('fitness',this)">🏋️ Fitness</a>
    <a href="#products" onclick="filterCat('accesorios',this)">👜 Accesorios</a>
    <a href="#products" onclick="filterCat('juguetes',this)">🧸 Juguetes</a>
    <a href="#products" onclick="filterCat('cocina',this)">🍳 Cocina</a>
  </div>
</nav>

<!-- SLIDER -->
<div class="slider-section">
  <div class="slider-wrap">
    <div class="slider-track" id="slider-track">
      <div class="slide slide-1">
        <div class="slide-deco"></div>
        <div class="slide-content">
          <h2>🇨🇴 Envío Gratis<br>a <span>Toda Colombia</span></h2>
          <p>Más de 35 productos increíbles · Pago contra entrega · Sin riesgo</p>
          <a href="#products" class="slide-btn">¡Ver Ofertas!</a>
        </div>
      </div>
      <div class="slide slide-2">
        <div class="slide-deco"></div>
        <div class="slide-content">
          <h2>💵 Pago<br><span>Contra Entrega</span></h2>
          <p>Pagas cuando recibes tu pedido. Sin tarjeta, sin riesgo, con confianza.</p>
          <a href="#products" class="slide-btn">Comprar Ahora</a>
        </div>
      </div>
      <div class="slide slide-3">
        <div class="slide-deco"></div>
        <div class="slide-content">
          <h2>📦 Recibe en<br><span>3 a 7 Días</span></h2>
          <p>Enviamos con Coordinadora, Interrapidísimo y Envia a todo el país.</p>
          <a href="#products" class="slide-btn">Ver Productos</a>
        </div>
      </div>
    </div>
    <button class="slider-arrow prev" onclick="moveSlider(-1)">‹</button>
    <button class="slider-arrow next" onclick="moveSlider(1)">›</button>
  </div>
  <div class="slider-dots" id="slider-dots">
    <div class="dot active" onclick="goSlide(0)"></div>
    <div class="dot" onclick="goSlide(1)"></div>
    <div class="dot" onclick="goSlide(2)"></div>
  </div>
</div>

<!-- BADGES -->
<div class="badges-strip">
  <div class="badges-inner">
    <div class="badge-item">✅ <em>Pago Contra Entrega</em></div>
    <div class="badge-item">🚚 <em>Envío GRATIS</em></div>
    <div class="badge-item">📦 <em>3 a 7 días hábiles</em></div>
    <div class="badge-item">🔒 <em>Compra Segura</em></div>
    <div class="badge-item">⭐ <em>+500 Clientes Felices</em></div>
  </div>
</div>

<!-- NOTIFICATION -->
<div class="notif" id="notif-box"></div>

<!-- PRODUCTS -->
<div id="products">
  <h2 class="section-title" id="products-title">🔥 Productos en <span>OFERTA</span></h2>
  <p class="section-sub">Envío gratis a toda Colombia · Pago contra entrega · ¡Precios increíbles!</p>
  <div class="products-section">
    <div class="products-grid" id="products-grid"></div>
  </div>
</div>

<!-- DELIVERY CALC -->
<div style="max-width:1320px;margin:0 auto;padding:0 14px 20px">
  <div class="delivery-wrap">
    <h3>📅 ¿Cuándo llega mi pedido?</h3>
    <p style="font-size:13px;color:var(--gray);margin-bottom:12px">Selecciona tu ciudad y te calculamos la fecha estimada:</p>
    <select id="delivery-city" style="width:100%;padding:11px;border:2px solid var(--border);border-radius:11px;font-size:14px;font-family:'Nunito',sans-serif;margin-bottom:10px;outline:none">
      <option value="">-- Selecciona tu ciudad --</option>
      <option value="3">Bogotá D.C.</option>
      <option value="4">Medellín</option>
      <option value="4">Cali</option>
      <option value="5">Barranquilla</option>
      <option value="5">Cartagena</option>
      <option value="5">Bucaramanga</option>
      <option value="6">Pereira</option>
      <option value="6">Manizales</option>
      <option value="7">Pasto</option>
      <option value="7">Montería</option>
      <option value="7">Leticia</option>
    </select>
    <button onclick="calcDelivery()" style="background:var(--orange);color:#fff;border:none;padding:11px 26px;border-radius:11px;font-weight:800;cursor:pointer;font-size:14px">Calcular Fecha</button>
    <div class="delivery-result" id="delivery-result"></div>
  </div>
</div>

<!-- PRODUCT MODAL -->
<div class="modal-overlay" id="product-modal">
  <div class="modal-box">
    <button class="modal-close" onclick="closeModal()">✕</button>
    <div class="modal-content" id="modal-content"></div>
  </div>
</div>

<!-- ORDER FORM -->
<div class="order-overlay" id="order-overlay">
  <div class="order-form-box">
    <h2 class="form-title">📋 Confirmar Pedido</h2>
    <p class="form-prod" id="form-prod-name"></p>
    <div class="form-price-show" id="form-price-show"></div>
    <div class="form-group"><label>Nombre <span class="req">*</span></label><input type="text" id="f-nombre" placeholder="Tu nombre completo"></div>
    <div class="form-group"><label>Apellido <span class="req">*</span></label><input type="text" id="f-apellido" placeholder="Tu apellido"></div>
    <div class="form-group">
      <label>Departamento <span class="req">*</span></label>
      <select id="f-departamento">
        <option value="">-- Selecciona --</option>
        <option>Amazonas</option><option>Antioquia</option><option>Arauca</option><option>Atlántico</option>
        <option>Bolívar</option><option>Boyacá</option><option>Caldas</option><option>Caquetá</option>
        <option>Casanare</option><option>Cauca</option><option>Cesar</option><option>Chocó</option>
        <option>Córdoba</option><option>Cundinamarca</option><option>Guainía</option><option>Guaviare</option>
        <option>Huila</option><option>La Guajira</option><option>Magdalena</option><option>Meta</option>
        <option>Nariño</option><option>Norte de Santander</option><option>Putumayo</option><option>Quindío</option>
        <option>Risaralda</option><option>San Andrés y Providencia</option><option>Santander</option>
        <option>Sucre</option><option>Tolima</option><option>Valle del Cauca</option><option>Vaupés</option>
        <option>Vichada</option><option>Bogotá D.C.</option>
      </select>
    </div>
    <div class="form-group"><label>Ciudad <span class="req">*</span></label><input type="text" id="f-ciudad" placeholder="Ej: Bogotá, Medellín, Cali..."></div>
    <div class="form-group"><label>Dirección completa <span class="req">*</span></label><input type="text" id="f-direccion" placeholder="Calle, carrera, barrio, apto..."></div>
    <div class="form-group"><label>Teléfono <span class="req">*</span></label><input type="tel" id="f-telefono" placeholder="Ej: 3001234567"></div>
    <div class="form-group"><label>Nota (opcional)</label><textarea id="f-nota" placeholder="Color, talla, variante u otro detalle..."></textarea></div>
    <button class="btn-confirm" onclick="confirmOrder()">✅ Confirmar Pedido por WhatsApp</button>
    <button class="btn-cancel-f" onclick="closeOrderForm()">Cancelar</button>
  </div>
</div>

<!-- CART DRAWER -->
<div class="cart-drawer" id="cart-drawer">
  <div class="cart-title">🛒 Mi Carrito <button onclick="toggleCart()" style="background:none;border:none;font-size:24px;cursor:pointer">✕</button></div>
  <div id="cart-items-list"></div>
  <div class="cart-total-row" id="cart-total"></div>
  <button class="btn-checkout" id="btn-checkout" onclick="checkoutCart()" style="display:none">Pedir Todo por WhatsApp 💬</button>
</div>

<!-- ROULETTE MODAL -->
<div class="roulette-overlay" id="roulette-overlay">
  <div class="roulette-box">
    <button class="roulette-close" onclick="closeRoulette()">✕</button>
    <div class="roulette-title">🎡 ¡Gira y <span>Gana!</span></div>
    <p class="roulette-sub">¡Gira la ruleta y obtén un premio especial para tu pedido!</p>
    <div class="roulette-canvas-wrap">
      <div class="roulette-pointer">▼</div>
      <canvas id="roulette-canvas" width="280" height="280"></canvas>
    </div>
    <button class="roulette-btn" id="roulette-btn" onclick="spinRoulette()">¡Girar Ruleta! 🎉</button>
    <div class="roulette-result" id="roulette-result"></div>
  </div>
</div>

<!-- ADMIN PANELS -->
<div class="admin-btns">
  <button class="admin-btn r-btn" title="Editar Productos" onclick="adminAuth('r')">R</button>
  <button class="admin-btn c-btn" title="Ver Pedidos" onclick="adminAuth('c')">C</button>
  <button class="admin-btn e-btn" title="Editar Página" onclick="adminAuth('e')">E</button>
</div>

<!-- ADMIN R: PRODUCTS -->
<div class="admin-overlay" id="admin-r">
  <div class="admin-panel">
    <h2>✏️ Editor de Productos</h2>
    <div class="visitors-badge"><span class="visitors-dot"></span><span id="v1">0</span> personas en la página ahora</div>
    <button class="btn-add-prod" onclick="addNewProduct()">+ Agregar Producto</button>
    <div id="admin-product-list"></div>
    <div style="display:flex;gap:10px;margin-top:18px;flex-wrap:wrap">
      <button class="btn-save-admin" onclick="saveAllProducts()">💾 Guardar Todos</button>
      <button onclick="closeAdmin('admin-r')" style="background:#eee;border:none;padding:10px 20px;border-radius:10px;cursor:pointer;font-weight:700">Cerrar</button>
    </div>
  </div>
</div>

<!-- ADMIN C: ORDERS -->
<div class="admin-overlay" id="admin-c">
  <div class="admin-panel">
    <h2>📦 Pedidos Recibidos</h2>
    <div class="visitors-badge"><span class="visitors-dot"></span><span id="v2">0</span> personas en la página ahora</div>
    <div class="orders-stats" id="orders-stats"></div>
    <div class="orders-toolbar">
      <input type="text" id="order-search" placeholder="🔍 Buscar por nombre, ciudad, producto..." oninput="filterOrders(this.value)">
      <button onclick="exportCSV()" style="background:var(--green);color:#fff;border:none;padding:9px 16px;border-radius:9px;font-weight:800;cursor:pointer;white-space:nowrap">📥 Exportar CSV</button>
      <button onclick="clearOrders()" style="background:var(--red);color:#fff;border:none;padding:9px 14px;border-radius:9px;font-weight:700;cursor:pointer;white-space:nowrap">🗑️ Limpiar</button>
    </div>
    <div id="admin-orders-list"></div>
    <button onclick="closeAdmin('admin-c')" style="background:#eee;border:none;padding:10px 20px;border-radius:10px;cursor:pointer;font-weight:700;margin-top:16px">Cerrar</button>
  </div>
</div>

<!-- ADMIN E: PAGE EDITOR -->
<div class="admin-overlay" id="admin-e">
  <div class="admin-panel">
    <h2>🎨 Editor de Página</h2>
    <div class="page-editor-group">
      <label>🔊 URL de Audio/Música de Fondo (MP3)</label>
      <input type="text" id="audio-url" placeholder="https://... .mp3">
      <button class="btn-save-admin" onclick="setAudio()" style="margin-top:8px">Aplicar Audio</button>
    </div>
    <div class="page-editor-group">
      <label>📢 Texto del Marquee (Barra superior)</label>
      <input type="text" id="edit-topbar" placeholder="Texto scrolling del topbar">
      <button class="btn-save-admin" onclick="saveSetting('topbar')" style="margin-top:8px">Guardar</button>
    </div>
    <div class="page-editor-group">
      <label>🏷️ Título de Sección Productos</label>
      <input type="text" id="edit-prod-title" placeholder="Ej: 🔥 Productos en OFERTA">
      <button class="btn-save-admin" onclick="saveSetting('prod-title')" style="margin-top:8px">Guardar</button>
    </div>
    <div class="page-editor-group">
      <label>⭐ Editar Reseñas</label>
      <div id="admin-reviews-list"></div>
      <button class="btn-save-admin" onclick="saveReviews()">💾 Guardar Reseñas</button>
    </div>
    <button onclick="closeAdmin('admin-e')" style="background:#eee;border:none;padding:10px 20px;border-radius:10px;cursor:pointer;font-weight:700;margin-top:16px">Cerrar</button>
  </div>
</div>

<a href="https://wa.link/lhneng" target="_blank" class="wa-float" title="WhatsApp">💬</a>
<audio id="bg-audio" loop style="display:none"><source id="bg-audio-src" src="" type="audio/mpeg"></audio>

<footer style="background:var(--dark);color:#fff;padding:44px 16px 22px;margin-top:30px">
  <div style="max-width:1320px;margin:0 auto;display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:32px">
    <div>
      <div style="font-size:30px;font-weight:900;color:var(--orange);margin-bottom:12px;font-family:'Poppins',sans-serif">TROGÜI</div>
      <p style="font-size:13px;color:#bbb;line-height:1.8">Tienda colombiana de confianza. Enviamos a todo el país con las mejores transportadoras.</p>
      <div style="display:flex;gap:10px;margin-top:14px">
        <a href="https://wa.link/lhneng" target="_blank" style="color:#25D366;font-size:24px">💬</a>
        <a href="https://www.instagram.com/store_trog" target="_blank" style="font-size:24px">📸</a>
        <a href="https://www.tiktok.com/@trogui_store" target="_blank" style="color:#fff;font-size:24px">🎵</a>
      </div>
    </div>
    <div>
      <h4 style="font-weight:800;margin-bottom:12px;color:var(--orange)">Contacto</h4>
      <ul style="list-style:none;font-size:13px;color:#bbb;line-height:2">
        <li>📞 320 657 2598</li>
        <li>📧 trogui.store@gmail.com</li>
        <li>🇨🇴 Colombia - Nacional</li>
      </ul>
    </div>
    <div>
      <h4 style="font-weight:800;margin-bottom:12px;color:var(--orange)">Transportadoras</h4>
      <ul style="list-style:none;font-size:13px;color:#bbb;line-height:2">
        <li>📦 Interrapidísimo</li>
        <li>📦 Coordinadora</li>
        <li>📦 Envia</li>
      </ul>
    </div>
    <div>
      <h4 style="font-weight:800;margin-bottom:12px;color:var(--orange)">Pagos</h4>
      <ul style="list-style:none;font-size:13px;color:#bbb;line-height:2">
        <li>💵 Contra Entrega</li>
        <li>🏦 Transferencia</li>
        <li>💳 Nequi / Daviplata</li>
      </ul>
    </div>
  </div>
  <div style="text-align:center;margin-top:32px;padding-top:20px;border-top:1px solid #333;font-size:12px;color:#888">© 2025 TROGÜI · Tienda Colombiana de Confianza 🇨🇴</div>
</footer>

<script>
const ADMIN_PASS = '4325';
let products = JSON.parse(localStorage.getItem('trogui_v2_products') || 'null') || [
  {id:'T001',name:'Escurridor Loza Con Tapa 65cm 2 Niveles',cat:'cocina',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1916715/1756999631142.png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1886527/1753723291WhatsApp%20Image%202025-07-27%20at%209.38.06%20PM%20(1).jpeg'],
   price:139000,oldPrice:220000,
   desc:'Escurreplatos con tapa innovadora que mantiene el polvo fuera. Gran capacidad para platos, cuencos, tazas y cubiertos. Fabricado en acero inoxidable con revestimiento negro resistente al óxido. 4 ventosas para mayor estabilidad. Diseño 2 niveles para máximo aprovechamiento del espacio.',
   sold:89,stars:5,lastUnits:false,timer:4*60*60},
  {id:'T002',name:'Maquina Quita Callos Eléctrica Removedor',cat:'salud',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1635913/1737489352Screenshot_11.png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1176532/1725899615Removedor%20de%20callos%20de%20pies%20el%C3%A9ctrico%208.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1635913/1737489352Screenshot_9.png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1176555/1761839437Removedor%20de%20callos%20de%20pies%20el%C3%A9ctrico%2015.jpg'],
   price:49000,oldPrice:89000,
   desc:'Elimina callos, piel dura y talones agrietados de forma rápida y segura. Diseño ergonómico con mango cómodo. Cuerpo portátil giratorio 360° con rodillos de partículas microabrasivas impermeables y fáciles de reemplazar. ¡Resultados desde la primera aplicación!',
   sold:340,stars:5,lastUnits:true,timer:30*60},
  {id:'T003',name:'Armario 3 Cuerpos Tela No Tejida',cat:'hogar',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/640729/1707407078WhatsApp%20Image%202024-02-08%20at%2010.40.11%20AM.jpeg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/431969/16968755751695661087Alpi88EsRuch6KZ4F4ep1M2qUqYsW5QfL9bm9PAu.png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2151831/177886033588130.webp','https://d39ru7awumhhs2.cloudfront.net/colombia/products/697347/1774473913armarion%203.jpg'],
   price:85000,oldPrice:149000,
   desc:'Armario portátil de gran capacidad con barra para colgar ropa y 9 estantes. Construcción robusta con tela no tejida impermeable y tubos de acero de alta calidad. Ideal para organizar tu ropa, calzado y accesorios. Disponible en negro, gris, vino tinto y café.',
   sold:210,stars:4,lastUnits:false,timer:6*60*60},
  {id:'T004',name:'Zapatero Organizador 9 Niveles',cat:'hogar',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2151325/1778790428Captura%20de%20pantalla%202026-05-14%20152040.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2151325/1778790428Captura%20de%20pantalla%202026-05-14%20152147.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2139088/1777304863WhatsApp%20Image%202026-04-27%20at%2010.44.43.jpeg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1876905/17526759711723776108Screenshot_2024_0807_221349.jpg'],
   price:65000,oldPrice:110000,
   desc:'Zapatero de 9 niveles con gran capacidad de almacenamiento. Organiza hasta 27 pares de zapatos. Estructura resistente y fácil de armar. Ideal para habitaciones, entradas y closets. Ahorra espacio y mantiene tu calzado ordenado y protegido.',
   sold:175,stars:5,lastUnits:false,timer:2*60*60},
  {id:'T005',name:'Hidrolavadora 6 Chorros Potentes',cat:'hogar',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1872413/1752165098Hidrolavadora%206%20chorros%203.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1872413/1752165098Hidrolavadora%206%20chorros%2010.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1872413/1752165098Hidrolavadora%206%20chorros%209.jpg'],
   price:89900,oldPrice:160000,
   desc:'Boquilla 6 en 1 con ángulos ajustables (0°, 15°, 25°, 40°). Presión máxima 450 PSI. Caudal 135L/h. Alcance más de 4 metros de altura. Lata de espuma incluida para mayor efecto limpiador. Perfecta para carros, motos, jardín, muebles y superficies difíciles.',
   sold:95,stars:5,lastUnits:true,timer:3*60*60},
  {id:'T006',name:'Organizador de Baño Universal 3 Niveles',cat:'hogar',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1815317/1762527418%F0%9F%98%8DORGANIZA%20TU%20BA%C3%91O,%20AHORRA%20ESPACIO%20CON%20EL%20ESTANTE%20ORGANIZADOR%20DE%20BA%C3%91O.LLEVALO%20A%20UN%20SUPER%20PRECIO%20.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1127641/17248682961698332152estante%20ba%C3%B1o.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1934840/1758597600Organizador%20de%20ba%C3%B1o%204.png'],
   price:75000,oldPrice:130000,
   desc:'Estante organizador de baño con diseño elegante en blanco. 3 niveles prácticos para organizar tus productos de higiene personal. Estructura de acero resistente. Profundidad de 25cm para máximo aprovechamiento. Se adapta a cualquier estilo de decoración.',
   sold:142,stars:5,lastUnits:false,timer:45*60},
  {id:'T007',name:'Perchero 4 Niveles Con Zapatero',cat:'hogar',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/671801/1708726377percheroZapatero4Niveles.png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/233273/17019840001701984000Z%20-%20Tendedero%20-%201.jpg'],
   price:59000,oldPrice:99000,
   desc:'Rack multifuncional 4 en 1: cuelga ropa en la parte superior, organiza zapatos en la inferior y usa el nivel medio como mesa para bolsos y accesorios. Da glamour y orden a tu habitación. Diseño práctico y elegante que aprovecha cada rincón.',
   sold:198,stars:4,lastUnits:false,timer:60*60},
  {id:'T008',name:'Nebulizador Respirador Portátil',cat:'salud',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2155990/1779384719SEC%20RESPIRADOR_-2%20(1).jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2148270/17784646881764466495D_NQ_NP_2X_786151-MLU78819306019_082024-F.webp'],
   price:55000,oldPrice:95000,
   desc:'Nebulizador portátil silencioso ideal para tratamientos respiratorios en casa. Fácil de usar, perfecto para toda la familia incluyendo niños y adultos mayores. Convierte el líquido en micropartículas para una absorción efectiva. Compacto y recargable.',
   sold:67,stars:5,lastUnits:false,timer:2*60*60},
  {id:'T009',name:'Freidora de Aire 12L Extra Capacidad + Accesorios',cat:'cocina',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2152705/1778955350ChatGPT%20Image%2016%20may%202026,%2001_10_20%20p.m..png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2152705/1778955351ChatGPT%20Image%2016%20may%202026,%2001_05_39%20p.m..png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2152705/1778955351ChatGPT%20Image%2016%20may%202026,%2001_08_19%20p.m..png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2154464/1779231764AIRFRYER......jpg'],
   price:235000,oldPrice:420000,
   desc:'🍟 Freidora de aire X HOME con extra capacidad 12L. Cocina más fácil, rápido y saludable con hasta 80% menos aceite. Panel moderno e intuitivo. Cocción rápida y uniforme. Incluye accesorios. Ideal para familias. Perfecto para papas, alitas, empanadas, pizzas y mucho más.',
   sold:55,stars:5,lastUnits:true,timer:24*60*60},
  {id:'T010',name:'Fire TV Stick 4K Control de Voz',cat:'tecnologia',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1884233/1753385392Imagen%20de%20WhatsApp%202025-07-24%20a%20las%2011.15.27_97e32929.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2000277/1763589760fire%20tv%20magis..jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2000277/1767724666fire.jpg'],
   price:99000,oldPrice:179000,
   desc:'Convierte cualquier TV en un Smart TV. Control por voz Alexa. Acceso a Netflix, YouTube, Disney+, Prime Video, HBO Max y más. Resolución hasta 4K. Wi-Fi integrado. Fácil instalación en minutos. Sin mensualidad, pago único.',
   sold:280,stars:5,lastUnits:false,timer:3*60*60},
  {id:'T011',name:'Lonchera Eléctrica Portátil',cat:'hogar',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2132401/1776528877Captura%20de%20pantalla%202026-04-18%20111044.png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2150102/1778686955photo_2026-05-12_16-25-56.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2150102/1778686955photo_2026-05-12_16-25-58.jpg'],
   price:75000,oldPrice:130000,
   desc:'Calienta tu comida en cualquier lugar. Conexión USB para auto, oficina o viajes. Mantiene los alimentos calientes por horas. Libre de BPA, material de alta calidad. Fácil de limpiar. Ideal para el trabajo, viajes y quienes cuidan su alimentación.',
   sold:130,stars:5,lastUnits:false,timer:60*60},
  {id:'T012',name:'Audífonos Bluetooth con Pantalla LED',cat:'tecnologia',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1966260/1760735613WhatsApp%20Image%202025-10-17%20at%204.11.38%20PM%20(1).jpeg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1510875/173214620317298658215.jpg'],
   price:59900,oldPrice:110000,
   desc:'Audífonos inalámbricos con pantalla digital que muestra el nivel de batería. Sonido de alta calidad. Conexión Bluetooth estable. Batería de larga duración. Diseño cómodo y plegable. Compatible con todos los teléfonos Android e iPhone. Incluye cable de carga.',
   sold:215,stars:4,lastUnits:false,timer:2*60*60},
  {id:'T013',name:'Kit Buceo Snorkel Máscara',cat:'accesorios',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/683907/1709323851IMG-20240301-WA0039.jpg'],
   price:59900,oldPrice:105000,
   desc:'Equipo de snorkel completo para explorar el mundo submarino. Máscara de silicona de alta calidad con amplio campo visual. Tubo de respiración cómodo y antivaho. Ideal para playas, ríos y piscinas. Para adultos y niños. Perfecto para vacaciones.',
   sold:88,stars:4,lastUnits:false,timer:45*60},
  {id:'T014',name:'Audífonos Ambie Sound Oreja Abierta',cat:'tecnologia',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/372272/171837588557.PNG'],
   price:55000,oldPrice:98000,
   desc:'Auriculares de diseño oreja abierta: escuchas música y también tu entorno con seguridad. Bluetooth 5.2. 6 horas de reproducción + 24h con estuche de carga. Peso ultra ligero (4.2g por oreja). Impermeables IPX5. Micrófono integrado para llamadas. Ideal para deporte, trabajo y conducción.',
   sold:310,stars:5,lastUnits:false,timer:30*60},
  {id:'T015',name:'Proyector Portátil HD',cat:'tecnologia',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2028712/1766853261image%20-%202025-12-27T113356.503.png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1213390/1726624197WhatsApp%20Image%202024-09-17%20at%208.40.44%20PM.jpeg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1007720/1721785503WhatsApp%20Image%202024-07-23%20at%208.38.21%20PM.jpeg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2011451/1764368578Proyector%20Portatil%203.jpg'],
   price:165000,oldPrice:290000,
   desc:'Proyector portátil con imagen HD nítida. Pantalla hasta 120 pulgadas. Conecta tu celular, USB, HDMI. Batería recargable para uso sin cables. Perfecto para cine en casa, presentaciones o viajes. Altavoz integrado. Compacto y fácil de transportar.',
   sold:72,stars:4,lastUnits:true,timer:6*60*60},
  {id:'T016',name:'Careta y Snorkel Kit Completo de Buceo',cat:'accesorios',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1776906/1746026425WhatsApp%20Image%202025-04-29%20at%202.21.01%20PM.jpeg'],
   price:69000,oldPrice:120000,
   desc:'Kit de buceo completo con máscara panorámica de cara completa y snorkel integrado. Campo de visión 180°. Anti-vaho avanzado. Válvula de purga. Fácil de ajustar para adultos. Ideal para vacaciones, esnórquel y exploración submarina. Incluye bolsa de transporte.',
   sold:64,stars:4,lastUnits:false,timer:90*60},
  {id:'T017',name:'Compresor de Aire Digital Portátil',cat:'accesorios',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2128613/1776114630gl1.jpg'],
   price:89000,oldPrice:159000,
   desc:'Infla neumáticos de carros, motos y bicicletas. Pantalla LED que muestra la presión actual. Apagado automático al alcanzar la presión deseada. Batería recargable interna. Linterna LED integrada para uso nocturno. Compacto y fácil de llevar en el maletero.',
   sold:145,stars:5,lastUnits:false,timer:4*60*60},
  {id:'T018',name:'Afeitadora 3 en 1 Recargable',cat:'salud',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/241636/17019755901701975590Screenshot_139.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2084758/1771097372202211292725100.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2084757/17710973659488ed82-c5b6-4498-986a-9d569175b40b.webp'],
   price:55000,oldPrice:98000,
   desc:'Afeitadora multifuncional 3 en 1: rasura, recorta y perfilador de precisión. Recargable USB. Cuchillas de acero inoxidable. Cabezal lavable. Apta para uso en seco y húmedo. Ideal para barba, bigote y cuello. Para hombres que quieren verse siempre impecables.',
   sold:189,stars:4,lastUnits:false,timer:60*60},
  {id:'T019',name:'Organizador de Condimentos Giratorio x18',cat:'cocina',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1908987/1769180297Organizador%20De%20Condimentos%20Giratorio%20X18_2.png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1908987/1769180289Organizador%20De%20Condimentos%20Giratorio%20X18.png'],
   price:69000,oldPrice:120000,
   desc:'Organizador giratorio con 18 frascos incluidos. Base 360° para acceder fácilmente a todos tus condimentos. Añade elegancia y orden a tu cocina. Frascos herméticos de alta calidad. Etiquetas incluidas para identificar cada especia. Ahorra espacio y tiempo al cocinar.',
   sold:230,stars:5,lastUnits:false,timer:2*60*60},
  {id:'T020',name:'Tensiómetro Digital con Voz',cat:'salud',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2109657/17738473851771888968tensiometro%203.webp','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2130492/17763345271000000105.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2093052/17719638461720884377leman.webp'],
   price:55000,oldPrice:95000,
   desc:'Tensiómetro digital de brazo con voz en español. Mide presión arterial y pulso con alta precisión. Memoria para múltiples usuarios. Detecta irregularidades cardíacas. Pantalla grande y fácil de leer. Perfecto para adultos mayores y personas con hipertensión.',
   sold:198,stars:5,lastUnits:false,timer:3*60*60},
  {id:'T021',name:'Oxímetro Digital de Pulso',cat:'salud',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2152741/1778960041WhatsApp%20Image%202026-04-09%20at%204.57.08%20PM.jpeg'],
   price:28000,oldPrice:55000,
   desc:'Oxímetro de pulso rápido y preciso. Mide la saturación de oxígeno en sangre (SpO2) y la frecuencia cardíaca en segundos. Pantalla OLED de fácil lectura. Ideal para control en casa. Funciona con 2 pilas AAA. Compacto y liviano. Esencial para el cuidado de la salud.',
   sold:415,stars:5,lastUnits:false,timer:30*60},
  {id:'T022',name:'Estuche Huevo Juego Cubiertos 24 Pzas',cat:'cocina',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2111127/1773974903cubiertos-forma-de-huevo.png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2111127/1773974903WhatsApp%20Image%202026-03-19%20at%2019.31.35.jpeg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2111127/1773974903public.jpeg'],
   price:89900,oldPrice:160000,
   desc:'Elegante juego de cubiertos 24 piezas presentado en estuche con forma de huevo. Acero inoxidable de alta calidad, resistente y duradero. Incluye tenedores, cucharas, cuchillos y cucharitas. Perfecto como regalo o para tu mesa del diario. Presentación lujosa.',
   sold:145,stars:5,lastUnits:true,timer:60*60},
  {id:'T023',name:'Iniciador de Batería Cargador 12V Inteligente',cat:'accesorios',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2077325/1770401328cargador-bateria-para-carros-y-motos-12v-6-amp.webp'],
   price:69000,oldPrice:125000,
   desc:'¿Batería muerta? ¡Nunca más! Cargador inteligente 12V para carros y motos. Diagnostica, carga y repara baterías. Protección contra cortocircuito y sobrecarga. Pantalla indicadora de estado. Fácil conexión con pinzas tipo cocodrilo. Imprescindible para tu vehículo.',
   sold:110,stars:5,lastUnits:false,timer:4*60*60},
  {id:'T024',name:'Taladro Inalámbrico Profesional',cat:'accesorios',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2043245/176901088317676296461761583467110.jpg'],
   price:125000,oldPrice:220000,
   desc:'Taladro inalámbrico de alto rendimiento. Batería recargable de larga duración. Modos perforación y destornillador. Incluye set de brocas. Diseño ergonómico anti-fatiga. Ideal para hogar, trabajos de mantenimiento, instalación de muebles y mucho más.',
   sold:78,stars:4,lastUnits:true,timer:8*60*60},
  {id:'T025',name:'Organizador de Ollas y Tapas',cat:'cocina',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2126689/1775838291ollas%201.webp','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2126689/1775838291ollas.webp'],
   price:59000,oldPrice:99000,
   desc:'Organiza tus ollas y tapas de forma eficiente. Divisores ajustables. Estructura resistente de acero. Ahorra espacio en cajones y gabinetes. Fácil de instalar. Compatible con ollas de todos los tamaños. Mantén tu cocina limpia, ordenada y lista para cocinar.',
   sold:165,stars:5,lastUnits:false,timer:45*60},
  {id:'T026',name:'Consola Retro Portátil R36S 15000 Juegos',cat:'tecnologia',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2008339/1764092783video.png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2008339/1764092784video%20(3).png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2008339/1764092783video%20(1).png'],
   price:179000,oldPrice:320000,
   desc:'Consola portátil retro con más de 15,000 juegos preinstalados. Pantalla IPS de 3.5". Batería 3500mAh. Soporte para PS1, GBA, SNES, NES, Sega y más. Controles cómodos tipo GameBoy. Salida HDMI para jugar en TV. ¡El regalo ideal para los amantes de los videojuegos!',
   sold:92,stars:5,lastUnits:true,timer:12*60*60},
  {id:'T027',name:'Juguete Perro Robot Interactivo',cat:'juguetes',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2001384/1763739468D_Q_NP_2X_957362-MLA96425148737_102025-T.webp','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1995592/1763073811Lobo%20movimiento.JPG'],
   price:109000,oldPrice:190000,
   desc:'Adorable perro robot interactivo que camina, baila y hace trucos. Responde al tacto y voz. Múltiples modos de juego. Pilas incluidas. Seguro para niños desde 3 años. El compañero perfecto para los más pequeños. Les encantará su pelaje suave y sus movimientos reales.',
   sold:88,stars:5,lastUnits:false,timer:3*60*60},
  {id:'T028',name:'TV Stick Android HD Streaming',cat:'tecnologia',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1965814/1760720817sin%20(3).JPG','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1965814/1760720817sin%20(1).JPG'],
   price:89000,oldPrice:160000,
   desc:'Convierte tu TV en Smart TV al instante. Soporte Android con acceso a Play Store. Reproducción HD/4K. Wi-Fi integrado. Control remoto incluido. Accede a Netflix, YouTube, Prime Video y todas tus apps favoritas. Sin mensualidades. Plug & Play en minutos.',
   sold:195,stars:4,lastUnits:false,timer:2*60*60},
  {id:'T029',name:'Kit Máquina Afeitadora para Mascotas',cat:'accesorios',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1942148/17591538771992f34d9d2-electrohogarcyc-gneuklg0t7n-iest5inm75d.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1942148/17591538771992f34e3e7-electrohogarcyc-gneuklg0t7n-bteqsvyf7nu.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1942148/17591538771992f34d56e-electrohogarcyc-gneuklg0t7n-3nqhgzuzcf.jpg'],
   price:59000,oldPrice:105000,
   desc:'Kit completo para peluquería de mascotas en casa. Silencioso para no asustar a tu perro o gato. Cuchillas de acero inoxidable ajustables. Recargable USB. Incluye accesorios para diferentes longitudes de pelo. Ahorra en peluquería y cuida a tu mascota con amor.',
   sold:142,stars:5,lastUnits:false,timer:60*60},
  {id:'T030',name:'Power Bank 10.000mAh Con Cables Incluidos',cat:'tecnologia',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1971753/176125897513ee3767-e1b3-4979-b91e-60045d161bc3.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1971753/176125897598402836-63d7-47d1-b973-db94c2fe68f0.jpg'],
   price:85000,oldPrice:149000,
   desc:'Power Bank 10,000mAh con carga rápida. Entradas: Tipo C y Micro USB. Salidas: USB, Tipo C, Lightning. Compatible con iPhone, Samsung, Xiaomi y todos los celulares. Cables incluidos. Diseño compacto y elegante. Perfecto para viajes, trabajo y emergencias.',
   sold:268,stars:5,lastUnits:false,timer:4*60*60},
  {id:'T031',name:'Báscula Inteligente Bluetooth Análisis Corporal',cat:'salud',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1930136/1758208266BASCULA%20BLUETOOTH%208.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1930136/1758208266BASCULA%20BLUETOOTH%2010.jpg'],
   price:55000,oldPrice:99000,
   desc:'Báscula inteligente con análisis corporal completo: peso, grasa, músculo, agua y más. Sincronización Bluetooth con tu celular. Compatible con Apple Health y Samsung Health. Capacidad hasta 180kg. Vidrio templado resistente. Pantalla LCD clara. Multiusuario para toda la familia.',
   sold:188,stars:5,lastUnits:false,timer:3*60*60},
  {id:'T032',name:'Perchero con Cubierta Organizador',cat:'hogar',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1900120/1755196031WhatsApp%20Image%202025-08-14%20at%201.16.21%20PM.jpeg'],
   price:67000,oldPrice:119000,
   desc:'Perchero con cubierta protectora que mantiene tu ropa libre de polvo y humedad. Varios niveles de organización. Estructura robusta y estable. Ideal para dormitorios, entradas y cuartos pequeños. Fácil de armar, sin herramientas. Solución elegante para organizar tu ropa.',
   sold:99,stars:4,lastUnits:false,timer:90*60},
];

let reviews = JSON.parse(localStorage.getItem('trogui_reviews') || 'null') || [
  {name:'Valentina Torres',city:'Bogotá',stars:5,text:'Me llegó en 4 días!! El producto está 10/10, lo recomiendo mucho 😍'},
  {name:'Juan Camilo Restrepo',city:'Medellín',stars:5,text:'Pagué contra entrega y todo salió perfecto. La calidad es increíble, gracias TROGÜI!'},
  {name:'Luisa Fernanda Gómez',city:'Cali',stars:4,text:'Muy buen producto, llegó bien empacado. Lo recomiendo!'},
  {name:'Andrés Felipe Ospina',city:'Bucaramanga',stars:5,text:'Segunda vez que compro aquí y siempre quedo satisfecho. 100% confiable.'},
  {name:'Natalia Suárez',city:'Barranquilla',stars:5,text:'Excelente! El quita callos funcionó de maravilla desde el primer uso!'},
];

let cart = [];
let orders = JSON.parse(localStorage.getItem('trogui_orders') || '[]');
let currentOrderProduct = null;
let timers = {};
let sliderIdx = 0;
let visitors = Math.floor(Math.random()*38)+12;
let rouletteSpun = false;
let rouletteInactivityTimer = null;

// ========== INIT ==========
document.addEventListener('DOMContentLoaded', () => {
  loadSettings();
  renderProducts(products);
  startSlider();
  startNotifications();
  startShakeLoop();
  updateVisitors();
  startInactivityWatcher();
  drawRoulette();
});

function loadSettings(){
  const tb = localStorage.getItem('trogui_topbar');
  if(tb) document.getElementById('topbar-text').textContent = tb;
  const pt = localStorage.getItem('trogui_prod_title');
  if(pt) document.getElementById('products-title').innerHTML = pt;
  const au = localStorage.getItem('trogui_audio');
  if(au){ document.getElementById('bg-audio-src').src=au; document.getElementById('bg-audio').load(); document.getElementById('bg-audio').play().catch(()=>{}); }
}

// ========== SLIDER ==========
function moveSlider(d){ sliderIdx=(sliderIdx+d+3)%3; updateSlider(); }
function goSlide(i){ sliderIdx=i; updateSlider(); }
function updateSlider(){
  document.getElementById('slider-track').style.transform=`translateX(-${sliderIdx*100}%)`;
  document.querySelectorAll('.dot').forEach((d,i)=>d.classList.toggle('active',i===sliderIdx));
}
function startSlider(){ setInterval(()=>moveSlider(1), 6000); }

// ========== FORMAT ==========
function fmt(n){ return Number(n).toLocaleString('es-CO'); }

// ========== PRODUCTS ==========
function renderProducts(prods){
  const grid = document.getElementById('products-grid');
  grid.innerHTML = '';
  if(prods.length===0){ grid.innerHTML='<div style="grid-column:1/-1;text-align:center;padding:40px;color:var(--gray);font-size:16px">😕 No se encontraron productos</div>'; return; }
  prods.forEach(p => {
    const disc = Math.round((1-p.price/p.oldPrice)*100);
    const img = p.imgs && p.imgs[0] ? p.imgs[0] : 'https://via.placeholder.com/400x300?text=TROGUI';
    const el = document.createElement('div');
    el.className = 'product-card';
    el.id = 'card-'+p.id;
    el.innerHTML = `
      <div class="product-img-wrap" onclick="openModal('${p.id}')">
        <img src="${img}" alt="${p.name}" onerror="this.src='https://via.placeholder.com/400x300?text=TROGUI'">
        <div class="badge-off">-${disc}% OFF</div>
        <div class="badge-sold-c">✅ ${p.sold}+ vendidos</div>
        ${p.lastUnits?'<div class="badge-last">⚠️ ¡Últimas!</div>':''}
      </div>
      <div class="product-info" onclick="openModal('${p.id}')">
        <div class="product-name">${p.name}</div>
        <div class="stars">${'⭐'.repeat(p.stars)}<span>(${p.stars}.0)</span></div>
        <div class="price-wrap">
          <span class="price-old">$${fmt(p.oldPrice)}</span>
          <span class="price-new">$${fmt(p.price)}</span>
        </div>
        <div class="timer-badge" id="timer-${p.id}">⏰ Cargando...</div>
        <div class="free-ship">🚚 Envío GRATIS toda Colombia</div>
        <div class="contra-e">💵 Pago Contra Entrega disponible</div>
      </div>
      <div class="card-btns">
        <button class="btn-add" onclick="event.stopPropagation();addToCart('${p.id}')">🛒 Al Carrito</button>
        <button class="btn-pedir" id="pedir-${p.id}" onclick="event.stopPropagation();openOrderDirect('${p.id}')">🔥 ¡Pedir Ya!</button>
      </div>`;
    grid.appendChild(el);
    startTimer(p.id, p.timer);
  });
}

function filterCat(cat, el){
  document.querySelectorAll('.nav-inner a').forEach(a=>a.classList.remove('active'));
  el.classList.add('active');
  const f = cat==='all' ? products : products.filter(p=>p.cat===cat);
  renderProducts(f);
}

// ========== TIMER ==========
function startTimer(id, seconds){
  if(timers[id]) clearInterval(timers[id]);
  let rem = seconds;
  function update(){
    const el = document.getElementById('timer-'+id);
    if(!el){ clearInterval(timers[id]); return; }
    if(rem<=0){ el.innerHTML='⚡ ¡Oferta vigente!'; return; }
    const h=Math.floor(rem/3600),m=Math.floor((rem%3600)/60),s=rem%60;
    const label=h>0?`${h}h ${m}m ${s}s`:m>0?`${m}m ${s}s`:`${s}s`;
    el.innerHTML=`⏰ Acaba en: <b>${label}</b>`;
    rem--;
  }
  update();
  timers[id]=setInterval(update,1000);
}

// ========== SHAKE ==========
function startShakeLoop(){
  setInterval(()=>{
    const btns=document.querySelectorAll('.btn-pedir');
    if(!btns.length) return;
    const btn=btns[Math.floor(Math.random()*btns.length)];
    btn.classList.remove('shaking');
    void btn.offsetWidth;
    btn.classList.add('shaking');
    setTimeout(()=>btn.classList.remove('shaking'),700);
  },2800);
}

// ========== MODAL ==========
function openModal(id){
  const p = products.find(x=>x.id===id);
  if(!p) return;
  const disc = Math.round((1-p.price/p.oldPrice)*100);
  const imgs = p.imgs && p.imgs.length ? p.imgs : ['https://via.placeholder.com/400x300?text=TROGUI'];
  const galleryHtml = imgs.map((src,i)=>`<img src="${src}" alt="${p.name}" class="modal-media-item${i===0?' active-img':''}" onerror="this.src='https://via.placeholder.com/400x300?text=TROGUI'" onclick="setActiveImg(this)">`).join('');
  const revHtml = reviews.map(r=>`
    <div class="review-item">
      <div class="review-top">
        <div class="review-avatar">${r.name[0]}</div>
        <div><div class="review-name">${r.name} — ${r.city}</div><div class="review-stars">${'⭐'.repeat(r.stars)}</div></div>
      </div>
      <div class="review-text">${r.text}</div>
    </div>`).join('');
  document.getElementById('modal-content').innerHTML=`
    <div class="modal-gallery">${galleryHtml}</div>
    <span style="font-size:11px;color:var(--gray)">ID: ${p.id}</span>
    <div class="modal-title">${p.name}</div>
    <div class="stars">${'⭐'.repeat(p.stars)}<span style="color:var(--gray);font-size:13px">${p.stars}.0 (${p.sold}+ vendidos)</span></div>
    <div class="modal-price-wrap">
      <span class="modal-price-old">$${fmt(p.oldPrice)}</span>
      <span class="modal-price-new">$${fmt(p.price)}</span>
      <span style="background:#ffe0cc;color:var(--orange);font-weight:900;padding:5px 12px;border-radius:20px;font-size:13px">-${disc}% OFF</span>
    </div>
    <div class="modal-delivery">
      🚚 <strong>Envío GRATIS</strong> a toda Colombia · Entrega <strong>3 a 7 días hábiles</strong><br>
      💵 <strong>Pago Contra Entrega</strong> · Interrapidísimo · Coordinadora · Envia
    </div>
    <div class="modal-desc">${p.desc}</div>
    ${p.lastUnits?'<div style="background:#fff0f0;border:1px solid var(--red);border-radius:11px;padding:11px;font-size:13px;font-weight:800;color:var(--red);margin-bottom:10px">⚠️ ¡ÚLTIMAS UNIDADES! Stock muy limitado</div>':''}
    <button class="btn-order" onclick="openOrderForm('${p.id}')">🔥 ¡Pedir Ahora — Pago Contra Entrega!</button>
    <h3 style="margin:22px 0 12px;font-family:'Poppins',sans-serif;font-size:17px">⭐ Reseñas de Clientes</h3>
    <div class="review-list">${revHtml}</div>`;
  document.getElementById('product-modal').classList.add('active');
}
function setActiveImg(img){
  document.querySelectorAll('.modal-gallery img').forEach(i=>i.classList.remove('active-img'));
  img.classList.add('active-img');
}
function closeModal(){ document.getElementById('product-modal').classList.remove('active'); }

// ========== ORDER FORM ==========
function openOrderForm(id){
  const p=products.find(x=>x.id===id);
  if(!p) return;
  currentOrderProduct=p;
  closeModal();
  _showOrderForm(p);
}
function openOrderDirect(id){
  const p=products.find(x=>x.id===id);
  if(!p) return;
  currentOrderProduct=p;
  _showOrderForm(p);
}
function _showOrderForm(p){
  document.getElementById('form-prod-name').textContent=p.name+' (ID: '+p.id+')';
  document.getElementById('form-price-show').innerHTML=`
    <div><div style="font-size:13px;color:var(--gray);font-weight:700">Precio anterior:</div><div class="fold">$${fmt(p.oldPrice)}</div></div>
    <div style="text-align:right"><div style="font-size:13px;color:var(--gray);font-weight:700">Pagas al recibir:</div><div class="fprice">$${fmt(p.price)}</div></div>`;
  document.getElementById('order-overlay').classList.add('active');
}
function closeOrderForm(){ document.getElementById('order-overlay').classList.remove('active'); }

function confirmOrder(){
  const nombre=document.getElementById('f-nombre').value.trim();
  const apellido=document.getElementById('f-apellido').value.trim();
  const depto=document.getElementById('f-departamento').value.trim();
  const ciudad=document.getElementById('f-ciudad').value.trim();
  const direccion=document.getElementById('f-direccion').value.trim();
  const telefono=document.getElementById('f-telefono').value.trim();
  const nota=document.getElementById('f-nota').value.trim();
  if(!nombre||!apellido||!depto||!ciudad||!direccion||!telefono){
    alert('⚠️ Por favor completa todos los campos obligatorios.');return;
  }
  const p=currentOrderProduct;
  const disc=Math.round((1-p.price/p.oldPrice)*100);
  const order={id:'ORD'+Date.now(),product:p.name,productId:p.id,price:p.price,oldPrice:p.oldPrice,discount:disc,nombre,apellido,departamento:depto,ciudad,direccion,telefono,nota,fecha:new Date().toLocaleString('es-CO'),fechaISO:new Date().toISOString()};
  orders.push(order);
  localStorage.setItem('trogui_orders',JSON.stringify(orders));
  const msg=encodeURIComponent(
    `🛍️ *NUEVO PEDIDO - TROGÜI*\n\n📦 *Producto:* ${p.name}\n🆔 *ID:* ${p.id}\n💰 *Precio:* $${fmt(p.price)} (-${disc}%)\n\n👤 *Cliente:* ${nombre} ${apellido}\n🗺️ *Departamento:* ${depto}\n🏙️ *Ciudad:* ${ciudad}\n🏠 *Dirección:* ${direccion}\n📞 *Teléfono:* ${telefono}\n📝 *Nota:* ${nota||'Sin nota'}\n\n✅ Pago contra entrega`
  );
  closeOrderForm();
  window.open(`https://wa.me/573206572598?text=${msg}`,'_blank');
}

// ========== CART ==========
function addToCart(id){
  const p=products.find(x=>x.id===id);
  if(!p) return;
  const ex=cart.find(x=>x.id===id);
  if(ex) ex.qty++;
  else cart.push({...p,qty:1});
  updateCartUI();
  showFloatMsg('✅ '+p.name.substring(0,28)+'... al carrito');
}
function removeFromCart(id){ cart=cart.filter(x=>x.id!==id); updateCartUI(); }
function changeQty(id,delta){
  const item=cart.find(x=>x.id===id);
  if(!item) return;
  item.qty=Math.max(1,item.qty+delta);
  updateCartUI();
}
function updateCartUI(){
  const count=cart.reduce((a,b)=>a+b.qty,0);
  document.getElementById('cart-count').textContent=count;
  const list=document.getElementById('cart-items-list');
  if(!cart.length){
    list.innerHTML='<div class="empty-cart">🛒<br>Tu carrito está vacío<br><small style="font-size:13px;color:#aaa">Agrega productos para comenzar</small></div>';
    document.getElementById('cart-total').textContent='';
    document.getElementById('btn-checkout').style.display='none';
    return;
  }
  list.innerHTML=cart.map(item=>`
    <div class="cart-item">
      <img src="${item.imgs&&item.imgs[0]||''}" alt="${item.name}" onerror="this.src='https://via.placeholder.com/72?text=T'">
      <div class="cart-item-info">
        <div class="cart-item-name">${item.name}</div>
        <div class="cart-item-price">$${fmt(item.price)}</div>
        <div class="cart-qty">
          <button class="qty-btn" onclick="changeQty('${item.id}',-1)">−</button>
          <span class="qty-val">${item.qty}</span>
          <button class="qty-btn" onclick="changeQty('${item.id}',1)">+</button>
        </div>
      </div>
      <button class="cart-remove" onclick="removeFromCart('${item.id}')">✕</button>
    </div>`).join('');
  const total=cart.reduce((a,b)=>a+b.price*b.qty,0);
  document.getElementById('cart-total').innerHTML=`Total: <span>$${fmt(total)}</span>`;
  document.getElementById('btn-checkout').style.display='block';
}
function toggleCart(){ document.getElementById('cart-drawer').classList.toggle('open'); }
function checkoutCart(){
  if(!cart.length) return;
  const lines=cart.map(i=>`• ${i.name} x${i.qty} = $${fmt(i.price*i.qty)}`).join('\n');
  const total=cart.reduce((a,b)=>a+b.price*b.qty,0);
  const msg=encodeURIComponent(`🛍️ *PEDIDO CARRITO - TROGÜI*\n\n${lines}\n\n💰 *Total: $${fmt(total)}*\n\nDeseo pagar contra entrega 🙏`);
  window.open(`https://wa.me/573206572598?text=${msg}`,'_blank');
}

// ========== SEARCH ==========
function levenshtein(a,b){
  const m=a.length,n=b.length;
  if(m===0) return n;
  if(n===0) return m;
  const dp=[];
  for(let i=0;i<=m;i++){dp[i]=[i];for(let j=1;j<=n;j++) dp[i][j]=0;}
  for(let j=0;j<=n;j++) dp[0][j]=j;
  for(let i=1;i<=m;i++) for(let j=1;j<=n;j++){
    if(a[i-1]===b[j-1]) dp[i][j]=dp[i-1][j-1];
    else dp[i][j]=1+Math.min(dp[i-1][j],dp[i][j-1],dp[i-1][j-1]);
  }
  return dp[m][n];
}
function searchProducts(q){
  const dd=document.getElementById('search-dropdown');
  if(!q||q.length<2){ dd.classList.remove('open'); renderProducts(products); return; }
  const ql=q.toLowerCase().replace(/[áàä]/g,'a').replace(/[éèë]/g,'e').replace(/[íìï]/g,'i').replace(/[óòö]/g,'o').replace(/[úùü]/g,'u');
  const scored=products.map(p=>{
    const nl=p.name.toLowerCase().replace(/[áàä]/g,'a').replace(/[éèë]/g,'e').replace(/[íìï]/g,'i').replace(/[óòö]/g,'o').replace(/[úùü]/g,'u');
    const dl=p.desc.toLowerCase().replace(/[áàä]/g,'a').replace(/[éèë]/g,'e').replace(/[íìï]/g,'i').replace(/[óòö]/g,'o').replace(/[úùü]/g,'u');
    const exact=nl.includes(ql)||dl.includes(ql)?0:1;
    const words=nl.split(' ');
    const lev=Math.min(...words.map(w=>levenshtein(ql,w)));
    return{p,score:exact*8+lev};
  }).filter(x=>x.score<7).sort((a,b)=>a.score-b.score).slice(0,8);
  if(!scored.length){
    dd.innerHTML='<div style="padding:14px 16px;color:var(--gray);font-size:14px">😕 No encontramos ese producto</div>';
    dd.classList.add('open');
    renderProducts([]);
    return;
  }
  dd.innerHTML=scored.map(({p})=>`
    <div class="search-dd-item" onclick="openModal('${p.id}');document.getElementById('search-dropdown').classList.remove('open')">
      <img src="${p.imgs&&p.imgs[0]||''}" alt="${p.name}" onerror="this.src='https://via.placeholder.com/40?text=T'">
      <div><div class="sdi-name">${p.name}</div><div class="sdi-price">$${fmt(p.price)}</div></div>
    </div>`).join('');
  dd.classList.add('open');
  renderProducts(scored.map(x=>x.p));
}
function doSearch(){ searchProducts(document.getElementById('search-input').value); }
document.addEventListener('click',e=>{ if(!e.target.closest('.search-bar')) document.getElementById('search-dropdown').classList.remove('open'); });

// ========== DELIVERY ==========
function calcDelivery(){
  const sel=document.getElementById('delivery-city');
  const days=parseInt(sel.value)||0;
  if(!days){ alert('Selecciona una ciudad'); return; }
  const date=new Date();
  date.setDate(date.getDate()+days);
  const dateStr=date.toLocaleDateString('es-CO',{weekday:'long',year:'numeric',month:'long',day:'numeric'});
  const el=document.getElementById('delivery-result');
  el.style.display='block';
  el.innerHTML=`📦 Tu pedido llegaría aproximadamente el <strong>${dateStr}</strong> (entre ${days} y ${days+2} días hábiles).`;
}

// ========== NOTIFICATIONS ==========
const notifPeople=[
  {name:'Ana María Roa',city:'Bogotá'},{name:'Camilo Vargas',city:'Medellín'},
  {name:'Sofía López',city:'Cali'},{name:'Jorge Herrera',city:'Barranquilla'},
  {name:'Daniela Ruiz',city:'Bucaramanga'},{name:'Mauricio Torres',city:'Pereira'},
  {name:'Valentina Soto',city:'Cartagena'},{name:'Felipe Molina',city:'Manizales'},
  {name:'Gloria Jiménez',city:'Ibagué'},{name:'Ernesto Díaz',city:'Santa Marta'},
];
let notifIdx=0;
function startNotifications(){
  setInterval(()=>{
    const {name,city}=notifPeople[notifIdx%notifPeople.length];
    const p=products[Math.floor(Math.random()*products.length)];
    showNotif(`🛍️ <span class="nn">${name}</span> de ${city} acaba de pedir <b>${p.name.substring(0,30)}</b>`);
    notifIdx++;
  },9000);
}
function showNotif(html){
  const nb=document.getElementById('notif-box');
  nb.innerHTML=html; nb.style.display='block';
  setTimeout(()=>nb.style.display='none',5000);
}
function showFloatMsg(msg){
  const existing=document.querySelector('.float-msg');
  if(existing) existing.remove();
  const div=document.createElement('div');
  div.className='float-msg'; div.textContent=msg;
  document.body.appendChild(div);
  setTimeout(()=>div.remove(),2800);
}
function updateVisitors(){
  setInterval(()=>{
    visitors=Math.max(8,visitors+Math.floor(Math.random()*7)-3);
    document.querySelectorAll('#v1,#v2').forEach(el=>el.textContent=visitors);
  },5000);
  document.querySelectorAll('#v1,#v2').forEach(el=>el.textContent=visitors);
}

// ========== ROULETTE ==========
const rouletteSegments=[
  {label:'🚚 Envío GRATIS',color:'#FF5200',prize:'¡Envío GRATIS en tu pedido!',win:true},
  {label:'5% Descuento',color:'#00b050',prize:'¡5% de descuento adicional en tu pedido!',win:true},
  {label:'💵 Contra Entrega',color:'#1a1a2e',prize:'¡Tienes Pago Contra Entrega disponible!',win:true},
  {label:'🎁 Regalo Sorpresa',color:'#e94560',prize:'¡Recibirás un pequeño regalo con tu pedido!',win:true},
  {label:'😅 Mejor Suerte',color:'#888',prize:'¡No ganaste esta vez! Pero tenemos envío gratis de todos modos 😊',win:false},
  {label:'10% Extra OFF',color:'#FF5200',prize:'¡10% de descuento adicional! Cuéntale al vendedor.',win:true},
  {label:'😅 Casi!',color:'#aaa',prize:'¡Casi! Pero igual tienes precios increíbles 🎉',win:false},
  {label:'🌟 Cliente VIP',color:'#f5c518',prize:'¡Eres Cliente VIP! Prioridad en atención.',win:true},
];
let rouletteAngle=0;
let rouletteSpinning=false;

function drawRoulette(angle=0){
  const canvas=document.getElementById('roulette-canvas');
  if(!canvas) return;
  const ctx=canvas.getContext('2d');
  const cx=140,cy=140,radius=135;
  const n=rouletteSegments.length;
  const arc=2*Math.PI/n;
  ctx.clearRect(0,0,280,280);
  rouletteSegments.forEach((seg,i)=>{
    const start=angle+i*arc-Math.PI/2;
    const end=start+arc;
    ctx.beginPath();
    ctx.moveTo(cx,cy);
    ctx.arc(cx,cy,radius,start,end);
    ctx.closePath();
    ctx.fillStyle=seg.color;
    ctx.fill();
    ctx.strokeStyle='rgba(255,255,255,.3)';
    ctx.lineWidth=2;
    ctx.stroke();
    ctx.save();
    ctx.translate(cx,cy);
    ctx.rotate(start+arc/2);
    ctx.textAlign='right';
    ctx.fillStyle='#fff';
    ctx.font='bold 11px Nunito,sans-serif';
    ctx.fillText(seg.label,radius-8,4);
    ctx.restore();
  });
  // Center circle
  ctx.beginPath();
  ctx.arc(cx,cy,22,0,2*Math.PI);
  ctx.fillStyle='#fff';
  ctx.fill();
  ctx.fillStyle='#FF5200';
  ctx.font='bold 13px Nunito,sans-serif';
  ctx.textAlign='center';
  ctx.fillText('TROGÜI',cx,cy+4);
}

function spinRoulette(){
  if(rouletteSpinning) return;
  rouletteSpinning=true;
  document.getElementById('roulette-btn').disabled=true;
  document.getElementById('roulette-result').style.display='none';
  // Bias: win 80% of time
  const winSegs=rouletteSegments.map((s,i)=>({...s,i})).filter(s=>s.win);
  const loseSegs=rouletteSegments.map((s,i)=>({...s,i})).filter(s=>!s.win);
  const chosen=Math.random()<0.8 ? winSegs[Math.floor(Math.random()*winSegs.length)] : loseSegs[Math.floor(Math.random()*loseSegs.length)];
  const n=rouletteSegments.length;
  const arc=2*Math.PI/n;
  const targetIdx=chosen.i;
  const totalSpins=5+Math.random()*3;
  const totalAngle=totalSpins*2*Math.PI - targetIdx*arc - arc/2 + Math.random()*arc*0.6;
  const duration=5000;
  let start=null;
  const baseAngle=rouletteAngle;
  function animate(ts){
    if(!start) start=ts;
    const elapsed=ts-start;
    const progress=Math.min(elapsed/duration,1);
    const ease=1-Math.pow(1-progress,4);
    rouletteAngle=baseAngle+totalAngle*ease;
    drawRoulette(rouletteAngle);
    if(progress<1){ requestAnimationFrame(animate); }
    else {
      rouletteSpinning=false;
      const res=document.getElementById('roulette-result');
      res.style.display='block';
      res.innerHTML=chosen.win
        ? `🎉 <b>¡Felicidades!</b><br>${chosen.prize}<br><small style="color:var(--gray)">Muestra esta pantalla al hacer tu pedido.</small>`
        : `😅 <b>¡Suerte la próxima!</b><br>${chosen.prize}`;
      res.style.color=chosen.win?'var(--orange)':'var(--gray)';
    }
  }
  requestAnimationFrame(animate);
}

function openRoulette(){ document.getElementById('roulette-overlay').classList.add('active'); }
function closeRoulette(){ document.getElementById('roulette-overlay').classList.remove('active'); }

// Inactivity watcher (1 min)
function startInactivityWatcher(){
  let lastActivity=Date.now();
  const events=['mousemove','keydown','scroll','click','touchstart'];
  events.forEach(e=>document.addEventListener(e,()=>{ lastActivity=Date.now(); }));
  setInterval(()=>{
    if(Date.now()-lastActivity > 60000 && !rouletteSpun){
      rouletteSpun=true;
      openRoulette();
    }
  },5000);
}

// ========== ADMIN AUTH ==========
function adminAuth(panel){
  const pass=prompt('🔐 Contraseña de administrador:');
  if(pass!==ADMIN_PASS){ alert('❌ Contraseña incorrecta'); return; }
  if(panel==='r') openAdminR();
  else if(panel==='c') openAdminC();
  else openAdminE();
}
function closeAdmin(id){ document.getElementById(id).classList.remove('active'); }

// ========== ADMIN R: PRODUCTS ==========
function openAdminR(){ renderAdminProducts(); document.getElementById('admin-r').classList.add('active'); }

function renderAdminProducts(){
  const list=document.getElementById('admin-product-list');
  list.innerHTML='';
  products.forEach(p=>{
    const div=document.createElement('div');
    div.className='admin-product-item';
    div.id='aitem-'+p.id;
    const imgsJson=JSON.stringify(p.imgs||[]).replace(/"/g,'&quot;');
    div.innerHTML=`
      <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:8px">
        <b style="color:var(--orange);font-size:13px">${p.id} — ${p.name}</b>
        <button class="btn-del-admin" onclick="deleteProduct('${p.id}')">🗑️ Eliminar</button>
      </div>
      <label>Nombre</label><input type="text" id="an-${p.id}" value="${p.name.replace(/"/g,'&quot;')}">
      <label>Descripción</label><textarea id="ad-${p.id}" rows="3">${p.desc}</textarea>
      <div class="admin-row2">
        <div><label>Precio ($)</label><input type="number" id="ap-${p.id}" value="${p.price}"></div>
        <div><label>Precio Anterior ($)</label><input type="number" id="ao-${p.id}" value="${p.oldPrice}"></div>
      </div>
      <div class="admin-row2">
        <div><label>Vendidos</label><input type="number" id="av-${p.id}" value="${p.sold}"></div>
        <div><label>Estrellas (1-5)</label><input type="number" id="as-${p.id}" value="${p.stars}" min="1" max="5"></div>
      </div>
      <label>Categoría</label>
      <select id="ac-${p.id}">
        ${['hogar','tecnologia','salud','belleza','fitness','accesorios','juguetes','cocina'].map(c=>`<option value="${c}"${p.cat===c?' selected':''}>${c}</option>`).join('')}
      </select>
      <label>URLs de Imágenes/GIFs (una por línea)</label>
      <textarea id="ai-${p.id}" rows="4" placeholder="https://imagen1.jpg&#10;https://imagen2.jpg&#10;https://gif.gif">${(p.imgs||[]).join('\n')}</textarea>
      <div style="display:flex;gap:8px;flex-wrap:wrap;margin-top:8px" id="preview-${p.id}">
        ${(p.imgs||[]).map(src=>`<img src="${src}" class="img-preview" onerror="this.style.display='none'">`).join('')}
      </div>
      <div class="admin-row2" style="margin-top:8px">
        <div><label>Últimas unidades</label><select id="alu-${p.id}"><option value="false"${!p.lastUnits?' selected':''}>No</option><option value="true"${p.lastUnits?' selected':''}>Sí</option></select></div>
        <div><label>Timer (segundos)</label><input type="number" id="at-${p.id}" value="${p.timer}"></div>
      </div>
      <button class="btn-save-admin" style="width:100%;margin-top:12px;font-size:14px" onclick="saveOneProduct('${p.id}')">💾 Guardar este producto</button>`;
    list.appendChild(div);
    // live preview update
    const ta=div.querySelector(`#ai-${p.id}`);
    const prev=div.querySelector(`#preview-${p.id}`);
    ta.addEventListener('input',()=>{
      const urls=ta.value.split('\n').map(u=>u.trim()).filter(Boolean);
      prev.innerHTML=urls.map(src=>`<img src="${src}" class="img-preview" onerror="this.style.display='none'">`).join('');
    });
  });
}

function saveOneProduct(id){
  const p=products.find(x=>x.id===id);
  if(!p) return;
  p.name=document.getElementById('an-'+id).value||p.name;
  p.desc=document.getElementById('ad-'+id).value;
  p.price=parseInt(document.getElementById('ap-'+id).value)||p.price;
  p.oldPrice=parseInt(document.getElementById('ao-'+id).value)||p.oldPrice;
  p.sold=parseInt(document.getElementById('av-'+id).value)||p.sold;
  p.stars=parseInt(document.getElementById('as-'+id).value)||p.stars;
  p.cat=document.getElementById('ac-'+id).value;
  const imgsRaw=document.getElementById('ai-'+id).value.split('\n').map(u=>u.trim()).filter(Boolean);
  if(imgsRaw.length) p.imgs=imgsRaw;
  p.lastUnits=document.getElementById('alu-'+id).value==='true';
  p.timer=parseInt(document.getElementById('at-'+id).value)||p.timer;
  localStorage.setItem('trogui_v2_products',JSON.stringify(products));
  renderProducts(products);
  showFloatMsg('✅ "'+p.name.substring(0,24)+'" guardado!');
}

function saveAllProducts(){
  products.forEach(p=>saveOneProduct(p.id));
  showFloatMsg('✅ Todos los productos guardados!');
}

function addNewProduct(){
  const newId='T'+String(Date.now()).slice(-4);
  products.push({id:newId,name:'Nuevo Producto',cat:'hogar',imgs:['https://via.placeholder.com/400x300?text=TROGUI'],price:49000,oldPrice:89000,desc:'Descripción del producto.',sold:10,stars:5,lastUnits:false,timer:3600});
  localStorage.setItem('trogui_v2_products',JSON.stringify(products));
  renderAdminProducts();
  renderProducts(products);
  setTimeout(()=>document.getElementById('admin-product-list').lastElementChild?.scrollIntoView({behavior:'smooth'}),150);
}

function deleteProduct(id){
  if(!confirm('¿Eliminar este producto?')) return;
  products=products.filter(p=>p.id!==id);
  localStorage.setItem('trogui_v2_products',JSON.stringify(products));
  renderAdminProducts();
  renderProducts(products);
}

// ========== ADMIN C: ORDERS ==========
let filteredOrders=[];
function openAdminC(){
  filteredOrders=[...orders].reverse();
  renderOrderStats();
  renderOrdersList(filteredOrders);
  document.getElementById('order-search').value='';
  document.getElementById('admin-c').classList.add('active');
}
function renderOrderStats(){
  const total=orders.length;
  const totalRev=orders.reduce((s,o)=>s+(o.price||0),0);
  const today=new Date().toLocaleDateString('es-CO');
  const todayCount=orders.filter(o=>o.fecha&&o.fecha.startsWith(today)).length;
  const ciudades=[...new Set(orders.map(o=>o.ciudad).filter(Boolean))].length;
  document.getElementById('orders-stats').innerHTML=`
    <div class="stat-card"><div class="sv">${total}</div><div class="sl">Total Pedidos</div></div>
    <div class="stat-card"><div class="sv">$${fmt(totalRev)}</div><div class="sl">Ingresos</div></div>
    <div class="stat-card"><div class="sv">${todayCount}</div><div class="sl">Pedidos Hoy</div></div>
    <div class="stat-card"><div class="sv">${ciudades}</div><div class="sl">Ciudades</div></div>`;
}
function renderOrdersList(list){
  const cont=document.getElementById('admin-orders-list');
  if(!list.length){ cont.innerHTML='<div class="no-orders">📭 No hay pedidos aún</div>'; return; }
  cont.innerHTML=list.map(o=>{
    const waMsg=encodeURIComponent(`Hola ${o.nombre}, tu pedido de *${o.product}* por $${fmt(o.price)} está confirmado. ¡Gracias por comprar en TROGÜI! 🛍️`);
    return `<div class="order-card">
      <div class="order-product-name">${o.product}</div>
      <div style="font-size:11px;color:var(--gray);margin-bottom:8px">#${o.id} · ${o.fecha}</div>
      <div class="order-grid">
        <div class="order-field"><span class="of-label">👤 Nombre</span><span class="of-value">${o.nombre} ${o.apellido||''}</span></div>
        <div class="order-field"><span class="of-label">📞 Teléfono</span><span class="of-value">${o.telefono}</span></div>
        <div class="order-field"><span class="of-label">🗺️ Departamento</span><span class="of-value">${o.departamento||'—'}</span></div>
        <div class="order-field"><span class="of-label">🏙️ Ciudad</span><span class="of-value">${o.ciudad}</span></div>
        <div class="order-field" style="grid-column:1/-1"><span class="of-label">🏠 Dirección</span><span class="of-value">${o.direccion}</span></div>
      </div>
      <div class="order-price-row">
        <div><div class="order-price-new">$${fmt(o.price)}</div><div class="order-price-old">Antes $${fmt(o.oldPrice)}</div></div>
        <button class="order-wa-btn" onclick="window.open('https://wa.me/57${(o.telefono||'').replace(/\D/g,'')}?text=${waMsg}','_blank')">💬 Contactar</button>
      </div>
      ${o.nota?`<div class="order-nota">📝 ${o.nota}</div>`:''}
    </div>`;
  }).join('');
}
function filterOrders(q){
  if(!q){ filteredOrders=[...orders].reverse(); renderOrdersList(filteredOrders); return; }
  const ql=q.toLowerCase();
  filteredOrders=[...orders].reverse().filter(o=>
    (o.nombre||'').toLowerCase().includes(ql)||(o.apellido||'').toLowerCase().includes(ql)||
    (o.ciudad||'').toLowerCase().includes(ql)||(o.product||'').toLowerCase().includes(ql)||
    (o.telefono||'').includes(q)||(o.id||'').toLowerCase().includes(ql)
  );
  renderOrdersList(filteredOrders);
}
function exportCSV(){
  if(!orders.length){ alert('No hay pedidos para exportar.'); return; }
  const h=['ID','Producto','Precio','Descuento%','Nombre','Apellido','Departamento','Ciudad','Dirección','Teléfono','Nota','Fecha'];
  const rows=orders.map(o=>[o.id,o.product,o.price,o.discount||'',o.nombre,o.apellido||'',o.departamento||'',o.ciudad,o.direccion,o.telefono,o.nota||'',o.fecha].map(v=>`"${String(v||'').replace(/"/g,'""')}"`).join(','));
  const csv='\uFEFF'+[h.join(','),...rows].join('\n');
  const blob=new Blob([csv],{type:'text/csv;charset=utf-8;'});
  const url=URL.createObjectURL(blob);
  const a=document.createElement('a');
  a.href=url; a.download='pedidos_trogui_'+new Date().toISOString().slice(0,10)+'.csv'; a.click();
  URL.revokeObjectURL(url);
  showFloatMsg('✅ CSV exportado!');
}
function clearOrders(){
  if(!confirm('¿Eliminar TODOS los pedidos? Esto no se puede deshacer.')) return;
  orders=[];
  localStorage.removeItem('trogui_orders');
  openAdminC();
}

// ========== ADMIN E: PAGE EDITOR ==========
function openAdminE(){
  document.getElementById('edit-topbar').value=document.getElementById('topbar-text').textContent;
  document.getElementById('edit-prod-title').value=document.getElementById('products-title').textContent;
  document.getElementById('audio-url').value=localStorage.getItem('trogui_audio')||'';
  renderAdminReviews();
  document.getElementById('admin-e').classList.add('active');
}
function saveSetting(key){
  if(key==='topbar'){
    const v=document.getElementById('edit-topbar').value;
    document.getElementById('topbar-text').textContent=v;
    localStorage.setItem('trogui_topbar',v);
  } else if(key==='prod-title'){
    const v=document.getElementById('edit-prod-title').value;
    document.getElementById('products-title').innerHTML=v;
    localStorage.setItem('trogui_prod_title',v);
  }
  showFloatMsg('✅ Guardado!');
}
function setAudio(){
  const url=document.getElementById('audio-url').value.trim();
  if(!url){ alert('Ingresa una URL de audio'); return; }
  document.getElementById('bg-audio-src').src=url;
  document.getElementById('bg-audio').load();
  document.getElementById('bg-audio').play().catch(()=>{});
  localStorage.setItem('trogui_audio',url);
  showFloatMsg('✅ Audio establecido');
}
function renderAdminReviews(){
  document.getElementById('admin-reviews-list').innerHTML=reviews.map((r,i)=>`
    <div class="admin-review-item">
      <input type="text" id="rn-${i}" value="${r.name}" placeholder="Nombre">
      <input type="text" id="rc-${i}" value="${r.city}" placeholder="Ciudad">
      <select id="rs-${i}">${[1,2,3,4,5].map(s=>`<option value="${s}"${r.stars===s?' selected':''}>${s} ⭐</option>`).join('')}</select>
      <textarea id="rt-${i}" rows="2">${r.text}</textarea>
    </div>`).join('');
}
function saveReviews(){
  reviews=reviews.map((r,i)=>({
    name:document.getElementById('rn-'+i).value||r.name,
    city:document.getElementById('rc-'+i).value||r.city,
    stars:parseInt(document.getElementById('rs-'+i).value)||r.stars,
    text:document.getElementById('rt-'+i).value||r.text,
  }));
  localStorage.setItem('trogui_reviews',JSON.stringify(reviews));
  showFloatMsg('✅ Reseñas guardadas!');
}
</script>
</body>
</html>
