
web development project about portfolio and representing my self in that
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Charan's Portfolio</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;800&display=swap" rel="stylesheet">

  <!-- Font Awesome for Contact Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" crossorigin="anonymous" referrerpolicy="no-referrer" />

  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: "Poppins", sans-serif;
      overflow-x: hidden;
      background: linear-gradient(to right, #2c5364, #203a43, #0f2027);
      color: #fff;
      transition: background 0.5s, color 0.5s;
    }

    #particles-js {
      position: fixed;
      width: 100%;
      height: 100%;
      z-index: -1;
      top: 0;
      left: 0;
    }

    nav {
      position: sticky;
      top: 0;
      background: rgba(0,0,0,0.6);
      backdrop-filter: blur(6px);
      display: flex;
      justify-content: center;
      padding: 15px;
      z-index: 10;
    }
    nav a {
      color: #fff;
      text-decoration: none;
      margin: 0 20px;
      font-weight: 600;
      position: relative;
    }
    nav a::after {
      content: "";
      position: absolute;
      bottom: -5px;
      left: 0;
      width: 0;
      height: 3px;
      background: #1abc9c;
      transition: width 0.3s;
    }
    nav a:hover::after { width: 100%; }

    .hero {
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
    }

    .hero img {
      width: 180px;
      height: 180px;
      border-radius: 50%;
      border: 4px solid #1abc9c;
      object-fit: cover;
      margin-bottom: 20px;
      box-shadow: 0 8px 25px rgba(0,0,0,0.5);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
    .hero img:hover {
      transform: scale(1.08);
      box-shadow: 0 12px 30px rgba(0,0,0,0.7);
    }

    .hero h1 {
      font-size: 3rem;
      font-weight: 800;
      margin-bottom: 15px;
    }
    .typing {
      color: #1abc9c;
      font-weight: bold;
      border-right: 3px solid #1abc9c;
      animation: blink 0.7s infinite;
    }
    @keyframes blink { 50% { border-color: transparent; } }

    section { padding: 60px 10%; }
    h2 {
      font-size: 2rem;
      margin-bottom: 20px;
      text-align: center;
    }

    .card {
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(10px);
      border-radius: 15px;
      padding: 20px;
      margin: 20px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.3);
      transition: transform 0.3s;
    }
    .card:hover { transform: translateY(-10px) scale(1.02); }

    .projects, .certifications {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
    }

    footer {
      text-align: center;
      padding: 20px;
      background: rgba(0,0,0,0.7);
      margin-top: 40px;
    }
    footer a { color: #1abc9c; text-decoration: none; }

    .dark { background: #fdfdfd; color: #222; }
    .dark nav { background: rgba(255,255,255,0.8); }
    .dark nav a { color: #222; }
    .dark footer { background: #ddd; }

    /* About Section Photo */
    .about-card {
      display: flex;
      align-items: center;
      gap: 20px;
      flex-wrap: wrap;
    }
    .about-pic {
      width: 150px;
      height: 150px;
      border-radius: 50%;
      border: 3px solid #1abc9c;
      object-fit: cover;
      box-shadow: 0 8px 20px rgba(0,0,0,0.4);
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .about-pic:hover {
      transform: scale(1.05);
      box-shadow: 0 12px 25px rgba(0,0,0,0.6);
    }
    .about-card p {
      flex: 1;
      font-size: 1.05rem;
      line-height: 1.6;
    }

    /* Contact Buttons with Logos */
    .contact-card {
      display: flex;
      justify-content: center;
      gap: 30px;
      margin-top: 20px;
    }

    .contact-btn {
      width: 60px;
      height: 60px;
      background: #1abc9c;
      display: flex;
      justify-content: center;
      align-items: center;
      border-radius: 50%;
      color: #fff;
      font-size: 1.5rem;
      transition: transform 0.3s, box-shadow 0.3s, background 0.3s;
      text-decoration: none;
    }

    .contact-btn:hover {
      transform: scale(1.2);
      box-shadow: #1abc9c;
      background: #16a085;
    }
  </style>
</head>
<body>

  <div id="particles-js"></div>

  <nav>
    <a href="#about">About</a>
    <a href="#skills">Skills</a>
    <a href="#certifications">Certifications</a>
    <a href="#projects">Projects</a>
    <a href="#contact">Contact</a>
    <a href="#" id="toggleMode">🌙</a>
  </nav>

  <!-- Hero Section -->
  <section class="hero">
    <img src="image copy 2.png" alt="Charan's Photo">
    <h1>Hi, I'm <span style="color:#1abc9c;">Charan</span></h1>
    <h2 class="typing"></h2>
  </section>

  <!-- About Me Section -->
  <section id="about">
    <h2>About Me</h2>
    <div class="card about-card">
      <img src="image copy 2.png" alt="Charan's Photo" class="about-pic">
      <p>
        Motivated Computer Science student with strong knowledge in Java, Python, and Web technologies.  
        Passionate about problem-solving, software development, and learning new technologies.
      </p>
    </div>
  </section>

  <!-- Skills Section -->
  <section id="skills">
    <h2>Skills</h2>
    <div class="card">
      <ul>
        <li>Java</li>
        <li>Python</li>
        <li>Web Development</li>
        <li>Data Structures</li>
      </ul>
    </div>
  </section>

  <!-- Certifications Section -->
  <section id="certifications">
    <h2>Certifications</h2>
    <div class="certifications">
      <div class="card"><b>Meta Data Analyst</b> — Coursera</div>
      <div class="card"><b>Data Science and Analytics</b> — HP Life</div>
      <div class="card"><b>Soft Skills</b> — TCS iON</div>
      <div class="card"><b>IT Prime Course</b> — TCS iON</div>
      <div class="card"><b>Introduction to AI Generative</b> — Microsoft</div>
      <div class="card"><b>Introduction to MS Excel</b> — Microsoft</div>
      <div class="card"><b>Step Programming</b> — Soft Skills</div>
    </div>
  </section>

  <!-- Projects Section -->
  <section id="projects">
    <h2>Projects</h2>
    <div class="projects">
      <div class="card">
        <h3>E-Sports Database</h3>
        <p>Efficiently stores, manages, and retrieves e-sports data.</p>
      </div>
      <div class="card">
        <h3>College Event Planner</h3>
        <p>Streamlines scheduling and organizing college events.</p>
      </div>
      <div class="card">
        <h3>IoT Smoke Detection</h3>
        <p>Real-time fire hazard detection using Cisco Packet Tracer.</p>
      </div>
    </div>
  </section>

  <!-- Contact Section with Logo Buttons -->
  <section id="contact">
    <h2>Contact</h2>
    <div class="card contact-card">
      <a href="mailto:charan.kotha18@gmail.com" class="contact-btn" title="Email"><i class="fas fa-envelope"></i></a>
      <a href="https://linkedin.com/in/charan-kotha-0b10652b9" target="_blank" class="contact-btn" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
      <a href="https://github.com/charan111-c" target="_blank" class="contact-btn" title="GitHub"><i class="fab fa-github"></i></a>
         <a href="tel:+91 9392679111" class="contact-btn" title="Phone"><i class="fas fa-phone"></i></a><span style="font-size: 25px;margin-top: 10px;">+91 9392679111</span>
    </div>
  </section>

  <footer>
    <p>© Charan 2025 | All Rights Reserved</p>
  </footer>

  
  <script src="https://cdn.jsdelivr.net/npm/particles.js"></script>
  <script>
  
    particlesJS("particles-js", {
      "particles": {
        "number": { "value": 80 },
        "size": { "value": 3 },
        "move": { "speed": 2 },
        "line_linked": { "enable": true, "color": "#1abc9c" },
        "color": { "value": "#1abc9c" }
      }
    });


    const texts = ["Web Developer", "Java Developer"];
    let i = 0, j = 0, currentText = "", isDeleting = false;
    function type() {
      const typingEl = document.querySelector(".typing");
      if (i < texts.length) {
        if (!isDeleting && j <= texts[i].length) { currentText = texts[i].substring(0, j++); }
        else if (isDeleting && j >= 0) { currentText = texts[i].substring(0, j--); }
        typingEl.textContent = currentText;
        if (j === texts[i].length + 1) { isDeleting = true; }
        else if (isDeleting && j === 0) { isDeleting = false; i++; }
        if (i === texts.length) i = 0;
      }
      setTimeout(type, isDeleting ? 100 : 200);
    }
    type();

    document.getElementById("toggleMode").addEventListener("click", function(e){
      e.preventDefault();
      document.body.classList.toggle("dark");
      this.textContent = document.body.classList.contains("dark") ? "☀️" : "🌙";
    });
  </script>
</body>
</html>
