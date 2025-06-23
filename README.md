<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Learnify - CodTech</title>
  <style>
    :root {
      --primary: #006699;
      --secondary: #f8f9fa;
      --accent: #ffc107;
      --dark: #1a1a1a;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      background: var(--secondary);
      color: var(--dark);
    }

    header {
      background: var(--primary);
      color: white;
      padding: 20px;
      text-align: center;
    }

    header h1 {
      font-size: 2em;
    }

    nav {
      margin-top: 10px;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin: 0 12px;
      font-weight: bold;
    }

    nav a:hover {
      text-decoration: underline;
    }

    .container {
      max-width: 1100px;
      margin: auto;
      padding: 30px 20px;
    }

    section {
      margin-bottom: 60px;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 25px;
    }

    .card {
      background: white;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.07);
      transition: transform 0.2s ease;
    }

    .card:hover {
      transform: translateY(-5px);
    }

    .card img {
      width: 100%;
      border-radius: 8px;
      margin-bottom: 12px;
    }

    .card h3 {
      margin-bottom: 10px;
    }

    .card button {
      background: var(--primary);
      border: none;
      color: white;
      padding: 10px 14px;
      border-radius: 6px;
      cursor: pointer;
    }

    .card button:hover {
      background: #004d66;
    }

    .video-container iframe {
      width: 100%;
      height: 420px;
      border: none;
      border-radius: 10px;
      margin-top: 20px;
    }

    .progress-item {
      background: white;
      padding: 20px;
      border-radius: 10px;
      margin-bottom: 20px;
    }

    .progress-label {
      margin-bottom: 10px;
      font-weight: bold;
    }

    .progress-bar {
      width: 100%;
      background: #ddd;
      height: 14px;
      border-radius: 20px;
      overflow: hidden;
    }

    .progress-fill {
      background: var(--accent);
      height: 100%;
      width: 0%;
      transition: width 0.8s;
    }

    footer {
      text-align: center;
      padding: 20px;
      background: var(--primary);
      color: white;
    }

    @media (max-width: 600px) {
      nav a {
        display: block;
        margin: 10px 0;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>Learnify - CodTech</h1>
    <nav>
      <a href="#courses">Courses</a>
      <a href="#player">Watch</a>
      <a href="#progress">Progress</a>
    </nav>
  </header>

  <div class="container">

    <!-- Courses Section -->
    <section id="courses">
      <h2 style="margin-bottom: 20px;">📚 Courses</h2>
      <div class="grid">
        <div class="card">
          <img src="https://via.placeholder.com/300x150?text=HTML+Course" alt="HTML">
          <h3>HTML & CSS Basics</h3>
          <p>Master the structure and style of web pages.</p>
          <button onclick="playCourse('HTML & CSS Basics', 'https://www.youtube.com/embed/UB1O30fR-EE', 80)">Watch</button>
        </div>
        <div class="card">
          <img src="https://via.placeholder.com/300x150?text=JavaScript" alt="JS">
          <h3>JavaScript Essentials</h3>
          <p>Bring your websites to life with dynamic content.</p>
          <button onclick="playCourse('JavaScript Essentials', 'https://www.youtube.com/embed/hdI2bqOjy3c', 60)">Watch</button>
        </div>
        <div class="card">
          <img src="https://via.placeholder.com/300x150?text=React+JS" alt="React">
          <h3>React JS Starter</h3>
          <p>Build modern interfaces using React framework.</p>
          <button onclick="playCourse('React JS Starter', 'https://www.youtube.com/embed/bMknfKXIFA8', 30)">Watch</button>
        </div>
      </div>
    </section>

    <!-- Video Player Section -->
    <section id="player">
      <h2 id="videoTitle">🎬 Course Player</h2>
      <div class="video-container">
        <iframe id="videoFrame" src="https://www.youtube.com/embed/UB1O30fR-EE" allowfullscreen></iframe>
      </div>
    </section>

    <!-- Progress Tracking -->
    <section id="progress">
      <h2>📈 Progress Dashboard</h2>

      <div class="progress-item">
        <div class="progress-label">HTML & CSS Basics</div>
        <div class="progress-bar"><div class="progress-fill" style="width: 80%;"></div></div>
      </div>

      <div class="progress-item">
        <div class="progress-label">JavaScript Essentials</div>
        <div class="progress-bar"><div class="progress-fill" style="width: 60%;"></div></div>
      </div>

      <div class="progress-item">
        <div class="progress-label">React JS Starter</div>
        <div class="progress-bar"><div class="progress-fill" style="width: 30%;"></div></div>
      </div>

    </section>

  </div>

  <footer>
    &copy; 2025 Learnify | Designed for CodTech Internship Task-4
  </footer>

  <script>
    function playCourse(title, videoUrl, progress) {
      document.getElementById('videoTitle').innerText = `🎬 Now Playing: ${title}`;
      document.getElementById('videoFrame').src = videoUrl;
      window.scrollTo({ top: document.getElementById("player").offsetTop, behavior: "smooth" });
    }
  </script>

</body>
</html>
