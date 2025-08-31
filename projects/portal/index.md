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
    <a href="/projects/portal">EN</a>
    <a href="/kr/projects/portal">KR</a>
  </div>

<span id="nav-menu-toggle">☰</span>
  <div id="nav-links">
    <!-- Navigation Links will be dynamically populated -->
  </div>
</div>

<div style="position: relative; margin-bottom: 40px;">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=300&section=header&fontSize=45&animation=fadeIn&fontAlignY=38&desc=&descAlignY=51&descAlign=62" alt="Header" style="display: block; width: 100%; height: auto; margin: 0; padding: 0; border-radius: 8px;" />

<div style="position:absolute;left:40px;bottom:-10px;width:80px;height:80px;background:white;border-radius:20px;display:flex;align-items:center;justify-content:center;box-shadow:0 2px 6px rgba(0,0,0,0.15);">
<img src="../../images/portal/app_icon.png" alt="Project Icon" style="max-width:70%;max-height:70%;object-fit:contain;" />
</div>

</div>

# Government Portal App

## 📝 Overview
**📌 App Introduction:** Android app for the official [government portal](https://www.redpinar.gob.cu/) of the city of Pinar del Rio, Cuba  
**🕒 Duration:** February 2021 ~ April 2021  
**📱 Platform:** Native Android app  
**🏢 Company:** Desoft (Cuba's national software development company)  
**👥 Team Size:** 2 developers  
**💼 Role:** Responsible for legacy code modernization and development of citizen service module  
**🛠️ Key Technologies:** `Kotlin` `MVVM` `Retrofit` `Room` `Jetpack` `ViewPager2` `WebView` `JavaScript` `Coroutines` `Moshi`  
**🔗 GitHub:** [daehan-lim/government-portal-app](https://github.com/daehan-lim/government-portal-app)

<div style="display: flex; overflow-x: auto; border: 2px solid #ccc; padding: 6px; border-radius: 8px;">
  <img src="../../images/portal/menu.png" width="240" style="margin-right: 5px;" alt="Government portal menu screen"/>
  <img src="../../images/portal/delegado.png" width="240" style="margin-right: 5px;" alt="District representative portal screen"/>
  <img src="../../images/portal/form.png" width="240" style="margin-right: 5px;" alt="Request submission form screen"/>
  <img src="../../images/portal/code.png" width="240" style="margin-right: 5px;" alt="Code input screen"/>
  <img src="../../images/portal/guide.png" width="240" alt="User guide screen"/> 
</div>
<span style="display: block; height: 11px;"></span>

## 📖 Project Background
There was a growing need to develop a mobile app that would allow citizens of Pinar del Río, Cuba, to seamlessly access the government portal, which had previously been limited to the existing website. The website was optimized for desktop use, causing inconvenience for mobile users when submitting government requests, accessing local information, or using administrative services. In particular, urgent improvements were needed in mobile accessibility to core services such as access to district representative information, tracking the status of civil requests, and browsing local classified listings. This led to developing a government portal app to provide intuitive mobile services for citizens. As part of this project, I was responsible for modernizing the existing legacy codebase.

## 🛠️ Tech Stack

[![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?logo=kotlin&logoColor=white&style=for-the-badge)](https://kotlinlang.org)
[![MVVM](https://img.shields.io/badge/MVVM-FF5252?style=for-the-badge)](https://developer.android.com/topic/architecture)
[![Room](https://img.shields.io/badge/Room-00796B?logo=android&logoColor=white&style=for-the-badge)](https://developer.android.com/training/data-storage/room)
[![RETROFIT](https://img.shields.io/badge/retrofit-67b586?logo=square&logoColor=white&style=for-the-badge)](https://square.github.io/retrofit)
[![Jetpack](https://img.shields.io/badge/Jetpack-F57C00?logo=android&logoColor=white&style=for-the-badge)](https://developer.android.com/jetpack)
[![Coroutines](https://img.shields.io/badge/Coroutines-7F52FF?logo=kotlin&logoColor=white&style=for-the-badge)](https://kotlinlang.org/docs/coroutines-overview.html)
[![ViewPager2](https://img.shields.io/badge/ViewPager2-7CB342?style=for-the-badge&logo=android&logoColor=white)](https://developer.android.com/jetpack/androidx/releases/viewpager2)
[![LiveData](https://img.shields.io/badge/LiveData-3F51B5?style=for-the-badge)](https://developer.android.com/topic/libraries/architecture/livedata)
[![DataBinding](https://img.shields.io/badge/DataBinding-7CB342?style=for-the-badge)](https://developer.android.com/topic/libraries/data-binding)
[![ViewBinding](https://img.shields.io/badge/ViewBinding-7CB342?style=for-the-badge)](https://developer.android.com/topic/libraries/view-binding)
[![Moshi](https://img.shields.io/badge/Moshi-4CAF50?style=for-the-badge)](https://github.com/square/moshi)
[![WebView](https://img.shields.io/badge/WebView-4285F4?style=for-the-badge&logo=android&logoColor=white)](https://developer.android.com/reference/android/webkit/WebView)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://www.w3.org/html/)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Material Design](https://img.shields.io/badge/Material%20Design-4285F4?logo=material-design&logoColor=white&style=for-the-badge)](https://material.io/design)

## 📋 Project Structure
```
├── data/                                    # Data layer
│   ├── database/                            # Room local database
│   │   └── classifieddatabase/              # Local property database
│   │       ├── Classified.kt                # Property information entity
│   │       ├── ClassifiedDao.kt             # Data access object
│   │       └── ClassifiedDatabase.kt        # Database configuration
│   ├── model/                               # Data model classes
│   │   ├── DelegateData.kt                  # Local representative information
│   │   ├── ClassifiedApi.kt                 # Property API response model
│   │   ├── Municipality.kt                  # Administrative district model
│   │   └── gestiondelegado/                 # Representative management models
│   └── network/                             # Network communication layer
│       └── PortalGobiernoApiService.kt      # REST API service
├── ui/                                      # Presentation layer
│   ├── classified/                          # Local property features
│   │   ├── ClassifiedFragment.kt            # Property listings screen
│   │   ├── ClassifiedViewModel.kt           # Property business logic
│   │   ├── ClassifiedAdapter.kt             # RecyclerView adapter
│   │   └── classifieddetail/                # Property detail information
│   ├── gestiondelegado/                     # Local representative management
│   │   ├── GestionDelegadoFragment.kt       # Representative menu screen
│   │   └── gestiondelegadosection/          # Representative service tabs
│   │       ├── GestionSectionActivity.kt    # ViewPager2-based tab interface
│   │       ├── GestionSectionViewModel.kt   # Shared business logic
│   │       ├── DelegadoDataFragment.kt      # Representative information lookup
│   │       ├── DispatchFragment.kt          # Online civil petition submission
│   │       └── ProcedureFollowUpFragment.kt # Civil petition tracking
│   └── goverment/                           # Government services WebView
│       └── GovernmentFragment.kt            # JavaScript injection WebView
├── misc/                                    # Utilities and common features
│   ├── Util.kt                              # Date formatting and other utilities
│   └── Converters.kt                        # Room type converters
└── BindingUtils.kt                          # Data binding adapters
```

## 🌟 Key Contributions
- Modernized the legacy codebase by adopting MVVM architecture, coroutines, and Jetpack components
- Implemented the district representative management system with automated administrative workflows for civil request submission, meeting schedule management, and processing status tracking using Retrofit/Moshi integration
- Built the local classifieds feed system with REST API integration, offline data caching, real-time synchronization, image carousel, and network status monitoring
- Integrated the Provincial Assembly portal by optimizing the desktop-oriented UI for mobile through WebView and JavaScript-based customization

## 🚀 Results and Impact
- Improved app stability and maintainability through legacy code modernization
- Streamlined administrative processes by automating civil request workflows
- Enhanced mobile accessibility with an offline-first design

<br><br><br>