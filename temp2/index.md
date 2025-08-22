<style>
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@400;700&display=swap');

/* Navigation Menu Styles */
#nav-menu {
position: fixed;
top: 0;
left: 0;
width: 100%;
background-color: #3464e1;
color: white;
padding: 15px 0;
z-index: 1000;
display: flex;
justify-content: space-between;
align-items: center;
box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
font-family: 'Noto Sans KR', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
}

code {
  background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
  color: #495057 !important;
  border: 1px solid #dee2e6;
  border-radius: 6px;
  padding: 0.3em 0.6em;
  font-size: 0.8em;
  font-weight: 600;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
}

.project-preview {
  width: 100%;
  aspect-ratio: 1160 / 663;
  border-radius: 8px 8px 0 0;
  border: none;
  object-fit: cover;
  transition: transform 0.3s ease;
}

.project-preview:hover {
  transform: scale(1.02);
}

.ko {
font-family: 'Noto Sans KR', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
font-weight: 400;
word-break: keep-all;
letter-spacing: -0.3px;
line-height: 1.8; 
font-size: 17px;
}

#nav-menu a {
color: white;
text-decoration: none;
margin: 0 16px;
font-size: 16px;
transition: color 0.3s ease;
font-weight: 700;
-webkit-font-smoothing: antialiased;
-moz-osx-font-smoothing: grayscale;
}

#nav-menu > div:first-child a {
font-size: 14px;
margin: 0 10px;
padding: 6px 12px;
border-radius: 20px;
background: rgba(255, 255, 255, 0.1);
transition: all 0.3s ease;
}

#nav-menu > div:first-child a.active {
background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
transform: translateY(-1px);
}

#nav-menu > div:first-child a:hover {
background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
}

#nav-menu a:hover {
color: #f1c40f;
}

/* Adjust content padding for the fixed navbar */
body {
padding-top: 50px;
background: #ffffff;
}

/* Hamburger Menu (Toggle Button) */
#nav-menu-toggle {
display: none;
cursor: pointer;
font-size: 18px;
margin-right: 20px;
z-index: 1100;
}

/* Navigation Links */
#nav-links {
display: flex;
flex-wrap: wrap;
padding-right: 20px;
}

/* Project Cards - Enhanced but not flashy */
.project-grid-item {
  background: #ffffff;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
  transition: all 0.3s ease;
  border: 1px solid rgba(0, 0, 0, 0.06);
  overflow: hidden;
  position: relative;
}

.project-grid-item::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 3px;
  background: linear-gradient(90deg, #667eea, #764ba2, #f093fb);
  opacity: 0;
  transition: opacity 0.3s ease;
}

.project-grid-item:hover::before {
  opacity: 1;
}

.project-grid-item:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.12);
}

.project-grid-item p {
  padding: 18px;
  margin: 0;
}

.project-grid-item strong {
  color: #2d3748;
  font-size: 1.1rem;
}

/* Typography improvements */
h1 {
  font-size: 3.2rem;
  font-weight: 700;
  margin: 40px 0 20px 0;
  text-align: left;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

h2 {
  font-size: 1.8rem;
  font-weight: 700;
  margin: 50px 0 30px 0;
  color: #2d3748;
}

/* Project date styling */
small {
  background: rgba(52, 100, 225, 0.1);
  color: #3464e1;
  padding: 4px 8px;
  border-radius: 12px;
  font-size: 0.75rem;
  font-weight: 500;
  border: 1px solid rgba(52, 100, 225, 0.2);
}

/* Section styling with reduced padding */
.intro-section {
  background: #ffffff;
  border-radius: 12px;
  padding: 20px 30px;
  margin: 30px 0;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
  border-left: 4px solid;
  border-image: linear-gradient(135deg, #667eea 0%, #764ba2 100%) 1;
}

.contact-section {
  background: #ffffff;
  border-radius: 12px;
  padding: 20px 30px;
  margin: 30px 0;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
  text-align: center;
  border-left: 4px solid;
  border-image: linear-gradient(135deg, #f093fb 0%, #f5576c 100%) 1;
}

/* Modern enhancements */
.social-links a img,
.contact-links a img {
  transition: all 0.3s ease;
  border-radius: 6px;
}

.social-links a:hover img,
.contact-links a:hover img {
  transform: scale(1.05);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.15);
}

/* Improve typing SVG container */
.typing-container img {
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(102, 126, 234, 0.2);
}

@media (max-width: 768px) {
#nav-links {
  display: none;
  flex-direction: column;
  align-items: center;
  background-color: #3464e1;
  width: 100%;
  position: absolute;
  top: 60px;
  left: 0;
  padding: 15px 0;
  z-index: 1000;
}

#nav-links.active {
  display: flex;
}

#nav-links a {
  margin: 15px 0;
}

#nav-menu-toggle {
  display: block;
}

.project-grid-item {
  margin: 20px 0;
}

h1 {
  font-size: 2.5rem;
  text-align: center;
}

.intro-section,
.contact-section {
  padding: 15px 20px;
}
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
          top: target.offsetTop - 75,
          behavior: 'smooth'
        });
      }
    };

    // Handle nav bar links
    document.querySelectorAll('#nav-links a').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        adjustScroll(e, this.getAttribute('href'));
        navLinksContainer.classList.remove('active');
      });
    });

    // Handle all markdown links with hash anchors
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        adjustScroll(e, this.getAttribute('href'));
      });
    });

    // Apply project card styling after page loads
    setTimeout(() => {
      const projectLinks = document.querySelectorAll('a[href*="sharelingo/"], a[href*="cooki/"], a[href*="cubadebate/"]');
      projectLinks.forEach(link => {
        const div = link.querySelector('div');
        if (div) {
          div.classList.add('project-grid-item');
        }
      });

      // Style intro section
      const introText = document.querySelector('h2[id*="소개"]');
      if (introText && introText.nextElementSibling) {
        let current = introText.nextElementSibling;
        const wrapper = document.createElement('div');
        wrapper.className = 'intro-section';
        introText.parentNode.insertBefore(wrapper, current);
        
        while (current && current.tagName !== 'H2') {
          const next = current.nextElementSibling;
          wrapper.appendChild(current);
          current = next;
        }
      }

      // Style contact section
      const contactH2 = document.querySelector('h2[id*="연락처"]');
      if (contactH2) {
        let current = contactH2.nextElementSibling;
        const wrapper = document.createElement('div');
        wrapper.className = 'contact-section';
        contactH2.parentNode.insertBefore(wrapper, current);
        
        while (current) {
          const next = current.nextElementSibling;
          wrapper.appendChild(current);
          current = next;
        }
      }
    }, 100);
  });
</script>

# 임대한

<div class="typing-container">
[![Typing SVG](https://readme-typing-svg.herokuapp.com?color=%23667eea&size=24&width=600&height=45&lines=Welcome+to+my+portfolio!;I'm+Daehan%2C+innovating+digital+solutions)](https://git.io/typing-svg)
</div>

<div align="center"> 
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

## 👋 소개
Flutter 크로스플랫폼 앱 개발자로서 4명으로 구성된 팀을 리드하며 CI/CD 파이프라인 구축과 팀 코드 리뷰 프로세스 도입을 통해 수동 검수 시간 50% 단축을 이끌었습니다. 네이티브 Android 개발 배경을 바탕으로 플랫폼별 최적화에 강점을 보유하고 있습니다.

AI 석사 학위와 Gemini API 연동 경험을 통해 모바일 앱에 생성형 AI 기능을 효과적으로 통합할 수 있고, 레시피 생성 시스템에서 프롬프트 엔지니어링과 검증 모델 도입을 통해 적합하지 않은 레시피 생성률을 85%에서 12%로 낮춘 경험이 있습니다.

Firebase 백엔드 연동, 위치 기반 서비스, 다국어 지원 등 다양한 모바일 기능을 구현하여 Play Store와 App Store에 성공적으로 앱을 배포했으며, 성능 최적화를 통해 AI 처리 시간 40% 단축과 API 비용 35% 절감을 달성했습니다.

## 📱 모바일 애플리케이션

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px;">

<!--ShareLingo-->
<a href="sharelingo/" style="text-decoration: none; color: inherit;">
<div>
  <img src="../images/sharelingo/preview.png" alt="ShareLingo - 언어교류 SNS 앱" class="project-preview" />
  <p><strong>ShareLingo<span style="color: #21427D; font-size: 15px;">&thinsp;&thinsp;🔗</span></strong><br/>
    <span style="font-size: 0.9em;">언어교류 SNS 앱</span><br/> 
    <code>Flutter</code> <code>Clean Architecture</code> <code>Google OAuth</code> <code>CI/CD</code> <code>Firebase</code> <code>Riverpod</code><br/>
    <small>2025.05.16 ~ 2025.05.27 (2주)</small>
  </p>
</div>
</a>

<!--Cooki-->
<a href="cooki/" style="text-decoration: none; color: inherit;">
<div>
  <img src="../images/cooki/preview.png" alt="Cooki - AI 레시피 커뮤니티 앱" class="project-preview" />
  <p><strong>Cooki<span style="color: #21427D; font-size: 15px;">&thinsp;&thinsp;🔗</span></strong><br/>
    <span style="font-size: 0.9em;">AI 레시피 커뮤니티 앱</span><br/> 
    <code>Flutter</code> <code>Gemini API</code> <code>Dio</code> <code>Cloud Functions</code> <code>Riverpod</code> <code>MVVM</code> <code>Firestore</code><br/>
    <small>2025.06.01 ~ 2025.07.04 (1개월)</small>
  </p>
</div>
</a>

<!--Cubadebate-->
<a href="cubadebate/" style="text-decoration: none; color: inherit;">
<div>
  <img src="../images/cubadebate/preview.png" alt="Cubadebate 뉴스 앱" class="project-preview" />
  <p><strong>Cubadebate<span style="color: #21427D; font-size: 15px;">&thinsp;&thinsp;🔗</span></strong><br/>
    <span style="font-size: 0.9em;">맞춤형 뉴스 플랫폼</span><br/>
    <code>Android</code> <code>Kotlin</code> <code>Coroutines</code> <code>MVVM</code> <code>Room</code> <code>Retrofit</code> <code>Glide</code> <code>Lottie</code> <code>ViewBinding</code><br/>
    <small>2021.03.15 ~ 2021.06.30 (3.5개월)</small>
  </p>
</div>
</a>

</div>

## 🔬 머신러닝 프로젝트

<div style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); border-radius: 12px; padding: 25px; margin: 20px auto; max-width: 800px; text-align: center; box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);">
  <div style="color: white; margin-bottom: 15px;">
    <h3 style="margin: 0; font-size: 1.3em; font-weight: 700;">🎓 AI/ML 프로젝트</h3>
    <p style="color: white; margin: 10px 0 0 0; opacity: 0.9; font-size: 1.1em;">충남대학교 석사과정 중 수행한 머신러닝 프로젝트</p>
  </div>
  <div style="display: flex; justify-content: center; gap: 15px; flex-wrap: wrap; margin-top: 20px;">
    <span style="background: rgba(255,255,255,0.2); padding: 8px 16px; border-radius: 20px; color: white; font-size: 0.9em;">연합학습</span>
    <span style="background: rgba(255,255,255,0.2); padding: 8px 16px; border-radius: 20px; color: white; font-size: 0.9em;">NLP 분류 모델</span>
    <span style="background: rgba(255,255,255,0.2); padding: 8px 16px; border-radius: 20px; color: white; font-size: 0.9em;">의료 데이터 분석기</span>
    <span style="background: rgba(255,255,255,0.2); padding: 8px 16px; border-radius: 20px; color: white; font-size: 0.9em;">정보 검색 시스템</span>
  </div>
  <div style="margin-top: 20px;">
    <a href="/ml_projects/kr" style="display: inline-block; background: white; color: #667eea; padding: 12px 30px; border-radius: 25px; text-decoration: none; font-weight: 700; font-size: 1.1em; transition: all 0.3s ease; box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);">
      머신러닝 프로젝트 보기 →
    </a>
  </div>
</div>

## 📫 연락처

<p class="ko">
채용 및 협업 문의는 언제든 환영합니다. 아래 링크를 통해 링크드인이나 이메일로 연락해 주실 수 있습니다.
</p>

<div align="center"> 
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
<br>

<script>
// Apply styling after DOM is ready
document.addEventListener("DOMContentLoaded", function() {
  // Style project grid items
  setTimeout(() => {
    const projectDivs = document.querySelectorAll('a[href*="sharelingo/"] > div, a[href*="cooki/"] > div, a[href*="cubadebate/"] > div');
    projectDivs.forEach(div => {
      div.style.cssText = `
        background: #ffffff;
        border-radius: 12px;
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
        transition: all 0.3s ease;
        border: 1px solid rgba(0, 0, 0, 0.06);
        overflow: hidden;
        position: relative;
        padding: 0;
      `;
      
      // Add gradient top border
      const gradientBorder = document.createElement('div');
      gradientBorder.style.cssText = `
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        height: 3px;
        background: linear-gradient(90deg, #667eea, #764ba2, #f093fb);
        opacity: 0;
        transition: opacity 0.3s ease;
      `;
      div.appendChild(gradientBorder);
      
      const p = div.querySelector('p');
      if (p) {
        p.style.cssText = 'padding: 18px; margin: 0;';
      }

      const strong = div.querySelector('strong');
      if (strong) {
        strong.style.cssText = 'color: #2d3748; font-size: 1.1rem;';
      }
    });

    // Add hover effects to project links
    const projectLinks = document.querySelectorAll('a[href*="sharelingo/"], a[href*="cooki/"], a[href*="cubadebate/"]');
    projectLinks.forEach(link => {
      link.addEventListener('mouseenter', () => {
        const div = link.querySelector('div');
        const gradientBorder = div.querySelector('div:last-child');
        if (div) {
          div.style.transform = 'translateY(-3px)';
          div.style.boxShadow = '0 8px 25px rgba(0, 0, 0, 0.12)';
          if (gradientBorder) {
            gradientBorder.style.opacity = '1';
          }
        }
      });
      
      link.addEventListener('mouseleave', () => {
        const div = link.querySelector('div');
        const gradientBorder = div.querySelector('div:last-child');
        if (div) {
          div.style.transform = 'translateY(0)';
          div.style.boxShadow = '0 2px 8px rgba(0, 0, 0, 0.08)';
          if (gradientBorder) {
            gradientBorder.style.opacity = '0';
          }
        }
      });
    });
  }, 50);
});
</script>