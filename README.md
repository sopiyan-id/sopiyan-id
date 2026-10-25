<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sopiyan, S.I.P. | Profil Pribadi</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: #f5f5f5;
        }

        header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            transition: opacity 0.3s;
        }

        .nav-links a:hover {
            opacity: 0.8;
        }

        .menu-toggle {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }

        .hero {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 150px 2rem 100px;
            text-align: center;
            margin-top: 60px;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease;
        }

        .hero .tagline {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .hero p {
            max-width: 700px;
            margin: 0 auto 2rem;
            font-size: 1.1rem;
        }

        .btn {
            display: inline-block;
            padding: 12px 30px;
            background: white;
            color: #667eea;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }

        .btn-secondary {
            background: transparent;
            border: 2px solid white;
            color: white;
            margin-left: 1rem;
        }

        section {
            max-width: 1200px;
            margin: 0 auto;
            padding: 80px 2rem;
        }

        h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            color: #667eea;
            text-align: center;
        }

        .section-subtitle {
            text-align: center;
            color: #666;
            margin-bottom: 3rem;
            font-size: 1.1rem;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }

        .about-text {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .about-info {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .info-item {
            display: flex;
            align-items: center;
            margin-bottom: 1.5rem;
            padding-bottom: 1.5rem;
            border-bottom: 1px solid #eee;
        }

        .info-item:last-child {
            border-bottom: none;
        }

        .info-icon {
            font-size: 2rem;
            margin-right: 1rem;
            min-width: 50px;
        }

        .info-label {
            font-weight: bold;
            color: #667eea;
            display: block;
            margin-bottom: 0.3rem;
        }

        .education-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .education-card {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }

        .education-card:hover {
            transform: translateY(-5px);
        }

        .education-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .interests-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-bottom: 3rem;
        }

        .interest-tag {
            background: white;
            padding: 1rem;
            border-radius: 50px;
            text-align: center;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            transition: all 0.3s;
        }

        .interest-tag:hover {
            background: #667eea;
            color: white;
            transform: scale(1.05);
        }

        .focus-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .focus-card {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .focus-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .principles {
            background: white;
            padding: 3rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .principles-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .principle-item {
            text-align: center;
        }

        .principle-title {
            font-size: 1.3rem;
            font-weight: bold;
            color: #667eea;
            margin-bottom: 1rem;
        }

        .contact {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            text-align: center;
        }

        .contact h2 {
            color: white;
        }

        .contact-btn {
            display: inline-block;
            padding: 15px 40px;
            background: white;
            color: #667eea;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            margin-top: 2rem;
            transition: transform 0.3s;
        }

        .contact-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        }

        footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 2rem;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
                flex-direction: column;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background: #667eea;
                padding: 1rem;
            }

            .nav-links.active {
                display: flex;
            }

            .menu-toggle {
                display: block;
            }

            .hero h1 {
                font-size: 2rem;
            }

            .about-content {
                grid-template-columns: 1fr;
            }

            .btn-secondary {
                margin-left: 0;
                margin-top: 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <div class="logo">SOPIYAN, S.I.P.</div>
            <button class="menu-toggle" onclick="toggleMenu()">☰</button>
            <ul class="nav-links" id="navLinks">
                <li><a href="#beranda">Beranda</a></li>
                <li><a href="#tentang">Tentang</a></li>
                <li><a href="#pendidikan">Pendidikan</a></li>
                <li><a href="#minat">Minat</a></li>
                <li><a href="#kontak">Kontak</a></li>
            </ul>
        </nav>
    </header>

    <section id="beranda" class="hero">
        <h1>SOPIYAN, S.I.P.</h1>
        <p class="tagline">Ilmu Pemerintahan · Pelayanan Publik · Pembangunan Desa Atau Kelurahan</p>
        <p>Berkomitmen untuk terus belajar, berkarya, dan berkontribusi dalam mewujudkan tata kelola pemerintahan yang baik serta pembangunan yang bermanfaat bagi masyarakat.</p>
        <a href="#tentang" class="btn">Kenali Saya</a>
        <a href="#" class="btn btn-secondary" onclick="window.print(); return false;">Cetak PDF</a>
    </section>

    <section id="tentang">
        <h2>Tentang Saya</h2>
        <p class="section-subtitle">Mengenal Lebih Dekat</p>
        <div class="about-content">
            <div class="about-text">
                <p>Saya Sopiyan, S.I.P., dengan latar belakang dan minat di bidang Ilmu Pemerintahan. Saya tertarik pada tata kelola publik, pembangunan desa, pelayanan publik, serta penguatan partisipasi masyarakat dalam proses kebijakan.</p>
                <br>
                <p>Melalui pembelajaran dan pengalaman, saya berupaya mengembangkan wawasan serta kemampuan untuk mendukung pemerintahan yang transparan, akuntabel, responsif, dan berorientasi pada kebutuhan masyarakat.</p>
            </div>
            <div class="about-info">
                <div class="info-item">
                    <span class="info-icon">👤</span>
                    <div>
                        <span class="info-label">Nama</span>
                        SOPIYAN, S.I.P.
                    </div>
                </div>
                <div class="info-item">
                    <span class="info-icon">🏛️</span>
                    <div>
                        <span class="info-label">Bidang</span>
                        Ilmu Pemerintahan dan tata kelola publik
                    </div>
                </div>
                <div class="info-item">
                    <span class="info-icon">🎓</span>
                    <div>
                        <span class="info-label">Pendidikan</span>
                        Ilmu Pemerintahan — Universitas Terbuka
                    </div>
                </div>
                <div class="info-item">
                    <span class="info-icon">🎯</span>
                    <div>
                        <span class="info-label">Fokus</span>
                        Pelayanan publik, pembangunan desa, dan partisipasi masyarakat
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="pendidikan">
        <h2>Pendidikan & Pengembangan</h2>
        <p class="section-subtitle">Belajar untuk Memberi Dampak</p>
        <p style="text-align: center; max-width: 800px; margin: 0 auto 3rem;">Pendidikan menjadi bagian penting dalam memperluas pemahaman tentang pemerintahan, kebijakan publik, dan pembangunan masyarakat.</p>
        <div class="education-grid">
            <div class="education-card">
                <div class="education-icon">🎓</div>
                <h3>Ilmu Pemerintahan</h3>
                <p>Universitas Terbuka — Fakultas Hukum, Ilmu Sosial, dan Ilmu Politik (FHISIP).</p>
            </div>
            <div class="education-card">
                <div class="education-icon">📚</div>
                <h3>Pembelajaran Berkelanjutan</h3>
                <p>Mengembangkan pengetahuan tentang administrasi pemerintahan, kebijakan publik, dan inovasi pelayanan.</p>
            </div>
            <div class="education-card">
                <div class="education-icon">🤝</div>
                <h3>Kolaborasi Masyarakat</h3>
                <p>Mendorong dialog, kerja sama, dan partisipasi warga dalam proses pembangunan.</p>
            </div>
        </div>
    </section>

    <section id="minat">
        <h2>Fokus & Minat</h2>
        <p class="section-subtitle">Bidang yang Saya Dalami</p>
        <p style="text-align: center; max-width: 800px; margin: 0 auto 3rem;">Beberapa tema yang menjadi perhatian dalam pengembangan diri dan kontribusi profesional.</p>
        <div class="interests-grid">
            <div class="interest-tag">Tata Kelola Publik</div>
            <div class="interest-tag">Kebijakan Publik</div>
            <div class="interest-tag">Pembangunan Desa</div>
            <div class="interest-tag">Pelayanan Publik</div>
            <div class="interest-tag">Partisipasi Masyarakat</div>
            <div class="interest-tag">Reformasi Birokrasi</div>
            <div class="interest-tag">Digitalisasi Pemerintahan</div>
            <div class="interest-tag">Pemberdayaan Masyarakat Dan Desa</div>
            <div class="interest-tag">Perencanaan Wilayah dan Kota</div>
        </div>
        <div class="focus-cards">
            <div class="focus-card">
                <div class="focus-icon">🏛️</div>
                <h3>Pemerintahan yang Baik</h3>
                <p>Mendukung prinsip transparansi, akuntabilitas, efektivitas, dan responsivitas dalam penyelenggaraan pemerintahan.</p>
            </div>
            <div class="focus-card">
                <div class="focus-icon">🌱</div>
                <h3>Pembangunan Desa</h3>
                <p>Menaruh perhatian pada potensi lokal, pemberdayaan warga, dan pembangunan desa yang berkelanjutan.</p>
            </div>
            <div class="focus-card">
                <div class="focus-icon">💡</div>
                <h3>Inovasi Pelayanan</h3>
                <p>Mempelajari peluang pemanfaatan teknologi dan inovasi untuk meningkatkan kualitas pelayanan kepada masyarakat.</p>
            </div>
        </div>
    </section>

    <section>
        <h2>Prinsip Pribadi</h2>
        <p class="section-subtitle">Belajar · Berkarya · Berdampak</p>
        <div class="principles">
            <div class="principles-grid">
                <div class="principle-item">
                    <div class="principle-title">Integritas</div>
                    <p>Menjunjung kejujuran, tanggung jawab, dan konsistensi dalam menjalankan amanah.</p>
                </div>
                <div class="principle-item">
                    <div class="principle-title">Kolaborasi</div>
                    <p>Menghargai gagasan dan membangun kerja sama untuk mencapai tujuan bersama.</p>
                </div>
                <div class="principle-item">
                    <div class="principle-title">Pengabdian</div>
                    <p>Mengutamakan manfaat bagi masyarakat sebagai orientasi dalam belajar dan berkarya.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="kontak" class="contact">
        <h2>Mari Terhubung</h2>
        <p style="max-width: 700px; margin: 0 auto;">Terbuka untuk diskusi, kolaborasi, dan pertukaran gagasan seputar pemerintahan, pelayanan publik, serta pembangunan desa/Kelurahan.</p>
        <a href="mailto:sopiyan.go.id@gmail.com" class="contact-btn">Hubungi Saya</a>
        <p style="margin-top: 2rem; font-size: 0.9rem; opacity: 0.8;"
    </section>
    <footer>
        <p><strong>SOPIYAN, S.I.P.</strong></p>
        <p>Belajar · Berkarya · Berdampak</p>
        <p style="margin-top: 1rem; opacity: 0.7;">© 2026 Sopiyan, S.I.P. · Dibuat dengan semangat kontribusi.</p>
    </footer>

    <script>
        function toggleMenu() {
            document.getElementById('navLinks').classList.toggle('active');
        }

        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                    // Close mobile menu
                    document.getElementById('navLinks').classList.remove('active');
                }
            });
        });
    </script>
</body>
</html>
