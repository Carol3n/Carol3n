<style>
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=Outfit:wght@300;400;600;700&display=swap');
  
  body {
    background: linear-gradient(135deg, #0f0c29 0%, #302b63 100%);
    min-height: 100vh;
  }
  
  .canvas {
    position: relative;
    width: 100%;
    min-height: 1200px;
    background: linear-gradient(135deg, #1a1a2e 0%, #16213e 50%, #0f3460 100%);
    overflow: hidden;
    padding: 40px 20px;
  }
  
  .floating-icon {
    position: absolute;
    width: 60px;
    height: 60px;
    opacity: 0.15;
    filter: blur(1px);
    pointer-events: none;
  }
  
  /* Scattered tech icons */
  .icon-1 { top: 5%; left: 5%; animation: float 6s ease-in-out infinite; }
  .icon-2 { top: 15%; right: 10%; animation: float 7s ease-in-out infinite 1s; }
  .icon-3 { top: 30%; left: 15%; animation: float 8s ease-in-out infinite 2s; }
  .icon-4 { top: 45%; right: 8%; animation: float 6.5s ease-in-out infinite 0.5s; }
  .icon-5 { top: 60%; left: 10%; animation: float 7.5s ease-in-out infinite 1.5s; }
  .icon-6 { bottom: 20%; right: 12%; animation: float 6s ease-in-out infinite 0.8s; }
  .icon-7 { bottom: 35%; left: 8%; animation: float 7s ease-in-out infinite 1.2s; }
  .icon-8 { bottom: 15%; right: 20%; animation: float 8s ease-in-out infinite 0.3s; }
  
  @keyframes float {
    0%, 100% { transform: translateY(0px); }
    50% { transform: translateY(-20px); }
  }
  
  .content-wrapper {
    position: relative;
    z-index: 10;
    max-width: 900px;
    margin: 0 auto;
    text-align: center;
  }
  
  .name-title {
    font-family: 'Playfair Display', serif;
    font-size: 4.5em;
    font-weight: 900;
    background: linear-gradient(135deg, #00d4ff 0%, #7c3aed 50%, #ff006e 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin: 20px 0;
    letter-spacing: -2px;
    animation: glow 3s ease-in-out infinite;
  }
  
  @keyframes glow {
    0%, 100% { filter: drop-shadow(0 0 10px rgba(124, 58, 237, 0.3)); }
    50% { filter: drop-shadow(0 0 20px rgba(0, 212, 255, 0.5)); }
  }
  
  .funny-line {
    font-family: 'Outfit', sans-serif;
    font-size: 1.8em;
    font-weight: 700;
    color: #00d4ff;
    margin: 15px 0;
    text-shadow: 0 0 20px rgba(0, 212, 255, 0.5);
    font-style: italic;
  }
  
  .cat-walk {
    position: relative;
    height: 250px;
    margin: 50px 0;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  .cat {
    font-size: 120px;
    position: absolute;
    animation: walkCat 10s infinite cubic-bezier(0.4, 0, 0.6, 1);
  }
  
  @keyframes walkCat {
    0% {
      left: -150px;
      transform: scaleX(1);
    }
    10%, 90% {
      transform: scaleX(1);
    }
    50% {
      transform: scaleX(1);
    }
    91%, 100% {
      left: 110%;
      transform: scaleX(-1);
    }
  }
  
  .role-badge {
    font-family: 'Outfit', sans-serif;
    font-size: 1.4em;
    font-weight: 700;
    color: #fff;
    margin: 30px 0;
    letter-spacing: 2px;
    text-transform: uppercase;
    background: rgba(124, 58, 237, 0.2);
    border: 2px solid #7c3aed;
    padding: 15px 30px;
    border-radius: 50px;
    display: inline-block;
  }
  
  .divider-line {
    width: 80px;
    height: 3px;
    background: linear-gradient(90deg, transparent, #7c3aed, transparent);
    margin: 40px auto;
  }
  
  .section-header {
    font-family: 'Playfair Display', serif;
    font-size: 2.5em;
    font-weight: 900;
    color: #00d4ff;
    margin: 50px 0 40px 0;
    text-shadow: 0 0 15px rgba(0, 212, 255, 0.3);
  }
  
  .tech-showcase {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 30px;
    margin: 40px 0;
    padding: 40px;
    background: rgba(124, 58, 237, 0.1);
    border-radius: 20px;
    border: 1px solid rgba(0, 212, 255, 0.3);
  }
  
  .tech-badge {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 12px;
    padding: 20px;
    background: rgba(0, 212, 255, 0.05);
    border-radius: 12px;
    border: 1px solid rgba(0, 212, 255, 0.2);
    transition: all 0.3s ease;
    cursor: pointer;
  }
  
  .tech-badge:hover {
    background: rgba(0, 212, 255, 0.15);
    border-color: rgba(0, 212, 255, 0.6);
    transform: translateY(-5px);
    box-shadow: 0 10px 30px rgba(0, 212, 255, 0.2);
  }
  
  .tech-icon-main {
    width: 55px;
    height: 55px;
    filter: drop-shadow(0 0 8px rgba(0, 212, 255, 0.5));
    transition: filter 0.3s ease;
  }
  
  .tech-badge:hover .tech-icon-main {
    filter: drop-shadow(0 0 15px rgba(124, 58, 237, 0.8));
  }
  
  .tech-label {
    font-family: 'Outfit', sans-serif;
    font-size: 0.95em;
    font-weight: 700;
    color: #fff;
    text-transform: uppercase;
    letter-spacing: 1px;
  }
  
  .connect-section {
    margin: 60px 0;
  }
  
  .linkedin-btn {
    display: inline-block;
    padding: 18px 50px;
    background: linear-gradient(135deg, #00d4ff 0%, #7c3aed 100%);
    color: white;
    text-decoration: none;
    border-radius: 50px;
    font-family: 'Outfit', sans-serif;
    font-weight: 700;
    font-size: 1.1em;
    transition: all 0.3s ease;
    box-shadow: 0 10px 30px rgba(0, 212, 255, 0.3);
    border: 2px solid transparent;
  }
  
  .linkedin-btn:hover {
    transform: translateY(-3px);
    box-shadow: 0 15px 40px rgba(0, 212, 255, 0.5);
    border-color: #00d4ff;
  }
  
  .motto {
    font-family: 'Outfit', sans-serif;
    font-size: 1.3em;
    color: #00d4ff;
    margin: 30px 0;
    font-weight: 600;
    font-style: italic;
  }
  
  .footer {
    font-family: 'Outfit', sans-serif;
    color: #888;
    font-size: 0.95em;
    margin-top: 50px;
    font-weight: 300;
  }
  
  @media (max-width: 768px) {
    .name-title {
      font-size: 2.5em;
    }
    
    .funny-line {
      font-size: 1.3em;
    }
    
    .tech-showcase {
      grid-template-columns: repeat(2, 1fr);
      gap: 15px;
      padding: 20px;
    }
    
    .cat {
      font-size: 80px;
    }
  }
</style>

<div class="canvas">
  <!-- Floating background icons -->
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/java/java-original.svg" class="floating-icon icon-1" alt="">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/spring/spring-original.svg" class="floating-icon icon-2" alt="">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/angular/angular-original.svg" class="floating-icon icon-3" alt="">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/mysql/mysql-original.svg" class="floating-icon icon-4" alt="">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/typescript/typescript-original.svg" class="floating-icon icon-5" alt="">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg" class="floating-icon icon-6" alt="">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vscode/vscode-original.svg" class="floating-icon icon-7" alt="">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/intellij/intellij-original.svg" class="floating-icon icon-8" alt="">

  <div class="content-wrapper">
    <div class="name-title">caroline laura mathias</div>
    
  <div class="funny-line">✨ Turning caffeine into code, bugs into features ✨</div>
    
   <div class="cat-walk">
      <div class="cat">🐱</div>
    </div>
        <div class="role-badge">💻 Full Stack Developer</div>
    
  <div class="divider-line"></div>
    
  <div class="section-header">Tech Arsenal</div>
        <div class="tech-showcase">
      <div class="tech-badge">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/java/java-original.svg" alt="Java" class="tech-icon-main">
        <div class="tech-label">Java</div>
      </div>
          <div class="tech-badge">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/spring/spring-original.svg" alt="Spring Boot" class="tech-icon-main">
        <div class="tech-label">Spring Boot</div>
      </div>
          <div class="tech-badge">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/angular/angular-original.svg" alt="Angular" class="tech-icon-main">
        <div class="tech-label">Angular</div>
      </div>
      
      <div class="tech-badge">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/mysql/mysql-original.svg" alt="MySQL" class="tech-icon-main">
        <div class="tech-label">MySQL</div>
      </div>
      
      <div class="tech-badge">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/typescript/typescript-original.svg" alt="TypeScript" class="tech-icon-main">
        <div class="tech-label">TypeScript</div>
      </div>
      
      <div class="tech-badge">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg" alt="JavaScript" class="tech-icon-main">
        <div class="tech-label">JavaScript</div>
      </div>
      
      <div class="tech-badge">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vscode/vscode-original.svg" alt="VSCode" class="tech-icon-main">
        <div class="tech-label">VSCode</div>
      </div>
      
      <div class="tech-badge">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/intellij/intellij-original.svg" alt="IntelliJ" class="tech-icon-main">
        <div class="tech-label">IntelliJ</div>
      </div>
    </div>
    
    <div class="divider-line"></div>
    
    <div class="connect-section">
      <a href="https://www.linkedin.com/in/caroline-laura-mathias/" target="_blank" class="linkedin-btn">→ Let's Connect on LinkedIn</a>
    </div>
    
    <div class="motto">"Code like there's no debugger tomorrow"</div>
    
    <div class="footer">
      Made with ❤️ by Caroline • Powered by ☕ and debugging sessions
    </div>
  </div>
</div>
