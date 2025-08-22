<style>
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;500;600;700&family=Inter:wght@300;400;500;600;700&display=swap');

:root {
  --primary-gradient: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  --accent-gradient: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
  --tech-gradient: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
  --card-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
  --card-hover-shadow: 0 20px 60px rgba(0, 0, 0, 0.15);
  --text-primary: #2d3748;
  --text-secondary: #718096;
  --bg-primary: #ffffff;
  --bg-secondary: #f7fafc;
  --border-radius: 16px;
  --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

/* Navigation Menu Styles */
#nav-menu {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background: rgba(255, 255, 255, 0.95);
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
  border-bottom: 1px solid rgba(255, 255, 255, 0.2);
  color: var(--text-primary);
  padding: 15px 0;
  z-index: 1000;
  display: flex;
  justify-content: space-between;
  align-items: center;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
  font-family: 'Inter', 'Noto Sans KR', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  transition: var(--transition);
}

#nav-menu a {
  color: var(--text-primary);
  text-decoration: none;
  margin: 0 16px;
  font-size: 15px;
  font-weight: 500;
  transition: var(--transition);
  position: relative;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#nav-menu > div:first-child a {
  font-size: 13px;
  margin: 0 10px;
  padding: 6px 12px;
  border-radius: 20px;
  background: var(--bg-secondary);
  transition: var(--transition);
}

#nav-menu > div:first-child a.active {
  background: var(--primary-gradient);
  color: white;
  transform: translateY(-1px);
}

#nav-menu a:hover {
  color: #667eea;
  transform: translateY(-1px);
}

#nav-menu a::after {
  content: '';
  position: absolute;
  width: 0;
  height: 2px;
  bottom: -5px;
  left: 50%;
  background: var(--primary-gradient);
  transition: var(--transition);
  transform: translateX(-50%);
}

#nav-menu a:hover::after {
  width: 100%;
}

body {
  padding-top: 80px;
  font-family: 'Inter', 'Noto Sans KR', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  line-height: 1.7;
  color: var(--text-primary);
  background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
  min-height: 100vh;
}

/* Hero Section */
.hero-section {
  background: var(--primary-gradient);
  padding: 80px 20px;
  text-align: center;
  color: white;
  margin: -80px -20px 60px -20px;
  position: relative;
  overflow: hidden;
}

.hero-section::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 100" fill="white" opacity="0.1"><polygon points="0,0 1000,0 1000,60 0,100"/></svg>');
  background-size: 100% 100%;
}

.hero-content {
  position: relative;
  z-index: 2;
  max-width: 800px;
  margin: 0 auto;
}

.hero-section h1 {
  font-size: 3.5rem;
  font-weight: 700;
  margin: 0 0 20px 0;
  text-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
  animation: fadeInUp 1s ease-out;
}

.hero-section .subtitle {
  font-size: 1.3rem;
  opacity: 0.95;
  font-weight: 300;
  margin-bottom: 40px;
  animation: fadeInUp 1s ease-out 0.2s both;
}

.social-links {
  display: flex;
  justify-content: center;
  gap: 20px;
  margin-top: 30px;
  animation: fadeInUp 1s ease-out 0.4s both;
}

.social-links a {
  transform: scale(1.1);
  transition: var(--transition);
  border-radius: 12px;
  overflow: hidden;
}

.social-links a:hover {
  transform: scale(1.2) translateY(-3px);
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.2);
}

/* Content Container */
.content-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

/* Modern Card Design */
.modern-card {
  background: var(--bg-primary);
  border-radius: var(--border-radius);
  padding: 30px;
  margin: 40px auto;
  box-shadow: var(--card-shadow);
  transition: var(--transition);
  border: 1px solid rgba(255, 255, 255, 0.2);
  position: relative;
  overflow: hidden;
}

.modern-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  background: var(--primary-gradient);
}

.modern-card:hover {
  transform: translateY(-8px);
  box-shadow: var(--card-hover-shadow);
}

/* Section Headings */
h2 {
  font-size: 2.5rem;
  font-weight: 700;
  margin: 60px 0 40px 0;
  text-align: center;
  background: var(--primary-gradient);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  position: relative;
}

h2::after {
  content: '';
  position: absolute;
  bottom: -10px;
  left: 50%;
  transform: translateX(-50%);
  width: 60px;
  height: 3px;
  background: var(--accent-gradient);
  border-radius: 2px;
}

/* Introduction Section */
.intro-section {
  background: var(--bg-primary);
  border-radius: var(--border-radius);
  padding: 40px;
  margin: 40px auto;
  box-shadow: var(--card-shadow);
  position: relative;
  overflow: hidden;
}

.intro-section::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  background: var(--tech-gradient);
}

/* Projects Grid */
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 30px;
  margin: 40px 0;
}

.project-card {
  background: var(--bg-primary);
  border-radius: var(--border-radius);
  overflow: hidden;
  box-shadow: var(--card-shadow);
  transition: var(--transition);
  text-decoration: none;
  color: inherit;
  position: relative;
  border: 1px solid rgba(255, 255, 255, 0.2);
}

.project-card:hover {
  transform: translateY(-12px) scale(1.02);
  box-shadow: var(--card-hover-shadow);
  text-decoration: none;
  color: inherit;
}

.project-preview {
  width: 100%;
  aspect-ratio: 1160 / 663;
  object-fit: cover;
  transition: var(--transition);
}

.project-card:hover .project-preview {
  transform: scale(1.05);
}

.project-info {
  padding: 25px;
  position: relative;
}

.project-title {
  font-size: 1.4rem;
  font-weight: 700;
  margin: 0 0 8px 0;
  color: var(--text-primary);
  display: flex;
  align-items: center;
  gap: 8px;
}

.project-description {
  color: var(--text-secondary);
  font-size: 1rem;
  margin: 0 0 15px 0;
  font-weight: 500;
}

.tech-stack {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin: 15px 0 10px 0;
}

.tech-tag {
  background: linear-gradient(135deg, #e3f2fd 0%, #bbdefb 100%);
  color: #1976d2;
  padding: 6px 12px;
  border-radius: 20px;
  font-size: 0.8rem;
  font-weight: 500;
  border: 1px solid rgba(25, 118, 210, 0.2);
  transition: var(--transition);
}

.tech-tag:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(25, 118, 210, 0.2);
}

.project-date {
  font-size: 0.85rem;
  color: var(--text-secondary);
  margin-top: 15px;
  font-weight: 400;
}

/* ML Projects Section */
.ml-projects-card {
  background: var(--primary-gradient);
  border-radius: var(--border-radius);
  padding: 40px;
  margin: 40px auto;
  max-width: 800px;
  text-align: center;
  box-shadow: var(--card-shadow);
  color: white;
  position: relative;
  overflow: hidden;
  transition: var(--transition);
}

.ml-projects-card::before {
  content: '';
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
  animation: float 6s ease-in-out infinite;
}

.ml-title {
  font-size: 1.6rem;
  font-weight: 700;
  margin: 0 0 15px 0;
  text-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
}

.ml-subtitle {
  font-size: 1.1rem;
  opacity: 0.95;
  font-weight: 400;
  margin: 0 0 25px 0;
}

.ml-tags {
  display: flex;
  justify-content: center;
  gap: 12px;
  flex-wrap: wrap;
  margin: 25px 0;
}

.ml-tag {
  background: rgba(255, 255, 255, 0.25);
  backdrop-filter: blur(10px);
  padding: 10px 18px;
  border-radius: 25px;
  color: white;
  font-size: 0.9rem;
  font-weight: 500;
  border: 1px solid rgba(255, 255, 255, 0.3);
  transition: var(--transition);
}

.ml-tag:hover {
  background: rgba(255, 255, 255, 0.35);
  transform: translateY(-3px);
}

.ml-cta {
  display: inline-block;
  background: white;
  color: #667eea;
  padding: 16px 35px;
  border-radius: 30px;
  text-decoration: none;
  font-weight: 700;
  font-size: 1.1rem;
  transition: var(--transition);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
  margin-top: 25px;
  position: relative;
  z-index: 2;
}

.ml-cta:hover {
  transform: translateY(-3px);
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.2);
  color: #667eea;
  text-decoration: none;
}

/* Contact Section */
.contact-section {
  background: var(--bg-primary);
  border-radius: var(--border-radius);
  padding: 40px;
  margin: 60px auto 40px auto;
  text-align: center;
  box-shadow: var(--card-shadow);
  position: relative;
  overflow: hidden;
}

.contact-section::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  background: var(--accent-gradient);
}

.contact-description {
  font-size: 1.1rem;
  color: var(--text-secondary);
  margin: 0 0 30px 0;
  line-height: 1.6;
}

.contact-links {
  display: flex;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
}

.contact-links a {
  transition: var(--transition);
  border-radius: 12px;
  overflow: hidden;
  opacity: 0.9;
}

.contact-links a:hover {
  transform: scale(1.1) translateY(-3px);
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
  opacity: 1;
}

/* Code styling */
code {
  background: var(--tech-gradient);
  color: white !important;
  border-radius: 6px;
  padding: 4px 8px;
  font-weight: 500;
  font-size: 0.85rem;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

/* Korean text styling */
.ko {
  font-family: 'Noto Sans KR', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  font-weight: 400;
  word-break: keep-all;
  letter-spacing: -0.3px;
  line-height: 1.8;
  font-size: 17px;
}

/* Hamburger Menu */
#nav-menu-toggle {
  display: none;
  cursor: pointer;
  font-size: 20px;
  margin-right: 20px;
  z-index: 1100;
  color: var(--text-primary);
  padding: 8px;
  border-radius: 8px;
  transition: var(--transition);
}

#nav-menu-toggle:hover {
  background: var(--bg-secondary);
}

#nav-links {
  display: flex;
  flex-wrap: wrap;
  padding-right: 20px;
}

/* Animations */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes float {
  0%, 100% { transform: translate(-50%, -50%) rotate(0deg); }
  50% { transform: translate(-50%, -50%) rotate(180deg); }
}

.fade-in {
  animation: fadeInUp 0.8s ease-out;
}

/* Typing SVG Container */
.typing-container {
  margin: 20px 0;
  position: relative;
  z-index: 2;
}

/* Mobile Responsive */
@media (max-width: 768px) {
  .hero-section h1 {
    font-size: 2.5rem;
  }
  
  .hero-section .subtitle {
    font-size: 1.1rem;
  }
  
  .projects-grid {
    grid-template-columns: 1fr;
    gap: 20px;
  }
  
  .ml-projects-card {
    padding: 30px 20px;
  }
  
  .ml-tags {
    gap: 8px;
  }
  
  .ml-tag {
    padding: 8px 14px;
    font-size: 0.85rem;
  }

  #nav-links {
    display: none;
    flex-direction: column;
    align-items: center;
    background: rgba(255, 255, 255, 0.98);
    backdrop-filter: blur(20px);
    width: 100%;
    position: absolute;
    top: 70px;
    left: 0;
    padding: 20px 0;
    border-radius: 0 0 16px 16px;
    box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
  }

  #nav-links.active {
    display: flex;
  }

  #nav-links a {
    margin: 10px 0;
    padding: 10px 20px;
    border-radius: 8px;
    transition: var(--transition);
  }

  #nav-links a:hover {
    background: var(--bg-secondary);
  }

  #nav-menu-toggle {
    display: block;
  }

  .contact-links {
    flex-direction: column;
    align-items: center;
  }
}

@media (max-width: 480px) {
  .hero-section {
    padding: 60px 15px;
  }
  
  .hero-section h1 {
    font-size: 2rem;
  }
  
  .modern-card, .intro-section, .contact-section {
    padding: 25px 20px;
  }
  
  .content-container {
    padding: 0 15px;
  }
}

/* Scroll behavior improvement */
html {
  scroll-behavior: smooth;
}

/* Enhanced hover effects for better interactivity */
.project-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
  transition: left 0.5s;
}

.project-card:hover::before {
  left: 100%;
}
</style>

<div id="nav-menu">
  <div style="margin-left: 20px;">
    <a href="/">EN</a>
    <a href="/kr" class="active">KR</a>
  </div>

<span id="nav-menu-toggle">☰</span>
  <div id="nav-links">
    <!-- Navigation Links will be dynamically populated -->
  </div>
</div>

<div class="hero-section">
  <div class="hero-content">
    <h1>임대한</h1>
    <p class="subtitle">Flutter 앱 개발자 & AI 솔루션 전문가</p>
    <div class="typing-container">
      <div style="display: flex; justify-content: center;">
        <img src="https://readme-typing-svg.herokuapp.com?color=%23FFFFFF&size=20&width=500&height=40&lines=Welcome+to+my+portfolio!;I'm+Daehan%2C+innovating+digital+solutions" alt="Typing animation" style="border-radius: 8px;">
      </div>
    </div>
    <div class="social-links">
      <a href="https://linkedin.com/in/penjan-a-eng-lim">
        <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge">
      </a>
      <a href="mailto:penjan.eng@gmail.com">
        <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email Badge">
      </a>
      <a href="https://github.com/daehan-lim">
        <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Badge">
      </a>
    </div>
  </div>
</div>

<div class="content-container">

<div class="intro-section fade-in">

## 👋 소개

<p class="ko">
Flutter 크로스플랫폼 앱 개발자로서 4명으로 구성된 팀을 리드하며 CI/CD 파이프라인 구축과 팀 코드 리뷰 프로세스 도입을 통해 수동 검수 시간 50% 단축을 이끌었습니다. 네이티브 Android 개발 배경을 바탕으로 플랫폼별 최적화에 강점을 보유하고 있습니다.
</p>

<p class="ko">
AI 석사 학위와 Gemini API 연동 경험을 통해 모바일 앱에 생성형 AI 기능을 효과적으로 통합할 수 있고, 레시피 생성 시스템에서 프롬프트 엔지니어링과 검증 모델 도입을 통해 적합하지 않은 레시피 생성률을 85%에서 12%로 낮춘 경험이 있습니다.
</p>

<p class="ko">
Firebase 백엔드 연동, 위치 기반 서비스, 다국어 지원 등 다양한 모바일 기능을 구현하여 Play Store와 App Store에 성공적으로 앱을 배포했으며, 성능 최적화를 통해 AI 처리 시간 40% 단축과 API 비용 35% 절감을 달성했습니다.
</p>

</div>

## 📱 모바일 애플리케이션

<div class="projects-grid">

<!--ShareLingo-->
<a href="sharelingo/" class="project-card">
  <img src="../images/sharelingo/preview.png" alt="ShareLingo - 언어교류 SNS 앱" class="project-preview" />
  <div class="project-info">
    <h3 class="project-title">ShareLingo <span style="color: #21427D; font-size: 15px;">🔗</span></h3>
    <p class="project-description">언어교류 SNS 앱</p>
    <div class="tech-stack">
      <span class="tech-tag">Flutter</span>
      <span class="tech-tag">Clean Architecture</span>
      <span class="tech-tag">Google OAuth</span>
      <span class="tech-tag">CI/CD</span>
      <span class="tech-tag">Firebase</span>
      <span class="tech-tag">Riverpod</span>
    </div>
    <p class="project-date">2025.05.16 ~ 2025.05.27 (2주)</p>
  </div>
</a>

<!--Cooki-->
<a href="cooki/" class="project-card">
  <img src="../images/cooki/preview.png" alt="Cooki - AI 레시피 커뮤니티 앱" class="project-preview" />
  <div class="project-info">
    <h3 class="project-title">Cooki <span style="color: #21427D; font-size: 15px;">🔗</span></h3>
    <p class="project-description">AI 레시피 커뮤니티 앱</p>
    <div class="tech-stack">
      <span class="tech-tag">Flutter</span>
      <span class="tech-tag">Gemini API</span>
      <span class="tech-tag">Dio</span>
      <span class="tech-tag">Cloud Functions</span>
      <span class="tech-tag">Riverpod</span>
      <span class="tech-tag">MVVM</span>
      <span class="tech-tag">Firestore</span>
    </div>
    <p class="project-date">2025.06.01 ~ 2025.07.04 (1개월)</p>
  </div>
</a>

<!--Cubadebate-->
<a href="cubadebate/" class="project-card">
  <img src="../images/cubadebate/preview.png" alt="Cubadebate 뉴스 앱" class="project-preview" />
  <div class="project-info">
    <h3 class="project-title">Cubadebate <span style="color: #21427D; font-size: 15px;">🔗</span></h3>
    <p class="project-description">맞춤형 뉴스 플랫폼</p>
    <div class="tech-stack">
      <span class="tech-tag">Android</span>
      <span class="tech-tag">Kotlin</span>
      <span class="tech-tag">Coroutines</span>
      <span class="tech-tag">MVVM</span>
      <span class="tech-tag">Room</span>
      <span class="tech-tag">Retrofit</span>
      <span class="tech-tag">Glide</span>
      <span class="tech-tag">Lottie</span>
      <span class="tech-tag">ViewBinding</span>
    </div>
    <p class="project-date">2021.03.15 ~ 2021.06.30 (3.5개월)</p>
  </div>
</a>

</div>

## 🔬 머신러닝 프로젝트

<div class="ml-projects-card">
  <h3 class="ml-title">🎓 AI/ML 프로젝트</h3>
  <p class="ml-subtitle">충남대학교 석사과정 중 수행한 머신러닝 프로젝트</p>
  <div class="ml-tags">
    <span class="ml-tag">연합학습</span>
    <span class="ml-tag">NLP 분류 모델</span>
    <span class="ml-tag">의료 데이터 분석기</span>
    <span class="ml-tag">정보 검색 시스템</span>
  </div>
  <a href="/ml_projects/kr" class="ml-cta">
    머신러닝 프로젝트 보기 →
  </a>
</div>

## 📫 연락처

<div class="contact-section">
  <p class="contact-description ko">
    채용 및 협업 문의는 언제든 환영합니다. 아래 링크를 통해 링크드인이나 이메일로 연락해 주실 수 있습니다.
  </p>
  <div class="contact-links">
    <a href="https://linkedin.com/in/penjan-a-eng-lim">
      <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge">
    </a>
    <a href="mailto:penjan.eng@gmail.com">
      <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email Badge">
    </a>
    <a href="https://github.com/daehan-lim">
      <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Badge">
    </a>
  </div>
</div>

</div>

<script>
  document.addEventListener("DOMContentLoaded", function () {
    const navLinksContainer = document.getElementById("nav-links");
    const toggle = document.getElementById("nav-menu-toggle");
    const headings = document.querySelectorAll("h2");

    // Remove auto-generated H1 heading completely to avoid spacing issues
    const autoGeneratedH1 = document.querySelector("h1:first-of-type");
    if (autoGeneratedH1) {
      autoGeneratedH1.remove();
    }

    // Create navigation links dynamically, excluding subheadings (###)
    headings.forEach((heading, index) => {
      if (heading.tagName === "H3") return; // Skip ### subheadings

      // Create a clean title without emojis for the nav bar
      const cleanText = heading.textContent.replace(/[\u{1F300}-\u{1FAF6}]/gu, '').trim();

      // Create an ID for each heading if not already present
      if (!heading.id) {
        heading.id = "section-" + index;
      }

      // Create navigation link
      const navLink = document.createElement("a");
      navLink.href = "#" + heading.id;
      navLink.textContent = cleanText;
      navLinksContainer.appendChild(navLink);
    });

    // Add click event for hamburger toggle
    toggle.addEventListener("click", () => {
      navLinksContainer.classList.toggle("active");
    });

    // Adjust scroll behavior to account for fixed navbar height
    const adjustScroll = (e, href) => {
      e.preventDefault();
      const target = document.querySelector(href);
      if (target) {
        window.scrollTo({
          top: target.offsetTop - 100, // Offset for navbar height
          behavior: 'smooth'
        });
      }
    };

    // Handle nav bar links
    document.querySelectorAll('#nav-links a').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        adjustScroll(e, this.getAttribute('href'));
        navLinksContainer.classList.remove('active'); // Collapse the dropdown
      });
    });

    // Handle all markdown links with hash anchors
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        adjustScroll(e, this.getAttribute('href'));
      });
    });

    // Add intersection observer for fade-in animations
    const observerOptions = {
      threshold: 0.1,
      rootMargin: '0px 0px -50px 0px'
    };

    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('fade-in');
        }
      });
    }, observerOptions);

    // Observe all cards for animation
    document.querySelectorAll('.project-card, .modern-card, .ml-projects-card, .contact-section').forEach(card => {
      observer.observe(card);
    });
  });
</script>