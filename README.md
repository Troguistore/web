<!DOCTYPE html>
<html lang="es-CO">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0">
<title>Trogüi — Bodega Colombiana | Envío Gratis y Pago Contra Entrega</title>
<meta name="description" content="Trogüi, bodega colombiana con más de 3 años de experiencia. Productos para hogar, cocina, tecnología y salud. Envío gratis a toda Colombia y pago contra entrega.">
<link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><rect width=%22100%22 height=%22100%22 rx=%2220%22 fill=%22%23ff6a00%22/><text x=%2250%22 y=%2266%22 font-size=%2255%22 font-family=%22Arial%22 font-weight=%22900%22 fill=%22white%22 text-anchor=%22middle%22>T</text></svg>">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="preconnect" href="https://d39ru7awumhhs2.cloudfront.net">
<link rel="dns-prefetch" href="https://d39ru7awumhhs2.cloudfront.net">
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700;800;900&display=swap" rel="stylesheet">
<style>
:root{
  --black:#14140f;
  --black-soft:#1f1f18;
  --white:#ffffff;
  --cream:#faf9f6;
  --orange:#ff6a00;
  --orange-dark:#e25a00;
  --orange-light:#ff8a3d;
  --green:#25d366;
  --gray:#6b6b63;
  --gray-light:#e9e7e0;
  --radius:14px;
  --shadow:0 6px 24px rgba(20,20,15,.10);
  font-size:16px;
}
*{box-sizing:border-box;}
html,body{margin:0;padding:0;}
body{
  font-family:'Poppins',system-ui,-apple-system,Segoe UI,Roboto,sans-serif;
  background:var(--cream);
  color:var(--black);
  -webkit-font-smoothing:antialiased;
  overflow-x:hidden;
}
img{max-width:100%;display:block;}
a{color:inherit;text-decoration:none;}
button{font-family:inherit;cursor:pointer;border:none;}
.hidden{display:none !important;}
::selection{background:var(--orange);color:#fff;}

/* ---------- ICONOS ---------- */
.icon{width:17px;height:17px;flex:none;display:inline-block;vertical-align:-4px;}

/* ---------- HEADER ---------- */
header.site-header{
  background:var(--black);
  position:sticky;top:0;z-index:60;
  padding:12px 16px;
  box-shadow:0 2px 10px rgba(0,0,0,.25);
}
.header-inner{
  max-width:1280px;margin:0 auto;
  display:flex;align-items:center;gap:16px;flex-wrap:wrap;
}
.logo{
  font-family:'Poppins',sans-serif;
  font-weight:800;
  font-size:1.7rem;
  color:#fff;
  letter-spacing:.02em;
  display:flex;align-items:center;gap:2px;
  user-select:none;
}
.logo .accent-o{color:var(--orange);}
.logo small{
  display:block;font-size:.55rem;font-weight:500;letter-spacing:.25em;
  color:var(--orange-light);text-transform:uppercase;margin-top:-2px;
}
.search-wrap{
  flex:1 1 320px;
  position:relative;
  min-width:180px;
}
.search-wrap input{
  width:100%;padding:11px 44px 11px 16px;
  border-radius:999px;border:2px solid transparent;
  font-size:.92rem;outline:none;background:#fff;
  transition:border .15s;
}
.search-wrap input:focus{border-color:var(--orange);}
.search-wrap button{
  position:absolute;right:4px;top:4px;bottom:4px;
  width:38px;background:var(--orange);border-radius:999px;color:#fff;
  display:flex;align-items:center;justify-content:center;font-size:1rem;
}
.header-wsp{
  display:flex;align-items:center;gap:7px;background:var(--green);color:#fff;
  padding:9px 15px;border-radius:999px;font-size:.82rem;font-weight:700;flex:none;
  white-space:nowrap;transition:filter .15s;
}
.header-wsp:hover{filter:brightness(1.08);}
.header-wsp .icon{width:18px;height:18px;}
.header-wsp span{display:none;}
@media (min-width:520px){ .header-wsp span{display:inline;} }

/* ---------- NAV CATEGORIES ---------- */
nav.cat-nav{
  background:var(--black);
  border-bottom:1px solid #2a2a20;
  overflow-x:auto;
  white-space:nowrap;
  -ms-overflow-style:none;scrollbar-width:none;
}
nav.cat-nav::-webkit-scrollbar{display:none;}
.cat-nav-inner{max-width:1280px;margin:0 auto;display:flex;gap:2px;padding:0 10px;}
.cat-chip{
  color:#b9b9b0;font-weight:600;font-size:.8rem;
  padding:11px 15px;display:inline-block;border-bottom:2px solid transparent;
  transition:.15s;
}
.cat-chip.active,.cat-chip:hover{background:rgba(255,106,0,.1);border-bottom-color:var(--orange);color:#fff;}

/* ---------- MARQUEE TRUST BAR (pie de página) ---------- */
.marquee{
  background:var(--black);
  color:#cfcfc6;
  padding:8px 0;overflow:hidden;position:relative;
  font-size:.74rem;font-weight:600;letter-spacing:.02em;
}
.marquee-track{
  display:flex;gap:50px;white-space:nowrap;
  animation:scrollLeft 26s linear infinite;
  width:max-content;
}
@keyframes scrollLeft{0%{transform:translateX(0);}100%{transform:translateX(-50%);}}
.marquee-track span{display:flex;align-items:center;gap:7px;}
.marquee-track .icon{width:14px;height:14px;color:var(--orange-light);}

/* ---------- TRUST STRIP / TRANSPORTADORAS (parte inferior) ---------- */
.trust-strip{background:#fff;border-top:1px solid var(--gray-light);padding:22px 14px;margin-top:36px;}
.trust-strip-inner{max-width:1180px;margin:0 auto;display:grid;grid-template-columns:repeat(4,1fr);gap:16px;}
@media (max-width:700px){ .trust-strip-inner{grid-template-columns:1fr 1fr;} }
.ts-item{display:flex;align-items:center;gap:10px;}
.ts-item .icon{width:24px;height:24px;color:var(--orange);}
.ts-item b{display:block;font-size:.84rem;}
.ts-item span{font-size:.72rem;color:var(--gray);}
.carriers-block{max-width:1180px;margin:0 auto;padding:22px 14px 4px;text-align:center;}
.carriers-label{font-size:.74rem;color:var(--gray);margin:0 0 10px;letter-spacing:.06em;text-transform:uppercase;font-weight:700;}
.carriers-row{display:flex;justify-content:center;gap:10px;flex-wrap:wrap;}
.carrier-badge{border:1px solid var(--gray-light);border-radius:999px;padding:7px 16px;font-size:.78rem;font-weight:700;color:#333;background:#fafaf7;}
.carriers-mini{display:flex;align-items:center;gap:8px;font-size:.72rem;color:var(--gray);background:#f7f6f2;border-radius:8px;padding:9px 10px;margin-top:6px;}
.carriers-mini .icon{width:15px;height:15px;color:var(--orange);}

/* ---------- NOTIFICACIONES DE CONFIANZA ---------- */
.notif-host{position:fixed;bottom:88px;left:14px;z-index:85;display:flex;flex-direction:column;gap:8px;max-width:260px;}
.notif-toast{
  background:#fff;border:1px solid var(--gray-light);border-left:3px solid var(--orange);border-radius:10px;
  padding:10px 12px;display:flex;align-items:center;gap:8px;font-size:.76rem;font-weight:600;color:#222;
  box-shadow:0 10px 26px rgba(0,0,0,.14);opacity:0;transform:translateY(8px);transition:opacity .3s, transform .3s;
}
.notif-toast.show{opacity:1;transform:translateY(0);}
.notif-toast .icon{width:16px;height:16px;color:var(--orange);}
@media (max-width:600px){ .notif-host{left:10px;bottom:78px;max-width:220px;} }

/* ---------- HERO ---------- */
.hero{
  max-width:1280px;margin:18px auto;padding:0 14px;
}
.hero-banner{
  background:linear-gradient(120deg,var(--black) 55%,var(--orange-dark) 130%);
  border-radius:20px;padding:34px 30px;color:#fff;
  display:flex;align-items:center;justify-content:space-between;gap:20px;
  position:relative;overflow:hidden;
  box-shadow:var(--shadow);
}
.hero-banner::before{
  content:'';position:absolute;right:-60px;top:-60px;width:220px;height:220px;
  background:radial-gradient(circle,var(--orange) 0%,transparent 70%);
  opacity:.5;animation:pulseGlow 4s ease-in-out infinite;
}
@keyframes pulseGlow{0%,100%{transform:scale(1);opacity:.45;}50%{transform:scale(1.25);opacity:.7;}}
.hero-text h1{font-size:clamp(1.4rem,3.4vw,2.3rem);margin:0 0 8px;font-weight:800;line-height:1.15;}
.hero-text p{margin:0 0 16px;color:#e7e7de;font-size:.95rem;max-width:480px;}
.hero-badges{display:flex;gap:10px;flex-wrap:wrap;}
.hero-badge{
  background:rgba(255,255,255,.12);border:1px solid rgba(255,255,255,.25);
  padding:6px 12px;border-radius:999px;font-size:.72rem;font-weight:600;
  display:flex;align-items:center;gap:6px;
}
.hero-badge .icon{width:14px;height:14px;color:var(--orange-light);}
.hero-cta{
  background:var(--orange);color:#fff;font-weight:700;padding:13px 26px;
  border-radius:999px;font-size:.95rem;display:inline-flex;align-items:center;gap:8px;margin-top:14px;
  animation:pulseBtn 1.8s ease-in-out infinite;box-shadow:0 4px 14px rgba(255,106,0,.4);
}
.hero-cta .icon{width:18px;height:18px;}
@keyframes pulseBtn{0%,100%{transform:scale(1);}50%{transform:scale(1.045);}}

/* ---------- SECTION TITLES ---------- */
.section-title{
  max-width:1280px;margin:26px auto 12px;padding:0 14px;
  display:flex;align-items:center;justify-content:space-between;
}
.section-title h2{font-size:1.25rem;margin:0;font-weight:800;}
.section-title span{color:var(--orange);}
.section-sub{color:var(--gray);font-size:.82rem;margin:2px 0 0;}

/* ---------- PRODUCT GRID ---------- */
.grid{
  max-width:1280px;margin:0 auto;padding:0 14px 40px;
  display:grid;gap:16px;
  grid-template-columns:repeat(auto-fill,minmax(210px,1fr));
}
.card{
  background:#fff;border-radius:var(--radius);overflow:hidden;
  box-shadow:0 2px 10px rgba(20,20,15,.06);
  border:1px solid #eeece5;
  display:flex;flex-direction:column;
  transition:transform .18s, box-shadow .18s;
  position:relative;
}
.card:hover{transform:translateY(-4px);box-shadow:0 10px 26px rgba(20,20,15,.14);}
.card-img-wrap{position:relative;aspect-ratio:1/1;background:#f4f3ee;overflow:hidden;cursor:pointer;}
.card-img-wrap img{width:100%;height:100%;object-fit:cover;transition:transform .35s;}
.card:hover .card-img-wrap img{transform:scale(1.06);}
.badge{
  position:absolute;top:8px;left:8px;background:var(--orange);color:#fff;
  font-size:.68rem;font-weight:700;padding:4px 9px;border-radius:6px;
  box-shadow:0 2px 6px rgba(0,0,0,.2);
}
.badge.last{background:var(--black);top:34px;}
.badge.top{background:#111;top:8px;right:8px;left:auto;}
.card-body{padding:12px 12px 14px;display:flex;flex-direction:column;gap:6px;flex:1;}
.card-title{
  font-size:.86rem;font-weight:600;line-height:1.3;
  display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden;
  cursor:pointer;min-height:2.4em;
}
.card-title:hover{color:var(--orange-dark);}
.stars{color:#ffb400;font-size:.78rem;letter-spacing:1px;}
.stars .count{color:var(--gray);font-size:.72rem;margin-left:4px;letter-spacing:0;}
.price-row{display:flex;align-items:baseline;gap:8px;flex-wrap:wrap;}
.price-now{color:var(--orange-dark);font-weight:800;font-size:1.1rem;}
.price-old{color:#9c9c94;text-decoration:line-through;font-size:.78rem;}
.discount-tag{background:#fff0e6;color:var(--orange-dark);font-weight:700;font-size:.68rem;padding:2px 6px;border-radius:5px;}
.timer-row{
  font-size:.72rem;color:var(--orange-dark);font-weight:700;background:#fff4ea;
  padding:4px 8px;border-radius:6px;display:flex;align-items:center;gap:5px;
}
.btn{
  text-align:center;padding:10px 6px;border-radius:9px;font-size:.8rem;font-weight:700;
  display:flex;align-items:center;justify-content:center;gap:5px;transition:.15s;
}
.btn.full{width:100%;margin-top:2px;}
.btn-dark{background:var(--black);color:#fff;}
.btn-dark:hover{background:#000;}
.btn-orange{background:var(--orange);color:#fff;animation:btnShake 3.2s ease-in-out infinite;}
.btn-orange:hover{background:var(--orange-dark);animation:none;}
@keyframes btnShake{
  0%,84%{transform:translateX(0) scale(1);}
  86%{transform:translateX(-3px) scale(1.02);}
  88%{transform:translateX(3px) scale(1.02);}
  90%{transform:translateX(-3px) scale(1.02);}
  92%{transform:translateX(2px) scale(1.02);}
  94%{transform:translateX(0) scale(1.03);}
  100%{transform:translateX(0) scale(1);}
}
.sold-row{font-size:.7rem;color:var(--gray);}
.timer-row .icon{width:13px;height:13px;color:var(--orange-dark);}
.empty-ico{color:var(--gray);margin-bottom:8px;}
.empty-ico .icon{width:34px;height:34px;}

/* ---------- PRODUCT DETAIL ---------- */
.detail-wrap{max-width:1180px;margin:0 auto;padding:18px 14px 50px;}
.breadcrumb{font-size:.78rem;color:var(--gray);margin-bottom:14px;}
.breadcrumb a{color:var(--orange-dark);}
.detail-grid{display:grid;grid-template-columns:1fr 1fr;gap:36px;}
@media (max-width:860px){.detail-grid{grid-template-columns:1fr;gap:20px;}}
.gallery-main{
  aspect-ratio:1/1;border-radius:16px;overflow:hidden;background:#f4f3ee;
  border:1px solid #eeece5;position:relative;
}
.gallery-main img{width:100%;height:100%;object-fit:cover;cursor:zoom-in;}
.gallery-thumbs{display:flex;gap:8px;margin-top:10px;overflow-x:auto;}
.gallery-thumbs img{
  width:64px;height:64px;object-fit:cover;border-radius:8px;cursor:pointer;
  border:2px solid transparent;opacity:.7;flex:none;
}
.gallery-thumbs img.active{border-color:var(--orange);opacity:1;}
.detail-title{font-size:1.5rem;font-weight:800;margin:0 0 8px;line-height:1.25;}
.detail-meta{display:flex;align-items:center;gap:12px;flex-wrap:wrap;font-size:.85rem;color:var(--gray);margin-bottom:12px;}
.detail-price-block{
  background:#fff8f2;border:1px dashed var(--orange);border-radius:12px;padding:14px 16px;margin-bottom:14px;
}
.detail-price-row{display:flex;align-items:baseline;gap:12px;flex-wrap:wrap;}
.detail-price-now{font-size:2rem;font-weight:900;color:var(--orange-dark);}
.detail-price-old{font-size:1.1rem;color:#9c9c94;text-decoration:line-through;}
.savings{display:flex;align-items:center;gap:6px;font-size:.8rem;color:#1a8a4a;font-weight:700;margin-top:4px;}
.savings .icon{width:14px;height:14px;}
.detail-timer{
  display:inline-flex;align-items:center;gap:8px;background:var(--black);color:#fff;
  padding:8px 14px;border-radius:999px;font-size:.82rem;font-weight:700;margin:10px 0;
}
.detail-timer .icon{width:15px;height:15px;color:var(--orange-light);}
.detail-timer b{color:var(--orange-light);font-variant-numeric:tabular-nums;}
.trust-grid{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin:16px 0;}
.trust-item{
  display:flex;align-items:center;gap:8px;background:#fff;border:1px solid var(--gray-light);
  border-radius:10px;padding:9px 10px;font-size:.76rem;font-weight:600;color:#333;
}
.trust-item .icon{width:19px;height:19px;color:var(--orange);flex:none;}
.qty-row{display:flex;align-items:center;gap:14px;margin:14px 0;}
.qty-box{display:flex;align-items:center;border:1px solid var(--gray-light);border-radius:10px;overflow:hidden;}
.qty-box button{width:36px;height:36px;background:#f5f4ef;font-size:1.1rem;font-weight:700;}
.qty-box input{width:46px;text-align:center;border:none;font-size:.95rem;}
.cta-col{display:flex;flex-direction:column;gap:10px;}
.cta-big{
  padding:16px;border-radius:12px;font-size:1rem;font-weight:800;
  display:flex;align-items:center;justify-content:center;gap:10px;
}
.cta-whatsapp{background:var(--green);color:#fff;box-shadow:0 6px 18px rgba(37,211,102,.4);animation:btnShake 3.2s ease-in-out infinite;}
.cta-whatsapp .icon{width:20px;height:20px;}
.cta-buy{background:var(--orange);color:#fff;box-shadow:0 6px 18px rgba(255,106,0,.4);}
.cta-cart{background:var(--black);color:#fff;}
.share-row{display:flex;gap:10px;margin-top:6px;}
.share-btn{
  flex:1;border:1px solid var(--gray-light);border-radius:10px;padding:9px;text-align:center;font-size:.78rem;font-weight:700;background:#fff;color:#333;
  display:flex;align-items:center;justify-content:center;gap:6px;
}
.share-btn .icon{width:15px;height:15px;}
.share-btn:hover{border-color:var(--orange);color:var(--orange-dark);}

/* ---------- CALCULADORA DE ENTREGA ---------- */
.delivery-calc{background:#f7f6f2;border:1px solid var(--gray-light);border-radius:12px;padding:14px 16px;margin:14px 0;}
.delivery-calc label{display:block;font-size:.78rem;font-weight:700;margin-bottom:6px;}
.delivery-calc-row{display:flex;gap:8px;}
.delivery-calc-row input{flex:1;padding:10px 12px;border:1.5px solid var(--gray-light);border-radius:9px;font-size:.85rem;font-family:inherit;outline:none;}
.delivery-calc-row input:focus{border-color:var(--orange);}
.delivery-calc-row button{background:var(--black);color:#fff;padding:0 16px;border-radius:9px;font-size:.8rem;font-weight:700;white-space:nowrap;}
.delivery-result{margin-top:10px;font-size:.82rem;font-weight:700;display:none;align-items:center;gap:8px;padding:8px 10px;border-radius:8px;}
.delivery-result.show{display:flex;}
.delivery-result.main{background:#e9f9ee;color:#1a8a4a;}
.delivery-result.other{background:#fff4ea;color:var(--orange-dark);}
.delivery-result .icon{width:16px;height:16px;}

.desc-block{max-width:1180px;margin:30px auto;padding:0 14px;}
.desc-card{background:#fff;border:1px solid var(--gray-light);border-radius:16px;padding:22px 24px;}
.desc-card h3{margin:0 0 12px;font-size:1.1rem;}
.desc-line{display:flex;gap:10px;margin-bottom:10px;font-size:.92rem;line-height:1.55;}
.desc-line .em{font-size:1.15rem;}
.desc-line b{font-weight:700;}
.benefits-list{margin:10px 0 0;padding-left:0;list-style:none;}
.benefits-list li{
  display:flex;gap:8px;font-size:.9rem;margin-bottom:8px;line-height:1.4;
}
.benefits-list li::before{content:'✔';color:var(--orange);font-weight:900;}

.reviews-block{max-width:1180px;margin:0 auto 40px;padding:0 14px;}
.reviews-head{display:flex;align-items:center;justify-content:space-between;margin-bottom:14px;}
.review-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(260px,1fr));gap:14px;}
.review-card{background:#fff;border:1px solid var(--gray-light);border-radius:14px;padding:16px;}
.review-top{display:flex;align-items:center;gap:10px;margin-bottom:8px;}
.review-avatar{
  width:36px;height:36px;border-radius:50%;background:var(--orange);color:#fff;font-weight:800;
  display:flex;align-items:center;justify-content:center;font-size:.9rem;flex:none;
}
.review-name{font-weight:700;font-size:.86rem;}
.review-loc{font-size:.72rem;color:var(--gray);}
.review-text{font-size:.85rem;color:#333;line-height:1.45;}
.verified{font-size:.68rem;color:#1a8a4a;font-weight:700;margin-top:6px;display:flex;align-items:center;gap:4px;}
.verified .icon{width:13px;height:13px;}

.related-block{max-width:1280px;margin:0 auto 50px;padding:0 14px;}

/* ---------- FOOTER ---------- */
footer{background:var(--black);color:#d9d9d0;margin-top:40px;padding:40px 14px 20px;}
.footer-inner{max-width:1280px;margin:0 auto;display:grid;grid-template-columns:1.4fr 1fr 1fr 1fr;gap:28px;}
@media (max-width:760px){.footer-inner{grid-template-columns:1fr 1fr;}}
.footer-inner h4{color:#fff;font-size:.92rem;margin:0 0 12px;}
.footer-inner p,.footer-inner a{font-size:.8rem;color:#b9b9b0;line-height:1.7;display:block;}
.footer-inner a:hover{color:var(--orange-light);}
.foot-logo{font-weight:800;font-size:1.4rem;color:#fff;margin-bottom:8px;}
.foot-logo span{color:var(--orange);}
.carriers{display:flex;gap:10px;flex-wrap:wrap;margin-top:8px;}
.carrier-pill{background:#242419;color:#cfcfc6;font-size:.7rem;font-weight:700;padding:5px 10px;border-radius:999px;border:1px solid #33332a;}
.social-row{display:flex;gap:10px;margin-top:10px;}
.social-pill{
  width:38px;height:38px;border-radius:50%;background:#242419;display:flex;align-items:center;justify-content:center;
  border:1px solid #33332a;color:#e2e2d8;
}
.social-pill .icon{width:18px;height:18px;}
.social-pill:hover{background:var(--orange);border-color:var(--orange);color:#fff;}
.foot-bottom{
  max-width:1280px;margin:26px auto 0;padding-top:16px;border-top:1px solid #2a2a20;
  font-size:.72rem;color:#8c8c82;display:flex;justify-content:space-between;flex-wrap:wrap;gap:8px;
}

/* ---------- FLOATING BUTTONS ---------- */
.fab-whatsapp{
  position:fixed;bottom:20px;right:18px;z-index:80;
  width:56px;height:56px;background:var(--green);border-radius:50%;
  display:flex;align-items:center;justify-content:center;color:#fff;
  box-shadow:0 6px 18px rgba(0,0,0,.3);
  animation:whatsPulse 2s infinite;
}
.fab-whatsapp .icon{width:28px;height:28px;}
@keyframes whatsPulse{
  0%{box-shadow:0 0 0 0 rgba(37,211,102,.55);}
  70%{box-shadow:0 0 0 14px rgba(37,211,102,0);}
  100%{box-shadow:0 0 0 0 rgba(37,211,102,0);}
}
.fab-admin{
  position:fixed;bottom:20px;left:14px;z-index:80;
  width:26px;height:26px;border-radius:50%;background:rgba(20,20,15,.12);
  color:rgba(20,20,15,.35);font-size:.7rem;font-weight:800;
  display:flex;align-items:center;justify-content:center;
  transition:.2s;
}
.fab-admin:hover{background:var(--black);color:#fff;opacity:1;}
.fab-orders{
  position:fixed;bottom:52px;left:14px;z-index:80;
  width:26px;height:26px;border-radius:50%;background:rgba(20,20,15,.12);
  color:rgba(20,20,15,.35);font-size:.65rem;font-weight:800;
  display:flex;align-items:center;justify-content:center;
  transition:.2s;
}
.fab-orders:hover{background:var(--orange);color:#fff;opacity:1;}
.fab-ai{
  position:fixed;bottom:86px;right:18px;z-index:80;
  width:52px;height:52px;background:var(--black);border-radius:50%;
  display:flex;align-items:center;justify-content:center;color:#fff;
  box-shadow:0 6px 18px rgba(0,0,0,.3);
}
.fab-ai .icon{width:24px;height:24px;color:var(--orange-light);}
.fab-ai-label{
  position:absolute;right:60px;top:50%;transform:translateY(-50%);
  background:var(--black);color:#fff;font-size:.68rem;font-weight:700;
  padding:6px 10px;border-radius:8px;white-space:nowrap;opacity:0;pointer-events:none;transition:.2s;
}
.fab-ai:hover .fab-ai-label{opacity:1;}

/* ---------- MODALS ---------- */
.modal-overlay{
  position:fixed;inset:0;background:rgba(15,15,10,.55);z-index:200;
  display:flex;align-items:center;justify-content:center;padding:16px;
  backdrop-filter:blur(2px);
}
.modal{
  background:#fff;border-radius:16px;max-width:520px;width:100%;max-height:88vh;overflow-y:auto;
  padding:22px;position:relative;box-shadow:0 20px 60px rgba(0,0,0,.35);
}
.modal.wide{max-width:820px;}
.modal-close{
  position:absolute;top:14px;right:14px;width:30px;height:30px;border-radius:50%;background:#f2f1ec;
  display:flex;align-items:center;justify-content:center;font-size:1.1rem;color:#333;
}
.modal h3{margin:0 0 4px;font-size:1.15rem;}
.modal .sub{color:var(--gray);font-size:.8rem;margin-bottom:16px;}
.form-row{margin-bottom:12px;}
.form-row label{display:block;font-size:.78rem;font-weight:700;margin-bottom:5px;color:#333;}
.form-row input,.form-row select,.form-row textarea{
  width:100%;padding:10px 12px;border:1.5px solid var(--gray-light);border-radius:9px;font-size:.88rem;font-family:inherit;outline:none;
}
.form-row input:focus,.form-row select:focus,.form-row textarea:focus{border-color:var(--orange);}
.radio-group{display:flex;gap:10px;flex-wrap:wrap;}
.radio-opt{
  flex:1;min-width:140px;border:1.5px solid var(--gray-light);border-radius:10px;padding:10px 12px;
  display:flex;align-items:center;gap:8px;cursor:pointer;font-size:.82rem;font-weight:600;
}
.radio-opt input{width:auto;}
.radio-opt.checked{border-color:var(--orange);background:#fff8f2;}
.modal-submit{
  width:100%;padding:14px;background:var(--green);color:#fff;font-weight:800;border-radius:11px;font-size:.95rem;
  display:flex;align-items:center;justify-content:center;gap:8px;margin-top:6px;
}
.modal-submit:disabled{opacity:.6;}
.summary-box{background:#f7f6f2;border-radius:10px;padding:12px 14px;font-size:.82rem;margin-bottom:14px;display:flex;gap:12px;align-items:center;}
.summary-box img{width:52px;height:52px;object-fit:cover;border-radius:8px;flex:none;}

/* admin */
.admin-list{display:flex;flex-direction:column;gap:8px;max-height:60vh;overflow-y:auto;}
.admin-row{
  display:flex;align-items:center;gap:10px;border:1px solid var(--gray-light);border-radius:10px;padding:8px;
}
.admin-row img{width:44px;height:44px;object-fit:cover;border-radius:6px;flex:none;}
.admin-row .info{flex:1;min-width:0;}
.admin-row .info b{display:block;font-size:.8rem;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;}
.admin-row .info small{color:var(--gray);font-size:.72rem;}
.admin-row button{background:var(--black);color:#fff;font-size:.7rem;padding:6px 10px;border-radius:7px;font-weight:700;}
.admin-row button.del{background:#c0392b;}
.admin-actions-top{display:flex;gap:8px;margin-bottom:12px;}
.admin-actions-top button{flex:1;background:var(--orange);color:#fff;padding:10px;border-radius:9px;font-weight:700;font-size:.82rem;}
.img-chip-list{display:flex;flex-wrap:wrap;gap:8px;margin-bottom:8px;}
.img-chip{position:relative;width:56px;height:56px;border-radius:8px;overflow:hidden;border:1px solid var(--gray-light);}
.img-chip img{width:100%;height:100%;object-fit:cover;}
.img-chip .rm{position:absolute;top:0;right:0;background:#c0392b;color:#fff;width:16px;height:16px;font-size:.6rem;display:flex;align-items:center;justify-content:center;}
.toast{
  position:fixed;bottom:90px;left:50%;transform:translateX(-50%);background:var(--black);color:#fff;
  padding:10px 18px;border-radius:999px;font-size:.82rem;font-weight:600;z-index:300;box-shadow:0 6px 20px rgba(0,0,0,.3);
  opacity:0;transition:opacity .25s;
}
.toast.show{opacity:1;}

/* pedidos (orders admin) */
.order-card{border:1px solid var(--gray-light);border-radius:12px;padding:12px 14px;margin-bottom:10px;background:#fff;}
.order-card-head{display:flex;justify-content:space-between;align-items:flex-start;gap:10px;margin-bottom:8px;}
.order-card-head b{font-size:.9rem;}
.order-card-head .date{font-size:.7rem;color:var(--gray);}
.order-line{font-size:.8rem;color:#333;margin-bottom:3px;line-height:1.4;}
.order-line b{font-weight:700;}
.order-status{display:inline-block;font-size:.68rem;font-weight:700;padding:3px 9px;border-radius:999px;}
.order-status.pendiente{background:#fff4ea;color:var(--orange-dark);}
.order-status.entregado{background:#e9f9ee;color:#1a8a4a;}
.order-status.cancelado{background:#fbe9e7;color:#c0392b;}
.order-actions{display:flex;gap:6px;margin-top:8px;flex-wrap:wrap;}
.order-actions button{font-size:.68rem;padding:5px 9px;border-radius:6px;font-weight:700;background:#f2f1ec;color:#333;}
.order-actions button.active{background:var(--black);color:#fff;}
.orders-summary{display:flex;gap:8px;margin-bottom:14px;flex-wrap:wrap;}
.orders-summary .pill{background:#f7f6f2;border-radius:999px;padding:7px 13px;font-size:.75rem;font-weight:700;color:#333;}
.orders-empty{text-align:center;padding:30px;color:var(--gray);font-size:.85rem;}

/* asistente IA */
.ai-chat-body{max-height:340px;overflow-y:auto;display:flex;flex-direction:column;gap:10px;padding:4px 2px;margin-bottom:12px;}
.ai-msg{max-width:85%;padding:10px 13px;border-radius:14px;font-size:.85rem;line-height:1.45;}
.ai-msg.bot{background:#f2f1ec;align-self:flex-start;border-bottom-left-radius:4px;}
.ai-msg.user{background:var(--orange);color:#fff;align-self:flex-end;border-bottom-right-radius:4px;}
.ai-msg.bot .mini-product{display:flex;gap:8px;align-items:center;background:#fff;border:1px solid var(--gray-light);border-radius:9px;padding:6px;margin-top:8px;cursor:pointer;}
.ai-msg.bot .mini-product img{width:38px;height:38px;object-fit:cover;border-radius:6px;flex:none;}
.ai-msg.bot .mini-product .mp-name{font-size:.75rem;font-weight:600;line-height:1.2;}
.ai-msg.bot .mini-product .mp-price{font-size:.75rem;color:var(--orange-dark);font-weight:800;}
.ai-input-row{display:flex;gap:8px;}
.ai-input-row input{flex:1;padding:11px 13px;border:1.5px solid var(--gray-light);border-radius:999px;font-size:.85rem;outline:none;}
.ai-input-row input:focus{border-color:var(--orange);}
.ai-input-row button{width:42px;height:42px;border-radius:50%;background:var(--orange);color:#fff;display:flex;align-items:center;justify-content:center;flex:none;}
.ai-suggest-row{display:flex;gap:6px;flex-wrap:wrap;margin-bottom:10px;}
.ai-suggest-chip{background:#fff;border:1px solid var(--gray-light);border-radius:999px;padding:5px 11px;font-size:.72rem;font-weight:600;color:#333;}
.ai-suggest-chip:hover{border-color:var(--orange);color:var(--orange-dark);}
.ai-typing span{display:inline-block;width:5px;height:5px;background:#999;border-radius:50%;margin-right:3px;animation:aiTyping 1s infinite;}
.ai-typing span:nth-child(2){animation-delay:.15s;}
.ai-typing span:nth-child(3){animation-delay:.3s;}
@keyframes aiTyping{0%,60%,100%{opacity:.3;}30%{opacity:1;}}

.empty-state{text-align:center;padding:60px 20px;color:var(--gray);}
.spinner-row{display:flex;justify-content:center;padding:40px;}

@media (max-width:600px){
  .logo{font-size:1.15rem;}
  .logo small{font-size:.48rem;}
  .header-inner{gap:10px;}
  .header-actions{gap:8px;}
  .header-actions a{font-size:.68rem;}
  .search-wrap{order:3;flex:1 1 100%;}
  .grid{grid-template-columns:repeat(2,1fr);gap:10px;}
  .hero-banner{flex-direction:column;text-align:left;padding:22px 18px;}
  .hero-text p{font-size:.85rem;}
  .detail-price-now{font-size:1.6rem;}
  .trust-grid{grid-template-columns:1fr;}
  .footer-inner{grid-template-columns:1fr 1fr;}
  .modal{padding:18px;}
}
@media (max-width:380px){
  .grid{grid-template-columns:1fr 1fr;gap:8px;}
  .card-body{padding:9px 9px 11px;}
}

</style>
</head>
<body>
<div id="app">
  <div class="spinner-row">Cargando Trogüi...</div>
</div>

<script>
const RAW_PRODUCTS = [
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
   desc:'Freidora de aire X HOME con extra capacidad 12L. Cocina más fácil, rápido y saludable con hasta 80% menos aceite. Panel moderno e intuitivo. Cocción rápida y uniforme. Incluye accesorios. Ideal para familias. Perfecto para papas, alitas, empanadas, pizzas y mucho más.',
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
  {id:'T032',name:'Parlante JBL Boombox 3 Mini LED',cat:'tecnologia',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/827576/1714766066425321695_7609998525712221_4306800719508153007_n.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/827576/171476606615a438cb39617cc026517efb13949d88.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/827576/1714766066427540955_7456219337747742_1902590583006082060_n.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/827576/1714766066421837815_6940456066081576_2793123522810349384_n.jpg'
],
price:89000,oldPrice:169000,
desc:'Disfruta un sonido potente con bajos profundos y luces LED que siguen el ritmo de la música. Ideal para reuniones, fiestas, paseos y uso diario. Conexión Bluetooth rápida, diseño portátil y batería recargable para llevar la diversión a cualquier lugar.',
sold:184,stars:5,lastUnits:false,timer:3*60*60},

{id:'T033',name:'Parlante JBL Wind 3 Portátil',cat:'tecnologia',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1618784/1736435001WhatsApp%20Image%202025-01-09%20at%2010.00.48%20AM%20(1).jpeg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1618784/1736435000WhatsApp%20Image%202025-01-09%20at%2010.00.51%20AM.jpeg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1618784/1736435000WhatsApp%20Image%202025-01-09%20at%2010.00.51%20AM%20(2).jpeg'
],
price:55000,oldPrice:119000,
desc:'Perfecto para bicicleta, moto o caminatas. Incluye Bluetooth, radio FM, entrada auxiliar y reproducción por microSD. Resistente a salpicaduras y fácil de instalar. Lleva tu música favorita a cualquier aventura.',
sold:223,stars:5,lastUnits:false,timer:2*60*60},

{id:'T034',name:'Parlante JBL Flip 6 Con Marquilla',cat:'tecnologia',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2133937/1776781569Captura%20de%20pantalla%202026-04-21%20092329.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2133937/1776781569Imagen%20de%20WhatsApp%202024-12-20%20a%20las%2015.00.38_6450639f%20(1).jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2133937/1776781569WhatsApp%20Image%202025-08-19%20at%2010.38.44%20AM%20(1).jpeg'
],
price:65000,oldPrice:139000,
desc:'Sonido potente y diseño moderno para disfrutar música en cualquier lugar. Conexión Bluetooth estable, batería recargable y excelente calidad de audio para reuniones, oficina o entretenimiento diario.',
sold:157,stars:5,lastUnits:false,timer:2*60*60},

{id:'T035',name:'Parlante JBL Charge 5',cat:'tecnologia',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/675632/1708974851photo_5089455367687089337_x%20(1).jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1616579/1736272346image%20(4).png',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/675632/1708974851photo_5089455367687089390_y.jpg'
],
price:63000,oldPrice:129000,
desc:'Potencia, portabilidad y autonomía en un solo equipo. Ideal para quienes buscan un parlante compacto con gran volumen y sonido envolvente para fiestas, viajes o uso diario.',
sold:245,stars:5,lastUnits:false,timer:4*60*60},

{id:'T036',name:'Consola Q9 Pro Retro',cat:'tecnologia',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1974861/17614359421.webp',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1974861/17614359423.webp'
],
price:169000,oldPrice:289000,
desc:'Con miles de juegos clásicos incluidos, controles inalámbricos y salida HDMI, esta consola es perfecta para disfrutar en familia. Revive la nostalgia y diviértete durante horas sin necesidad de internet.',
sold:132,stars:5,lastUnits:false,timer:5*60*60},

{id:'T037',name:'Consola Retro 10000 Juegos 4K',cat:'tecnologia',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/355902/17018761741701876174da165ae2e8f6121968db11c04c1586f6-product.jpeg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1202261/1760218038Dise%C3%B1o%20sin%20t%C3%ADtulo%20-%202025-08-13T111659.315.png'
],
price:69000,oldPrice:149000,
desc:'Más de 10.000 juegos clásicos en una sola consola. Incluye dos controles inalámbricos para jugar con amigos o familiares. Compatible con televisores mediante HDMI y calidad de imagen 4K.',
sold:311,stars:5,lastUnits:false,timer:3*60*60},

{id:'T038',name:'Termo Premium 3 En 1',cat:'hogar',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1223914/1726847960termo3.webp',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1223914/1726847960451034626_18030781265116909_6319577442867853304_n.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1223914/1726847960termo33.webp'
],
price:49000,oldPrice:99000,
desc:'Mantén tus bebidas frías o calientes por más tiempo. Diseño elegante, práctico y resistente para oficina, gimnasio, universidad o viajes. Ideal para quienes buscan comodidad todos los días.',
sold:287,stars:5,lastUnits:false,timer:2*60*60},

{id:'T039',name:'Depilador Recargable',cat:'salud',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1884098/1753379889depilador.JPG'
],
price:39000,oldPrice:79000,
desc:'Elimina el vello de forma rápida, cómoda y sin irritaciones. Diseño compacto y recargable para usar en casa o llevar de viaje. Ideal para mantener una apariencia impecable en minutos.',
sold:176,stars:5,lastUnits:false,timer:2*60*60},

{id:'T040',name:'Filtro Universal Para Ducha',cat:'hogar',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1876903/1752676012filtro%20de%20ducha%20universal.JPG'
],
price:55000,oldPrice:110000,
desc:'Ayuda a reducir cloro, impurezas y malos olores del agua. Protege tu piel y cabello mientras disfrutas de una ducha más saludable. Fácil instalación compatible con la mayoría de duchas estándar.',
sold:198,stars:5,lastUnits:false,timer:3*60*60},

{id:'T041',name:'Lámpara Solar 50W',cat:'hogar',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1209291/1740405054lampara%20sola%2050w%20gd.JPG'
],
price:59900,oldPrice:129900,
desc:'Ilumina patios, terrazas, fincas y exteriores sin aumentar el consumo de energía. Funciona con energía solar, brinda excelente iluminación nocturna y es resistente para uso exterior.',
sold:165,stars:5,lastUnits:false,timer:2*60*60},

{id:'T042',name:'Cámara Digital Para Niños',cat:'juguetes',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1584177/1734034325IMG_6987.JPG',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1584177/1734034325IMG_6988.JPG'
],
price:49000,oldPrice:99000,
desc:'Estimula la creatividad de los niños permitiéndoles tomar fotos y grabar videos fácilmente. Resistente, segura y divertida. Un regalo ideal para desarrollar imaginación y aprendizaje.',
sold:224,stars:5,lastUnits:false,timer:3*60*60},

{id:'T043',name:'Almohada Ortopédica Premium',cat:'salud',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/655374/1729089926ALMOHADA.webp',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/655374/1729089926ALMOHADA%20ORTOPEDICA223.webp'
],
price:45000,oldPrice:95000,
desc:'Diseñada para brindar soporte cervical y mejorar la postura al dormir. Ayuda a disminuir molestias en cuello y espalda, proporcionando un descanso más cómodo y reparador.',
sold:354,stars:5,lastUnits:false,timer:2*60*60},

{id:'T044',name:'Ejercitador De Manos Ajustable',cat:'salud',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/323974/17018817971701881797D_NQ_NP_646020-MCO70479652653_072023-O.jpeg'
],
price:28000,oldPrice:59000,
desc:'Fortalece dedos, manos y antebrazos. Ideal para deportistas, músicos, rehabilitación física o personas que desean mejorar fuerza y resistencia de agarre.',
sold:173,stars:5,lastUnits:false,timer:60*60},

{id:'T045',name:'Rodillera De Compresión',cat:'salud',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/587016/1704688558rodillera.jpeg'
],
price:29000,oldPrice:59000,
desc:'Brinda soporte y estabilidad durante caminatas, ejercicio o actividades diarias. Ayuda a reducir molestias articulares y mejora la sensación de seguridad al moverte.',
sold:191,stars:5,lastUnits:false,timer:60*60},

{id:'T046',name:'Masajeador Facial Antiarrugas',cat:'belleza',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1243990/17272726811718573660MASAJEADOR%20FACIAL.jpeg'
],
price:49000,oldPrice:99000,
desc:'Ayuda a mejorar la apariencia de la piel mediante suaves vibraciones que favorecen la relajación facial. Ideal para complementar tu rutina de cuidado personal desde casa.',
sold:145,stars:5,lastUnits:false,timer:2*60*60},

{id:'T047',name:'Maletín Antirrobo Impermeable',cat:'accesorios',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/870258/1716052118maleta%20manos%20Libres.JPG',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/870258/1766246446Mochila%20Cruzada%20Impermeable%20Antirrobo%20-%20Carga%20USB%20ND.jpg'
],
price:55000,oldPrice:119000,
desc:'Protege tus pertenencias con un diseño moderno, impermeable y resistente. Cuenta con múltiples compartimentos para organizar celular, billetera, llaves y accesorios de forma segura.',
sold:278,stars:5,lastUnits:false,timer:3*60*60},

{id:'T048',name:'Reloj Despertador Con Proyector LED',cat:'hogar',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2160113/1779813291RELOJ%20PROYECTOR%20LED%208.JPG',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2160113/1779813291RELOJ%20PROYECTOR%20LED%2014.jpg'
],
price:55000,oldPrice:119000,
desc:'Visualiza la hora proyectada en techo o pared sin levantarte de la cama. Incluye temperatura, humedad y pantalla LED de fácil lectura. Perfecto para dormitorios modernos.',
sold:169,stars:5,lastUnits:false,timer:2*60*60},

{id:'T049',name:'Maleta Cabina De Viaje',cat:'viajes',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1358873/1741453295Maleta%20Amazon%20Con%20Zapatero%20Gris%20A.JPG',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1358873/1741453295Maleta%20Amazon%20Con%20Zapatero%20Lila%206.jpg'
],
price:89000,oldPrice:169000,
desc:'Ideal para viajes cortos, gimnasio o escapadas de fin de semana. Amplio espacio interior, compartimentos funcionales y diseño elegante para llevar todo organizado.',
sold:144,stars:5,lastUnits:false,timer:3*60*60},

{id:'T050',name:'Molino Eléctrico Multiusos',cat:'hogar',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1918942/1757248815IMG_0493.jpeg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2148755/1778530520Molinillo%20de%20caf%C3%A9%20el%C3%A9ctrico%20de%20cocina%20Grande%202.jpg'
],
price:49900,oldPrice:99900,
desc:'Muele café, especias, semillas y otros ingredientes en segundos. Potente, compacto y fácil de usar. Perfecto para quienes disfrutan preparar alimentos frescos en casa.',
sold:188,stars:5,lastUnits:false,timer:2*60*60},

{id:'T051',name:'Organizador Para Lavadora',cat:'hogar',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/337207/17018798431701879843WhatsApp%20Image%202023-07-31%20at%208.15.30%20PM.jpeg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/591719/1704992977ORGANIZADOR%20LAVADORA..jpg'
],
price:79000,oldPrice:149000,
desc:'Aprovecha el espacio sobre la lavadora y mantén detergentes, suavizantes y accesorios siempre organizados. Ideal para baños y zonas de lavado pequeñas.',
sold:152,stars:5,lastUnits:false,timer:3*60*60},
  {id:'T029',name:'Kit Máquina Afeitadora para Mascotas',cat:'accesorios',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1942148/17591538771992f34d9d2-electrohogarcyc-gneuklg0t7n-iest5inm75d.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1942148/17591538771992f34e3e7-electrohogarcyc-gneuklg0t7n-bteqsvyf7nu.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1942148/17591538771992f34d56e-electrohogarcyc-gneuklg0t7n-3nqhgzuzcf.jpg'],
   price:59000,oldPrice:105000,
   desc:'Kit completo para peluquería de mascotas en casa. Silencioso para no asustar a tu perro o gato. Cuchillas de acero inoxidable ajustables. Recargable USB. Incluye accesorios para diferentes longitudes de pelo. Ahorra en peluquería y cuida a tu mascota con amor.',
   sold:142,stars:5,lastUnits:false,timer:60*60},
  {id:'T052',name:'Estufa Eléctrica Doble Puesto',cat:'hogar',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2031440/1767718572Haac6d35fa02d468eb197d8b2a91bd799Y.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2002901/1763821917D_NQ_NP_2X_833686-MCO79108625469_092024-F.webp',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1646802/1738172135estufas.webp'
],
price:65000,oldPrice:129000,
desc:'Cocina de forma rápida y práctica sin necesidad de gas. Cuenta con dos puestos para preparar varias recetas al mismo tiempo. Ideal para apartamentos, oficinas, fincas o estudiantes.',
sold:247,stars:5,lastUnits:false,timer:3*60*60},

{id:'T053',name:'Estufa Eléctrica Un Puesto',cat:'hogar',
imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2129027/1776178830estu.webp'],
price:49000,oldPrice:99000,
desc:'Solución práctica para cocinar en espacios reducidos. Compacta, fácil de transportar y perfecta para apartamentos, habitaciones, oficinas o viajes.',
sold:196,stars:5,lastUnits:false,timer:2*60*60},

{id:'T054',name:'Buzo Colombia Mundial Cuello Alto',cat:'ropa',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2160515/1779829600COOMBIA%20AMARILLO%20NUEVO.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2160515/1779829600COOMBIA%20NEGRO%20NUEVO.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2160515/1779829600COOMBIA%20azul%20oscuroNUEVO.jpg'
],
price:115000,oldPrice:199000,
desc:'Chaqueta premium inspirada en la Selección Colombia. Fabricada en tela de excelente calidad, cuello alto, cremallera completa y tallas para hombre y mujer. Ideal para lucir la pasión por Colombia con estilo.',
sold:312,stars:5,lastUnits:false,timer:4*60*60},

{id:'T055',name:'Buzo Junior FC',cat:'ropa',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2080820/17707696941000000157.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2080820/17707696941000000156.jpg'
],
price:95000,oldPrice:169000,
desc:'Diseño deportivo cómodo y moderno para los verdaderos hinchas del Junior. Perfecto para uso diario, eventos deportivos o regalar a un apasionado del fútbol.',
sold:154,stars:5,lastUnits:false,timer:2*60*60},

{id:'T056',name:'Buzo Deportivo Cali Bordado',cat:'ropa',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2044517/1769109981WhatsApp%20Image%202026-01-15%20at%202.57.16%20PM.jpeg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2044517/1769109984WhatsApp%20Image%202026-01-15%20at%202.57.15%20PM.jpeg'
],
price:115000,oldPrice:199000,
desc:'Buzo premium bordado para los seguidores del Deportivo Cali. Confección cómoda, excelente acabado y diseño elegante para demostrar tu pasión verdiblanca.',
sold:142,stars:5,lastUnits:false,timer:3*60*60},

{id:'T057',name:'Buzo Millonarios FC',cat:'ropa',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2080700/1770761411MILLONARIOS%201.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2080700/1770761411MILLONARIOS%203.jpg'
],
price:115000,oldPrice:199000,
desc:'Prenda deportiva diseñada para los aficionados embajadores. Tela cómoda, excelente calidad y acabados modernos para cualquier ocasión.',
sold:201,stars:5,lastUnits:false,timer:3*60*60},

{id:'T058',name:'Buzo América De Cali',cat:'ropa',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1836238/1748668187AMERICA.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1836238/1748668186ROJO.jpg'
],
price:115000,oldPrice:199000,
desc:'Lleva con orgullo los colores de La Mechita. Diseño moderno, cómodo y perfecto para acompañarte en cualquier momento del día.',
sold:263,stars:5,lastUnits:false,timer:4*60*60},

{id:'T059',name:'Saco América De Cali Premium',cat:'ropa',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1735937/1770477714AMERICA%20RAMON%20GARRA%204.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1735937/1770477714COLLAGE%20AMERICA.jpg'
],
price:95000,oldPrice:169000,
desc:'La pasión de un pueblo reflejada en una prenda cómoda y elegante. Ideal para hinchas que quieren representar al América dentro y fuera del estadio.',
sold:174,stars:5,lastUnits:false,timer:2*60*60},

{id:'T060',name:'Buzo Atlético Nacional',cat:'ropa',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1666448/1763070522NACIONAL%20RAMON%20VERTICAL%204.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1669284/1763069456collage%203.jpg'
],
price:95000,oldPrice:179000,
desc:'Diseñado para los verdaderos verdolagas. Cómodo, resistente y con acabados de alta calidad para acompañarte durante todo el año.',
sold:286,stars:5,lastUnits:false,timer:3*60*60},

{id:'T061',name:'Buzo Independiente Medellín',cat:'ropa',
imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1851963/1750177022WhatsApp%20Image%202025-06-17%20at%2010.41.38.jpeg'],
price:115000,oldPrice:199000,
desc:'Representa al Poderoso de la Montaña con una prenda deportiva cómoda, moderna y perfecta para cualquier ocasión.',
sold:135,stars:5,lastUnits:false,timer:2*60*60},

{id:'T062',name:'Buzo Once Caldas',cat:'ropa',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2077063/1775406122NEUMO%20ONCE%20CALDAS%201.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2077063/1775406123NEUMO%20ONCE%20CALDAS%203.jpg'
],
price:115000,oldPrice:199000,
desc:'Diseño exclusivo inspirado en uno de los equipos históricos del fútbol colombiano. Cómodo, elegante y de excelente calidad.',
sold:117,stars:5,lastUnits:false,timer:2*60*60},

{id:'T063',name:'Buzo Once Caldas Bordado',cat:'ropa',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1822990/1747409041ONCE-Photoroom.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1822990/1747409041WhatsApp%20Image%202025-05-15%20at%2018.11.49%20(1).jpeg'
],
price:95000,oldPrice:169000,
desc:'Acabados bordados premium y diseño elegante para quienes viven la pasión del Once Caldas todos los días.',
sold:121,stars:5,lastUnits:false,timer:2*60*60},

{id:'T064',name:'Buzo Colombia Petróleo',cat:'ropa',
imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2134937/1776822875WhatsApp%20Image%202026-04-21%20at%208.44.57%20PM.jpeg'],
price:115000,oldPrice:199000,
desc:'Edición especial con diseño moderno y colores llamativos. Ideal para fanáticos de la Selección Colombia que buscan destacar.',
sold:164,stars:5,lastUnits:false,timer:3*60*60},

{id:'T065',name:'Toldillo Plegable',cat:'bebes',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2147859/1778344866Toldillo-Plegable-BebeAzul3.webp',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1593349/1734472536IMG-20241216-WA0045.jpg'
],
price:49000,oldPrice:99000,
desc:'Protege a tu bebé de mosquitos e insectos mientras duerme. Diseño plegable, liviano y fácil de transportar para usar en casa o viajes.',
sold:238,stars:5,lastUnits:false,timer:2*60*60},

{id:'T066',name:'Toldillo Para Bebés',cat:'bebes',
imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/921828/171900446117018815061701881506toldillo-mosquitero-bebes-cuna-plegable-cama-portatil-312012-importadora-blue-353152921_1200x1200.jpeg'],
price:59900,oldPrice:119900,
desc:'Brinda tranquilidad y protección mientras tu bebé descansa. Fácil de instalar y compatible con diferentes tipos de cunas.',
sold:207,stars:5,lastUnits:false,timer:2*60*60},

{id:'T067',name:'Silla Mecedora Para Bebé',cat:'bebes',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2015545/1764878056WhatsApp%20Image%202025-12-03%20at%2010.58.48%20AM.jpeg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2092041/1771882063mecedora%203.jpg'
],
price:119000,oldPrice:219000,
desc:'Ayuda a relajar y entretener al bebé gracias a su suave movimiento. Cómoda, segura y perfecta para los primeros meses de crecimiento.',
sold:148,stars:5,lastUnits:false,timer:3*60*60},

{id:'T068',name:'Juego De Ollas Premium',cat:'hogar',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2041825/1768875446w=1200,h=1200,fit=pad%20(12).webp',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1817856/1747071190Imagen%20de%20WhatsApp%202025-05-12%20a%20las%2012.31.21_2cd5bc55.jpg'
],
price:69900,oldPrice:149900,
desc:'Renueva tu cocina con un juego completo de ollas resistentes y elegantes. Distribuyen el calor uniformemente para cocinar de manera más eficiente.',
sold:293,stars:5,lastUnits:false,timer:3*60*60},

{id:'T069',name:'Sellador Y Cortador De Bolsas',cat:'hogar',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1960353/176014278933ea0d74-e47f-4d51-bcdf-9d1d818534f5.JPG',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2013355/1764696875bol.webp'
],
price:32000,oldPrice:69000,
desc:'Mantén tus alimentos frescos por más tiempo sellando bolsas en segundos. Fácil de usar, portátil y perfecto para la cocina diaria.',
sold:354,stars:5,lastUnits:false,timer:60*60},

{id:'T070',name:'Utensilio Multifuncional Cocina',cat:'hogar',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1515374/17485563742.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2126664/1775837217cocina.webp'
],
price:75000,oldPrice:139000,
desc:'Herramienta práctica que facilita múltiples tareas en la cocina. Ahorra tiempo y mejora la preparación de tus recetas favoritas.',
sold:138,stars:5,lastUnits:false,timer:2*60*60},
  {id:'T072',name:'Juego de Ollas Antiadherentes Premium',cat:'hogar',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2041825/1768875446w=1200,h=1200,fit=pad%20(12).webp','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1817856/1747071190Imagen%20de%20WhatsApp%202025-05-12%20a%20las%2012.31.21_2cd5bc55.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2041825/1768875445w=1200,h=1200,fit=pad%20(10).webp'],
 price:69900,oldPrice:139000,
 desc:'Renueva tu cocina con este completo juego de ollas antiadherentes. Distribuyen el calor de forma uniforme, reducen el consumo de aceite y facilitan la limpieza. Ideales para preparar tus recetas favoritas de manera rápida y práctica. Resistentes, elegantes y perfectas para el uso diario.',
 sold:201,stars:5,lastUnits:false,timer:3*60*60},

{id:'T073',name:'Sellador y Cortador de Bolsas Portátil',cat:'hogar',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1960353/176014278933ea0d74-e47f-4d51-bcdf-9d1d818534f5.JPG','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2013355/1764696875bol.webp'],
 price:32000,oldPrice:69000,
 desc:'Mantén tus alimentos frescos por más tiempo. Este práctico sellador y cortador portátil evita desperdicios, conserva snacks, arroz, café y mucho más. Funciona en segundos y ocupa muy poco espacio. Ideal para hogares organizados y ahorradores.',
 sold:263,stars:5,lastUnits:false,timer:2*60*60},

{id:'T074',name:'Utensilio Multifuncional de Cocina',cat:'hogar',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1515374/17485563742.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2126664/1775837217cocina.webp'],
 price:75000,oldPrice:129000,
 desc:'Herramienta versátil diseñada para facilitar múltiples tareas en la cocina. Ahorra tiempo en la preparación de alimentos y mejora la organización de tus espacios. Resistente, fácil de limpiar y perfecta para cualquier hogar moderno.',
 sold:116,stars:5,lastUnits:false,timer:2*60*60},

{id:'T075',name:'Organizador Metálico para Cocina',cat:'hogar',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2159999/1779807048ORGANIZADOR%20METALICO%20DE%20COCINA%201.webp','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1085959/1723832912WhatsApp%20Image%202024-08-16%20at%2012.58.33%20PM.jpeg'],
 price:42000,oldPrice:79000,
 desc:'Aprovecha el espacio de tus paredes y mantén utensilios, cucharas y accesorios siempre organizados. Diseño resistente y elegante que ayuda a mantener la cocina ordenada y funcional. Fácil instalación y gran capacidad.',
 sold:171,stars:5,lastUnits:false,timer:60*60},

{id:'T076',name:'Set de Utensilios de Cocina 12 Piezas',cat:'hogar',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/377463/17018734491701873449Utensilio-de-cocina-12pz-Verde-1.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/377463/17018734491701873449Utensilio-de-cocina-12pz-Rojo-2.jpg'],
 price:49900,oldPrice:99000,
 desc:'Set completo de utensilios de silicona resistente al calor con elegantes mangos de madera. No raya ollas ni sartenes, es fácil de limpiar y aporta un toque moderno a tu cocina. Incluye soporte organizador para mantener todo en su lugar.',
 sold:312,stars:5,lastUnits:false,timer:3*60*60},

{id:'T077',name:'Gorro Terapéutico para Migraña y Dolor de Cabeza',cat:'salud',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/656487/1708057119WhatsApp%20Image%202023-08-29%20at%206.27.56%20PM%20(1).jpeg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/926788/171943595358b7d2b7-f548-4f85-9eaa-82dbfefe3d98.jpeg'],
 price:35000,oldPrice:69000,
 desc:'Alivio relajante para migrañas, estrés, cansancio visual y dolores de cabeza. Puede utilizarse frío o tibio para brindar una sensación inmediata de bienestar. Su diseño cómodo cubre completamente la zona afectada y ayuda a relajarte en minutos.',
 sold:289,stars:5,lastUnits:false,timer:60*60},

{id:'T078',name:'Radios Comunicadores Baofeng X2',cat:'tecnologia',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2034990/1768246197IMG_0355.jpeg'],
 price:75000,oldPrice:149000,
 desc:'Comunicación clara y estable para trabajo, seguridad, fincas, viajes y actividades al aire libre. Incluye dos radios, cargadores, auriculares y accesorios completos. Excelente alcance y batería de larga duración para mantenerte siempre conectado.',
 sold:152,stars:5,lastUnits:false,timer:3*60*60},

{id:'T079',name:'Sofá Inflable Portátil',cat:'hogar',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2130523/1776346965sofa%201.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2130523/1776346965SOFA%20AZUL.jpeg'],
 price:79000,oldPrice:149000,
 desc:'Descansa cómodamente en la playa, camping, parque o jardín. Se infla rápidamente y ofrece gran comodidad sin necesidad de muebles pesados. Ligero, resistente y fácil de transportar a cualquier lugar.',
 sold:136,stars:5,lastUnits:false,timer:2*60*60},

{id:'T080',name:'Destornillador Eléctrico Inalámbrico',cat:'herramientas',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1750036/1744224377DESTOR.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1750036/1768490298photo_2026-01-05_14-52-13.jpg'],
 price:49000,oldPrice:99000,
 desc:'Ideal para reparaciones en el hogar, muebles y proyectos de bricolaje. Facilita el trabajo, ahorra tiempo y reduce el esfuerzo. Diseño ergonómico, batería recargable y gran precisión para cualquier tarea.',
 sold:247,stars:5,lastUnits:false,timer:2*60*60},

{id:'T081',name:'Candado con Alarma para Moto',cat:'accesorios',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1882997/1753289533candado%20alarma.webp'],
 price:39000,oldPrice:79000,
 desc:'Protege tu motocicleta con este candado de alta resistencia equipado con alarma sonora. Detecta movimientos sospechosos y emite una potente alerta para disuadir robos. Seguridad adicional para tu tranquilidad.',
 sold:322,stars:5,lastUnits:false,timer:60*60},

{id:'T082',name:'Depiladora Trimmer Recargable 4 en 1',cat:'belleza',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2141242/1777486064gememy%20mujer%7D.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2141242/1777486062gemmey%20mujer.jpg'],
 price:49900,oldPrice:99000,
 desc:'Elimina vello facial y corporal de forma rápida, segura y sin irritaciones. Incluye diferentes cabezales para adaptarse a cada zona del cuerpo. Recargable, compacta y perfecta para mantener una apariencia impecable.',
 sold:183,stars:5,lastUnits:false,timer:2*60*60},

{id:'T083',name:'Aspiradora Inalámbrica 3 en 1',cat:'hogar',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1881968/1777060523ASPIRADORA%203%20EN%201.webp','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1881968/1777060523ASPIRAORA%203%20EN%201.webp'],
 price:65000,oldPrice:129000,
 desc:'Potente aspiradora portátil con gran capacidad de succión para hogar, oficina y automóvil. Elimina polvo, migas y suciedad en segundos. Ligera, recargable y fácil de usar, ideal para mantener cualquier espacio impecable.',
 sold:341,stars:5,lastUnits:false,timer:3*60*60},

{id:'T084',name:'Limpiador Eléctrico Multifuncional 9 en 1',cat:'hogar',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2102797/1776435194limpiadotr%209%20en%201.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2102797/1776435194CEPILLO%20LIM%20NPIADOR.webp'],
 price:65000,oldPrice:129000,
 desc:'Limpia baños, cocinas, juntas, vidrios y superficies difíciles sin esfuerzo. Incluye múltiples accesorios para diferentes usos. Ahorra tiempo y consigue resultados profesionales en cada limpieza.',
 sold:229,stars:5,lastUnits:false,timer:2*60*60},

{id:'T085',name:'Tapete Antideslizante para Baño',cat:'hogar',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1132537/1724951185TAPETE%20DE%20BA%C3%91O%202.webp'],
 price:32000,oldPrice:65000,
 desc:'Mayor seguridad y comodidad al salir de la ducha. Material absorbente, suave al tacto y con base antideslizante que ayuda a prevenir accidentes. Ideal para baños modernos y hogares con niños o adultos mayores.',
 sold:286,stars:5,lastUnits:false,timer:60*60},

{id:'T086',name:'Maleta Tocador para Niñas',cat:'infantil',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2010932/17643471924988295547701627829.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2010932/1768315742tocadr%202.jpg'],
 price:89000,oldPrice:159000,
 desc:'Divertido set de belleza infantil para estimular la imaginación y el juego creativo. Incluye accesorios organizados en una práctica maleta portátil. Ideal para regalar y disfrutar horas de entretenimiento.',
 sold:164,stars:5,lastUnits:false,timer:2*60*60},

{id:'T087',name:'Ducha Portátil Recargable',cat:'hogar',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2140982/1777474239ducha%203333.jpg'],
 price:55000,oldPrice:109000,
 desc:'Perfecta para camping, viajes, mascotas, jardines y emergencias. Funciona con batería recargable y proporciona un flujo constante de agua donde lo necesites. Compacta, práctica y fácil de transportar.',
 sold:198,stars:5,lastUnits:false,timer:2*60*60},

{id:'T088',name:'Máquina Eléctrica para Pintar',cat:'herramientas',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/422645/1741295923MAQUINA%20REAL.jpg'],
 price:135000,oldPrice:229000,
 desc:'Obtén acabados uniformes y profesionales en paredes, muebles y superficies. Reduce el tiempo de trabajo y evita marcas de brocha. Ideal para proyectos de remodelación, pintura doméstica y uso profesional.',
 sold:119,stars:5,lastUnits:false,timer:4*60*60},

{id:'T089',name:'Kit de Aseo para Bebé 9 Piezas',cat:'bebes',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1920100/1771462301BEBE%20REAL.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1920100/1757360432kit%20bebe%20N.webp'],
 price:49900,oldPrice:99000,
 desc:'Todo lo necesario para el cuidado diario de tu bebé en un práctico estuche portátil. Incluye accesorios seguros y diseñados especialmente para los más pequeños. Ideal para el hogar y para llevar de viaje.',
 sold:274,stars:5,lastUnits:false,timer:2*60*60},

{id:'T090',name:'Electroestimulador de Gimnasia Pasiva',cat:'salud',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2086052/1771287122ELETRODO.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2086052/1771287122ELECTP.jpg'],
 price:45000,oldPrice:89000,
 desc:'Ayuda a relajar músculos cansados, aliviar tensiones y complementar rutinas de bienestar. Cuenta con diferentes niveles de intensidad y programas de masaje para adaptarse a tus necesidades diarias.',
 sold:205,stars:5,lastUnits:false,timer:60*60},
{id:'T091',name:'Juego de Tapetes Antideslizantes',cat:'hogar',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1951912/1759788205nuebo%20tap.jpg'],
 price:45000,oldPrice:89000,
 desc:'Protege tus pisos y añade confort a cualquier espacio del hogar. Material resistente, fácil de limpiar y diseño moderno que combina con cualquier decoración. Ideal para baños, habitaciones y salas.',
 sold:158,stars:5,lastUnits:false,timer:60*60},
{id:'T071',name:'Organizador Metálico De Cocina',cat:'hogar',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2159999/1779807048ORGANIZADOR%20METALICO%20DE%20COCINA%201.webp',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1085959/1723832912WhatsApp%20Image%202024-08-16%20at%2012.58.33%20PM.jpeg'
],
price:42000,oldPrice:89000,
desc:'Organiza utensilios, especias y accesorios aprovechando el espacio de las paredes. Diseño resistente y moderno para una cocina más ordenada.',
sold:225,stars:5,lastUnits:false,timer:2*60*60},
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
  {id:'T092',name:'Perchero con Cubierta Organizador',cat:'hogar',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1900120/1755196031WhatsApp%20Image%202025-08-14%20at%201.16.21%20PM.jpeg'],
   price:67000,oldPrice:119000,
   desc:'Perchero con cubierta protectora que mantiene tu ropa libre de polvo y humedad. Varios niveles de organización. Estructura robusta y estable. Ideal para dormitorios, entradas y cuartos pequeños. Fácil de armar, sin herramientas. Solución elegante para organizar tu ropa.',
   sold:99,stars:4,lastUnits:false,timer:90*60},
];

</script>
<script>
/* =========================================================
   TROGÜI — lógica de la tienda
   ========================================================= */
const WHATSAPP_NUMBER = '573206572598';
const PLACEHOLDER_IMG = 'data:image/svg+xml,%3Csvg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 400 400%22%3E%3Crect width=%22400%22 height=%22400%22 fill=%22%23f4f3ee%22/%3E%3Ctext x=%22200%22 y=%22210%22 font-size=%2228%22 font-family=%22Arial%22 fill=%22%23ff6a00%22 text-anchor=%22middle%22%3ETROG%C3%9CI%3C/text%3E%3C/svg%3E';

/* ---------- Iconos SVG (sin emojis) ---------- */
const ICONS = {
  truck:'<svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><rect x="1" y="7" width="14" height="10"/><path d="M15 10h4l3 3v4h-7z"/><circle cx="6" cy="19" r="1.6"/><circle cx="17.5" cy="19" r="1.6"/></svg>',
  cash:'<svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><rect x="2" y="6" width="20" height="12" rx="2"/><circle cx="12" cy="12" r="3"/></svg>',
  shield:'<svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M12 2 4 5v6c0 5 3.5 9 8 11 4.5-2 8-6 8-11V5z"/><path d="M9 12l2 2 4-4"/></svg>',
  repeat:'<svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M17 2l4 4-4 4"/><path d="M3 11V9a4 4 0 0 1 4-4h14"/><path d="M7 22l-4-4 4-4"/><path d="M21 13v2a4 4 0 0 1-4 4H3"/></svg>',
  clock:'<svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="9"/><path d="M12 7v5l3 3"/></svg>',
  search:'<svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><circle cx="11" cy="11" r="7"/><path d="M21 21l-4.3-4.3"/></svg>',
  whatsapp:'<svg class="icon" viewBox="0 0 32 32" fill="currentColor"><path d="M16.001 3C9.373 3 4 8.373 4 15c0 2.386.7 4.61 1.902 6.478L4 29l7.72-1.867A11.94 11.94 0 0 0 16 27c6.627 0 12-5.373 12-12S22.628 3 16.001 3zm6.994 17.02c-.29.815-1.44 1.5-2.36 1.694-.633.13-1.46.234-4.24-.906-3.556-1.47-5.84-5.05-6.017-5.285-.176-.235-1.44-1.916-1.44-3.655 0-1.74.91-2.594 1.234-2.95.324-.354.706-.443.94-.443.235 0 .47.003.674.013.216.01.507-.082.793.605.29.7.984 2.418 1.07 2.594.088.176.147.382.03.618-.117.235-.176.382-.35.588-.176.206-.368.46-.526.618-.176.176-.36.367-.156.72.206.353.914 1.51 1.964 2.446 1.35 1.203 2.49 1.576 2.844 1.752.353.176.56.147.766-.088.206-.235.882-1.03 1.117-1.383.235-.353.47-.294.793-.176.324.117 2.06.97 2.412 1.147.353.176.588.264.674.412.088.147.088.85-.204 1.665z"/></svg>',
  instagram:'<svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><rect x="3" y="3" width="18" height="18" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.4" cy="6.6" r="1"/></svg>',
  tiktok:'<svg class="icon" viewBox="0 0 24 24" fill="currentColor"><path d="M14 3c.3 1.9 1.6 3.4 3.6 3.8v2.4c-1.3-.1-2.5-.5-3.6-1.2v6.4a5 5 0 1 1-4.3-5v2.3a2.7 2.7 0 1 0 1.9 2.6V3z"/></svg>',
  link:'<svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M10 14a5 5 0 0 0 7 0l3-3a5 5 0 0 0-7-7l-1.5 1.5"/><path d="M14 10a5 5 0 0 0-7 0l-3 3a5 5 0 0 0 7 7l1.5-1.5"/></svg>',
  copy:'<svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><rect x="9" y="9" width="12" height="12" rx="2"/><path d="M5 15V5a2 2 0 0 1 2-2h10"/></svg>',
  check:'<svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round"><path d="M4 12l5 5L20 6"/></svg>',
  bag:'<svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M6 8h12l-1 12H7z"/><path d="M9 8V6a3 3 0 0 1 6 0v2"/></svg>',
  bot:'<svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><rect x="4" y="8" width="16" height="12" rx="3"/><path d="M12 8V4"/><circle cx="8.5" cy="14" r="1.3" fill="currentColor" stroke="none"/><circle cx="15.5" cy="14" r="1.3" fill="currentColor" stroke="none"/><path d="M9 18h6"/></svg>',
  send:'<svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M22 2 11 13"/><path d="M22 2 15 22l-4-9-9-4z"/></svg>',
  location:'<svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M12 21s7-6.5 7-12a7 7 0 0 0-14 0c0 5.5 7 12 7 12z"/><circle cx="12" cy="9" r="2.4"/></svg>'
};
const ADMIN_PASS = '4325';
const STORAGE_KEY = 'trogui_store_v1';
const SOCIAL = {
  tiktok: 'https://www.tiktok.com/@trogui_store?_r=1&_t=ZS-98Z2FAUQMPH',
  instagram: 'https://www.instagram.com/store_trogu?igsh=MWZleXFlY21weDhnMQ%3D%3D&utm_source=qr'
};

/* ---------- Pedidos: contraseña, almacenamiento y hoja de cálculo ---------- */
const ORDERS_PASSWORD = '3214';
const ORDERS_STORAGE_KEY = 'trogui_orders_v1';
/* Pega aquí la URL de tu Google Apps Script (Web App) para que los pedidos se vean
   EN LÍNEA desde cualquier celular o computador, no solo en el navegador donde se hizo el pedido.
   Instrucciones completas en el mensaje de Claude. Ejemplo de URL válida:
   'https://script.google.com/macros/s/AKfycb.../exec'
   Si la dejas vacía, los pedidos solo quedan guardados en el navegador de cada visitante (modo local). */
const GOOGLE_SCRIPT_URL = '';

/* ---------- Calculadora de tiempos de entrega ---------- */
const CIUDADES_PRINCIPALES = ['bogota','medellin','cali','barranquilla','cartagena','bucaramanga','pereira',
'manizales','ibague','cucuta','santa marta','villavicencio','monteria','neiva','armenia','pasto','popayan',
'sincelejo','valledupar','soacha','envigado','itagui','bello','soledad','floridablanca','dosquebradas',
'palmira','buenaventura','tulua','rionegro','chia','girardot','yopal','tunja','riohacha','quibdo','sogamoso'];
function estimateDelivery(cityText){
  const norm = normalizeTxt(cityText||'').trim();
  if(!norm) return null;
  const isMain = CIUDADES_PRINCIPALES.some(c => norm.includes(c) || c.includes(norm));
  return isMain ? {min:3,max:5,main:true} : {min:3,max:7,main:false};
}

const CAT_LABELS = {
  cocina:{label:'Cocina', icon:''}, salud:{label:'Salud', icon:''},
  hogar:{label:'Hogar', icon:''}, tecnologia:{label:'Tecnología', icon:''},
  accesorios:{label:'Accesorios', icon:''}, juguetes:{label:'Juguetes', icon:''},
  belleza:{label:'Belleza', icon:''}, ropa:{label:'Ropa Deportiva', icon:''},
  bebes:{label:'Bebés', icon:''}, viajes:{label:'Viajes', icon:''},
  herramientas:{label:'Herramientas', icon:''}, infantil:{label:'Infantil', icon:''}
};

const PROBLEMA_POR_CATEGORIA = {
  cocina:'¿Tu cocina se te desordena y cocinar se vuelve una tarea eterna?',
  salud:'¿Buscas cuidar tu bienestar y el de tu familia sin salir de casa?',
  hogar:'¿Sientes que en tu casa falta espacio y orden?',
  tecnologia:'¿Quieres disfrutar tecnología de punta sin pagar de más?',
  accesorios:'¿Necesitas algo práctico que te resuelva el día a día?',
  juguetes:'¿Buscas el regalo que de verdad saque una sonrisa?',
  belleza:'¿Sueñas con lucir radiante todos los días sin ir al spa?',
  ropa:'¿Quieres mostrar tu pasión por tu equipo con estilo y calidad?',
  bebes:'¿Quieres darle a tu bebé el cuidado y la seguridad que merece?',
  viajes:'¿Necesitas viajar organizado, cómodo y sin complicaciones?',
  herramientas:'¿Los arreglos en casa te quitan tiempo, plata y paciencia?',
  infantil:'¿Buscas algo que despierte la imaginación de los más pequeños?'
};

/* ---------- Reseñas: nombres y ciudades colombianas ---------- */
const NOMBRES_CO = ['Valentina Torres','Juan Camilo Restrepo','Luisa Fernanda Gómez','Andrés Felipe Ospina',
'Natalia Suárez','Camila Andrea Rincón','Santiago Zuluaga','Mariana Cárdenas','Daniela Muñoz','Carlos Eduardo Peña',
'Laura Sofía Bedoya','Jhon Alexander Vargas','Yuliana Marcela Ríos','Cristian David Higuita','Paula Andrea Salazar',
'Diego Fernando Arango','Sara Isabel Moreno','Miguel Ángel Cortés','Angie Lorena Puentes','Brayan Steven Quintero',
'Karen Dayana Bonilla','Jorge Iván Castañeda','Estefanía López','Sebastián Correa','Yesenia Patricia Villalba',
'Nicolás Herrera','Mónica Alexandra Duque','Fabián Andrés Trujillo','Lina Marcela Ocampo','Wilmer Alexis Guzmán'];
const CIUDADES_CO = ['Bogotá','Medellín','Cali','Barranquilla','Bucaramanga','Cartagena','Pereira','Manizales',
'Ibagué','Cúcuta','Villavicencio','Santa Marta','Neiva','Armenia','Popayán','Valledupar','Montería','Pasto',
'Sincelejo','Tuluá','Soacha','Envigado','Rionegro','Chía','Girardot'];
const COMENTARIOS_POOL = [
'Me llegó en pocos días y quedé feliz, la calidad superó lo que esperaba.',
'Pedí contra entrega y todo salió perfecto, muy confiables.',
'Excelente producto, exactamente como en las fotos. Ya hice mi segundo pedido.',
'El empaque llegó impecable y el vendedor respondió todas mis dudas por WhatsApp.',
'100% recomendado, muy buena atención y envío rápido a mi ciudad.',
'Superó mis expectativas, se nota que es un producto de buena calidad.',
'Fácil de pedir, pagué contra entrega y llegó antes de lo esperado.',
'Ya es la segunda vez que compro en Trogüi y siempre quedo satisfecho.',
'Excelente relación precio-calidad, totalmente recomendado.',
'El domiciliario fue muy amable y el producto llegó bien empacado.',
'Compré por WhatsApp y todo el proceso fue súper fácil y rápido.',
'Me encantó, funciona tal cual lo describen. Gracias Trogüi!',
'Buena atención al cliente, resolvieron mis dudas antes de comprar.',
'Llegó a tiempo y en excelente estado, muy contenta con la compra.',
'Se los recomiendo a todos mis amigos, son muy serios y cumplidos.'
];

function seededRand(seed){
  let x = Math.sin(seed) * 10000;
  return x - Math.floor(x);
}
function hashStr(str){
  let h = 0;
  for(let i=0;i<str.length;i++){ h = (h*31 + str.charCodeAt(i)) >>> 0; }
  return h;
}
function buildReviewsFor(product){
  const seedBase = hashStr(product.id + product.name);
  const n = 3 + Math.floor(seededRand(seedBase) * 3); // 3-5
  const list = [];
  const usedNames = new Set();
  for(let i=0;i<n;i++){
    let ni = Math.floor(seededRand(seedBase + i*7.13) * NOMBRES_CO.length);
    while(usedNames.has(ni)){ ni = (ni+1) % NOMBRES_CO.length; }
    usedNames.add(ni);
    const ci = Math.floor(seededRand(seedBase + i*3.71) * CIUDADES_CO.length);
    const txi = Math.floor(seededRand(seedBase + i*5.29) * COMENTARIOS_POOL.length);
    const starVal = seededRand(seedBase + i*1.91) > 0.15 ? 5 : 4;
    list.push({name:NOMBRES_CO[ni], city:CIUDADES_CO[ci], text:COMENTARIOS_POOL[txi], stars:starVal});
  }
  return list;
}

/* ---------- Utilidades ---------- */
function money(n){ return '$' + Math.round(n).toLocaleString('es-CO'); }
function pct(oldP, newP){ return Math.round((1 - (newP/oldP)) * 100); }
function slug(s){ return s.toLowerCase().normalize('NFD').replace(/[\u0300-\u036f]/g,'').replace(/[^a-z0-9]+/g,'-').replace(/(^-|-$)/g,''); }
function normalizeTxt(s){ return (s||'').toLowerCase().normalize('NFD').replace(/[\u0300-\u036f]/g,''); }
function fmtTime(totalSeconds){
  totalSeconds = Math.max(0, Math.floor(totalSeconds));
  const h = Math.floor(totalSeconds/3600);
  const m = Math.floor((totalSeconds%3600)/60);
  const s = totalSeconds%60;
  if(h>0) return `${h}h ${String(m).padStart(2,'0')}m ${String(s).padStart(2,'0')}s`;
  return `${String(m).padStart(2,'0')}m ${String(s).padStart(2,'0')}s`;
}
function levenshtein(a,b){
  const m=a.length,n=b.length;
  if(!m) return n; if(!n) return m;
  const dp = Array.from({length:m+1},(_,i)=>[i,...Array(n).fill(0)]);
  for(let j=0;j<=n;j++) dp[0][j]=j;
  for(let i=1;i<=m;i++){
    for(let j=1;j<=n;j++){
      dp[i][j] = a[i-1]===b[j-1] ? dp[i-1][j-1] : 1+Math.min(dp[i-1][j-1],dp[i-1][j],dp[i][j-1]);
    }
  }
  return dp[m][n];
}
function fuzzyIncludes(haystack, needle){
  haystack = normalizeTxt(haystack); needle = normalizeTxt(needle).trim();
  if(!needle) return true;
  if(haystack.includes(needle)) return true;
  const words = haystack.split(/[^a-z0-9]+/).filter(Boolean);
  const needleWords = needle.split(/\s+/).filter(Boolean);
  return needleWords.every(nw=>{
    if(nw.length<3) return haystack.includes(nw);
    return words.some(w=> w.includes(nw) || levenshtein(w,nw) <= (nw.length>=6?2:1));
  });
}

/* ---------- Persistencia / merge de productos ---------- */
function readStore(){
  try{
    const raw = localStorage.getItem(STORAGE_KEY);
    if(!raw) return {overrides:{}, custom:[], deleted:[]};
    const parsed = JSON.parse(raw);
    return {overrides:parsed.overrides||{}, custom:parsed.custom||[], deleted:parsed.deleted||[]};
  }catch(e){ return {overrides:{}, custom:[], deleted:[]}; }
}
function writeStore(data){
  try{ localStorage.setItem(STORAGE_KEY, JSON.stringify(data)); }catch(e){ console.error('No se pudo guardar', e); }
}
function getAllProducts(){
  const store = readStore();
  const base = RAW_PRODUCTS
    .filter(p=> !store.deleted.includes(p.id))
    .map(p=> store.overrides[p.id] ? {...p, ...store.overrides[p.id]} : p);
  return [...base, ...store.custom];
}
function garantiaDias(id){ return (hashStr(id) % 2 === 0) ? 30 : 60; }

/* ---------- Pedidos: lectura/escritura local + envío a Google Sheets (opcional) ---------- */
function readOrders(){
  try{
    const raw = localStorage.getItem(ORDERS_STORAGE_KEY);
    return raw ? JSON.parse(raw) : [];
  }catch(e){ return []; }
}
function writeOrders(list){
  try{ localStorage.setItem(ORDERS_STORAGE_KEY, JSON.stringify(list)); }catch(e){ console.error('No se pudo guardar pedidos', e); }
}
function saveOrder(order){
  // Guardado local inmediato (respaldo, funciona incluso sin internet en ese instante)
  const list = readOrders();
  list.unshift(order);
  writeOrders(list);
  // Envío a la hoja de cálculo en línea, para que se vea desde cualquier dispositivo
  if(GOOGLE_SCRIPT_URL){
    fetch(GOOGLE_SCRIPT_URL, {
      method:'POST',
      mode:'no-cors', // Apps Script no siempre permite leer la respuesta, pero sí recibe los datos
      headers:{'Content-Type':'text/plain;charset=utf-8'},
      body: JSON.stringify({action:'create', order})
    }).catch(()=>{ /* si falla la conexión, el pedido ya quedó guardado localmente como respaldo */ });
  }
}
function updateOrderStatus(id, status){
  const list = readOrders();
  const idx = list.findIndex(o=>o.id===id);
  if(idx>-1){ list[idx].estado = status; writeOrders(list); }
  if(GOOGLE_SCRIPT_URL){
    fetch(GOOGLE_SCRIPT_URL, {
      method:'POST',
      mode:'no-cors',
      headers:{'Content-Type':'text/plain;charset=utf-8'},
      body: JSON.stringify({action:'updateStatus', id, status})
    }).catch(()=>{});
  }
}
async function fetchOrdersOnline(){
  if(!GOOGLE_SCRIPT_URL) return null;
  try{
    const res = await fetch(GOOGLE_SCRIPT_URL + '?t=' + Date.now());
    if(!res.ok) return null;
    const data = await res.json();
    return Array.isArray(data) ? data : null;
  }catch(e){ return null; }
}

/* ---------- Estado en memoria ---------- */
let STATE = {
  products: [],
  order: [],          // orden barajado (ids), fijo durante la sesión
  category: 'todas',
  query: '',
  timers: {},          // id -> {end: timestamp}
};

function shuffle(arr){
  const a = [...arr];
  for(let i=a.length-1;i>0;i--){
    const j = Math.floor(Math.random()*(i+1));
    [a[i],a[j]] = [a[j],a[i]];
  }
  return a;
}

const MIN_TIMER_SECONDS = 14*60; // mínimo 14 minutos
function randomTimerSeconds(base){
  base = base || 1800;
  return Math.max(MIN_TIMER_SECONDS, base * (0.7 + Math.random()*1.6));
}
function initTimers(products){
  products.forEach(p=>{
    STATE.timers[p.id] = { end: Date.now() + randomTimerSeconds(p.timer)*1000 };
  });
}
function tickTimers(){
  const now = Date.now();
  document.querySelectorAll('[data-timer]').forEach(el=>{
    const id = el.getAttribute('data-timer');
    let t = STATE.timers[id];
    if(!t){ t = {end: now + randomTimerSeconds()*1000}; STATE.timers[id] = t; }
    let remaining = (t.end - now)/1000;
    if(remaining <= 0){
      const p = STATE.products.find(pp=>pp.id===id);
      const fresh = randomTimerSeconds(p && p.timer);
      t.end = now + fresh*1000;
      remaining = fresh;
    }
    el.textContent = fmtTime(remaining);
  });
}
setInterval(tickTimers, 1000);

/* ---------- Router ---------- */
function currentRoute(){
  const hash = location.hash || '#/';
  const m = hash.match(/^#\/producto\/(.+)$/);
  if(m) return {name:'product', id: decodeURIComponent(m[1])};
  return {name:'home'};
}
window.addEventListener('hashchange', render);

/* ---------- Render raíz ---------- */
const app = document.getElementById('app');

function render(){
  STATE.products = getAllProducts();
  if(!STATE.order.length || STATE.order.length !== STATE.products.length){
    STATE.order = shuffle(STATE.products.map(p=>p.id));
    initTimers(STATE.products);
  }
  const route = currentRoute();
  window.scrollTo({top:0, behavior:'instant'});
  if(route.name === 'product'){
    const product = STATE.products.find(p=>p.id === route.id);
    if(product) renderProductPage(product);
    else { location.hash = '#/'; }
  } else {
    renderHome();
  }
}

/* ---------- HOME ---------- */
function orderedProducts(){
  const byId = Object.fromEntries(STATE.products.map(p=>[p.id,p]));
  let list = STATE.order.map(id=>byId[id]).filter(Boolean);
  if(STATE.category !== 'todas') list = list.filter(p=>p.cat === STATE.category);
  if(STATE.query.trim()){
    list = list.filter(p=> fuzzyIncludes(p.name+' '+p.desc+' '+(CAT_LABELS[p.cat]?.label||p.cat), STATE.query));
  }
  return list;
}

function categoriesPresent(){
  const set = new Set(STATE.products.map(p=>p.cat));
  return [...set];
}

function renderHome(){
  const cats = categoriesPresent();
  const list = orderedProducts();
  app.innerHTML = `
    ${headerHtml()}
    ${navHtml(cats)}
    <div class="hero">
      <div class="hero-banner">
        <div class="hero-text">
          <h1>Todo lo que necesitas, al mejor precio de Colombia</h1>
          <p>Más de 3 años despachando a toda Colombia. Paga contra entrega, sin sorpresas. Productos nuevos, garantizados y con envío gratis.</p>
          <div class="hero-badges">
            <span class="hero-badge">${ICONS.truck}<span>Envío gratis a toda Colombia</span></span>
            <span class="hero-badge">${ICONS.cash}<span>Pago contra entrega</span></span>
            <span class="hero-badge">${ICONS.shield}<span>Garantía real</span></span>
          </div>
          <a href="https://wa.me/${WHATSAPP_NUMBER}?text=${encodeURIComponent('Hola Trogüi, quiero saber más sobre sus productos.')}" target="_blank" class="hero-cta">${ICONS.whatsapp}<span>Escríbenos por WhatsApp</span></a>
        </div>
      </div>
    </div>
    <div class="section-title">
      <div>
        <h2>${STATE.category==='todas' ? 'Todos los <span>productos</span>' : (CAT_LABELS[STATE.category]?.label || STATE.category)}</h2>
        <p class="section-sub">${list.length} producto${list.length===1?'':'s'} disponible${list.length===1?'':'s'} · envío gratis a toda Colombia</p>
      </div>
    </div>
    <div class="grid" id="grid">
      ${list.length ? list.map(cardHtml).join('') : emptyStateHtml()}
    </div>
    ${trustStripHtml()}
    ${carriersHtml()}
    ${marqueeHtml()}
    ${footerHtml()}
    ${fabsHtml()}
  `;
  bindGlobalEvents();
  tickTimers();
  startNotifications();
}

function updateGrid(){
  const list = orderedProducts();
  const gridEl = document.getElementById('grid');
  const titleWrap = document.querySelector('.section-title h2');
  const subWrap = document.querySelector('.section-sub');
  if(gridEl) gridEl.innerHTML = list.length ? list.map(cardHtml).join('') : emptyStateHtml();
  if(titleWrap) titleWrap.innerHTML = STATE.category==='todas' ? 'Todos los <span>productos</span>' : (CAT_LABELS[STATE.category]?.label || STATE.category);
  if(subWrap) subWrap.textContent = `${list.length} producto${list.length===1?'':'s'} disponible${list.length===1?'':'s'} · envío gratis a toda Colombia`;
  tickTimers();
}

function emptyStateHtml(){
  return `<div class="empty-state" style="grid-column:1/-1;">
    <div class="empty-ico">${ICONS.search}</div>
    <p>No encontramos productos con esa búsqueda.<br>Intenta con otra palabra o mira todas las categorías.</p>
  </div>`;
}

function cardHtml(p){
  const discount = p.oldPrice ? pct(p.oldPrice, p.price) : 0;
  const img = (p.imgs && p.imgs[0]) || '';
  return `
  <div class="card">
    ${discount>0 ? `<span class="badge">-${discount}%</span>` : ''}
    ${p.lastUnits ? `<span class="badge last">Últimas unidades</span>` : (p.sold>200 ? `<span class="badge last">Más vendido</span>` : '')}
    <div class="card-img-wrap" onclick="goToProduct('${p.id}')">
      <img src="${img}" alt="${escapeHtml(p.name)}" loading="lazy" onerror="this.onerror=null;this.src='${PLACEHOLDER_IMG}';">
    </div>
    <div class="card-body">
      <div class="card-title" onclick="goToProduct('${p.id}')">${escapeHtml(p.name)}</div>
      <div class="stars">${starIcons(p.stars)} <span class="count">(${p.sold}+ vendidos)</span></div>
      <div class="price-row">
        <span class="price-now">${money(p.price)}</span>
        ${p.oldPrice ? `<span class="price-old">${money(p.oldPrice)}</span>` : ''}
      </div>
      <div class="timer-row">${ICONS.clock}<span data-timer="${p.id}">--:--</span></div>
      <button class="btn btn-orange full" onclick="quickOrder('${p.id}')">Comprar ahora</button>
    </div>
  </div>`;
}

function starIcons(n){
  n = Math.round(n||5);
  return '★'.repeat(n) + '☆'.repeat(Math.max(0,5-n));
}
function escapeHtml(s){
  return (s||'').replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;').replace(/"/g,'&quot;');
}

function goToProduct(id){ location.hash = '#/producto/' + encodeURIComponent(id); }
function quickOrder(id){
  const p = STATE.products.find(pp=>pp.id===id);
  if(p) openOrderModal(p);
}

/* ---------- Bloques compartidos ---------- */
function headerHtml(){
  return `<header class="site-header">
    <div class="header-inner">
      <a href="#/" class="logo">TR<span class="accent-o">O</span>GÜI<small>bodega colombiana</small></a>
      <div class="search-wrap">
        <input id="searchInput" type="text" placeholder="Buscar productos..." value="${escapeHtml(STATE.query)}" autocomplete="off">
        <button onclick="doSearch()">${ICONS.search}</button>
      </div>
      <a class="header-wsp" href="https://wa.me/${WHATSAPP_NUMBER}" target="_blank">${ICONS.whatsapp}<span>WhatsApp</span></a>
    </div>
  </header>`;
}
function navHtml(cats){
  const chips = ['todas', ...cats];
  return `<nav class="cat-nav"><div class="cat-nav-inner">
    ${chips.map(c=>{
      const active = STATE.category===c ? 'active' : '';
      const label = c==='todas' ? 'Todas' : (CAT_LABELS[c]?.label || c);
      return `<a href="javascript:void(0)" class="cat-chip ${active}" data-cat="${c}" onclick="setCategory('${c}')">${label}</a>`;
    }).join('')}
  </div></nav>`;
}
function trustStripHtml(){
  return `<div class="trust-strip"><div class="trust-strip-inner">
    <div class="ts-item">${ICONS.truck}<div><b>Envío gratis</b><span>A toda Colombia</span></div></div>
    <div class="ts-item">${ICONS.cash}<div><b>Pago contra entrega</b><span>Sin anticipos</span></div></div>
    <div class="ts-item">${ICONS.shield}<div><b>Garantía real</b><span>30 a 60 días</span></div></div>
    <div class="ts-item">${ICONS.check}<div><b>+3 años</b><span>En el mercado colombiano</span></div></div>
  </div></div>`;
}
function carriersHtml(mini){
  if(mini){
    return `<div class="carriers-mini">${ICONS.truck}<span>Enviamos con Interrapidísimo · Envía · Coordinadora</span></div>`;
  }
  return `<div class="carriers-block">
    <p class="carriers-label">Envíos certificados a toda Colombia</p>
    <div class="carriers-row">
      <span class="carrier-badge">Interrapidísimo</span>
      <span class="carrier-badge">Envía</span>
      <span class="carrier-badge">Coordinadora</span>
    </div>
  </div>`;
}
function marqueeHtml(){
  const items = ['Envío gratis a toda Colombia','Pago contra entrega, sin anticipos','Garantía de 30 a 60 días según el producto',
  'Enviamos con Interrapidísimo, Envía y Coordinadora','Más de 3 años de experiencia en el mercado colombiano','Productos 100% nuevos y garantizados'];
  const track = [...items, ...items].map(t=>`<span>${ICONS.check}${t}</span>`).join('');
  return `<div class="marquee"><div class="marquee-track">${track}</div></div>`;
}
function footerHtml(){
  return `<footer>
    <div class="footer-inner">
      <div>
        <div class="foot-logo">TR<span>O</span>GÜI</div>
        <p>Trogüi es una bodega colombiana con más de 3 años en el mercado, con sede en <b>Bogotá y Cali</b>, especializada en productos para el hogar, tecnología y bienestar. Trabajamos con productos 100% nuevos y garantizados, pensando siempre en la satisfacción de nuestros clientes.</p>
        <div class="social-row">
          <a class="social-pill" href="${SOCIAL.tiktok}" target="_blank" title="TikTok">${ICONS.tiktok}</a>
          <a class="social-pill" href="${SOCIAL.instagram}" target="_blank" title="Instagram">${ICONS.instagram}</a>
          <a class="social-pill" href="https://wa.me/${WHATSAPP_NUMBER}" target="_blank" title="WhatsApp">${ICONS.whatsapp}</a>
        </div>
      </div>
      <div>
        <h4>Envíos</h4>
        <p>Hacemos envíos a toda Colombia de forma segura y confiable. Ciudades principales: 3 a 5 días hábiles. Municipios y otras zonas: 3 a 7 días hábiles.</p>
        <div class="carriers">
          <span class="carrier-pill">Interrapidísimo</span>
          <span class="carrier-pill">Envía</span>
          <span class="carrier-pill">Coordinadora</span>
        </div>
      </div>
      <div>
        <h4>Ayuda</h4>
        <a href="https://wa.me/${WHATSAPP_NUMBER}" target="_blank">Contáctanos por WhatsApp</a>
        <a href="javascript:void(0)" onclick="alert('Garantía: 30 a 60 días según el producto. Tienes 5 días hábiles desde la entrega para reportar cualquier inconveniente escribiéndonos por WhatsApp.')">Garantía y devoluciones</a>
        <a href="javascript:void(0)" onclick="alert('Pago contra entrega disponible en la mayoría de ciudades de Colombia. También aceptamos pago anticipado.')">Métodos de pago</a>
      </div>
      <div>
        <h4>Síguenos</h4>
        <a href="${SOCIAL.tiktok}" target="_blank">TikTok @trogui_store</a>
        <a href="${SOCIAL.instagram}" target="_blank">Instagram @store_trogu</a>
        <a href="https://wa.me/${WHATSAPP_NUMBER}" target="_blank">WhatsApp 320 657 2598</a>
      </div>
    </div>
    <div class="foot-bottom">
      <span>© ${new Date().getFullYear()} Trogüi — Bodega colombiana. Todos los derechos reservados.</span>
      <span>Hecho en Colombia</span>
    </div>
  </footer>`;
}
function fabsHtml(){
  return `
  <a class="fab-whatsapp" href="https://wa.me/${WHATSAPP_NUMBER}?text=${encodeURIComponent('Hola Trogüi, tengo una pregunta.')}" target="_blank" title="Escríbenos por WhatsApp">${ICONS.whatsapp}</a>
  <div class="fab-ai" onclick="openAiChat()" title="Asistente Trogüi">
    <span class="fab-ai-label">Pregúntale al asistente</span>
    ${ICONS.bot}
  </div>
  <div class="fab-admin" onclick="openAdminLogin()" title="Panel de productos">R</div>
  <div class="fab-orders" onclick="openOrdersLogin()" title="Ver pedidos">P</div>
  <div id="notifHost" class="notif-host"></div>
  <div id="toast" class="toast"></div>
  `;
}

/* ---------- Notificaciones de confianza (social proof) ---------- */
const NOTIF_POOL = [
  {text:'Envío gratis a toda Colombia', icon:''},
  {text:'Pago contra entrega disponible', icon:''},
  {text:'Garantía de hasta 60 días', icon:''},
  {text:'Más de 3 años sirviendo a Colombia', icon:''},
  {text:'Productos 100% nuevos y verificados', icon:''}
];
function randomSocialProof(){
  if(!STATE.products.length) return null;
  const p = STATE.products[Math.floor(Math.random()*STATE.products.length)];
  const city = CIUDADES_CO[Math.floor(Math.random()*CIUDADES_CO.length)];
  return {text:`Compra reciente en ${city}: ${p.name}`, icon:''};
}
let NOTIF_STARTED = false;
function startNotifications(){
  if(NOTIF_STARTED) return;
  NOTIF_STARTED = true;
  setTimeout(()=> pushNotif(NOTIF_POOL[0]), 7000);
  setTimeout(()=> pushNotif(NOTIF_POOL[1]), 20000);
  const loop = ()=>{
    const delay = 26000 + Math.random()*18000;
    setTimeout(()=>{
      const n = Math.random() < 0.5 ? randomSocialProof() : NOTIF_POOL[Math.floor(Math.random()*NOTIF_POOL.length)];
      if(n) pushNotif(n);
      loop();
    }, delay);
  };
  setTimeout(loop, 34000);
}
function pushNotif(n){
  const host = document.getElementById('notifHost');
  if(!host || !n) return;
  const el = document.createElement('div');
  el.className = 'notif-toast';
  el.innerHTML = `<span class="notif-ico">${ICONS[n.icon]||ICONS.check}</span><span>${escapeHtml(n.text)}</span>`;
  host.appendChild(el);
  requestAnimationFrame(()=> el.classList.add('show'));
  setTimeout(()=>{ el.classList.remove('show'); setTimeout(()=> el.remove(), 400); }, 4600);
}

/* ---------- Búsqueda y categoría ---------- */
function setCategory(c){
  STATE.category = c;
  document.querySelectorAll('.cat-chip').forEach(el=> el.classList.toggle('active', el.getAttribute('data-cat')===c));
  updateGrid();
}
function doSearch(){
  const el = document.getElementById('searchInput');
  STATE.query = el ? el.value : '';
  updateGrid();
}
function bindGlobalEvents(){
  const input = document.getElementById('searchInput');
  if(input){
    input.addEventListener('keydown', e=>{ if(e.key==='Enter') doSearch(); });
    input.addEventListener('input', debounce(()=>doSearch(), 250));
  }
}
function debounce(fn, wait){
  let t;
  return (...args)=>{ clearTimeout(t); t = setTimeout(()=>fn(...args), wait); };
}

/* ---------- PRODUCT DETAIL ---------- */
let GALLERY_STATE = {idx:0};

function renderProductPage(p){
  GALLERY_STATE.idx = 0;
  const discount = p.oldPrice ? pct(p.oldPrice, p.price) : 0;
  const savings = p.oldPrice ? (p.oldPrice - p.price) : 0;
  const reviews = buildReviewsFor(p);
  const garantia = garantiaDias(p.id);
  const related = STATE.products.filter(x=>x.cat===p.cat && x.id!==p.id).slice(0,4);
  const relatedFallback = related.length ? related : STATE.products.filter(x=>x.id!==p.id).slice(0,4);
  const problema = PROBLEMA_POR_CATEGORIA[p.cat] || '¿Buscas calidad, garantía y buen precio?';
  const sentences = p.desc.split(/(?<=[.!?])\s+/).filter(Boolean);
  const solucion = sentences[0] || p.desc;
  const beneficios = sentences.slice(1,5);

  app.innerHTML = `
    ${headerHtml()}
    ${navHtml(categoriesPresent())}
    <div class="detail-wrap">
      <div class="breadcrumb"><a href="#/">Inicio</a> / <a href="#/">${CAT_LABELS[p.cat]?.label || p.cat}</a> / ${escapeHtml(p.name)}</div>
      <div class="detail-grid">
        <div>
          <div class="gallery-main"><img id="mainImg" src="${p.imgs[0]}" alt="${escapeHtml(p.name)}" onerror="this.onerror=null;this.src='${PLACEHOLDER_IMG}';"></div>
          <div class="gallery-thumbs" id="thumbs">
            ${p.imgs.map((im,i)=>`<img src="${im}" class="${i===0?'active':''}" onclick="setGalleryImg(${i})" onerror="this.onerror=null;this.src='${PLACEHOLDER_IMG}';">`).join('')}
          </div>
        </div>
        <div>
          <h1 class="detail-title">${escapeHtml(p.name)}</h1>
          <div class="detail-meta">
            <span class="stars">${starIcons(p.stars)}</span>
            <span>${p.sold}+ vendidos</span>
            ${p.lastUnits ? '<span style="color:#c0392b;font-weight:700;">¡Últimas unidades!</span>' : ''}
          </div>
          <div class="detail-price-block">
            <div class="detail-price-row">
              <span class="detail-price-now">${money(p.price)}</span>
              ${p.oldPrice ? `<span class="detail-price-old">${money(p.oldPrice)}</span>` : ''}
              ${discount>0 ? `<span class="discount-tag">-${discount}% OFF</span>` : ''}
            </div>
            ${savings>0 ? `<div class="savings">${ICONS.check}<span>Ahorras ${money(savings)} comprando hoy</span></div>` : ''}
            <div class="detail-timer">${ICONS.clock}<span>Promoción termina en</span> <b data-timer="${p.id}">--:--</b></div>
          </div>
          <div class="trust-grid">
            <div class="trust-item">${ICONS.truck}<span>Envío gratis a toda Colombia</span></div>
            <div class="trust-item">${ICONS.cash}<span>Pago contra entrega</span></div>
            <div class="trust-item">${ICONS.shield}<span>Garantía de ${garantia} días</span></div>
            <div class="trust-item">${ICONS.repeat}<span>5 días hábiles para reportar</span></div>
          </div>
          <div class="delivery-calc">
            <label>${ICONS.location}Calcula el tiempo de entrega a tu ciudad</label>
            <div class="delivery-calc-row">
              <input type="text" id="deliveryCityInput" placeholder="Escribe tu ciudad o municipio..." onkeydown="if(event.key==='Enter')calcDeliveryOnPage()">
              <button type="button" onclick="calcDeliveryOnPage()">Calcular</button>
            </div>
            <div id="deliveryResultBox" class="delivery-result"></div>
          </div>
          <div class="qty-row">
            <span style="font-weight:700;font-size:.85rem;">Cantidad:</span>
            <div class="qty-box">
              <button onclick="changeQty(-1)">−</button>
              <input id="qtyInput" type="text" value="1" readonly>
              <button onclick="changeQty(1)">+</button>
            </div>
          </div>
          <div class="cta-col">
            <button class="cta-big cta-whatsapp" onclick="openOrderModal(STATE.products.find(x=>x.id==='${p.id}'))">${ICONS.bag}<span>Comprar ahora — Pago contra entrega</span></button>
            <div class="share-row">
              <button class="share-btn" onclick="shareProduct('${p.id}')">${ICONS.link}<span>Compartir</span></button>
              <button class="share-btn" onclick="copyLink('${p.id}')">${ICONS.copy}<span>Copiar enlace</span></button>
            </div>
            ${carriersHtml(true)}
          </div>
        </div>
      </div>
    </div>

    <div class="desc-block">
      <div class="desc-card">
        <h3>Descripción del producto</h3>
        <div class="desc-line"><span><b>Problema:</b> ${problema}</span></div>
        <div class="desc-line"><span><b>Solución:</b> ${solucion}</span></div>
        ${beneficios.length ? `<div class="desc-line"><span><b>Beneficios</b></span></div>
        <ul class="benefits-list">${beneficios.map(b=>`<li>${b}</li>`).join('')}</ul>` : ''}
        <div class="desc-line" style="margin-top:10px;"><span>Este producto cuenta con <b>${garantia} días de garantía</b>. Si algo no sale como esperabas, tienes <b>5 días hábiles</b> desde la entrega para reportarlo y te ayudamos sin complicaciones.</span></div>
      </div>
    </div>

    <div class="reviews-block">
      <div class="reviews-head">
        <h2 style="margin:0;font-size:1.1rem;">Lo que dicen nuestros clientes</h2>
        <span class="stars">${starIcons(p.stars)} <span style="color:var(--gray);font-size:.78rem;">(${reviews.length} reseñas)</span></span>
      </div>
      <div class="review-grid">
        ${reviews.map(r=>`
          <div class="review-card">
            <div class="review-top">
              <div class="review-avatar">${r.name.charAt(0)}</div>
              <div>
                <div class="review-name">${r.name}</div>
                <div class="review-loc">${r.city}, Colombia</div>
              </div>
            </div>
            <div class="stars">${starIcons(r.stars)}</div>
            <div class="review-text">"${r.text}"</div>
            <div class="verified">${ICONS.check}<span>Compra verificada</span></div>
          </div>
        `).join('')}
      </div>
    </div>

    <div class="related-block">
      <div class="section-title" style="margin:0 0 12px;padding:0;">
        <h2>También te puede <span>interesar</span></h2>
      </div>
      <div class="grid" style="padding:0;">
        ${relatedFallback.map(cardHtml).join('')}
      </div>
    </div>

    ${trustStripHtml()}
    ${carriersHtml()}
    ${marqueeHtml()}
    ${footerHtml()}
    ${fabsHtml()}
  `;
  bindGlobalEvents();
  tickTimers();
  startNotifications();
}

function calcDeliveryOnPage(){
  const input = document.getElementById('deliveryCityInput');
  const box = document.getElementById('deliveryResultBox');
  if(!input || !box) return;
  const est = estimateDelivery(input.value);
  if(!est){ box.className = 'delivery-result'; return; }
  box.className = 'delivery-result show ' + (est.main ? 'main' : 'other');
  box.innerHTML = `${ICONS.truck}<span>Entrega estimada: ${est.min} a ${est.max} días hábiles ${est.main ? '(ciudad principal)' : '(municipio / otra zona)'}</span>`;
}

function setGalleryImg(i){
  const p = currentProduct();
  if(!p) return;
  GALLERY_STATE.idx = i;
  document.getElementById('mainImg').src = p.imgs[i];
  document.querySelectorAll('#thumbs img').forEach((el,idx)=> el.classList.toggle('active', idx===i));
}
function currentProduct(){
  const route = currentRoute();
  return STATE.products.find(p=>p.id===route.id);
}
function changeQty(delta){
  const input = document.getElementById('qtyInput');
  let v = parseInt(input.value||'1') + delta;
  if(v<1) v=1; if(v>20) v=20;
  input.value = v;
}
function shareProduct(id){
  const url = location.origin + location.pathname + '#/producto/' + encodeURIComponent(id);
  const p = STATE.products.find(x=>x.id===id);
  if(navigator.share){
    navigator.share({title:p?p.name:'Trogüi', text:'Mira este producto en Trogüi', url}).catch(()=>{});
  } else {
    copyLink(id);
  }
}
function copyLink(id){
  const url = location.origin + location.pathname + '#/producto/' + encodeURIComponent(id);
  navigator.clipboard.writeText(url).then(()=> showToast('Enlace copiado')).catch(()=> showToast(url));
}
function showToast(msg){
  const t = document.getElementById('toast');
  if(!t) return;
  t.textContent = msg;
  t.classList.add('show');
  setTimeout(()=> t.classList.remove('show'), 2400);
}

/* ---------- MODAL: Pedido directo en la página (sin salir a WhatsApp) ---------- */
function openOrderModal(product){
  if(!product) return;
  const qtyEl = document.getElementById('qtyInput');
  const qty = qtyEl ? parseInt(qtyEl.value||'1') : 1;
  const overlay = document.createElement('div');
  overlay.className = 'modal-overlay';
  overlay.id = 'orderOverlay';
  overlay.innerHTML = `
    <div class="modal">
      <div class="modal-close" onclick="closeModal('orderOverlay')">✕</div>
      <h3>Finaliza tu pedido</h3>
      <p class="sub">Pago contra entrega. Sin anticipos, sin sorpresas.</p>
      <div class="summary-box">
        <img src="${product.imgs[0]}" alt="">
        <div>
          <div style="font-weight:700;font-size:.85rem;">${escapeHtml(product.name)}</div>
          <div style="color:var(--orange-dark);font-weight:800;">${money(product.price)} <span style="color:var(--gray);font-weight:500;font-size:.78rem;">x <span id="modalQtyLabel">${qty}</span></span></div>
        </div>
      </div>
      <form id="orderForm">
        <div class="form-row"><label>Nombre y apellido *</label><input type="text" id="f_nombre" required placeholder="Ej: María López"></div>
        <div class="form-row"><label>Teléfono / WhatsApp *</label><input type="tel" id="f_telefono" required placeholder="Ej: 3001234567"></div>
        <div class="form-row"><label>Departamento *</label><input type="text" id="f_departamento" required placeholder="Ej: Antioquia"></div>
        <div class="form-row">
          <label>Ciudad / Municipio *</label>
          <input type="text" id="f_ciudad" required placeholder="Ej: Medellín" oninput="updateDeliveryEstimateModal()">
          <div id="modalDeliveryEstimate" class="delivery-result" style="margin-top:8px;"></div>
        </div>
        <div class="form-row">
          <label>Entrega *</label>
          <div class="radio-group">
            <label class="radio-opt checked" id="opt_casa"><input type="radio" name="entrega" value="casa" checked onchange="toggleEntrega()"> Enviar a mi casa</label>
            <label class="radio-opt" id="opt_oficina"><input type="radio" name="entrega" value="oficina" onchange="toggleEntrega()"> Recoger en oficina Interrapidísimo</label>
          </div>
        </div>
        <div class="form-row" id="direccionRow"><label id="direccionLabel">Dirección completa *</label><input type="text" id="f_direccion" required placeholder="Ej: Cra 45 #12-30, Barrio Laureles"></div>
        <div class="form-row"><label>Nota (opcional)</label><textarea id="f_nota" rows="2" placeholder="Color, talla u otra indicación..."></textarea></div>
        <button type="submit" class="modal-submit" id="orderSubmitBtn">${ICONS.check}<span>Confirmar pedido</span></button>
        ${carriersHtml(true)}
      </form>
    </div>
  `;
  document.body.appendChild(overlay);
  document.getElementById('orderForm').addEventListener('submit', (e)=>{
    e.preventDefault();
    submitOrder(product, qty);
  });
}
function updateDeliveryEstimateModal(){
  const input = document.getElementById('f_ciudad');
  const box = document.getElementById('modalDeliveryEstimate');
  if(!input || !box) return;
  const est = estimateDelivery(input.value);
  if(!est){ box.className = 'delivery-result'; return; }
  box.className = 'delivery-result show ' + (est.main ? 'main' : 'other');
  box.innerHTML = `${ICONS.truck}<span>Entrega estimada: ${est.min} a ${est.max} días hábiles</span>`;
}
function toggleEntrega(){
  const casa = document.querySelector('input[name="entrega"][value="casa"]').checked;
  document.getElementById('opt_casa').classList.toggle('checked', casa);
  document.getElementById('opt_oficina').classList.toggle('checked', !casa);
  const dirRow = document.getElementById('direccionRow');
  const dirInput = document.getElementById('f_direccion');
  const dirLabel = document.getElementById('direccionLabel');
  if(casa){
    dirRow.style.display = '';
    dirInput.required = true;
    dirInput.placeholder = 'Ej: Cra 45 #12-30, Barrio Laureles';
    if(dirLabel) dirLabel.textContent = 'Dirección completa *';
  } else {
    dirRow.style.display = '';
    dirInput.required = false;
    dirInput.placeholder = 'Nombre o ubicación de la oficina (si la conoces)';
    if(dirLabel) dirLabel.textContent = 'Oficina Interrapidísimo (opcional)';
  }
}
function submitOrder(product, qty){
  const nombre = document.getElementById('f_nombre').value.trim();
  const telefono = document.getElementById('f_telefono').value.trim();
  const departamento = document.getElementById('f_departamento').value.trim();
  const ciudad = document.getElementById('f_ciudad').value.trim();
  const entrega = document.querySelector('input[name="entrega"]:checked').value;
  const direccion = document.getElementById('f_direccion').value.trim();
  const nota = document.getElementById('f_nota').value.trim();
  const total = product.price * qty;
  const est = estimateDelivery(ciudad);

  const btn = document.getElementById('orderSubmitBtn');
  if(btn){ btn.disabled = true; btn.innerHTML = 'Enviando pedido...'; }

  const order = {
    id: 'PED-' + Date.now(),
    fecha: new Date().toISOString(),
    nombre, telefono, departamento, ciudad, entrega, direccion, nota,
    producto: product.name, productoId: product.id, cantidad: qty,
    precioUnitario: product.price, total,
    entregaEstimada: est ? `${est.min}-${est.max} días hábiles` : 'Por confirmar',
    estado: 'Pendiente'
  };
  saveOrder(order);
  closeModal('orderOverlay');
  showOrderConfirmation(order);
}
function showOrderConfirmation(order){
  const overlay = document.createElement('div');
  overlay.className = 'modal-overlay';
  overlay.id = 'orderConfirmOverlay';
  const waMsg = `Hola Trogüi, acabo de hacer un pedido en la página:\n\n*Producto:* ${order.producto}\n*Cantidad:* ${order.cantidad}\n*Total:* ${money(order.total)}\n*Nombre:* ${order.nombre}\n*Teléfono:* ${order.telefono}\n*Ciudad:* ${order.ciudad}, ${order.departamento}\n*Entrega:* ${order.entrega==='casa'?'A domicilio':'Oficina Interrapidísimo'}\n${order.direccion?`*Dirección:* ${order.direccion}\n`:''}Pago contra entrega.`;
  overlay.innerHTML = `
    <div class="modal" style="text-align:center;">
      <div class="modal-close" onclick="closeModal('orderConfirmOverlay')">✕</div>
      <div style="width:56px;height:56px;border-radius:50%;background:#e9f9ee;color:#1a8a4a;display:flex;align-items:center;justify-content:center;margin:0 auto 14px;">${ICONS.check}</div>
      <h3>¡Pedido recibido!</h3>
      <p class="sub">Guardamos tu pedido #${order.id.replace('PED-','')} y te contactaremos pronto para confirmar la entrega.</p>
      <div class="summary-box" style="text-align:left;">
        <div>
          <div class="order-line"><b>Producto:</b> ${escapeHtml(order.producto)} x${order.cantidad}</div>
          <div class="order-line"><b>Total:</b> ${money(order.total)} (pago contra entrega)</div>
          <div class="order-line"><b>Entrega estimada:</b> ${order.entregaEstimada}</div>
        </div>
      </div>
      <a class="modal-submit" style="text-decoration:none;" href="https://wa.me/${WHATSAPP_NUMBER}?text=${encodeURIComponent(waMsg)}" target="_blank">${ICONS.whatsapp}<span>Avisar también por WhatsApp (opcional)</span></a>
    </div>`;
  document.body.appendChild(overlay);
}
function closeModal(id){
  const el = document.getElementById(id);
  if(el) el.remove();
}

/* ---------- PEDIDOS (panel privado, contraseña 3214) ---------- */
function openOrdersLogin(){
  const overlay = document.createElement('div');
  overlay.className = 'modal-overlay';
  overlay.id = 'ordersLoginOverlay';
  overlay.innerHTML = `
    <div class="modal" style="max-width:340px;">
      <div class="modal-close" onclick="closeModal('ordersLoginOverlay')">✕</div>
      <h3>Pedidos — acceso privado</h3>
      <p class="sub">Ingresa la clave para ver los pedidos.</p>
      <div class="form-row"><input type="password" id="ordersPassInput" placeholder="Clave"></div>
      <button class="modal-submit" style="background:var(--black);" onclick="checkOrdersPass()">Entrar</button>
    </div>`;
  document.body.appendChild(overlay);
  document.getElementById('ordersPassInput').focus();
  document.getElementById('ordersPassInput').addEventListener('keydown', e=>{ if(e.key==='Enter') checkOrdersPass(); });
}
function checkOrdersPass(){
  const val = document.getElementById('ordersPassInput').value;
  if(val === ORDERS_PASSWORD){
    closeModal('ordersLoginOverlay');
    openOrdersDashboard();
  } else {
    showToast('Clave incorrecta');
  }
}
async function openOrdersDashboard(){
  const overlay = document.createElement('div');
  overlay.className = 'modal-overlay';
  overlay.id = 'ordersDashOverlay';
  overlay.innerHTML = `
    <div class="modal wide">
      <div class="modal-close" onclick="closeModal('ordersDashOverlay')">✕</div>
      <h3>Pedidos de la tienda</h3>
      <p class="sub" id="ordersSourceNote">Cargando pedidos...</p>
      <div class="orders-summary" id="ordersSummary"></div>
      <div id="ordersList"><div class="orders-empty">Cargando...</div></div>
    </div>`;
  document.body.appendChild(overlay);
  await renderOrdersInto();
}
async function renderOrdersInto(){
  let orders = readOrders();
  let sourceNote = 'Estos pedidos están guardados en este navegador (modo local, conecta tu hoja de cálculo para verlos en línea desde cualquier dispositivo).';
  if(GOOGLE_SCRIPT_URL){
    const online = await fetchOrdersOnline();
    if(online){
      orders = online;
      sourceNote = 'Pedidos en línea, actualizados en tiempo real desde tu hoja de cálculo. Se ven igual desde cualquier celular o computador.';
    } else {
      sourceNote = 'No se pudo conectar con tu hoja de cálculo en este momento, mostrando el respaldo guardado en este navegador.';
    }
  }
  const noteEl = document.getElementById('ordersSourceNote');
  const summaryEl = document.getElementById('ordersSummary');
  const listEl = document.getElementById('ordersList');
  if(!noteEl || !summaryEl || !listEl) return; // el modal pudo haberse cerrado mientras cargaba
  const pendientes = orders.filter(o=>o.estado==='Pendiente').length;
  const entregados = orders.filter(o=>o.estado==='Entregado').length;
  noteEl.textContent = sourceNote;
  summaryEl.innerHTML = `
    <span class="pill">Total: ${orders.length}</span>
    <span class="pill">Pendientes: ${pendientes}</span>
    <span class="pill">Entregados: ${entregados}</span>
    <span class="pill" style="cursor:pointer;" onclick="renderOrdersInto()">↻ Actualizar</span>`;
  listEl.innerHTML = orders.length ? orders.map(orderCardHtml).join('') : '<div class="orders-empty">Todavía no hay pedidos registrados.</div>';
}
function orderCardHtml(o){
  const fecha = new Date(o.fecha);
  const fechaStr = fecha.toLocaleString('es-CO', {dateStyle:'medium', timeStyle:'short'});
  const estadoClass = (o.estado||'Pendiente').toLowerCase();
  return `
  <div class="order-card">
    <div class="order-card-head">
      <div>
        <b>${escapeHtml(o.nombre)}</b>
        <div class="date">${fechaStr}</div>
      </div>
      <span class="order-status ${estadoClass}">${o.estado}</span>
    </div>
    <div class="order-line"><b>Producto:</b> ${escapeHtml(o.producto)} x${o.cantidad} — ${money(o.total)}</div>
    <div class="order-line"><b>Teléfono:</b> ${escapeHtml(o.telefono)}</div>
    <div class="order-line"><b>Ubicación:</b> ${escapeHtml(o.ciudad)}, ${escapeHtml(o.departamento)}</div>
    <div class="order-line"><b>Entrega:</b> ${o.entrega==='casa'?'A domicilio':'Oficina Interrapidísimo'}${o.direccion?' — '+escapeHtml(o.direccion):''}</div>
    <div class="order-line"><b>Tiempo estimado:</b> ${o.entregaEstimada||'—'}</div>
    ${o.nota ? `<div class="order-line"><b>Nota:</b> ${escapeHtml(o.nota)}</div>` : ''}
    <div class="order-actions">
      <button class="${o.estado==='Pendiente'?'active':''}" onclick="setOrderStatus('${o.id}','Pendiente')">Pendiente</button>
      <button class="${o.estado==='Entregado'?'active':''}" onclick="setOrderStatus('${o.id}','Entregado')">Entregado</button>
      <button class="${o.estado==='Cancelado'?'active':''}" onclick="setOrderStatus('${o.id}','Cancelado')">Cancelado</button>
    </div>
  </div>`;
}
function setOrderStatus(id, status){
  updateOrderStatus(id, status);
  renderOrdersInto();
  showToast('Estado actualizado');
}

/* ---------- ASISTENTE TROGÜI (búsqueda inteligente estilo chat) ---------- */
let AI_CHAT_HISTORY = [];
function openAiChat(){
  AI_CHAT_HISTORY = [];
  const overlay = document.createElement('div');
  overlay.className = 'modal-overlay';
  overlay.id = 'aiChatOverlay';
  overlay.innerHTML = `
    <div class="modal">
      <div class="modal-close" onclick="closeModal('aiChatOverlay')">✕</div>
      <h3>Asistente Trogüi</h3>
      <p class="sub">Cuéntame qué necesitas y te recomiendo productos al instante.</p>
      <div class="ai-suggest-row">
        <span class="ai-suggest-chip" onclick="aiQuickAsk('Necesito algo para organizar la cocina')">Organizar cocina</span>
        <span class="ai-suggest-chip" onclick="aiQuickAsk('Busco un regalo para niños')">Regalo para niños</span>
        <span class="ai-suggest-chip" onclick="aiQuickAsk('Tienen algo de tecnología barato')">Tecnología barata</span>
        <span class="ai-suggest-chip" onclick="aiQuickAsk('Cuánto se demora el envío')">Tiempo de envío</span>
        <span class="ai-suggest-chip" onclick="aiQuickAsk('Dónde están ubicados')">¿Dónde están?</span>
      </div>
      <div class="ai-chat-body" id="aiChatBody"></div>
      <div class="ai-input-row">
        <input type="text" id="aiChatInput" placeholder="Escribe tu mensaje..." onkeydown="if(event.key==='Enter')aiSend()">
        <button onclick="aiSend()">${ICONS.send}</button>
      </div>
    </div>`;
  document.body.appendChild(overlay);
  aiPushBotMessage('¡Hola! Soy el asistente de Trogüi. Cuéntame qué buscas (por ejemplo "algo para la cocina" o "un regalo barato") y te muestro opciones. También puedo decirte los tiempos de envío. 😊');
}
function aiQuickAsk(text){
  document.getElementById('aiChatInput').value = text;
  aiSend();
}
function aiSend(){
  const input = document.getElementById('aiChatInput');
  const text = input.value.trim();
  if(!text) return;
  aiPushUserMessage(text);
  input.value = '';
  aiShowTyping();
  setTimeout(()=> aiRespond(text), 550 + Math.random()*500);
}
function aiPushUserMessage(text){
  AI_CHAT_HISTORY.push({role:'user', text});
  const body = document.getElementById('aiChatBody');
  const el = document.createElement('div');
  el.className = 'ai-msg user';
  el.textContent = text;
  body.appendChild(el);
  body.scrollTop = body.scrollHeight;
}
function aiPushBotMessage(html){
  const body = document.getElementById('aiChatBody');
  const el = document.createElement('div');
  el.className = 'ai-msg bot';
  el.innerHTML = html;
  body.appendChild(el);
  body.scrollTop = body.scrollHeight;
}
function aiShowTyping(){
  const body = document.getElementById('aiChatBody');
  const el = document.createElement('div');
  el.className = 'ai-msg bot ai-typing';
  el.id = 'aiTypingIndicator';
  el.innerHTML = '<span></span><span></span><span></span>';
  body.appendChild(el);
  body.scrollTop = body.scrollHeight;
}
function aiRemoveTyping(){
  const el = document.getElementById('aiTypingIndicator');
  if(el) el.remove();
}
function aiRespond(text){
  aiRemoveTyping();
  const norm = normalizeTxt(text);

  // Preguntas sobre ubicación / quiénes son
  if(/(donde estan|donde queda|ubicad|de donde son|de donde envian|sede|bodega|tienda fisica|oficina de ustedes)/.test(norm)){
    aiPushBotMessage('Somos una bodega colombiana con más de 3 años en el mercado. Estamos ubicados principalmente en <b>Bogotá</b> y también tenemos operación en <b>Cali</b>. Desde ahí despachamos a <b>toda Colombia</b>. 🇨🇴');
    return;
  }
  // Preguntas sobre transportadora
  if(/(transportadora|interrapidisimo|envia\b|coordinadora|quien envia|como envian|con que empresa)/.test(norm)){
    aiPushBotMessage('Trabajamos con transportadoras autorizadas: <b>Interrapidísimo</b>, <b>Envía</b> y <b>Coordinadora</b>, con cobertura en toda Colombia. Puedes elegir recibir en tu casa o recoger en la oficina de Interrapidísimo más cercana.');
    return;
  }
  // Preguntas sobre envío / entrega
  if(/(envio|entrega|demora|tarda|cuanto.*llega|dias)/.test(norm)){
    const cityMatch = CIUDADES_PRINCIPALES.find(c=> norm.includes(c));
    if(cityMatch || /bogota|medellin|cali|barranquilla/.test(norm)){
      aiPushBotMessage('A las ciudades principales (Bogotá, Medellín, Cali, Barranquilla y similares) la entrega es de <b>3 a 5 días hábiles</b>. Si me dices tu ciudad exacta te confirmo el tiempo.');
    } else {
      aiPushBotMessage('Para ciudades principales el envío es de <b>3 a 5 días hábiles</b>, y para municipios u otras zonas de <b>3 a 7 días hábiles</b>. Enviamos con Interrapidísimo, Envía y Coordinadora a toda Colombia, con pago contra entrega. ¿Me dices tu ciudad para calcularlo exacto?');
    }
    return;
  }
  // Preguntas sobre pago
  if(/(pago|contraentrega|contra entrega|efectivo|tarjeta)/.test(norm)){
    aiPushBotMessage('Manejamos <b>pago contra entrega</b> en toda Colombia: pagas cuando el pedido llega a tus manos, sin anticipos. 👍');
    return;
  }
  // Preguntas sobre garantía
  if(/(garantia|devolucion|cambio|dañado|no sirve)/.test(norm)){
    aiPushBotMessage('Todos nuestros productos tienen <b>garantía de 30 a 60 días</b> según el artículo, y tienes <b>5 días hábiles</b> desde la entrega para reportar cualquier inconveniente.');
    return;
  }
  // Búsqueda de productos
  const matches = STATE.products.filter(p=> fuzzyIncludes(p.name+' '+p.desc+' '+(CAT_LABELS[p.cat]?.label||p.cat), text)).slice(0,3);
  if(matches.length){
    let html = `Encontré esto para ti:`;
    matches.forEach(p=>{
      html += `<div class="mini-product" onclick="closeModal('aiChatOverlay');goToProduct('${p.id}')">
        <img src="${p.imgs[0]}" onerror="this.onerror=null;this.src='${PLACEHOLDER_IMG}';">
        <div><div class="mp-name">${escapeHtml(p.name)}</div><div class="mp-price">${money(p.price)}</div></div>
      </div>`;
    });
    html += `<div style="margin-top:8px;font-size:.78rem;color:var(--gray);">Haz clic en un producto para verlo completo.</div>`;
    aiPushBotMessage(html);
    return;
  }
  // Búsqueda por categoría
  const catKey = Object.keys(CAT_LABELS).find(c=> norm.includes(c) || norm.includes(normalizeTxt(CAT_LABELS[c].label)));
  if(catKey){
    const catMatches = STATE.products.filter(p=>p.cat===catKey).slice(0,3);
    let html = `Mira algunas opciones en ${CAT_LABELS[catKey].label}:`;
    catMatches.forEach(p=>{
      html += `<div class="mini-product" onclick="closeModal('aiChatOverlay');goToProduct('${p.id}')">
        <img src="${p.imgs[0]}" onerror="this.onerror=null;this.src='${PLACEHOLDER_IMG}';">
        <div><div class="mp-name">${escapeHtml(p.name)}</div><div class="mp-price">${money(p.price)}</div></div>
      </div>`;
    });
    aiPushBotMessage(html);
    return;
  }
  aiPushBotMessage('No encontré algo exacto con esas palabras. Prueba contándome para qué lo necesitas (por ejemplo: "algo para la cocina", "un regalo", "tecnología") o escríbenos por WhatsApp y te ayudamos personalmente. 🙂');
}

/* ---------- ADMIN DE PRODUCTOS (contraseña 4325) ---------- */
function openAdminLogin(){
  const overlay = document.createElement('div');
  overlay.className = 'modal-overlay';
  overlay.id = 'adminLoginOverlay';
  overlay.innerHTML = `
    <div class="modal" style="max-width:340px;">
      <div class="modal-close" onclick="closeModal('adminLoginOverlay')">✕</div>
      <h3>Panel de administración</h3>
      <p class="sub">Ingresa la clave para editar productos.</p>
      <div class="form-row"><input type="password" id="adminPassInput" placeholder="Clave"></div>
      <button class="modal-submit" style="background:var(--black);" onclick="checkAdminPass()">Entrar</button>
    </div>`;
  document.body.appendChild(overlay);
  document.getElementById('adminPassInput').focus();
  document.getElementById('adminPassInput').addEventListener('keydown', e=>{ if(e.key==='Enter') checkAdminPass(); });
}
function checkAdminPass(){
  const val = document.getElementById('adminPassInput').value;
  if(val === ADMIN_PASS){
    closeModal('adminLoginOverlay');
    openAdminDashboard();
  } else {
    showToast('Clave incorrecta');
  }
}
function openAdminDashboard(){
  const overlay = document.createElement('div');
  overlay.className = 'modal-overlay';
  overlay.id = 'adminDashOverlay';
  const products = getAllProducts();
  overlay.innerHTML = `
    <div class="modal wide">
      <div class="modal-close" onclick="closeModal('adminDashOverlay')">✕</div>
      <h3>Panel Trogüi — Productos</h3>
      <p class="sub">Edita precio, descripción, imágenes o elimina productos.</p>
      <div class="admin-actions-top">
        <button onclick="openProductEditor(null)">Agregar producto nuevo</button>
        <button onclick="resetAllOverrides()" style="background:var(--black);">Restablecer todo</button>
      </div>
      <div class="admin-list" id="adminList">
        ${products.map(p=>`
          <div class="admin-row">
            <img src="${p.imgs[0]||''}">
            <div class="info">
              <b>${escapeHtml(p.name)}</b>
              <small>${money(p.price)} · ${p.cat}</small>
            </div>
            <button onclick="openProductEditor('${p.id}')">Editar</button>
            <button class="del" onclick="deleteProduct('${p.id}')">Eliminar</button>
          </div>
        `).join('')}
      </div>
    </div>`;
  document.body.appendChild(overlay);
}
function resetAllOverrides(){
  if(!confirm('¿Restablecer todos los productos a su versión original? Se perderán tus ediciones.')) return;
  writeStore({overrides:{}, custom:[], deleted:[]});
  closeModal('adminDashOverlay');
  STATE.order = [];
  render();
  showToast('Tienda restablecida');
}
function deleteProduct(id){
  if(!confirm('¿Eliminar este producto de la tienda?')) return;
  const store = readStore();
  const isCustom = store.custom.some(p=>p.id===id);
  if(isCustom){ store.custom = store.custom.filter(p=>p.id!==id); }
  else if(!store.deleted.includes(id)){ store.deleted.push(id); }
  writeStore(store);
  closeModal('adminDashOverlay');
  STATE.order = [];
  render();
  openAdminDashboard();
  showToast('Producto eliminado');
}

let EDITOR_IMGS = [];
function openProductEditor(id){
  const isNew = !id;
  const p = isNew
    ? {id:'CUST' + Date.now(), name:'', cat:'hogar', price:0, oldPrice:0, desc:'', imgs:[], sold:0, stars:5, lastUnits:false, timer:3600}
    : getAllProducts().find(x=>x.id===id);
  if(!p) return;
  EDITOR_IMGS = [...(p.imgs||[])];
  const overlay = document.createElement('div');
  overlay.className = 'modal-overlay';
  overlay.id = 'editorOverlay';
  overlay.innerHTML = `
    <div class="modal wide">
      <div class="modal-close" onclick="closeModal('editorOverlay')">✕</div>
      <h3>${isNew ? 'Nuevo producto' : 'Editar producto'}</h3>
      <div class="form-row"><label>Nombre</label><input id="e_name" value="${escapeHtml(p.name)}"></div>
      <div class="form-row"><label>Categoría</label>
        <select id="e_cat">
          ${Object.keys(CAT_LABELS).map(c=>`<option value="${c}" ${p.cat===c?'selected':''}>${CAT_LABELS[c].label}</option>`).join('')}
        </select>
      </div>
      <div class="form-row" style="display:flex;gap:10px;">
        <div style="flex:1;"><label>Precio actual</label><input id="e_price" type="number" value="${p.price}"></div>
        <div style="flex:1;"><label>Precio antes (tachado)</label><input id="e_oldprice" type="number" value="${p.oldPrice||0}"></div>
      </div>
      <div class="form-row"><label>Descripción</label><textarea id="e_desc" rows="4">${escapeHtml(p.desc)}</textarea></div>
      <div class="form-row">
        <label>Imágenes</label>
        <div class="img-chip-list" id="imgChipList">${renderImgChips()}</div>
        <div style="display:flex;gap:8px;">
          <input id="e_imgurl" placeholder="Pegar link de imagen..." style="flex:1;">
          <button type="button" onclick="addImgUrl()" style="background:var(--black);color:#fff;padding:0 14px;border-radius:8px;">Agregar</button>
        </div>
        <div style="margin-top:8px;">
          <input type="file" id="e_imgfile" accept="image/*" multiple onchange="addImgFile(event)">
          <div style="font-size:.7rem;color:var(--gray);margin-top:4px;">También puedes subir fotos directo desde la galería del celular.</div>
        </div>
      </div>
      <div class="form-row" style="display:flex;gap:10px;">
        <div style="flex:1;"><label>Vendidos</label><input id="e_sold" type="number" value="${p.sold}"></div>
        <div style="flex:1;"><label>Estrellas (1-5)</label><input id="e_stars" type="number" min="1" max="5" value="${p.stars}"></div>
      </div>
      <div class="form-row"><label><input type="checkbox" id="e_last" style="width:auto;" ${p.lastUnits?'checked':''}> Marcar como "últimas unidades"</label></div>
      <button class="modal-submit" style="background:var(--orange);" onclick="saveProduct('${isNew?'':id}')">Guardar producto</button>
    </div>`;
  document.body.appendChild(overlay);
}
function renderImgChips(){
  return EDITOR_IMGS.map((im,i)=>`<div class="img-chip"><img src="${im}"><div class="rm" onclick="removeImgChip(${i})">✕</div></div>`).join('')
    || '<div style="font-size:.75rem;color:var(--gray);">Sin imágenes aún</div>';
}
function refreshImgChips(){ document.getElementById('imgChipList').innerHTML = renderImgChips(); }
function addImgUrl(){
  const input = document.getElementById('e_imgurl');
  const val = input.value.trim();
  if(val){ EDITOR_IMGS.push(val); input.value=''; refreshImgChips(); }
}
function addImgFile(evt){
  const files = Array.from(evt.target.files||[]);
  files.forEach(file=>{
    const reader = new FileReader();
    reader.onload = e=>{ EDITOR_IMGS.push(e.target.result); refreshImgChips(); };
    reader.readAsDataURL(file);
  });
}
function removeImgChip(i){ EDITOR_IMGS.splice(i,1); refreshImgChips(); }

function saveProduct(id){
  const name = document.getElementById('e_name').value.trim();
  const cat = document.getElementById('e_cat').value;
  const price = parseFloat(document.getElementById('e_price').value)||0;
  const oldPrice = parseFloat(document.getElementById('e_oldprice').value)||0;
  const desc = document.getElementById('e_desc').value.trim();
  const sold = parseInt(document.getElementById('e_sold').value)||0;
  const stars = Math.min(5,Math.max(1, parseInt(document.getElementById('e_stars').value)||5));
  const lastUnits = document.getElementById('e_last').checked;
  if(!name || !EDITOR_IMGS.length){ showToast('Falta nombre o al menos una imagen'); return; }

  const store = readStore();
  if(id){
    store.overrides[id] = {name, cat, price, oldPrice, desc, sold, stars, lastUnits, imgs:[...EDITOR_IMGS]};
  } else {
    store.custom.push({id:'CUST'+Date.now(), name, cat, price, oldPrice, desc, sold, stars, lastUnits, imgs:[...EDITOR_IMGS], timer:3600});
  }
  writeStore(store);
  closeModal('editorOverlay');
  closeModal('adminDashOverlay');
  STATE.order = [];
  render();
  showToast('Producto guardado');
}

/* ---------- Arranque ---------- */
render();

</script>
</body>
</html>
