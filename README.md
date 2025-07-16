<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="description" content="Official website of Alif Hossain - Student and Programmer">
  <title>alifhossain.rain - Official Website</title>
  <style>
    /* Reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      line-height: 1.6;
      background-color: #f5f7fa;
      color: #333;
    }
    a {
      text-decoration: none;
      color: #0077cc;
      transition: color 0.3s ease;
    }
    a:hover {
      color: #005fa3;
    }
    /* Container */
    .container {
      max-width: 1100px;
      margin: 0 auto;
      padding: 0 20px;
    }
    /* Header */
    header {
      background-color: #004d99;
      color: white;
      padding: 15px 0;
      position: sticky;
      top: 0;
      z-index: 1000;
      box-shadow: 0 2px 6px rgba(0,0,0,0.2);
    }
    header .container {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .logo {
      font-size: 1.8rem;
      font-weight: bold;
      letter-spacing: 2px;
      cursor: pointer;
    }
    nav ul {
      list-style: none;
      display: flex;
      gap: 25px;
    }
    nav ul li {
      font-weight: 600;
    }
    nav ul li a {
      color: white;
      padding: 6px 10px;
      border-radius: 4px;
      display: block;
    }
    nav ul li a:hover,
    nav ul li a.active {
      background-color: #003366;
    }
    /* Hero */
    .hero {
      background: linear-gradient(rgba(0, 77, 153, 0.7), rgba(0, 51, 102, 0.7)), 
                  url('https://images.unsplash.com/photo-1504384308090-c894fdcc538d?auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
      height: 70vh;
      color: white;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 0 20px;
      flex-direction: column;
    }
    .hero h1 {
      font-size: clamp(2rem, 5vw, 3.5rem);
      margin-bottom: 15px;
      max-width: 700px;
    }
    .hero p {
      font-size: clamp(1rem, 2vw, 1.3rem);
      margin-bottom: 30px;
      max-width: 600px;
    }
    .btn-primary {
      background-color: #ffd700;
      color: #222;
      padding: 15px 35px;
      font-weight: 700;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      text-transform: uppercase;
      transition: all 0.3s ease;
    }
    .btn-primary:hover {
      background-color: #e6c200;
      transform: translateY(-3px);
      box-shadow: 0 5px 15px rgba(0,0,0,0.2);
    }
    /* Sections */
    section {
      padding: 60px 0;
      scroll-margin-top: 80px;
    }
    h2.section-title {
      text-align: center;
      color: #004d99;
      margin-bottom: 40px;
      font-size: clamp(1.8rem, 4vw, 2.5rem);
    }
    /* About */
    #about .content {
      max-width: 800px;
      margin: 0 auto;
      font-size: 1.1rem;
      color: #444;
      text-align: center;
    }
    /* Services */
    #services .services-list {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 30px;
      max-width: 1000px;
      margin: 0 auto;
    }
    .service-card {
      background: white;
      padding: 25px 20px;
      border-radius: 8px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      text-align: center;
      transition: all 0.3s ease;
    }
    .service-card:hover {
      transform: translateY(-10px);
      box-shadow: 0 10px 25px rgba(0,0,0,0.15);
    }
    .service-card h3 {
      color: #004d99;
      margin-bottom: 15px;
    }
    .service-card p {
      color: #555;
      font-size: 1rem;
      line-height: 1.4;
    }
    /* Portfolio */
    #portfolio .portfolio-list {
      max-width: 1100px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 30px;
      padding: 0 20px;
    }
    .portfolio-item {
      background: white;
      border-radius: 10px;
      overflow: hidden;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      transition: all 0.3s ease;
      cursor: pointer;
      display: flex;
      flex-direction: column;
    }
    .portfolio-item:hover {
      transform: translateY(-10px);
      box-shadow: 0 10px 25px rgba(0,0,0,0.15);
    }
    .portfolio-img {
      width: 100%;
      height: 180px;
      object-fit: cover;
      transition: transform 0.5s ease;
    }
    .portfolio-item:hover .portfolio-img {
      transform: scale(1.05);
    }
    .portfolio-info {
      padding: 15px;
      flex-grow: 1;
    }
    .portfolio-info h4 {
      margin-bottom: 10px;
      color: #004d99;
    }
    .portfolio-info p {
      color: #555;
      font-size: 0.95rem;
    }
    /* Contact */
    #contact .contact-form {
      max-width: 600px;
      margin: 0 auto;
    }
    #contact form {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
    #contact input, #contact textarea {
      padding: 15px;
      font-size: 1rem;
      border: 1.5px solid #ccc;
      border-radius: 6px;
      resize: vertical;
      transition: all 0.3s ease;
    }
    #contact input:focus, #contact textarea:focus {
      outline: none;
      border-color: #004d99;
      box-shadow: 0 0 0 3px rgba(0, 77, 153, 0.2);
    }
    #contact button {
      background-color: #004d99;
      color: white;
      padding: 15px;
      font-size: 1.1rem;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      transition: all 0.3s ease;
      text-transform: uppercase;
      font-weight: 700;
    }
    #contact button:hover {
      background-color: #003366;
      transform: translateY(-3px);
      box-shadow: 0 5px 15px rgba(0,0,0,0.2);
    }
    /* Footer */
    footer {
      background-color: #222;
      color: #bbb;
      text-align: center;
      padding: 30px 10px;
      font-size: 0.9rem;
    }
    .social-links {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-top: 20px;
    }
    .social-links a {
      color: #bbb;
      font-size: 1.5rem;
      transition: color 0.3s ease;
    }
    .social-links a:hover {
      color: #ffd700;
    }
    /* Responsive */
    @media (max-width: 768px) {
      header .container {
        flex-direction: column;
        gap: 15px;
      }
      nav ul {
        gap: 15px;
        flex-wrap: wrap;
        justify-content: center;
      }
      .hero {
        height: 60vh;
      }
      section {
        padding: 40px 0;
      }
    }
  </style>
</head>
<body>

  <header>
    <div class="container">
      <div class="logo">alifhossain.rain</div>
      <nav>
        <ul>
          <li><a href="#home" class="active">Home</a></li>
          <li><a href="#about">About</a></li>
          <li><a href="#services">Services</a></li>
          <li><a href="#portfolio">Portfolio</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <section class="hero" id="home">
    <div class="container">
      <h1>Welcome to alifhossain.rain</h1>
      <p>Your official website for professional projects and services.</p>
      <button class="btn-primary" onclick="document.getElementById('contact').scrollIntoView({behavior:'smooth'})">Get in Touch</button>
    </div>
  </section>

  <section id="about">
    <h2 class="section-title">About Me</h2>
    <div class="content container">
      <p>
        Hello! I'm Alif Hossain, a passionate student and programmer dedicated to crafting clean and efficient solutions. I love learning new technologies and delivering projects that make a difference. With a strong foundation in computer science and hands-on experience in various programming languages, I strive to create meaningful digital experiences.
      </p>
    </div>
  </section>

  <section id="services">
    <h2 class="section-title">Services</h2>
    <div class="services-list container">
      <div class="service-card">
        <h3>Web Development</h3>
        <p>Building responsive, user-friendly websites with modern technologies like HTML5, CSS3, JavaScript, and popular frameworks.</p>
      </div>
      <div class="service-card">
        <h3>Programming Projects</h3>
        <p>Developing customized software solutions tailored to your specific needs using Python, Java, and other programming languages.</p>
      </div>
      <div class="service-card">
        <h3>Technical Consulting</h3>
        <p>Helping you choose the right tools, technologies, and strategies for your digital projects and business success.</p>
      </div>
    </div>
  </section>

  <section id="portfolio">
    <h2 class="section-title">Portfolio</h2>
    <div class="portfolio-list">
      <div class="portfolio-item">
        <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Task Management App" class="portfolio-img" />
        <div class="portfolio-info">
          <h4>Task Management App</h4>
          <p>A web application for managing tasks efficiently with modern UI and real-time updates.</p>
        </div>
      </div>
      <div class="portfolio-item">
        <img src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Business Automation" class="portfolio-img" />
        <div class="portfolio-info">
          <h4>Business Automation</h4>
          <p>Custom software solution for automating business processes and increasing productivity.</p>
        </div>
      </div>
      <div class="portfolio-item">
        <img src="https://images.unsplash.com/photo-1512941937669-90a1b58e7e9c?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Responsive Website" class="portfolio-img" />
        <div class="portfolio-info">
          <h4>Responsive Website</h4>
          <p>A mobile-friendly website optimized for performance, accessibility, and user experience.</p>
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
