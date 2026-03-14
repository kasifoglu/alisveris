<!DOCTYPE html>  
  
<html lang="tr">  
<head>  
<meta charset="UTF-8"/>  
<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no"/>  
<title>Alışveriş Listesi</title>  
<link href="https://fonts.googleapis.com/css2?family=Nunito:wght@600;700;800;900&display=swap" rel="stylesheet"/>  
<style>  
*{box-sizing:border-box;-webkit-tap-highlight-color:transparent;font-family:'Nunito',sans-serif;user-select:none;}  
body{margin:0;min-height:100vh;background:linear-gradient(160deg,#0f0c29,#302b63,#24243e);padding:20px 16px 120px;}  
input,textarea{user-select:text;-webkit-user-select:text;}  
input::placeholder,textarea::placeholder{color:rgba(255,255,255,0.3)}  
input:focus,textarea:focus{outline:none}  
@keyframes slideIn{from{opacity:0;transform:translateY(-8px)}to{opacity:1;transform:translateY(0)}}  
@keyframes fadeUp{from{opacity:0;transform:translateY(6px)}to{opacity:1;transform:translateY(0)}}  
.slide-in{animation:slideIn .25s ease forwards}  
::-webkit-scrollbar{width:3px}::-webkit-scrollbar-thumb{background:rgba(255,255,255,0.15);border-radius:2px}  
.swipe-wrapper{position:relative;border-radius:12px;margin-bottom:5px;overflow:hidden;}  
.swipe-bg{position:absolute;inset:0;border-radius:12px;display:flex;align-items:center;padding:0 18px;font-weight:800;pointer-events:none;opacity:0;}  
.swipe-bg-right{background:linear-gradient(90deg,#1a6b3a,#27ae60);justify-content:flex-start;color:#fff;gap:8px;font-size:13px;}  
.swipe-bg-left{background:linear-gradient(90deg,#7b1a1a,#c0392b);justify-content:flex-end;color:#fff;gap:8px;font-size:13px;}  
.swipe-item{position:relative;z-index:1;padding:10px 14px;border-radius:12px;background:rgba(255,255,255,0.04);cursor:pointer;display:flex;align-items:center;gap:10px;border:1px solid transparent;will-change:transform;touch-action:pan-y;}  
#suggestions{position:absolute;left:0;right:0;top:calc(100% + 6px);background:rgba(20,15,50,0.97);backdrop-filter:blur(24px);border:1px solid rgba(255,255,255,0.12);border-radius:14px;overflow:hidden;z-index:200;animation:fadeUp .15s ease;box-shadow:0 8px 32px rgba(0,0,0,0.5);}  
.sug-item{padding:11px 16px;display:flex;align-items:center;gap:10px;cursor:pointer;border-bottom:1px solid rgba(255,255,255,0.05);}  
.sug-item:last-child{border-bottom:none;}  
.sug-item:active{background:rgba(255,255,255,0.1);}  
.sug-name{color:#fff;font-size:14px;font-weight:700;flex:1;}  
.sug-match{color:#43e97b;font-weight:900;}  
.sug-cat{font-size:11px;color:rgba(255,255,255,0.35);font-weight:700;}  
.bought-chip{padding:6px 10px 6px 12px;border-radius:99px;background:rgba(255,255,255,0.04);border:1px solid rgba(255,255,255,0.07);display:flex;align-items:center;gap:6px;}  
.restore-btn{width:22px;height:22px;border-radius:99px;border:none;cursor:pointer;background:rgba(255,255,255,0.1);color:rgba(255,255,255,0.5);font-size:12px;display:flex;align-items:center;justify-content:center;flex-shrink:0;padding:0;touch-action:manipulation;}  
button{touch-action:manipulation;-webkit-tap-highlight-color:transparent;}  
</style>  
</head>  
<body>  
<div id="app">  
<div style="text-align:center;margin-bottom:22px">  
<div style="font-size:42px">🛒</div>  
<h1 style="margin:4px 0 0;color:#fff;font-size:26px;font-weight:900">Alışveriş Listesi</h1>  
<div id="progress-bar" style="display:none;max-width:300px;margin:12px auto 0">  
<div style="display:flex;justify-content:space-between;color:rgba(255,255,255,0.45);font-size:12px;font-weight:700;margin-bottom:6px">  
<span id="bought-count">✓ 0 alındı</span><span id="pct-text">0%</span><span id="waiting-count">0 bekliyor</span>  
</div>  
<div style="background:rgba(255,255,255,0.1);border-radius:99px;height:6px">  
<div id="progress-fill" style="height:100%;width:0%;background:linear-gradient(90deg,#43e97b,#38f9d7);border-radius:99px;transition:width .5s"></div>  
</div>  
</div>  
</div>  
<div style="display:flex;gap:10px;margin-bottom:10px;">  
<div style="flex:1;position:relative;">  
<input id="item-input" type="text" autocomplete="off" placeholder="Ürün ekle..."  
style="width:100%;padding:13px 16px;border-radius:16px;border:1.5px solid rgba(255,255,255,0.15);background:rgba(255,255,255,0.08);color:#fff;font-size:15px;font-weight:600;"/>  
<div id="suggestions" style="display:none;"></div>  
</div>  
<button id="add-btn"  
style="width:50px;height:50px;border-radius:16px;border:none;cursor:pointer;background:rgba(255,255,255,0.15);font-size:24px;font-weight:900;color:#1a1a2e;flex-shrink:0;line-height:1">+</button>  
</div>  
<div style="margin-bottom:20px;">  
<button id="bulk-toggle"  
style="width:100%;padding:14px 16px;border-radius:14px;border:1.5px dashed rgba(255,255,255,0.3);background:rgba(255,255,255,0.05);color:rgba(255,255,255,0.6);font-size:13px;font-weight:700;cursor:pointer;display:flex;align-items:center;justify-content:center;gap:8px;">  
<span>📋</span><span>Listeyi buraya yapıştır</span><span id="bulk-arrow">▾</span>  
</button>  
<div id="bulk-area" style="display:none;margin-top:8px;">  
<textarea id="bulk-input" rows="5"  
style="width:100%;padding:14px 16px;border-radius:16px;border:1.5px solid rgba(255,255,255,0.15);background:rgba(255,255,255,0.06);color:#fff;font-size:14px;font-weight:600;resize:none;font-family:'Nunito',sans-serif;line-height:1.6;"  
placeholder="Listeyi buraya yapıştır veya yaz..."></textarea>  
<button id="bulk-btn"  
style="margin-top:8px;width:100%;padding:13px;border-radius:14px;border:none;cursor:pointer;background:linear-gradient(135deg,#a78bfa,#818cf8);color:#fff;font-size:14px;font-weight:800;font-family:'Nunito',sans-serif;">  
✨ Listeyi Analiz Et ve Ekle  
</button>  
</div>  
</div>  
<div id="groups"></div>  
<div id="bought-section" style="display:none;margin-top:16px">  
<div style="display:flex;align-items:center;gap:8px;margin-bottom:8px">  
<div style="flex:1;height:1px;background:rgba(255,255,255,0.08)"></div>  
<span style="color:rgba(255,255,255,0.3);font-size:11px;font-weight:800;letter-spacing:1px">✓ ALINANLAR</span>  
<div style="flex:1;height:1px;background:rgba(255,255,255,0.08)"></div>  
</div>  
<p style="color:rgba(255,255,255,0.2);font-size:11px;font-weight:700;margin:0 0 10px;text-align:center">↩ butonuna bas → geri listeye ekle</p>  
<div id="bought-list" style="display:flex;flex-wrap:wrap;gap:8px"></div>  
</div>  
<div id="empty-state" style="text-align:center;padding:60px 20px">  
<div style="font-size:64px;opacity:.2">🧺</div>  
<p style="color:rgba(255,255,255,0.25);font-size:15px;font-weight:700;margin-top:12px">Liste boş!<br>Ürün ekleyerek başla.</p>  
</div>  
<div id="reset-btn-wrap" style="display:none;position:fixed;bottom:24px;left:50%;transform:translateX(-50%);z-index:20">  
<button id="reset-btn"  
style="padding:13px 32px;border-radius:99px;border:1.5px solid rgba(255,100,100,0.4);background:rgba(15,5,5,0.85);color:#ff7070;font-size:14px;font-weight:800;cursor:pointer;box-shadow:0 8px 30px rgba(0,0,0,0.5);">  
🔄 Alışverişi Sıfırla  
</button>  
</div>  
</div>  
<script>  
var CAT={  
"Süt Ürünleri":{b:"#F0C040",i:"🧀"},  
"Et & Balık":{b:"#E88080",i:"🥩"},  
"Sebze & Meyve":{b:"#68D391",i:"🥦"},  
"Fırın & Ekmek":{b:"#F6AD55",i:"🥖"},  
"İçecekler":{b:"#63B3ED",i:"🧃"},  
"Temizlik":{b:"#9F7AEA",i:"🧹"},  
"Kişisel Bakım":{b:"#F687B3",i:"🧴"},  
"Atıştırmalık":{b:"#FFA07A",i:"🍿"},  
"Dondurulmuş":{b:"#76D7EA",i:"🧊"},  
"Bakliyat":{b:"#C8B880",i:"🌾"},  
"Züccaciye":{b:"#F4A460",i:"🍽️"},  
"Tekstil":{b:"#DDA0DD",i:"🧺"},  
"Hırdavat":{b:"#708090",i:"🔧"},  
"Ev Eşyaları":{b:"#87CEEB",i:"🏠"},  
"Diğer":{b:"#AAAAAA",i:"🛒"}  
};  
function trk(s){  
return s.toLowerCase()  
.replace(/ğ/g,"g").replace(/ü/g,"u").replace(/ş/g,"s")  
.replace(/ı/g,"i").replace(/ö/g,"o").replace(/ç/g,"c")  
.replace(/î/g,"i").replace(/â/g,"a").replace(/û/g,"u").trim();  
}  
function rgb(hex){  
var r=/^#?([a-f\d]{2})([a-f\d]{2})([a-f\d]{2})$/i.exec(hex);  
return r?parseInt(r[1],16)+","+parseInt(r[2],16)+","+parseInt(r[3],16):"255,255,255";  
}  
function lev(a,b){  
var m=a.length,n=b.length;  
if(Math.abs(m-n)>3)return 99;  
var R=[];  
for(var i=0;i<=m;i++){R[i]=[];for(var j=0;j<=n;j++)R[i][j]=i===0?j:j===0?i:0;}  
for(var i=1;i<=m;i++)for(var j=1;j<=n;j++)  
R[i][j]=a[i-1]===b[j-1]?R[i-1][j-1]:1+Math.min(R[i-1][j],R[i][j-1],R[i-1][j-1]);  
return R[m][n];  
}  
var DB=[  
{n:"Süt",c:"Süt Ürünleri"},{n:"Tam Yağlı Süt",c:"Süt Ürünleri"},{n:"Yarım Yağlı Süt",c:"Süt Ürünleri"},{n:"Yağsız Süt",c:"Süt Ürünleri"},{n:"Çiğ Süt",c:"Süt Ürünleri"},{n:"Laktozsuz Süt",c:"Süt Ürünleri"},{n:"Soya Sütü",c:"Süt Ürünleri"},{n:"Badem Sütü",c:"Süt Ürünleri"},{n:"Hindistancevizi Sütü",c:"Süt Ürünleri"},  
{n:"Yoğurt",c:"Süt Ürünleri"},{n:"Süzme Yoğurt",c:"Süt Ürünleri"},{n:"Meyveli Yoğurt",c:"Süt Ürünleri"},{n:"Probiyotik Yoğurt",c:"Süt Ürünleri"},{n:"Kefir",c:"Süt Ürünleri"},{n:"Ayran",c:"Süt Ürünleri"},  
{n:"Peynir",c:"Süt Ürünleri"},{n:"Beyaz Peynir",c:"Süt Ürünleri"},{n:"Kaşar Peyniri",c:"Süt Ürünleri"},{n:"Tulum Peyniri",c:"Süt Ürünleri"},{n:"Lor Peyniri",c:"Süt Ürünleri"},{n:"Labne",c:"Süt Ürünleri"},{n:"Mozarella",c:"Süt Ürünleri"},{n:"Çökelek",c:"Süt Ürünleri"},{n:"Hellim",c:"Süt Ürünleri"},{n:"Gravyer",c:"Süt Ürünleri"},{n:"Parmesan",c:"Süt Ürünleri"},{n:"Cheddar",c:"Süt Ürünleri"},{n:"Gouda",c:"Süt Ürünleri"},{n:"Edam",c:"Süt Ürünleri"},{n:"Brie",c:"Süt Ürünleri"},{n:"Camembert",c:"Süt Ürünleri"},{n:"Ricotta",c:"Süt Ürünleri"},{n:"Mascarpone",c:"Süt Ürünleri"},{n:"Cottage Cheese",c:"Süt Ürünleri"},{n:"Feta Peyniri",c:"Süt Ürünleri"},{n:"Mihaliç Peyniri",c:"Süt Ürünleri"},{n:"Ezine Peyniri",c:"Süt Ürünleri"},{n:"Çerkez Peyniri",c:"Süt Ürünleri"},{n:"Dil Peyniri",c:"Süt Ürünleri"},{n:"Örgü Peyniri",c:"Süt Ürünleri"},{n:"Füme Peynir",c:"Süt Ürünleri"},  
{n:"Tereyağı",c:"Süt Ürünleri"},{n:"Tuzlu Tereyağı",c:"Süt Ürünleri"},{n:"Tuzsuz Tereyağı",c:"Süt Ürünleri"},{n:"Kaymak",c:"Süt Ürünleri"},{n:"Taze Kaymak",c:"Süt Ürünleri"},{n:"Krema",c:"Süt Ürünleri"},{n:"Krem Şanti",c:"Süt Ürünleri"},{n:"Sıvı Krema",c:"Süt Ürünleri"},{n:"Süt Kreması",c:"Süt Ürünleri"},{n:"Mascarpone",c:"Süt Ürünleri"},{n:"Crème Fraîche",c:"Süt Ürünleri"},{n:"Süt Tozu",c:"Süt Ürünleri"},{n:"Bebek Sütü",c:"Süt Ürünleri"},  
{n:"Yumurta",c:"Süt Ürünleri"},{n:"Köy Yumurtası",c:"Süt Ürünleri"},{n:"Organik Yumurta",c:"Süt Ürünleri"},{n:"Bıldırcın Yumurtası",c:"Süt Ürünleri"},  
{n:"Tavuk",c:"Et & Balık"},{n:"Tavuk Göğsü",c:"Et & Balık"},{n:"Tavuk But",c:"Et & Balık"},{n:"Tavuk Kanat",c:"Et & Balık"},{n:"Tavuk Bütün",c:"Et & Balık"},{n:"Tavuk Kıyma",c:"Et & Balık"},{n:"Tavuk Pirzola",c:"Et & Balık"},{n:"Tavuk Şinitzel",c:"Et & Balık"},{n:"Piliç",c:"Et & Balık"},{n:"Hindi",c:"Et & Balık"},{n:"Hindi Göğsü",c:"Et & Balık"},{n:"Hindi Kıyma",c:"Et & Balık"},  
{n:"Dana Eti",c:"Et & Balık"},{n:"Dana Kıyma",c:"Et & Balık"},{n:"Dana Bonfile",c:"Et & Balık"},{n:"Dana Pirzola",c:"Et & Balık"},{n:"Dana Biftek",c:"Et & Balık"},{n:"Dana Antrikot",c:"Et & Balık"},{n:"Dana Kaburga",c:"Et & Balık"},{n:"Dana But",c:"Et & Balık"},{n:"Dana Rosto",c:"Et & Balık"},{n:"Dana Ciğer",c:"Et & Balık"},{n:"Dana Böbrek",c:"Et & Balık"},  
{n:"Kuzu Eti",c:"Et & Balık"},{n:"Kuzu Kıyma",c:"Et & Balık"},{n:"Kuzu Pirzola",c:"Et & Balık"},{n:"Kuzu But",c:"Et & Balık"},{n:"Kuzu Kaburga",c:"Et & Balık"},{n:"Kuzu Ciğer",c:"Et & Balık"},{n:"Kıyma",c:"Et & Balık"},{n:"Karışık Kıyma",c:"Et & Balık"},  
{n:"Sucuk",c:"Et & Balık"},{n:"Sosis",c:"Et & Balık"},{n:"Pastırma",c:"Et & Balık"},{n:"Salam",c:"Et & Balık"},{n:"Jambon",c:"Et & Balık"},{n:"Hindi Sucuğu",c:"Et & Balık"},{n:"Tavuk Sucuğu",c:"Et & Balık"},{n:"Kangal Sucuk",c:"Et & Balık"},{n:"Baton Sucuk",c:"Et & Balık"},{n:"Kavurma",c:"Et & Balık"},{n:"Döner",c:"Et & Balık"},{n:"Kokoreç",c:"Et & Balık"},  
{n:"Köfte",c:"Et & Balık"},{n:"İnegöl Köfte",c:"Et & Balık"},{n:"Izgara Köfte",c:"Et & Balık"},{n:"Çiğ Köfte",c:"Et & Balık"},  
{n:"Balık",c:"Et & Balık"},{n:"Hamsi",c:"Et & Balık"},{n:"İstavrit",c:"Et & Balık"},{n:"Levrek",c:"Et & Balık"},{n:"Çipura",c:"Et & Balık"},{n:"Somon",c:"Et & Balık"},{n:"Alabalık",c:"Et & Balık"},{n:"Gökkuşağı Alabalığı",c:"Et & Balık"},{n:"Uskumru",c:"Et & Balık"},{n:"Palamut",c:"Et & Balık"},{n:"Lüfer",c:"Et & Balık"},{n:"Sardalya",c:"Et & Balık"},{n:"Ton Balığı",c:"Et & Balık"},{n:"Barbun",c:"Et & Balık"},{n:"Mezgit",c:"Et & Balık"},{n:"Kalkan",c:"Et & Balık"},{n:"Dil Balığı",c:"Et & Balık"},{n:"Kılıç Balığı",c:"Et & Balık"},{n:"Mercan",c:"Et & Balık"},{n:"Çupra",c:"Et & Balık"},{n:"Lagos",c:"Et & Balık"},{n:"İzmarit",c:"Et & Balık"},{n:"Tekir",c:"Et & Balık"},{n:"Kolyoz",c:"Et & Balık"},{n:"Orkinos",c:"Et & Balık"},  
{n:"Karides",c:"Et & Balık"},{n:"Midye",c:"Et & Balık"},{n:"Ahtapot",c:"Et & Balık"},{n:"Kalamar",c:"Et & Balık"},{n:"İstakoz",c:"Et & Balık"},{n:"Yengeç",c:"Et & Balık"},{n:"İstiridye",c:"Et & Balık"},{n:"Deniz Tarağı",c:"Et & Balık"},{n:"Karidesli Deniz Ürünleri",c:"Et & Balık"},  
{n:"Domates",c:"Sebze & Meyve"},{n:"Çeri Domates",c:"Sebze & Meyve"},{n:"Cherry Domates",c:"Sebze & Meyve"},{n:"Salkım Domates",c:"Sebze & Meyve"},{n:"Dilimlik Domates",c:"Sebze & Meyve"},  
{n:"Salatalık",c:"Sebze & Meyve"},{n:"Biber",c:"Sebze & Meyve"},{n:"Kırmızı Biber",c:"Sebze & Meyve"},{n:"Yeşil Biber",c:"Sebze & Meyve"},{n:"Dolmalık Biber",c:"Sebze & Meyve"},{n:"Sivri Biber",c:"Sebze & Meyve"},{n:"Kapya Biber",c:"Sebze & Meyve"},{n:"Çarliston Biber",c:"Sebze & Meyve"},{n:"Acı Biber",c:"Sebze & Meyve"},{n:"Jalapeno",c:"Sebze & Meyve"},  
{n:"Patlıcan",c:"Sebze & Meyve"},{n:"Patates",c:"Sebze & Meyve"},{n:"Tatlı Patates",c:"Sebze & Meyve"},{n:"Mor Patates",c:"Sebze & Meyve"},  
{n:"Soğan",c:"Sebze & Meyve"},{n:"Kırmızı Soğan",c:"Sebze & Meyve"},{n:"Taze Soğan",c:"Sebze & Meyve"},{n:"Arpacık Soğan",c:"Sebze & Meyve"},{n:"Sarımsak",c:"Sebze & Meyve"},{n:"Taze Sarımsak",c:"Sebze & Meyve"},  
{n:"Havuç",c:"Sebze & Meyve"},{n:"Bebek Havuç",c:"Sebze & Meyve"},{n:"Marul",c:"Sebze & Meyve"},{n:"Kıvırcık Marul",c:"Sebze & Meyve"},{n:"Kıvırcık",c:"Sebze & Meyve"},{n:"Roka",c:"Sebze & Meyve"},{n:"Semizotu",c:"Sebze & Meyve"},{n:"Tere",c:"Sebze & Meyve"},{n:"Ispanak",c:"Sebze & Meyve"},{n:"Bebek Ispanak",c:"Sebze & Meyve"},{n:"Pazı",c:"Sebze & Meyve"},{n:"Hindiba",c:"Sebze & Meyve"},{n:"Arugula",c:"Sebze & Meyve"},  
{n:"Kabak",c:"Sebze & Meyve"},{n:"Sakız Kabağı",c:"Sebze & Meyve"},{n:"Balkabağı",c:"Sebze & Meyve"},{n:"Brokoli",c:"Sebze & Meyve"},{n:"Karnabahar",c:"Sebze & Meyve"},{n:"Brüksel Lahanası",c:"Sebze & Meyve"},{n:"Lahana",c:"Sebze & Meyve"},{n:"Mor Lahana",c:"Sebze & Meyve"},{n:"Kırmızı Lahana",c:"Sebze & Meyve"},{n:"Beyaz Lahana",c:"Sebze & Meyve"},{n:"Çin Lahanası",c:"Sebze & Meyve"},{n:"Kara Lahana",c:"Sebze & Meyve"},  
{n:"Mantar",c:"Sebze & Meyve"},{n:"Şampinyon",c:"Sebze & Meyve"},{n:"Portobello Mantar",c:"Sebze & Meyve"},{n:"Shiitake",c:"Sebze & Meyve"},{n:"Kuru Mantar",c:"Sebze & Meyve"},  
{n:"Kereviz",c:"Sebze & Meyve"},{n:"Kereviz Sapı",c:"Sebze & Meyve"},{n:"Turp",c:"Sebze & Meyve"},{n:"Kırmızı Turp",c:"Sebze & Meyve"},{n:"Pancar",c:"Sebze & Meyve"},{n:"Enginar",c:"Sebze & Meyve"},{n:"Bamya",c:"Sebze & Meyve"},{n:"Taze Fasulye",c:"Sebze & Meyve"},{n:"Pırasa",c:"Sebze & Meyve"},{n:"Kuşkonmaz",c:"Sebze & Meyve"},{n:"Rezene",c:"Sebze & Meyve"},{n:"Şalgam",c:"Sebze & Meyve"},{n:"Bezelye",c:"Sebze & Meyve"},{n:"Taze Bezelye",c:"Sebze & Meyve"},{n:"Mısır",c:"Sebze & Meyve"},{n:"Tatlı Mısır",c:"Sebze & Meyve"},{n:"Taze Mısır",c:"Sebze & Meyve"},  
{n:"Maydanoz",c:"Sebze & Meyve"},{n:"Dereotu",c:"Sebze & Meyve"},{n:"Nane",c:"Sebze & Meyve"},{n:"Taze Nane",c:"Sebze & Meyve"},{n:"Fesleğen",c:"Sebze & Meyve"},{n:"Kişniş",c:"Sebze & Meyve"},{n:"Tarhun",c:"Sebze & Meyve"},{n:"Kekik",c:"Sebze & Meyve"},{n:"Biberiye",c:"Sebze & Meyve"},{n:"Adaçayı",c:"Sebze & Meyve"},{n:"Taze Zencefil",c:"Sebze & Meyve"},{n:"Zerdeçal Kökü",c:"Sebze & Meyve"},  
{n:"Elma",c:"Sebze & Meyve"},{n:"Yeşil Elma",c:"Sebze & Meyve"},{n:"Kırmızı Elma"  ,c:"Sebze & Meyve"},{n:"Granny Smith",c:"Sebze & Meyve"},{n:"Fuji Elma",c:"Sebze & Meyve"},  
{n:"Muz",c:"Sebze & Meyve"},{n:"Kırmızı Muz",c:"Sebze & Meyve"},{n:"Bebek Muz",c:"Sebze & Meyve"},  
{n:"Portakal",c:"Sebze & Meyve"},{n:"Mandalina",c:"Sebze & Meyve"},{n:"Klementine",c:"Sebze & Meyve"},{n:"Limon",c:"Sebze & Meyve"},{n:"Misket Limonu",c:"Sebze & Meyve"},{n:"Greyfurt",c:"Sebze & Meyve"},{n:"Pembe Greyfurt",c:"Sebze & Meyve"},{n:"Kumkat",c:"Sebze & Meyve"},  
{n:"Armut",c:"Sebze & Meyve"},{n:"Şeftali",c:"Sebze & Meyve"},{n:"Nektarin",c:"Sebze & Meyve"},{n:"Kayısı",c:"Sebze & Meyve"},{n:"Erik",c:"Sebze & Meyve"},{n:"Mor Erik",c:"Sebze & Meyve"},{n:"Can Eriği",c:"Sebze & Meyve"},  
{n:"Çilek",c:"Sebze & Meyve"},{n:"Ahududu",c:"Sebze & Meyve"},{n:"Böğürtlen",c:"Sebze & Meyve"},{n:"Yaban Mersini",c:"Sebze & Meyve"},{n:"Blueberry",c:"Sebze & Meyve"},{n:"Frambuaz",c:"Sebze & Meyve"},  
{n:"Üzüm",c:"Sebze & Meyve"},{n:"Siyah Üzüm",c:"Sebze & Meyve"},{n:"Yeşil Üzüm",c:"Sebze & Meyve"},{n:"Çekirdeksiz Üzüm",c:"Sebze & Meyve"},{n:"Kiraz",c:"Sebze & Meyve"},{n:"Vişne",c:"Sebze & Meyve"},  
{n:"Karpuz",c:"Sebze & Meyve"},{n:"Kavun",c:"Sebze & Meyve"},{n:"Ananas",c:"Sebze & Meyve"},{n:"Avokado",c:"Sebze & Meyve"},{n:"Mango",c:"Sebze & Meyve"},{n:"Kivi",c:"Sebze & Meyve"},{n:"Sarı Kivi",c:"Sebze & Meyve"},{n:"Papaya",c:"Sebze & Meyve"},{n:"Passion Fruit",c:"Sebze & Meyve"},{n:"Dragon Fruit",c:"Sebze & Meyve"},{n:"Liçi",c:"Sebze & Meyve"},{n:"Maracuja",c:"Sebze & Meyve"},  
{n:"Nar",c:"Sebze & Meyve"},{n:"İncir",c:"Sebze & Meyve"},{n:"Dut",c:"Sebze & Meyve"},{n:"Ayva",c:"Sebze & Meyve"},{n:"Malta Eriği",c:"Sebze & Meyve"},{n:"Muşmula",c:"Sebze & Meyve"},{n:"Hurma (Taze)",c:"Sebze & Meyve"},{n:"Kaktüs Meyvesi",c:"Sebze & Meyve"},  
{n:"Ekmek",c:"Fırın & Ekmek"},{n:"Beyaz Ekmek",c:"Fırın & Ekmek"},{n:"Tam Buğday Ekmeği",c:"Fırın & Ekmek"},{n:"Çavdar Ekmeği",c:"Fırın & Ekmek"},{n:"Kepek Ekmeği",c:"Fırın & Ekmek"},{n:"Köy Ekmeği",c:"Fırın & Ekmek"},{n:"Baget",c:"Fırın & Ekmek"},{n:"Tost Ekmeği",c:"Fırın & Ekmek"},{n:"Sandviç Ekmeği",c:"Fırın & Ekmek"},{n:"Hamburger Ekmeği",c:"Fırın & Ekmek"},{n:"Pide Ekmeği",c:"Fırın & Ekmek"},{n:"Lavaş",c:"Fırın & Ekmek"},{n:"Bazlama",c:"Fırın & Ekmek"},{n:"Francala",c:"Fırın & Ekmek"},{n:"Somun",c:"Fırın & Ekmek"},{n:"Tahıllı Ekmek",c:"Fırın & Ekmek"},{n:"Glutensiz Ekmek",c:"Fırın & Ekmek"},{n:"Pita",c:"Fırın & Ekmek"},{n:"Tortilla",c:"Fırın & Ekmek"},{n:"Chapati",c:"Fırın & Ekmek"},  
{n:"Simit",c:"Fırın & Ekmek"},{n:"Poğaça",c:"Fırın & Ekmek"},{n:"Açma",c:"Fırın & Ekmek"},{n:"Çörek",c:"Fırın & Ekmek"},{n:"Pide",c:"Fırın & Ekmek"},{n:"Börek",c:"Fırın & Ekmek"},{n:"Su Böreği",c:"Fırın & Ekmek"},{n:"Sigara Böreği",c:"Fırın & Ekmek"},{n:"Tepsi Böreği",c:"Fırın & Ekmek"},{n:"Ispanaklı Börek",c:"Fırın & Ekmek"},{n:"Peynirli Börek",c:"Fırın & Ekmek"},  
{n:"Pasta",c:"Fırın & Ekmek"},{n:"Kek",c:"Fırın & Ekmek"},{n:"Kup Kek",c:"Fırın & Ekmek"},{n:"Cupcake",c:"Fırın & Ekmek"},{n:"Muffin",c:"Fırın & Ekmek"},{n:"Brownie",c:"Fırın & Ekmek"},{n:"Cheesecake",c:"Fırın & Ekmek"},{n:"Tart",c:"Fırın & Ekmek"},{n:"Waffle",c:"Fırın & Ekmek"},{n:"Krep",c:"Fırın & Ekmek"},{n:"Pancake",c:"Fırın & Ekmek"},{n:"Galeta",c:"Fırın & Ekmek"},{n:"Grisini",c:"Fırın & Ekmek"},  
{n:"Bisküvi",c:"Fırın & Ekmek"},{n:"Kraker",c:"Fırın & Ekmek"},{n:"Çubuk Kraker",c:"Fırın & Ekmek"},{n:"Kurabiye",c:"Fırın & Ekmek"},{n:"Petit Beurre",c:"Fırın & Ekmek"},{n:"Grissini",c:"Fırın & Ekmek"},{n:"Rice Cake",c:"Fırın & Ekmek"},{n:"Pirinç Keki",c:"Fırın & Ekmek"},  
{n:"Su",c:"İçecekler"},{n:"Şişe Su",c:"İçecekler"},{n:"Damacana Su",c:"İçecekler"},{n:"Maden Suyu",c:"İçecekler"},{n:"Soda",c:"İçecekler"},{n:"Aromalı Soda",c:"İçecekler"},  
{n:"Kola",c:"İçecekler"},{n:"Diyet Kola",c:"İçecekler"},{n:"Sprite",c:"İçecekler"},{n:"Fanta",c:"İçecekler"},{n:"Gazoz",c:"İçecekler"},{n:"Meyveli Gazoz",c:"İçecekler"},  
{n:"Meyve Suyu",c:"İçecekler"},{n:"Elma Suyu",c:"İçecekler"},{n:"Portakal Suyu",c:"İçecekler"},{n:"Vişne Suyu",c:"İçecekler"},{n:"Nar Suyu",c:"İçecekler"},{n:"Domates Suyu",c:"İçecekler"},{n:"Şeftali Suyu",c:"İçecekler"},{n:"Kayısı Suyu",c:"İçecekler"},{n:"Karışık Meyve Suyu",c:"İçecekler"},{n:"Limonata",c:"İçecekler"},{n:"Şalgam Suyu",c:"İçecekler"},  
{n:"Çay",c:"İçecekler"},{n:"Demlik Çay",c:"İçecekler"},{n:"Poşet Çay",c:"İçecekler"},{n:"Yeşil Çay",c:"İçecekler"},{n:"Beyaz Çay",c:"İçecekler"},{n:"Bitki Çayı",c:"İçecekler"},{n:"Ihlamur",c:"İçecekler"},{n:"Papatya Çayı",c:"İçecekler"},{n:"Adaçayı Çayı",c:"İçecekler"},{n:"Kuşburnu Çayı",c:"İçecekler"},{n:"Zencefil Çayı",c:"İçecekler"},{n:"Nane Limon",c:"İçecekler"},{n:"Mate",c:"İçecekler"},  
{n:"Kahve",c:"İçecekler"},{n:"Türk Kahvesi",c:"İçecekler"},{n:"Nescafe",c:"İçecekler"},{n:"Filtre Kahve",c:"İçecekler"},{n:"Espresso",c:"İçecekler"},{n:"Kapsül Kahve",c:"İçecekler"},{n:"Granül Kahve",c:"İçecekler"},{n:"Soğuk Kahve",c:"İçecekler"},{n:"Ice Coffee",c:"İçecekler"},{n:"Ice Tea",c:"İçecekler"},{n:"Sıcak Çikolata",c:"İçecekler"},{n:"Kakao",c:"İçecekler"},{n:"Salep",c:"İçecekler"},{n:"Boza",c:"İçecekler"},{n:"Kefir İçeceği",c:"İçecekler"},  
{n:"Enerji İçeceği",c:"İçecekler"},{n:"Red Bull",c:"İçecekler"},{n:"Monster",c:"İçecekler"},{n:"Burn",c:"İçecekler"},{n:"Smoothie",c:"İçecekler"},{n:"Protein Shake",c:"İçecekler"},{n:"Kombucha",c:"İçecekler"},{n:"Kefir Suyu",c:"İçecekler"},  
{n:"Bira",c:"İçecekler"},{n:"Alkolsüz Bira",c:"İçecekler"},{n:"Şarap",c:"İçecekler"},{n:"Kırmızı Şarap",c:"İçecekler"},{n:"Beyaz Şarap",c:"İçecekler"},{n:"Rosé Şarap",c:"İçecekler"},{n:"Rakı",c:"İçecekler"},{n:"Viski",c:"İçecekler"},{n:"Votka",c:"İçecekler"},{n:"Cin",c:"İçecekler"},{n:"Şampanya",c:"İçecekler"},{n:"Prosecco",c:"İçecekler"},  
{n:"Deterjan",c:"Temizlik"},{n:"Çamaşır Deterjanı",c:"Temizlik"},{n:"Sıvı Deterjan",c:"Temizlik"},{n:"Toz Deterjan",c:"Temizlik"},{n:"Kapsül Deterjan",c:"Temizlik"},{n:"Çamaşır Suyu",c:"Temizlik"},{n:"Yumuşatıcı",c:"Temizlik"},{n:"Çamaşır Kiri Çıkarıcı",c:"Temizlik"},{n:"Leke Çıkarıcı",c:"Temizlik"},{n:"Elde Yıkama Deterjanı",c:"Temizlik"},  
{n:"Bulaşık Deterjanı",c:"Temizlik"},{n:"Bulaşık Sıvısı",c:"Temizlik"},{n:"Bulaşık Tableti",c:"Temizlik"},{n:"Parlatıcı",c:"Temizlik"},{n:"Tuz Tableti",c:"Temizlik"},{n:"Bulaşık Makinesi Tuzu",c:"Temizlik"},  
{n:"Yüzey Temizleyici",c:"Temizlik"},{n:"Banyo Temizleyici",c:"Temizlik"},{n:"Tuvalet Temizleyici",c:"Temizlik"},{n:"WC Taşı",c:"Temizlik"},{n:"Kireç Çözücü",c:"Temizlik"},{n:"Fırın Temizleyici",c:"Temizlik"},{n:"Cam Temizleyici",c:"Temizlik"},{n:"Yer Temizleyici",c:"Temizlik"},{n:"Mutfak Temizleyici",c:"Temizlik"},{n:"Çam Suyu",c:"Temizlik"},  
{n:"Kağıt Havlu",c:"Temizlik"},{n:"Temizlik Bezi",c:"Temizlik"},{n:"Mutfak Bezi",c:"Temizlik"},{n:"Paspas",c:"Temizlik"},{n:"Sünger",c:"Temizlik"},{n:"Tel Süngeri",c:"Temizlik"},{n:"Ovma Teli",c:"Temizlik"},{n:"Fırça",c:"Temizlik"},{n:"Toz Bezi",c:"Temizlik"},{n:"Mikrofibra Bez",c:"Temizlik"},  
{n:"Çöp Torbası",c:"Temizlik"},{n:"Çöp Poşeti",c:"Temizlik"},{n:"Büyük Çöp Torbası",c:"Temizlik"},{n:"Hava Spreyi",c:"Temizlik"},{n:"Oda Spreyi",c:"Temizlik"},{n:"Koku Giderici",c:"Temizlik"},{n:"Güve İlacı",c:"Temizlik"},{n:"Böcek İlacı",c:"Temizlik"},{n:"Haşere İlacı",c:"Temizlik"},{n:"Tuzak",c:"Temizlik"},  
{n:"Diş Macunu",c:"Kişisel Bakım"},{n:"Diş Fırçası",c:"Kişisel Bakım"},{n:"Elektrikli Diş Fırçası",c:"Kişisel Bakım"},{n:"Ağız Gargarası",c:"Kişisel Bakım"},{n:"Diş İpi",c:"Kişisel Bakım"},{n:"Diş Suyu",c:"Kişisel Bakım"},  
{n:"Tuvalet Kağıdı",c:"Kişisel Bakım"},{n:"Islak Mendil",c:"Kişisel Bakım"},{n:"Kağıt Mendil",c:"Kişisel Bakım"},{n:"Bebek Islak Mendil",c:"Kişisel Bakım"},  
{n:"Sabun",c:"Kişisel Bakım"},{n:"El Sabunu",c:"Kişisel Bakım"},{n:"Vücut Sabunu",c:"Kişisel Bakım"},{n:"Katı Sabun",c:"Kişisel Bakım"},{n:"Sıvı Sabun",c:"Kişisel Bakım"},{n:"Antibakteriyel Sabun",c:"Kişisel Bakım"},  
{n:"Şampuan",c:"Kişisel Bakım"},{n:"Saç Kremi",c:"Kişisel Bakım"},{n:"Saç Maskesi",c:"Kişisel Bakım"},{n:"Saç Spreyi",c:"Kişisel Bakım"},{n:"Saç Jeli",c:"Kişisel Bakım"},{n:"Saç Köpüğü",c:"Kişisel Bakım"},{n:"Saç Boyası",c:"Kişisel Bakım"},{n:"Saç Açıcı",c:"Kişisel Bakım"},{n:"Saç Serumu",c:"Kişisel Bakım"},{n:"Saç Yağı",c:"Kişisel Bakım"},{n:"Kepek Şampuanı",c:"Kişisel Bakım"},  
{n:"Duş Jeli",c:"Kişisel Bakım"},{n:"Vücut Losyonu",c:"Kişisel Bakım"},{n:"Vücut Yağı",c:"Kişisel Bakım"},{n:"El Kremi",c:"Kişisel Bakım"},{n:"Yüz Kremi",c:"Kişisel Bakım"},{n:"Gece Kremi",c:"Kişisel Bakım"},{n:"Göz Kremi",c:"Kişisel Bakım"},{n:"Nemlendirici",c:"Kişisel Bakım"},{n:"Güneş Kremi",c:"Kişisel Bakım"},{n:"SPF Krem",c:"Kişisel Bakım"},{n:"Serum",c:"Kişisel Bakım"},{n:"Tonik",c:"Kişisel Bakım"},{n:"Yüz Temizleyici",c:"Kişisel Bakım"},{n:"Maske",c:"Kişisel Bakım"},{n:"Peeling",c:"Kişisel Bakım"},{n:"Misel Suyu",c:"Kişisel Bakım"},{n:"Dudak Balsamı",c:"Kişisel Bakım"},  
{n:"Deodorant",c:"Kişisel Bakım"},{n:"Roll-on",c:"Kişisel Bakım"},{n:"Stick Deodorant",c:"Kişisel Bakım"},{n:"Parfüm",c:"Kişisel Bakım"},{n:"Kolonya",c:"Kişisel Bakım"},{n:"Tuvalet Suyu",c:"Kişisel Bakım"},  
{n:"Fondöten",c:"Kişisel Bakım"},{n:"Maskara",c:"Kişisel Bakım"},{n:"Ruj",c:"Kişisel Bakım"},{n:"Ruj Parlatıcı",c:"Kişisel Bakım"},{n:"Oje",c:"Kişisel Bakım"},{n:"Göz Kalemi",c:"Kişisel Bakım"},{n:"Kaş Kalemi",c:"Kişisel Bakım"},{n:"Far",c:"Kişisel Bakım"},{n:"Allık",c:"Kişisel Bakım"},{n:"Bronzer",c:"Kişisel Bakım"},{n:"Makyaj Temizleyici",c:"Kişisel Bakım"},{n:"BB Krem",c:"Kişisel Bakım"},{n:"CC Krem",c:"Kişisel Bakım"},{n:"Pudra",c:"Kişisel Bakım"},{n:"Kapatıcı",c:"Kişisel Bakım"},  
{n:"Jilet",c:"Kişisel Bakım"},{n:"Tıraş Jeli",c:"Kişisel Bakım"},{n:"Tıraş Köpüğü",c:"Kişisel Bakım"},{n:"Tıraş Kremi",c:"Kişisel Bakım"},{n:"Epilasyon",c:"Kişisel Bakım"},{n:"Ağda",c:"Kişisel Bakım"},{n:"Epilatör Bandı",c:"Kişisel Bakım"},  
{n:"Pamuk",c:"Kişisel Bakım"},{n:"Kulak Çubuğu",c:"Kişisel Bakım"},{n:"Cımbız",c:"Kişisel Bakım"},{n:"Tırnak Makası",c:"Kişisel Bakım"},{n:"Tırnak Törpüsü",c:"Kişisel Bakım"},{n:"Bandaj",c:"Kişisel Bakım"},{n:"Yara Bandı",c:"Kişisel Bakım"},{n:"Flaster",c:"Kişisel Bakım"},  
{n:"Tampon",c:"Kişisel Bakım"},{n:"Hijyenik Ped",c:"Kişisel Bakım"},{n:"Gece Pedi",c:"Kişisel Bakım"},{n:"Günlük Ped",c:"Kişisel Bakım"},{n:"Menstrual Kap",c:"Kişisel Bakım"},  
{n:"Çikolata",c:"Atıştırmalık"},{n:"Sütlü Çikolata",c:"Atıştırmalık"},{n:"Bitter Çikolata",c:"Atıştırmalık"},{n:"Beyaz Çikolata",c:"Atıştırmalık"},{n:"Çikolatalı Fındık",c:"Atıştırmalık"},{n:"Pralin",c:"Atıştırmalık"},{n:"Trüf Çikolata",c:"Atıştırmalık"},{n:"Nutella",c:"Atıştırmalık"},{n:"Çikolata Kaplama",c:"Atıştırmalık"},  
{n:"Cips",c:"Atıştırmalık"},{n:"Patates Cipsi",c:"Atıştırmalık"},{n:"Mısır Cipsi",c:"Atıştırmalık"},{n:"Tortilla Cipsi",c:"Atıştırmalık"},{n:"Gofret",c:"Atıştırmalık"},{n:"Şeker",c:"Atıştırmalık"},{n:"Bonbon",c:"Atıştırmalık"},{n:"Jöle",c:"Atıştırmalık"},{n:"Gummy",c:"Atıştırmalık"},{n:"Sakız",c:"Atıştırmalık"},{n:"Lokum",c:"Atıştırmalık"},{n:"Akide Şekeri",c:"Atıştırmalık"},{n:"Helva",c:"Atıştırmalık"},{n:"Tahin Helvası",c:"Atıştırmalık"},{n:"Pişmaniye",c:"Atıştırmalık"},{n:"Baklava",c:"Atıştırmalık"},{n:"Kadayıf",c:"Atıştırmalık"},  
{n:"Fındık",c:"Atıştırmalık"},{n:"Fıstık",c:"Atıştırmalık"},{n:"Antep Fıstığı",c:"Atıştırmalık"},{n:"Badem",c:"Atıştırmalık"},{n:"Ceviz",c:"Atıştırmalık"},{n:"Kaju",c:"Atıştırmalık"},{n:"Çerez",c:"Atıştırmalık"},{n:"Karışık Kuruyemiş",c:"Atıştırmalık"},{n:"Kabak Çekirdeği",c:"Atıştırmalık"},{n:"Ay Çekirdeği",c:"Atıştırmalık"},{n:"Çekirdek",c:"Atıştırmalık"},{n:"Leblebi",c:"Atıştırmalık"},{n:"Mısır Leblebi",c:"Atıştırmalık"},{n:"Sarı Leblebi",c:"Atıştırmalık"},  
{n:"Mısır Gevreği",c:"Atıştırmalık"},{n:"Granola",c:"Atıştırmalık"},{n:"Müsli",c:"Atıştırmalık"},{n:"Enerji Barı",c:"Atıştırmalık"},{n:"Protein Bar",c:"Atıştırmalık"},{n:"Meyve Barı",c:"Atıştırmalık"},{n:"Popcorn",c:"Atıştırmalık"},{n:"Mısır Patlaması",c:"Atıştırmalık"},  
{n:"Kuru Üzüm",c:"Atıştırmalık"},{n:"Kuru Kayısı",c:"Atıştırmalık"},{n:"Kuru İncir",c:"Atıştırmalık"},{n:"Kuru Erik",c:"Atıştırmalık"},{n:"Kuru Dut",c:"Atıştırmalık"},{n:"Kuru Meyve",c:"Atıştırmalık"},{n:"Hurma",c:"Atıştırmalık"},{n:"Medjool Hurma",c:"Atıştırmalık"},{n:"Keçiboynuzu",c:"Atıştırmalık"},{n:"Meyve Cipsi",c:"Atıştırmalık"},{n:"Elma Cipsi",c:"Atıştırmalık"},  
{n:"Fıstık Ezmesi",c:"Atıştırmalık"},{n:"Badem Ezmesi",c:"Atıştırmalık"},{n:"Susam Ezmesi",c:"Atıştırmalık"},{n:"Avokado Sosu",c:"Atıştırmalık"},  
{n:"Dondurma",c:"Dondurulmuş"},{n:"Külah Dondurma",c:"Dondurulmuş"},{n:"Stick Dondurma",c:"Dondurulmuş"},{n:"Dondurma Kap",c:"Dondurulmuş"},{n:"Çikolatalı Dondurma",c:"Dondurulmuş"},{n:"Meyveli Dondurma",c:"Dondurulmuş"},{n:"Sorbe",c:"Dondurulmuş"},  
{n:"Dondurulmuş Sebze",c:"Dondurulmuş"},{n:"Dondurulmuş Meyve",c:"Dondurulmuş"},{n:"Dondurulmuş Bezelye",c:"Dondurulmuş"},{n:"Dondurulmuş Mısır",c:"Dondurulmuş"},{n:"Dondurulmuş Ispanak",c:"Dondurulmuş"},{n:"Dondurulmuş Karışık Sebze",c:"Dondurulmuş"},{n:"Dondurulmuş Edamame",c:"Dondurulmuş"},  
{n:"Pizza",c:"Dondurulmuş"},{n:"Hazır Pizza",c:"Dondurulmuş"},{n:"Nugget",c:"Dondurulmuş"},{n:"Tavuk Nugget",c:"Dondurulmuş"},{n:"Patates Kızartması",c:"Dondurulmuş"},{n:"Hazır Yemek",c:"Dondurulmuş"},{n:"Lazanya",c:"Dondurulmuş"},{n:"Mantı",c:"Dondurulmuş"},{n:"Börek (Hazır)",c:"Dondurulmuş"},{n:"Gözleme (Hazır)",c:"Dondurulmuş"},{n:"Dondurulmuş Balık",c:"Dondurulmuş"},{n:"Dondurulmuş Et",c:"Dondurulmuş"},{n:"Dondurulmuş Köfte",c:"Dondurulmuş"},{n:"Hazır Çorba",c:"Dondurulmuş"},{n:"Falafel (Hazır)",c:"Dondurulmuş"},  
{n:"Mercimek",c:"Bakliyat"},{n:"Kırmızı Mercimek",c:"Bakliyat"},{n:"Yeşil Mercimek",c:"Bakliyat"},{n:"Sarı Mercimek",c:"Bakliyat"},{n:"Nohut",c:"Bakliyat"},{n:"Fasulye",c:"Bakliyat"},{n:"Barbunya",c:"Bakliyat"},{n:"Siyah Fasulye",c:"Bakliyat"},{n:"Beyaz Fasulye",c:"Bakliyat"},{n:"Börülce",c:"Bakliyat"},{n:"Soya Fasulyesi",c:"Bakliyat"},{n:"Edamame",c:"Bakliyat"},{n:"Bakla",c:"Bakliyat"},  
{n:"Pirinç",c:"Bakliyat"},{n:"Basmati Pirinç",c:"Bakliyat"},{n:"Jasmin Pirinç",c:"Bakliyat"},{n:"Arborio Pirinç",c:"Bakliyat"},{n:"Esmer Pirinç",c:"Bakliyat"},{n:"Bulgur",c:"Bakliyat"},{n:"İnce Bulgur",c:"Bakliyat"},{n:"Kısır Bulguru",c:"Bakliyat"},  
{n:"Makarna",c:"Bakliyat"},{n:"Spagetti",c:"Bakliyat"},{n:"Penne",c:"Bakliyat"},{n:"Fusilli",c:"Bakliyat"},{n:"Farfalle",c:"Bakliyat"},{n:"Rigatoni",c:"Bakliyat"},{n:"Tagliatelle",c:"Bakliyat"},{n:"Lasagne",c:"Bakliyat"},{n:"Erişte",c:"Bakliyat"},{n:"Yufka",c:"Bakliyat"},{n:"Kadayıf Teli",c:"Bakliyat"},  
{n:"Un",c:"Bakliyat"},{n:"Tam Buğday Unu",c:"Bakliyat"},{n:"Mısır Unu",c:"Bakliyat"},{n:"Nohut Unu",c:"Bakliyat"},{n:"Pirinç Unu",c:"Bakliyat"},{n:"Badem Unu",c:"Bakliyat"},{n:"Glutensiz Un",c:"Bakliyat"},{n:"İrmik",c:"Bakliyat"},{n:"Yulaf",c:"Bakliyat"},{n:"Yulaf Ezmesi",c:"Bakliyat"},{n:"Kinoa",c:"Bakliyat"},{n:"Karabuğday",c:"Bakliyat"},{n:"Arpa",c:"Bakliyat"},{n:"Nişasta",c:"Bakliyat"},{n:"Mısır Nişastası",c:"Bakliyat"},{n:"Kepek",c:"Bakliyat"},{n:"Buğday Kepeği",c:"Bakliyat"},  
{n:"Zeytinyağı",c:"Bakliyat"},{n:"Sızma Zeytinyağı",c:"Bakliyat"},{n:"Riviera Zeytinyağı",c:"Bakliyat"},{n:"Ayçiçek Yağı",c:"Bakliyat"},{n:"Mısır Yağı",c:"Bakliyat"},{n:"Hindistancevizi Yağı",c:"Bakliyat"},{n:"Sıvı Yağ",c:"Bakliyat"},{n:"Susam Yağı",c:"Bakliyat"},  
{n:"Sirke",c:"Bakliyat"},{n:"Elma Sirkesi",c:"Bakliyat"},{n:"Üzüm Sirkesi",c:"Bakliyat"},{n:"Balzamik Sirke",c:"Bakliyat"},{n:"Pirinç Sirkesi",c:"Bakliyat"},  
{n:"Salça",c:"Bakliyat"},{n:"Domates Salçası",c:"Bakliyat"},{n:"Biber Salçası",c:"Bakliyat"},{n:"Domates Konservesi",c:"Bakliyat"},{n:"Domates Sosu",c:"Bakliyat"},{n:"Konserve Nohut",c:"Bakliyat"},{n:"Konserve Fasulye",c:"Bakliyat"},{n:"Konserve Mısır",c:"Bakliyat"},{n:"Konserve Ton Balığı",c:"Bakliyat"},{n:"Konserve Sardalya",c:"Bakliyat"},{n:"Konserve Ançüez",c:"Bakliyat"},  
{n:"Ketçap",c:"Bakliyat"},{n:"Mayonez",c:"Bakliyat"},{n:"Hardal",c:"Bakliyat"},{n:"Dijon Hardal",c:"Bakliyat"},{n:"Soya Sosu",c:"Bakliyat"},{n:"Worcestershire Sosu",c:"Bakliyat"},{n:"Tabasco",c:"Bakliyat"},{n:"Sriracha",c:"Bakliyat"},{n:"Nar Ekşisi",c:"Bakliyat"},{n:"Sos",c:"Bakliyat"},{n:"Pesto",c:"Bakliyat"},{n:"Tahin",c:"Bakliyat"},{n:"Humus",c:"Bakliyat"},  
{n:"Bal",c:"Bakliyat"},{n:"Çiçek Balı",c:"Bakliyat"},{n:"Kestane Balı",c:"Bakliyat"},{n:"Pekmez",c:"Bakliyat"},{n:"Üzüm Pekmezi",c:"Bakliyat"},{n:"Dut Pekmezi",c:"Bakliyat"},{n:"Keçiboynuzu Pekmezi",c:"Bakliyat"},{n:"Reçel",c:"Bakliyat"},{n:"Çilek Reçeli",c:"Bakliyat"},{n:"Kayısı Reçeli",c:"Bakliyat"},{n:"Vişne Reçeli",c:"Bakliyat"},{n:"Marmelat",c:"Bakliyat"},  
{n:"Tuz",c:"Bakliyat"},{n:"Deniz Tuzu",c:"Bakliyat"},{n:"Kaya Tuzu",c:"Bakliyat"},{n:"İyotlu Tuz",c:"Bakliyat"},{n:"Şeker",c:"Bakliyat"},{n:"Toz Şeker",c:"Bakliyat"},{n:"Pudra Şekeri",c:"Bakliyat"},{n:"Esmer Şeker",c:"Bakliyat"},{n:"Hindistancevizi Şekeri",c:"Bakliyat"},{n:"Stevia",c:"Bakliyat"},  
{n:"Karabiber",c:"Bakliyat"},{n:"Kırmızı Pul Biber",c:"Bakliyat"},{n:"Pul Biber",c:"Bakliyat"},{n:"Kimyon",c:"Bakliyat"},{n:"Kekik",c:"Bakliyat"},{n:"Nane (Kuru)",c:"Bakliyat"},{n:"Tarçın",c:"Bakliyat"},{n:"Zerdeçal",c:"Bakliyat"},{n:"Köri",c:"Bakliyat"},{n:"Zencefil Tozu",c:"Bakliyat"},{n:"Kakule",c:"Bakliyat"},{n:"Karanfil",c:"Bakliyat"},{n:"Defne Yaprağı",c:"Bakliyat"},{n:"Sumak",c:"Bakliyat"},{n:"İsot",c:"Bakliyat"},{n:"Mahlep",c:"Bakliyat"},{n:"Safran",c:"Bakliyat"},{n:"Muskat",c:"Bakliyat"},{n:"Anason",c:"Bakliyat"},{n:"Rezene Tohumu",c:"Bakliyat"},{n:"Hardal Tohumu",c:"Bakliyat"},{n:"Çörek Otu",c:"Bakliyat"},{n:"Susam",c:"Bakliyat"},{n:"Keten Tohumu",c:"Bakliyat"},{n:"Chia Tohumu",c:"Bakliyat"},{n:"Kabartma Tozu",c:"Bakliyat"},{n:"Karbonat",c:"Bakliyat"},{n:"Maya",c:"Bakliyat"},{n:"Kuru Maya",c:"Bakliyat"},{n:"Vanilya",c:"Bakliyat"},{n:"Vanilya Özü",c:"Bakliyat"},{n:"Kakao Tozu",c:"Bakliyat"},{n:"Bisküvi Kırıntısı",c:"Bakliyat"},  
{n:"Zeytin",c:"Bakliyat"},{n:"Yeşil Zeytin",c:"Bakliyat"},{n:"Siyah Zeytin",c:"Bakliyat"},{n:"Kapari",c:"Bakliyat"},{n:"Turşu",c:"Bakliyat"},{n:"Kornişon Turşu",c:"Bakliyat"},{n:"Lahana Turşusu",c:"Bakliyat"},{n:"Karışık Turşu",c:"Bakliyat"}  
,  
  
{n:“Tabak”,c:“Züccaciye”},{n:“Düz Tabak”,c:“Züccaciye”},{n:“Çorba Tabağı”,c:“Züccaciye”},{n:“Tatlı Tabağı”,c:“Züccaciye”},{n:“Salata Tabağı”,c:“Züccaciye”},{n:“Servis Tabağı”,c:“Züccaciye”},{n:“Kahvaltı Tabağı”,c:“Züccaciye”},  
{n:“Kase”,c:“Züccaciye”},{n:“Salata Kasesi”,c:“Züccaciye”},{n:“Çorba Kasesi”,c:“Züccaciye”},{n:“Meyve Kasesi”,c:“Züccaciye”},  
{n:“Bardak”,c:“Züccaciye”},{n:“Su Bardağı”,c:“Züccaciye”},{n:“Çay Bardağı”,c:“Züccaciye”},{n:“Kahve Fincanı”,c:“Züccaciye”},{n:“Kupa”,c:“Züccaciye”},{n:“Mug”,c:“Züccaciye”},{n:“Meşrubat Bardağı”,c:“Züccaciye”},{n:“Şarap Kadehi”,c:“Züccaciye”},{n:“Bira Bardağı”,c:“Züccaciye”},{n:“Viski Bardağı”,c:“Züccaciye”},  
{n:“Tencere”,c:“Züccaciye”},{n:“Düdüklü Tencere”,c:“Züccaciye”},{n:“Çorba Tenceresi”,c:“Züccaciye”},{n:“Süt Tenceresi”,c:“Züccaciye”},{n:“Tava”,c:“Züccaciye”},{n:“Kızartma Tavası”,c:“Züccaciye”},{n:“Döküm Tava”,c:“Züccaciye”},{n:“Wok”,c:“Züccaciye”},{n:“Teflon Tava”,c:“Züccaciye”},{n:“Granit Tava”,c:“Züccaciye”},{n:“Izgara Tava”,c:“Züccaciye”},  
{n:“Çaydanlık”,c:“Züccaciye”},{n:“Demlik”,c:“Züccaciye”},{n:“Kettle”,c:“Züccaciye”},{n:“Su Isıtıcı”,c:“Züccaciye”},{n:“Kahve Makinesi”,c:“Züccaciye”},{n:“French Press”,c:“Züccaciye”},{n:“Moka Pot”,c:“Züccaciye”},  
{n:“Bıçak”,c:“Züccaciye”},{n:“Şef Bıçağı”,c:“Züccaciye”},{n:“Ekmek Bıçağı”,c:“Züccaciye”},{n:“Soyma Bıçağı”,c:“Züccaciye”},{n:“Bıçak Seti”,c:“Züccaciye”},{n:“Çatal”,c:“Züccaciye”},{n:“Kaşık”,c:“Züccaciye”},{n:“Tatlı Kaşığı”,c:“Züccaciye”},{n:“Çay Kaşığı”,c:“Züccaciye”},{n:“Servis Kaşığı”,c:“Züccaciye”},{n:“Çatal Kaşık Takımı”,c:“Züccaciye”},  
{n:“Kesme Tahtası”,c:“Züccaciye”},{n:“Ahşap Kesme Tahtası”,c:“Züccaciye”},{n:“Plastik Kesme Tahtası”,c:“Züccaciye”},  
{n:“Kap”,c:“Züccaciye”},{n:“Saklama Kabı”,c:“Züccaciye”},{n:“Cam Saklama Kabı”,c:“Züccaciye”},{n:“Plastik Saklama Kabı”,c:“Züccaciye”},{n:“Vacuum Kap”,c:“Züccaciye”},{n:“Bento Kutusu”,c:“Züccaciye”},{n:“Yemek Kabı”,c:“Züccaciye”},  
{n:“Kavanoz”,c:“Züccaciye”},{n:“Cam Kavanoz”,c:“Züccaciye”},{n:“Mason Kavanoz”,c:“Züccaciye”},{n:“Reçel Kavanozu”,c:“Züccaciye”},  
{n:“Termos”,c:“Züccaciye”},{n:“Matara”,c:“Züccaciye”},{n:“Suluk”,c:“Züccaciye”},{n:“Çelik Matara”,c:“Züccaciye”},  
{n:“Mutfak Tartısı”,c:“Züccaciye”},{n:“Dijital Tartı”,c:“Züccaciye”},{n:“Ölçü Bardağı”,c:“Züccaciye”},{n:“Ölçü Kaşığı”,c:“Züccaciye”},{n:“Ölçü Seti”,c:“Züccaciye”},  
{n:“Rende”,c:“Züccaciye”},{n:“Sebze Rendesi”,c:“Züccaciye”},{n:“Peynir Rendesi”,c:“Züccaciye”},{n:“Mandolin”,c:“Züccaciye”},{n:“Sebze Doğrayıcı”,c:“Züccaciye”},{n:“Doğrayıcı”,c:“Züccaciye”},  
{n:“Blender”,c:“Züccaciye”},{n:“El Blender”,c:“Züccaciye”},{n:“Mutfak Robotu”,c:“Züccaciye”},{n:“Mikser”,c:“Züccaciye”},{n:“El Mikseri”,c:“Züccaciye”},{n:“Smoothie Blender”,c:“Züccaciye”},  
{n:“Elek”,c:“Züccaciye”},{n:“Süzgeç”,c:“Züccaciye”},{n:“Makarna Süzgeci”,c:“Züccaciye”},{n:“Tel Süzgeç”,c:“Züccaciye”},{n:“Kepçe”,c:“Züccaciye”},{n:“Spatula”,c:“Züccaciye”},{n:“Silikon Spatula”,c:“Züccaciye”},{n:“Tahta Kaşık”,c:“Züccaciye”},{n:“Servis Kaşığı Seti”,c:“Züccaciye”},  
{n:“Fırın Tepsisi”,c:“Züccaciye”},{n:“Kek Kalıbı”,c:“Züccaciye”},{n:“Muffin Kalıbı”,c:“Züccaciye”},{n:“Pasta Kalıbı”,c:“Züccaciye”},{n:“Silikon Kalıp”,c:“Züccaciye”},{n:“Yağlı Kağıt”,c:“Züccaciye”},{n:“Fırın Eldiveni”,c:“Züccaciye”},{n:“Pişirme Kağıdı”,c:“Züccaciye”},{n:“Streç Film”,c:“Züccaciye”},{n:“Alüminyum Folyo”,c:“Züccaciye”},  
{n:“Huni”,c:“Züccaciye”},{n:“Açacak”,c:“Züccaciye”},{n:“Şişe Açacağı”,c:“Züccaciye”},{n:“Konserve Açacağı”,c:“Züccaciye”},{n:“Korkmaç”,c:“Züccaciye”},{n:“Şarap Açacağı”,c:“Züccaciye”},  
{n:“Servis Seti”,c:“Züccaciye”},{n:“Yemek Takımı”,c:“Züccaciye”},{n:“Çay Seti”,c:“Züccaciye”},{n:“Kahve Seti”,c:“Züccaciye”},{n:“Tuzluk”,c:“Züccaciye”},{n:“Biberlik”,c:“Züccaciye”},{n:“Tuzluk Biberlik”,c:“Züccaciye”},{n:“Yağdanlık”,c:“Züccaciye”},{n:“Sirkelik”,c:“Züccaciye”},{n:“Sosluk”,c:“Züccaciye”},  
{n:“Çamaşır Ipi”,c:“Tekstil”},{n:“Çamaşır Mandal”,c:“Tekstil”},{n:“Havlu”,c:“Tekstil”},{n:“Banyo Havlusu”,c:“Tekstil”},{n:“El Havlusu”,c:“Tekstil”},{n:“Yüz Havlusu”,c:“Tekstil”},{n:“Plaj Havlusu”,c:“Tekstil”},{n:“Havlu Seti”,c:“Tekstil”},  
{n:“Çarşaf”,c:“Tekstil”},{n:“Nevresim”,c:“Tekstil”},{n:“Nevresim Takımı”,c:“Tekstil”},{n:“Yastık Kılıfı”,c:“Tekstil”},{n:“Pike”,c:“Tekstil”},{n:“Battaniye”,c:“Tekstil”},{n:“Yorgan”,c:“Tekstil”},{n:“Yastık”,c:“Tekstil”},{n:“Uyku Yastığı”,c:“Tekstil”},{n:“Dekoratif Yastık”,c:“Tekstil”},  
{n:“Perde”,c:“Tekstil”},{n:“Tül Perde”,c:“Tekstil”},{n:“Stor Perde”,c:“Tekstil”},{n:“Karartma Perdesi”,c:“Tekstil”},{n:“Duş Perdesi”,c:“Tekstil”},  
{n:“Mutfak Önlüğü”,c:“Tekstil”},{n:“Önlük”,c:“Tekstil”},{n:“Mutfak Lifi”,c:“Tekstil”},{n:“Bulaşık Lifi”,c:“Tekstil”},{n:“Yer Bezi”,c:“Tekstil”},{n:“Halı”,c:“Tekstil”},{n:“Kilim”,c:“Tekstil”},{n:“Paspas”,c:“Tekstil”},{n:“Banyo Paspası”,c:“Tekstil”},{n:“Kapı Paspası”,c:“Tekstil”},  
{n:“Çanta”,c:“Tekstil”},{n:“Alışveriş Çantası”,c:“Tekstil”},{n:“Bez Çanta”,c:“Tekstil”},{n:“Termal Çanta”,c:“Tekstil”},{n:“Sırt Çantası”,c:“Tekstil”},  
{n:“Çorap”,c:“Tekstil”},{n:“Erkek Çorabı”,c:“Tekstil”},{n:“Kadın Çorabı”,c:“Tekstil”},{n:“Spor Çorap”,c:“Tekstil”},{n:“İç Çamaşırı”,c:“Tekstil”},{n:“Atlet”,c:“Tekstil”},{n:“Pijama”,c:“Tekstil”},{n:“Bornoz”,c:“Tekstil”},{n:“Terlik”,c:“Tekstil”},  
{n:“Vida”,c:“Hırdavat”},{n:“Çivi”,c:“Hırdavat”},{n:“Dübel”,c:“Hırdavat”},{n:“Somun”,c:“Hırdavat”},{n:“Cıvata”,c:“Hırdavat”},{n:“Vida Seti”,c:“Hırdavat”},{n:“Çivi Seti”,c:“Hırdavat”},  
{n:“Tornavida”,c:“Hırdavat”},{n:“Tornavida Seti”,c:“Hırdavat”},{n:“Çekiç”,c:“Hırdavat”},{n:“Pense”,c:“Hırdavat”},{n:“Kargaburun”,c:“Hırdavat”},{n:“Anahtar”,c:“Hırdavat”},{n:“İngiliz Anahtarı”,c:“Hırdavat”},{n:“Somun Anahtarı”,c:“Hırdavat”},{n:“Allen Anahtar”,c:“Hırdavat”},{n:“Maket Bıçağı”,c:“Hırdavat”},{n:“Testere”,c:“Hırdavat”},{n:“Demir Testeresi”,c:“Hırdavat”},  
{n:“Ölçü Şeridi”,c:“Hırdavat”},{n:“Metre”,c:“Hırdavat”},{n:“Su Terazisi”,c:“Hırdavat”},{n:“Fırça”,c:“Hırdavat”},{n:“Boya Fırçası”,c:“Hırdavat”},{n:“Rulo”,c:“Hırdavat”},{n:“Boya Rulosu”,c:“Hırdavat”},{n:“Spatula”,c:“Hırdavat”},  
{n:“Yapıştırıcı”,c:“Hırdavat”},{n:“Silikonlu Yapıştırıcı”,c:“Hırdavat”},{n:“Güçlü Yapıştırıcı”,c:“Hırdavat”},{n:“Çift Taraflı Bant”,c:“Hırdavat”},{n:“Yapışkan Bant”,c:“Hırdavat”},{n:“Elektrik Bandı”,c:“Hırdavat”},{n:“İzole Bant”,c:“Hırdavat”},{n:“Selobant”,c:“Hırdavat”},  
{n:“Pil”,c:“Hırdavat”},{n:“AA Pil”,c:“Hırdavat”},{n:“AAA Pil”,c:“Hırdavat”},{n:“9V Pil”,c:“Hırdavat”},{n:“Şarjlı Pil”,c:“Hırdavat”},{n:“Pil Şarjı”,c:“Hırdavat”},  
{n:“Ampul”,c:“Hırdavat”},{n:“LED Ampul”,c:“Hırdavat”},{n:“Floresan”,c:“Hırdavat”},{n:“Gece Lambası”,c:“Hırdavat”},{n:“Uzatma Kablosu”,c:“Hırdavat”},{n:“Çok Prizli”,c:“Hırdavat”},{n:“Priz”,c:“Hırdavat”},{n:“Sigorta”,c:“Hırdavat”},  
{n:“Kilit”,c:“Hırdavat”},{n:“Asma Kilit”,c:“Hırdavat”},{n:“Kapı Kilidi”,c:“Hırdavat”},{n:“Menteşe”,c:“Hırdavat”},{n:“Kanca”,c:“Hırdavat”},{n:“Askı”,c:“Hırdavat”},{n:“Raf Askısı”,c:“Hırdavat”},  
{n:“Hortum”,c:“Hırdavat”},{n:“Bahçe Hortumu”,c:“Hırdavat”},{n:“Sprinkler”,c:“Hırdavat”},{n:“Sulama Kabı”,c:“Hırdavat”},{n:“Bahçe Makası”,c:“Hırdavat”},{n:“Kürek”,c:“Hırdavat”},{n:“Bel Küreği”,c:“Hırdavat”},  
{n:“Çöp Kovası”,c:“Ev Eşyaları”},{n:“Mutfak Çöp Kovası”,c:“Ev Eşyaları”},{n:“Banyo Çöp Kovası”,c:“Ev Eşyaları”},{n:“Pedallı Çöp Kovası”,c:“Ev Eşyaları”},  
{n:“Süpürge”,c:“Ev Eşyaları”},{n:“El Süpürgesi”,c:“Ev Eşyaları”},{n:“Elektrikli Süpürge”,c:“Ev Eşyaları”},{n:“Robot Süpürge”,c:“Ev Eşyaları”},{n:“Faraş”,c:“Ev Eşyaları”},{n:“Faraş Süpürge Seti”,c:“Ev Eşyaları”},{n:“Mop”,c:“Ev Eşyaları”},{n:“Saplı Mop”,c:“Ev Eşyaları”},  
{n:“Kova”,c:“Ev Eşyaları”},{n:“Temizlik Kovası”,c:“Ev Eşyaları”},{n:“Çamaşır Sepeti”,c:“Ev Eşyaları”},{n:“Kirli Çamaşır Sepeti”,c:“Ev Eşyaları”},{n:“Çamaşır Askısı”,c:“Ev Eşyaları”},{n:“Ütü Masası”,c:“Ev Eşyaları”},{n:“Ütü”,c:“Ev Eşyaları”},{n:“Buharlı Ütü”,c:“Ev Eşyaları”},  
{n:“Ayna”,c:“Ev Eşyaları”},{n:“Duvar Aynası”,c:“Ev Eşyaları”},{n:“Boy Aynası”,c:“Ev Eşyaları”},{n:“Banyo Aynası”,c:“Ev Eşyaları”},  
{n:“Raf”,c:“Ev Eşyaları”},{n:“Duvar Rafı”,c:“Ev Eşyaları”},{n:“Mutfak Rafı”,c:“Ev Eşyaları”},{n:“Banyo Rafı”,c:“Ev Eşyaları”},{n:“Kitaplık”,c:“Ev Eşyaları”},{n:“Konsol”,c:“Ev Eşyaları”},  
{n:“Sabunluk”,c:“Ev Eşyaları”},{n:“Sabun Kabı”,c:“Ev Eşyaları”},{n:“Diş Fırçalık”,c:“Ev Eşyaları”},{n:“Tuvalet Fırçası”,c:“Ev Eşyaları”},{n:“Tuvalet Fırça Seti”,c:“Ev Eşyaları”},{n:“Banyo Seti”,c:“Ev Eşyaları”},{n:“Havluluk”,c:“Ev Eşyaları”},{n:“Havlu Askısı”,c:“Ev Eşyaları”},  
{n:“Çerçeve”,c:“Ev Eşyaları”},{n:“Fotoğraf Çerçevesi”,c:“Ev Eşyaları”},{n:“Tablo”,c:“Ev Eşyaları”},{n:“Dekorasyon”,c:“Ev Eşyaları”},{n:“Vazo”,c:“Ev Eşyaları”},{n:“Mum”,c:“Ev Eşyaları”},{n:“Tütsü”,c:“Ev Eşyaları”},{n:“Aromaterapi”,c:“Ev Eşyaları”},{n:“Difüzör”,c:“Ev Eşyaları”},  
{n:“Saat”,c:“Ev Eşyaları”},{n:“Duvar Saati”,c:“Ev Eşyaları”},{n:“Masa Saati”,c:“Ev Eşyaları”},{n:“Alarm Saati”,c:“Ev Eşyaları”},  
{n:“Termostat”,c:“Ev Eşyaları”},{n:“Termometre”,c:“Ev Eşyaları”},{n:“Higrometre”,c:“Ev Eşyaları”},{n:“Hava Durumu İstasyonu”,c:“Ev Eşyaları”},  
{n:“Pil Yuvası”,c:“Ev Eşyaları”},{n:“Kablo Düzenleyici”,c:“Ev Eşyaları”},{n:“Uzaktan Kumanda Tutucu”,c:“Ev Eşyaları”},{n:“Telefon Tutucu”,c:“Ev Eşyaları”},{n:“Şarj Aleti”,c:“Ev Eşyaları”},{n:“USB Hub”,c:“Ev Eşyaları”},  
{n:“Masa Lambası”,c:“Ev Eşyaları”},{n:“Zemin Lambası”,c:“Ev Eşyaları”},{n:“Abajur”,c:“Ev Eşyaları”},{n:“Gece Lambası”,c:“Ev Eşyaları”},  
{n:“Kapı Paspası”,c:“Ev Eşyaları”},{n:“Kapı Durdurucu”,c:“Ev Eşyaları”},{n:“Kapı Arkası Askı”,c:“Ev Eşyaları”}  
];  
var DBNORM=DB.map(function(x){return{n:x.n,c:x.c,k:trk(x.n)};});  
var KW={  
“Süt Ürünleri”:[“süt”,“yoğurt”,“peynir”,“kaşar”,“tulum”,“mozarella”,“lor”,“labne”,“çökelek”,“tereyağı”,“kaymak”,“kefir”,“ayran”,“krema”,“krem şanti”,“mascarpone”,“yumurta”,“hellim”,“gravyer”,“parmesan”,“cheddar”,“gouda”,“edam”,“brie”,“ricotta”,“süzme”,“bıldırcın yumurtası”,“süt tozu”,“soya sütü”,“badem sütü”],  
“Et & Balık”:[“et”,“tavuk”,“kıyma”,“balık”,“dana”,“kuzu”,“hindi”,“sucuk”,“sosis”,“pastırma”,“salam”,“jambon”,“bonfile”,“biftek”,“pirzola”,“köfte”,“kavurma”,“levrek”,“çipura”,“somon”,“hamsi”,“istavrit”,“uskumru”,“sardalya”,“ton”,“midye”,“karides”,“ahtapot”,“kalamar”,“palamut”,“alabalık”,“lüfer”,“barbun”,“mezgit”,“kalkan”,“döner”,“ciğer”,“böbrek”],  
“Sebze & Meyve”:[“domates”,“salatalık”,“biber”,“patlıcan”,“patates”,“soğan”,“sarımsak”,“havuç”,“marul”,“kıvırcık”,“ıspanak”,“kabak”,“brokoli”,“karnabahar”,“mantar”,“şampinyon”,“kereviz”,“turp”,“pancar”,“enginar”,“bamya”,“fasulye”,“pırasa”,“kuşkonmaz”,“roka”,“semizotu”,“tere”,“maydanoz”,“dereotu”,“nane”,“fesleğen”,“kişniş”,“rezene”,“tarhun”,“biberiye”,“lahana”,“mor lahana”,“kırmızı lahana”,“beyaz lahana”,“kara lahana”,“pazı”,“hindiba”,“balkabağı”,“mısır”,“bezelye”,“elma”,“muz”,“portakal”,“mandalina”,“limon”,“armut”,“çilek”,“üzüm”,“kiraz”,“vişne”,“kavun”,“karpuz”,“ananas”,“avokado”,“şeftali”,“kayısı”,“erik”,“nar”,“kivi”,“mango”,“greyfurt”,“incir”,“dut”,“ayva”,“ahududu”,“böğürtlen”,“yaban mersini”,“frambuaz”,“papaya”,“zencefil”,“taze soğan”,“taze sarımsak”,“bebek havuç”,“sakız kabağı”,“tatlı patates”,“kırmızı turp”],  
“Fırın & Ekmek”:[“ekmek”,“tam buğday ekmeği”,“çavdar ekmeği”,“tost ekmeği”,“simit”,“poğaça”,“börek”,“su böreği”,“sigara böreği”,“pasta”,“kek”,“kurabiye”,“kraker”,“bisküvi”,“pide”,“lavaş”,“bazlama”,“baget”,“galeta”,“grisini”,“waffle”,“krep”,“çörek”,“açma”,“tart”,“brownie”,“muffin”,“cupcake”,“cheesecake”,“pancake”,“tortilla”,“pita”],  
“İçecekler”:[“su”,“maden suyu”,“soda”,“meyve suyu”,“kola”,“sprite”,“fanta”,“çay”,“kahve”,“nescafe”,“türk kahvesi”,“espresso”,“filtre kahve”,“bira”,“şarap”,“rakı”,“viski”,“votka”,“limonata”,“ice tea”,“enerji içeceği”,“red bull”,“monster”,“gazoz”,“boza”,“kombucha”,“smoothie”,“ihlamur”,“papatya”,“adaçayı”,“kuşburnu”,“salep”,“kakao”,“sıcak çikolata”,“elma suyu”,“portakal suyu”,“vişne suyu”,“nar suyu”,“şalgam suyu”,“nane limon”,“zencefil çayı”,“yeşil çay”,“mate”,“prosecco”,“şampanya”],  
“Temizlik”:[“deterjan”,“çamaşır suyu”,“çamaşır deterjanı”,“bulaşık deterjanı”,“bulaşık sıvısı”,“bulaşık tableti”,“yumuşatıcı”,“temizlik bezi”,“mutfak bezi”,“kağıt havlu”,“çöp torbası”,“sünger”,“wc taşı”,“tuvalet temizleyici”,“banyo temizleyici”,“cam temizleyici”,“yer temizleyici”,“kireç çözücü”,“fırın temizleyici”,“hava spreyi”,“güve ilacı”,“böcek ilacı”,“ovma teli”,“paspas”,“toz bezi”,“leke çıkarıcı”,“çam suyu”,“mikrofibra”],  
“Kişisel Bakım”:[“diş macunu”,“diş fırçası”,“ağız gargarası”,“tuvalet kağıdı”,“ıslak mendil”,“kağıt mendil”,“el sabunu”,“vücut sabunu”,“şampuan”,“saç kremi”,“saç maskesi”,“saç spreyi”,“saç jeli”,“saç boyası”,“duş jeli”,“vücut losyonu”,“el kremi”,“yüz kremi”,“gece kremi”,“nemlendirici”,“güneş kremi”,“serum”,“tonik”,“deodorant”,“roll-on”,“parfüm”,“kolonya”,“fondöten”,“maskara”,“ruj”,“oje”,“göz kalemi”,“kaş kalemi”,“makyaj”,“jilet”,“tıraş jeli”,“pamuk”,“kulak çubuğu”,“bandaj”,“yara bandı”,“tampon”,“hijyenik ped”,“gece pedi”,“cımbız”,“tırnak makası”,“peeling”,“misel suyu”,“dudak balsamı”],  
“Atıştırmalık”:[“çikolata”,“sütlü çikolata”,“bitter çikolata”,“beyaz çikolata”,“nutella”,“cips”,“patates cipsi”,“gofret”,“şeker”,“bonbon”,“jöle”,“sakız”,“lokum”,“helva”,“baklava”,“fındık”,“fıstık”,“antep fıstığı”,“badem”,“ceviz”,“kaju”,“çerez”,“kabak çekirdeği”,“ay çekirdeği”,“leblebi”,“mısır gevreği”,“granola”,“müsli”,“enerji barı”,“protein bar”,“popcorn”,“kuru üzüm”,“kuru kayısı”,“kuru incir”,“kuru erik”,“hurma”,“keçiboynuzu”,“fıstık ezmesi”,“badem ezmesi”],  
“Dondurulmuş”:[“dondurulmuş”,“dondurma”,“hazır yemek”,“pizza”,“nugget”,“patates kızartması”,“lazanya”,“mantı”,“dondurulmuş sebze”,“dondurulmuş meyve”,“donmuş”,“sorbe”],  
“Züccaciye”:[“tabak”,“kase”,“bardak”,“kupa”,“tencere”,“tava”,“çaydanlık”,“demlik”,“bıçak”,“çatal”,“kaşık”,“kesme tahtası”,“saklama kabı”,“kavanoz”,“termos”,“matara”,“rende”,“blender”,“mikser”,“mutfak robotu”,“elek”,“süzgeç”,“kepçe”,“spatula”,“fırın tepsisi”,“kek kalıbı”,“yağlı kağıt”,“alüminyum folyo”,“streç film”,“açacak”,“tuzluk”,“biberlik”,“yağdanlık”,“çay seti”,“kahve seti”,“ölçü bardağı”,“ölçü kaşığı”,“mutfak tartısı”],  
“Tekstil”:[“havlu”,“banyo havlusu”,“el havlusu”,“çarşaf”,“nevresim”,“yastık kılıfı”,“pike”,“battaniye”,“yorgan”,“yastık”,“perde”,“tül perde”,“duş perdesi”,“önlük”,“halı”,“kilim”,“paspas”,“banyo paspası”,“çorap”,“iç çamaşırı”,“pijama”,“bornoz”,“terlik”,“alışveriş çantası”,“bez çanta”,“çamaşır mandal”],  
“Hırdavat”:[“vida”,“çivi”,“dübel”,“tornavida”,“çekiç”,“pense”,“anahtar”,“maket bıçağı”,“testere”,“metre”,“ölçü şeridi”,“yapıştırıcı”,“çift taraflı bant”,“selobant”,“elektrik bandı”,“pil”,“ampul”,“led ampul”,“uzatma kablosu”,“çok prizli”,“kilit”,“asma kilit”,“kanca”,“hortum”,“sulama kabı”,“bahçe makası”,“kürek”,“boya fırçası”,“rulo”],  
“Ev Eşyaları”:[“çöp kovası”,“süpürge”,“el süpürgesi”,“faraş”,“mop”,“kova”,“çamaşır sepeti”,“ütü”,“ayna”,“raf”,“sabunluk”,“tuvalet fırçası”,“havlu askısı”,“çerçeve”,“vazo”,“mum”,“difüzör”,“saat”,“duvar saati”,“masa lambası”,“kapı paspası”,“çamaşır askısı”],  
“Bakliyat”:[“mercimek”,“nohut”,“fasulye”,“barbunya”,“börülce”,“soya fasulyesi”,“bakla”,“pirinç”,“bulgur”,“makarna”,“spagetti”,“erişte”,“yufka”,“un”,“irmik”,“yulaf”,“kinoa”,“karabuğday”,“nişasta”,“zeytinyağı”,“ayçiçek yağı”,“sıvı yağ”,“sirke”,“elma sirkesi”,“balzamik sirke”,“salça”,“domates salçası”,“biber salçası”,“ketçap”,“mayonez”,“hardal”,“soya sosu”,“nar ekşisi”,“bal”,“pekmez”,“tahin”,“reçel”,“marmelat”,“tuz”,“şeker”,“karabiber”,“pul biber”,“kimyon”,“kekik”,“tarçın”,“zerdeçal”,“köri”,“sumak”,“isot”,“mahlep”,“safran”,“anason”,“çörek otu”,“susam”,“chia”,“keten tohumu”,“kabartma tozu”,“karbonat”,“maya”,“vanilya”,“kakao tozu”,“zeytin”,“yeşil zeytin”,“siyah zeytin”,“turşu”,“kapari”,“humus”,“pesto”,“konserve”]  
};  
function categorize(raw){  
var input=trk(raw);  
var words=input.split(” “).filter(function(w){return w.length>=2;});  
var cats=Object.keys(KW);  
for(var ci=0;ci<cats.length;ci++){  
var list=KW[cats[ci]];  
for(var ki=0;ki<list.length;ki++){if(trk(list[ki])===input)return cats[ci];}  
}  
for(var ci=0;ci<cats.length;ci++){  
var list=KW[cats[ci]];  
for(var ki=0;ki<list.length;ki++){var k=trk(list[ki]);if(input.includes(k)||k.includes(input))return cats[ci];}  
}  
for(var ci=0;ci<cats.length;ci++){  
var list=KW[cats[ci]];  
for(var ki=0;ki<list.length;ki++){  
var k=trk(list[ki]);  
for(var wi=0;wi<words.length;wi++){if(words[wi].length>=3&&(k.includes(words[wi])||words[wi].includes(k)))return cats[ci];}  
}  
}  
var bestCat=“Diğer”,bestDist=99;  
for(var ci=0;ci<cats.length;ci++){  
var list=KW[cats[ci]];  
for(var ki=0;ki<list.length;ki++){  
var k=trk(list[ki]);var maxD=k.length<=5?1:k.length<=9?2:3;  
var d=lev(input,k);  
for(var wi=0;wi<words.length;wi++){if(words[wi].length>=4)d=Math.min(d,lev(words[wi],k));}  
if(d<=maxD&&d<bestDist){bestDist=d;bestCat=cats[ci];}  
}  
}  
return bestCat;  
}  
function saveData(){  
try{localStorage.setItem(“ag”,JSON.stringify(groups));localStorage.setItem(“ab”,JSON.stringify(bought));localStorage.setItem(“au”,String(uid));}catch(e){}  
}  
function loadData(){  
try{  
var g=localStorage.getItem(“ag”);var b=localStorage.getItem(“ab”);var u=localStorage.getItem(“au”);  
if(g)groups=JSON.parse(g);if(b)bought=JSON.parse(b);if(u)uid=parseInt(u)+1;  
}catch(e){}  
}  
var groups={},bought=[],uid=1,sugIndex=-1;  
loadData();  
function getSuggestions(val){  
if(!val||val.length<2)return[];  
var q=trk(val);  
var inList={};  
Object.values(groups).forEach(function(arr){arr.forEach(function(x){inList[trk(x.name)]=1;});});  
var results=[];  
for(var i=0;i<DBNORM.length;i++){  
var item=DBNORM[i];  
if(inList[item.k])continue;  
if(item.k===q){results.unshift(item);continue;}  
if(item.k.startsWith(q)||item.k.includes(q)){results.push(item);continue;}  
if(q.length>=3&&lev(q,item.k.slice(0,q.length+1))<=1)results.push(item);  
}  
return results.slice(0,6);  
}  
function renderSuggestions(val){  
var box=document.getElementById(“suggestions”);  
var sugs=getSuggestions(val);  
if(!sugs.length){box.style.display=“none”;sugIndex=-1;return;}  
var q=val.toLowerCase();  
box.innerHTML=””;  
for(var i=0;i<sugs.length;i++){  
var item=sugs[i];  
var s=CAT[item.c]||CAT[“Diğer”];  
var lname=item.n.toLowerCase();  
var mi=lname.indexOf(q);  
var label=mi>=0?item.n.slice(0,mi)+”<span class='sug-match'>”+item.n.slice(mi,mi+val.length)+”</span>”+item.n.slice(mi+val.length):item.n;  
var div=document.createElement(“div”);  
div.className=“sug-item”;  
div.innerHTML=”<span style='font-size:16px'>”+s.i+”</span><span class='sug-name'>”+label+”</span><span class='sug-cat' style='color:"+s.b+"'>”+item.c+”</span>”;  
(function(name){  
div.addEventListener(“touchend”,function(e){e.preventDefault();selectSug(name);});  
div.addEventListener(“mousedown”,function(e){e.preventDefault();selectSug(name);});  
})(item.n);  
box.appendChild(div);  
}  
box.style.display=“block”;  
}  
function selectSug(name){  
document.getElementById(“item-input”).value=name;  
document.getElementById(“suggestions”).style.display=“none”;  
sugIndex=-1;addItem();  
}  
var inp=document.getElementById(“item-input”);  
inp.addEventListener(“input”,function(){  
var btn=document.getElementById(“add-btn”);  
if(this.value.trim()){btn.style.background=“linear-gradient(135deg,#43e97b,#38f9d7)”;btn.style.boxShadow=“0 4px 18px rgba(67,233,123,0.4)”;}  
else{btn.style.background=“rgba(255,255,255,0.15)”;btn.style.boxShadow=“none”;}  
renderSuggestions(this.value);  
});  
inp.addEventListener(“keydown”,function(e){  
var box=document.getElementById(“suggestions”);  
var items=box.querySelectorAll(”.sug-item”);  
if(e.key===“ArrowDown”){e.preventDefault();sugIndex=Math.min(sugIndex+1,items.length-1);items.forEach(function(el,i){el.style.background=i===sugIndex?“rgba(255,255,255,0.08)”:””;});}  
else if(e.key===“ArrowUp”){e.preventDefault();sugIndex=Math.max(sugIndex-1,-1);items.forEach(function(el,i){el.style.background=i===sugIndex?“rgba(255,255,255,0.08)”:””;});}  
else if(e.key===“Enter”){  
if(sugIndex>=0&&items[sugIndex]){e.preventDefault();var name=items[sugIndex].querySelector(”.sug-name”).textContent;selectSug(name);}  
else addItem();  
}else if(e.key===“Escape”){box.style.display=“none”;sugIndex=-1;}  
else if(e.key===“Tab”&&items.length>0){e.preventDefault();var name=items[0].querySelector(”.sug-name”).textContent;selectSug(name);}  
});  
inp.addEventListener(“blur”,function(){setTimeout(function(){document.getElementById(“suggestions”).style.display=“none”;sugIndex=-1;},150);});  
function showToast(msg){  
var old=document.getElementById(“toast”);if(old)old.remove();  
var t=document.createElement(“div”);t.id=“toast”;t.textContent=msg;  
t.style.cssText=“position:fixed;bottom:90px;left:50%;transform:translateX(-50%);background:rgba(30,20,70,0.95);color:#fff;padding:12px 24px;border-radius:99px;font-size:14px;font-weight:700;z-index:999;white-space:nowrap;pointer-events:none;”;  
document.body.appendChild(t);  
setTimeout(function(){t.style.opacity=“0”;t.style.transition=“opacity .3s”;setTimeout(function(){t.remove();},300);},2500);  
}  
function addItem(){  
var text=inp.value.trim();if(!text)return;  
inp.value=””;  
document.getElementById(“suggestions”).style.display=“none”;  
var cat=categorize(text);  
if(!groups[cat])groups[cat]=[];  
groups[cat].push({id:uid++,name:text});  
var btn=document.getElementById(“add-btn”);  
btn.style.background=“linear-gradient(135deg,#43e97b,#38f9d7)”;  
btn.style.boxShadow=“0 4px 18px rgba(67,233,123,0.4)”;  
saveData();render();inp.focus();  
}  
document.getElementById(“bulk-toggle”).addEventListener(“click”,function(){  
var area=document.getElementById(“bulk-area”);  
var arrow=document.getElementById(“bulk-arrow”);  
var open=area.style.display!==“none”;  
area.style.display=open?“none”:“block”;  
arrow.textContent=open?“▾”:“▴”;  
if(!open)setTimeout(function(){document.getElementById(“bulk-input”).focus();},100);  
});  
document.getElementById(“bulk-btn”).addEventListener(“click”,function(){doBulkImport();});  
function doBulkImport(){  
var ta=document.getElementById(“bulk-input”);  
var rawText=ta.value.trim();  
if(!rawText)return;  
var btn=document.getElementById(“bulk-btn”);  
btn.textContent=“Analiz ediliyor…”;btn.disabled=true;  
var added=0;  
{  
var hasSep=false;  
for(var i=0;i<rawText.length;i++){  
var code=rawText.charCodeAt(i);  
if(code===10||code===13||rawText[i]===”,”||rawText[i]===”;”){hasSep=true;break;}  
}  
var tokens=[];  
if(hasSep){  
var cur=””;  
for(var i=0;i<rawText.length;i++){  
var code=rawText.charCodeAt(i);  
if(code===10||code===13||rawText[i]===”,”||rawText[i]===”;”){  
if(cur.trim())tokens.push(cur.trim());cur=””;  
}else cur+=rawText[i];  
}  
if(cur.trim())tokens.push(cur.trim());  
}else{  
var words=rawText.split(” “).map(function(w){return w.trim();}).filter(function(w){return w.length>0;});  
var used=new Array(words.length).fill(false);  
for(var len=3;len>=2;len–){  
for(var i=0;i<=words.length-len;i++){  
if(used[i])continue;  
var skip=false;for(var j=i;j<i+len;j++)if(used[j]){skip=true;break;}  
if(skip)continue;  
var cand=words.slice(i,i+len).join(” “);  
var candTrk=trk(cand);  
var found=false;  
for(var di=0;di<DBNORM.length;di++){if(DBNORM[di].k===candTrk){found=true;break;}}  
if(!found){var kwcats=Object.keys(KW);for(var ci=0;ci<kwcats.length;ci++){for(var ki=0;ki<KW[kwcats[ci]].length;ki++){if(trk(KW[kwcats[ci]][ki])===candTrk){found=true;break;}}if(found)break;}}  
if(found){tokens.push(cand);for(var j=i;j<i+len;j++)used[j]=true;}  
}  
}  
for(var i=0;i<words.length;i++){  
if(!used[i]){var w=words[i].replace(/^[0-9.-* ]+/,””).trim();if(w.length>=2)tokens.push(w);}  
}  
}  
for(var i=0;i<tokens.length;i++){  
var line=tokens[i].replace(/^[0-9.-* ]+/,””).trim();  
if(line.length<2||line.length>60)continue;  
var cat=categorize(line);  
if(!groups[cat])groups[cat]=[];  
groups[cat].push({id:uid++,name:line});added++;  
}  
}  
ta.value=””;  
document.getElementById(“bulk-area”).style.display=“none”;  
document.getElementById(“bulk-arrow”).textContent=“▾”;  
btn.textContent=“✨ Listeyi Analiz Et ve Ekle”;btn.disabled=false;  
if(added>0){saveData();render();showToast(“✅ “+added+” ürün eklendi!”);}  
else showToast(“⚠️ Ürün bulunamadı”);  
}  
function moveItem(id){  
var cats=Object.keys(groups);  
for(var ci=0;ci<cats.length;ci++){  
var idx=groups[cats[ci]].findIndex(function(x){return x.id===id;});  
if(idx!==-1){var item=groups[cats[ci]][idx];groups[cats[ci]].splice(idx,1);if(!groups[cats[ci]].length)delete groups[cats[ci]];bought.push({id:item.id,name:item.name,category:cats[ci]});break;}  
}saveData();render();  
}  
function deleteItem(id){  
var cats=Object.keys(groups);  
for(var ci=0;ci<cats.length;ci++){  
var idx=groups[cats[ci]].findIndex(function(x){return x.id===id;});  
if(idx!==-1){groups[cats[ci]].splice(idx,1);if(!groups[cats[ci]].length)delete groups[cats[ci]];break;}  
}saveData();render();  
}  
function restoreItem(id){  
var idx=bought.findIndex(function(x){return x.id===id;});  
if(idx===-1)return;  
var item=bought[idx];bought.splice(idx,1);  
var cat=item.category||categorize(item.name);  
if(!groups[cat])groups[cat]=[];  
groups[cat].push({id:item.id,name:item.name});  
saveData();render();  
}  
function resetAll(){groups={};bought=[];saveData();render();}  
document.getElementById(“reset-btn”).addEventListener(“click”,resetAll);  
function attachSwipe(wrapper,itemEl,itemId){  
var sx=0,sy=0,cx=0,drag=false,dec=false;  
var bgR=wrapper.querySelector(”.swipe-bg-right”),bgL=wrapper.querySelector(”.swipe-bg-left”);  
var TH=75;  
function start(x,y){sx=x;sy=y;cx=0;drag=true;dec=false;itemEl.style.transition=“none”;}  
function move(x,y){  
if(!drag)return;var dx=x-sx,dy=y-sy;  
if(!dec&&Math.abs(dy)>Math.abs(dx)&&Math.abs(dy)>10){drag=false;return;}  
if(Math.abs(dx)>8)dec=true;if(!dec)return;cx=dx;  
itemEl.style.transform=“translateX(”+dx+“px)”;  
var r=Math.min(Math.abs(dx)/TH,1);  
if(dx>0){bgR.style.opacity=r;bgL.style.opacity=0;itemEl.style.background=“rgba(39,174,96,”+(r*.2)+”)”;}  
else{bgL.style.opacity=r;bgR.style.opacity=0;itemEl.style.background=“rgba(192,57,43,”+(r*.2)+”)”;}  
}  
function end(){  
if(!drag)return;drag=false;bgR.style.opacity=0;bgL.style.opacity=0;  
itemEl.style.transition=“transform .28s ease,opacity .28s”;  
if(cx>TH){itemEl.style.transform=“translateX(115%)”;itemEl.style.opacity=“0”;(function(id){setTimeout(function(){moveItem(id);},280);})(itemId);}  
else if(cx<-TH){itemEl.style.transform=“translateX(-115%)”;itemEl.style.opacity=“0”;(function(id){setTimeout(function(){deleteItem(id);},280);})(itemId);}  
else{itemEl.style.transform=“translateX(0)”;itemEl.style.background=“rgba(255,255,255,0.04)”;}  
}  
itemEl.addEventListener(“touchstart”,function(e){var t=e.touches[0];start(t.clientX,t.clientY);},{passive:true});  
itemEl.addEventListener(“touchmove”,function(e){var t=e.touches[0];move(t.clientX,t.clientY);if(dec)e.preventDefault();},{passive:false});  
itemEl.addEventListener(“touchend”,end);itemEl.addEventListener(“touchcancel”,end);  
itemEl.addEventListener(“mousedown”,function(e){start(e.clientX,e.clientY);});  
document.addEventListener(“mousemove”,function(e){if(drag)move(e.clientX,e.clientY);});  
document.addEventListener(“mouseup”,function(){if(drag)end();});  
}  
function render(){  
var ge=document.getElementById(“groups”),bs=document.getElementById(“bought-section”),  
bl=document.getElementById(“bought-list”),es=document.getElementById(“empty-state”),  
rw=document.getElementById(“reset-btn-wrap”),pb=document.getElementById(“progress-bar”);  
var ti=Object.values(groups).reduce(function(a,x){return a+x.length;},0);  
var total=ti+bought.length;  
if(total>0){  
pb.style.display=“block”;var pct=Math.round(bought.length/total*100);  
document.getElementById(“bought-count”).textContent=“✓ “+bought.length+” alındı”;  
document.getElementById(“pct-text”).textContent=pct+”%”;  
document.getElementById(“waiting-count”).textContent=ti+” bekliyor”;  
document.getElementById(“progress-fill”).style.width=pct+”%”;  
}else pb.style.display=“none”;  
es.style.display=total===0?“block”:“none”;  
rw.style.display=total>0?“block”:“none”;  
ge.innerHTML=””;  
var cats=Object.keys(groups);  
for(var ci=0;ci<cats.length;ci++){  
var cat=cats[ci],items=groups[cat];  
var s=CAT[cat]||CAT[“Diğer”],r=rgb(s.b);  
var gd=document.createElement(“div”);gd.className=“slide-in”;  
gd.style.cssText=“margin-bottom:12px;background:rgba(255,255,255,0.04);border-radius:20px;overflow:hidden;border:1px solid rgba(255,255,255,0.07)”;  
var hd=document.createElement(“div”);  
hd.style.cssText=“padding:10px 16px;display:flex;align-items:center;gap:8px;background:rgba(”+r+”,.15);border-bottom:1px solid rgba(255,255,255,0.06)”;  
hd.innerHTML=”<span style='font-size:18px'>”+s.i+”</span><span style='color:"+s.b+";font-weight:800;font-size:12px;letter-spacing:1px;text-transform:uppercase'>”+cat+”</span><span style='margin-left:auto;background:"+s.b+";color:#fff;border-radius:99px;min-width:22px;height:22px;display:flex;align-items:center;justify-content:center;font-size:11px;font-weight:800;padding:0 6px'>”+items.length+”</span>”;  
gd.appendChild(hd);  
var iw=document.createElement(“div”);iw.style.padding=“8px”;  
for(var ii=0;ii<items.length;ii++){  
var item=items[ii];  
var wr=document.createElement(“div”);wr.className=“swipe-wrapper slide-in”;  
wr.innerHTML=”<div class='swipe-bg swipe-bg-right'><span style='font-size:16px'>✅</span><span>Alındı</span></div><div class='swipe-bg swipe-bg-left'><span>Sil</span><span style='font-size:16px'>🗑️</span></div>”;  
var ie=document.createElement(“div”);ie.className=“swipe-item”;  
ie.innerHTML=”<div style='width:20px;height:20px;border-radius:6px;border:2px solid "+s.b+"80;flex-shrink:0;'></div><span style='color:rgba(255,255,255,0.85);font-size:14px;font-weight:700;flex:1'>”+item.name+”</span><span style='color:rgba(255,255,255,0.18);font-size:13px'>⇄</span>”;  
wr.appendChild(ie);attachSwipe(wr,ie,item.id);iw.appendChild(wr);  
}  
gd.appendChild(iw);ge.appendChild(gd);  
}  
if(bought.length>0){  
bs.style.display=“block”;bl.innerHTML=””;  
for(var bi=0;bi<bought.length;bi++){  
var item=bought[bi],s=CAT[item.category]||CAT[“Diğer”];  
var chip=document.createElement(“div”);chip.className=“bought-chip slide-in”;  
chip.innerHTML=”<span style='font-size:12px'>”+s.i+”</span><span style='color:rgba(255,255,255,0.3);font-size:13px;font-weight:600;text-decoration:line-through'>”+item.name+”</span><button class='restore-btn' data-id='"+item.id+"'>↩</button>”;  
chip.querySelector(”.restore-btn”).addEventListener(“click”,function(){restoreItem(parseInt(this.getAttribute(“data-id”)));});  
bl.appendChild(chip);  
}  
}else bs.style.display=“none”;  
}  
document.getElementById(“add-btn”).addEventListener(“click”,addItem);  
render();  
</script>  
  
</body>  
</html>  
