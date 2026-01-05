# Bangkit-network
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Bangkit Network - Layanan WiFi</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family: Arial, sans-serif;
}

body{
    background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)),
    url("https://images.unsplash.com/photo-1518770660439-4636190af475") no-repeat center/cover;
    color:white;
}

header{
    background:#e60000;
    padding:15px;
    text-align:center;
    font-size:24px;
    font-weight:bold;
}

nav{
    display:flex;
    justify-content:center;
    gap:20px;
    background:#111;
    padding:10px;
}

nav a{
    color:white;
    text-decoration:none;
    font-weight:bold;
}

nav a:hover{
    color:#ff0000;
}

section{
    padding:40px 20px;
    max-width:1000px;
    margin:auto;
}

.hero{
    text-align:center;
}

.hero h1{
    font-size:36px;
    margin-bottom:10px;
}

.hero p{
    font-size:18px;
    opacity:0.9;
}

.cards{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:20px;
    margin-top:30px;
}

.card{
    background:rgba(255,255,255,0.1);
    padding:20px;
    border-radius:10px;
    text-align:center;
}

.card h3{
    margin-bottom:10px;
    color:#ff4444;
}

form{
    background:rgba(0,0,0,0.6);
    padding:25px;
    border-radius:10px;
}

form h2{
    text-align:center;
    margin-bottom:20px;
}

input, select, textarea, button{
    width:100%;
    padding:12px;
    margin-bottom:12px;
    border:none;
    border-radius:5px;
}

button{
    background:#e60000;
    color:white;
    font-size:16px;
    font-weight:bold;
    cursor:pointer;
}

button:hover{
    background:#ff0000;
}

footer{
    text-align:center;
    padding:15px;
    background:#111;
    margin-top:40px;
    font-size:14px;
}
</style>
</head>

<body>

<header>Bangkit Network</header>

<nav>
    <a href="#beranda">Beranda</a>
    <a href="#paket">Paket Internet</a>
    <a href="#daftar">Pendaftaran</a>
</nav>

<section id="beranda" class="hero">
    <h1>Layanan Internet WiFi Cepat & Stabil</h1>
    <p>Melayani pemasangan WiFi rumah & bisnis dengan jaringan terbaik</p>
</section>

<section id="paket">
    <h2 style="text-align:center;">Paket Internet</h2>
    <div class="cards">
        <div class="card">
            <h3>Paket 10 Mbps</h3>
            <p>Rp 150.000 / bulan</p>
        </div>
        <div class="card">
            <h3>Paket 20 Mbps</h3>
            <p>Rp 200.000 / bulan</p>
        </div>
        <div class="card">
            <h3>Paket 30 Mbps</h3>
            <p>Rp 300.000 / bulan</p>
        </div>
    </div>
</section>

<section id="daftar">
    <form onsubmit="kirimWA(); return false;">
        <h2>Form Pendaftaran WiFi</h2>

        <input type="text" id="nama" placeholder="Nama Lengkap" required>
        <input type="text" id="alamat" placeholder="Alamat Lengkap" required>
        <input type="tel" id="hp" placeholder="Nomor WhatsApp" required>
        <input type="text" id="nik"
        placeholder="NIK KTP"
        required>

        <select id="paket" required>
            <option value="">-- Pilih Paket --</option>
            <option value="10 Mbps">10 Mbps</option>
            <option value="20 Mbps">20 Mbps</option>
            <option value="30 Mbps">30 Mbps</option>
        </select>

        <button type="submit">Daftar Sekarang</button>
    </form>
</section>

<footer>
    © 2026 Bangkit Network | Internet Cepat & Terpercaya
</footer>

<script>
function kirimWA(){
    let nama = document.getElementById("nama").value;
    let alamat = document.getElementById("alamat").value;
    let hp = document.getElementById("hp").value;
    let nik = document.getElementById("nik").value;
    let paket = document.getElementById("paket").value;
    

    let nomorAdmin = "087782617477"; // GANTI NOMOR ADMIN

    let pesan = 
`Pendaftaran WiFi Bangkit Network

Nama: ${nama}
Alamat: ${alamat}
No HP: ${hp}
Paket: ${paket}
Catatan: ${catatan}`;

    let url = "https://wa.me/" + nomorAdmin + "?text=" + encodeURIComponent(pesan);
    window.open(url, "_blank");
}
</script>

</body>
</html>
