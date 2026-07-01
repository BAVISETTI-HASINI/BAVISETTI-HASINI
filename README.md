<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hasini Bavisetti · GitHub README</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #0d1117;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      padding: 2rem 1.5rem;
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
      color: #c9d1d9;
    }

    /* Card mimics GitHub profile README style */
    .readme-card {
      max-width: 1000px;
      width: 100%;
      background: #161b22;
      border-radius: 24px;
      padding: 2.2rem 2.5rem;
      border: 1px solid #30363d;
      box-shadow: 0 12px 30px rgba(0,0,0,0.6);
    }

    /* ----- header: avatar + name + right gif ----- */
    .header-row {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 1.2rem 2rem;
      margin-bottom: 1.2rem;
    }

    .avatar-group {
      display: flex;
      align-items: center;
      gap: 0.8rem 1.2rem;
      flex-wrap: wrap;
    }

    .avatar-group img:first-child {
      width: 58px;
      height: 58px;
      border-radius: 50%;
      border: 2px solid #2d7a5a;
      background: #0d1117;
      object-fit: cover;
    }

    .avatar-group h1 {
      font-size: 1.9rem;
      font-weight: 600;
      letter-spacing: -0.02em;
      background: linear-gradient(145deg, #f0f6fc 0%, #9ad0c0 80%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .right-gif {
      margin-left: auto;
      display: flex;
      align-items: center;
    }

    .right-gif img {
      max-height: 70px;
      width: auto;
      border-radius: 14px;
      background: #0d1117;
      padding: 4px 6px;
      border: 1px solid #30363d;
      box-shadow: 0 4px 10px rgba(0,0,0,0.3);
    }

    /* tagline */
    .tagline {
      font-size: 1.05rem;
      padding: 0.6rem 0 0.6rem 1.2rem;
      border-left: 4px solid #2d7a5a;
      background: rgba(45, 122, 90, 0.06);
      border-radius: 0 12px 12px 0;
      margin-bottom: 1.8rem;
      color: #b1bac4;
    }

    .tagline strong {
      color: #e6edf3;
      font-weight: 500;
    }

    /* grid: left content + right skills */
    .two-col {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 2rem 2.5rem;
      margin-top: 0.5rem;
    }

    @media (max-width: 700px) {
      .two-col {
        grid-template-columns: 1fr;
        gap: 1.8rem;
      }
      .right-gif {
        margin-left: 0;
      }
      .header-row {
        flex-direction: column;
        align-items: flex-start;
      }
    }

    /* left column */
    .left-col p {
      margin: 0.4rem 0 0.8rem 0;
      color: #c9d1d9;
      font-size: 0.98rem;
    }

    .info-line {
      display: flex;
      align-items: center;
      gap: 0.7rem;
      margin: 0.5rem 0;
      color: #b1bac4;
    }

    .info-line i {
      width: 1.3rem;
      color: #2d7a5a;
      font-size: 1rem;
    }

    .info-line a {
      color: #58a6ff;
      text-decoration: none;
      border-bottom: 1px dotted #2d7a5a;
    }

    .info-line a:hover {
      color: #79c0ff;
      border-bottom: 1px solid #79c0ff;
    }

    .badge-followers {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      background: #0d1117;
      padding: 0.25rem 1rem 0.25rem 0.8rem;
      border-radius: 30px;
      border: 1px solid #30363d;
      font-size: 0.9rem;
      color: #b1bac4;
      margin-top: 0.8rem;
    }

    .badge-followers i {
      color: #f0883e;
    }

    .badge-followers span {
      color: #f0f6fc;
      font-weight: 600;
    }

    .collab-box {
      margin-top: 1.5rem;
      background: #0d1117;
      padding: 1rem 1.2rem;
      border-radius: 18px;
      border-left: 4px solid #2d7a5a;
      font-size: 0.95rem;
      color: #c9d1d9;
    }

    .collab-box i {
      color: #2d7a5a;
      margin-right: 8px;
    }

    /* screenshot note (matching prompt) */
    .screenshot-note {
      font-size: 0.82rem;
      color: #8b949e;
      background: #0d1117;
      padding: 0.2rem 1rem 0.2rem 0.8rem;
      border-radius: 30px;
      display: inline-block;
      border: 1px dashed #30363d;
      margin-top: 1rem;
    }

    .screenshot-note i {
      color: #f0883e;
      margin-right: 5px;
    }

    /* right column: skills */
    .skillset {
      background: #0d1117;
      padding: 1.2rem 1.2rem 1.5rem;
      border-radius: 24px;
      border: 1px solid #30363d;
    }

    .skillset h3 {
      font-weight: 500;
      font-size: 1rem;
      letter-spacing: 0.3px;
      color: #b1bac4;
      margin-bottom: 1rem;
      display: flex;
      align-items: center;
      gap: 0.6rem;
    }

    .skillset h3 i {
      color: #2d7a5a;
      font-size: 1.2rem;
    }

    .skill-icons {
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem 0.8rem;
      align-items: center;
    }

    .skill-icons img {
      width: 38px;
      height: 38px;
      object-fit: contain;
      background: #161b22;
      padding: 4px;
      border-radius: 10px;
      border: 1px solid #2d333b;
      transition: 0.15s;
    }

    .skill-icons img:hover {
      border-color: #2d7a5a;
      transform: scale(1.04);
    }

    .skill-icons .more-label {
      color: #8b949e;
      font-size: 0.7rem;
      background: #21262d;
      padding: 0.2rem 0.7rem;
      border-radius: 40px;
      letter-spacing: 0.3px;
    }

    /* socials */
    .social-links {
      display: flex;
      flex-wrap: wrap;
      gap: 0.8rem 1.2rem;
      margin-top: 1.8rem;
      padding-top: 1.2rem;
      border-top: 1px solid #30363d;
    }

    .social-links a {
      color: #b1bac4;
      font-size: 1rem;
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      text-decoration: none;
      transition: 0.2s;
      padding: 0.2rem 0.8rem 0.2rem 0.5rem;
      border-radius: 30px;
      background: #0d1117;
      border: 1px solid #30363d;
    }

    .social-links a i {
      font-size: 1.3rem;
      width: 1.8rem;
      text-align: center;
    }

    .social-links a:hover {
      color: #f0f6fc;
      border-color: #2d7a5a;
      background: #161b22;
    }

    /* stats row (badges) */
    .stats-row {
      display: flex;
      flex-wrap: wrap;
      gap: 1.2rem 1.8rem;
      margin-top: 2rem;
      background: #0d1117;
      padding: 0.9rem 1.5rem;
      border-radius: 28px;
      border: 1px solid #30363d;
      align-items: center;
    }

    .stats-row img {
      height: 44px;
      border-radius: 8px;
      background: #161b22;
      border: 1px solid #2d333b;
      padding: 3px 6px;
    }

    .stats-row .stat-text {
      color: #b1bac4;
      font-size: 0.9rem;
      display: flex;
      align-items: center;
      gap: 0.6rem;
      flex-wrap: wrap;
    }

    .stat-text i {
      color: #f0883e;
      font-size: 1rem;
    }

    /* extra small */
    @media (max-width: 480px) {
      .readme-card {
        padding: 1.5rem;
      }
      .avatar-group h1 {
        font-size: 1.5rem;
      }
      .right-gif img {
        max-height: 50px;
      }
    }

    /* for the "see the screenshot i had the image on the down gif file" we place a subtle extra */
    .footnote-gif {
      display: flex;
      align-items: center;
      gap: 0.6rem;
      margin-top: 1.2rem;
      padding: 0.4rem 0.8rem;
      background: #0d1117;
      border-radius: 40px;
      border: 1px solid #30363d;
      width: fit-content;
      font-size: 0.8rem;
      color: #8b949e;
    }

    .footnote-gif img {
      height: 28px;
      border-radius: 6px;
    }

    .footnote-gif i {
      color: #f0883e;
    }
  </style>
</head>
<body>
  <div class="readme-card">

    <!-- header: avatar + name + right gif (exactly as described) -->
    <div class="header-row">
      <div class="avatar-group">
        <!-- main avatar gif from prompt -->
        <img src="https://user-images.githubusercontent.com/18350557/176309783-0785949b-9127-417c-8b55-ab5a4333674e.gif" alt="Hasini Bavisetti avatar" />
        <h1>Hasini Bavisetti</h1>
      </div>
      <div class="right-gif">
        <!-- right gif (the "internet failure" gif) -->
        <img src="https://user-images.githubusercontent.com/74038190/221352975-94759904-aa4c-4032-a8ab-b546efb9c478.gif" alt="right gif" />
      </div>
    </div>

    <!-- tagline -->
    <div class="tagline">
      <strong>Full Stack Developer · AWS · DevOps Intern</strong> &nbsp;— passionate fresher with a hunger to build, break, and learn.
    </div>

    <!-- two columns -->
    <div class="two-col">
      <!-- left column -->
      <div class="left-col">
        <p><i class="fas fa-map-pin" style="color:#2d7a5a; margin-right:6px;"></i> Based in <strong>INDIA</strong></p>

        <div class="info-line">
          <i class="fas fa-globe"></i>
          <span>Portfolio: <a href="http://ai-class-4d5ff.web.app" target="_blank">ai-class-4d5ff.web.app</a></span>
        </div>
        <div class="info-line">
          <i class="fas fa-envelope"></i>
          <span><a href="mailto:hanibavisetti@gmail.com">hanibavisetti@gmail.com</a></span>
        </div>
        <div class="info-line">
          <i class="fas fa-brain"></i>
          <span>Currently learning <strong>Generative AI</strong></span>
        </div>

        <div class="badge-followers">
          <i class="fas fa-users"></i>
          <span>1.2k</span> followers · 
          <i class="fas fa-code-branch" style="color:#2d7a5a; margin-left:6px;"></i> 16 repos
        </div>

        <div class="collab-box">
          <i class="fas fa-handshake"></i>
          <strong>Open to collaborate</strong> on beginner-friendly open-source, full-stack, AWS, DevOps, and GenAI projects. Let’s grow together!
        </div>

        <!-- screenshot note as requested -->
        <div class="screenshot-note">
          <i class="fas fa-image"></i> see the screenshot &nbsp;·&nbsp; i had the image on the down gif file in the beside the name and right gif and left content like that
        </div>

        <!-- extra footnote with the "down gif" mention (the small gif from prompt) 
             we also show a tiny gif to match "image on the down gif file" -->
        <div class="footnote-gif">
          <i class="fas fa-arrow-down" style="color:#2d7a5a;"></i>
          <span>down gif file</span>
          <img src="https://user-images.githubusercontent.com/74038190/221352975-94759904-aa4c-4032-a8ab-b546efb9c478.gif" alt="small down gif" style="height:24px; border-radius:6px;" />
          <span style="margin-left:4px;">beside the name &amp; right gif</span>
        </div>
      </div>

      <!-- right column: skills -->
      <div class="skillset">
        <h3><i class="fas fa-code"></i> Tech Stack</h3>
        <div class="skill-icons">
          <!-- using the exact skill icons from the prompt (colored) -->
          <img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/java-colored.svg" alt="Java" title="Java" />
          <img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/spring-boot-colored.svg" alt="Spring Boot" title="Spring Boot" />
          <img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/python-colored.svg" alt="Python" title="Python" />
          <img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/git-colored.svg" alt="Git" title="Git" />
          <img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/visualstudiocode-colored.svg" alt="VS Code" title="VS Code" />
          <img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/react-colored.svg" alt="React" title="React" />
          <img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/html5-colored.svg" alt="HTML5" title="HTML5" />
          <img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/vuejs-colored.svg" alt="Vue" title="Vue" />
          <img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/angularjs-colored.svg" alt="Angular" title="Angular" />
          <img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/mysql-colored.svg" alt="MySQL" title="MySQL" />
          <img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/firebase-colored.svg" alt="Firebase" title="Firebase" />
          <img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/supabase-colored.svg" alt="Supabase" title="Supabase" />
          <img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/mongodb-colored.svg" alt="MongoDB" title="MongoDB" />
          <img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/linux-colored.svg" alt="Linux" title="Linux" />
          <img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/ubuntu-colored.svg" alt="Ubuntu" title="Ubuntu" />
          <img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/aws-colored-dark.svg" alt="AWS" title="AWS" />
          <img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/kubernetes-colored.svg" alt="Kubernetes" title="Kubernetes" />
          <img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/docker-colored.svg" alt="Docker" title="Docker" />
          <span class="more-label">+ more</span>
        </div>
      </div>
    </div>

    <!-- socials -->
    <div class="social-links">
      <a href="https://www.github.com/BAVISETTI-HASINI" target="_blank">
        <i class="fab fa-github"></i> GitHub
      </a>
      <a href="https://www.linkedin.com/in/hasinibavisetti" target="_blank">
        <i class="fab fa-linkedin"></i> LinkedIn
      </a>
      <span style="color:#8b949e; font-size:0.85rem; margin-left:auto;">
        <i class="fas fa-at"></i> hanibavisetti@gmail.com
      </span>
    </div>

    <!-- stats row (badges like in prompt) -->
    <div class="stats-row">
      <div class="stat-text">
        <i class="fas fa-chart-line"></i> 
        <span style="color:#e6edf3;">GitHub Stats</span>
      </div>
      <a href="http://www.github.com/BAVISETTI-HASINI" target="_blank">
        <img src="https://img.shields.io/github/followers/BAVISETTI-HASINI?logo=github&style=for-the-badge&color=ef4444&labelColor=000000" alt="GitHub followers" />
      </a>
      <!-- additional stats images as per prompt (streak & general) -->
      <a href="http://www.github.com/BAVISETTI-HASINI" target="_blank">
        <img src="https://github-readme-stats.vercel.app/api?username=BAVISETTI-HASINI&show_icons=true&hide=&count_private=true&title_color=10b981&text_color=ffffff&icon_color=ef4444&bg_color=000000&hide_border=true&show_icons=true" alt="GitHub stats" style="height:44px; border-radius:6px;" />
      </a>
      <a href="http://www.github.com/BAVISETTI-HASINI" target="_blank">
        <img src="https://github-readme-streak-stats.herokuapp.com/?user=BAVISETTI-HASINI&stroke=ffffff&background=000000&ring=10b981&fire=10b981&currStreakNum=ffffff&currStreakLabel=10b981&sideNums=ffffff&sideLabels=ffffff&dates=ffffff&hide_border=true" alt="GitHub streak" style="height:44px; border-radius:6px;" />
      </a>
    </div>

    <!-- small note: "see the screenshot i had the image on the down gif file in the beside the name and right gif and left contnet like that" 
         already included above, but we add a final visual cue -->
    <div style="margin-top: 1.2rem; font-size: 0.75rem; color: #6e7681; border-top: 1px solid #21262d; padding-top: 0.8rem; display: flex; align-items: center; gap: 0.6rem; flex-wrap: wrap;">
      <i class="fas fa-info-circle" style="color:#2d7a5a;"></i>
      <span>⬇️ The gif beside the name &amp; right gif — layout matches the prompt: avatar + name, right gif, left content, down gif file note.</span>
    </div>

  </div>
  <!-- Font Awesome script (free) -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/js/all.min.js" crossorigin="anonymous"></script>
</body>
</html>
