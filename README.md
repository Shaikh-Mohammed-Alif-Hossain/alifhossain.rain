<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>alifhossain.rain - Official Website</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" />
  <style>
    /* Reset & Base Styles */
    * { margin: 0; padding: 0; box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      font-family: 'Segoe UI', Roboto, sans-serif;
      line-height: 1.6;
      background-color: #f5f7fa;
      color: #333;
    }
    a { text-decoration: none; transition: 0.3s ease; }

    /* Header */
    header {
      background-color: #004d99;
      color: white;
      padding: 15px 0;
      position: fixed;
      width: 100%;
      top: 0;
      z-index: 1000;
      box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    }
    header .container {
      display: flex;
      justify-content: space-between;
      align-items: center;
      max-width: 1100px;
      margin: 0 auto;
      padding: 0 20px;
    }
    .logo { font-size: 1.6rem; font-weight: bold; letter-spacing: 1px; }
    nav ul { list-style: none; display: flex; gap: 15px; align-items: center; }
    nav ul li a {
      color: rgba(255,255,255,0.8);
      padding: 8px 12px;
      border-radius: 4px;
      font-size: 0.95rem;
    }
    nav ul li a:hover, nav ul li a.active {
      color: white;
      background-color: rgba(255,255,255,0.1);
    }

    /* Facebook Menu Icon Style */
    .nav-fb { color: #1877F2 !important; font-size: 1.2rem; }

    /* Hero Section */
    .hero {
      background: linear-gradient(rgba(0, 77, 153, 0.8), rgba(0, 77, 153, 0.8)), 
                  url('https://images.unsplash.com/photo-1504384308090-c894fdcc538d?auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
      height: 100vh;
      color: white;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding-top: 60px;
    }
    .hero-content h1 { font-size: 3.5rem; margin-bottom: 10px; }
    .hero-content p { font-size: 1.2rem; margin-bottom: 30px; opacity: 0.9; }
    
    .btn-group { display: flex; gap: 15px; justify-content: center; flex-wrap: wrap; }
    
    .btn-main {
      background: #ffd700;
      color: #222;
      padding: 12px 30px;
      border-radius: 30px;
      font-weight: bold;
      display: inline-block;
    }
    .btn-fb {
      background: #1877F2;
      color: white;
      padding: 12px 30px;
      border-radius: 30px;
      font-weight: bold;
      display: inline-flex;
      align-items: center;
      gap: 8px;
    }
    .btn-fb:hover { background: #166fe5; transform: translateY(-3px); }

    /* Section Styles */
    section { padding: 100px 20px 60px; max-width: 1100px; margin: 0 auto; }
    .section-title { text-align: center; color: #004d99; margin-bottom: 50px; font-size: 2.2rem; }

    /* Contact Form */
    .contact-form { max-width: 600px; margin: 0 auto; background: white; padding: 30px; border-radius: 15px; box-shadow: 0 10px 30px rgba(0,0,0,0.05); }
    input, textarea { width: 100%; padding: 12px; margin-bottom: 15px; border: 1px solid #ddd; border-radius: 8px; font-family: inherit; }
    .btn-submit { background: #004d99; color: white; border: none; padding: 12px; border-radius: 8px; cursor: pointer; width: 100%; font-weight: bold; }

    footer { background: #1a1a1a; color: #999; padding: 30px; text-align: center; }

    @media (max-width: 768px) {
      .hero-content h1 { font-size: 2.5rem; }
      nav ul { display: none; }
    }
  </style>
</head>
<body>

  <header>
    <div class="container">
      <div class="logo">alifhossain.rain</div>
      <nav>
        <ul>
          <li><a href="#home">Home</a></li>
          <li><a href="#about">About</a></li>
          <li><a href="#services">Services</a></li>
          <li><a href="#portfolio">Portfolio</a></li>
          <li><a href="#contact">Contact</a></li>
          <li><a href="https://www.facebook.com/share/16A8t2QkpF/" target="_blank" class="nav-fb"><i class="fab fa-facebook"></i></a></li>
        </ul>
      </nav>
    </div>
  </header>

  <section class="hero" id="home">
    <div class="hero-content">
      <h1>Hi, I'm Alif Hossain</h1>
      <p>Student & Programmer | Problem Solver | Tech Enthusiast</p>
      
      <div class="btn-group">
        <a href="#contact" class="btn-main">Get in Touch</a>
        <a href="https://www.facebook.com/share/16A8t2QkpF/" target="_blank" class="btn-fb">
          <i class="fab fa-facebook-f"></i> Facebook Profile
        </a>
      </div>
    </div>
  </section>

  <section id="about">
    <h2 class="section-title">About Me</h2>
    <div style="text-align: center; max-width: 800px; margin: 0 auto;">
      <p>I am a dedicated student and programmer with a passion for creating digital solutions. I enjoy learning new frameworks and building projects that help people.</p>
    </div>
  </section>

  <section id="contact">
    <h2 class="section-title">Message Me</h2>
    <div class="contact-form">
      <form action="https://formspree.io/f/mqkwazpl" method="POST">
        <input type="text" name="name" placeholder="Name" required />
        <input type="email" name="email" placeholder="Email" required />
        <textarea name="message" rows="5" placeholder="Your Message" required></textarea>
        <button type="submit" class="btn-submit">Send Message</button>
      </form>
    </div>
  </section>

  <footer>
    <p>&copy; 2026 alifhossain.rain. All rights reserved.</p>
    <div style="margin-top: 10px;">
        <a href="https://www.facebook.com/share/16A8t2QkpF/" target="_blank" style="color: #999; font-size: 1.5rem;"><i class="fab fa-facebook"></i></a>
    </div>
  </footer>

</body>
</html>ce, accessibility, and user experience.</p>
        </div>
      </div>
    </div>
  </section>

  <section id="contact">
    <h2 class="section-title">Contact Me</h2>
    <div class="contact-form container">
      <form action="https://formspree.io/f/mqkwazpl" method="POST">
        <input type="text" name="name" placeholder="Your Name" required />
        <input type="email" name="_replyto" placeholder="Your Email" required />
        <textarea name="message" rows="6" placeholder="Your Message" required></textarea>
        <button type="submit">Send Message</button>
      </form>
    </div>
  </section>

  <footer>
    <div class="container">
      <p>&copy; 2025 alifhossain.rain. All rights reserved.</p>
      <div class="social-links">
        <a href="#" aria-label="GitHub"><i class="fab fa-github"></i></a>
        <a href="#" aria-label="LinkedIn"><i class="fab fa-linkedin"></i></a>
        <a href="#" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
      </div>
    </div>
  </footer>

  <!-- Font Awesome for icons -->
  <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
  
  <!-- Smooth scrolling for anchor links -->
  <script>
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        e.preventDefault();
        document.querySelector(this.getAttribute('href')).scrollIntoView({
          behavior: 'smooth'
        });
        
        // Update active class
        document.querySelectorAll('nav ul li a').forEach(link => {
          link.classList.remove('active');
        });
        this.classList.add('active');
      });
    });
  </script>
</body>
</html>
