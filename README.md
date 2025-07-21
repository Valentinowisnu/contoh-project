<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sribu - Bekerja dengan Desainer Grafis Berbakat secara Online</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/js/all.min.js"></script>
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
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        header {
            background: #fff;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }
        
        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
        }
        
        .logo {
            display: flex;
            align-items: center;
            font-size: 2rem;
            font-weight: bold;
            color: #8B1538;
        }
        
        .logo i {
            margin-right: 10px;
            color: #8B1538;
        }
        
        .tagline {
            font-size: 0.9rem;
            color: #666;
            margin-left: 5px;
            font-weight: normal;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #8B1538 0%, #A91B47 50%, #C72C5B 100%);
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
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grid" width="10" height="10" patternUnits="userSpaceOnUse"><path d="M 10 0 L 0 0 0 10" fill="none" stroke="white" stroke-width="0.5" opacity="0.1"/></pattern></defs><rect width="100" height="100" fill="url(%23grid)"/></svg>');
            opacity: 0.3;
        }
        
        .hero-content {
            position: relative;
            z-index: 2;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            font-weight: 700;
            margin-bottom: 20px;
            animation: fadeInUp 1s ease-out;
        }
        
        .hero p {
            font-size: 1.4rem;
            margin-bottom: 40px;
            opacity: 0.95;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            animation: fadeInUp 1s ease-out 0.2s both;
        }
        
        .cta-button {
            display: inline-block;
            background: white;
            color: #8B1538;
            padding: 18px 40px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.2rem;
            transition: all 0.3s ease;
            box-shadow: 0 8px 25px rgba(0,0,0,0.2);
            animation: fadeInUp 1s ease-out 0.4s both;
        }
        
        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 12px 35px rgba(0,0,0,0.3);
            background: #f8f8f8;
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
        
        .problem-title {
            font-size: 2.5rem;
            color: #8B1538;
            margin-bottom: 30px;
            font-weight: 700;
        }
        
        .problem-text {
            font-size: 1.3rem;
            color: #666;
            margin-bottom: 20px;
        }
        
        .reason-text {
            font-size: 1.1rem;
            color: #888;
            font-style: italic;
        }
        
        /* Comparison Section */
        .comparison-section {
            padding: 80px 0;
            background: white;
        }
        
        .comparison-title {
            text-align: center;
            font-size: 2.5rem;
            color: #8B1538;
            margin-bottom: 60px;
            font-weight: 700;
        }
        
        .comparison-table {
            overflow-x: auto;
            margin: 0 auto;
            max-width: 1000px;
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        
        th, td {
            padding: 20px;
            text-align: center;
            border-bottom: 1px solid #eee;
        }
        
        th {
            background: #8B1538;
            color: white;
            font-weight: 600;
            font-size: 1.1rem;
        }
        
        td {
            font-size: 1rem;
        }
        
        .sribu-column {
            background: #f8f9fa;
            font-weight: 600;
        }
        
        .check {
            color: #28a745;
            font-size: 1.5rem;
        }
        
        .cross {
            color: #dc3545;
            font-size: 1.5rem;
        }
        
        .partial {
            color: #ffc107;
            font-size: 1.5rem;
        }
        
        /* Portfolio Section */
        .portfolio-section {
            padding: 80px 0;
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
        }
        
        .portfolio-title {
            text-align: center;
            font-size: 2.5rem;
            color: #8B1538;
            margin-bottom: 60px;
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
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .portfolio-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        }
        
        .portfolio-image {
            height: 200px;
            background: linear-gradient(45deg, #8B1538, #C72C5B);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }
        
        .portfolio-content {
            padding: 25px;
        }
        
        .portfolio-content h3 {
            color: #8B1538;
            margin-bottom: 10px;
            font-size: 1.3rem;
        }
        
        .portfolio-content p {
            color: #666;
            font-size: 1rem;
        }
        
        /* About Section */
        .about-section {
            padding: 80px 0;
            background: white;
        }
        
        .about-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }
        
        .about-title {
            font-size: 2.5rem;
            color: #8B1538;
            margin-bottom: 40px;
            font-weight: 700;
        }
        
        .about-text {
            font-size: 1.2rem;
            color: #666;
            line-height: 1.8;
            margin-bottom: 40px;
        }
        
        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        .stat-item {
            text-align: center;
        }
        
        .stat-number {
            font-size: 3rem;
            font-weight: bold;
            color: #8B1538;
            display: block;
        }
        
        .stat-label {
            font-size: 1.1rem;
            color: #666;
            margin-top: 10px;
        }
        
        /* CTA Section */
        .final-cta {
            padding: 80px 0;
            background: linear-gradient(135deg, #8B1538 0%, #A91B47 50%, #C72C5B 100%);
            text-align: center;
            color: white;
        }
        
        .final-cta h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            font-weight: 700;
        }
        
        .final-cta p {
            font-size: 1.2rem;
            margin-bottom: 40px;
            opacity: 0.95;
        }
        
        .email-form {
            max-width: 500px;
            margin: 0 auto;
            display: flex;
            gap: 15px;
        }
        
        .email-input {
            flex: 1;
            padding: 15px;
            border: none;
            border-radius: 25px;
            font-size: 1rem;
            outline: none;
        }
        
        .submit-btn {
            background: white;
            color: #8B1538;
            border: none;
            padding: 15px 30px;
            border-radius: 25px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        /* Animations */
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
        
        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .problem-title, .comparison-title, .portfolio-title, .about-title {
                font-size: 2rem;
            }
            
            .email-form {
                flex-direction: column;
            }
            
            .nav-container {
                flex-direction: column;
                gap: 10px;
            }
            
            .logo {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="nav-container">
                <div class="logo">
                    <i class="fas fa-palette"></i>
                    Sribu
                    <span class="tagline">Find the Right Freelancer Fast</span>
                </div>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Bekerja dengan Desainer Grafis Berbakat secara Online</h1>
                <p>Dapatkan lebih banyak ide desain berkualitas dan ucapkan selamat tinggal pada pertemuan offline yang memakan waktu.</p>
                <a href="#cta" class="cta-button">Mulai Sekarang <i class="fas fa-arrow-right"></i></a>
            </div>
        </div>
    </section>

    <!-- Problem Section -->
    <section class="problem-section">
        <div class="container">
            <div class="problem-content">
                <h2 class="problem-title">Masalah yang Sering Dihadapi</h2>
                <p class="problem-text">Sulit menemukan desain terbaik melalui freelancer, studio/agen, atau desainer in-house.</p>
                <p class="reason-text">Pilihan ide kreatif yang terbatas, biaya tinggi, dan memakan waktu.</p>
            </div>
        </div>
    </section>

    <!-- Comparison Section -->
    <section class="comparison-section">
        <div class="container">
            <h2 class="comparison-title">Mengapa Memilih Sribu?</h2>
            <div class="comparison-table">
                <table>
                    <thead>
                        <tr>
                            <th>Fitur</th>
                            <th>Freelancer</th>
                            <th>In-house Designer</th>
                            <th>Agensi</th>
                            <th class="sribu-column">Sribu</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td><strong>Kualitas Terjamin</strong></td>
                            <td><i class="fas fa-times cross"></i></td>
                            <td><i class="fas fa-check-circle partial"></i></td>
                            <td><i class="fas fa-check-circle check"></i></td>
                            <td class="sribu-column"><i class="fas fa-check-circle check"></i></td>
                        </tr>
                        <tr>
                            <td><strong>Banyak Pilihan Desain</strong></td>
                            <td><i class="fas fa-times cross"></i></td>
                            <td><i class="fas fa-times cross"></i></td>
                            <td><i class="fas fa-check-circle partial"></i></td>
                            <td class="sribu-column"><i class="fas fa-check-circle check"></i></td>
                        </tr>
                        <tr>
                            <td><strong>Biaya Terjangkau</strong></td>
                            <td><i class="fas fa-check-circle check"></i></td>
                            <td><i class="fas fa-times cross"></i></td>
                            <td><i class="fas fa-times cross"></i></td>
                            <td class="sribu-column"><i class="fas fa-check-circle check"></i></td>
                        </tr>
                        <tr>
                            <td><strong>Waktu Cepat</strong></td>
                            <td><i class="fas fa-check-circle partial"></i></td>
                            <td><i class="fas fa-check-circle check"></i></td>
                            <td><i class="fas fa-times cross"></i></td>
                            <td class="sribu-column"><i class="fas fa-check-circle check"></i></td>
                        </tr>
                        <tr>
                            <td><strong>Revisi Unlimited</strong></td>
                            <td><i class="fas fa-times cross"></i></td>
                            <td><i class="fas fa-check-circle check"></i></td>
                            <td><i class="fas fa-times cross"></i></td>
                            <td class="sribu-column"><i class="fas fa-check-circle check"></i></td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </section>

    <!-- Portfolio Section -->
    <section class="portfolio-section">
        <div class="container">
            <h2 class="portfolio-title">Anda akan mendapatkan desain seperti ini saat bekerja dengan desainer berbakat secara online</h2>
            <div class="portfolio-grid">
                <div class="portfolio-item">
                    <div class="portfolio-image">
                        <i class="fas fa-image"></i>
                    </div>
                    <div class="portfolio-content">
                        <h3>Logo Design</h3>
                        <p>Desain logo profesional yang mencerminkan identitas brand Anda dengan sempurna.</p>
                    </div>
                </div>
                <div class="portfolio-item">
                    <div class="portfolio-image">
                        <i class="fas fa-desktop"></i>
                    </div>
                    <div class="portfolio-content">
                        <h3>Website Design</h3>
                        <p>Website modern dan responsif yang memberikan pengalaman user yang optimal.</p>
                    </div>
                </div>
                <div class="portfolio-item">
                    <div class="portfolio-image">
                        <i class="fas fa-print"></i>
                    </div>
                    <div class="portfolio-content">
                        <h3>Print Design</h3>
                        <p>Desain material marketing yang menarik untuk mendukung strategi promosi Anda.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about-section">
        <div class="container">
            <div class="about-content">
                <h2 class="about-title">Tentang Sribu</h2>
                <p class="about-text">
                    Sribu.com adalah website yang menghubungkan antara klien yang membutuhkan desain dan komunitas desainer dari seluruh dunia. Sribu.com menawarkan 20 jenis kategori desain mulai dari logo, website, mascot, poster dan lain-lain. Konsep yang diterapkan di Sribu.com adalah bersifat kontes.
                </p>
                <div class="stats">
                    <div class="stat-item">
                        <span class="stat-number">30,000+</span>
                        <div class="stat-label">Desainer Berbakat</div>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">15,000+</span>
                        <div class="stat-label">Klien Puas</div>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">20+</span>
                        <div class="stat-label">Kategori Desain</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Final CTA -->
    <section class="final-cta" id="cta">
        <div class="container">
            <h2>Siap Memulai Proyek Desain Anda?</h2>
            <p>Masukkan email Anda dan kami akan mengirimkan panduan lengkap cara bekerja dengan desainer berbakat secara online.</p>
            <form class="email-form">
                <input type="email" class="email-input" placeholder="Masukkan email Anda...">
                <button type="submit" class="submit-btn">Kirim Panduan</button>
            </form>
            <p style="font-size: 0.9rem; margin-top: 20px; opacity: 0.8;">
                *Kami tidak akan mengirim spam ke email Anda
            </p>
        </div>
    </section>

    <script>
        // Smooth scrolling for CTA button
        document.querySelector('.cta-button').addEventListener('click', function(e) {
            e.preventDefault();
            document.querySelector('#cta').scrollIntoView({
                behavior: 'smooth'
            });
        });

        // Form submission
        document.querySelector('.email-form').addEventListener('submit', function(e) {
            e.preventDefault();
            const email = document.querySelector('.email-input').value;
            if (email) {
                alert('Terima kasih! Panduan akan segera dikirim ke email Anda.');
                document.querySelector('.email-input').value = '';
            }
        });

        // Add animation on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(function(entry) {
                if (entry.isIntersecting) {
                    entry.target.style.animation = 'fadeInUp 0.8s ease-out forwards';
                }
            });
        }, observerOptions);

        // Observe all sections
        document.querySelectorAll('section').forEach(function(section) {
            observer.observe(section);
        });
    </script>
</body>
</html>

