# Vegetables-app-
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>V Unit - Fresh Vegetables Delivered Fast</title>

  <!-- Google Fonts for modern typography -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">

  <style>
    /* ==========================================================================
       1. GLOBAL & RESET STYLES
       ========================================================================== */
    :root {
      /* Professional Fresh Color Palette */
      --primary: #2E7D32;        /* Fresh Forest Green */
      --primary-hover: #1B5E20;  /* Darker Green for hover states */
      --secondary: #FF8F00;      /* Vibrant Orange / Produce Accent */
      --secondary-hover: #E65100;/* Darker Orange */
      --bg-light: #F4F7F4;       /* Subtle off-white background */
      --card-bg: #FFFFFF;        /* White background for cards */
      --text-main: #212121;      /* High contrast body text */
      --text-muted: #616161;     /* Secondary text */
      --border-color: #E0E0E0;  /* Clean light borders */
      --radius: 12px;            /* Modern border radius */
      --shadow: 0 4px 16px rgba(0, 0, 0, 0.08); /* Soft elevation shadow */
      --font-heading: 'Poppins', sans-serif;
      --font-body: 'Inter', sans-serif;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: var(--font-body);
      background-color: var(--bg-light);
      color: var(--text-main);
      line-height: 1.6;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    ul {
      list-style: none;
    }

    /* Container for consistent alignment */
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }

    .section-padding {
      padding: 80px 0;
    }

    .section-title {
      font-family: var(--font-heading);
      font-size: 2.2rem;
      text-align: center;
      margin-bottom: 12px;
      color: var(--primary);
    }

    .section-subtitle {
      text-align: center;
      color: var(--text-muted);
      margin-bottom: 48px;
      font-size: 1.05rem;
    }

    /* Primary and Secondary Buttons */
    .btn {
      display: inline-block;
      padding: 14px 28px;
      border-radius: var(--radius);
      font-family: var(--font-heading);
      font-weight: 600;
      font-size: 1rem;
      cursor: pointer;
      transition: all 0.3s ease;
      border: none;
      text-align: center;
    }

    .btn-primary {
      background-color: var(--primary);
      color: #ffffff;
    }

    .btn-primary:hover {
      background-color: var(--primary-hover);
      transform: translateY(-2px);
    }

    .btn-secondary {
      background-color: var(--secondary);
      color: #ffffff;
    }

    .btn-secondary:hover {
      background-color: var(--secondary-hover);
      transform: translateY(-2px);
    }

    /* ==========================================================================
       2. HEADER & NAVIGATION
       ========================================================================== */
    .header {
      background-color: #ffffff;
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    .nav-container {
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 70px;
    }

    .logo {
      font-family: var(--font-heading);
      font-size: 1.8rem;
      font-weight: 700;
      color: var(--primary);
      display: flex;
      align-items: center;
      gap: 6px;
    }

    .logo span {
      color: var(--secondary);
    }

    .nav-links {
      display: flex;
      gap: 28px;
      align-items: center;
    }

    .nav-links a {
      font-weight: 500;
      transition: color 0.3s;
    }

    .nav-links a:hover {
      color: var(--primary);
    }

    /* ==========================================================================
       3. HERO SECTION
       ========================================================================== */
    .hero {
      background: linear-gradient(135deg, rgba(46, 125, 50, 0.08), rgba(255, 143, 0, 0.08));
      padding: 100px 0 80px 0;
    }

    .hero-wrapper {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 40px;
      align-items: center;
    }

    .hero-content h1 {
      font-family: var(--font-heading);
      font-size: 2.8rem;
      line-height: 1.2;
      margin-bottom: 20px;
      color: var(--text-main);
    }

    .hero-content p {
      font-size: 1.1rem;
      color: var(--text-muted);
      margin-bottom: 30px;
    }

    .hero-buttons {
      display: flex;
      gap: 16px;
      flex-wrap: wrap;
    }

    .hero-card {
      background: var(--card-bg);
      padding: 32px;
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      text-align: center;
      border-top: 5px solid var(--primary);
    }

    .hero-card h3 {
      font-family: var(--font-heading);
      margin-bottom: 12px;
      font-size: 1.5rem;
    }

    /* ==========================================================================
       4. ABOUT SECTION
       ========================================================================== */
    .about-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 24px;
    }

    .about-card {
      background: var(--card-bg);
      padding: 28px;
      border-radius: var(--radius);
      border: 1px solid var(--border-color);
      box-shadow: 0 2px 8px rgba(0,0,0,0.04);
    }

    .about-card h3 {
      font-family: var(--font-heading);
      color: var(--primary);
      margin-bottom: 12px;
    }

    /* ==========================================================================
       5. SERVICES SECTION
       ========================================================================== */
    .services {
      background-color: #ffffff;
    }

    .services-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 30px;
    }

    .service-box {
      padding: 32px;
      border-radius: var(--radius);
      background: var(--bg-light);
      text-align: center;
      transition: transform 0.3s ease;
    }

    .service-box:hover {
      transform: translateY(-5px);
    }

    .service-icon {
      font-size: 2.5rem;
      margin-bottom: 16px;
    }

    .service-box h3 {
      font-family: var(--font-heading);
      margin-bottom: 12px;
      color: var(--primary);
    }

    /* ==========================================================================
       6. PRODUCTS SECTION
       ========================================================================== */
    .product-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 24px;
    }

    .product-card {
      background: var(--card-bg);
      border-radius: var(--radius);
      padding: 20px;
      text-align: center;
      box-shadow: var(--shadow);
      border: 1px solid var(--border-color);
    }

    .product-emoji {
      font-size: 3.5rem;
      margin-bottom: 12px;
    }

    .product-card h4 {
      font-family: var(--font-heading);
      font-size: 1.2rem;
      margin-bottom: 6px;
    }

    .product-card p {
      color: var(--text-muted);
      font-size: 0.9rem;
      margin-bottom: 16px;
    }

    /* ==========================================================================
       7. CONTACT & FREE DEMO FORM SECTION
       ========================================================================== */
    .contact-section {
      background-color: #ffffff;
    }

    .contact-wrapper {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 40px;
    }

    .contact-info {
      display: flex;
      flex-direction: column;
      gap: 24px;
    }

    .info-item {
      display: flex;
      align-items: flex-start;
      gap: 16px;
    }

    .info-icon {
      background: rgba(46, 125, 50, 0.1);
      color: var(--primary);
      width: 44px;
      height: 44px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: bold;
      flex-shrink: 0;
    }

    /* Form styling */
    .form-container {
      background: var(--bg-light);
      padding: 32px;
      border-radius: var(--radius);
      border: 1px solid var(--border-color);
    }

    .form-group {
      margin-bottom: 20px;
    }

    .form-group label {
      display: block;
      font-weight: 500;
      margin-bottom: 8px;
      font-size: 0.95rem;
    }

    .form-group input,
    .form-group textarea,
    .form-group select {
      width: 100%;
      padding: 12px 16px;
      border: 1px solid var(--border-color);
      border-radius: 8px;
      font-family: var(--font-body);
      font-size: 1rem;
      outline: none;
      transition: border-color 0.3s;
    }

    .form-group input:focus,
    .form-group textarea:focus,
    .form-group select:focus {
      border-color: var(--primary);
    }

    .form-group textarea {
      resize: vertical;
      min-height: 120px;
    }

    /* ==========================================================================
       8. FLOATING WHATSAPP BUTTON
       ========================================================================== */
    .whatsapp-float {
      position: fixed;
      bottom: 24px;
      right: 24px;
      background-color: #25D366;
      color: #ffffff;
      padding: 12px 20px;
      border-radius: 50px;
      display: flex;
      align-items: center;
      gap: 10px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
      font-weight: 600;
      z-index: 999;
      transition: transform 0.3s ease;
    }

    .whatsapp-float:hover {
      transform: scale(1.05);
    }

    /* ==========================================================================
       9. FOOTER
       ========================================================================== */
    .footer {
      background-color: #1A2E1B;
      color: #E0E0E0;
      padding: 60px 0 20px 0;
    }

    .footer-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 32px;
      margin-bottom: 40px;
    }

    .footer-col h4 {
      font-family: var(--font-heading);
      color: #ffffff;
      margin-bottom: 16px;
    }

    .footer-col p, .footer-col a {
      color: #B0BEC5;
      font-size: 0.95rem;
      margin-bottom: 8px;
      display: block;
    }

    .footer-bottom {
      border-top: 1px solid rgba(255, 255, 255, 0.1);
      padding-top: 20px;
      text-align: center;
      font-size: 0.9rem;
      color: #81C784;
    }

    /* ==========================================================================
       10. RESPONSIVE DESIGN (MOBILE ADAPTATION)
       ========================================================================== */
    @media (max-width: 768px) {
      .hero-wrapper,
      .contact-wrapper {
        grid-template-columns: 1fr;
      }

      .hero-content h1 {
        font-size: 2.1rem;
      }

      .nav-links {
        display: none; /* Can be expanded into a mobile menu drawer */
      }

      .section-padding {
        padding: 50px 0;
      }
    }
  </style>
</head>
<body>

  <!-- HEADER / NAVIGATION -->
  <header class="header">
    <div class="container nav-container">
      <a href="#" class="logo">V <span>UNIT</span></a>
      <nav>
        <ul class="nav-links">
          <li><a href="#about">About</a></li>
          <li><a href="#services">Services</a></li>
          <li><a href="#products">Products</a></li>
          <li><a href="#demo">Free Demo</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
      <a href="#demo" class="btn btn-primary" style="padding: 8px 18px; font-size: 0.9rem;">Book Demo</a>
    </div>
  </header>

  <!-- HERO SECTION -->
  <section class="hero">
    <div class="container hero-wrapper">
      <div class="hero-content">
        <h1>Fresh Vegetables Delivered Directly To Your Doorstep</h1>
        <p>V Unit makes fresh vegetable booking seamless, affordable, and quick. Experience effortless ordering with our dedicated application platform.</p>
        <div class="hero-buttons">
          <a href="#demo" class="btn btn-primary">Book Free Demo</a>
          <a href="https://wa.me/916305682369?text=Hi%20V%20Unit,%20I%20want%20to%20know%20more%20about%20your%20app" target="_blank" class="btn btn-secondary">WhatsApp Us</a>
        </div>
      </div>
      <div class="hero-card">
        <h3>V Unit Mobile App</h3>
        <p style="color: var(--text-muted); margin-bottom: 20px;">Book farm-fresh produce with just a few taps on your smartphone.</p>
        <a href="#contact" class="btn btn-primary" style="width: 100%;">Get Early Access</a>
      </div>
    </div>
  </section>

  <!-- ABOUT SECTION -->
  <section id="about" class="section-padding">
    <div class="container">
      <h2 class="section-title">About V Unit</h2>
      <p class="section-subtitle">Bridging the gap between local fresh supply and your daily kitchen needs.</p>
      
      <div class="about-grid">
        <div class="about-card">
          <h3>Our Mission</h3>
          <p>To provide local communities in Secunderabad and Hyderabad with clean, fresh, and handpicked daily vegetables effortlessly through technology.</p>
        </div>
        <div class="about-card">
          <h3>Quality Promise</h3>
          <p>Every order booked through the V Unit app undergoes strict quality checks before dispatch to ensure 100% farm freshness.</p>
        </div>
        <div class="about-card">
          <h3>Fast Delivery</h3>
          <p>Located strategically in Bowenpally, we optimize delivery routes for rapid fulfillment across Anjaiah Nagar and neighboring regions.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- SERVICES SECTION -->
  <section id="services" class="section-padding services">
    <div class="container">
      <h2 class="section-title">What We Offer</h2>
      <p class="section-subtitle">Designed to simplify your daily and weekly produce shopping.</p>
      
      <div class="services-grid">
        <div class="service-box">
          <div class="service-icon">📱</div>
          <h3>Easy App Booking</h3>
          <p>Browse, select, and order fresh vegetables using an intuitive interface designed for all age groups.</p>
        </div>
        <div class="service-box">
          <div class="service-icon">🧺</div>
          <h3>Custom Vegetable Bundles</h3>
          <p>Choose individual items or pick pre-curated weekly family baskets tailored to your kitchen budget.</p>
        </div>
        <div class="service-box">
          <div class="service-icon">🚚</div>
          <h3>Scheduled Delivery</h3>
          <p>Select your preferred delivery time slot and receive doorstep delivery right when you need it.</p>
        </div>
        <div class="service-box">
          <div class="service-icon">💬</div>
          <h3>Instant Support</h3>
          <p>Direct WhatsApp integration for immediate query resolution, order tracking, and support.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- PRODUCTS SECTION -->
  <section id="products" class="section-padding">
    <div class="container">
      <h2 class="section-title">Fresh Categories</h2>
      <p class="section-subtitle">A glimpse of the produce available for booking on our app.</p>
      
      <div class="product-grid">
        <div class="product-card">
          <div class="product-emoji">🥬</div>
          <h4>Leafy Greens</h4>
          <p>Spinach, Coriander, Mint, and Fresh Herbs</p>
        </div>
        <div class="product-card">
          <div class="product-emoji">🍅</div>
          <h4>Daily Staples</h4>
          <p>Tomatoes, Potatoes, Onions, and Garlic</p>
        </div>
        <div class="product-card">
          <div class="product-emoji">🥕</div>
          <h4>Root Vegetables</h4>
          <p>Carrots, Beetroot, Radish, and Sweet Potatoes</p>
        </div>
        <div class="product-card">
          <div class="product-emoji">🥦</div>
          <h4>Exotic Vegetables</h4>
          <p>Broccoli, Bell Peppers, Zucchini, and Mushrooms</p>
        </div>
      </div>
    </div>
  </section>

  <!-- CONTACT & FREE DEMO SECTION -->
  <section id="contact" class="section-padding contact-section">
    <div class="container">
      <h2 class="section-title">Book a Free Demo / Contact Us</h2>
      <p class="section-subtitle">Send us a message and receive response directly in your inbox.</p>
      
      <div class="contact-wrapper">
        <!-- Contact Information -->
        <div class="contact-info">
          <h3>Get In Touch</h3>
          <p>Interested in trying out the V Unit app or booking a demonstration? Reach out to us through any of the channels below.</p>
          
          <div class="info-item">
            <div class="info-icon">📍</div>
            <div>
              <strong>Address:</strong>
              <p>Bowenpally, Anjaiah Nagar, Secunderabad, Hyderabad, Telangana</p>
            </div>
          </div>
          
          <div class="info-item">
            <div class="info-icon">📞</div>
            <div>
              <strong>Phone / Call:</strong>
              <p><a href="tel:6305682369">+91 63056 82369</a></p>
            </div>
          </div>
          
          <div class="info-item">
            <div class="info-icon">✉️</div>
            <div>
              <strong>Email Us:</strong>
              <p><a href="mailto:Vishnuvaddevishnu63@gmail.com">Vishnuvaddevishnu63@gmail.com</a></p>
            </div>
          </div>

          <div class="info-item">
            <div class="info-icon">💬</div>
            <div>
              <strong>WhatsApp:</strong>
              <p><a href="https://wa.me/916305682369" target="_blank">+91 63056 82369</a></p>
            </div>
          </div>
        </div>

        <!-- Form Submission via Web3Forms -->
        <div class="form-container" id="demo">
          <h3>Request a Free Demo</h3>
          <p style="margin-bottom: 20px; font-size: 0.9rem; color: var(--text-muted);">Fill out this form to schedule an app walkthrough or place an inquiry.</p>
          
          <!-- Web3Forms Form Integration -->
          <form action="https://api.web3forms.com/submit" method="POST">
            <!-- Web3Forms Access Key Replace Placeholder -->
            <input type="hidden" name="access_key" value="YOUR-WEB3FORM-KEY-HERE">
            <input type="hidden" name="subject" value="New Demo Booking Request - V Unit App">
            <input type="hidden" name="from_name" value="V Unit App Website">

            <div class="form-group">
              <label for="name">Full Name</label>
              <input type="text" id="name" name="name" placeholder="Enter your name" required>
            </div>

            <div class="form-group">
              <label for="phone">Phone Number</label>
              <input type="tel" id="phone" name="phone" placeholder="Enter mobile number" required>
            </div>

            <div class="form-group">
              <label for="email">Email Address</label>
              <input type="email" id="email" name="email" placeholder="Enter your email" required>
            </div>

            <div class="form-group">
              <label for="request_type">Request Type</label>
              <select id="request_type" name="request_type">
                <option value="Free Demo Booking">Free Demo Booking</option>
                <option value="General Inquiry">General Inquiry</option>
                <option value="Bulk Order Inquiry">Bulk Order Inquiry</option>
              </select>
            </div>

            <div class="form-group">
              <label for="message">Long Message / Inquiry Details</label>
              <textarea id="message" name="message" placeholder="Write your long message, requirement, or questions here..." required></textarea>
            </div>

            <button type="submit" class="btn btn-primary" style="width: 100%;">Submit Request</button>
          </form>
        </div>
      </div>
    </div>
  </section>

  <!-- FLOATING WHATSAPP BUTTON -->
  <a href="https://wa.me/916305682369?text=Hello%20V%20Unit,%20I%20am%20interested%20in%20your%20vegetable%20booking%20app." 
     class="whatsapp-float" 
     target="_blank" 
     aria-label="Chat on WhatsApp">
     <span>💬</span> WhatsApp
  </a>

  <!-- FOOTER -->
  <footer class="footer">
    <div class="container">
      <div class="footer-grid">
        <div class="footer-col">
          <h4>V Unit App</h4>
          <p>Your trusted vegetable booking platform delivering fresh produce across Bowenpally, Anjaiah Nagar, Secunderabad, and Hyderabad.</p>
        </div>
        <div class="footer-col">
          <h4>Quick Links</h4>
          <a href="#about">About Us</a>
          <a href="#services">Our Services</a>
          <a href="#products">Fresh Categories</a>
          <a href="#demo">Book Demo</a>
        </div>
        <div class="footer-col">
          <h4>Contact Info</h4>
          <p>📍 Bowenpally, Anjaiah Nagar, Secunderabad, Hyderabad</p>
          <p>📞 +91 63056 82369</p>
          <p>✉️ Vishnuvaddevishnu63@gmail.com</p>
        </div>
      </div>
      <div class="footer-bottom">
        <p>&copy; 2026 V Unit Vegetable Booking App. All rights reserved.</p>
      </div>
    </div>
  </footer>

</body>
</html>
