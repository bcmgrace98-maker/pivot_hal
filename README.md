[showcase-homepage.html](https://github.com/user-attachments/files/29231325/showcase-homepage.html)
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>2026 Online Showcase - GEN C</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Helvetica Neue', sans-serif;
            background: #ffffff;
            color: #2c3e50;
            line-height: 1.6;
        }

        /* Navigation */
        nav {
            border-bottom: 1px solid #e5e5e5;
            padding: 24px 0;
            position: sticky;
            top: 0;
            background: white;
            z-index: 100;
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 24px;
        }

        .nav-logo {
            font-size: 20px;
            font-weight: 700;
            color: #2c3e50;
            margin-bottom: 20px;
            letter-spacing: -0.5px;
        }

        .nav-menu {
            display: grid;
            grid-template-columns: repeat(6, 1fr);
            gap: 0;
            border-top: 1px solid #e5e5e5;
            border-bottom: 1px solid #e5e5e5;
        }

        .nav-item {
            padding: 16px 20px;
            text-align: center;
            font-size: 14px;
            font-weight: 500;
            border-right: 1px solid #e5e5e5;
            cursor: pointer;
            transition: background-color 0.2s;
            color: #2c3e50;
            text-decoration: none;
            display: block;
            letter-spacing: 0.3px;
        }

        .nav-item:last-child {
            border-right: none;
        }

        .nav-item:hover {
            background-color: #f8f9fa;
        }

        /* Hero Section */
        .hero {
            max-width: 1200px;
            margin: 0 auto;
            padding: 80px 24px;
            text-align: center;
        }

        .hero-subtitle {
            font-size: 13px;
            letter-spacing: 1.5px;
            text-transform: uppercase;
            color: #666;
            margin-bottom: 12px;
            font-weight: 500;
        }

        .hero-title {
            font-size: 48px;
            font-weight: 600;
            color: #2c3e50;
            margin-bottom: 8px;
            letter-spacing: -1px;
        }

        .hero-tagline {
            font-size: 18px;
            color: #555;
            margin-bottom: 60px;
            font-weight: 400;
            letter-spacing: 1px;
        }

        .hero-tagline span {
            display: inline-block;
            margin: 0 8px;
        }

        .hero-tagline span:first-child {
            margin-left: 0;
        }

        .hero-tagline span:last-child {
            margin-right: 0;
        }

        .hero-main-title {
            font-size: 140px;
            font-weight: 700;
            color: #2c3e50;
            margin-bottom: 40px;
            line-height: 1;
            letter-spacing: -2px;
            font-family: 'Georgia', serif;
        }

        .hero-divider {
            width: 100%;
            height: 3px;
            background: linear-gradient(to right, transparent, #ffd700 20%, #ffd700 80%, transparent);
            margin: 60px 0;
        }

        /* Themes Section */
        .themes {
            max-width: 1200px;
            margin: 0 auto;
            padding: 80px 24px;
        }

        .themes-title {
            font-size: 13px;
            letter-spacing: 1.5px;
            text-transform: uppercase;
            color: #999;
            margin-bottom: 40px;
            font-weight: 500;
        }

        .themes-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 40px;
            margin-bottom: 60px;
        }

        .theme-card {
            padding: 40px 30px;
            background: #f8f9fa;
            border: 1px solid #efefef;
            text-align: center;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .theme-card:hover {
            background: #f0f0f0;
            border-color: #ddd;
            transform: translateY(-2px);
        }

        .theme-card h3 {
            font-size: 24px;
            font-weight: 700;
            color: #2c3e50;
            margin-bottom: 16px;
        }

        .theme-card p {
            font-size: 14px;
            color: #666;
            line-height: 1.8;
        }

        /* Categories Section */
        .categories-section {
            max-width: 1200px;
            margin: 0 auto;
            padding: 80px 24px;
            border-top: 1px solid #e5e5e5;
        }

        .section-title {
            font-size: 13px;
            letter-spacing: 1.5px;
            text-transform: uppercase;
            color: #999;
            margin-bottom: 40px;
            font-weight: 500;
        }

        .categories-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 24px;
        }

        .category-item {
            padding: 24px 0;
            border-bottom: 1px solid #efefef;
            display: flex;
            justify-content: space-between;
            align-items: center;
            cursor: pointer;
            transition: all 0.2s;
        }

        .category-item:last-child {
            border-bottom: none;
        }

        .category-item:hover {
            padding-left: 8px;
        }

        .category-name {
            font-size: 16px;
            font-weight: 500;
            color: #2c3e50;
        }

        .category-arrow {
            color: #ccc;
            font-size: 18px;
            transition: all 0.2s;
        }

        .category-item:hover .category-arrow {
            color: #2c3e50;
            transform: translateX(4px);
        }

        /* Footer */
        footer {
            background: #f8f9fa;
            border-top: 1px solid #e5e5e5;
            margin-top: 80px;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 60px 24px;
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 40px;
        }

        .footer-section h4 {
            font-size: 12px;
            letter-spacing: 1px;
            text-transform: uppercase;
            color: #999;
            margin-bottom: 16px;
            font-weight: 600;
        }

        .footer-section a {
            display: block;
            margin-bottom: 12px;
            color: #666;
            text-decoration: none;
            font-size: 14px;
            transition: color 0.2s;
        }

        .footer-section a:hover {
            color: #2c3e50;
        }

        .footer-bottom {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 24px;
            border-top: 1px solid #e5e5e5;
            text-align: center;
            color: #999;
            font-size: 13px;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-menu {
                grid-template-columns: repeat(3, 1fr);
            }

            .hero-main-title {
                font-size: 80px;
            }

            .themes-grid {
                grid-template-columns: 1fr;
                gap: 24px;
            }

            .categories-grid {
                grid-template-columns: 1fr;
            }

            .footer-content {
                grid-template-columns: 1fr;
            }

            .hero {
                padding: 60px 24px;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <div class="nav-logo">CITD</div>
            <div class="nav-menu">
                <a href="#citd" class="nav-item">CITD</a>
                <a href="#showcase" class="nav-item">SHOWCASE</a>
                <a href="#genc-pick" class="nav-item">Gen C's Pick</a>
                <a href="#archive" class="nav-item">Archive</a>
                <a href="#event" class="nav-item">EVENT</a>
                <a href="#contact" class="nav-item">CONTACT</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-subtitle">2026 Online Showcase</div>
        <h1 class="hero-title">GEN C</h1>
        <div class="hero-tagline">
            <span>Content</span>
            <span>·</span>
            <span>Creativity</span>
            <span>·</span>
            <span>Challenge</span>
        </div>
        
        <h2 class="hero-main-title">pivot</h2>
        
        <div class="hero-divider"></div>
    </section>

    <!-- Themes Section -->
    <section class="themes">
        <h3 class="themes-title">Core Themes</h3>
        
        <div class="themes-grid">
            <div class="theme-card">
                <h3>Content</h3>
                <p>Diverse voices and perspectives from our emerging creators. Authentic narratives that reflect contemporary culture and innovation.</p>
            </div>
            <div class="theme-card">
                <h3>Creativity</h3>
                <p>Boundary-pushing work that challenges conventions. Experimental approaches to visual language, design thinking, and storytelling.</p>
            </div>
            <div class="theme-card">
                <h3>Challenge</h3>
                <p>Addressing real-world problems through creative solutions. Work that engages with current issues and imagines better futures.</p>
            </div>
        </div>
    </section>

    <!-- Categories Section -->
    <section class="categories-section">
        <h3 class="section-title">Explore</h3>
        
        <div class="categories-grid">
            <div class="category-item">
                <span class="category-name">SHOWCASE</span>
                <span class="category-arrow">→</span>
            </div>
            <div class="category-item">
                <span class="category-name">Gen C's Pick</span>
                <span class="category-arrow">→</span>
            </div>
            <div class="category-item">
                <span class="category-name">Archive</span>
                <span class="category-arrow">→</span>
            </div>
            <div class="category-item">
                <span class="category-name">EVENT</span>
                <span class="category-arrow">→</span>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-section">
                <h4>About</h4>
                <a href="#">About GEN C</a>
                <a href="#">CITD</a>
                <a href="#">Guidelines</a>
            </div>
            <div class="footer-section">
                <h4>Connect</h4>
                <a href="#">Instagram</a>
                <a href="#">Email</a>
                <a href="#">Newsletter</a>
            </div>
            <div class="footer-section">
                <h4>Info</h4>
                <a href="#">Privacy Policy</a>
                <a href="#">Terms</a>
                <a href="#">Contact</a>
            </div>
        </div>
        <div class="footer-bottom">
            <p>&copy; 2026 GEN C Showcase. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
