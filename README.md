<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rojali - Portofolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #2c3e50;
            --secondary: #3498db;
            --light: #ecf0f1;
            --dark: #1a252f;
            --accent: #e74c3c;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        header {
            background-color: var(--primary);
            color: white;
            padding: 20px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 24px;
            font-weight: bold;
            color: white;
            text-decoration: none;
        }
        
        .logo span {
            color: var(--secondary);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: var(--secondary);
        }
        
        .hamburger {
            display: none;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            background: linear-gradient(rgba(44, 62, 80, 0.9), rgba(44, 62, 80, 0.9)), url('https://images.unsplash.com/photo-1498050108023-c5249f4df085?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
            color: white;
            text-align: center;
            padding-top: 80px;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 20px;
        }
        
        .hero h1 span {
            color: var(--secondary);
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--secondary);
            color: white;
            padding: 12px 30px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
        }
        
        .btn:hover {
            background-color: #2980b9;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .btn-wa {
            background-color: #25D366;
            margin-left: 10px;
        }
        
        .btn-wa:hover {
            background-color: #128C7E;
        }
        
        /* About Section */
        .about {
            padding: 100px 0;
            background-color: white;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            font-size: 2.5rem;
            color: var(--primary);
        }
        
        .section-title span {
            color: var(--secondary);
        }
        
        .about-content {
            display: flex;
            align-items: center;
            flex-wrap: wrap;
        }
        
        .about-img {
            flex: 1;
            min-width: 300px;
            padding: 20px;
        }
        
        .about-img img {
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .about-text {
            flex: 1;
            min-width: 300px;
            padding: 20px;
        }
        
        .about-text h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--primary);
        }
        
        .about-text p {
            margin-bottom: 15px;
        }
        
        .info {
            margin-top: 30px;
        }
        
        .info-item {
            display: flex;
            margin-bottom: 15px;
        }
        
        .info-item i {
            margin-right: 15px;
            color: var(--secondary);
            font-size: 1.2rem;
        }
        
        /* Skills Section */
        .skills {
            padding: 100px 0;
            background-color: var(--light);
        }
        
        .skills-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 30px;
        }
        
        .skill-card {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            text-align: center;
            width: 250px;
            transition: transform 0.3s;
        }
        
        .skill-card:hover {
            transform: translateY(-10px);
        }
        
        .skill-card i {
            font-size: 3rem;
            color: var(--secondary);
            margin-bottom: 20px;
        }
        
        .skill-card h3 {
            margin-bottom: 15px;
            color: var(--primary);
        }
        
        /* Contact Section */
        .contact {
            padding: 100px 0;
            background-color: white;
        }
        
        .contact-buttons {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 30px;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            text-align: center;
            padding: 30px 0;
        }
        
        .social-links {
            margin-bottom: 20px;
        }
        
        .social-links a {
            color: white;
            font-size: 1.5rem;
            margin: 0 10px;
            transition: color 0.3s;
        }
        
        .social-links a:hover {
            color: var(--secondary);
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                position: fixed;
                top: 80px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 80px);
                background-color: var(--primary);
                flex-direction: column;
                align-items: center;
                justify-content: center;
                transition: left 0.5s;
            }
            
            .nav-links.active {
                left: 0;
            }
            
            .nav-links li {
                margin: 20px 0;
            }
            
            .hamburger {
                display: block;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .contact-buttons {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <a href="#" class="logo">Roj<span>ali</span></a>
                <ul class="nav-links">
                    <li><a href="#home">Beranda</a></li>
                    <li><a href="#about">Tentang</a></li>
                    <li><a href="#skills">Keahlian</a></li>
                    <li><a href="#contact">Kontak</a></li>
                </ul>
                <div class="hamburger">
                    <i class="fas fa-bars"></i>
                </div>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h1>Halo, Saya <span>Rojali</span></h1>
                <p>Seorang Pengembang Software dengan keahlian di Laravel, PHP, JavaScript, dan CSS. Saya mengubah ide menjadi pengalaman digital yang fungsional dan menarik. Perjalanan saya di dunia teknologi didorong oleh rasa ingin tahu dan komitmen untuk terus belajar.</p>
                <a href="#about" class="btn">Jelajahi</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <h2 class="section-title">Tentang <span>Saya</span></h2>
            <div class="about-content">
                <div class="about-img">
                    <img src="Foto.jpeg" alt="Rojali">
                </div>
                <div class="about-text">
                    <h3>Pengembang Software & Spesialis Web</h3>
                    <p>Sebagai lulusan Teknik Informatika dari Universitas Pelita Bangsa, saya berdedikasi untuk menguasai seni pengembangan web. Passion saya terletak pada pembuatan aplikasi yang efisien, scalable, dan user-friendly yang memecahkan masalah di dunia nyata.</p>
                    <p>Saya percaya pada kekuatan teknologi untuk mengubah bisnis dan meningkatkan kehidupan. Tujuan saya adalah berkontribusi pada proyek-proyek bermakna sambil terus memperluas pengetahuan saya dalam teknologi terkini.</p>
                    
                    <div class="info">
                        <div class="info-item">
                            <i class="fas fa-user"></i>
                            <div>
                                <strong>Nama:</strong>
                                <p>Rojali</p>
                            </div>
                        </div>
                        <div class="info-item">
                            <i class="fas fa-calendar-alt"></i>
                            <div>
                                <strong>Tanggal Lahir:</strong>
                                <p>18 Maret 1995</p>
                            </div>
                        </div>
                        <div class="info-item">
                            <i class="fas fa-graduation-cap"></i>
                            <div>
                                <strong>Pendidikan:</strong>
                                <p>Sarjana Teknik Informatika, Universitas Pelita Bangsa</p>
                            </div>
                        </div>
                        <div class="info-item">
                            <i class="fas fa-code"></i>
                            <div>
                                <strong>Spesialisasi:</strong>
                                <p>Pengembangan Web, Laravel, PHP, JavaScript</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section class="skills" id="skills">
        <div class="container">
            <h2 class="section-title">Keahlian <span>Saya</span></h2>
            <div class="skills-container">
                <div class="skill-card">
                    <i class="fab fa-laravel"></i>
                    <h3>Laravel 11</h3>
                    <p>Keahlian dalam membangun aplikasi web robust menggunakan framework Laravel terbaru dengan arsitektur MVC.</p>
                </div>
                <div class="skill-card">
                    <i class="fab fa-php"></i>
                    <h3>PHP</h3>
                    <p>Pemahaman kuat dalam server-side scripting dengan PHP, menciptakan aplikasi web dinamis dan interaktif.</p>
                </div>
                <div class="skill-card">
                    <i class="fab fa-js"></i>
                    <h3>JavaScript</h3>
                    <p>Lumayan Mahir dalam JavaScript untuk menciptakan antarmuka pengguna yang interaktif dan responsif.</p>
                </div>
                <div class="skill-card">
                    <i class="fab fa-css3-alt"></i>
                    <h3>CSS</h3>
                    <p>Terampil dalam membuat layout yang indah dan responsif dengan CSS3, Flexbox, dan sistem Grid.</p>
                </div>
            </div>
        </div>
    </section>

     <!-- Contact Section yang Sudah Diperbaiki -->
     <section class="contact" id="contact">
        <div class="container">
            <h2 class="section-title">Hubungi <span>Saya</span></h2>
            <div style="text-align: center;">
                <p>Saya selalu terbuka untuk diskusi tentang proyek baru, ide kreatif, atau peluang untuk menjadi bagian dari visi Anda.</p>
                <div class="contact-buttons">
                    <a href="mailto:rojali@example.com" class="btn">Email Saya</a>
                    <a href="https://wa.me/6281386049993" class="btn btn-wa" target="_blank">
                        <i class="fab fa-whatsapp"></i> WhatsApp
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer dengan Media Sosial yang Benar -->
    <footer>
        <div class="container">
            <div class="social-links">
                <!-- Ganti username dengan akun asli Anda -->
                <a href="https://github.com/rojali22" target="_blank"><i class="fab fa-github"></i></a>
                <a href="https://linkedin.com/in/rojali22" target="_blank"><i class="fab fa-linkedin"></i></a>
                <a href="https://instagram.com/zali" target="_blank"><i class="fab fa-instagram"></i></a>
            </div>
            <p>&copy; 2023 Rojali. Semua Hak Dilindungi.</p>
        </div>
    </footer>

    <script>
        // Mobile Navigation
        const hamburger = document.querySelector('.hamburger');
        const navLinks = document.querySelector('.nav-links');
        
        hamburger.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });
        
        // Close mobile menu when clicking a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
            });
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                window.scrollTo({
                    top: targetElement.offsetTop - 80,
                    behavior: 'smooth'
                });
            });
        });
        
        // Add scroll effect to header
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 50) {
                header.style.boxShadow = '0 2px 10px rgba(0, 0, 0, 0.1)';
            } else {
                header.style.boxShadow = 'none';
            }
        });
    </script>
</body>
</html>
