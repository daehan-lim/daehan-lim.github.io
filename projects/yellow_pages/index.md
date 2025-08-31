<!--suppress CssUnusedSymbol, JSUnusedLocalSymbols -->
<style>
/* Navigation Menu Styles */
#nav-menu {
  padding: 15px 0; /* Navbar height */
}

.image-row {
  display: flex;
  overflow-x: auto;
  border: 2px solid #ccc;
  padding: 6px;
  border-radius: 8px;
  gap: 5px;
  align-items: flex-start;
}

.image-item {
  width: 240px !important;
  height: auto !important;
  display: block !important;
  flex-shrink: 0 !important;
}

.linked-image {
  display: block !important;
  flex-shrink: 0 !important;
}

.markdown-body {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Helvetica Neue', Arial, sans-serif !important;
    font-weight: 400 !important;
    word-break: normal !important;
    overflow-wrap: break-word !important;
    letter-spacing: 0.02em !important;
    line-height: 1.6 !important;
    font-size: 16px !important;
}

#nav-menu a {
  margin: 0 14px;
  font-size: 14px;
}

</style>

<div id="nav-menu">
  <!-- Home button first -->
  <div style="margin-left: 20px; display: flex; align-items: center;">
    <a href="/" id="home-button">
      <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
        <path d="M12 3l9 7.5v10.5h-6v-6h-6v6H3V10.5L12 3z"/>
      </svg>
    </a>
    <a href="/projects/yellow_pages">EN</a>
    <a href="/kr/projects/yellow_pages">KR</a>
  </div>

<span id="nav-menu-toggle">☰</span>
  <div id="nav-links">
    <!-- Navigation Links will be dynamically populated -->
  </div>
</div>

<div style="position: relative; margin-bottom: 40px;">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=300&section=header&fontSize=45&animation=fadeIn&fontAlignY=38&desc=&descAlignY=51&descAlign=62" alt="Header" style="display: block; width: 100%; height: auto; margin: 0; padding: 0; border-radius: 8px;" />

<div style="position:absolute;left:40px;bottom:-10px;width:80px;height:80px;background:white;border-radius:20px;display:flex;align-items:center;justify-content:center;box-shadow:0 2px 6px rgba(0,0,0,0.15);">
<img src="../../images/yellow_pages/app_icon.png" alt="Project Icon" style="max-width:80%;max-height:80%;object-fit:contain;" />
</div>

</div>

# Yellow Pages Android App

## 📝 Overview
**📌 App Introduction:** Mobile business directory app for Cuba's telecommunications company combining business search with essential telecom services  
**🕒 Duration:** April 2019 ~ May 2020  
**📱 Platform:** Native Android app  
**🏢 Company:** ETECSA (Cuba's national telecommunications company)  
**👥 Team Size:** 2 developers (1 for main app, 1 for AR module)  
**💼 Role:** Lead Android app developer (excluding AR module)  
**🛠️ Key Technologies:** `Android` `Java` `SQLite` `VTM Maps` `WebView` `JavaScript` `SharedPreferences` `JUnit` `Apache HTTP Client`  
**🔗 GitHub:** [daehan-lim/cuban-yellow-pages](https://github.com/daehan-lim/cuban-yellow-pages)

<div style="display: flex; overflow-x: auto; border: 2px solid #ccc; padding: 6px; border-radius: 8px;">
  <img src="../../images/yellow_pages/1_home.png" width="240" style="margin-right: 5px;" alt="Home screen"/>
  <img src="../../images/yellow_pages/2_green_pages.png" width="240" style="margin-right: 5px;" alt="Green pages screen"/>
  <img src="../../images/yellow_pages/3_informative_pages.png" width="240" style="margin-right: 5px;" alt="Informative pages screen"/>
  <img src="../../images/yellow_pages/4_internet.png" width="240" style="margin-right: 5px;" alt="Internet screen"/>
  <img src="../../images/yellow_pages/5_long_distance.png" width="240" style="margin-right: 5px;" alt="Long distance screen"/>
  <img src="../../images/yellow_pages/6_advertisement.png" width="240" alt="Advertisement screen"/>

</div>
<span style="display: block; height: 11px;"></span>

## 📖 Project Background

ETECSA operated a Yellow Pages website for business and contact directory services, but Cuba's high internet costs and unreliable network connections severely limited mobile accessibility to this web-based platform. The website required constant connectivity, preventing offline access to information and missing opportunities to use native mobile features like offline mapping and direct calling. Users struggled to access directory information and government services without reliable internet access. ETECSA needed a mobile-first phone directory solution that could leverage their existing directory data and minimize data consumption.

## 🛠️ Tech Stack

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
[![Android SDK](https://img.shields.io/badge/Android%20SDK-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://developer.android.com)
![SQLite](https://img.shields.io/badge/sqlite-%2307405e.svg?style=for-the-badge&logo=sqlite&logoColor=white)
![VTM Maps](https://img.shields.io/badge/VTM%20Maps-4A90E2?style=for-the-badge)
[![WebView](https://img.shields.io/badge/WebView-4285F4?style=for-the-badge&logo=android&logoColor=white)](https://developer.android.com/reference/android/webkit/WebView)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://www.w3.org/html/)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://www.w3.org/Style/CSS/)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![SharedPreferences](https://img.shields.io/badge/SharedPreferences-4CAF50?style=for-the-badge)](https://developer.android.com/training/data-storage/shared-preferences)
![Gradle](https://img.shields.io/badge/Gradle-02303A.svg?style=for-the-badge&logo=Gradle&logoColor=white)
[![JUnit](https://img.shields.io/badge/JUnit-25A162?style=for-the-badge&logo=junit5&logoColor=white)](https://junit.org)
[![Apache HTTP](https://img.shields.io/badge/Apache%20HTTP%20Client-D22128?style=for-the-badge&logo=apache&logoColor=white)](https://hc.apache.org/httpcomponents-client-ga/)
![Material Design](https://img.shields.io/badge/Material%20Design-%234285F4.svg?style=for-the-badge&logo=material-design&logoColor=white)

## 🌟 Key Contributions
- Successfully developed Cuba's first Yellow Pages Android app, implementing a hybrid system combining online business searches with offline capabilities
- Developed offline location services using embedded vector maps
- Implemented automated background synchronization for offline government service content, using chunk-based transmission
- Built responsive search interface with dynamic filtering and efficient pagination
- Optimized stability and user experience through comprehensive unit, UI, and compatibility tests

## 🚀 Results and Impact
- Reduced data usage by 85% through offline vector mapping
- Improved synchronization success rate from 65% to 98% in unstable network environments by implementing chunk-based transmission

## 🌱 Problem Solving

**Data Synchronization in Unstable Network Conditions**

- **Problem**
  - Data synchronization success rate with server reached only 65% during beta testing
  - Synchronization failures required complete restart, causing significant user frustration
  - High data costs deterred users from attempting synchronization altogether
- **Root Cause Analysis**
  - **Network log Analysis**: Found that attempts to transmit large volumes of data in a single transfer were the main cause of failure in unstable network conditions
  - **User Feedback Collection**: Identified that the biggest complaint was progress being reset to the beginning whenever data transfer failed
- **Solution Process**
  - **Chunk-based data transfer**: Split large data into 500KB segments for transmission
  - **Progress tracking**: Used SQLite to save the transfer state of each chunk, preserving progress through failures
  - **Automatic retry mechanism**: Implemented network-aware automatic retry logic using `WorkManager`
- **Results**  
  Increased synchronization success rate to 98% and significantly improved user satisfaction

<br><br><br>