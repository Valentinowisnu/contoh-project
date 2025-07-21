<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sribu - Bekerja dengan Desainer Grafis Berbakat secara Online</title>
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
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        .header {
            background: linear-gradient(135deg, #8B1538 0%, #D32F2F 100%);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 2rem;
            font-weight: bold;
            color: white;
        }

        .tagline {
            font-size: 0.9rem;
            opacity: 0.9;
            margin-left: 10px;
        }

        .cta-button {
            background: white;
            color: #8B1538;
            padding: 12px 24px;
            border: none;
            border-radius: 25px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .cta-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #8B1538 0%, #D32F2F 50%, #FF5722 100%);
            color: white;
            padding: 120px 0 80px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grain" width="100" height="100" patternUnits="userSpaceOnUse"><circle cx="20" cy="20" r="1" fill="white" opacity="0.1"/><circle cx="80" cy="80" r="1" fill="white" opacity="0.1"/><circle cx="40" cy="60" r="1" fill="white" opacity="0.1"/></pattern></defs><rect width="100" height="100" fill="url(%23grain)"/></svg>');
            opacity: 0.3;
        }

        .hero-content {
            position: relative;
            z-index: 2;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            font-weight: 700;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            animation: slideInUp 1s ease-out;
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            opacity: 0.95;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            animation: slideInUp 1s ease-out 0.2s both;
        }

        .hero-cta {
            background: white;
            color: #8B1538;
            padding: 15px 40px;
            font-size: 1.1rem;
            border: none;
            border-radius: 30px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            animation: slideInUp 1s ease-out 0.4s both;
        }

        .hero-cta:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.2);
        }

        /* Problem Section */
        .problem-section {
            padding: 80px 0;
            background: #f8f9fa;
        }

        .problem-content {
            text-align: center;
            max-width: 800px;
            margin: 0 auto;
        }

        .section-title {
            font-size: 2.5rem;
            color: #8B1538;
            margin-bottom: 1rem;
            font-weight: 700;
        }

        .problem-text {
            font-size: 1.2rem;
            color: #666;
            margin-bottom: 2rem;
        }

        .reason-box {
            background: white;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            margin-top: 30px;
        }

        .reason-title {
            font-size: 1.5rem;
            color: #8B1538;
            margin-bottom: 1rem;
            font-weight: 600;
        }

        .reason-list {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            gap: 20px;
        }

        .reason-item {
            flex: 1;
            min-width: 200px;
            text-align: center;
            padding: 20px;
        }

        .reason-icon {
            font-size: 3rem;
            color: #D32F2F;
            margin-bottom: 10px;
        }

        /* Comparison Chart */
        .comparison-section {
            padding: 80px 0;
            background: white;
        }

        .comparison-title {
            text-align: center;
            font-size: 2.5rem;
            color: #8B1538;
            margin-bottom: 3rem;
            font-weight: 700;
        }

        .comparison-table {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .table-header {
            background: linear-gradient(135deg, #8B1538 0%, #D32F2F 100%);
            color: white;
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr 1fr;
            padding: 20px;
            font-weight: bold;
        }

        .table-row {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr 1fr;
            padding: 15px 20px;
            border-bottom: 1px solid #eee;
            align-items: center;
        }

        .table-row:nth-child(even) {
            background: #f8f9fa;
        }

        .check-mark {
            color: #28a745;
            font-size: 1.2rem;
            font-weight: bold;
        }

        .x-mark {
            color: #dc3545;
            font-size: 1.2rem;
            font-weight: bold;
        }

        .sribu-highlight {
            background: linear-gradient(135deg, #8B1538 0%, #D32F2F 100%);
            color: white !important;
            font-weight: bold;
        }

        /* Portfolio Section */
        .portfolio-section {
            padding: 80px 0;
            background: #f8f9fa;
        }

        .portfolio-title {
            text-align: center;
            font-size: 2.5rem;
            color: #8B1538;
            margin-bottom: 3rem;
            font-weight: 700;
        }

        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .portfolio-item {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }

        .portfolio-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        }

        .portfolio-image {
            height: 200px;
            background: linear-gradient(45deg, #8B1538, #D32F2F);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.2rem;
            font-weight: bold;
        }

        .portfolio-content {
            padding: 20px;
        }

        .portfolio-category {
            color: #8B1538;
            font-weight: bold;
            margin-bottom: 5px;
        }

        /* About Section */
        .about-section {
            padding: 80px 0;
            background: white;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }

        .about-text {
            font-size: 1.1rem;
            line-height: 1.8;
            color: #666;
        }

        .about-stats {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
        }

        .stat-item {
            text-align: center;
            padding: 30px;
            background: #f8f9fa;
            border-radius: 15px;
        }

        .stat-number {
            font-size: 3rem;
            font-weight: bold;
            color: #8B1538;
            display: block;
        }

        .stat-label {
            color: #666;
            font-size: 1.1rem;
        }

        /* Footer */
        .footer {
            background: linear-gradient(135deg, #8B1538 0%, #D32F2F 100%);
            color: white;
            padding: 60px 0 30px;
            text-align: center;
        }

        .footer-cta {
            font-size: 2rem;
            margin-bottom: 2rem;
            font-weight: 700;
        }

        .footer-button {
            background: white;
            color: #8B1538;
            padding: 15px 40px;
            font-size: 1.1rem;
            border: none;
            border-radius: 30px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            margin-bottom: 3rem;
        }

        .footer-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.2);
        }

        /* Animations */
        @keyframes slideInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .about-content {
                grid-template-columns: 1fr;
                gap: 40px;
            }
            
            .table-header,
            .table-row {
                grid-template-columns: 1fr;
                gap: 10px;
            }
            
            .table-header > *,
            .table-row > * {
                padding: 5px 0;
                text-align: center;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <div class="container">
            <div class="header-content">
                <div>
                    <span class="logo">SRIBU</span>
                    <span class="tagline">Platform Desain Terdepan</span>
                </div>
                <button class="cta-button">Mulai Kontes</button>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Bekerja dengan Desainer Grafis Berbakat secara Online</h1>
                <p>Dapatkan lebih banyak ide desain berkualitas dan ucapkan selamat tinggal pada pertemuan offline yang memakan waktu.</p>
                <button class="hero-cta">Mulai Kontes Desain Sekarang</button>
            </div>
        </div>
    </section>

    <!-- Problem Section -->
    <section class="problem-section">
        <div class="container">
            <div class="problem-content">
                <h2 class="section-title">Masalah yang Sering Dihadapi</h2>
                <p class="problem-text">Sulit menemukan desain terbaik melalui freelancer, studio/agen, atau desainer in-house.</p>
                
                <div class="reason-box">
                    <h3 class="reason-title">Mengapa Hal Ini Terjadi?</h3>
                    <div class="reason-list">
                        <div class="reason-item">
                            <div class="reason-icon">💡</div>
                            <h4>Pilihan Terbatas</h4>
                            <p>Ide kreatif yang terbatas dari sumber tunggal</p>
                        </div>
                        <div class="reason-item">
                            <div class="reason-icon">💰</div>
                            <h4>Biaya Tinggi</h4>
                            <p>Investasi besar tanpa jaminan hasil memuaskan</p>
                        </div>
                        <div class="reason-item">
                            <div class="reason-icon">⏰</div>
                            <h4>Memakan Waktu</h4>
                            <p>Proses revisi yang berulang dan meetings</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Comparison Chart -->
    <section class="comparison-section">
        <div class="container">
            <h2 class="comparison-title">Bandingkan Solusi Desain</h2>
            <div class="comparison-table">
                <div class="table-header">
                    <div>Kriteria</div>
                    <div>Freelancer</div>
                    <div>In-House</div>
                    <div>Agen</div>
                    <div>SRIBU</div>
                </div>
                <div class="table-row">
                    <div><strong>Variasi Desain</strong></div>
                    <div class="x-mark">✗</div>
                    <div class="x-mark">✗</div>
                    <div class="x-mark">✗</div>
                    <div class="check-mark sribu-highlight">✓</div>
                </div>
                <div class="table-row">
                    <div><strong>Biaya Efektif</strong></div>
                    <div class="x-mark">✗</div>
                    <div class="x-mark">✗</div>
                    <div class="x-mark">✗</div>
                    <div class="check-mark sribu-highlight">✓</div>
                </div>
                <div class="table-row">
                    <div><strong>Kecepatan</strong></div>
                    <div class="x-mark">✗</div>
                    <div class="x-mark">✗</div>
                    <div class="x-mark">✗</div>
                    <div class="check-mark sribu-highlight">✓</div>
                </div>
                <div class="table-row">
                    <div><strong>Jaminan Kualitas</strong></div>
                    <div class="x-mark">✗</div>
                    <div class="x-mark">✗</div>
                    <div class="check-mark">✓</div>
                    <div class="check-mark sribu-highlight">✓</div>
                </div>
                <div class="table-row">
                    <div><strong>Tanpa Komitmen Jangka Panjang</strong></div>
                    <div class="check-mark">✓</div>
                    <div class="x-mark">✗</div>
                    <div class="x-mark">✗</div>
                    <div class="check-mark sribu-highlight">✓</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Portfolio Section -->
    <section class="portfolio-section">
        <div class="container">
            <h2 class="portfolio-title">Anda akan mendapatkan desain seperti ini saat bekerja dengan desainer berbakat secara online</h2>
            <div class="portfolio-grid">
                <div class="portfolio-item">
                    <div class="portfolio-image">Logo Design</div>
                    <div class="portfolio-content">
                        <div class="portfolio-category">Logo & Branding</div>
                        <p>Desain logo profesional yang memorable dan mencerminkan identitas brand Anda</p>
                    </div>
                </div>
                <div class="portfolio-item">
                    <div class="portfolio-image">Website Design</div>
                    <div class="portfolio-content">
                        <div class="portfolio-category">Web Design</div>
                        <p>Desain website modern, responsif, dan user-friendly untuk semua perangkat</p>
                    </div>
                </div>
                <div class="portfolio-item">
                    <div class="portfolio-image">Poster Design</div>
                    <div class="portfolio-content">
                        <div class="portfolio-category">Poster & Print</div>
                        <p>Desain poster dan materi marketing yang eye-catching dan efektif</p>
                    </div>
                </div>
                <div class="portfolio-item">
                    <div class="portfolio-image">Mascot Design</div>
                    <div class="portfolio-content">
                        <div class="portfolio-category">Character Design</div>
                        <p>Karakter mascot yang unik dan engaging untuk memperkuat brand identity</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about-section">
        <div class="container">
            <div class="about-content">
                <div>
                    <h2 class="section-title">Tentang Sribu.com</h2>
                    <p class="about-text">
                        Sribu.com adalah website yang menghubungkan antara klien yang membutuhkan desain dan komunitas desainer dari seluruh dunia. Sribu.com menawarkan 20 jenis kategori desain mulai dari logo, website, mascot, poster dan lain-lain. 
                    </p>
                    <p class="about-text">
                        Konsep yang diterapkan di Sribu.com adalah bersifat kontes, dimana Anda akan mendapatkan banyak pilihan desain dari berbagai desainer berbakat, dan Anda hanya perlu memilih yang terbaik.
                    </p>
                </div>
                <div class="about-stats">
                    <div class="stat-item">
                        <span class="stat-number">20+</span>
                        <span class="stat-label">Kategori Desain</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">1000+</span>
                        <span class="stat-label">Desainer Berbakat</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">5000+</span>
                        <span class="stat-label">Proyek Selesai</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">24/7</span>
                        <span class="stat-label">Support</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer CTA -->
    <footer class="footer">
        <div class="container">
            <h2 class="footer-cta">Siap Mendapatkan Desain Terbaik?</h2>
            <button class="footer-button">Mulai Kontes Desain Sekarang</button>
            <p>&copy; 2025 Sribu.com - Platform Desain Terdepan Indonesia</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for better UX
        document.querySelectorAll('button').forEach(button => {
            button.addEventListener('click', function() {
                // Add click animation
                this.style.transform = 'scale(0.95)';
                setTimeout(() => {
                    this.style.transform = '';
                }, 150);
            });
        });

        // Add scroll animation for elements
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Observe portfolio items
        document.querySelectorAll('.portfolio-item').forEach(item => {
            item.style.opacity = '0';
            item.style.transform = 'translateY(30px)';
            item.style.transition = 'all 0.6s ease';
            observer.observe(item);
        });

        // Observe stat items
        document.querySelectorAll('.stat-item').forEach(item => {
            item.style.opacity = '0';
            item.style.transform = 'translateY(30px)';
            item.style.transition = 'all 0.6s ease';
            observer.observe(item);
        });
    </script>
</body>
</html>
