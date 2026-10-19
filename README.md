<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>JHULEY · Accesorios y Detalles</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Playfair+Display:wght@600;700;800&family=Sacramento&display=swap" rel="stylesheet">
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<style>
:root{
  --rose:#d81b60; --rose-d:#ad1457; --rose-l:#ff80ab; --blush:#ffe4ec; --cream:#fff7f9; --gold:#c9a24b;
  --bg:#fff7f9; --card:#ffffff; --text:#2b1a22; --muted:#7a6670; --line:#f6d5df;
  --shadow:0 10px 30px rgba(216,27,96,.10); --shadow-lg:0 20px 50px rgba(216,27,96,.18);
  --radius:20px;
}
body.dark{
  --bg:#150b10; --card:#221219; --text:#fde8ef; --muted:#c3a3b0; --line:#3b1f2b; --blush:#2f1722;
  --rose:#ff6f9f; --rose-d:#ff4081; --shadow:0 10px 30px rgba(0,0,0,.4); --shadow-lg:0 20px 50px rgba(0,0,0,.5);
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{font-family:'Poppins',sans-serif;background:var(--bg);color:var(--text);line-height:1.6;transition:background .4s,color .4s;overflow-x:hidden}
h1,h2,h3{font-family:'Playfair Display',serif;line-height:1.2}
img{max-width:100%;display:block}
a{color:inherit;text-decoration:none}
button{font-family:inherit;cursor:pointer}
.wrap{max-width:1180px;margin:0 auto;padding:0 20px}
section{padding:80px 0}
.eyebrow{display:inline-block;font-size:.78rem;font-weight:600;letter-spacing:.14em;text-transform:uppercase;color:var(--rose);background:var(--blush);padding:6px 14px;border-radius:30px;margin-bottom:14px}
.sec-head{text-align:center;max-width:680px;margin:0 auto 48px}
.sec-head h2{font-size:clamp(1.9rem,4vw,2.7rem);margin-bottom:12px}
.sec-head p{color:var(--muted)}
.reveal{opacity:0;transform:translateY(28px);transition:opacity .7s ease,transform .7s ease}
.reveal.show{opacity:1;transform:none}
.hidden-sec{display:none!important}

/* ---------- Bienvenida ---------- */
#welcome{position:fixed;inset:0;z-index:9999;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;padding:20px;
  background:radial-gradient(circle at 20% 20%,#ffd1dc 0,transparent 45%),radial-gradient(circle at 80% 80%,#ff94b8 0,transparent 45%),linear-gradient(135deg,#ffb1c1,#ffd9e2);
  transition:opacity .9s,visibility .9s;overflow:hidden}
#welcome.out{opacity:0;visibility:hidden}
#welcome .logo-script{font-family:'Sacramento',cursive;font-size:clamp(4rem,12vw,7.5rem);color:#fff;text-shadow:0 6px 22px rgba(173,20,87,.35);z-index:2;line-height:1}
#welcome .tag{color:#fff;font-weight:500;letter-spacing:.35em;text-transform:uppercase;font-size:.85rem;margin:6px 0 10px;z-index:2}
#welcome p.sub{color:#fff;font-size:1.15rem;margin-bottom:34px;z-index:2;text-shadow:0 1px 4px rgba(0,0,0,.15)}
.btn-enter{z-index:2;background:#fff;color:var(--rose-d);border:none;padding:16px 46px;border-radius:50px;font-weight:600;font-size:1.1rem;box-shadow:0 12px 30px rgba(173,20,87,.3);transition:.3s}
.btn-enter:hover{transform:translateY(-3px) scale(1.04)}
.float-p{position:absolute;animation:floatUp linear infinite;opacity:.9;pointer-events:none;z-index:1}
@keyframes floatUp{0%{transform:translateY(110vh) rotate(0);opacity:0}15%{opacity:.9}85%{opacity:.9}100%{transform:translateY(-15vh) rotate(360deg);opacity:0}}

/* ---------- Cierre ---------- */
#exit{position:fixed;inset:0;z-index:-1;opacity:0;visibility:hidden;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;padding:20px;
  background:linear-gradient(135deg,#ffc0cb,#ff94b8);color:#880e4f;transition:opacity .8s;overflow:hidden}
#exit.active{z-index:10000;opacity:1;visibility:visible}
#exit h1{font-family:'Sacramento',cursive;font-size:clamp(2.8rem,8vw,5rem);color:#ad1457;text-shadow:2px 2px 6px rgba(255,255,255,.6)}
#exit button{margin-top:26px;background:#fff;color:var(--rose-d);border:none;padding:12px 30px;border-radius:40px;font-weight:600}
.fall{position:absolute;top:-10vh;animation:fall linear forwards;pointer-events:none}
@keyframes fall{to{transform:translateY(115vh) rotate(360deg);opacity:0}}

/* ---------- Anuncio + Nav ---------- */
.topbar{background:linear-gradient(90deg,var(--rose-d),var(--rose),#ff6090);color:#fff;text-align:center;font-size:.82rem;padding:8px 12px;font-weight:500}
nav{position:sticky;top:0;z-index:500;background:color-mix(in srgb,var(--card) 88%,transparent);backdrop-filter:blur(14px);border-bottom:1px solid var(--line)}
.nav-in{display:flex;align-items:center;justify-content:space-between;height:68px;gap:16px}
.brand{font-family:'Sacramento',cursive;font-size:2.4rem;color:var(--rose);line-height:1}
.brand small{font-family:'Poppins';font-size:.62rem;letter-spacing:.2em;color:var(--muted);display:block;margin-top:-4px;text-transform:uppercase}
.nav-links{display:flex;gap:26px;font-size:.9rem;font-weight:500}
.nav-links a{color:var(--muted);transition:.2s;position:relative}
.nav-links a:hover{color:var(--rose)}
.nav-links a::after{content:"";position:absolute;left:0;bottom:-6px;width:0;height:2px;background:var(--rose);transition:.3s}
.nav-links a:hover::after{width:100%}
.nav-actions{display:flex;gap:10px;align-items:center}
.icon-btn{position:relative;width:42px;height:42px;border-radius:50%;border:1px solid var(--line);background:var(--card);color:var(--text);font-size:1.1rem;display:flex;align-items:center;justify-content:center;transition:.2s}
.icon-btn:hover{border-color:var(--rose);transform:translateY(-2px)}
.badge{position:absolute;top:-5px;right:-5px;background:var(--rose);color:#fff;border-radius:50%;min-width:20px;height:20px;font-size:.7rem;font-weight:700;display:flex;align-items:center;justify-content:center;padding:0 4px}
@media(max-width:860px){.nav-links{display:none}}

/* ---------- Hero ---------- */
.hero{padding:70px 0 90px;background:radial-gradient(circle at 85% 15%,#ffd1dc 0,transparent 40%),radial-gradient(circle at 5% 90%,#ffe9a8 0,transparent 30%),var(--bg);position:relative;overflow:hidden}
body.dark .hero{background:radial-gradient(circle at 85% 15%,#4a1525 0,transparent 40%),var(--bg)}
.hero-grid{display:grid;grid-template-columns:1.1fr .9fr;gap:50px;align-items:center}
.hero h1{font-size:clamp(2.4rem,5.4vw,4.1rem);margin-bottom:18px}
.hero h1 em{font-style:normal;background:linear-gradient(90deg,var(--rose),#ff6090,var(--gold));-webkit-background-clip:text;background-clip:text;color:transparent}
.hero p.lead{font-size:1.1rem;color:var(--muted);max-width:520px;margin-bottom:30px}
.cta-row{display:flex;gap:14px;flex-wrap:wrap}
.btn{border:none;border-radius:50px;padding:14px 30px;font-weight:600;font-size:.95rem;transition:.25s;display:inline-flex;align-items:center;gap:8px}
.btn-primary{background:linear-gradient(135deg,var(--rose),#ff4081);color:#fff;box-shadow:0 10px 24px rgba(216,27,96,.35)}
.btn-primary:hover{transform:translateY(-3px);box-shadow:0 14px 30px rgba(216,27,96,.45)}
.btn-ghost{background:var(--card);color:var(--rose);border:2px solid var(--line)}
.btn-ghost:hover{border-color:var(--rose)}
.hero-stats{display:flex;gap:34px;margin-top:42px;flex-wrap:wrap}
.hero-stats b{font-family:'Playfair Display';font-size:2rem;color:var(--rose);display:block;line-height:1}
.hero-stats span{font-size:.82rem;color:var(--muted)}
.hero-art{position:relative;height:420px}
.blob{position:absolute;border-radius:36px;box-shadow:var(--shadow-lg);display:flex;align-items:center;justify-content:center;font-size:5rem;animation:bob 5s ease-in-out infinite}
.blob.b1{width:210px;height:250px;left:6%;top:6%;background:linear-gradient(145deg,#ffb1c1,#ff80ab);transform:rotate(-6deg)}
.blob.b2{width:190px;height:220px;right:4%;top:0;background:linear-gradient(145deg,#ffe9a8,#ffc971);animation-delay:-1.5s;transform:rotate(7deg)}
.blob.b3{width:230px;height:190px;left:24%;bottom:0;background:linear-gradient(145deg,#d1c4ff,#f8bbd0);animation-delay:-3s;transform:rotate(3deg)}
@keyframes bob{50%{translate:0 -14px}}
.chip-float{position:absolute;background:var(--card);border-radius:14px;padding:10px 16px;font-size:.8rem;font-weight:600;box-shadow:var(--shadow);right:0;bottom:50px;z-index:3}
@media(max-width:860px){.hero-grid{grid-template-columns:1fr}.hero-art{height:320px}}

/* ---------- Beneficios ---------- */
.perks{margin-top:-46px;position:relative;z-index:5}
.perk-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:16px}
.perk{background:var(--card);border-radius:var(--radius);padding:22px;display:flex;gap:14px;align-items:center;box-shadow:var(--shadow);border:1px solid var(--line)}
.perk .ic{width:50px;height:50px;border-radius:14px;background:var(--blush);display:flex;align-items:center;justify-content:center;font-size:1.5rem;flex-shrink:0}
.perk b{display:block;font-size:.92rem}.perk span{font-size:.8rem;color:var(--muted)}

/* ---------- Catálogo ---------- */
.filters{display:flex;gap:10px;justify-content:center;flex-wrap:wrap;margin-bottom:34px}
.filter{background:var(--card);border:1px solid var(--line);color:var(--muted);padding:9px 20px;border-radius:30px;font-weight:500;font-size:.88rem;transition:.2s}
.filter:hover{color:var(--rose);border-color:var(--rose)}
.filter.on{background:var(--rose);color:#fff;border-color:var(--rose);box-shadow:0 8px 18px rgba(216,27,96,.3)}
.search{max-width:360px;margin:0 auto 28px;display:block;width:100%;padding:12px 20px;border-radius:30px;border:1px solid var(--line);background:var(--card);color:var(--text);font-family:inherit;outline:none}
.search:focus{border-color:var(--rose)}
.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(250px,1fr));gap:24px}
.card{background:var(--card);border-radius:var(--radius);overflow:hidden;border:1px solid var(--line);box-shadow:var(--shadow);transition:.3s;display:flex;flex-direction:column}
.card:hover{transform:translateY(-8px);box-shadow:var(--shadow-lg)}
.card .pic{position:relative;height:210px;overflow:hidden;display:flex;align-items:center;justify-content:center;font-size:5rem}
.card .pic img{position:absolute;inset:0;width:100%;height:100%;object-fit:cover;transition:.5s}
.card:hover .pic img{transform:scale(1.08)}
.tag{position:absolute;top:12px;left:12px;font-size:.7rem;font-weight:700;padding:5px 12px;border-radius:30px;color:#fff;z-index:2;letter-spacing:.04em}
.tag.new{background:#00b894}.tag.hot{background:#ff5252}.tag.off{background:#6c5ce7}.tag.top{background:var(--gold)}
.fav{position:absolute;top:10px;right:10px;z-index:2;width:36px;height:36px;border-radius:50%;border:none;background:rgba(255,255,255,.92);font-size:1rem;transition:.2s}
.fav:hover{transform:scale(1.15)}
.card .body{padding:18px;display:flex;flex-direction:column;gap:6px;flex:1}
.card .cat{font-size:.72rem;color:var(--rose);font-weight:600;letter-spacing:.1em;text-transform:uppercase}
.card h3{font-family:'Poppins';font-size:1.02rem;font-weight:600}
.card .desc{font-size:.82rem;color:var(--muted);flex:1}
.stars{color:#f5b301;font-size:.8rem;letter-spacing:2px}
.price-row{display:flex;align-items:center;justify-content:space-between;margin-top:8px}
.price{font-family:'Playfair Display';font-size:1.35rem;font-weight:700;color:var(--rose)}
.price s{font-family:'Poppins';font-size:.8rem;color:var(--muted);font-weight:400;margin-left:6px}
.add{background:var(--rose);color:#fff;border:none;border-radius:50px;padding:9px 16px;font-size:.82rem;font-weight:600;transition:.2s}
.add:hover{background:var(--rose-d);transform:scale(1.06)}
.empty{grid-column:1/-1;text-align:center;color:var(--muted);padding:40px}

/* ---------- Combos ---------- */
.combos{background:linear-gradient(135deg,var(--blush),var(--bg))}
.combo-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(290px,1fr));gap:24px}
.combo{border-radius:var(--radius);padding:30px;color:#fff;position:relative;overflow:hidden;box-shadow:var(--shadow-lg);min-height:230px;display:flex;flex-direction:column;justify-content:flex-end}
.combo .big{position:absolute;right:-10px;top:-14px;font-size:8rem;opacity:.25}
.combo h3{font-size:1.5rem;margin-bottom:6px}.combo p{font-size:.88rem;opacity:.95;margin-bottom:14px}
.combo .btn{background:#fff;color:var(--rose-d);align-self:flex-start;padding:10px 22px}
.c1{background:linear-gradient(135deg,#e91e63,#ff6090)}.c2{background:linear-gradient(135deg,#8e24aa,#ec407a)}.c3{background:linear-gradient(135deg,#f57c00,#ff7aa2)}

/* ---------- Ruleta ---------- */
.roulette-box{display:grid;grid-template-columns:1fr 1fr;gap:40px;align-items:center;background:var(--card);border-radius:30px;padding:46px;box-shadow:var(--shadow-lg);border:1px solid var(--line)}
.wheel-wrap{position:relative;width:min(340px,80vw);aspect-ratio:1;margin:0 auto}
.pointer{position:absolute;top:-14px;left:50%;translate:-50% 0;z-index:5;width:0;height:0;border-left:15px solid transparent;border-right:15px solid transparent;border-top:30px solid var(--rose-d);filter:drop-shadow(0 4px 4px rgba(0,0,0,.25))}
.wheel{width:100%;height:100%;border-radius:50%;border:8px solid #fff;box-shadow:0 0 0 4px var(--rose-l),var(--shadow-lg);position:relative;overflow:hidden;
  background:conic-gradient(#ffd1dc 0 60deg,#ffb1c1 60deg 120deg,#f8bbd0 120deg 180deg,#ffc2d1 180deg 240deg,#ff94b8 240deg 300deg,#ffe3ea 300deg 360deg);
  transition:transform 5s cubic-bezier(.12,.8,.1,1)}
.wheel .lab{position:absolute;inset:0;display:flex;justify-content:center;padding-top:30px;color:#5a0a2b;font-weight:700;font-size:.78rem;text-align:center}
.wheel .lab span{width:70px}
.hub{position:absolute;left:50%;top:50%;translate:-50% -50%;width:62px;height:62px;border-radius:50%;background:#fff;z-index:4;display:flex;align-items:center;justify-content:center;font-size:1.6rem;box-shadow:0 4px 14px rgba(0,0,0,.2)}
#prize{margin-top:18px;padding:14px 18px;border-radius:14px;background:var(--blush);font-weight:600;color:var(--rose);min-height:52px}
@media(max-width:860px){.roulette-box{grid-template-columns:1fr;padding:28px}}

/* ---------- Estrategia ---------- */
.foda-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:20px}
.foda{background:var(--card);border-radius:var(--radius);padding:26px;border:1px solid var(--line);border-top-width:5px;box-shadow:var(--shadow)}
.foda h3{font-family:'Poppins';font-size:1.05rem;margin-bottom:12px}
.foda ul{list-style:none}.foda li{font-size:.88rem;color:var(--muted);padding:5px 0 5px 22px;position:relative}
.foda li::before{content:"✦";position:absolute;left:0;color:inherit}
.f-f{border-top-color:#2e7d32}.f-f h3,.f-f li::before{color:#2e7d32}
.f-o{border-top-color:#1565c0}.f-o h3,.f-o li::before{color:#1565c0}
.f-d{border-top-color:#ef6c00}.f-d h3,.f-d li::before{color:#ef6c00}
.f-a{border-top-color:#c62828}.f-a h3,.f-a li::before{color:#c62828}
.two{display:grid;grid-template-columns:1fr 1fr;gap:24px;margin-top:30px}
.panel{background:var(--card);border-radius:var(--radius);padding:28px;border:1px solid var(--line);box-shadow:var(--shadow)}
.panel h3{font-size:1.3rem;margin-bottom:14px;color:var(--rose)}
.panel ul{padding-left:18px;color:var(--muted);font-size:.9rem}.panel li{margin:6px 0}
.persona{display:flex;gap:16px;align-items:center;margin-bottom:16px}
.avatar{width:70px;height:70px;border-radius:50%;background:linear-gradient(135deg,#ffb1c1,#ff80ab);display:flex;align-items:center;justify-content:center;font-size:2.2rem}
table{width:100%;border-collapse:collapse;font-size:.88rem}
th,td{padding:11px 12px;text-align:left;border-bottom:1px solid var(--line)}
th{color:var(--rose);font-size:.75rem;letter-spacing:.08em;text-transform:uppercase}
@media(max-width:860px){.two{grid-template-columns:1fr}}

/* ---------- Cronograma ---------- */
.timeline{position:relative;max-width:820px;margin:0 auto}
.timeline::before{content:"";position:absolute;left:23px;top:0;bottom:0;width:3px;background:linear-gradient(var(--rose),var(--rose-l),var(--line));border-radius:3px}
.step{position:relative;padding:0 0 26px 70px}
.dot{position:absolute;left:0;top:0;width:48px;height:48px;border-radius:50%;background:var(--rose);color:#fff;font-weight:700;display:flex;align-items:center;justify-content:center;box-shadow:0 0 0 6px var(--bg),0 8px 18px rgba(216,27,96,.35)}
.step .box{background:var(--card);border:1px solid var(--line);border-radius:16px;padding:16px 20px;box-shadow:var(--shadow)}
.step b{display:block}.step small{color:var(--muted)}
.step .when{float:right;background:var(--blush);color:var(--rose);font-size:.72rem;font-weight:700;padding:4px 12px;border-radius:20px}
.charts{display:grid;grid-template-columns:1fr 1fr;gap:24px;margin-top:50px}
.charts .panel canvas{max-height:280px}
@media(max-width:860px){.charts{grid-template-columns:1fr}}

/* ---------- Multimedia ---------- */
.video-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(300px,1fr));gap:24px}
.vbox{background:var(--card);border-radius:var(--radius);padding:18px;border:1px solid var(--line);box-shadow:var(--shadow)}
.vbox p{font-weight:600;font-size:.9rem;margin-bottom:10px}
.ratio{position:relative;padding-bottom:56.25%;border-radius:14px;overflow:hidden}
.ratio iframe{position:absolute;inset:0;width:100%;height:100%;border:0}
.local-video{width:100%;border-radius:14px;max-height:320px;background:#000}

/* ---------- Opiniones ---------- */
.final{background:linear-gradient(rgba(255,240,245,.88),rgba(255,226,236,.92)),url('PAL FINAL.avif') center/cover,linear-gradient(135deg,#ffe4ec,#ffc2d1);color:#2b1a22}
body.dark .final{background:linear-gradient(rgba(21,11,16,.9),rgba(34,18,25,.93)),url('PAL FINAL.avif') center/cover,#150b10;color:#fde8ef}
.testi-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:20px;margin-bottom:40px}
.testi{background:var(--card);border-radius:var(--radius);padding:24px;box-shadow:var(--shadow);border:1px solid var(--line)}
.testi p{font-size:.9rem;color:var(--muted);margin:10px 0 14px;font-style:italic}
.testi .who{display:flex;gap:10px;align-items:center;font-size:.85rem;font-weight:600}
.testi .who i{width:36px;height:36px;border-radius:50%;background:var(--blush);display:flex;align-items:center;justify-content:center;font-style:normal}
.reactions{display:flex;gap:12px;justify-content:center;flex-wrap:wrap;margin-bottom:30px}
.react{background:var(--card);border:2px solid var(--line);border-radius:50px;padding:10px 20px;font-size:1.3rem;transition:.2s;color:var(--text)}
.react:hover{transform:scale(1.12);border-color:var(--rose)}
.react b{font-size:.85rem;margin-left:6px;color:var(--rose)}
.comment-box{max-width:680px;margin:0 auto;background:var(--card);padding:26px;border-radius:var(--radius);box-shadow:var(--shadow);border:1px solid var(--line)}
textarea{width:100%;height:90px;border-radius:12px;border:2px solid var(--line);background:var(--bg);color:var(--text);padding:12px;font-family:inherit;resize:vertical;outline:none}
textarea:focus{border-color:var(--rose)}
#comments{margin-top:16px;max-height:190px;overflow:auto}
.cm{padding:9px 12px;border-bottom:1px solid var(--line);font-size:.88rem}
.snoopy{display:flex;align-items:center;gap:18px;justify-content:center;margin:34px auto 0;max-width:680px;background:var(--card);padding:16px 22px;border-radius:18px;border:2px dashed var(--rose-l)}
.snoopy img{width:96px;height:96px;object-fit:contain;animation:wig .6s infinite alternate}
@keyframes wig{from{transform:rotate(-4deg)}to{transform:translateY(-8px) rotate(4deg)}}

/* ---------- Footer ---------- */
footer{background:#2b0f1c;color:#f5d3df;padding:56px 0 24px}
.f-grid{display:grid;grid-template-columns:2fr 1fr 1fr;gap:34px;margin-bottom:30px}
footer .brand{color:#ff80ab}footer h4{margin-bottom:12px;font-family:'Poppins';font-size:.95rem}
footer p,footer li{font-size:.85rem;color:#d9aebf;list-style:none;margin:6px 0}
footer .copy{border-top:1px solid #4a2234;padding-top:18px;text-align:center;font-size:.8rem;color:#b88a9c}
.close-btn{margin-top:16px;background:none;border:1px solid #ff80ab;color:#ff80ab;border-radius:30px;padding:9px 24px;font-weight:600}
.close-btn:hover{background:#ff80ab;color:#2b0f1c}
@media(max-width:700px){.f-grid{grid-template-columns:1fr}}

/* ---------- Carrito lateral ---------- */
.overlay{position:fixed;inset:0;background:rgba(0,0,0,.45);opacity:0;visibility:hidden;transition:.3s;z-index:900}
.overlay.on{opacity:1;visibility:visible}
.drawer{position:fixed;top:0;right:0;height:100%;width:min(420px,100%);background:var(--card);z-index:950;transform:translateX(105%);transition:transform .4s cubic-bezier(.2,.8,.2,1);display:flex;flex-direction:column;box-shadow:-20px 0 50px rgba(0,0,0,.25)}
.drawer.on{transform:none}
.d-head{display:flex;justify-content:space-between;align-items:center;padding:20px 24px;border-bottom:1px solid var(--line)}
.d-head h3{font-size:1.3rem;color:var(--rose)}
.d-items{flex:1;overflow:auto;padding:12px 24px}
.item{display:flex;gap:12px;align-items:center;padding:14px 0;border-bottom:1px solid var(--line)}
.item .em{width:52px;height:52px;border-radius:12px;background:var(--blush);display:flex;align-items:center;justify-content:center;font-size:1.7rem;flex-shrink:0}
.item .nm{flex:1;font-size:.88rem;font-weight:600}.item .nm small{display:block;color:var(--muted);font-weight:400}
.qty{display:flex;align-items:center;gap:8px}
.qty button{width:26px;height:26px;border-radius:50%;border:1px solid var(--line);background:var(--bg);color:var(--text);font-weight:700}
.qty button:hover{border-color:var(--rose);color:var(--rose)}
.d-foot{padding:20px 24px;border-top:1px solid var(--line);background:var(--bg)}
.d-foot select{width:100%;padding:10px;border-radius:10px;border:1px solid var(--line);background:var(--card);color:var(--text);font-family:inherit;margin-bottom:12px}
.line{display:flex;justify-content:space-between;font-size:.88rem;margin:4px 0;color:var(--muted)}
.line.total{font-size:1.15rem;font-weight:700;color:var(--text);margin-top:10px}
.line.disc{color:#00a67e}
.btn-wa{width:100%;justify-content:center;margin-top:14px;background:#25d366;color:#fff;box-shadow:0 10px 24px rgba(37,211,102,.35)}
.btn-wa:hover{transform:translateY(-2px)}
.mini-clear{background:none;border:none;color:var(--muted);font-size:.78rem;text-decoration:underline;margin-top:8px}

/* ---------- Flotantes ---------- */
.wa-float{position:fixed;bottom:24px;right:24px;width:60px;height:60px;border-radius:50%;background:#25d366;color:#fff;font-size:1.8rem;display:flex;align-items:center;justify-content:center;box-shadow:0 8px 24px rgba(37,211,102,.5);z-index:800;animation:pulse 2.2s infinite}
@keyframes pulse{0%{box-shadow:0 0 0 0 rgba(37,211,102,.55)}70%{box-shadow:0 0 0 18px rgba(37,211,102,0)}100%{box-shadow:0 0 0 0 rgba(37,211,102,0)}}
.settings{position:fixed;bottom:24px;left:24px;z-index:800}
.settings .panel-s{position:absolute;bottom:56px;left:0;width:260px;background:var(--card);border:1px solid var(--line);border-radius:16px;padding:16px;box-shadow:var(--shadow-lg);display:none}
.settings .panel-s.on{display:block}
.settings label{display:flex;gap:8px;align-items:center;font-size:.85rem;margin:7px 0;cursor:pointer}
.toast{position:fixed;left:50%;bottom:90px;translate:-50% 30px;background:#2b0f1c;color:#fff;padding:12px 24px;border-radius:30px;font-size:.88rem;opacity:0;visibility:hidden;transition:.35s;z-index:2000}
.toast.on{opacity:1;visibility:visible;translate:-50% 0}
</style>
</head>
<body>

<!-- BIENVENIDA -->
<div id="welcome">
  <div id="wp"></div>
  <div class="logo-script">Jhuley</div>
  <div class="tag">Accesorios &amp; Detalles</div>
  <p class="sub">Detalles que hablan por ti 💕</p>
  <button class="btn-enter" onclick="entrar()">Entrar a la tienda ✨</button>
</div>

<!-- CIERRE -->
<div id="exit">
  <div id="ep"></div>
  <h1>¡Gracias por visitar JHULEY! 🌹</h1>
  <p style="font-size:1.2rem;font-weight:600;position:relative">Detalles que hablan por ti. ¡Hasta pronto! 💖</p>
  <button onclick="volver()" style="position:relative">Volver a la tienda</button>
</div>

<div class="topbar">🚚 Delivery desde S/ 5.00 · 💳 Paga con Yape o Plin · 🎡 ¡Gira la ruleta y gana descuentos!</div>

<nav>
  <div class="wrap nav-in">
    <a href="#inicio" class="brand">Jhuley<small>Accesorios &amp; Detalles</small></a>
    <div class="nav-links">
      <a href="#catalogo">Catálogo</a>
      <a href="#combos">Combos</a>
      <a href="#ruleta">Ruleta</a>
      <a href="#estrategia">Estrategia</a>
      <a href="#cronograma">Cronograma</a>
      <a href="#multimedia">Multimedia</a>
      <a href="#opiniones">Opiniones</a>
    </div>
    <div class="nav-actions">
      <button class="icon-btn" onclick="toggleTheme()" title="Modo oscuro">🌙</button>
      <button class="icon-btn" onclick="openCart()" title="Carrito">🛍️<span class="badge" id="badge">0</span></button>
    </div>
  </div>
</nav>

<!-- HERO -->
<header class="hero" id="inicio">
  <div class="wrap hero-grid">
    <div class="reveal">
      <span class="eyebrow">💝 Hecho con cariño en Perú</span>
      <h1>Regalos que dicen lo que <em>sientes</em></h1>
      <p class="lead">Accesorios y detalles personalizados para parejas y amigos. Cajas románticas, ramos, tazas, peluches y mucho más, pensados para cada ocasión.</p>
      <div class="cta-row">
        <a href="#catalogo" class="btn btn-primary">Ver catálogo 🎁</a>
        <a href="#ruleta" class="btn btn-ghost">Girar la ruleta 🎡</a>
      </div>
      <div class="hero-stats">
        <div><b data-count="20" data-plus="+">0</b><span>Productos</span></div>
        <div><b data-count="100" data-plus="%">0</b><span>Personalizable</span></div>
        <div><b data-count="2">0</b><span>Emprendedoras</span></div>
      </div>
    </div>
    <div class="hero-art reveal">
      <div class="blob b1">💐</div>
      <div class="blob b2">🧸</div>
      <div class="blob b3">🎁</div>
      <div class="chip-float">⭐ Más de 10 pedidos en el primer mes</div>
    </div>
  </div>
</header>

<!-- BENEFICIOS -->
<div class="wrap perks">
  <div class="perk-grid">
    <div class="perk reveal"><div class="ic">🎨</div><div><b>100% personalizado</b><span>Con tu mensaje y estilo</span></div></div>
    <div class="perk reveal"><div class="ic">🚚</div><div><b>Delivery a domicilio</b><span>Zonas céntricas y periféricas</span></div></div>
    <div class="perk reveal"><div class="ic">📲</div><div><b>Pide por WhatsApp</b><span>Atención rápida y directa</span></div></div>
    <div class="perk reveal"><div class="ic">💳</div><div><b>Yape y Plin</b><span>Pagos fáciles y seguros</span></div></div>
  </div>
</div>

<!-- CATÁLOGO -->
<section id="catalogo" data-sec="catalogo">
  <div class="wrap">
    <div class="sec-head reveal">
      <span class="eyebrow">Catálogo</span>
      <h2>Encuentra el detalle perfecto</h2>
      <p>Elige, agrega al carrito y envíanos tu pedido por WhatsApp en un clic.</p>
    </div>
    <div class="filters" id="filters">
      <button class="filter on" data-f="todos">✨ Todos</button>
      <button class="filter" data-f="parejas">💕 Parejas</button>
      <button class="filter" data-f="amigos">🧸 Amigos</button>
      <button class="filter" data-f="accesorios">💎 Accesorios</button>
      <button class="filter" data-f="sorpresas">🎉 Sorpresas</button>
    </div>
    <input class="search" id="search" type="search" placeholder="🔍 Buscar un detalle...">
    <div class="grid" id="grid"></div>
  </div>
</section>

<!-- COMBOS -->
<section class="combos" id="combos" data-sec="catalogo">
  <div class="wrap">
    <div class="sec-head reveal">
      <span class="eyebrow">Combos especiales</span>
      <h2>Packs listos para sorprender</h2>
      <p>Ahorra más llevando varios detalles juntos.</p>
    </div>
    <div class="combo-grid">
      <div class="combo c1 reveal"><div class="big">💘</div><h3>Combo San Valentín</h3><p>Caja romántica + Ramo de rosas + Tazas para parejas</p><button class="btn" onclick="addCombo('Combo San Valentín',95,'💘')">S/ 95.00 · Agregar</button></div>
      <div class="combo c2 reveal"><div class="big">🎂</div><h3>Combo Cumpleaños</h3><p>Box de cumpleaños + Globo con mensaje + Pack de dulces</p><button class="btn" onclick="addCombo('Combo Cumpleaños',58,'🎂')">S/ 58.00 · Agregar</button></div>
      <div class="combo c3 reveal"><div class="big">👭</div><h3>Combo Amistad</h3><p>2 Pulseras de amistad + Peluche con detalle + Stickers</p><button class="btn" onclick="addCombo('Combo Amistad',35,'👭')">S/ 35.00 · Agregar</button></div>
    </div>
  </div>
</section>

<!-- RULETA -->
<section id="ruleta" data-sec="catalogo">
  <div class="wrap">
    <div class="roulette-box reveal">
      <div>
        <div class="wheel-wrap">
          <div class="pointer"></div>
          <div class="wheel" id="wheel">
            <div class="lab" style="transform:rotate(30deg)"><span>10% DCTO</span></div>
            <div class="lab" style="transform:rotate(90deg)"><span>🍫 Chocolates</span></div>
            <div class="lab" style="transform:rotate(150deg)"><span>🚚 Envío gratis</span></div>
            <div class="lab" style="transform:rotate(210deg)"><span>5% DCTO</span></div>
            <div class="lab" style="transform:rotate(270deg)"><span>🎁 Regalo sorpresa</span></div>
            <div class="lab" style="transform:rotate(330deg)"><span>🌸 Sigue intentando</span></div>
          </div>
          <div class="hub">💖</div>
        </div>
      </div>
      <div>
        <span class="eyebrow">Ruleta sorpresa</span>
        <h2 style="font-size:2.2rem;margin-bottom:12px">¡Gira y gana un premio!</h2>
        <p style="color:var(--muted);margin-bottom:22px">Tu premio se aplica automáticamente a tu carrito. Un giro ganador por visita.</p>
        <button class="btn btn-primary" id="spinBtn" onclick="spin()">Girar ruleta 🎲</button>
        <div id="prize">🎁 ¡Haz clic para girar!</div>
      </div>
    </div>
  </div>
</section>

<!-- ESTRATEGIA -->
<section id="estrategia" data-sec="estrategia" style="background:var(--blush)">
  <div class="wrap">
    <div class="sec-head reveal">
      <span class="eyebrow">Diagnóstico y estrategia</span>
      <h2>Nuestro análisis FODA</h2>
      <p><b>Propuesta de valor:</b> detalles que expresan lo que sentimos, hechos con cariño y pensados para cada ocasión. Es nuestra primera página web, creada desde cero con mucha ilusión.</p>
    </div>
    <div class="foda-grid">
      <div class="foda f-f reveal"><h3>✨ Fortalezas</h3><ul><li>Productos personalizados y con valor emocional</li><li>Dos emprendedoras que se complementan</li><li>Logo e identidad de marca definidos</li></ul></div>
      <div class="foda f-o reveal"><h3>🚀 Oportunidades</h3><ul><li>Fechas de alta demanda (San Valentín, aniversarios, Navidad)</li><li>Crecimiento de las compras por redes sociales</li><li>Plataformas gratuitas y fáciles para principiantes</li></ul></div>
      <div class="foda f-d reveal"><h3>⚠️ Debilidades</h3><ul><li>Aún sin catálogo ordenado en línea</li><li>Primera vez creando una web</li><li>Recursos económicos limitados</li></ul></div>
      <div class="foda f-a reveal"><h3>🛡️ Amenazas</h3><ul><li>Emprendimientos con precios más bajos</li><li>Cambios de alcance en redes sociales</li><li>Desconfianza inicial en compras en línea</li></ul></div>
    </div>
    <div class="two">
      <div class="panel reveal">
        <h3>🎯 Objetivos</h3>
        <p style="font-size:.9rem;color:var(--muted);margin-bottom:10px"><b>General:</b> lanzar la página web de Jhuley en 30 días para mostrar el catálogo y recibir pedidos ordenados.</p>
        <p style="font-size:.9rem;margin-bottom:4px"><b>Objetivos SMART:</b></p>
        <ul><li>Publicar un catálogo con al menos 15 productos (foto, descripción, precio).</li><li>Recibir los primeros 10 pedidos web en el primer mes.</li><li>Aumentar un 20% las visitas desde redes sociales.</li></ul>
      </div>
      <div class="panel reveal">
        <h3>👩 Cliente ideal (Buyer Persona)</h3>
        <div class="persona"><div class="avatar">👩‍❤️‍👨</div><div><b>Jóvenes de 15 a 40 años</b><br><small style="color:var(--muted)">En pareja o que quieren sorprender a un amigo/a</small></div></div>
        <table>
          <tr><th>Característica</th><th>Perfil</th></tr>
          <tr><td>Qué busca</td><td>Detalle original, con significado y buen precio</td></tr>
          <tr><td>Cómo compra</td><td>Escribe por WhatsApp</td></tr>
          <tr><td>Cómo paga</td><td>Yape o Plin</td></tr>
        </table>
      </div>
    </div>
  </div>
</section>

<!-- CRONOGRAMA -->
<section id="cronograma" data-sec="cronograma">
  <div class="wrap">
    <div class="sec-head reveal">
      <span class="eyebrow">Implementación</span>
      <h2>Cronograma y metas</h2>
      <p>Siete etapas para lanzar Jhuley en cuatro semanas.</p>
    </div>
    <div class="timeline">
      <div class="step reveal"><div class="dot">1</div><div class="box"><span class="when">Semana 1</span><b>Preparación</b><small>Reunir logo, fotos y precios · Leydi y Jhuby</small></div></div>
      <div class="step reveal"><div class="dot">2</div><div class="box"><span class="when">Semana 1</span><b>Plataforma</b><small>Elegir plataforma y dominio · Jhuby</small></div></div>
      <div class="step reveal"><div class="dot">3</div><div class="box"><span class="when">Semana 2</span><b>Diseño</b><small>Armar secciones e identidad · Leydi</small></div></div>
      <div class="step reveal"><div class="dot">4</div><div class="box"><span class="when">Semana 2-3</span><b>Contenido</b><small>Subir productos y textos · Leydi y Jhuby</small></div></div>
      <div class="step reveal"><div class="dot">5</div><div class="box"><span class="when">Semana 3</span><b>Pagos</b><small>Configurar Yape, Plin y envíos · Jhuby</small></div></div>
      <div class="step reveal"><div class="dot">6</div><div class="box"><span class="when">Semana 4</span><b>Pruebas</b><small>Revisar en celular y corregir · Leydi y Jhuby</small></div></div>
      <div class="step reveal"><div class="dot">7</div><div class="box"><span class="when">Semana 4</span><b>Lanzamiento</b><small>Publicar y difundir · Leydi y Jhuby</small></div></div>
    </div>
    <div class="charts">
      <div class="panel reveal"><h3>🎯 Metas del primer mes</h3><canvas id="chartMetas"></canvas></div>
      <div class="panel reveal"><h3>🛍️ Catálogo por categoría</h3><canvas id="chartCat"></canvas></div>
    </div>
  </div>
</section>

<!-- MULTIMEDIA -->
<section id="multimedia" data-sec="multimedia" style="background:var(--blush)">
  <div class="wrap">
    <div class="sec-head reveal">
      <span class="eyebrow">Multimedia</span>
      <h2>Música, ideas y unboxing</h2>
    </div>
    <div class="video-grid">
      <div class="vbox reveal"><p>🎧 Música romántica · Daniel Lazo – Si No Es Contigo</p><div class="ratio"><iframe src="https://www.youtube.com/embed/pWxpHSahRw4" title="Daniel Lazo - Si No Es Contigo" allowfullscreen loading="lazy"></iframe></div></div>
      <div class="vbox reveal"><p>📦 MUSICA luna - Zoe </p><div class="ratio"><iframe src="[https://www.youtube.com/embed/ScMzIvxBSi4](https://www.youtube.com/watch?v=RYlKXvCxBz8&list=RDRYlKXvCxBz8&start_radio=1)" title="Unboxing de regalos" allowfullscreen loading="lazy"></iframe></div></div>
      <div class="vbox reveal"><p>💙 Unboxing especial JHULEY</p>
        <video class="local-video" controls autoplay loop muted playsinline><source src="Jhuley_video1_unboxing_azul.mp4" type="video/mp4">Tu navegador no soporta video.</video>
      </div>
    </div>
  </div>
</section>

<!-- OPINIONES -->
<section class="final" id="opiniones">
  <div class="wrap">
    <div class="sec-head reveal">
      <span class="eyebrow">Opiniones</span>
      <h2>Lo que dicen de Jhuley</h2>
      <p>¡Déjanos tu reacción y tus sugerencias para mejorar nuestro emprendimiento!</p>
    </div>
    <div class="testi-grid">
      <div class="testi reveal"><div class="stars">★★★★★</div><p>“¡Excelente iniciativa chicas, mucho éxito con la web de Jhuley!”</p><div class="who"><i>👩</i>Ana G.</div></div>
      <div class="testi reveal"><div class="stars">★★★★★</div><p>“Los precios están súper accesibles para sorprender a mi enamorada.”</p><div class="who"><i>👨</i>Carlos M.</div></div>
      <div class="testi reveal"><div class="stars">★★★★★</div><p>“La caja sorpresa quedó hermosa, llegó justo a tiempo.”</p><div class="who"><i>👩‍🦱</i>Lucía R.</div></div>
    </div>
    <div class="reactions">
      <button class="react" onclick="react('love')">❤️<b id="c-love">12</b></button>
      <button class="react" onclick="react('gift')">🎁<b id="c-gift">8</b></button>
      <button class="react" onclick="react('sparkles')">✨<b id="c-sparkles">15</b></button>
      <button class="react" onclick="react('star')">⭐<b id="c-star">10</b></button>
    </div>
    <div class="comment-box reveal">
      <label for="txt" style="font-weight:600;color:var(--rose)">Escribe tu opinión o sugerencia:</label>
      <textarea id="txt" placeholder="Ej: ¡Me encanta la caja romántica! ¿Agregarían más opciones de chocolates?"></textarea>
      <button class="btn btn-primary" style="margin-top:12px" onclick="comentar()">Enviar mensaje 💌</button>
      <div id="comments">
        <div class="cm"><b>Ana G.:</b> ¡Excelente iniciativa chicas! 🎉</div>
        <div class="cm"><b>Carlos M.:</b> Los precios están súper accesibles 💖</div>
      </div>
    </div>
    <div class="snoopy reveal">
      <img src="SNOOPY CON FLORES.jpg" alt="Snoopy con flores" onerror="this.outerHTML='<div style=&quot;font-size:3.5rem&quot;>🐶🌷</div>'">
      <div><b style="color:var(--rose)">¡Snoopy celebra el éxito de JHULEY! 🐶🌷</b><p style="font-size:.85rem;color:var(--muted)">Gracias por visitar nuestra página, creada con mucho amor por Leydi y Jhuby.</p></div>
    </div>
  </div>
</section>

<footer>
  <div class="wrap">
    <div class="f-grid">
      <div><div class="brand">Jhuley</div><p>Detalles que hablan por ti. Accesorios y regalos personalizados para parejas y amigos.</p><button class="close-btn" onclick="cerrar()">Cerrar página 🌹</button></div>
      <div><h4>Emprendedoras</h4><ul><li>Leydi Noemi Pacco Huanca</li><li>Deinny Jhuby Colquehuanca Colquehuanca</li></ul></div>
      <div><h4>Contacto</h4><ul><li>📲 WhatsApp</li><li>💳 Yape / Plin</li><li>🚚 Delivery</li></ul></div>
    </div>
    <div class="copy">JHULEY 2026 · Detalles que hablan por ti 💫</div>
  </div>
</footer>

<!-- Carrito lateral -->
<div class="overlay" id="overlay" onclick="closeCart()"></div>
<aside class="drawer" id="drawer">
  <div class="d-head"><h3>🛍️ Tu carrito</h3><button class="icon-btn" onclick="closeCart()">✕</button></div>
  <div class="d-items" id="items"></div>
  <div class="d-foot">
    <select id="zona" onchange="render()">
      <option value="0">🚚 Selecciona tu zona de delivery...</option>
      <option value="5">Zona céntrica · S/ 5.00</option>
      <option value="8">Zona periférica · S/ 8.00</option>
      <option value="12">Otras provincias · S/ 12.00</option>
    </select>
    <div class="line"><span>Subtotal</span><span id="sub">S/ 0.00</span></div>
    <div class="line disc" id="discLine" style="display:none"><span id="discName">Descuento</span><span id="disc">- S/ 0.00</span></div>
    <div class="line"><span>Delivery</span><span id="ship">S/ 0.00</span></div>
    <div class="line total"><span>Total</span><span id="total">S/ 0.00</span></div>
    <button class="btn btn-wa" onclick="checkout()">Pedir por WhatsApp 📲</button>
    <button class="mini-clear" onclick="clearCart()">Vaciar carrito</button>
  </div>
</aside>

<a class="wa-float" id="waf" href="#" target="_blank" title="Escríbenos por WhatsApp">💬</a>

<div class="settings">
  <button class="icon-btn" onclick="document.getElementById('sp').classList.toggle('on')" title="Personalizar vista">⚙️</button>
  <div class="panel-s" id="sp">
    <b style="font-size:.9rem">Mostrar / ocultar secciones</b>
    <label><input type="checkbox" checked onchange="secToggle('catalogo',this.checked)"> Catálogo, combos y ruleta</label>
    <label><input type="checkbox" checked onchange="secToggle('estrategia',this.checked)"> Estrategia y FODA</label>
    <label><input type="checkbox" checked onchange="secToggle('cronograma',this.checked)"> Cronograma y métricas</label>
    <label><input type="checkbox" checked onchange="secToggle('multimedia',this.checked)"> Multimedia</label>
  </div>
</div>
<div class="toast" id="toast"></div>

<script>
/* ======= CONFIGURA AQUÍ ======= */
const WHATSAPP = "51999999999";   // ← cambia por tu número real (51 + 9 dígitos)

/* ======= PRODUCTOS =======
   Para usar tus fotos, agrega  img:"nombre.jpg"  (en la misma carpeta que este archivo). */
const PRODUCTS = [
 {id:1,name:"Caja romántica",cat:"parejas",price:35,emoji:"🎁",bg:"#ffb1c1,#ff80ab",desc:"Caja decorada con detalles, mensaje y sorpresas para tu pareja.",tag:["top","Más vendido"],img:"https://images.unsplash.com/photo-1549465220-1a8b9238cd48?w=600&auto=format&fit=crop&q=60"},
 {id:2,name:"Ramo de rosas y chocolates",cat:"parejas",price:45,emoji:"💐",bg:"#ffc2d1,#ff94b8",desc:"Rosas frescas acompañadas de chocolates selectos.",tag:["hot","Popular"],img:"https://images.unsplash.com/photo-1518895949257-7621c3c786d7?w=600&auto=format&fit=crop&q=60"},
 {id:3,name:"Tazas para parejas",cat:"parejas",price:25,emoji:"☕",bg:"#ffe9a8,#ffc971",desc:"Set de dos tazas con frases y diseño personalizado.",img:"TAZA DE PAREJA.jpg"},
 {id:4,name:"Caja sorpresa",cat:"sorpresas",price:40,emoji:"🎀",bg:"#d1c4ff,#f8bbd0",desc:"Caja que se abre con sorpresas y mensajes escondidos.",img:"https://images.unsplash.com/photo-1513201099705-a9746e1e201f?w=600&auto=format&fit=crop&q=60"},
 {id:5,name:"Collares de pareja",cat:"parejas",price:30,emoji:"💞",bg:"#ffd1dc,#ff9ec0",desc:"Collares que se complementan, con dije de corazón.",tag:["new","Nuevo"]},
 {id:6,name:"Pulseras a juego",cat:"parejas",price:18,emoji:"📿",bg:"#c5e1ff,#f8bbd0",desc:"Pulseras ajustables con iniciales o fecha especial.",tag:["new","Nuevo"]},
 {id:7,name:"Marco de fotos personalizado",cat:"parejas",price:28,emoji:"🖼️",bg:"#ffe4ec,#ffb1c1",desc:"Marco con vuestra mejor foto y una frase única.",old:34,tag:["off","-18%"]},
 {id:8,name:"Cofre de recuerdos",cat:"parejas",price:38,emoji:"💌",bg:"#e1bee7,#f48fb1",desc:"Cofre con cartas, fotos y pequeños detalles de amor.",tag:["top","Premium"]},
 {id:9,name:"Peluche con detalle",cat:"amigos",price:20,emoji:"🧸",bg:"#ffe0b2,#ffab91",desc:"Peluche suave con mensaje y lazo personalizado.",img:"ROMANTICO.jpg"},
 {id:10,name:"Pack de dulces",cat:"amigos",price:15,emoji:"🍬",bg:"#ffcdd2,#f48fb1",desc:"Variedad de dulces y chocolates en presentación de regalo.",img:"https://images.unsplash.com/photo-1549007994-cb92caebd54b?w=600&auto=format&fit=crop&q=60"},
 {id:11,name:"Pulseras de amistad",cat:"amigos",price:10,emoji:"👭",bg:"#b2ebf2,#f8bbd0",desc:"Pulseras tejidas en pack de 2 para compartir.",tag:["hot","Popular"]},
 {id:12,name:"Taza personalizada",cat:"amigos",price:22,emoji:"🍵",bg:"#fff9c4,#ffe082",desc:"Taza con el nombre o frase favorita de tu amigo/a.",tag:["new","Nuevo"]},
 {id:13,name:"Box de cumpleaños",cat:"amigos",price:32,emoji:"🎂",bg:"#f8bbd0,#ce93d8",desc:"Box con dulce, tarjeta, globo y detalles para festejar.",tag:["top","Más vendido"]},
 {id:14,name:"Set de stickers",cat:"amigos",price:8,emoji:"⭐",bg:"#c8e6c9,#ffe082",desc:"Stickers kawaii para cuadernos, laptop y más.",old:10,tag:["off","-20%"]},
 {id:15,name:"Pack de scrunchies",cat:"accesorios",price:12,emoji:"🎀",bg:"#ffcdd2,#ff80ab",desc:"3 scrunchies suaves en tonos pastel.",tag:["new","Nuevo"]},
 {id:16,name:"Aretes de corazón",cat:"accesorios",price:15,emoji:"💖",bg:"#ffd1dc,#ffb74d",desc:"Aretes livianos con diseño delicado.",},
 {id:17,name:"Collar con inicial",cat:"accesorios",price:25,emoji:"🔤",bg:"#e1bee7,#ffcdd2",desc:"Collar dorado con la inicial que tú elijas.",tag:["hot","Popular"]},
 {id:18,name:"Desayuno sorpresa",cat:"sorpresas",price:55,emoji:"🥐",bg:"#ffe0b2,#ffcc80",desc:"Desayuno completo con globo, tarjeta y presentación especial.",tag:["top","Premium"]},
 {id:19,name:"Globo con mensaje",cat:"sorpresas",price:18,emoji:"🎈",bg:"#b3e5fc,#f8bbd0",desc:"Globo transparente con mensaje, confeti y luces.",tag:["new","Nuevo"]},
 {id:20,name:"Flores eternas",cat:"sorpresas",price:48,emoji:"🌹",bg:"#ffcdd2,#e57373",desc:"Ramo de flores preservadas que duran para siempre.",tag:["hot","Popular"]}
];
const CATS = {parejas:"Parejas",amigos:"Amigos",accesorios:"Accesorios",sorpresas:"Sorpresas"};

/* ======= UTILIDADES ======= */
const $ = id => document.getElementById(id);
const money = n => "S/ " + n.toFixed(2);
function toast(msg){const t=$("toast");t.textContent=msg;t.classList.add("on");clearTimeout(t._t);t._t=setTimeout(()=>t.classList.remove("on"),2200)}
function rain(container,icons,n,cls){for(let i=0;i<n;i++){const p=document.createElement("div");p.className=cls;p.textContent=icons[Math.floor(Math.random()*icons.length)];p.style.left=Math.random()*100+"vw";p.style.fontSize=(Math.random()*22+18)+"px";p.style.animationDuration=(Math.random()*3+2.5)+"s";p.style.animationDelay=(Math.random()*2)+"s";container.appendChild(p)}}

/* ======= PANTALLAS ======= */
rain($("wp"),["🎈","🌸","💖","🌷","✨","🌺"],30,"float-p");
function entrar(){$("welcome").classList.add("out");setTimeout(()=>$("welcome").style.display="none",900)}
function cerrar(){const e=$("exit");$("ep").innerHTML="";e.classList.add("active");rain($("ep"),["🌹","💖","🌸","🌷","✨","💕"],50,"fall")}
function volver(){$("exit").classList.remove("active")}
function toggleTheme(){document.body.classList.toggle("dark");buildCharts()}
function secToggle(k,on){document.querySelectorAll('[data-sec="'+k+'"]').forEach(s=>s.classList.toggle("hidden-sec",!on))}
$("waf").href = "https://wa.me/"+WHATSAPP+"?text="+encodeURIComponent("¡Hola! Me interesa un detalle de JHULEY 💖");

/* ======= CATÁLOGO ======= */
let filtro="todos", fav=new Set();
function renderGrid(){
  const q=$("search").value.trim().toLowerCase();
  const list=PRODUCTS.filter(p=>(filtro==="todos"||p.cat===filtro)&&(p.name.toLowerCase().includes(q)||p.desc.toLowerCase().includes(q)));
  $("grid").innerHTML = list.length ? list.map(p=>`
   <article class="card">
     <div class="pic" style="background:linear-gradient(145deg,${p.bg})">
       ${p.tag?`<span class="tag ${p.tag[0]}">${p.tag[1]}</span>`:""}
       <button class="fav" onclick="toggleFav(${p.id},this)">${fav.has(p.id)?"❤️":"🤍"}</button>
       <span>${p.emoji}</span>
       ${p.img?`<img src="${p.img}" alt="${p.name}" loading="lazy" onerror="this.remove()">`:""}
     </div>
     <div class="body">
       <span class="cat">${CATS[p.cat]}</span>
       <h3>${p.name}</h3>
       <div class="stars">★★★★★</div>
       <p class="desc">${p.desc}</p>
       <div class="price-row">
         <span class="price">${money(p.price)}${p.old?`<s>${money(p.old)}</s>`:""}</span>
         <button class="add" onclick="addToCart(${p.id})">+ Agregar</button>
       </div>
     </div>
   </article>`).join("") : '<div class="empty">No encontramos ese detalle 🥲 Prueba con otra búsqueda.</div>';
}
function toggleFav(id,btn){fav.has(id)?fav.delete(id):fav.add(id);btn.textContent=fav.has(id)?"❤️":"🤍"}
$("filters").addEventListener("click",e=>{const b=e.target.closest(".filter");if(!b)return;document.querySelectorAll(".filter").forEach(x=>x.classList.remove("on"));b.classList.add("on");filtro=b.dataset.f;renderGrid()});
$("search").addEventListener("input",renderGrid);
renderGrid();

/* ======= CARRITO ======= */
let cart={}, coupon=null; // coupon: {type:'pct'|'ship'|'gift', value, label}
function addToCart(id){const p=PRODUCTS.find(x=>x.id===id);add(p.name,p.price,p.emoji);}
function addCombo(n,pr,em){add(n,pr,em)}
function add(name,price,emoji){cart[name]=cart[name]||{price,emoji,qty:0};cart[name].qty++;render();toast("Agregado: "+name+" 🛍️")}
function chg(name,d){cart[name].qty+=d;if(cart[name].qty<=0)delete cart[name];render()}
function clearCart(){cart={};render()}
function openCart(){$("drawer").classList.add("on");$("overlay").classList.add("on")}
function closeCart(){$("drawer").classList.remove("on");$("overlay").classList.remove("on")}
function calc(){
  const keys=Object.keys(cart);
  const sub=keys.reduce((s,k)=>s+cart[k].price*cart[k].qty,0);
  let disc=0, shipBase=parseFloat($("zona").value)||0, ship=shipBase;
  if(coupon&&sub>0){ if(coupon.type==="pct") disc=sub*coupon.value/100; if(coupon.type==="ship") ship=0; }
  return {keys,sub,disc,ship,total:Math.max(0,sub-disc)+ship};
}
function render(){
  const c=calc();
  $("badge").textContent=c.keys.reduce((s,k)=>s+cart[k].qty,0);
  $("items").innerHTML=c.keys.length?c.keys.map(k=>{const i=cart[k];const sk=k.replace(/'/g,"\\'");return `
    <div class="item"><div class="em">${i.emoji}</div>
    <div class="nm">${k}<small>${money(i.price)} c/u</small></div>
    <div class="qty"><button onclick="chg('${sk}',-1)">−</button><b>${i.qty}</b><button onclick="chg('${sk}',1)">+</button></div></div>`}).join("")
    :'<div style="text-align:center;color:var(--muted);padding:50px 10px">Tu carrito está vacío 🥺<br>¡Elige tus detalles favoritos!</div>';
  $("sub").textContent=money(c.sub);
  $("discLine").style.display=(coupon&&coupon.type!=="none"&&c.sub>0)?"flex":"none";
  if(coupon){$("discName").textContent="🎡 "+coupon.label;$("disc").textContent=coupon.type==="pct"?"- "+money(c.disc):(coupon.type==="ship"?"Envío gratis":"Incluido")}
  $("ship").textContent=c.ship===0&&coupon&&coupon.type==="ship"&&parseFloat($("zona").value)>0?"¡Gratis!":money(c.ship);
  $("total").textContent=money(c.total);
}
function checkout(){
  const c=calc();
  if(!c.keys.length){toast("Agrega al menos un producto 🛍️");return}
  if(!parseFloat($("zona").value)){toast("Selecciona tu zona de delivery 🚚");return}
  let t="¡Hola! Quiero hacer este pedido en JHULEY:\n\n";
  c.keys.forEach(k=>t+="• "+cart[k].qty+" x "+k+" ("+money(cart[k].price*cart[k].qty)+")\n");
  t+="\nSubtotal: "+money(c.sub);
  if(coupon&&coupon.type!=="none")t+="\nPremio ruleta: "+coupon.label+(c.disc?" (-"+money(c.disc)+")":"");
  t+="\nDelivery: "+money(c.ship)+"\nTOTAL: "+money(c.total)+"\n\n¡Espero su confirmación! 💖";
  window.open("https://wa.me/"+WHATSAPP+"?text="+encodeURIComponent(t),"_blank");
}
render();

/* ======= RULETA ======= */
const PRIZES=[
 {label:"10% de descuento",type:"pct",value:10,msg:"✨ ¡Ganaste 10% de descuento en tu compra!",w:10},
 {label:"Chocolates gratis",type:"gift",msg:"🍫 ¡Ganaste una cajita de chocolates gratis!",w:12},
 {label:"Envío gratis",type:"ship",msg:"🚚 ¡Ganaste envío totalmente gratis!",w:12},
 {label:"5% de descuento",type:"pct",value:5,msg:"💖 ¡Ganaste 5% de descuento!",w:26},
 {label:"Regalo sorpresa",type:"gift",msg:"🎁 ¡Ganaste un regalo sorpresa en tu pedido!",w:15},
 {label:"Sin premio",type:"none",msg:"🌸 ¡Sigue intentando! Gira otra vez.",w:25}
];
let rot=0, spinning=false;
function spin(){
  if(spinning)return;
  if(coupon&&coupon.type!=="none"){toast("Ya tienes un premio activo 🎉");return}
  spinning=true; $("spinBtn").disabled=true; $("prize").textContent="🎡 Girando...";
  const tot=PRIZES.reduce((s,p)=>s+p.w,0); let r=Math.random()*tot, idx=0;
  for(;idx<PRIZES.length;idx++){r-=PRIZES[idx].w;if(r<=0)break}
  idx=Math.min(idx,PRIZES.length-1);
  const center=idx*60+30, jitter=(Math.random()-.5)*36;
  const targetMod=((360-center+jitter)%360+360)%360;
  const delta=((targetMod-(rot%360))+360)%360+360*6;
  rot+=delta; $("wheel").style.transform="rotate("+rot+"deg)";
  setTimeout(()=>{
    const p=PRIZES[idx]; spinning=false; $("spinBtn").disabled=false; $("prize").textContent=p.msg;
    if(p.type!=="none"){coupon={type:p.type,value:p.value,label:p.label};render();toast("Premio aplicado a tu carrito 🛍️");rain(document.body,["🎉","💖","✨"],14,"fall")}
    else coupon=null;
  },5100);
}

/* ======= REACCIONES Y COMENTARIOS ======= */
const R={love:12,gift:8,sparkles:15,star:10};
function react(t){R[t]++;$("c-"+t).textContent=R[t]}
function comentar(){
  const v=$("txt").value.trim();
  if(!v){toast("Escribe un comentario primero ✍️");return}
  const d=document.createElement("div");d.className="cm";
  const b=document.createElement("b");b.textContent="Visitante: ";d.appendChild(b);d.appendChild(document.createTextNode(v));
  $("comments").prepend(d);$("txt").value="";toast("¡Gracias por tu comentario! 💌");
}

/* ======= ANIMACIONES ======= */
const io=new IntersectionObserver(es=>es.forEach(e=>{if(e.isIntersecting){e.target.classList.add("show");io.unobserve(e.target)}}),{threshold:.12});
document.querySelectorAll(".reveal").forEach(el=>io.observe(el));
const cio=new IntersectionObserver(es=>es.forEach(e=>{if(!e.isIntersecting)return;const el=e.target,end=+el.dataset.count,suf=el.dataset.plus||"";let n=0;const step=Math.max(1,Math.ceil(end/40));const t=setInterval(()=>{n+=step;if(n>=end){n=end;clearInterval(t)}el.textContent=n+suf},30);cio.unobserve(el)}),{threshold:.5});
document.querySelectorAll("[data-count]").forEach(el=>cio.observe(el));

/* ======= GRÁFICOS ======= */
let ch1,ch2;
function buildCharts(){
  if(typeof Chart==="undefined")return;
  const dark=document.body.classList.contains("dark");
  Chart.defaults.color=dark?"#e8c9d4":"#7a6670";
  Chart.defaults.font.family="Poppins";
  ch1&&ch1.destroy();ch2&&ch2.destroy();
  ch1=new Chart($("chartMetas"),{type:"bar",data:{labels:["Productos publicados","Pedidos web","Visitas desde redes (+%)"],datasets:[{data:[15,10,20],backgroundColor:["rgba(216,27,96,.75)","rgba(255,64,129,.75)","rgba(201,162,75,.8)"],borderRadius:10}]},options:{plugins:{legend:{display:false}},scales:{y:{beginAtZero:true,grid:{color:dark?"#3b1f2b":"#f6d5df"}},x:{grid:{display:false}}}}});
  const counts=Object.keys(CATS).map(k=>PRODUCTS.filter(p=>p.cat===k).length);
  ch2=new Chart($("chartCat"),{type:"doughnut",data:{labels:Object.values(CATS),datasets:[{data:counts,backgroundColor:["#d81b60","#ff80ab","#c9a24b","#8e24aa"],borderWidth:0}]},options:{cutout:"62%",plugins:{legend:{position:"bottom"}}}});
}
window.addEventListener("load",buildCharts);
</script>
</body>
</html>
