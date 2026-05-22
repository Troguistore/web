<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TROGÜI - Tienda Online Colombia</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700;800;900&family=Nunito:wght@400;600;700;800&display=swap" rel="stylesheet">
<style>
:root{
  --orange:#FF5200;
  --dark:#1a1a2e;
  --white:#fff;
  --light:#f8f8f8;
  --green:#00b050;
  --red:#e00;
  --gray:#666;
  --border:#e5e5e5;
  --shadow:0 4px 20px rgba(0,0,0,.10);
}
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:'Nunito',sans-serif;background:#f4f4f4;color:var(--dark);overflow-x:hidden}
a{text-decoration:none;color:inherit}
img{max-width:100%;border-radius:8px}

.topbar{background:var(--dark);color:#fff;text-align:center;padding:7px;font-size:13px;font-weight:700;letter-spacing:.5px}
.topbar span{color:var(--orange)}

header{background:#fff;box-shadow:0 2px 12px rgba(0,0,0,.09);position:sticky;top:0;z-index:900}
.header-inner{max-width:1300px;margin:0 auto;display:flex;align-items:center;gap:16px;padding:12px 16px;flex-wrap:wrap}
.logo-area{display:flex;align-items:center;gap:8px;min-width:160px}
.logo-svg{width:130px;height:44px}
.search-bar{flex:1;min-width:180px;position:relative}
.search-bar input{width:100%;padding:10px 44px 10px 16px;border:2px solid var(--border);border-radius:30px;font-size:15px;font-family:'Nunito',sans-serif;outline:none;transition:.2s}
.search-bar input:focus{border-color:var(--orange)}
.search-bar button{position:absolute;right:8px;top:50%;transform:translateY(-50%);background:var(--orange);border:none;border-radius:50%;width:32px;height:32px;color:#fff;cursor:pointer;font-size:15px}
.header-actions{display:flex;align-items:center;gap:14px;flex-wrap:wrap}
.whatsapp-btn{display:flex;align-items:center;gap:6px;background:#25D366;color:#fff;padding:8px 14px;border-radius:20px;font-weight:700;font-size:13px;transition:.2s}
.whatsapp-btn:hover{background:#128C7E}
.cart-btn{position:relative;background:var(--orange);color:#fff;border:none;border-radius:20px;padding:8px 16px;font-weight:700;font-size:14px;cursor:pointer;display:flex;align-items:center;gap:6px}
.cart-count{background:#fff;color:var(--orange);border-radius:50%;width:20px;height:20px;font-size:12px;font-weight:900;display:flex;align-items:center;justify-content:center}
.social-links{display:flex;gap:8px}
.social-links a{width:34px;height:34px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:17px;transition:.2s}
.social-links a.ig{background:linear-gradient(45deg,#f09433,#e6683c,#dc2743,#cc2366,#bc1888)}
.social-links a.tk{background:#010101;color:#fff}
.social-links a.wa{background:#25D366;color:#fff}
.social-links a:hover{transform:scale(1.13)}

nav{background:var(--orange);padding:0 16px}
.nav-inner{max-width:1300px;margin:0 auto;display:flex;gap:4px;overflow-x:auto;padding:0}
.nav-inner a{color:#fff;padding:12px 18px;font-weight:700;font-size:14px;white-space:nowrap;border-bottom:3px solid transparent;transition:.2s}
.nav-inner a:hover,.nav-inner a.active{border-bottom-color:#fff;background:rgba(255,255,255,.12)}

.slider-section{background:#fff;padding:0}
.slider-wrap{position:relative;overflow:hidden;max-height:320px}
.slider-track{display:flex;transition:transform .6s ease}
.slide{min-width:100%;height:260px;display:flex;align-items:center;justify-content:center;position:relative;overflow:hidden}
.slide-1{background:linear-gradient(135deg,#1a1a2e 60%,#FF5200 100%)}
.slide-2{background:linear-gradient(135deg,#0f3460 60%,#e94560 100%)}
.slide-3{background:linear-gradient(135deg,#16213e 60%,#0f3460 100%)}
.slide-content{color:#fff;padding:32px;z-index:2}
.slide-content h2{font-size:clamp(22px,4vw,42px);font-weight:900;line-height:1.2;font-family:'Poppins',sans-serif}
.slide-content h2 span{color:var(--orange)}
.slide-content p{font-size:15px;margin:10px 0 18px;opacity:.9}
.slide-btn{background:var(--orange);color:#fff;padding:12px 28px;border-radius:30px;font-weight:800;font-size:15px;display:inline-block;transition:.2s}
.slide-btn:hover{background:#e04800;transform:scale(1.05)}
.slider-dots{display:flex;justify-content:center;gap:8px;padding:12px;background:#fff}
.dot{width:10px;height:10px;border-radius:50%;background:#ccc;cursor:pointer;transition:.2s}
.dot.active{background:var(--orange);width:24px;border-radius:5px}
.slider-arrow{position:absolute;top:50%;transform:translateY(-50%);background:rgba(255,255,255,.2);color:#fff;border:none;font-size:22px;width:42px;height:42px;border-radius:50%;cursor:pointer;z-index:10;transition:.2s}
.slider-arrow:hover{background:rgba(255,255,255,.4)}
.slider-arrow.prev{left:12px}
.slider-arrow.next{right:12px}

.badges-strip{background:#fff;border-bottom:2px solid var(--border)}
.badges-inner{max-width:1300px;margin:0 auto;display:flex;justify-content:center;flex-wrap:wrap;gap:0}
.badge-item{display:flex;align-items:center;gap:8px;padding:14px 24px;font-weight:700;font-size:13px;border-right:1px solid var(--border)}
.badge-item:last-child{border-right:none}

.notif{position:fixed;bottom:80px;left:16px;background:var(--dark);color:#fff;padding:10px 16px;border-radius:12px;font-size:13px;font-weight:700;z-index:1200;display:none;max-width:280px;box-shadow:0 4px 20px rgba(0,0,0,.3);animation:slideUp .4s}
@keyframes slideUp{from{opacity:0;transform:translateY(20px)}to{opacity:1;transform:translateY(0)}}
.notif .notif-name{color:var(--orange)}

.section-title{text-align:center;padding:30px 16px 8px;font-size:clamp(20px,3vw,28px);font-weight:900;font-family:'Poppins',sans-serif;color:var(--dark)}
.section-title span{color:var(--orange)}
.section-sub{text-align:center;color:var(--gray);margin-bottom:20px;font-size:14px}

.products-section{max-width:1300px;margin:0 auto;padding:0 12px 40px}
.products-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(200px,1fr));gap:16px}

/* ---- PRODUCT CARD ---- */
.product-card{background:#fff;border-radius:16px;overflow:hidden;box-shadow:var(--shadow);transition:.25s;position:relative;cursor:pointer}
.product-card:hover{transform:translateY(-4px);box-shadow:0 8px 32px rgba(0,0,0,.15)}
.product-img-wrap{position:relative;background:#f8f8f8;height:200px;overflow:hidden;display:flex;align-items:center;justify-content:center}
.product-img-wrap img{height:180px;width:100%;object-fit:cover;transition:.3s}
.product-card:hover .product-img-wrap img{transform:scale(1.06)}
.badge-offer{position:absolute;top:10px;left:10px;background:var(--orange);color:#fff;font-size:11px;font-weight:800;padding:4px 10px;border-radius:20px}
.badge-sold{position:absolute;top:10px;right:10px;background:var(--dark);color:#fff;font-size:10px;font-weight:700;padding:3px 8px;border-radius:10px}
.badge-last{position:absolute;bottom:10px;left:10px;background:var(--red);color:#fff;font-size:10px;font-weight:800;padding:3px 8px;border-radius:10px;animation:pulse 1.2s infinite}
@keyframes pulse{0%,100%{opacity:1}50%{opacity:.6}}
.product-info{padding:12px}
.product-name{font-weight:800;font-size:14px;line-height:1.3;margin-bottom:6px;font-family:'Poppins',sans-serif}
.stars{color:#f5c518;font-size:14px;margin-bottom:4px}
.stars span{color:var(--gray);font-size:12px;margin-left:4px}
.price-wrap{display:flex;align-items:center;gap:8px;flex-wrap:wrap}
.price-old{color:var(--gray);font-size:13px;text-decoration:line-through}
.price-new{color:var(--orange);font-size:20px;font-weight:900}
.timer-badge{background:#fff3e0;border:1px solid var(--orange);border-radius:8px;padding:4px 8px;font-size:11px;font-weight:800;color:var(--orange);margin-top:6px;display:flex;align-items:center;gap:4px}
.free-ship{font-size:11px;color:var(--green);font-weight:800;display:flex;align-items:center;gap:3px;margin-top:4px}
.delivery-info{font-size:11px;color:var(--gray);margin-top:3px}

/* ---- BOTONES DE ACCIÓN EN CARD ---- */
.card-btns{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-top:10px}
.btn-add{background:var(--orange);color:#fff;border:none;padding:9px 6px;border-radius:10px;font-weight:800;font-size:13px;cursor:pointer;transition:.2s;font-family:'Nunito',sans-serif;width:100%}
.btn-add:hover{background:#e04800}

/* ---- BOTÓN PEDIR AHORA CON SHAKE ---- */
.btn-pedir{background:var(--dark);color:#fff;border:none;padding:9px 6px;border-radius:10px;font-weight:800;font-size:13px;cursor:pointer;font-family:'Nunito',sans-serif;width:100%;position:relative;overflow:hidden}
.btn-pedir:hover{background:#0f0f25}

@keyframes shake{
  0%{transform:translateX(0)}
  10%{transform:translateX(-5px) rotate(-1deg)}
  20%{transform:translateX(5px) rotate(1deg)}
  30%{transform:translateX(-5px) rotate(-1deg)}
  40%{transform:translateX(5px) rotate(1deg)}
  50%{transform:translateX(-4px)}
  60%{transform:translateX(4px)}
  70%{transform:translateX(-2px)}
  80%{transform:translateX(2px)}
  90%{transform:translateX(-1px)}
  100%{transform:translateX(0)}
}
.btn-pedir.shaking{animation:shake 0.6s ease-in-out}

/* ---- MODAL ---- */
.modal-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.55);z-index:1100;align-items:center;justify-content:center;padding:16px}
.modal-overlay.active{display:flex}
.modal-box{background:#fff;border-radius:20px;max-width:700px;width:100%;max-height:90vh;overflow-y:auto;position:relative;padding:0}
.modal-close{position:absolute;top:14px;right:14px;background:var(--dark);color:#fff;border:none;border-radius:50%;width:32px;height:32px;font-size:18px;cursor:pointer;z-index:10}
.modal-content{padding:24px}
.modal-imgs{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-bottom:16px}
.modal-imgs img{border-radius:10px;height:200px;object-fit:cover}
.modal-title{font-size:20px;font-weight:900;font-family:'Poppins',sans-serif;margin-bottom:8px}
.modal-price-wrap{display:flex;align-items:center;gap:12px;margin:10px 0}
.modal-price-old{font-size:16px;text-decoration:line-through;color:var(--gray)}
.modal-price-new{font-size:28px;font-weight:900;color:var(--orange)}
.modal-desc{font-size:14px;color:var(--gray);line-height:1.6;margin:10px 0}
.modal-delivery{background:#f0fff4;border:1px solid var(--green);border-radius:10px;padding:12px;margin:12px 0;font-size:13px}
.modal-delivery strong{color:var(--green)}
.btn-order{width:100%;background:var(--orange);color:#fff;border:none;padding:14px;border-radius:14px;font-weight:900;font-size:16px;cursor:pointer;margin-top:12px;font-family:'Nunito',sans-serif;transition:.2s}
.btn-order:hover{background:#e04800}

.review-list{margin-top:20px}
.review-item{border:1px solid var(--border);border-radius:12px;padding:12px;margin-bottom:10px}
.review-top{display:flex;align-items:center;gap:10px;margin-bottom:6px}
.review-avatar{width:36px;height:36px;border-radius:50%;background:var(--orange);color:#fff;display:flex;align-items:center;justify-content:center;font-weight:900;font-size:15px}
.review-name{font-weight:800;font-size:14px}
.review-stars{color:#f5c518;font-size:13px}
.review-text{font-size:13px;color:#444;line-height:1.5}

/* ---- ORDER FORM ---- */
.order-form-section{display:none;position:fixed;inset:0;background:rgba(0,0,0,.6);z-index:1200;align-items:center;justify-content:center;padding:16px}
.order-form-section.active{display:flex}
.order-form-box{background:#fff;border-radius:20px;max-width:540px;width:100%;max-height:90vh;overflow-y:auto;padding:28px;position:relative}
.form-title{font-size:20px;font-weight:900;font-family:'Poppins',sans-serif;margin-bottom:6px}
.form-prod{font-size:14px;color:var(--gray);margin-bottom:16px}
.form-price-show{background:#fff8f0;border:2px solid var(--orange);border-radius:12px;padding:12px;margin-bottom:16px;display:flex;justify-content:space-between;align-items:center}
.form-price-show .fprice{font-size:22px;font-weight:900;color:var(--orange)}
.form-price-show .fold{font-size:13px;text-decoration:line-through;color:var(--gray)}
.form-group{margin-bottom:14px}
.form-group label{font-weight:700;font-size:14px;display:block;margin-bottom:4px}
.form-group label span.req{color:var(--red)}
.form-group input,.form-group textarea,.form-group select{width:100%;padding:11px 14px;border:2px solid var(--border);border-radius:10px;font-size:14px;font-family:'Nunito',sans-serif;outline:none;transition:.2s;color:var(--dark)}
.form-group input:focus,.form-group textarea:focus{border-color:var(--orange)}
.form-group textarea{resize:vertical;min-height:70px}
.btn-confirm{width:100%;background:var(--green);color:#fff;border:none;padding:14px;border-radius:14px;font-weight:900;font-size:16px;cursor:pointer;margin-top:8px;font-family:'Nunito',sans-serif;transition:.2s}
.btn-confirm:hover{background:#009040}
.btn-cancel{width:100%;background:#eee;color:var(--dark);border:none;padding:11px;border-radius:14px;font-weight:700;font-size:14px;cursor:pointer;margin-top:8px;font-family:'Nunito',sans-serif}

/* ---- CART DRAWER ---- */
.cart-drawer{position:fixed;right:-400px;top:0;height:100vh;width:370px;background:#fff;box-shadow:-4px 0 30px rgba(0,0,0,.2);z-index:1300;transition:.35s;overflow-y:auto;padding:20px}
.cart-drawer.open{right:0}
.cart-drawer-title{font-size:20px;font-weight:900;font-family:'Poppins',sans-serif;margin-bottom:16px;display:flex;justify-content:space-between;align-items:center}
.cart-item{display:flex;gap:12px;border-bottom:1px solid var(--border);padding:12px 0}
.cart-item img{width:70px;height:70px;object-fit:cover;border-radius:8px;background:#f4f4f4}
.cart-item-info{flex:1}
.cart-item-name{font-weight:700;font-size:14px}
.cart-item-price{color:var(--orange);font-weight:900;font-size:15px}
.cart-item-remove{color:var(--red);font-size:18px;cursor:pointer;background:none;border:none}
.cart-total{font-size:18px;font-weight:900;color:var(--orange);text-align:right;margin:16px 0}
.btn-checkout{width:100%;background:var(--orange);color:#fff;border:none;padding:14px;border-radius:14px;font-weight:900;font-size:16px;cursor:pointer;font-family:'Nunito',sans-serif}
.empty-cart{text-align:center;color:var(--gray);padding:40px 0;font-size:15px}

.delivery-calc{background:#fff;max-width:500px;margin:0 auto 30px;border-radius:16px;padding:20px;box-shadow:var(--shadow)}
.delivery-calc h3{font-size:17px;font-weight:900;margin-bottom:12px;font-family:'Poppins',sans-serif}
.delivery-result{background:#f0fff4;border:1px solid var(--green);border-radius:10px;padding:12px;font-size:14px;font-weight:700;color:var(--green);margin-top:10px}

footer{background:var(--dark);color:#fff;padding:40px 16px 20px;margin-top:20px}
.footer-grid{max-width:1300px;margin:0 auto;display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:30px}
.footer-logo{font-size:28px;font-weight:900;color:var(--orange);margin-bottom:12px}
.footer-col h4{font-weight:800;margin-bottom:12px;color:var(--orange)}
.footer-col p,.footer-col li{font-size:13px;color:#bbb;line-height:1.9;list-style:none}
.footer-bottom{text-align:center;margin-top:30px;padding-top:20px;border-top:1px solid #333;font-size:12px;color:#888}

.wa-float{position:fixed;bottom:90px;right:20px;background:#25D366;color:#fff;width:54px;height:54px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:26px;box-shadow:0 4px 16px rgba(0,0,0,.3);z-index:1000;transition:.2s;text-decoration:none}
.wa-float:hover{transform:scale(1.1);background:#128C7E}

.admin-btns{position:fixed;bottom:16px;right:16px;display:flex;gap:8px;z-index:1100}
.admin-btn{width:36px;height:36px;border-radius:50%;border:none;font-weight:900;font-size:14px;cursor:pointer;opacity:.6;transition:.2s;box-shadow:0 2px 8px rgba(0,0,0,.2)}
.admin-btn:hover{opacity:1;transform:scale(1.1)}
.admin-btn.r-btn{background:var(--orange);color:#fff}
.admin-btn.c-btn{background:var(--dark);color:#fff}
.admin-btn.e-btn{background:#0f3460;color:#fff}

.admin-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.6);z-index:2000;align-items:flex-start;justify-content:center;padding:16px;overflow-y:auto}
.admin-overlay.active{display:flex}
.admin-panel{background:#fff;border-radius:20px;max-width:960px;width:100%;margin:20px auto;padding:24px;position:relative;max-height:90vh;overflow-y:auto}
.admin-panel h2{font-size:22px;font-weight:900;font-family:'Poppins',sans-serif;color:var(--orange);margin-bottom:20px}
.admin-product-list{display:grid;gap:12px}
.admin-product-item{border:2px solid var(--border);border-radius:12px;padding:16px;display:grid;gap:8px}
.admin-product-item label{font-weight:700;font-size:13px;margin-bottom:2px;display:block}
.admin-product-item input,.admin-product-item textarea{width:100%;padding:8px 12px;border:1.5px solid var(--border);border-radius:8px;font-size:13px;font-family:'Nunito',sans-serif}
.admin-product-item .row2{display:grid;grid-template-columns:1fr 1fr;gap:8px}
.btn-save-admin{background:var(--green);color:#fff;border:none;padding:10px 20px;border-radius:10px;font-weight:800;cursor:pointer;font-family:'Nunito',sans-serif;margin-top:8px}
.btn-del-admin{background:var(--red);color:#fff;border:none;padding:6px 12px;border-radius:8px;font-weight:700;cursor:pointer;font-size:12px;font-family:'Nunito',sans-serif}
.btn-add-prod{background:var(--orange);color:#fff;border:none;padding:12px 24px;border-radius:12px;font-weight:800;cursor:pointer;font-size:15px;font-family:'Nunito',sans-serif;margin-bottom:20px}

/* ---- PANEL DE PEDIDOS MEJORADO ---- */
.orders-toolbar{display:flex;gap:10px;align-items:center;flex-wrap:wrap;margin-bottom:16px;padding:14px;background:#f8f8f8;border-radius:12px}
.orders-toolbar input{flex:1;min-width:160px;padding:8px 12px;border:1.5px solid var(--border);border-radius:8px;font-size:13px;font-family:'Nunito',sans-serif;outline:none}
.orders-toolbar input:focus{border-color:var(--orange)}
.orders-stats{display:grid;grid-template-columns:repeat(auto-fit,minmax(130px,1fr));gap:10px;margin-bottom:18px}
.stat-card{background:#fff;border:1.5px solid var(--border);border-radius:12px;padding:14px;text-align:center}
.stat-card .sv{font-size:22px;font-weight:900;color:var(--orange)}
.stat-card .sl{font-size:12px;color:var(--gray);font-weight:700;margin-top:2px}
.order-card{border:2px solid var(--border);border-radius:14px;padding:16px;margin-bottom:12px;background:#fff;transition:.2s}
.order-card:hover{border-color:var(--orange);box-shadow:0 4px 16px rgba(255,82,0,.1)}
.order-card-header{display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:10px;flex-wrap:wrap;gap:8px}
.order-id{font-size:12px;color:var(--gray);font-weight:700}
.order-time-badge{background:#fff3e0;border:1px solid var(--orange);border-radius:20px;padding:3px 10px;font-size:11px;font-weight:800;color:var(--orange)}
.order-product-name{font-size:15px;font-weight:900;color:var(--dark);font-family:'Poppins',sans-serif;margin-bottom:8px}
.order-grid{display:grid;grid-template-columns:1fr 1fr;gap:6px;font-size:13px}
.order-field{display:flex;flex-direction:column;gap:2px}
.order-field .of-label{font-size:11px;font-weight:800;color:var(--gray);text-transform:uppercase;letter-spacing:.5px}
.order-field .of-value{font-weight:700;color:var(--dark)}
.order-price-row{display:flex;align-items:center;gap:10px;margin-top:10px;padding-top:10px;border-top:1px solid var(--border)}
.order-price-new{font-size:20px;font-weight:900;color:var(--orange)}
.order-price-old{font-size:13px;text-decoration:line-through;color:var(--gray)}
.order-discount-badge{background:#fff0e6;color:var(--orange);border-radius:20px;padding:3px 10px;font-size:12px;font-weight:800}
.order-wa-btn{margin-left:auto;background:#25D366;color:#fff;border:none;border-radius:10px;padding:7px 14px;font-weight:800;font-size:12px;cursor:pointer;font-family:'Nunito',sans-serif}
.order-nota{background:#fffbe6;border:1px solid #ffe082;border-radius:8px;padding:8px 12px;font-size:12px;color:#7a6000;margin-top:8px;font-weight:700}
.no-orders{text-align:center;padding:40px 20px;color:var(--gray)}
.no-orders .no-ico{font-size:48px;margin-bottom:12px}

/* ---- PAGE EDITOR ---- */
.page-editor-section{display:grid;gap:14px}
.page-editor-group{border:1px solid var(--border);border-radius:12px;padding:14px}
.page-editor-group label{font-weight:800;font-size:14px;display:block;margin-bottom:6px;color:var(--dark)}
.page-editor-group input,.page-editor-group textarea{width:100%;padding:9px 13px;border:1.5px solid var(--border);border-radius:8px;font-size:13px;font-family:'Nunito',sans-serif}
.page-editor-group textarea{min-height:60px;resize:vertical}

.visitors-badge{background:var(--dark);color:#fff;border-radius:12px;padding:10px 16px;font-size:13px;font-weight:700;margin-bottom:16px;display:flex;align-items:center;gap:8px}
.visitors-dot{width:10px;height:10px;border-radius:50%;background:var(--green);display:inline-block;animation:blink 1s infinite}
@keyframes blink{0%,100%{opacity:1}50%{opacity:.2}}

.search-dropdown{position:absolute;top:110%;left:0;right:0;background:#fff;border-radius:12px;box-shadow:0 8px 24px rgba(0,0,0,.15);z-index:500;display:none;max-height:280px;overflow-y:auto}
.search-dropdown.open{display:block}
.search-dropdown-item{padding:10px 16px;cursor:pointer;font-size:14px;border-bottom:1px solid var(--border);transition:.15px;display:flex;align-items:center;gap:10px}
.search-dropdown-item:hover{background:#fff8f0}
.search-dropdown-item img{width:36px;height:36px;object-fit:cover;border-radius:6px;background:#f4f4f4}

.admin-review-item{border:1.5px solid var(--border);border-radius:10px;padding:12px;display:grid;gap:6px;margin-bottom:10px}
.admin-review-item input,.admin-review-item textarea,.admin-review-item select{width:100%;padding:7px 10px;border:1.5px solid var(--border);border-radius:7px;font-size:13px;font-family:'Nunito',sans-serif}

#audio-autoplay{display:none}

@media(max-width:700px){
  .header-inner{flex-wrap:wrap;gap:10px}
  .products-grid{grid-template-columns:repeat(2,1fr)}
  .modal-imgs{grid-template-columns:1fr}
  .cart-drawer{width:100%;right:-110%}
  .admin-product-item .row2{grid-template-columns:1fr}
  .badges-inner{gap:0}
  .badge-item{padding:10px 12px;font-size:12px}
  .order-grid{grid-template-columns:1fr}
  .orders-stats{grid-template-columns:1fr 1fr}
  .card-btns{grid-template-columns:1fr}
}
@media(max-width:400px){
  .products-grid{grid-template-columns:1fr}
}
</style>
</head>
<body>

<audio id="audio-autoplay" autoplay loop>
  <source id="audio-src" src="" type="audio/mpeg">
</audio>

<div class="topbar">🇨🇴 Envíos a toda Colombia &nbsp;|&nbsp; <span>¡PAGO CONTRA ENTREGA!</span> &nbsp;|&nbsp; 📦 Interrapidísimo · Coordinadora · Envia</div>

<header>
  <div class="header-inner">
    <div class="logo-area">
      <svg class="logo-svg" viewBox="0 0 200 70" xmlns="http://www.w3.org/2000/svg" id="main-logo">
        <rect width="200" height="70" rx="10" fill="#FF5200"/>
        <text x="16" y="52" font-family="Poppins,sans-serif" font-weight="900" font-size="38" fill="#1a1a2e" letter-spacing="-1">TROGÜI</text>
      </svg>
    </div>
    <div class="search-bar" style="position:relative">
      <input type="text" id="search-input" placeholder="🔍  Buscar productos..." autocomplete="off" oninput="searchProducts(this.value)">
      <button onclick="searchProducts(document.getElementById('search-input').value)">🔍</button>
      <div class="search-dropdown" id="search-dropdown"></div>
    </div>
    <div class="header-actions">
      <a href="https://wa.link/lhneng" target="_blank" class="whatsapp-btn">📱 320 657 2598</a>
      <div class="social-links">
        <a href="https://www.instagram.com/store_trog?igsh=MWZleXFlY21weDhnMQ%3D%3D&utm_source=qr" target="_blank" class="ig" title="Instagram">📸</a>
        <a href="https://www.tiktok.com/@trogui_store?_r=1&_t=ZS-96QXU6BiNk2" target="_blank" class="tk" title="TikTok">🎵</a>
        <a href="https://wa.link/lhneng" target="_blank" class="wa" title="WhatsApp">💬</a>
      </div>
      <button class="cart-btn" onclick="toggleCart()">🛒 Carrito <span class="cart-count" id="cart-count">0</span></button>
    </div>
  </div>
</header>

<nav>
  <div class="nav-inner">
    <a href="#" class="active" onclick="filterCat('all',this)">🏠 Tienda</a>
    <a href="#" onclick="filterCat('belleza',this)">💄 Belleza</a>
    <a href="#" onclick="filterCat('hogar',this)">🏡 Hogar</a>
    <a href="#" onclick="filterCat('tecnologia',this)">📱 Tecnología</a>
    <a href="#" onclick="filterCat('salud',this)">💊 Salud</a>
    <a href="#" onclick="filterCat('fitness',this)">🏋️ Fitness</a>
    <a href="#" onclick="filterCat('juguetes',this)">🧸 Juguetes</a>
    <a href="#" onclick="filterCat('accesorios',this)">👜 Accesorios</a>
  </div>
</nav>

<div class="slider-section">
  <div class="slider-wrap" id="main-slider">
    <div class="slider-track" id="slider-track">
      <div class="slide slide-1">
        <div class="slide-content">
          <h2>🇨🇴 Envíos Gratis<br>a <span>Toda Colombia</span></h2>
          <p>Más de 45 productos con descuentos increíbles • Pago contra entrega</p>
          <a href="#products" class="slide-btn">¡Ver Ofertas!</a>
        </div>
      </div>
      <div class="slide slide-2">
        <div class="slide-content">
          <h2>⚡ Pago<br><span>Contra Entrega</span></h2>
          <p>Sin riesgo, sin tarjetas. Pagas cuando recibes tu pedido en casa.</p>
          <a href="#products" class="slide-btn">Ver Productos</a>
        </div>
      </div>
      <div class="slide slide-3">
        <div class="slide-content">
          <h2>📦 Recibe en<br><span>3 a 7 Días</span></h2>
          <p>Coordinadora · Interrapidísimo · Envia · Entrega a domicilio</p>
          <a href="#products" class="slide-btn">Comprar Ahora</a>
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

<div class="badges-strip">
  <div class="badges-inner">
    <div class="badge-item">✅ <b>Pago Contra Entrega</b></div>
    <div class="badge-item">🚚 <b>Envío Gratis Colombia</b></div>
    <div class="badge-item">📦 <b>3 a 7 días hábiles</b></div>
    <div class="badge-item">🔒 <b>Compra 100% Segura</b></div>
    <div class="badge-item">⭐ <b>+500 Clientes Felices</b></div>
  </div>
</div>

<div class="notif" id="notif-box"></div>

<div id="products">
  <h2 class="section-title">🔥 Productos en <span>OFERTA</span></h2>
  <p class="section-sub">Envío gratis a toda Colombia · Pago contra entrega · Solo quedan pocas unidades</p>
  <div class="products-section">
    <div class="products-grid" id="products-grid"></div>
  </div>
</div>

<div style="max-width:1300px;margin:0 auto;padding:0 12px 20px">
  <div class="delivery-calc">
    <h3>📅 ¿Cuándo llega mi pedido?</h3>
    <p style="font-size:13px;color:var(--gray);margin-bottom:10px">Ingresa tu ciudad y te decimos la fecha estimada de entrega:</p>
    <select id="delivery-city" style="width:100%;padding:10px;border:2px solid var(--border);border-radius:10px;font-size:14px;margin-bottom:8px;font-family:'Nunito',sans-serif">
      <option value="">-- Selecciona tu ciudad --</option>
      <option value="3">Bogotá</option>
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
    <button onclick="calcDelivery()" style="background:var(--orange);color:#fff;border:none;padding:10px 24px;border-radius:10px;font-weight:800;cursor:pointer;font-family:'Nunito',sans-serif">Calcular</button>
    <div class="delivery-result" id="delivery-result" style="display:none"></div>
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
<div class="order-form-section" id="order-form-section">
  <div class="order-form-box">
    <h2 class="form-title">📋 Confirmar Pedido</h2>
    <p class="form-prod" id="form-prod-name"></p>
    <div class="form-price-show" id="form-price-show"></div>
    <div class="form-group">
      <label>Nombre <span class="req">*</span></label>
      <input type="text" id="f-nombre" placeholder="Digita tu nombre completo">
    </div>
    <div class="form-group">
      <label>Apellido <span class="req">*</span></label>
      <input type="text" id="f-apellido" placeholder="Digita tu apellido">
    </div>
    <div class="form-group">
      <label>Departamento <span class="req">*</span></label>
      <select id="f-departamento">
        <option value="">-- Selecciona departamento --</option>
        <option>Amazonas</option><option>Antioquia</option><option>Arauca</option>
        <option>Atlántico</option><option>Bolívar</option><option>Boyacá</option>
        <option>Caldas</option><option>Caquetá</option><option>Casanare</option>
        <option>Cauca</option><option>Cesar</option><option>Chocó</option>
        <option>Córdoba</option><option>Cundinamarca</option><option>Guainía</option>
        <option>Guaviare</option><option>Huila</option><option>La Guajira</option>
        <option>Magdalena</option><option>Meta</option><option>Nariño</option>
        <option>Norte de Santander</option><option>Putumayo</option><option>Quindío</option>
        <option>Risaralda</option><option>San Andrés y Providencia</option>
        <option>Santander</option><option>Sucre</option><option>Tolima</option>
        <option>Valle del Cauca</option><option>Vaupés</option><option>Vichada</option>
        <option>Bogotá D.C.</option>
      </select>
    </div>
    <div class="form-group">
      <label>Ciudad o Municipio <span class="req">*</span></label>
      <input type="text" id="f-ciudad" placeholder="Ej: Bogotá, Medellín, Cali...">
    </div>
    <div class="form-group">
      <label>Dirección completa <span class="req">*</span></label>
      <input type="text" id="f-direccion" placeholder="Calle, carrera, barrio, detalle...">
    </div>
    <div class="form-group">
      <label>Teléfono <span class="req">*</span></label>
      <input type="tel" id="f-telefono" placeholder="Ej: 3001234567">
    </div>
    <div class="form-group">
      <label>Nota (opcional)</label>
      <textarea id="f-nota" placeholder="Color, talla, instrucciones especiales..."></textarea>
    </div>
    <button class="btn-confirm" onclick="confirmOrder()">✅ Confirmar Pedido por WhatsApp</button>
    <button class="btn-cancel" onclick="closeOrderForm()">Cancelar</button>
  </div>
</div>

<!-- CART DRAWER -->
<div class="cart-drawer" id="cart-drawer">
  <div class="cart-drawer-title">
    🛒 Mi Carrito
    <button onclick="toggleCart()" style="background:none;border:none;font-size:22px;cursor:pointer">✕</button>
  </div>
  <div id="cart-items-list"></div>
  <div class="cart-total" id="cart-total"></div>
  <button class="btn-checkout" onclick="checkoutCart()" id="btn-checkout" style="display:none">Pedir por WhatsApp 💬</button>
</div>

<footer>
  <div class="footer-grid">
    <div class="footer-col">
      <div class="footer-logo">TROGÜI</div>
      <p>Tienda colombiana de confianza. Enviamos a todo el país con las mejores transportadoras.</p>
      <div style="display:flex;gap:10px;margin-top:12px">
        <a href="https://wa.link/lhneng" target="_blank" style="color:#25D366;font-size:22px">💬</a>
        <a href="https://www.instagram.com/store_trog" target="_blank" style="font-size:22px">📸</a>
        <a href="https://www.tiktok.com/@trogui_store" target="_blank" style="color:#fff;font-size:22px">🎵</a>
      </div>
    </div>
    <div class="footer-col">
      <h4>Información</h4>
      <ul>
        <li>📞 Línea: 320 657 2598</li>
        <li>📧 trogui.store@gmail.com</li>
        <li>🇨🇴 Colombia - Nacional</li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>Transportadoras</h4>
      <ul>
        <li>📦 Interrapidísimo</li>
        <li>📦 Coordinadora</li>
        <li>📦 Envia</li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>Métodos de Pago</h4>
      <ul>
        <li>💵 Contra Entrega</li>
        <li>🏦 Transferencia</li>
        <li>💳 Nequi / Daviplata</li>
      </ul>
    </div>
  </div>
  <div class="footer-bottom">© 2025 TROGÜI · Tienda Colombiana de Confianza 🇨🇴</div>
</footer>

<a href="https://wa.link/lhneng" target="_blank" class="wa-float" title="WhatsApp">💬</a>

<div class="admin-btns">
  <button class="admin-btn r-btn" title="Editar Productos" onclick="adminAuth('r')">R</button>
  <button class="admin-btn c-btn" title="Ver Pedidos" onclick="adminAuth('c')">C</button>
  <button class="admin-btn e-btn" title="Editar Página" onclick="adminAuth('e')">E</button>
</div>

<!-- ADMIN PANEL R -->
<div class="admin-overlay" id="admin-r">
  <div class="admin-panel">
    <h2>✏️ Editor de Productos</h2>
    <div class="visitors-badge">
      <span class="visitors-dot"></span>
      <span id="visitors-count">0</span> personas viendo la página ahora
    </div>
    <button class="btn-add-prod" onclick="addNewProduct()">+ Agregar Nuevo Producto</button>
    <div class="admin-product-list" id="admin-product-list"></div>
    <div style="display:flex;gap:10px;margin-top:20px">
      <button class="btn-save-admin" onclick="saveProducts()">💾 Guardar Cambios</button>
      <button onclick="closeAdmin('admin-r')" style="background:#eee;border:none;padding:10px 20px;border-radius:10px;cursor:pointer;font-weight:700">Cerrar</button>
    </div>
  </div>
</div>

<!-- ADMIN PANEL C - PEDIDOS MEJORADO -->
<div class="admin-overlay" id="admin-c">
  <div class="admin-panel">
    <h2>📦 Pedidos Recibidos</h2>
    <div class="visitors-badge">
      <span class="visitors-dot"></span>
      <span id="visitors-count2">0</span> personas viendo la página ahora
    </div>
    <!-- Stats -->
    <div class="orders-stats" id="orders-stats"></div>
    <!-- Toolbar -->
    <div class="orders-toolbar">
      <input type="text" id="order-search" placeholder="🔍 Buscar por nombre, ciudad, producto..." oninput="filterOrders(this.value)">
      <button onclick="exportOrdersCSV()" style="background:var(--green);color:#fff;border:none;padding:8px 16px;border-radius:8px;font-weight:800;cursor:pointer;font-family:'Nunito',sans-serif;white-space:nowrap">📥 Exportar CSV</button>
      <button onclick="clearOrders()" style="background:var(--red);color:#fff;border:none;padding:8px 14px;border-radius:8px;font-weight:700;cursor:pointer;font-family:'Nunito',sans-serif;white-space:nowrap">🗑️ Limpiar</button>
    </div>
    <!-- Orders list -->
    <div id="admin-orders-list"></div>
    <div style="margin-top:16px">
      <button onclick="closeAdmin('admin-c')" style="background:#eee;border:none;padding:10px 20px;border-radius:10px;cursor:pointer;font-weight:700">Cerrar</button>
    </div>
  </div>
</div>

<!-- ADMIN PANEL E -->
<div class="admin-overlay" id="admin-e">
  <div class="admin-panel">
    <h2>🎨 Editor de Página</h2>
    <div class="page-editor-section">
      <div class="page-editor-group">
        <label>🔊 Audio de Bienvenida (URL MP3)</label>
        <input type="text" id="audio-url-input" placeholder="https://... .mp3">
        <button class="btn-save-admin" onclick="setAudio()" style="margin-top:8px">Establecer Audio</button>
      </div>
      <div class="page-editor-group">
        <label>🏷️ Texto del TopBar</label>
        <input type="text" id="edit-topbar" placeholder="Texto del top bar">
        <button class="btn-save-admin" onclick="savePageSetting('topbar')" style="margin-top:8px">Guardar</button>
      </div>
      <div class="page-editor-group">
        <label>📝 Título Sección Productos</label>
        <input type="text" id="edit-prod-title" placeholder="Título de sección">
        <button class="btn-save-admin" onclick="savePageSetting('prod-title')" style="margin-top:8px">Guardar</button>
      </div>
      <div class="page-editor-group">
        <label>⭐ Editar Reseñas</label>
        <div id="admin-reviews-list"></div>
        <button class="btn-save-admin" onclick="saveReviews()">💾 Guardar Reseñas</button>
      </div>
    </div>
    <div style="margin-top:20px">
      <button onclick="closeAdmin('admin-e')" style="background:#eee;border:none;padding:10px 20px;border-radius:10px;cursor:pointer;font-weight:700">Cerrar</button>
    </div>
  </div>
</div>

<script>
const ADMIN_PASS = '4325';

let products = JSON.parse(localStorage.getItem('trogui_products') || 'null') || [
  {id:'P001',name:'Quita Callos Profesional',cat:'belleza',img:'https://images.unsplash.com/photo-1556228578-8c89e6adf883?w=400',img2:'https://images.unsplash.com/photo-1607462109225-6b64ae2dd3cb?w=400',price:49000,oldPrice:89000,desc:'Elimina callos y durezas de forma rápida y segura. Resultado desde la primera aplicación. Incluye lima especial.',sold:120,stars:5,lastUnits:true,timer:30*60,cat:'belleza'},
  {id:'P002',name:'Masajeador Eléctrico Cervical',cat:'salud',img:'https://images.unsplash.com/photo-1544367567-0f2fcb009e0b?w=400',img2:'https://images.unsplash.com/photo-1585559609834-b89c95c17c72?w=400',price:79000,oldPrice:130000,desc:'Alivio inmediato del dolor de cuello y espalda. 8 modos de masaje. Calor infrarrojo. Recargable USB.',sold:300,stars:5,lastUnits:false,timer:2*60*60,cat:'salud'},
  {id:'P003',name:'Plancha de Cabello Profesional',cat:'belleza',img:'https://images.unsplash.com/photo-1522337360788-8b13dee7a37e?w=400',img2:'https://images.unsplash.com/photo-1527799820374-87ae27d38c85?w=400',price:89000,oldPrice:160000,desc:'Plancha cerámica profesional con control de temperatura. Alisado perfecto sin dañar el cabello.',sold:80,stars:4,lastUnits:true,timer:60*60,cat:'belleza'},
  {id:'P004',name:'Rodillo Facial Jade Anti-Edad',cat:'belleza',img:'https://images.unsplash.com/photo-1616394584738-fc6e612e71b9?w=400',img2:'https://images.unsplash.com/photo-1570172619644-dfd03ed5d881?w=400',price:44000,oldPrice:75000,desc:'Reduce bolsas, ojeras y arrugas. Mejora la circulación facial. Piedra de jade natural.',sold:210,stars:5,lastUnits:false,timer:45*60,cat:'belleza'},
  {id:'P005',name:'Organizador Cocina Giratorio',cat:'hogar',img:'https://images.unsplash.com/photo-1556909114-f6e7ad7d3136?w=400',img2:'https://images.unsplash.com/photo-1556909190-eccf4a8bf97a?w=400',price:54000,oldPrice:90000,desc:'Organizador 360° para especias, salsas y condimentos. Ahorra espacio. Fácil limpieza.',sold:175,stars:5,lastUnits:false,timer:24*60*60,cat:'hogar'},
  {id:'P006',name:'Lámpara LED Solar Jardín',cat:'hogar',img:'https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=400',img2:'https://images.unsplash.com/photo-1513694203232-719a280e022f?w=400',price:49000,oldPrice:85000,desc:'Pack x4 lámparas solares. Enciende automáticamente al oscurecer. Resistente al agua. Sin cables.',sold:90,stars:4,lastUnits:true,timer:3*60*60,cat:'hogar'},
  {id:'P007',name:'Banda Resistencia Fitness',cat:'fitness',img:'https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b?w=400',img2:'https://images.unsplash.com/photo-1540497077202-7c8a3999166f?w=400',price:39000,oldPrice:70000,desc:'Set de 5 bandas elásticas. Ideal para glúteos, piernas y brazos. Material premium antirasgado.',sold:400,stars:5,lastUnits:false,timer:2*60*60,cat:'fitness'},
  {id:'P008',name:'Smartwatch Deportivo',cat:'tecnologia',img:'https://images.unsplash.com/photo-1523275335684-37898b6baf30?w=400',img2:'https://images.unsplash.com/photo-1508685096489-7aacd43bd3b1?w=400',price:119000,oldPrice:199000,desc:'Monitor cardíaco, GPS, 20+ modos deporte. Batería 7 días. Compatible Android/iPhone.',sold:150,stars:5,lastUnits:true,timer:60*60,cat:'tecnologia'},
  {id:'P009',name:'Audífonos Bluetooth Inalámbricos',cat:'tecnologia',img:'https://images.unsplash.com/photo-1505740420928-5e560c06d30e?w=400',img2:'https://images.unsplash.com/photo-1484704849700-f032a568e944?w=400',price:84000,oldPrice:149000,desc:'Sonido HD. Cancelación de ruido activa. Batería 40 horas. Carga rápida 15 min.',sold:320,stars:5,lastUnits:false,timer:6*60*60,cat:'tecnologia'},
  {id:'P010',name:'Cepillo Eléctrico Ultrasónico',cat:'salud',img:'https://images.unsplash.com/photo-1559304787-1a0c9c1a2c2e?w=400',img2:'https://images.unsplash.com/photo-1607613009820-a29f7bb81c04?w=400',price:69000,oldPrice:110000,desc:'40,000 vibraciones por minuto. 3 modos de limpieza. Cabezal de repuesto incluido. Batería 30 días.',sold:88,stars:4,lastUnits:false,timer:30*60,cat:'salud'},
  {id:'P011',name:'Juego Yoga Mat Antideslizante',cat:'fitness',img:'https://images.unsplash.com/photo-1544367567-0f2fcb009e0b?w=400',img2:'https://images.unsplash.com/photo-1517963879433-6ad2b056d712?w=400',price:74000,oldPrice:120000,desc:'Mat 6mm ultra grip. Incluye bolsa de transporte y banda. 183x61cm. Ecológico TPE.',sold:60,stars:5,lastUnits:true,timer:4*60*60,cat:'fitness'},
  {id:'P012',name:'Vaporizador Facial Portátil',cat:'belleza',img:'https://images.unsplash.com/photo-1596755094514-f87e34085b2c?w=400',img2:'https://images.unsplash.com/photo-1522337913716-6a5aa24e2c3c?w=400',price:59000,oldPrice:95000,desc:'Hidratación profunda, abre poros, limpieza facial. Nano vapor frío. Uso en casa o viaje.',sold:140,stars:5,lastUnits:false,timer:2*60*60,cat:'belleza'},
  {id:'P013',name:'Organizador Cables USB',cat:'hogar',img:'https://images.unsplash.com/photo-1558618047-f4f89e5e1e7b?w=400',img2:'https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=400',price:34000,oldPrice:60000,desc:'Pack x10 organizadores de cables. Adhesivo fuerte. Ideal escritorio, televisor, consola.',sold:500,stars:5,lastUnits:false,timer:30*60,cat:'hogar'},
  {id:'P014',name:'Crema Reductora Anticelulítica',cat:'belleza',img:'https://images.unsplash.com/photo-1587293852726-70cdb56c2866?w=400',img2:'https://images.unsplash.com/photo-1556228578-8c89e6adf883?w=400',price:64000,oldPrice:105000,desc:'Reduce medidas y celulitis. Con cafeína, retinol y aloe vera. Resultados en 30 días.',sold:230,stars:4,lastUnits:true,timer:60*60,cat:'belleza'},
  {id:'P015',name:'Mini Ventilador USB de Escritorio',cat:'hogar',img:'https://images.unsplash.com/photo-1589275862052-c5b5bb9c7a93?w=400',img2:'https://images.unsplash.com/photo-1557804506-669a67965ba0?w=400',price:44000,oldPrice:75000,desc:'3 velocidades silencioso. Rotación 360°. Conexión USB o banco de energía. Ideal oficina.',sold:190,stars:5,lastUnits:false,timer:45*60,cat:'hogar'},
  {id:'P016',name:'Cargador Inalámbrico 15W',cat:'tecnologia',img:'https://images.unsplash.com/photo-1586953208448-b95a79798f07?w=400',img2:'https://images.unsplash.com/photo-1612815153805-37df13efa28e?w=400',price:49000,oldPrice:89000,desc:'Carga rápida compatible con iPhone y Android. Diseño ultrafino. LED indicador.',sold:280,stars:5,lastUnits:false,timer:3*60*60,cat:'tecnologia'},
  {id:'P017',name:'Kit Pesas Mancuernas Ajustables',cat:'fitness',img:'https://images.unsplash.com/photo-1517836357463-d25dfeac3438?w=400',img2:'https://images.unsplash.com/photo-1534438327276-14e5300c3a48?w=400',price:149000,oldPrice:250000,desc:'Set 2kg a 10kg ajustables. Agarre antideslizante. Ideal para ejercicios en casa.',sold:70,stars:5,lastUnits:true,timer:24*60*60,cat:'fitness'},
  {id:'P018',name:'Mascarilla LED Facial',cat:'belleza',img:'https://images.unsplash.com/photo-1570172619644-dfd03ed5d881?w=400',img2:'https://images.unsplash.com/photo-1516975080664-ed2fc6a32937?w=400',price:129000,oldPrice:220000,desc:'7 colores terapia de luz. Anti-acné, anti-arrugas, rejuvenecimiento. Uso profesional en casa.',sold:55,stars:5,lastUnits:true,timer:2*60*60,cat:'belleza'},
  {id:'P019',name:'Termómetro Digital Infrarrojo',cat:'salud',img:'https://images.unsplash.com/photo-1584515933487-779824d29309?w=400',img2:'https://images.unsplash.com/photo-1584515933487-779824d29309?w=400',price:49000,oldPrice:90000,desc:'Sin contacto. Resultado en 1 segundo. Indicador de fiebre. Apto bebés y adultos.',sold:350,stars:5,lastUnits:false,timer:4*60*60,cat:'salud'},
  {id:'P020',name:'Bolsa Térmica Lonchera',cat:'hogar',img:'https://images.unsplash.com/photo-1553361371-9b22f78e8b1d?w=400',img2:'https://images.unsplash.com/photo-1556909114-f6e7ad7d3136?w=400',price:54000,oldPrice:90000,desc:'Mantiene frío o calor 8 horas. Impermeable. Capacidad 8L. Varios colores.',sold:160,stars:4,lastUnits:false,timer:6*60*60,cat:'hogar'},
  {id:'P021',name:'Collar Anti-Pulgas Perro/Gato',cat:'accesorios',img:'https://images.unsplash.com/photo-1587300003388-59208cc962cb?w=400',img2:'https://images.unsplash.com/photo-1546422072-7a5d6e8c2f44?w=400',price:39000,oldPrice:70000,desc:'Protege por 8 meses. Efecto repelente natural. Ajustable. Para mascotas hasta 50kg.',sold:420,stars:5,lastUnits:false,timer:30*60,cat:'accesorios'},
  {id:'P022',name:'Faja Reductora Cintura',cat:'fitness',img:'https://images.unsplash.com/photo-1576013551627-0cc20b96c2a7?w=400',img2:'https://images.unsplash.com/photo-1518611012118-696072aa579a?w=400',price:59000,oldPrice:100000,desc:'Reduce cintura, control postural. Neopreno de alta compresión. Tallas S-XXXL.',sold:310,stars:4,lastUnits:true,timer:60*60,cat:'fitness'},
  {id:'P023',name:'Silla Gaming Ergonómica',cat:'hogar',img:'https://images.unsplash.com/photo-1586023492125-27b2c045efd7?w=400',img2:'https://images.unsplash.com/photo-1555041469-a586c61ea9bc?w=400',price:349000,oldPrice:580000,desc:'Espaldar reclinable 180°. Descansabrazos ajustables. Cojín lumbar y cervical.',sold:45,stars:5,lastUnits:true,timer:24*60*60,cat:'hogar'},
  {id:'P024',name:'Set Pincel Maquillaje 15pcs',cat:'belleza',img:'https://images.unsplash.com/photo-1522337913716-6a5aa24e2c3c?w=400',img2:'https://images.unsplash.com/photo-1503236823255-94609f598e71?w=400',price:44000,oldPrice:79000,desc:'Cerdas sintéticas ultra suaves. Incluye estuche. Aptos para polvo, líquido y crema.',sold:260,stars:5,lastUnits:false,timer:45*60,cat:'belleza'},
  {id:'P025',name:'Purificador Aire USB',cat:'hogar',img:'https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=400',img2:'https://images.unsplash.com/photo-1555041469-a586c61ea9bc?w=400',price:74000,oldPrice:130000,desc:'Filtro HEPA. Elimina polvo, alérgenos y bacterias. Silencioso. Para habitaciones hasta 20m².',sold:100,stars:4,lastUnits:false,timer:3*60*60,cat:'hogar'},
  {id:'P026',name:'Pastillero Semanal Electrónico',cat:'salud',img:'https://images.unsplash.com/photo-1584515933487-779824d29309?w=400',img2:'https://images.unsplash.com/photo-1631549916768-4119b2e5f926?w=400',price:54000,oldPrice:90000,desc:'Alarma para recordar tus medicamentos. 7 compartimentos. Pantalla LCD. Portátil.',sold:75,stars:5,lastUnits:false,timer:2*60*60,cat:'salud'},
  {id:'P027',name:'Cuerda para Saltar Profesional',cat:'fitness',img:'https://images.unsplash.com/photo-1571019614242-c5c5dee9f50b?w=400',img2:'https://images.unsplash.com/photo-1534438327276-14e5300c3a48?w=400',price:34000,oldPrice:60000,desc:'Ajustable. Mango ergonómico con contador de saltos y calorías. Acero recubierto.',sold:380,stars:5,lastUnits:false,timer:30*60,cat:'fitness'},
  {id:'P028',name:'Mascarilla Puntos Negros',cat:'belleza',img:'https://images.unsplash.com/photo-1587293852726-70cdb56c2866?w=400',img2:'https://images.unsplash.com/photo-1556228578-8c89e6adf883?w=400',price:39000,oldPrice:69000,desc:'Peel-off de carbón activo. Elimina puntos negros, impurezas y poros dilatados en 20 min.',sold:190,stars:4,lastUnits:true,timer:45*60,cat:'belleza'},
  {id:'P029',name:'Luz LED RGB Escritorio',cat:'tecnologia',img:'https://images.unsplash.com/photo-1593640408182-31c70c8268f5?w=400',img2:'https://images.unsplash.com/photo-1587202372775-e229f172b9d7?w=400',price:59000,oldPrice:100000,desc:'16 millones de colores. Control por app. Ideal gaming, streaming y estudiar.',sold:215,stars:5,lastUnits:false,timer:6*60*60,cat:'tecnologia'},
  {id:'P030',name:'Soporte Celular Auto Magnético',cat:'accesorios',img:'https://images.unsplash.com/photo-1586953208448-b95a79798f07?w=400',img2:'https://images.unsplash.com/photo-1612815153805-37df13efa28e?w=400',price:34000,oldPrice:60000,desc:'Imán potente 360°. Ajuste por rejilla o parabrisas. Compatible todos los celulares.',sold:550,stars:5,lastUnits:false,timer:30*60,cat:'accesorios'},
  {id:'P031',name:'Almohada Ortopédica Cervical',cat:'hogar',img:'https://images.unsplash.com/photo-1555041469-a586c61ea9bc?w=400',img2:'https://images.unsplash.com/photo-1559494007-9f5847c49d94?w=400',price:89000,oldPrice:149000,desc:'Espuma viscoelástica. Alivia dolor de cuello y mejora postura al dormir. Funda lavable.',sold:130,stars:5,lastUnits:true,timer:60*60,cat:'hogar'},
  {id:'P032',name:'Depiladora Eléctrica Facial',cat:'belleza',img:'https://images.unsplash.com/photo-1522337913716-6a5aa24e2c3c?w=400',img2:'https://images.unsplash.com/photo-1516975080664-ed2fc6a32937?w=400',price:49000,oldPrice:85000,desc:'Elimina el vello no deseado de raíz. Sin dolor. Recargable USB. Para dama.',sold:290,stars:5,lastUnits:false,timer:45*60,cat:'belleza'},
  {id:'P033',name:'Bolígrafo Espía HD 1080p',cat:'tecnologia',img:'https://images.unsplash.com/photo-1586953208448-b95a79798f07?w=400',img2:'https://images.unsplash.com/photo-1612815153805-37df13efa28e?w=400',price:74000,oldPrice:125000,desc:'Cámara oculta en bolígrafo. Graba video Full HD. Detección de movimiento. 32GB.',sold:85,stars:4,lastUnits:true,timer:2*60*60,cat:'tecnologia'},
  {id:'P034',name:'Guantes Box Entrenamiento',cat:'fitness',img:'https://images.unsplash.com/photo-1538805060514-97d9cc17730c?w=400',img2:'https://images.unsplash.com/photo-1517836357463-d25dfeac3438?w=400',price:79000,oldPrice:140000,desc:'Cuero sintético PU. Relleno gel. Tallas S-XL. Para saco, sparring y entrenamiento.',sold:65,stars:5,lastUnits:false,timer:24*60*60,cat:'fitness'},
  {id:'P035',name:'Mochila USB Antirrobo',cat:'accesorios',img:'https://images.unsplash.com/photo-1553361371-9b22f78e8b1d?w=400',img2:'https://images.unsplash.com/photo-1573100925118-870b8efc799d?w=400',price:119000,oldPrice:200000,desc:'Puerto USB integrado, cerradura oculta. Impermeable. Capacidad 30L. Para laptop 15.6".',sold:170,stars:5,lastUnits:true,timer:3*60*60,cat:'accesorios'},
  {id:'P036',name:'Secadora de Uñas UV/LED',cat:'belleza',img:'https://images.unsplash.com/photo-1503236823255-94609f598e71?w=400',img2:'https://images.unsplash.com/photo-1522337913716-6a5aa24e2c3c?w=400',price:64000,oldPrice:110000,desc:'36W. Seca gel en 30 segundos. Timer automático. Temporizador. Para manos y pies.',sold:200,stars:5,lastUnits:false,timer:45*60,cat:'belleza'},
  {id:'P037',name:'Tensiómetro Digital Brazo',cat:'salud',img:'https://images.unsplash.com/photo-1584515933487-779824d29309?w=400',img2:'https://images.unsplash.com/photo-1631549916768-4119b2e5f926?w=400',price:89000,oldPrice:149000,desc:'Medición precisa ±2mmHg. Detecta arritmias. Memoria 60 mediciones. Pantalla grande.',sold:95,stars:5,lastUnits:false,timer:6*60*60,cat:'salud'},
  {id:'P038',name:'Taza Calentadora USB Inteligente',cat:'hogar',img:'https://images.unsplash.com/photo-1510972527921-ce03766a1cf1?w=400',img2:'https://images.unsplash.com/photo-1556909114-f6e7ad7d3136?w=400',price:54000,oldPrice:89000,desc:'Mantiene tu bebida a 55°C. Base calentadora inteligente. Control de temperatura.',sold:240,stars:5,lastUnits:false,timer:30*60,cat:'hogar'},
  {id:'P039',name:'Tapete Acupuntura Spa',cat:'salud',img:'https://images.unsplash.com/photo-1544367567-0f2fcb009e0b?w=400',img2:'https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b?w=400',price:69000,oldPrice:120000,desc:'6,210 puntos de acupuntura. Reduce estrés, dolor muscular. Incluye almohada.',sold:145,stars:4,lastUnits:true,timer:2*60*60,cat:'salud'},
  {id:'P040',name:'Sombra de Ojos 18 Tonos',cat:'belleza',img:'https://images.unsplash.com/photo-1503236823255-94609f598e71?w=400',img2:'https://images.unsplash.com/photo-1522337913716-6a5aa24e2c3c?w=400',price:44000,oldPrice:79000,desc:'Paleta pigmentada mate y brillante. Larga duración 24h. Sin grumos.',sold:310,stars:5,lastUnits:false,timer:60*60,cat:'belleza'},
  {id:'P041',name:'Altavoz Bluetooth Resistente Agua',cat:'tecnologia',img:'https://images.unsplash.com/photo-1608043152269-423dbba4e7e1?w=400',img2:'https://images.unsplash.com/photo-1606220945770-b5b6c2c55bf1?w=400',price:99000,oldPrice:169000,desc:'IPX7 sumergible. 360° sonido. Batería 20h. Ideal ducha, piscina, camping.',sold:195,stars:5,lastUnits:true,timer:3*60*60,cat:'tecnologia'},
  {id:'P042',name:'Kit Herramientas Reparación Celular',cat:'tecnologia',img:'https://images.unsplash.com/photo-1586953208448-b95a79798f07?w=400',img2:'https://images.unsplash.com/photo-1612815153805-37df13efa28e?w=400',price:39000,oldPrice:70000,desc:'25 piezas. Abre pantallas, destornilladores de precisión, palancas, pinzas.',sold:115,stars:4,lastUnits:false,timer:4*60*60,cat:'tecnologia'},
  {id:'P043',name:'Aceite Esencial Relajante',cat:'salud',img:'https://images.unsplash.com/photo-1544161515-4ab6ce6db874?w=400',img2:'https://images.unsplash.com/photo-1580618672591-eb180b1a973f?w=400',price:44000,oldPrice:75000,desc:'100% natural. Lavanda, eucalipto y menta. Difusor, masajes o baño relajante.',sold:280,stars:5,lastUnits:false,timer:45*60,cat:'salud'},
  {id:'P044',name:'Plantillas Ortopédicas',cat:'salud',img:'https://images.unsplash.com/photo-1542291026-7eec264c27ff?w=400',img2:'https://images.unsplash.com/photo-1542291026-7eec264c27ff?w=400',price:49000,oldPrice:85000,desc:'Corrección de pisada plana. Gel silicona. Alivio fascitis plantar. Tallas 35-45.',sold:165,stars:5,lastUnits:false,timer:6*60*60,cat:'salud'},
  {id:'P045',name:'Collar GPS para Mascotas',cat:'accesorios',img:'https://images.unsplash.com/photo-1587300003388-59208cc962cb?w=400',img2:'https://images.unsplash.com/photo-1546422072-7a5d6e8c2f44?w=400',price:119000,oldPrice:199000,desc:'Rastreo tiempo real por app. Alerta zona segura. Resistente al agua. Batería 7 días.',sold:55,stars:4,lastUnits:true,timer:24*60*60,cat:'accesorios'},
];

let reviews = JSON.parse(localStorage.getItem('trogui_reviews') || 'null') || [
  {name:'Valentina Torres',city:'Bogotá',stars:5,text:'Me llegó super rápido, en 4 días! El producto está 10/10, lo recomiendo 😍'},
  {name:'Juan Camilo Restrepo',city:'Medellín',stars:5,text:'Pagé contra entrega y todo bien. La calidad es buenísima, gracias trogui!'},
  {name:'Luisa Fernanda Gómez',city:'Cali',stars:4,text:'lindo producto aunq la entrega demoro un poco pero llegó bien, lo recomiendo'},
  {name:'Andrés Felipe Ospina',city:'Bucaramanga',stars:5,text:'Segunda vez que compro aquí y siempre quedo satisfecho. 100% confiable'},
  {name:'Natalia Suárez',city:'Barranquilla',stars:5,text:'Excelente! El quita callos me funcionó de maravilla desde el primer uso jajaja'},
];

let cart = [];
let orders = JSON.parse(localStorage.getItem('trogui_orders') || '[]');
let currentOrderProduct = null;
let timers = {};
let sliderIndex = 0;
let visitors = Math.floor(Math.random()*40)+15;

// ===================== INIT =====================
document.addEventListener('DOMContentLoaded', ()=>{
  renderProducts(products);
  startSlider();
  startNotifications();
  updateVisitors();
  loadPageSettings();
  startVisitorCount();
  startShakeLoop();
});

function loadPageSettings(){
  const tb = localStorage.getItem('trogui_topbar');
  if(tb) document.querySelector('.topbar').innerHTML = tb;
  const pt = localStorage.getItem('trogui_prod_title');
  if(pt) document.querySelector('.section-title').innerHTML = pt;
  const au = localStorage.getItem('trogui_audio');
  if(au){ document.getElementById('audio-src').src=au; document.getElementById('audio-autoplay').load(); }
}

// ===================== SLIDER =====================
function moveSlider(dir){sliderIndex=(sliderIndex+dir+3)%3;updateSlider();}
function goSlide(i){sliderIndex=i;updateSlider();}
function updateSlider(){
  document.getElementById('slider-track').style.transform=`translateX(-${sliderIndex*100}%)`;
  document.querySelectorAll('.dot').forEach((d,i)=>d.classList.toggle('active',i===sliderIndex));
}
function startSlider(){setInterval(()=>moveSlider(1),6000);}

// ===================== FORMAT =====================
function fmt(n){return Number(n).toLocaleString('es-CO');}

// ===================== PRODUCTS =====================
function renderProducts(prods){
  const grid=document.getElementById('products-grid');
  grid.innerHTML='';
  prods.forEach(p=>{
    const disc=Math.round((1-p.price/p.oldPrice)*100);
    const el=document.createElement('div');
    el.className='product-card';
    el.id='card-'+p.id;
    el.innerHTML=`
      <div class="product-img-wrap" onclick="openModal('${p.id}')">
        <img src="${p.img}" alt="${p.name}" onerror="this.src='https://via.placeholder.com/400x300?text=TROGUI'">
        <div class="badge-offer">-${disc}% OFF</div>
        <div class="badge-sold">✅ ${p.sold}+ vendidos</div>
        ${p.lastUnits?'<div class="badge-last">⚠️ Últimas unidades</div>':''}
      </div>
      <div class="product-info" onclick="openModal('${p.id}')">
        <div class="product-name">${p.name}</div>
        <div class="stars">${'⭐'.repeat(p.stars)}<span>(${p.stars}.0)</span></div>
        <div class="price-wrap">
          <span class="price-old">$${fmt(p.oldPrice)}</span>
          <span class="price-new">$${fmt(p.price)}</span>
        </div>
        <div class="timer-badge" id="timer-${p.id}">⏰ Cargando...</div>
        <div class="free-ship">🚚 Envío GRATIS a toda Colombia</div>
        <div class="delivery-info">💵 Pago contra entrega disponible</div>
      </div>
      <div class="product-info" style="padding-top:0">
        <div class="card-btns">
          <button class="btn-add" onclick="event.stopPropagation();addToCart('${p.id}')">🛒 Al Carrito</button>
          <button class="btn-pedir" id="pedir-${p.id}" onclick="event.stopPropagation();openOrderFormDirect('${p.id}')">🔥 ¡Pedir Ahora!</button>
        </div>
      </div>`;
    grid.appendChild(el);
    startTimer(p.id,p.timer);
  });
}

function filterCat(cat,el){
  document.querySelectorAll('.nav-inner a').forEach(a=>a.classList.remove('active'));
  el.classList.add('active');
  const filtered=cat==='all'?products:products.filter(p=>p.cat===cat);
  renderProducts(filtered);
}

// ===================== SHAKE LOOP =====================
function startShakeLoop(){
  setInterval(()=>{
    const btns=document.querySelectorAll('.btn-pedir');
    if(btns.length===0) return;
    const idx=Math.floor(Math.random()*btns.length);
    const btn=btns[idx];
    btn.classList.remove('shaking');
    void btn.offsetWidth;
    btn.classList.add('shaking');
    setTimeout(()=>btn.classList.remove('shaking'),700);
  },2500);
}

// ===================== TIMER =====================
function startTimer(id,seconds){
  if(timers[id]) clearInterval(timers[id]);
  let remaining=seconds;
  function update(){
    const el=document.getElementById('timer-'+id);
    if(!el) return;
    if(remaining<=0){el.innerHTML='⚡ ¡Oferta vigente!';return;}
    const h=Math.floor(remaining/3600);
    const m=Math.floor((remaining%3600)/60);
    const s=remaining%60;
    let label=h>0?`${h}h ${m}m ${s}s`:m>0?`${m}m ${s}s`:`${s}s`;
    el.innerHTML=`⏰ Oferta acaba en: <b>${label}</b>`;
    remaining--;
  }
  update();
  timers[id]=setInterval(update,1000);
}

// ===================== MODAL =====================
function openModal(id){
  const p=products.find(x=>x.id===id);
  if(!p) return;
  const disc=Math.round((1-p.price/p.oldPrice)*100);
  const revHtml=reviews.map(r=>`
    <div class="review-item">
      <div class="review-top">
        <div class="review-avatar">${r.name[0]}</div>
        <div><div class="review-name">${r.name} - ${r.city}</div><div class="review-stars">${'⭐'.repeat(r.stars)}</div></div>
      </div>
      <div class="review-text">${r.text}</div>
    </div>`).join('');
  document.getElementById('modal-content').innerHTML=`
    <div class="modal-imgs">
      <img src="${p.img}" alt="${p.name}" onerror="this.src='https://via.placeholder.com/400x300?text=TROGUI'">
      <img src="${p.img2||p.img}" alt="${p.name}" onerror="this.src='https://via.placeholder.com/400x300?text=TROGUI'">
    </div>
    <div style="font-size:11px;color:var(--gray);margin-bottom:4px">ID: ${p.id}</div>
    <div class="modal-title">${p.name}</div>
    <div class="stars">${'⭐'.repeat(p.stars)} <span style="color:var(--gray);font-size:13px">${p.stars}.0 (${p.sold}+ vendidos)</span></div>
    <div class="modal-price-wrap">
      <span class="modal-price-old">$${fmt(p.oldPrice)}</span>
      <span class="modal-price-new">$${fmt(p.price)}</span>
      <span style="background:#ffe0cc;color:var(--orange);font-weight:800;padding:4px 10px;border-radius:20px;font-size:13px">-${disc}%</span>
    </div>
    <div class="modal-delivery">
      🚚 <strong>Envío GRATIS</strong> a toda Colombia · Entrega en <strong>3 a 7 días hábiles</strong><br>
      💵 <strong>Pago Contra Entrega</strong> disponible · Interrapidísimo · Coordinadora · Envia
    </div>
    <div class="modal-desc">${p.desc}</div>
    ${p.lastUnits?'<div style="background:#fff0f0;border:1px solid var(--red);border-radius:10px;padding:10px;font-size:13px;font-weight:800;color:var(--red)">⚠️ ¡ÚLTIMAS UNIDADES! Stock limitado</div>':''}
    <button class="btn-order" onclick="openOrderForm('${p.id}')">🔥 ¡Pedir Ahora - Pago Contra Entrega!</button>
    <h3 style="margin:20px 0 12px;font-family:'Poppins',sans-serif">⭐ Reseñas de Clientes</h3>
    <div class="review-list">${revHtml}</div>`;
  document.getElementById('product-modal').classList.add('active');
}
function closeModal(){document.getElementById('product-modal').classList.remove('active');}

// ===================== ORDER FORM =====================
function openOrderForm(id){
  const p=products.find(x=>x.id===id);
  if(!p) return;
  currentOrderProduct=p;
  closeModal();
  _showOrderForm(p);
}
function openOrderFormDirect(id){
  const p=products.find(x=>x.id===id);
  if(!p) return;
  currentOrderProduct=p;
  _showOrderForm(p);
}
function _showOrderForm(p){
  document.getElementById('form-prod-name').textContent=p.name+' (ID: '+p.id+')';
  document.getElementById('form-price-show').innerHTML=`
    <div><div style="font-size:13px;color:var(--gray);font-weight:700">Precio anterior:</div><div class="fold">$${fmt(p.oldPrice)}</div></div>
    <div style="text-align:right"><div style="font-size:13px;font-weight:700;color:var(--gray)">Pagas hoy:</div><div class="fprice">$${fmt(p.price)}</div></div>`;
  document.getElementById('order-form-section').classList.add('active');
}
function closeOrderForm(){document.getElementById('order-form-section').classList.remove('active');}

function confirmOrder(){
  const nombre=document.getElementById('f-nombre').value.trim();
  const apellido=document.getElementById('f-apellido').value.trim();
  const depto=document.getElementById('f-departamento').value.trim();
  const ciudad=document.getElementById('f-ciudad').value.trim();
  const direccion=document.getElementById('f-direccion').value.trim();
  const telefono=document.getElementById('f-telefono').value.trim();
  const nota=document.getElementById('f-nota').value.trim();
  if(!nombre||!apellido||!depto||!ciudad||!direccion||!telefono){alert('Por favor completa todos los campos obligatorios.');return;}
  const p=currentOrderProduct;
  const disc=Math.round((1-p.price/p.oldPrice)*100);
  const order={
    id:'ORD'+Date.now(),
    product:p.name,
    productId:p.id,
    price:p.price,
    oldPrice:p.oldPrice,
    discount:disc,
    nombre,apellido,
    departamento:depto,
    ciudad,direccion,telefono,nota,
    fecha:new Date().toLocaleString('es-CO'),
    fechaISO:new Date().toISOString()
  };
  orders.push(order);
  localStorage.setItem('trogui_orders',JSON.stringify(orders));
  const msg=encodeURIComponent(
    `🛍️ *NUEVO PEDIDO - TROGÜI*\n\n`+
    `📦 *Producto:* ${p.name}\n`+
    `🆔 *ID:* ${p.id}\n`+
    `💰 *Precio:* $${fmt(p.price)} (-${disc}%)\n`+
    `\n👤 *Cliente:* ${nombre} ${apellido}\n`+
    `🗺️ *Departamento:* ${depto}\n`+
    `🏙️ *Ciudad:* ${ciudad}\n`+
    `🏠 *Dirección:* ${direccion}\n`+
    `📞 *Teléfono:* ${telefono}\n`+
    `📝 *Nota:* ${nota||'Sin nota'}\n\n`+
    `✅ Pago contra entrega`
  );
  closeOrderForm();
  window.open(`https://wa.me/573206572598?text=${msg}`,'_blank');
}

// ===================== CART =====================
function addToCart(id){
  const p=products.find(x=>x.id===id);
  if(!p) return;
  const existing=cart.find(x=>x.id===id);
  if(existing) existing.qty++;
  else cart.push({...p,qty:1});
  updateCartUI();
  showFloatMsg('✅ '+p.name+' agregado al carrito');
}
function removeFromCart(id){cart=cart.filter(x=>x.id!==id);updateCartUI();}
function updateCartUI(){
  const count=cart.reduce((a,b)=>a+b.qty,0);
  document.getElementById('cart-count').textContent=count;
  const list=document.getElementById('cart-items-list');
  if(cart.length===0){list.innerHTML='<div class="empty-cart">🛒 Tu carrito está vacío</div>';document.getElementById('cart-total').textContent='';document.getElementById('btn-checkout').style.display='none';return;}
  list.innerHTML=cart.map(item=>`
    <div class="cart-item">
      <img src="${item.img}" alt="${item.name}" onerror="this.src='https://via.placeholder.com/70?text=T'">
      <div class="cart-item-info">
        <div class="cart-item-name">${item.name}</div>
        <div class="cart-item-price">$${fmt(item.price)} × ${item.qty}</div>
      </div>
      <button class="cart-item-remove" onclick="removeFromCart('${item.id}')">✕</button>
    </div>`).join('');
  const total=cart.reduce((a,b)=>a+b.price*b.qty,0);
  document.getElementById('cart-total').innerHTML=`Total: <span style="color:var(--orange)">$${fmt(total)}</span>`;
  document.getElementById('btn-checkout').style.display='block';
}
function toggleCart(){document.getElementById('cart-drawer').classList.toggle('open');}
function checkoutCart(){
  if(cart.length===0) return;
  const lines=cart.map(i=>`• ${i.name} x${i.qty} = $${fmt(i.price*i.qty)}`).join('\n');
  const total=cart.reduce((a,b)=>a+b.price*b.qty,0);
  const msg=encodeURIComponent(`🛍️ *PEDIDO CARRITO - TROGÜI*\n\n${lines}\n\n💰 *Total: $${fmt(total)}*\n\nDeseo pagar contra entrega 🙏`);
  window.open(`https://wa.me/573206572598?text=${msg}`,'_blank');
}

// ===================== SEARCH =====================
function levenshtein(a,b){
  const m=a.length,n=b.length,dp=Array.from({length:m+1},(_,i)=>[i,...Array(n).fill(0)]);
  for(let j=0;j<=n;j++) dp[0][j]=j;
  for(let i=1;i<=m;i++) for(let j=1;j<=n;j++) dp[i][j]=a[i-1]===b[j-1]?dp[i-1][j-1]:1+Math.min(dp[i-1][j],dp[i][j-1],dp[i-1][j-1]);
  return dp[m][n];
}
function searchProducts(q){
  const dd=document.getElementById('search-dropdown');
  if(!q||q.length<2){dd.classList.remove('open');renderProducts(products);return;}
  const ql=q.toLowerCase();
  const scored=products.map(p=>{
    const nl=p.name.toLowerCase();
    const exact=nl.includes(ql)?0:1;
    const lev=Math.min(...nl.split(' ').map(w=>levenshtein(ql,w)));
    return{p,score:exact*10+lev};
  }).filter(x=>x.score<6).sort((a,b)=>a.score-b.score).slice(0,8);
  if(scored.length===0){dd.innerHTML='<div style="padding:12px 16px;color:var(--gray);font-size:14px">No se encontraron productos</div>';dd.classList.add('open');return;}
  dd.innerHTML=scored.map(({p})=>`
    <div class="search-dropdown-item" onclick="openModal('${p.id}');document.getElementById('search-dropdown').classList.remove('open')">
      <img src="${p.img}" alt="${p.name}" onerror="this.src='https://via.placeholder.com/36?text=T'">
      <div><div style="font-weight:700;font-size:14px">${p.name}</div><div style="color:var(--orange);font-weight:800;font-size:13px">$${fmt(p.price)}</div></div>
    </div>`).join('');
  dd.classList.add('open');
  renderProducts(scored.map(x=>x.p));
}
document.addEventListener('click',e=>{if(!e.target.closest('.search-bar')) document.getElementById('search-dropdown').classList.remove('open');});

// ===================== DELIVERY CALC =====================
function calcDelivery(){
  const sel=document.getElementById('delivery-city');
  const days=parseInt(sel.value)||5;
  if(!sel.value){alert('Selecciona una ciudad');return;}
  const now=new Date();
  now.setDate(now.getDate()+days);
  const opts={weekday:'long',year:'numeric',month:'long',day:'numeric'};
  const dateStr=now.toLocaleDateString('es-CO',opts);
  const el=document.getElementById('delivery-result');
  el.style.display='block';
  el.innerHTML=`📦 Tu pedido llegaría aproximadamente el <strong>${dateStr}</strong> (entre ${days} y ${days+1} días hábiles).`;
}

// ===================== NOTIFICATIONS =====================
const notifNames=[
  {name:'Juan Camilo Paz',city:'Medellín'},{name:'Valentina Torres',city:'Bogotá'},
  {name:'Luisa Gómez',city:'Cali'},{name:'Andrés Ospina',city:'Bucaramanga'},
  {name:'Natalia Suárez',city:'Barranquilla'},{name:'Carlos Herrera',city:'Pereira'},
  {name:'María José López',city:'Manizales'},{name:'Felipe Restrepo',city:'Cartagena'},
  {name:'Sofía Martínez',city:'Ibagué'},{name:'Daniel Vargas',city:'Santa Marta'},
];
function startNotifications(){
  let i=0;
  setInterval(()=>{
    const {name,city}=notifNames[i%notifNames.length];
    const p=products[Math.floor(Math.random()*products.length)];
    showNotif(`🛍️ <span class="notif-name">${name}</span> de ${city} hizo un pedido de <b>${p.name}</b>`);
    i++;
  },8000);
}
function showNotif(html){
  const nb=document.getElementById('notif-box');
  nb.innerHTML=html;nb.style.display='block';
  setTimeout(()=>nb.style.display='none',4000);
}
function showFloatMsg(msg){
  const div=document.createElement('div');
  div.style.cssText='position:fixed;bottom:150px;left:50%;transform:translateX(-50%);background:var(--dark);color:#fff;padding:10px 20px;border-radius:20px;font-weight:700;font-size:14px;z-index:9999;animation:slideUp .4s';
  div.textContent=msg;
  document.body.appendChild(div);
  setTimeout(()=>div.remove(),2500);
}
function updateVisitors(){
  setInterval(()=>{
    visitors=Math.max(8,visitors+Math.floor(Math.random()*5)-2);
    document.querySelectorAll('#visitors-count,#visitors-count2').forEach(el=>el.textContent=visitors);
  },5000);
}
function startVisitorCount(){
  document.querySelectorAll('#visitors-count,#visitors-count2').forEach(el=>el.textContent=visitors);
}

// ===================== ADMIN AUTH =====================
function adminAuth(panel){
  const pass=prompt('Ingresa la contraseña de administrador:');
  if(pass!==ADMIN_PASS){alert('Contraseña incorrecta');return;}
  if(panel==='r') openAdminR();
  else if(panel==='c') openAdminC();
  else if(panel==='e') openAdminE();
}
function closeAdmin(id){document.getElementById(id).classList.remove('active');}

// ===================== ADMIN R =====================
function openAdminR(){renderAdminProducts();document.getElementById('admin-r').classList.add('active');}

function mkLabel(text,styles){
  const l=document.createElement('label');l.textContent=text;
  Object.assign(l.style,{fontWeight:'800',fontSize:'13px',display:'block',marginBottom:'3px',marginTop:'8px',...(styles||{})});
  return l;
}
function mkInput(id,value,type,placeholder){
  const inp=document.createElement('input');
  inp.type=type||'text';inp.id=id;inp.value=value||'';
  if(placeholder) inp.placeholder=placeholder;
  Object.assign(inp.style,{width:'100%',padding:'8px 10px',border:'1.5px solid #e5e5e5',borderRadius:'8px',fontSize:'13px',fontFamily:'Nunito,sans-serif',boxSizing:'border-box'});
  return inp;
}
function buildImgRow(pid,suffix,currentSrc,label){
  const prevImg=document.createElement('img');
  prevImg.id='prev'+suffix+'-'+pid;prevImg.src=currentSrc||'https://via.placeholder.com/80?text=IMG';prevImg.alt='preview';
  Object.assign(prevImg.style,{width:'80px',height:'80px',objectFit:'cover',borderRadius:'10px',border:'2px solid #e5e5e5',background:'#f4f4f4',flexShrink:'0'});
  prevImg.onerror=function(){this.src='https://via.placeholder.com/80?text=IMG';};
  const urlInp=mkInput('ai'+suffix+'-'+pid,currentSrc,'text','🔗 URL de imagen (https://...)');
  urlInp.addEventListener('input',function(){const v=this.value.trim();if(v){prevImg.src=v;}});
  const fileInp=document.createElement('input');fileInp.type='file';fileInp.accept='image/*';fileInp.style.cssText='display:none';
  fileInp.addEventListener('change',function(){
    const file=this.files[0];if(!file)return;
    const reader=new FileReader();
    reader.onload=function(e){urlInp.value=e.target.result;prevImg.src=e.target.result;showFloatMsg('✅ Imagen cargada. Pulsa Guardar.');};
    reader.readAsDataURL(file);
  });
  const fileBtn=document.createElement('label');fileBtn.textContent='📁 Subir foto';fileBtn.appendChild(fileInp);
  Object.assign(fileBtn.style,{display:'block',background:'#FF5200',color:'#fff',padding:'7px 10px',borderRadius:'8px',cursor:'pointer',fontSize:'12px',fontWeight:'800',textAlign:'center',marginTop:'4px'});
  const col=document.createElement('div');Object.assign(col.style,{flex:'1',minWidth:'160px',display:'flex',flexDirection:'column',gap:'4px'});
  col.appendChild(urlInp);col.appendChild(fileBtn);
  const row=document.createElement('div');Object.assign(row.style,{display:'flex',gap:'10px',alignItems:'flex-start',flexWrap:'wrap',marginBottom:'6px'});
  row.appendChild(prevImg);row.appendChild(col);
  const lbl=mkLabel(label,{color:'#FF5200'});
  const wrap=document.createElement('div');wrap.appendChild(lbl);wrap.appendChild(row);
  return wrap;
}
function buildProductCard(p){
  const card=document.createElement('div');card.className='admin-product-item';card.id='aitem-'+p.id;
  const hdr=document.createElement('div');Object.assign(hdr.style,{display:'flex',justifyContent:'space-between',alignItems:'center',marginBottom:'8px'});
  const title=document.createElement('b');title.textContent=p.id+' — '+p.name;Object.assign(title.style,{fontSize:'13px',color:'#FF5200'});
  const delBtn=document.createElement('button');delBtn.textContent='🗑️ Eliminar';delBtn.className='btn-del-admin';delBtn.onclick=()=>deleteProduct(p.id);
  hdr.appendChild(title);hdr.appendChild(delBtn);card.appendChild(hdr);
  card.appendChild(mkLabel('Nombre'));card.appendChild(mkInput('an-'+p.id,p.name));
  card.appendChild(mkLabel('Descripción'));
  const ta=document.createElement('textarea');ta.id='ad-'+p.id;ta.rows=2;ta.textContent=p.desc||'';
  Object.assign(ta.style,{width:'100%',padding:'8px 10px',border:'1.5px solid #e5e5e5',borderRadius:'8px',fontSize:'13px',fontFamily:'Nunito,sans-serif',resize:'vertical',boxSizing:'border-box'});
  card.appendChild(ta);
  const r1=document.createElement('div');r1.className='row2';
  const c1=document.createElement('div');c1.appendChild(mkLabel('Precio ($)'));c1.appendChild(mkInput('ap-'+p.id,p.price,'number'));r1.appendChild(c1);
  const c2=document.createElement('div');c2.appendChild(mkLabel('Precio anterior ($)'));c2.appendChild(mkInput('ao-'+p.id,p.oldPrice,'number'));r1.appendChild(c2);
  card.appendChild(r1);
  const r2=document.createElement('div');r2.className='row2';
  const c3=document.createElement('div');c3.appendChild(mkLabel('Vendidos'));c3.appendChild(mkInput('av-'+p.id,p.sold,'number'));r2.appendChild(c3);
  const c4=document.createElement('div');c4.appendChild(mkLabel('Estrellas (1-5)'));const sinp=mkInput('as-'+p.id,p.stars,'number');sinp.min='1';sinp.max='5';c4.appendChild(sinp);r2.appendChild(c4);
  card.appendChild(r2);
  card.appendChild(buildImgRow(p.id,'',p.img,'📷 Imagen Principal'));
  card.appendChild(buildImgRow(p.id,'2',p.img2||p.img,'📷 Imagen Secundaria'));
  card.appendChild(mkLabel('Categoría'));
  const sel=document.createElement('select');sel.id='ac-'+p.id;
  Object.assign(sel.style,{width:'100%',padding:'8px',border:'1.5px solid #e5e5e5',borderRadius:'8px',fontSize:'13px',fontFamily:'Nunito,sans-serif'});
  ['belleza','hogar','tecnologia','salud','fitness','juguetes','accesorios'].forEach(c=>{const opt=document.createElement('option');opt.value=c;opt.textContent=c;if(p.cat===c)opt.selected=true;sel.appendChild(opt);});
  card.appendChild(sel);
  const r3=document.createElement('div');r3.className='row2';Object.assign(r3.style,{marginTop:'6px'});
  const c5=document.createElement('div');c5.appendChild(mkLabel('Últimas unidades'));
  const sel2=document.createElement('select');sel2.id='alu-'+p.id;
  Object.assign(sel2.style,{width:'100%',padding:'8px',border:'1.5px solid #e5e5e5',borderRadius:'8px',fontSize:'13px',fontFamily:'Nunito,sans-serif'});
  [{v:'true',t:'Sí'},{v:'false',t:'No'}].forEach(({v,t})=>{const o=document.createElement('option');o.value=v;o.textContent=t;if((p.lastUnits?'true':'false')===v)o.selected=true;sel2.appendChild(o);});
  c5.appendChild(sel2);r3.appendChild(c5);
  const c6=document.createElement('div');c6.appendChild(mkLabel('Timer (segundos)'));c6.appendChild(mkInput('at-'+p.id,p.timer,'number'));r3.appendChild(c6);
  card.appendChild(r3);
  const saveBtn=document.createElement('button');saveBtn.textContent='💾 Guardar este producto';saveBtn.className='btn-save-admin';
  Object.assign(saveBtn.style,{marginTop:'12px',width:'100%',fontSize:'14px'});saveBtn.onclick=()=>saveOneProduct(p.id);
  card.appendChild(saveBtn);
  return card;
}
function renderAdminProducts(){
  const list=document.getElementById('admin-product-list');list.innerHTML='';
  products.forEach(p=>list.appendChild(buildProductCard(p)));
}
function deleteProduct(id){
  if(!confirm('¿Eliminar este producto?'))return;
  products=products.filter(p=>p.id!==id);
  localStorage.setItem('trogui_products',JSON.stringify(products));
  renderAdminProducts();renderProducts(products);
}
function addNewProduct(){
  const newId='P'+String(Date.now()).slice(-5);
  products.push({id:newId,name:'Nuevo Producto',cat:'hogar',img:'https://images.unsplash.com/photo-1512436991641-6745cdb1723f?w=400',img2:'https://images.unsplash.com/photo-1512436991641-6745cdb1723f?w=400',price:49000,oldPrice:89000,desc:'Descripción del producto.',sold:10,stars:5,lastUnits:false,timer:3600});
  localStorage.setItem('trogui_products',JSON.stringify(products));
  renderAdminProducts();renderProducts(products);
  setTimeout(()=>document.getElementById('admin-product-list').lastElementChild?.scrollIntoView({behavior:'smooth'}),150);
}
function saveOneProduct(id){
  const p=products.find(x=>x.id===id);if(!p)return;
  const nEl=document.getElementById('an-'+id);if(!nEl)return;
  p.name=nEl.value||p.name;
  p.desc=document.getElementById('ad-'+id).value;
  p.price=parseInt(document.getElementById('ap-'+id).value)||p.price;
  p.oldPrice=parseInt(document.getElementById('ao-'+id).value)||p.oldPrice;
  p.sold=parseInt(document.getElementById('av-'+id).value)||p.sold;
  p.stars=parseInt(document.getElementById('as-'+id).value)||p.stars;
  const img1=document.getElementById('ai-'+id).value.trim();
  const img2=document.getElementById('ai2-'+id).value.trim();
  if(img1)p.img=img1;if(img2)p.img2=img2;
  p.cat=document.getElementById('ac-'+id).value;
  p.lastUnits=document.getElementById('alu-'+id).value==='true';
  p.timer=parseInt(document.getElementById('at-'+id).value)||p.timer;
  localStorage.setItem('trogui_products',JSON.stringify(products));
  renderProducts(products);showFloatMsg('✅ "'+p.name+'" guardado!');
}
function saveProducts(silent){
  products.forEach(p=>saveOneProduct(p.id));
  localStorage.setItem('trogui_products',JSON.stringify(products));
  renderProducts(products);
  if(!silent)showFloatMsg('✅ Todos los productos guardados!');
}

// ===================== ADMIN C - PEDIDOS =====================
let filteredOrders = [];

function openAdminC(){
  filteredOrders=[...orders].reverse();
  renderOrderStats();
  renderOrdersList(filteredOrders);
  document.getElementById('order-search').value='';
  document.getElementById('admin-c').classList.add('active');
}

function renderOrderStats(){
  const total=orders.length;
  const totalRevenue=orders.reduce((s,o)=>s+(o.price||0),0);
  const today=new Date().toLocaleDateString('es-CO');
  const todayOrders=orders.filter(o=>o.fecha&&o.fecha.startsWith(today)).length;
  const ciudades=[...new Set(orders.map(o=>o.ciudad).filter(Boolean))].length;
  document.getElementById('orders-stats').innerHTML=`
    <div class="stat-card"><div class="sv">${total}</div><div class="sl">Total pedidos</div></div>
    <div class="stat-card"><div class="sv">$${fmt(totalRevenue)}</div><div class="sl">Ingresos totales</div></div>
    <div class="stat-card"><div class="sv">${todayOrders}</div><div class="sl">Pedidos hoy</div></div>
    <div class="stat-card"><div class="sv">${ciudades}</div><div class="sl">Ciudades</div></div>`;
}

function renderOrdersList(list){
  const cont=document.getElementById('admin-orders-list');
  if(list.length===0){
    cont.innerHTML=`<div class="no-orders"><div class="no-ico">📭</div><b>No hay pedidos${document.getElementById('order-search').value?' con ese filtro':' aún'}.</b></div>`;
    return;
  }
  cont.innerHTML=list.map(o=>{
    const disc=o.discount||Math.round((1-(o.price/o.oldPrice))*100)||0;
    const waMsg=encodeURIComponent(`Hola ${o.nombre}, tu pedido de *${o.product}* por $${fmt(o.price)} está confirmado. ¡Gracias por comprar en TROGÜI! 🛍️`);
    return `
    <div class="order-card">
      <div class="order-card-header">
        <div>
          <div class="order-id">#${o.id}</div>
          <div class="order-product-name">${o.product}</div>
        </div>
        <div class="order-time-badge">🕐 ${o.fecha||'—'}</div>
      </div>
      <div class="order-grid">
        <div class="order-field">
          <span class="of-label">👤 Nombre</span>
          <span class="of-value">${o.nombre} ${o.apellido||''}</span>
        </div>
        <div class="order-field">
          <span class="of-label">📞 Teléfono</span>
          <span class="of-value">${o.telefono}</span>
        </div>
        <div class="order-field">
          <span class="of-label">🗺️ Departamento</span>
          <span class="of-value">${o.departamento||'—'}</span>
        </div>
        <div class="order-field">
          <span class="of-label">🏙️ Ciudad</span>
          <span class="of-value">${o.ciudad}</span>
        </div>
        <div class="order-field" style="grid-column:1/-1">
          <span class="of-label">🏠 Dirección</span>
          <span class="of-value">${o.direccion}</span>
        </div>
      </div>
      <div class="order-price-row">
        <div>
          <div class="order-price-new">$${fmt(o.price)}</div>
          <div class="order-price-old">Antes $${fmt(o.oldPrice)}</div>
        </div>
        <div class="order-discount-badge">-${disc}% OFF</div>
        <button class="order-wa-btn" onclick="window.open('https://wa.me/57${o.telefono.replace(/\D/g,'')}?text=${waMsg}','_blank')">💬 Contactar</button>
      </div>
      ${o.nota?`<div class="order-nota">📝 Nota: ${o.nota}</div>`:''}
    </div>`;
  }).join('');
}

function filterOrders(q){
  if(!q){filteredOrders=[...orders].reverse();renderOrdersList(filteredOrders);return;}
  const ql=q.toLowerCase();
  filteredOrders=[...orders].reverse().filter(o=>
    (o.nombre||'').toLowerCase().includes(ql)||
    (o.apellido||'').toLowerCase().includes(ql)||
    (o.ciudad||'').toLowerCase().includes(ql)||
    (o.departamento||'').toLowerCase().includes(ql)||
    (o.product||'').toLowerCase().includes(ql)||
    (o.telefono||'').includes(q)||
    (o.id||'').toLowerCase().includes(ql)
  );
  renderOrdersList(filteredOrders);
}

function exportOrdersCSV(){
  if(orders.length===0){alert('No hay pedidos para exportar.');return;}
  const headers=['ID','Producto','Precio','Precio Anterior','Descuento %','Nombre','Apellido','Departamento','Ciudad','Dirección','Teléfono','Nota','Fecha'];
  const rows=orders.map(o=>[
    o.id,o.product,o.price,o.oldPrice,o.discount||'',
    o.nombre,o.apellido||'',o.departamento||'',o.ciudad,o.direccion,o.telefono,o.nota||'',o.fecha
  ].map(v=>`"${String(v||'').replace(/"/g,'""')}"`).join(','));
  const csv='\uFEFF'+[headers.join(','),...rows].join('\n');
  const blob=new Blob([csv],{type:'text/csv;charset=utf-8;'});
  const url=URL.createObjectURL(blob);
  const a=document.createElement('a');a.href=url;a.download='pedidos_trogui_'+new Date().toISOString().slice(0,10)+'.csv';a.click();
  URL.revokeObjectURL(url);
  showFloatMsg('✅ CSV exportado correctamente');
}

function clearOrders(){
  if(!confirm('¿Limpiar TODOS los pedidos? Esta acción no se puede deshacer.'))return;
  orders=[];localStorage.removeItem('trogui_orders');openAdminC();
}

// ===================== ADMIN E =====================
function openAdminE(){
  document.getElementById('edit-topbar').value=document.querySelector('.topbar').innerHTML.replace(/<[^>]+>/g,'');
  document.getElementById('edit-prod-title').value=document.querySelector('.section-title').textContent;
  document.getElementById('audio-url-input').value=localStorage.getItem('trogui_audio')||'';
  renderAdminReviews();
  document.getElementById('admin-e').classList.add('active');
}
function savePageSetting(key){
  if(key==='topbar'){const val=document.getElementById('edit-topbar').value;document.querySelector('.topbar').textContent=val;localStorage.setItem('trogui_topbar',val);}
  else if(key==='prod-title'){const val=document.getElementById('edit-prod-title').value;document.querySelector('.section-title').innerHTML=val;localStorage.setItem('trogui_prod_title',val);}
  showFloatMsg('✅ Guardado correctamente');
}
function setAudio(){
  const url=document.getElementById('audio-url-input').value.trim();
  if(!url){alert('Ingresa una URL de audio');return;}
  document.getElementById('audio-src').src=url;
  document.getElementById('audio-autoplay').load();
  document.getElementById('audio-autoplay').play();
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
  showFloatMsg('✅ Reseñas guardadas');
}
</script>
</body>
</html>
