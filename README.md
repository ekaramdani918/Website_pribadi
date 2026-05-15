<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>GreenLife | Hidup Hijau, Bumi Lestari</title>
    <!-- Google Fonts + Font Awesome -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: #f8fef5;
            color: #1e3a2f;
            scroll-behavior: smooth;
            line-height: 1.5;
        }

        /* custom scroll */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #d9e8d5;
        }
        ::-webkit-scrollbar-thumb {
            background: #2c7a4b;
            border-radius: 10px;
        }

        /* container */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 24px;
        }

        /* navbar */
        nav {
            background: white;
            box-shadow: 0 4px 20px rgba(0, 32, 0, 0.05);
            position: sticky;
            top: 0;
            z-index: 100;
            backdrop-filter: blur(2px);
        }
        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 16px 24px;
            max-width: 1280px;
            margin: 0 auto;
            flex-wrap: wrap;
        }
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: #1b5e2a;
        }
        .logo i {
            color: #3c9e5c;
            margin-right: 6px;
        }
        .nav-links {
            display: flex;
            gap: 28px;
            flex-wrap: wrap;
        }
        .nav-links a {
            text-decoration: none;
            font-weight: 500;
            color: #1e4620;
            transition: 0.2s;
            font-size: 1rem;
        }
        .nav-links a:hover {
            color: #2e8b57;
            border-bottom: 2px solid #4caf7f;
            padding-bottom: 4px;
        }

        /* buttons, cards */
        .btn-green {
            background-color: #2c6e3f;
            color: white;
            padding: 10px 24px;
            border-radius: 40px;
            border: none;
            font-weight: 600;
            cursor: pointer;
            transition: 0.2s;
            display: inline-block;
            text-decoration: none;
        }
        .btn-green:hover {
            background-color: #1d5a33;
            transform: translateY(-2px);
        }

        /* hero / banner */
        .hero {
            background: linear-gradient(rgba(35, 79, 40, 0.7), rgba(20, 55, 28, 0.75)), url('https://images.pexels.com/photos/707344/pexels-photo-707344.jpeg?auto=compress&cs=tinysrgb&w=1600');
            background-size: cover;
            background-position: center 30%;
            padding: 100px 20px;
            text-align: center;
            color: white;
            border-radius: 0 0 32px 32px;
        }
        .hero h1 {
            font-size: 3.3rem;
            font-weight: 800;
            letter-spacing: -0.5px;
        }
        .hero p {
            font-size: 1.4rem;
            margin: 20px 0;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
            font-weight: 400;
        }
        .hero .slogan {
            font-size: 1.3rem;
            background: rgba(0,0,0,0.4);
            display: inline-block;
            padding: 8px 28px;
            border-radius: 60px;
            backdrop-filter: blur(3px);
        }
        .btn-hero {
            margin-top: 20px;
            background: #ffd966;
            color: #204d2e;
        }
        .btn-hero:hover {
            background: #ffcd38;
        }

        /* sections */
        section {
            padding: 70px 0;
            border-bottom: 1px solid #ddebe0;
        }
        .section-title {
            font-size: 2.2rem;
            font-weight: 700;
            margin-bottom: 40px;
            position: relative;
            display: inline-block;
        }
        .section-title:after {
            content: '';
            display: block;
            width: 60%;
            height: 4px;
            background: #3ea55c;
            margin-top: 8px;
            border-radius: 4px;
        }

        /* about grid */
        .about-grid {
            display: flex;
            gap: 40px;
            flex-wrap: wrap;
            justify-content: space-between;
        }
        .about-card {
            background: white;
            border-radius: 28px;
            padding: 28px;
            flex: 1;
            box-shadow: 0 12px 24px rgba(0, 32, 0, 0.05);
            transition: 0.2s;
        }
        .about-card i {
            font-size: 2.5rem;
            color: #2d8c4a;
            margin-bottom: 18px;
        }
        .about-card h3 {
            font-size: 1.7rem;
            margin-bottom: 16px;
        }

        /* artikel cards */
        .artikel-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
        }
        .artikel-card {
            background: white;
            border-radius: 24px;
            overflow: hidden;
            flex: 1 1 280px;
            box-shadow: 0 8px 20px rgba(0,0,0,0.05);
            transition: all 0.25s;
        }
        .artikel-card:hover {
            transform: translateY(-6px);
            box-shadow: 0 18px 30px rgba(0,0,0,0.1);
        }
        .artikel-img {
            background: #cfe6d5;
            height: 160px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            color: #1f633a;
        }
        .artikel-content {
            padding: 20px;
        }
        .artikel-content h4 {
            font-size: 1.35rem;
            margin-bottom: 10px;
        }
        .artikel-content p {
            color: #2c4b35;
        }

        /* galeri */
        .galeri-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 28px;
        }
        .galeri-item {
            background: white;
            border-radius: 24px;
            overflow: hidden;
            text-align: center;
            box-shadow: 0 5px 12px rgba(0,0,0,0.08);
            transition: 0.2s;
        }
        .galeri-item .galeri-foto {
            height: 190px;
            background-size: cover;
            background-position: center;
        }
        .galeri-item p {
            padding: 16px;
            font-weight: 500;
            background: #fefcf5;
        }

        /* kontak form */
        .kontak-wrapper {
            display: flex;
            flex-wrap: wrap;
            gap: 40px;
            background: #eef5ea;
            border-radius: 32px;
            padding: 40px;
        }
        .kontak-info {
            flex: 1;
        }
        .kontak-info i {
            font-size: 1.8rem;
            color: #2b7743;
            margin-right: 12px;
        }
        .kontak-info p {
            margin: 18px 0;
            font-size: 1.1rem;
        }
        .form-kontak {
            flex: 2;
        }
        .form-group {
            margin-bottom: 18px;
        }
        input, textarea {
            width: 100%;
            padding: 14px 18px;
            border: 1px solid #caddcd;
            border-radius: 40px;
            font-family: inherit;
            background: white;
            outline: none;
        }
        textarea {
            border-radius: 24px;
            resize: vertical;
        }
        button[type="submit"] {
            background: #2b6e3c;
            border: none;
            padding: 12px 28px;
            border-radius: 40px;
            color: white;
            font-weight: bold;
            cursor: pointer;
            font-size: 1rem;
        }
        .alert-message {
            margin-top: 14px;
            color: #22663a;
            font-weight: 500;
        }

        footer {
            background: #152e1f;
            color: #cfe4d0;
            text-align: center;
            padding: 32px 20px;
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            .nav-container {
                flex-direction: column;
                gap: 12px;
            }
            .hero h1 {
                font-size: 2.3rem;
            }
            .section-title {
                font-size: 1.9rem;
            }
            .kontak-wrapper {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
<nav>
    <div class="nav-container">
        <div class="logo"><i class="fas fa-leaf"></i> GreenLife</div>
        <div class="nav-links">
            <a href="#home">Beranda</a>
            <a href="#tentang">Tentang</a>
            <a href="#artikel">Artikel</a>
            <a href="#galeri">Galeri</a>
            <a href="#kontak">Kontak</a>
        </div>
    </div>
</nav>

<main>
    <!-- 1. HOME -->
    <section id="home" style="padding:0;">
        <div class="hero">
            <div class="slogan"><i class="fas fa-seedling"></i> Mulai dari langkah kecil untuk bumi yang lebih hijau.</div>
            <h1>GreenLife</h1>
            <p>Bergerak bersama melestarikan alam, mengurangi jejak karbon, dan menciptakan masa depan berkelanjutan.</p>
            <a href="#tentang" class="btn-green btn-hero"><i class="fas fa-hand-holding-heart"></i> Aksi Hijau Sekarang</a>
        </div>
    </section>

    <!-- 2. TENTANG KAMI (Visi, Misi, Tujuan, Pentingnya lingkungan) -->
    <section id="tentang">
        <div class="container">
            <h2 class="section-title">🌱 Tentang GreenLife</h2>
            <div class="about-grid">
                <div class="about-card">
                    <i class="fas fa-bullseye"></i>
                    <h3>Visi & Misi</h3>
                    <p><strong>Visi:</strong> “Menciptakan generasi muda yang peduli terhadap lingkungan.”</p>
                    <p><strong>Misi:</strong> Edukasi peduli sampah, tanam pohon, hemat energi, serta mendorong gaya hidup ramah lingkungan melalui aksi nyata dan informasi inspiratif.</p>
                </div>
                <div class="about-card">
                    <i class="fas fa-flag-checkered"></i>
                    <h3>Tujuan Website</h3>
                    <p>Menyediakan wadah edukasi & inspirasi bagi masyarakat untuk bertransformasi menuju kebiasaan ramah lingkungan. Jembatan antara informasi dan gerakan kolektif demi bumi yang lestari.</p>
                </div>
                <div class="about-card">
                    <i class="fas fa-globe-asia"></i>
                    <h3>Pentingnya Menjaga Lingkungan</h3>
                    <p>Bumi adalah rumah kita bersama. Pencemaran, limbah plastik, dan krisis iklim mengancam keseimbangan ekosistem. Setiap tindakan kecil seperti daur ulang, hemat air, dan reboisasi menyelamatkan masa depan anak cucu kita.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 3. ARTIKEL LINGKUNGAN (4 topik) -->
    <section id="artikel">
        <div class="container">
            <h2 class="section-title">📰 Artikel Lingkungan</h2>
            <div class="artikel-grid">
                <div class="artikel-card">
                    <div class="artikel-img"><i class="fas fa-trash-alt fa-3x"></i></div>
                    <div class="artikel-content">
                        <h4>🌍 Kurangi Sampah Plastik</h4>
                        <p>Ganti kantong plastik dengan tas belanja kain, bawa tumbler sendiri, hindari sedotan plastik, serta pilih kemasan ramah lingkungan. Setiap tahun 8 juta ton plastik mencemari laut.</p>
                    </div>
                </div>
                <div class="artikel-card">
                    <div class="artikel-img"><i class="fas fa-industry fa-3x"></i></div>
                    <div class="artikel-content">
                        <h4>⚠️ Dampak Pencemaran</h4>
                        <p>Polusi udara menyebabkan penyakit pernapasan, pencemaran air merusak biota laut, dan tanah tercemar menurunkan kesuburan. Aksi kolektif mengurangi emisi dan pabrik ilegal.</p>
                    </div>
                </div>
                <div class="artikel-card">
                    <div class="artikel-img"><i class="fas fa-lightbulb fa-3x"></i></div>
                    <div class="artikel-content">
                        <h4>💡 Tips Hemat Listrik</h4>
                        <p>Matikan lampu saat tidak digunakan, gunakan peralatan listrik berlabel hemat energi, cabut charger, manfaatkan sinar matahari, dan beralih ke lampu LED.</p>
                    </div>
                </div>
                <div class="artikel-card">
                    <div class="artikel-img"><i class="fas fa-recycle fa-3x"></i></div>
                    <div class="artikel-content">
                        <h4>♻️ Cara Daur Ulang Sampah</h4>
                        <p>Pisahkan organik & anorganik, buat kompos dari sisa makanan, daur ulang kertas menjadi kerajinan, dan manfaatkan botol plastik menjadi pot tanaman vertikal.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 4. GALERI KEGIATAN (4 foto ilustrasi) -->
    <section id="galeri">
        <div class="container">
            <h2 class="section-title">📸 Galeri Kegiatan Hijau</h2>
            <div class="galeri-grid">
                <div class="galeri-item">
                    <div class="galeri-foto" style="background-image: url('https://images.pexels.com/photos/1069623/pexels-photo-1069623.jpeg?auto=compress&cs=tinysrgb&w=600');"></div>
                    <p>🌳 Penanaman Pohon bersama Komunitas</p>
                </div>
                <div class="galeri-item">
                    <div class="galeri-foto" style="background-image: url('https://images.pexels.com/photos/6963985/pexels-photo-6963985.jpeg?auto=compress&cs=tinysrgb&w=600');"></div>
                    <p>🧹 Kerja Bakti Sekolah & Bersih Sungai</p>
                </div>
                <div class="galeri-item">
                    <div class="galeri-foto" style="background-image: url('https://images.pexels.com/photos/6022623/pexels-photo-6022623.jpeg?auto=compress&cs=tinysrgb&w=600');"></div>
                    <p>♻️ Workshop Daur Ulang Sampah Kreatif</p>
                </div>
                <div class="galeri-item">
                    <div class="galeri-foto" style="background-image: url('https://images.pexels.com/photos/210924/pexels-photo-210924.jpeg?auto=compress&cs=tinysrgb&w=600');"></div>
                    <p>🌎 Peringatan Hari Bumi – Aksi Tanam Mangrove</p>
                </div>
            </div>
            <p style="text-align: center; margin-top: 28px; font-style: italic;">✨ Bersama wujudkan lingkungan lebih asri – aksi nyata dari GreenLife!</p>
        </div>
    </section>

    <!-- 5. KONTAK (Email + Form Saran & Pesan) -->
    <section id="kontak">
        <div class="container">
            <h2 class="section-title">📬 Kontak & Kirim Pesan</h2>
            <div class="kontak-wrapper">
                <div class="kontak-info">
                    <h3><i class="fas fa-envelope-open-text"></i> Hubungi Kami</h3>
                    <p><i class="fas fa-envelope"></i> Email: <strong>hello@greenlife.id</strong></p>
                    <p><i class="fas fa-phone-alt"></i> WhatsApp: +62 812 3456 7890</p>
                    <p><i class="fab fa-instagram"></i> Instagram: @greenlife_earth</p>
                    <p style="margin-top: 20px;"><i class="fas fa-map-marker-alt"></i> Sekretariat: Jl. Lestari Hijau No. 9, Jakarta</p>
                    <div style="margin-top: 25px; background:#e2f0e0; border-radius: 20px; padding: 12px;">
                        <i class="fas fa-quote-left"></i> "Kami tunggu saran dan ide hijau darimu!"
                    </div>
                </div>
                <div class="form-kontak">
                    <h3><i class="fas fa-pen-fancy"></i> Kirim Saran / Pesan</h3>
                    <form id="pesanForm">
                        <div class="form-group">
                            <input type="text" id="nama" placeholder="Nama lengkap" required>
                        </div>
                        <div class="form-group">
                            <input type="email" id="email" placeholder="Email aktif" required>
                        </div>
                        <div class="form-group">
                            <textarea rows="4" id="pesan" placeholder="Tulis saran, kritik membangun, atau pesan untuk lingkungan..." required></textarea>
                        </div>
                        <button type="submit"><i class="fas fa-paper-plane"></i> Kirim Pesan</button>
                        <div id="formFeedback" class="alert-message"></div>
                    </form>
                </div>
            </div>
        </div>
    </section>
</main>

<footer>
    <div class="container">
        <p><i class="fas fa-leaf"></i> GreenLife — Bergerak untuk Alam, Aksi untuk Masa Depan</p>
        <p style="margin-top: 12px;">&copy; 2025 GreenLife | #LangkahKecilBumiHijau</p>
        <p style="margin-top: 6px; font-size: 0.8rem;">“Mulai dari langkah kecil untuk bumi yang lebih hijau.” 🌏</p>
    </div>
</footer>

<script>
    // Form handling sederhana untuk feedback (simulasi simpan pesan)
    const form = document.getElementById('pesanForm');
    const feedbackDiv = document.getElementById('formFeedback');

    form.addEventListener('submit', function(e) {
        e.preventDefault();
        const nama = document.getElementById('nama').value.trim();
        const email = document.getElementById('email').value.trim();
        const pesan = document.getElementById('pesan').value.trim();

        if (!nama || !email || !pesan) {
            feedbackDiv.innerHTML = '<span style="color:#c7362b;">✖ Semua bidang harus diisi!</span>';
            feedbackDiv.style.color = "#b4432c";
            setTimeout(() => { feedbackDiv.innerHTML = ''; }, 2500);
            return;
        }
        if (!email.includes('@') || !email.includes('.')) {
            feedbackDiv.innerHTML = '<span style="color:#c7362b;">✖ Masukkan email yang valid.</span>';
            setTimeout(() => { feedbackDiv.innerHTML = ''; }, 2500);
            return;
        }

        // Simulasi sukses mengirim data (tidak ke server riil)
        feedbackDiv.innerHTML = '✅ Terima kasih ' + nama + '! Pesan/saran Anda telah dikirim. Aksi hijau dimulai dari suaramu. 🌿';
        feedbackDiv.style.color = "#1d6738";
        form.reset();
        setTimeout(() => {
            feedbackDiv.innerHTML = '';
        }, 4000);
    });

    // smooth scrolling untuk semua tautan navigasi
    document.querySelectorAll('.nav-links a, .btn-hero').forEach(anchor => {
        anchor.addEventListener('click', function(e) {
            const hash = this.getAttribute('href');
            if(hash && hash.startsWith('#')) {
                e.preventDefault();
                const targetId = hash.substring(1);
                const targetSection = document.getElementById(targetId);
                if(targetSection) {
                    targetSection.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            }
        });
    });
</script>
</body>
</html>
