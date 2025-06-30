<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Poppy Piñatas - Custom Piñatas for Any Celebration</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            color: #333;
        }

        /* Header */
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 50px;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .logo {
            display: flex;
            align-items: center;
            font-size: 24px;
            font-weight: bold;
            color: #333;
        }

        .logo::before {
            content: "🎉";
            margin-right: 10px;
            font-size: 30px;
        }

        nav {
            display: flex;
            gap: 30px;
            align-items: center;
        }

        nav a {
            text-decoration: none;
            color: #666;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        nav a:hover {
            color: #FF6B6B;
        }

        .cta-button {
            background: linear-gradient(45deg, #FF6B6B, #FF8E8E);
            color: white;
            padding: 12px 25px;
            border-radius: 25px;
            text-decoration: none;
            font-weight: bold;
            box-shadow: 0 4px 15px rgba(255, 107, 107, 0.3);
            transition: all 0.3s ease;
        }

        .cta-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(255, 107, 107, 0.4);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #FFE4E6 0%, #FFF1E6 25%, #E6F3FF 50%, #F0E6FF 75%, #E6FFE6 100%);
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 120px 50px 80px;
            position: relative;
            overflow: hidden;
        }

        .hero-content {
            flex: 1;
            max-width: 600px;
        }

        .hero h1 {
            font-size: 4rem;
            line-height: 1.1;
            margin-bottom: 30px;
            color: #333;
        }

        .highlight {
            background: linear-gradient(45deg, #FF6B6B, #FF8E8E);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero p {
            font-size: 1.2rem;
            color: #666;
            line-height: 1.6;
            margin-bottom: 40px;
        }

        .action-buttons {
            display: flex;
            gap: 20px;
            margin-bottom: 60px;
        }

        .btn-primary {
            background: linear-gradient(45deg, #FF6B6B, #FF8E8E);
            color: white;
            padding: 15px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 10px;
            box-shadow: 0 4px 15px rgba(255, 107, 107, 0.3);
            transition: all 0.3s ease;
        }

        .btn-secondary {
            background: linear-gradient(45deg, #FFD700, #FFA500);
            color: #333;
            padding: 15px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 10px;
            box-shadow: 0 4px 15px rgba(255, 215, 0, 0.3);
            transition: all 0.3s ease;
        }

        .btn-primary:hover, .btn-secondary:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.2);
        }

        .stats {
            display: flex;
            gap: 60px;
        }

        .stat {
            text-align: center;
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            color: #FF6B6B;
            display: block;
        }

        .stat-label {
            color: #666;
            font-size: 1rem;
            margin-top: 5px;
        }

        .hero-visual {
            flex: 1;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .pinata-placeholder {
            width: 300px;
            height: 400px;
            background: linear-gradient(45deg, #FF1493, #FF69B4, #FFB6C1, #FF6347, #FFD700, #32CD32, #00CED1, #9370DB);
            border-radius: 30px;
            position: relative;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
            transform: rotate(-5deg);
        }

        /* Services Section */
        .services {
            padding: 100px 50px;
            background: #fff;
        }

        .services h2 {
            text-align: center;
            font-size: 3rem;
            margin-bottom: 20px;
            color: #333;
        }

        .services-description {
            text-align: center;
            font-size: 1.2rem;
            color: #666;
            margin-bottom: 80px;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 40px;
            margin-bottom: 80px;
        }

        .service-card {
            background: #F8F9FA;
            padding: 40px 30px;
            border-radius: 20px;
            text-align: center;
            transition: all 0.3s ease;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
        }

        .service-icon {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            margin: 0 auto 30px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
        }

        .service-icon.custom { background: linear-gradient(45deg, #FF6B6B, #FF8E8E); }
        .service-icon.ready { background: linear-gradient(45deg, #FFD700, #FFA500); }
        .service-icon.consultation { background: linear-gradient(45deg, #32CD32, #90EE90); }
        .service-icon.delivery { background: linear-gradient(45deg, #FF8C00, #FFA500); }

        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: #333;
        }

        .service-card p {
            color: #666;
            margin-bottom: 30px;
            line-height: 1.6;
        }

        .service-link {
            color: #FF6B6B;
            text-decoration: none;
            font-weight: bold;
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }

        .cta-section {
            background: linear-gradient(45deg, #FF6B6B, #FF8E8E);
            color: white;
            padding: 60px;
            border-radius: 30px;
            text-align: center;
        }

        .cta-section h3 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        .cta-section p {
            font-size: 1.2rem;
            margin-bottom: 40px;
            opacity: 0.9;
        }

        .cta-section .btn-secondary {
            background: white;
            color: #FF6B6B;
        }

        /* How It Works Section */
        .how-it-works {
            padding: 100px 50px;
            background: #F8F9FA;
        }

        .how-it-works h2 {
            text-align: center;
            font-size: 3rem;
            margin-bottom: 20px;
            color: #333;
        }

        .how-description {
            text-align: center;
            font-size: 1.2rem;
            color: #666;
            margin-bottom: 80px;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
        }

        .process-steps {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 80px;
        }

        .step {
            text-align: center;
            position: relative;
        }

        .step-icon {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            margin: 0 auto 30px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            position: relative;
        }

        .step-icon.idea { background: linear-gradient(45deg, #FF6B6B, #FF8E8E); }
        .step-icon.design { background: linear-gradient(45deg, #FFD700, #FFA500); }
        .step-icon.create { background: linear-gradient(45deg, #32CD32, #90EE90); }
        .step-icon.deliver { background: linear-gradient(45deg, #FF8C00, #FFA500); }

        .step-number {
            position: absolute;
            top: -10px;
            right: -10px;
            width: 30px;
            height: 30px;
            background: #FFD700;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.9rem;
            font-weight: bold;
            color: #333;
        }

        .step h3 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: #333;
        }

        .step p {
            color: #666;
            line-height: 1.6;
        }

        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 80px;
        }

        .feature-card {
            background: white;
            padding: 40px 30px;
            border-radius: 20px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }

        .feature-icon {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background: linear-gradient(45deg, #FF6B6B, #FF8E8E);
            margin: 0 auto 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
        }

        .feature-card h4 {
            font-size: 1.3rem;
            margin-bottom: 15px;
            color: #333;
        }

        .feature-card p {
            color: #666;
            line-height: 1.6;
        }

        .cta-buttons {
            text-align: center;
        }

        .cta-buttons .btn-primary,
        .cta-buttons .btn-secondary {
            margin: 0 10px;
        }

        /* Gallery Section */
        .gallery {
            padding: 100px 50px;
            background: linear-gradient(135deg, #FFE4E6 0%, #FFF1E6 100%);
        }

        .gallery h2 {
            text-align: center;
            font-size: 3rem;
            margin-bottom: 20px;
            color: #333;
        }

        .gallery-description {
            text-align: center;
            font-size: 1.2rem;
            color: #666;
            margin-bottom: 80px;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 60px;
        }

        .gallery-item {
            height: 250px;
            border-radius: 20px;
            position: relative;
            overflow: hidden;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
        }

        .gallery-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
        }

        .gallery-item:nth-child(1) { background: linear-gradient(45deg, #FF1493, #FF69B4, #FFB6C1); }
        .gallery-item:nth-child(2) { background: linear-gradient(45deg, #FFD700, #FFA500, #FF6347); }
        .gallery-item:nth-child(3) { background: linear-gradient(45deg, #32CD32, #90EE90, #00CED1); }
        .gallery-item:nth-child(4) { background: linear-gradient(45deg, #9370DB, #DDA0DD, #FF1493); }
        .gallery-item:nth-child(5) { background: linear-gradient(45deg, #FF4500, #FF6347, #FFD700); }

        .gallery-cta {
            text-align: center;
        }

        .gallery-cta p {
            color: #666;
            margin-bottom: 30px;
            font-size: 1.1rem;
        }

        /* Footer */
        footer {
            background: #2C2C2C;
            color: white;
            padding: 80px 50px 40px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 60px;
            margin-bottom: 60px;
        }

        .footer-section h3 {
            color: #FFD700;
            margin-bottom: 30px;
            font-size: 1.3rem;
        }

        .footer-section p {
            color: #ccc;
            line-height: 1.6;
            margin-bottom: 30px;
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section ul li {
            margin-bottom: 15px;
        }

        .footer-section ul li a {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-section ul li a:hover {
            color: #FFD700;
        }

        .contact-info {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 20px;
        }

        .contact-info .icon {
            width: 40px;
            height: 40px;
            background: linear-gradient(45deg, #FF6B6B, #FF8E8E);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .social-links {
            display: flex;
            gap: 15px;
        }

        .social-link {
            width: 50px;
            height: 50px;
            background: linear-gradient(45deg, #FF6B6B, #FF8E8E);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            color: white;
            font-size: 1.2rem;
            transition: all 0.3s ease;
        }

        .social-link:hover {
            transform: scale(1.1);
            box-shadow: 0 5px 15px rgba(255, 107, 107, 0.4);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 40px;
            border-top: 1px solid #444;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 20px;
        }

        .footer-bottom p {
            color: #999;
            margin: 0;
        }

        .footer-links {
            display: flex;
            gap: 30px;
        }

        .footer-links a {
            color: #999;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-links a:hover {
            color: #FFD700;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero {
                flex-direction: column;
                text-align: center;
                padding: 120px 20px 60px;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .stats {
                justify-content: center;
                margin-top: 40px;
            }

            header {
                padding: 15px 20px;
            }

            nav {
                gap: 15px;
            }

            .services, .how-it-works, .gallery {
                padding: 60px 20px;
            }

            footer {
                padding: 60px 20px 30px;
            }

            .footer-bottom {
                flex-direction: column;
                text-align: center;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="logo">poppy piñatas</div>
        <nav>
            <a href="#custom">Custom Piñatas</a>
            <a href="#ready">Ready-Made Piñatas</a>
            <a href="#gallery">Gallery</a>
            <a href="#faq">FAQs</a>
            <a href="#book" class="cta-button">Book an Appointment</a>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>
                Create the Perfect<br>
                <span class="highlight">Custom Piñata</span> for<br>
                Any Celebration
            </h1>
            
            <p>
                From birthday parties to special events, we craft beautiful 
                custom piñatas and offer ready-made options. Professional 
                design consultations, delivery, and event setup available.
            </p>
            
            <div class="action-buttons">
                <a href="#consultation" class="btn-primary">
                    📅 Book Consultation
                </a>
                <a href="#browse" class="btn-secondary">
                    🔒 Browse Ready-Made
                </a>
            </div>
            
            <div class="stats">
                <div class="stat">
                    <span class="stat-number">500+</span>
                    <div class="stat-label">Custom Designs</div>
                </div>
                <div class="stat">
                    <span class="stat-number">100%</span>
                    <div class="stat-label">Handmade</div>
                </div>
                <div class="stat">
                    <span class="stat-number">24hr</span>
                    <div class="stat-label">Rush Orders</div>
                </div>
            </div>
        </div>
        
        <div class="hero-visual">
            <div class="pinata-placeholder"></div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="services" id="services">
        <h2>Our Piñata Services</h2>
        <p class="services-description">
            From custom creations to ready-made favorites, we offer comprehensive piñata services 
            for every celebration
        </p>
        
        <div class="services-grid">
            <div class="service-card">
                <div class="service-icon custom">🎨</div>
                <h3>Custom Design</h3>
                <p>Work with our designers to create unique, personalized piñatas that match your vision perfectly</p>
                <a href="#" class="service-link">Learn More →</a>
            </div>
            
            <div class="service-card">
                <div class="service-icon ready">👑</div>
                <h3>Ready-Made</h3>
                <p>Choose from our collection of beautiful, pre-made piñatas available for immediate purchase</p>
                <a href="#" class="service-link">Shop Now →</a>
            </div>
            
            <div class="service-card">
                <div class="service-icon consultation">💬</div>
                <h3>Consultation</h3>
                <p>Book a personalized consultation to discuss your ideas and get expert advice on the perfect piñata</p>
                <a href="#" class="service-link">Book Now →</a>
            </div>
            
            <div class="service-card">
                <div class="service-icon delivery">🚚</div>
                <h3>Delivery & Setup</h3>
                <p>Professional delivery and event setup services to make your celebration stress-free and perfect</p>
                <a href="#" class="service-link">Get Details →</a>
            </div>
        </div>
        
        <div class="cta-section">
            <h3>Ready to Get Started?</h3>
            <p>Let's create something amazing for your next celebration</p>
            <a href="#" class="btn-secondary">Schedule Your Consultation</a>
        </div>
    </section>

    <!-- How It Works Section -->
    <section class="how-it-works">
        <h2>How It Works</h2>
        <p class="how-description">
            Getting your perfect piñata is simple and fun - follow these easy steps to bring your 
            celebration to life
        </p>
        
        <div class="process-steps">
            <div class="step">
                <div class="step-icon idea">💡</div>
                <div class="step-number">1</div>
                <h3>Share Your Idea</h3>
                <p>Tell us about your celebration, theme, colors, and any special ideas you have in mind</p>
            </div>
            
            <div class="step">
                <div class="step-icon design">✏️</div>
                <div class="step-number">2</div>
                <h3>Design & Quote</h3>
                <p>We'll create a custom design concept and provide you with a detailed quote for your approval</p>
            </div>
            
            <div class="step">
                <div class="step-icon create">🔨</div>
                <div class="step-number">3</div>
                <h3>We Create</h3>
                <p>Our skilled artisans handcraft your piñata with attention to every detail and quality materials</p>
            </div>
            
            <div class="step">
                <div class="step-icon deliver">🎁</div>
                <div class="step-number">4</div>
                <h3>Delivery & Fun</h3>
                <p>We deliver your custom piñata and can even set it up at your event for the perfect celebration</p>
            </div>
        </div>
        
        <div class="features">
            <div class="feature-card">
                <div class="feature-icon">⏰</div>
                <h4>Quick Turnaround</h4>
                <p>Most orders ready in 3-5 days, rush orders available</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">❤️</div>
                <h4>100% Handmade</h4>
                <p>Each piñata is carefully crafted by skilled artisans</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">🛡️</div>
                <h4>Quality Guaranteed</h4>
                <p>We stand behind every piñata we create</p>
            </div>
        </div>
        
        <div class="cta-buttons">
            <a href="#" class="btn-primary">📅 Book Free Consultation</a>
            <a href="#" class="btn-secondary">👁️ Browse Ready-Made</a>
        </div>
    </section>

    <!-- Gallery Section -->
    <section class="gallery" id="gallery">
        <h2>Our Beautiful Creations</h2>
        <p class="gallery-description">
            Discover the artistry and craftsmanship behind our handmade piñatas - each one a unique 
            masterpiece
        </p>
        
        <div class="gallery-grid">
            <div class="gallery-item"></div>
            <div class="gallery-item"></div>
            <div class="gallery-item"></div>
            <div class="gallery-item"></div>
            <div class="gallery-item"></div>
        </div>
        
        <div class="gallery-cta">
            <p>Want to see more of our work?</p>
            <a href="#" class="btn-primary">📷 View Full Gallery</a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-section">
                <div class="logo" style="color: white; margin-bottom: 30px;">poppy piñatas</div>
                <p>Creating magical moments with handcrafted piñatas for every celebration. From custom designs to ready-made favorites, we bring joy to your special occasions.</p>
                <div class="social-links">
                    <a href="#" class="social-link">f</a>
                    <a href="#" class="social-link">📷</a>
                    <a href="#" class="social-link">🐦</a>
                </div>
            </div>
            
            <div class="footer-section">
                <h3>Our Services</h3>
                <ul>
                    <li><a href="#">🎨 Custom Piñatas</a></li>
                    <li><a href="#">👑 Ready-Made Piñatas</a></li>
                    <li><a href="#">🚚 Delivery & Setup</a></li>
                    <li><a href="#">📅 Appointments</a></li>
                </ul>
            </div>
            
            <div class="footer-section">
                <h3>Quick Links</h3>
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#">About Us</a></li>
                    <li><a href="#">Gallery</a></li>
                    <li><a href="#">FAQs</a></li>
                    <li><a href="#">Blog</a></li>
                    <li><a href="#">Events</a></li>
                    <li><a href="#">Contact</a></li>
                </ul>
            </div>
            
            <div class="footer-section">
                <h3>Get In Touch</h3>
                <div class="contact-info">
                    <div class="icon">📍</div>
                    <div>
                        <strong>Visit Our Studio</strong><br>
                        123 Fiesta Street<br>
                        Party City, PC 12345
                    </div>
                </div>
                <div class="contact-info">
                    <div class="icon">📞</div>
                    <div>
                        <strong>Call Us</strong><br>
                        (123) 456-7890
                    </div>
                </div>
                <div class="contact-info">
                    <div class="icon">✉️</div>
                    <div>
                        <strong>Email Us</strong><br>
                        hello@poppypinatas.com
                    </div>
                </div>
                <div class="contact-info">
                    <div class="icon">🕒</div>
                    <div>
                        <strong>Studio Hours</strong><br>
                        Mon-Fri: 9AM-6PM<br>
                        Sat: 10AM-4PM
                    </div>
                </div>
            </div>
        </div>
        
        <div class="footer-bottom">
            <p>© 2025 Poppy Pinatas. All rights reserved. Made with ❤️ for celebrations.</p>
            <div class="footer-links">
                <a href="#">Privacy Policy</a>
                <a href="#">Terms of Service</a>
            </div>
        </div>
    </footer>
</body>
</html>
