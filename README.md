
<style>
  @import url('https://fonts.googleapis.com/css2?family=Syne:wght@400;500;700;800&family=JetBrains+Mono:wght@400;500&display=swap');

  * { box-sizing: border-box; margin: 0; padding: 0; }

  .profile-wrapper {
    font-family: 'Syne', sans-serif;
    max-width: 860px;
    margin: 0 auto;
    padding: 2rem 1rem;
    color: var(--color-text-primary);
  }

  .header-section {
    display: flex;
    align-items: center;
    gap: 2rem;
    margin-bottom: 2.5rem;
    padding: 2rem;
    background: var(--color-background-secondary);
    border-radius: var(--border-radius-lg);
    border: 0.5px solid var(--color-border-tertiary);
  }

  .avatar {
    width: 88px;
    height: 88px;
    border-radius: 50%;
    background: linear-gradient(135deg, #185FA5, #0C447C);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 28px;
    font-weight: 800;
    color: #E6F1FB;
    flex-shrink: 0;
  }

  .header-info h1 {
    font-size: 26px;
    font-weight: 800;
    letter-spacing: -0.5px;
    color: var(--color-text-primary);
    margin-bottom: 4px;
  }

  .header-info .handle {
    font-family: 'JetBrains Mono', monospace;
    font-size: 13px;
    color: var(--color-text-secondary);
    margin-bottom: 10px;
  }

  .badges-row {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
  }

  .badge {
    display: inline-flex;
    align-items: center;
    gap: 5px;
    padding: 4px 10px;
    border-radius: 20px;
    font-size: 12px;
    font-weight: 500;
    border: 0.5px solid var(--color-border-secondary);
    background: var(--color-background-primary);
    color: var(--color-text-secondary);
    text-decoration: none;
  }

  .badge-dot {
    width: 7px;
    height: 7px;
    border-radius: 50%;
  }

  .dot-blue { background: #378ADD; }
  .dot-teal { background: #1D9E75; }
  .dot-green { background: #639922; }

  .section-label {
    font-family: 'JetBrains Mono', monospace;
    font-size: 10px;
    font-weight: 500;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    color: var(--color-text-secondary);
    margin-bottom: 1rem;
    padding-left: 2px;
  }

  .about-card {
    padding: 1.5rem;
    background: var(--color-background-primary);
    border: 0.5px solid var(--color-border-tertiary);
    border-radius: var(--border-radius-lg);
    margin-bottom: 2rem;
  }

  .about-card p {
    font-size: 14px;
    line-height: 1.7;
    color: var(--color-text-secondary);
  }

  .about-card p span {
    color: var(--color-text-primary);
    font-weight: 500;
  }

  .stats-row {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 10px;
    margin-bottom: 2rem;
  }

  .stat-card {
    padding: 1rem;
    background: var(--color-background-secondary);
    border-radius: var(--border-radius-md);
    border: 0.5px solid var(--color-border-tertiary);
    text-align: center;
  }

  .stat-card .stat-val {
    font-size: 20px;
    font-weight: 800;
    color: var(--color-text-primary);
  }

  .stat-card .stat-lbl {
    font-size: 11px;
    color: var(--color-text-secondary);
    margin-top: 2px;
  }

  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    gap: 12px;
    margin-bottom: 2rem;
  }

  .project-card {
    padding: 1.25rem;
    background: var(--color-background-primary);
    border: 0.5px solid var(--color-border-tertiary);
    border-radius: var(--border-radius-lg);
    transition: border-color 0.2s;
    cursor: pointer;
  }

  .project-card:hover {
    border-color: var(--color-border-primary);
  }

  .project-icon {
    font-size: 20px;
    margin-bottom: 8px;
  }

  .project-title {
    font-size: 14px;
    font-weight: 700;
    color: var(--color-text-primary);
    margin-bottom: 6px;
  }

  .project-desc {
    font-size: 12px;
    color: var(--color-text-secondary);
    line-height: 1.5;
    margin-bottom: 10px;
  }

  .tech-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 4px;
  }

  .tech-tag {
    font-family: 'JetBrains Mono', monospace;
    font-size: 10px;
    padding: 2px 7px;
    border-radius: 4px;
    background: var(--color-background-info);
    color: var(--color-text-info);
    font-weight: 500;
  }

  .skills-section {
    margin-bottom: 2rem;
  }

  .skills-group {
    margin-bottom: 1.25rem;
  }

  .skills-group-title {
    font-size: 12px;
    font-weight: 500;
    color: var(--color-text-secondary);
    margin-bottom: 8px;
  }

  .skills-pills {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
  }

  .skill-pill {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    padding: 4px 10px;
    border-radius: 6px;
    border: 0.5px solid var(--color-border-secondary);
    background: var(--color-background-secondary);
    color: var(--color-text-primary);
    font-weight: 500;
  }

  .skill-pill.lang { border-color: #85B7EB; color: #185FA5; background: #E6F1FB; }
  .skill-pill.web { border-color: #5DCAA5; color: #0F6E56; background: #E1F5EE; }
  .skill-pill.back { border-color: #97C459; color: #3B6D11; background: #EAF3DE; }
  .skill-pill.db { border-color: #FAC775; color: #854F0B; background: #FAEEDA; }
  .skill-pill.tool { border-color: #B4B2A9; color: #444441; background: #F1EFE8; }

  .quote-block {
    padding: 1.25rem 1.5rem;
    border-left: 3px solid #378ADD;
    background: var(--color-background-secondary);
    border-radius: 0 var(--border-radius-md) var(--border-radius-md) 0;
    margin-bottom: 2rem;
  }

  .quote-block p {
    font-size: 14px;
    font-style: italic;
    color: var(--color-text-secondary);
    line-height: 1.6;
  }

  .contact-row {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .contact-link {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 6px 14px;
    border-radius: var(--border-radius-md);
    border: 0.5px solid var(--color-border-secondary);
    font-size: 13px;
    font-weight: 500;
    color: var(--color-text-primary);
    text-decoration: none;
    background: var(--color-background-secondary);
    cursor: pointer;
  }

  .contact-link:hover {
    background: var(--color-background-primary);
    border-color: var(--color-border-primary);
  }

  .divider {
    height: 0.5px;
    background: var(--color-border-tertiary);
    margin: 1.5rem 0;
  }

  @media (max-width: 500px) {
    .header-section { flex-direction: column; text-align: center; }
    .badges-row { justify-content: center; }
    .stats-row { grid-template-columns: repeat(2, 1fr); }
  }
</style>

<div class="profile-wrapper">

  <!-- Header -->
  <div class="header-section">
    <div class="avatar">AB</div>
    <div class="header-info">
      <h1>Abhay Barman</h1>
      <div class="handle">@ABHAYBARMAN067 · Jabalpur, MP</div>
      <div class="badges-row">
        <span class="badge"><span class="badge-dot dot-blue"></span>Full Stack Dev</span>
        <span class="badge"><span class="badge-dot dot-teal"></span>App Development</span>
        <span class="badge"><span class="badge-dot dot-green"></span>Machine Learning</span>
      </div>
    </div>
  </div>

  <!-- About -->
  <div class="section-label">About</div>
  <div class="about-card">
    <p>
      B.Tech CSE student at <span>Shri Ram Institute of Science & Technology, Jabalpur</span>.
      I love mixing <span>creative UI designs</span> with <span>powerful backend logic</span> —
      building real-time apps, event platforms, and ML-powered tools.
      Quick learner, always exploring new technologies to improve efficiency and performance.
    </p>
  </div>

  <!-- Stats -->
  <div class="stats-row">
    <div class="stat-card">
      <div class="stat-val">7.17</div>
      <div class="stat-lbl">CGPA (B.Tech)</div>
    </div>
    <div class="stat-card">
      <div class="stat-val">4+</div>
      <div class="stat-lbl">Projects built</div>
    </div>
    <div class="stat-card">
      <div class="stat-val">MERN</div>
      <div class="stat-lbl">Primary stack</div>
    </div>
  </div>

  <!-- Projects -->
  <div class="section-label">Projects</div>
  <div class="projects-grid">

    <div class="project-card">
      <div class="project-icon">📹</div>
      <div class="project-title">Video Calling Web App</div>
      <div class="project-desc">Real-time video conferencing with room-based IDs, ZegoCloud UIKit integration, and custom 404 routing.</div>
      <div class="tech-tags">
        <span class="tech-tag">React.js</span>
        <span class="tech-tag">Vite</span>
        <span class="tech-tag">Tailwind</span>
        <span class="tech-tag">ZegoCloud</span>
      </div>
    </div>

    <div class="project-card">
      <div class="project-icon">🎟️</div>
      <div class="project-title">Event Management Platform</div>
      <div class="project-desc">Scalable MERN platform for event browsing, ticket booking, JWT auth, and real-time seat availability.</div>
      <div class="tech-tags">
        <span class="tech-tag">React.js</span>
        <span class="tech-tag">Node.js</span>
        <span class="tech-tag">MongoDB</span>
        <span class="tech-tag">JWT</span>
      </div>
    </div>

    <div class="project-card">
      <div class="project-icon">🌿</div>
      <div class="project-title">Air Quality Prediction</div>
      <div class="project-desc">ML-powered web app to predict air quality levels using Python, Flask, and a trained model.</div>
      <div class="tech-tags">
        <span class="tech-tag">Python</span>
        <span class="tech-tag">Flask</span>
        <span class="tech-tag">ML</span>
      </div>
    </div>

    <div class="project-card">
      <div class="project-icon">🍲</div>
      <div class="project-title">Recipe Sharing Platform</div>
      <div class="project-desc">Community-driven recipe sharing built with the full MERN stack and custom UI design.</div>
      <div class="tech-tags">
        <span class="tech-tag">MongoDB</span>
        <span class="tech-tag">Express</span>
        <span class="tech-tag">React</span>
        <span class="tech-tag">Node</span>
      </div>
    </div>

    <div class="project-card">
      <div class="project-icon">📱</div>
      <div class="project-title">Bus Ticket Booking App</div>
      <div class="project-desc">Mobile app for booking bus tickets with React Native and Firebase backend.</div>
      <div class="tech-tags">
        <span class="tech-tag">React Native</span>
        <span class="tech-tag">Firebase</span>
      </div>
    </div>

  </div>

  <!-- Skills -->
  <div class="section-label">Tech Stack</div>
  <div class="skills-section">
    <div class="skills-group">
      <div class="skills-group-title">Languages</div>
      <div class="skills-pills">
        <span class="skill-pill lang">JavaScript</span>
        <span class="skill-pill lang">Python</span>
        <span class="skill-pill lang">SQL</span>
      </div>
    </div>
    <div class="skills-group">
      <div class="skills-group-title">Frontend</div>
      <div class="skills-pills">
        <span class="skill-pill web">HTML5</span>
        <span class="skill-pill web">CSS3</span>
        <span class="skill-pill web">React.js</span>
        <span class="skill-pill web">React Native</span>
        <span class="skill-pill web">GSAP</span>
        <span class="skill-pill web">Three.js</span>
        <span class="skill-pill web">Bootstrap</span>
        <span class="skill-pill web">Tailwind</span>
      </div>
    </div>
    <div class="skills-group">
      <div class="skills-group-title">Backend</div>
      <div class="skills-pills">
        <span class="skill-pill back">Node.js</span>
        <span class="skill-pill back">Express.js</span>
        <span class="skill-pill back">Flask</span>
        <span class="skill-pill back">Machine Learning</span>
      </div>
    </div>
    <div class="skills-group">
      <div class="skills-group-title">Databases & Cloud</div>
      <div class="skills-pills">
        <span class="skill-pill db">MongoDB</span>
        <span class="skill-pill db">MongoDB Atlas</span>
        <span class="skill-pill db">Cloudinary</span>
        <span class="skill-pill db">Firebase</span>
      </div>
    </div>
    <div class="skills-group">
      <div class="skills-group-title">Tools</div>
      <div class="skills-pills">
        <span class="skill-pill tool">Git</span>
        <span class="skill-pill tool">GitHub</span>
        <span class="skill-pill tool">VS Code</span>
        <span class="skill-pill tool">Postman</span>
        <span class="skill-pill tool">Vite</span>
      </div>
    </div>
  </div>

  <!-- Quote -->
  <div class="quote-block">
    <p>"Build things you love. Break things to learn. Fix things to grow."</p>
  </div>

  <!-- Contact -->
  <div class="section-label">Connect</div>
  <div class="contact-row">
    <a class="contact-link" href="https://github.com/ABHAYBARMAN067">
      <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z"/></svg>
      GitHub
    </a>
    <a class="contact-link" href="https://www.linkedin.com/in/abhay-barman-9a0b3a277">
      <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
      LinkedIn
    </a>
    <a class="contact-link" href="https://codepen.io/Abhay-Barman">
      <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M18.144 13.067v-2.134L16.55 12zm1.276 1.194a.628.628 0 01-.006.083l-.005.028-.011.053-.01.031c-.005.016-.01.031-.017.047l-.014.03a.78.78 0 01-.021.043l-.019.03a.57.57 0 01-.08.1l-.026.025a.602.602 0 01-.036.03l-.029.022-.01.008-6.782 4.522a.637.637 0 01-.708 0L4.864 14.79l-.01-.008a.599.599 0 01-.065-.052l-.026-.025-.032-.034-.021-.028a.588.588 0 01-.067-.11l-.014-.031a.644.644 0 01-.017-.047l-.01-.031-.01-.053-.006-.028a.628.628 0 01-.006-.083V9.739a.633.633 0 01.006-.083l.005-.028.011-.053.01-.031c.005-.016.01-.031.017-.047l.014-.03a.78.78 0 01.021-.043l.019-.03a.57.57 0 01.08-.1l.026-.025a.602.602 0 01.036-.03l.029-.022.01-.008 6.782-4.522a.637.637 0 01.708 0l6.782 4.522.01.008.029.022.036.03.026.025a.57.57 0 01.08.1l.019.03a.78.78 0 01.021.043l.014.03c.007.016.012.031.017.047l.01.031.011.053.005.028a.628.628 0 01.006.083v4.527zM12 4.364l-2.905 1.937L12 8.238l2.905-1.937zm-4.547 3.84L5.13 9.739l2.323 1.535zm9.09 0v3.435l2.323-1.536zm-3.814 4.11L12 14.251l-1.729-1.937L8.179 13.15l3.821 2.544 3.821-2.544zM8.83 13.067L7.236 11.933 5.643 13.067 7.236 14.2zm7.88 0L18.144 14.2l1.593-1.133-1.593-1.134zm-3.633 2.671l-2.323-1.535v3.07zm2.323-1.535l-2.323 1.535v1.535l2.323-1.535z"/></svg>
      CodePen
    </a>
    <a class="contact-link" href="mailto:abhaybarman067@gmail.com">
      <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="m22 7-10 7L2 7"/></svg>
      Email
    </a>
  </div>

</div>
