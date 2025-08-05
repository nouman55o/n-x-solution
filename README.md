<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>N-X Solution</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      font-family: Arial, sans-serif;
      background-color: #f0f4f4;
      color: #333;
    }

    header {
      background-color: #ffffff;
      padding: 15px 40px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      position: sticky;
      top: 0;
      z-index: 999;
    }

    .logo {
      font-size: 24px;
      font-weight: bold;
      color: rgb(35, 1, 231);
    }

    nav a {
      color: rgb(35, 12, 240);
      text-decoration: none;
      margin-left: 20px;
      font-size: 16px;
      transition: color 0.3s ease;
    }

    nav a:hover {
      color: #000;
    }

    .hero {
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 300px;
      background: linear-gradient(90deg, #ffffff 60%, #ffffff 40%);
      padding: 0 40px;
    }

    .hero-text {
      font-size: 36px;
      font-weight: bold;
      animation: textPop 1.5s ease-out forwards;
    }

    .hero-image img {
      width: 220px;
      height: auto;
      animation: slideRight 1.2s ease-out forwards;
    }

    @keyframes textPop {
      0% {
        opacity: 0;
        transform: scale(0.8) translateY(20px);
      }
      100% {
        opacity: 1;
        transform: scale(1) translateY(0);
      }
    }

    @keyframes slideRight {
      0% {
        opacity: 0;
        transform: translateX(100px);
      }
      100% {
        opacity: 1;
        transform: translateX(0);
      }
    }

    section {
      padding: 60px 40px;
    }

    #about h2 {
      text-align: center;
      color: rgb(74, 49, 214);
      font-size: 32px;
      margin-bottom: 10px;
      animation: fadeIn 1.2s ease-in-out;
    }

    #services h2, #projects h2, #contact h2 {
      font-size: 28px;
      margin-bottom: 20px;
    }

    p {
      font-size: 16px;
      line-height: 1.6;
    }

    .service-list, .project-list {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 20px;
    }

    .service-item, .project-item {
      background-color: #ffffff;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      transition: transform 0.3s;
    }

    .service-item:hover, .project-item:hover {
      transform: translateY(-5px);
    }

    footer {
      text-align: center;
      padding: 20px;
      background-color: #1daa61;
      color: white;
    }

    @keyframes fadeIn {
      0% {
        opacity: 0;
        transform: translateY(15px);
      }
      100% {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @media (max-width: 768px) {
      .hero {
        flex-direction: column;
        text-align: center;
        height: auto;
        padding: 30px 20px;
      }

      .hero-image {
        margin-top: 20px;
      }

      .hero-image img {
        width: 150px;
      }

      header {
        flex-direction: column;
        align-items: flex-start;
      }

      nav {
        margin-top: 10px;
      }
    }
    .build-section {
  background: linear-gradient(to right, #3d06d4, #a65bfc);
  color: white;
  text-align: center;
  padding: 60px 20px;
  font-size: 32px;
  font-weight: bold;
  text-shadow: 0 0 8px rgba(255, 255, 255, 0.7);
}

.build-section .highlight {
  color: #ffa600;
  text-shadow: 0 0 10px rgba(221, 141, 50, 0.9);
}
.contact-section {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 40px;
  background: linear-gradient(135deg, #fefeff, #ffffff);
}

.contact-card {
  background: rgba(160, 78, 180, 0.87);
  border: 1px solid rgba(235, 153, 153, 0.15);
  backdrop-filter: blur(12px);
  padding: 40px;
  border-radius: 20px;
  box-shadow: 0 15px 35px rgba(206, 0, 0, 0.5);
  width: 100%;
  max-width: 500px;
  animation: fadeUp 1s ease;
}

.contact-card h2 {
  text-align: center;
  margin-bottom: 25px;
  font-size: 28px;
  color: #fff;
  letter-spacing: 1px;
}

.field {
  position: relative;
  margin-bottom: 25px;
}

.field input,
.field textarea {
  width: 100%;
  padding: 14px;
  border: none;
  border-radius: 10px;
  background: rgba(255, 255, 255, 0.1);
  color: #fff;
  font-size: 16px;
  outline: none;
  transition: all 0.3s ease;
}

.field input:focus,
.field textarea:focus {
  background: rgba(224, 28, 28, 0.15);
  box-shadow: 0 0 15px rgba(202, 2, 2, 0.4);
}

.field label {
  position: absolute;
  top: 14px;
  left: 15px;
  color: rgba(143, 56, 56, 0.7);
  pointer-events: none;
  transition: 0.3s ease;
}

.field input:focus + label,
.field input:valid + label,
.field textarea:focus + label,
.field textarea:valid + label {
  top: -8px;
  left: 12px;
  font-size: 12px;
  color: #06e2d0;
}

.btn-pro {
  width: 100%;
  padding: 14px;
  border: none;
  border-radius: 10px;
  font-size: 16px;
  color: #04f3fc;
  background: linear-gradient(45deg, #f8f8f8, #f3f3f3);
  cursor: pointer;
  box-shadow: 0 5px 20px rgba(255, 255, 255, 0.3);
  transition: 0.3s ease;
}

.btn-pro:hover {
  background: linear-gradient(45deg, #8a2be2, #6bffa9);
  transform: translateY(-2px);
}

/* Animation */
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}
.contact-card {
  background: linear-gradient(135deg, #8f8c8c, #f1f1f1); /* Light gradient */
  padding: 40px;
  border-radius: 20px;
  box-shadow: 0 15px 35px rgba(243, 240, 240, 0.2);
  width: 100%;
  max-width: 500px;
  animation: fadeUp 1s ease;
  color: #333; /* Dark text for light background */
}
.field input,
.field textarea {
  background: #f8f8f8;
  color: #333;
  border: 2px solid #000000;
}

.field label {
  color: #666;
}

.field input:focus + label,
.field textarea:focus + label {
  color: #8a2be2;
}
/* Header Section */
.site-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: linear-gradient(90deg, #1025e2, #ab51ce);
  padding: 15px 40px;
  position: sticky;
  top: 0;
  z-index: 1000;
  box-shadow: 0 4px 15px rgba(0,0,0,0.2);
}

.logo {
  font-size: 22px;
  font-weight: bold;
  color: #fff;
  letter-spacing: 1px;
}

.nav-menu {
  display: flex;
  gap: 15px;
}

.nav-btn {
  padding: 8px 18px;
  background: rgba(255, 255, 255, 0.15);
  color: #fff;
  text-decoration: none;
  border-radius: 25px;
  transition: 0.3s ease;
  font-size: 14px;
}

.nav-btn:hover {
  background: rgba(255, 255, 255, 0.3);
  transform: translateY(-2px);
}

/* Mobile Responsive */
@media (max-width: 768px) {
  .site-header {
    flex-direction: column;
    gap: 10px;
    padding: 15px;
  }
  .nav-menu {
    flex-wrap: wrap;
    justify-content: center;
  }
}
.hero-image {
  position: relative;
  display: inline-block;
}

.hero-image::before {
  content: "";
  position: absolute;
  top: 50%;
  left: 50%;
  width: 280px; /* size of circle */
  height: 280px;
  background: radial-gradient(circle, #e0e0ff, #a1a1ff);
  border-radius: 50%;
  transform: translate(-50%, -50%);
  z-index: -1; /* behind the image */
}

.hero-image img {
  width: 220px;
  height: auto;
  position: relative;
  z-index: 1;
}

  </style>
</head>
<body>

  <header class="site-header">
  <div class="logo">N‑X Solution</div>
  <nav class="nav-menu">
    <a href="#home" class="nav-btn">Home</a>
    <a href="#about" class="nav-btn">About</a>
    <a href="#projects" class="nav-btn">Projects</a>
    <a href="#contact" class="nav-btn">Contact</a>
  </nav>
</header>


  <section id="hero" class="hero">
    <div class="hero-text">Welcome to N-X Solution</div>
    <div class="hero-image">
      <img src="c:\Users\m\Downloads\hi.PNG" alt="Man Image" />
    </div>
  </section>

  <section id="about">
    <h2>  ✅About Me </h2>
    <p style="text-align:center;">We are a creative web design agency dedicated to transforming your online vision into digital success.</p>
  </section>

  <section id="services">
    <h2>Our Services</h2>
    <div class="service-list">
      <div class="service-item">vimage.pngimage.pngimage.png
        <h3>Web Design</h3>
        <p>Modern and responsive website design tailored to your brand.</p>
      </div>
      <div class="service-item">
        <h3>Development</h3>
        <p>Custom HTML/CSS/JavaScript development services.</p>
      </div>
      <div class="service-item">
        <h3>SEO & Marketing</h3>
        <p>Boost your visibility on search engines with expert SEO.</p>
      </div>
    </div>
  </section>

  <section id="projects">
    <h2>Our Projects</h2>
    <div class="project-list">
      <div class="project-item">
        <h4>Portfolio Site</h4>
        <p>Built a clean personal portfolio site for a freelancer.</p>
      </div>
      <div class="project-item">
        <h4>E-commerce Page</h4>
        <p>Designed product landing pages with checkout flow.</p>
      </div>
    </div>
  </section>
<section id="build" class="build-section">
  <h2>
    ✨ Let’s Build <br />
    Something <span class="highlight">Amazing </span> <br />
    Together!
  </h2>
<form action="https://formspree.io/f/mabcdxyz" method="POST">
  <div class="field">
    <input type="text" name="name" id="name" required>
    <label for="name">Full Name</label>
  </div>

  <div class="field">
    <input type="email" name="email" id="email" required>
    <label for="email">Email Address</label>
  </div>

  <div class="field">
    <textarea name="message" id="message" rows="5" required></textarea>
    <label for="message">Your Message</label>
  </div>

  <button type="submit" class="btn-pro">Send Message</button>
</form>



  <section id="contact">
    <h2>Contact Us</h2>
    <p>Email: noumanameen439@gmail.com<br>Phone: 03134690738</p>
  </section>


  <footer>
    &copy; 2025 N-X Solution. All rights reserved.
  </footer>

</body>
</html>

