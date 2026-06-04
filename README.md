<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Esma Eren</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Poppins',sans-serif;
}

body{
    background:linear-gradient(135deg,#0f172a,#1e293b);
    color:white;
    overflow-x:hidden;
}

.hero{
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    text-align:center;
    padding:30px;
}

.hero-content{
    max-width:900px;
}

.hero h1{
    font-size:4rem;
    color:#ff6bb5;
    margin-bottom:10px;
}

.hero h2{
    font-weight:300;
    margin-bottom:20px;
    color:#d8d8d8;
}

.hero p{
    color:#cfcfcf;
    line-height:1.8;
    font-size:1.1rem;
}

.btns{
    margin-top:30px;
}

.btn{
    display:inline-block;
    text-decoration:none;
    padding:14px 30px;
    border-radius:50px;
    margin:10px;
    font-weight:600;
    transition:.3s;
}

.btn-primary{
    background:#ff6bb5;
    color:white;
}

.btn-primary:hover{
    transform:translateY(-4px);
}

.btn-secondary{
    border:1px solid #ff6bb5;
    color:#ff6bb5;
}

.btn-secondary:hover{
    background:#ff6bb5;
    color:white;
}

.section{
    max-width:1200px;
    margin:auto;
    padding:80px 20px;
}

.section-title{
    text-align:center;
    font-size:2.5rem;
    color:#ff6bb5;
    margin-bottom:50px;
}

.cards{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
    gap:25px;
}

.card{
    background:rgba(255,255,255,.05);
    backdrop-filter:blur(15px);
    border:1px solid rgba(255,255,255,.1);
    border-radius:25px;
    padding:30px;
    transition:.3s;
}

.card:hover{
    transform:translateY(-10px);
}

.card h3{
    color:#ff6bb5;
    margin-bottom:15px;
}

.skills{
    display:flex;
    flex-wrap:wrap;
    gap:12px;
    justify-content:center;
}

.skill{
    padding:10px 18px;
    border-radius:30px;
    background:#ff6bb520;
    border:1px solid #ff6bb5;
}

.project{
    text-align:center;
    padding:40px;
    background:rgba(255,255,255,.05);
    border-radius:25px;
}

.project h3{
    color:#ff6bb5;
    margin-bottom:15px;
}

.project a{
    text-decoration:none;
    color:white;
    background:#ff6bb5;
    padding:12px 25px;
    border-radius:30px;
    display:inline-block;
    margin-top:20px;
}

footer{
    text-align:center;
    padding:40px;
    color:#aaa;
}
</style>
</head>

<body>

<section class="hero">
<div class="hero-content">
<h1>Esma Eren ✨</h1>
<h2>Endüstri Mühendisi • IT Uzmanı</h2>

<p>
Süreç geliştirme, simülasyon, veri analizi ve yazılım geliştirme
alanlarında çalışıyorum. Endüstri mühendisliği bakış açısını
bilgi teknolojileriyle birleştirerek verimli çözümler üretmeyi
hedefliyorum.
</p>

<div class="btns">
<a href="mailto:esma_eren147@hotmail.com" class="btn btn-primary">İletişim</a>
<a href="https://github.com/1esmaeren" class="btn btn-secondary">GitHub</a>
</div>

</div>
</section>

<section class="section">

<h2 class="section-title">Hakkımda</h2>

<div class="cards">

<div class="card">
<h3>🏭 Endüstri Mühendisliği</h3>
<p>
Süreç analizi, iş etüdü, verimlilik artırma ve operasyon yönetimi.
</p>
</div>

<div class="card">
<h3>💻 Bilgi İşlem</h3>
<p>
Kullanıcı desteği, sistem yönetimi ve iş uygulamaları geliştirme.
</p>
</div>

<div class="card">
<h3>📊 Veri ve Simülasyon</h3>
<p>
Üretim süreçlerini modelleme ve karar destek sistemleri geliştirme.
</p>
</div>

</div>

</section>

<section class="section">

<h2 class="section-title">Teknolojiler</h2>

<div class="skills">
<div class="skill">HTML5</div>
<div class="skill">CSS3</div>
<div class="skill">JavaScript</div>
<div class="skill">PHP</div>
<div class="skill">MySQL</div>
<div class="skill">SQL</div>
</div>

</section>

<section class="section">

<h2 class="section-title">Öne Çıkan Proje</h2>

<div class="project">

<h3>🏭 VSM Studio</h3>

<p>
Üretim hattı modelleme ve simülasyon platformu.
Darboğazları ve kayıpları gerçek zamanlı analiz etmeyi sağlar.
</p>

<a href="https://1esmaeren.github.io/simulasyon">
Canlı Demo
</a>

</div>

</section>

<footer>
© 2026 Esma Eren • Tüm Hakları Saklıdır
</footer>

</body>
</html>
