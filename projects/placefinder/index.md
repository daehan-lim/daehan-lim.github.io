<!--suppress CssUnusedSymbol, JSUnusedLocalSymbols -->
<style>
/* Navigation Menu Styles */
#nav-menu {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background: linear-gradient(135deg, #3464e1 0%, #764ba2 100%); /* Navbar color */
  color: white;
  padding: 15px 0; /* Navbar height */
  z-index: 1000;
  display: flex;
  justify-content: space-between; /* Space between items */
  align-items: center; /* Vertically align items */
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

h1, h2 {
  color: #6951af !important;
}

code .nx,
code .n,
code .py,
code .p {
  color: #24292e !important;
}

.language-plaintext.highlighter-rouge > .highlight > pre.highlight > code {
  color: #24292e !important;
}

code.language-plaintext.highlighter-rouge {
  color: #EB5757 !important;                 /* strong red text */
  border-radius: 4px;                        /* rounded corners */
  padding: 0.2em 0.4em;                      /* small breathing space */
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
  color: white;
  text-decoration: none;
  margin: 0 14px;
  font-weight: bold;
  font-size: 14px;
  transition: color 0.3s ease;
}

#nav-menu > div:first-child a {
  font-size: 13px;
  margin: 0 7px;
  padding: 5px 11px;
  border-radius: 20px;
  background: rgba(255, 255, 255, 0.1);
  transition: all 0.3s ease;
  font-weight: 700; /* Increase from bold to 700 */
  -webkit-font-smoothing: antialiased; /* Better text rendering */
  -moz-osx-font-smoothing: grayscale;
}

#nav-menu > div:first-child a.active {
  background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
  color: white;
  transform: translateY(-1px);
}

#nav-menu > div:first-child a:hover {
  background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
  color: white;
}

/* Home button styles */
#home-button {
  color: white;
  text-decoration: none;
  font-weight: 700;
  font-size: 13px;
  padding: 5px 11px;
  border-radius: 50%; /* Changed from 20px to make it circular */
  background: rgba(255, 255, 255, 0.1);
  transition: all 0.3s ease;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin-right: 10px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
}

#home-button:hover {
  background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
  color: white;
  transform: translateY(-1px);
}

#home-button svg {
  width: 16px;
  height: 22px;
  fill: currentColor;
}

/* Adjust content padding for the fixed navbar */
body {
  padding-top: 50px; /* Adjusted for taller navbar */
}

/* Hamburger Menu (Toggle Button) */
#nav-menu-toggle {
  display: none;
  cursor: pointer;
  font-size: 18px;
  margin-right: 20px; /* Move to the right */
  z-index: 1100; /* Ensure toggle is above menu items */
}

/* Navigation Links */
#nav-links {
  display: flex;
  flex-wrap: wrap;
  padding-right: 20px;
}

@media (max-width: 768px) {
  #nav-links {
    display: none; /* Hide links initially on mobile */
    flex-direction: column;
    align-items: center;
    background: linear-gradient(135deg, #3464e1 0%, #764ba2 100%); /* Match navbar background */
    width: 100%;
    position: absolute;
    top: 60px; /* Space below navbar */
    left: 0;
    padding: 15px 0; /* Add spacing around links */
    z-index: 1000; /* Ensure it doesn't overlap the toggle button */
  }

  #nav-links.active {
    display: flex; /* Show links when active */
  }

  #nav-links a {
    margin: 15px 0; /* Added vertical spacing */
  }

  #nav-menu-toggle {
    display: block; /* Show hamburger menu */
  }
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
    <a href="/projects/placefinder">EN</a>
    <a href="/kr/projects/placefinder">KR</a>
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
          top: target.offsetTop - 75, // Offset for navbar height
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

    // Fix EN/KR active states based on current page
    function updateLanguageButtons() {
      const currentPath = window.location.pathname;
      const enButton = document.querySelector('a[href="/projects/placefinder"]');
      const krButton = document.querySelector('a[href="/kr/projects/placefinder"]');
      
      // Remove active class from both buttons first
      if (enButton) enButton.classList.remove('active');
      if (krButton) krButton.classList.remove('active');
      
      // Check for KR pages first (more specific)
      if (currentPath.includes('/kr')) {
        if (krButton) krButton.classList.add('active');
      } 
      // Then check for EN pages (root, index, etc.)
      else {
        if (enButton) enButton.classList.add('active');
      }
    }

    function updateHomeButton() {
      const currentPath = window.location.pathname;
      const homeButton = document.getElementById('home-button');
      
      if (homeButton) {
        if (currentPath.includes('/kr')) {
          homeButton.href = '/kr';
        } else {
          homeButton.href = '/';
        }
      }
    }

    // Update buttons on page load
    updateLanguageButtons();
    updateHomeButton();
    
    // Update buttons when navigation occurs (for SPAs)
    window.addEventListener('popstate', function() {
      updateLanguageButtons();
      updateHomeButton();
    });
  });
</script>

<div style="position: relative; margin-bottom: 40px;">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=300&section=header&fontSize=45&animation=fadeIn&fontAlignY=38&desc=&descAlignY=51&descAlign=62" alt="Header" style="display: block; width: 100%; height: auto; margin: 0; padding: 0; border-radius: 8px;" />

<img src="../../images/placefinder/app_logo.png" alt="Project Icon" style="position: absolute; left: 40px; bottom: -10px; width: 80px; height: 80px; border-radius: 20px; object-fit: cover;" />

</div>

# PlaceFinder - Location Search App

## 📝 Overview
**📌 App Introduction:** Mobile app for finding nearby places using Naver Local Search API and GPS location services  
**🕒 Duration:** April 20, 2025 ~ April 22, 2025 (3 days)  
**📱 Platform:** Flutter cross-platform app (iOS, Android)  
**👥 Team Size:** 1 developer (Personal project)  
**💼 Role:** Entire app UI/UX design & development, API integration  
**🛠️ Key Technologies:** `Flutter` `Dart` `Naver Local API` `VWorld API` `Riverpod` `Geolocator` `InAppWebView` `URL Launcher` `Dio`  
**🔗 GitHub:** [daehan-lim/flutter-place-finder](https://github.com/daehan-lim/flutter-place-finder)

<div class="image-row">
  <img src="../../images/placefinder/1_home_.png" alt="Home screen" class="image-item" />
  <img src="../../images/placefinder/2_web_view_.png" alt="Web view screen" class="image-item" />
  <img src="../../images/placefinder/3_naver_.png" alt="Naver screen" class="image-item" />
  <img src="../../images/placefinder/4_no_results_.png" alt="No results screen" class="image-item" />
  <img src="../../images/placefinder/5_offline_.png" alt="Offline screen" class="image-item" />
  <img src="../../images/placefinder/6_apple_maps_.png" alt="Apple Maps screen" class="image-item" />
  <img src="../../images/placefinder/7_map_selection_.png" alt="Map selection screen" class="image-item" />
  <img src="../../images/placefinder/8_naver_map_.png" alt="Naver Map screen" class="image-item" />
  <img src="../../images/placefinder/9_google_map_.png" alt="Google Map screen" class="image-item" />
  <img src="../../images/placefinder/10_kakao_map_.png" alt="Kakao Map screen" class="image-item" />
</div>
<span style="display: block; height: 11px;"></span>

## 📖 Project Description

PlaceFinder helps users discover nearby places by searching by place names or addresses. The app uses Naver Local Search API and VWorld API to provide GPS-based location search and supports seamless redirection to popular map applications. Users can quickly explore local businesses, restaurants, and points of interest while accessing detailed information through in-app web view integration.

## 🛠️ Tech Stack

[![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev)
[![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dart.dev/)
[![Riverpod](https://img.shields.io/badge/Riverpod-02569B?style=for-the-badge)](https://riverpod.dev/)
[![Dio](https://img.shields.io/badge/Dio-02569B?style=for-the-badge)](https://pub.dev/packages/dio)
[![Naver API](https://img.shields.io/badge/Naver_API-00C73C?style=for-the-badge&logo=naver&logoColor=white)](https://developers.naver.com/)
[![VWorld API](https://img.shields.io/badge/VWorld_API-4CAF50?style=for-the-badge)](https://www.vworld.kr/)
[![Geolocator](https://img.shields.io/badge/Geolocator-FF6B6B?style=for-the-badge)](https://pub.dev/packages/geolocator)
[![InAppWebView](https://img.shields.io/badge/InAppWebView-FF9800?style=for-the-badge)](https://pub.dev/packages/flutter_inappwebview)
[![URL Launcher](https://img.shields.io/badge/URL_Launcher-2196F3?style=for-the-badge)](https://pub.dev/packages/url_launcher)
[![Flutter Dotenv](https://img.shields.io/badge/Flutter_Dotenv-4CAF50?style=for-the-badge)](https://pub.dev/packages/flutter_dotenv)

## 📋 Project Structure

```
├── app/                               # App configuration and setup files
│   ├── constants/                     # App-wide constant definitions
│   │   ├── app_colors.dart            # Color constants
│   │   ├── app_constants.dart         # General app constants
│   │   └── app_styles.dart            # Style definitions
│   ├── app_providers.dart             # Riverpod provider setup
│   └── theme.dart                     # App theme configuration
│
├── core/                              # Core functionality and common utilities
│   ├── exceptions/                    # App-wide exception classes
│   │   └── data_exceptions.dart       # Data-related exception classes
│   ├── services/                      # External service integrations
│   │   └── map_launcher_service.dart
│   └── utils/                         # Helper functions and utility classes
│       ├── geolocator_util.dart
│       ├── snackbar_util.dart
│       └── string_format_utils.dart
│
├── data/                              # Data layer and data access
│   ├── dto/                           # Data Transfer Objects
│   │   ├── naver_place_dto.dart
│   │   └── vworld_district_dto.dart
│   ├── model/                         # Data models
│   │   └── place.dart
│   ├── network/                       # Network communication
│   │   └── dio_clients.dart
│   └── repository/                    # Repository implementations
│       └── location_repository.dart
│
├── ui/                                # User interface
│   ├── pages/                         # App screens
│   │   ├── home/                      # Home screen
│   │   │   ├── home_page.dart
│   │   │   ├── home_view_model.dart
│   │   │   └── widgets/
│   │   │       └── home_list_item.dart
│   │   └── web/                       # WebView screen
│   │       ├── place_web_page.dart
│   │       └── place_web_page_view_model.dart
│   └── widgets/                       # Common widgets
│       └── error_layout.dart
│
└── main.dart                          # App entry point
```

## 🎯 Key Features

- **Place Search**: Search for locations by entering place names or addresses through Naver Local Search API
- **GPS Location Search**: Find nearby places using current GPS location with one-tap access
- **Detailed Place Information**: Click on any search result to view detailed information through the place's web page
- **Map App Integration**: Launch places directly in device map apps (Google Maps, Apple Maps, Naver Map, etc.)
- **In-App Naver Search**: Browse Naver search results within the app using Custom Tabs (Android) and SFSafariViewController (iOS)

## 🌟 Implementation & Achievements

### Real-time Location-Based Search
- Integrated `Geolocator` for GPS coordinate acquisition with `VWorld API` to automatically identify user's current administrative district
- Implemented automatic nearby place loading on app startup to enhance user convenience with immediate local results
- Built reliable location detection with location permission handling and exception management

### Naver Local Search API and VWorld API Integration
- Implemented secure API communication through `Bearer Token` authentication and `Dio` HTTP client
- Processed place names, categories, addresses, and links with HTML tag cleaning and string formatting utilities
- Supported coordinate-to-address conversion via VWorld API for accurate location identification
- Configured `BaseOptions` for consistent HTTP settings with 10-second connection/reception timeout and debug logging through `LogInterceptor`

### Native App Integration and User Experience Enhancement
- **Platform-Specific Map App Integration**
  - **Android**: Implements `Geo URI` scheme allowing users to choose from installed map apps (Google Maps, Naver Map, KakaoMap)
  - **iOS**: Detects Naver Map installation and automatically falls back to Apple Maps when unavailable
  - Implemented `URL Launcher` integration for smooth transitions to map applications
  - Added 'Search on Naver' buttons to each place listing for accessing additional details within the app

- **InAppWebView-Based Detailed Information Access**
  - Implemented mobile-optimized web page loading with `Custom User Agent` configuration
  - Improved user wait time perception through loading indicators and error handling
  - Provided integrated in-app experience using `InAppBrowserView` mode for Naver search integration

### Robust Exception Handling and User Feedback
- **Layered Exception Handling System**
  - Implemented custom exception classes including `ApiException`, `NetworkException`, `EnvFileException` for specific scenarios
  - Provided intuitive error messages for network connection errors, no search results, missing environment variables, etc.
  - Optimized user notification experience with duplicate snackbar prevention logic
  - Implemented input validation to block empty search queries and prevent duplicate API requests during active searches, reducing unnecessary network calls
  - Improved user feedback for place details by preventing access to invalid or empty links and displaying snackbar notifications

- **User-Friendly UI/UX Implementation**
  - Added search bar with clear button, GPS icon, and loading indicators for better user interaction
  - Enhanced readability by providing `Tooltip` for long addresses
  - Implemented card-style list items using `InkWell` effects and shadows
  - Added automatic keyboard hiding on screen touch through `GestureDetector` for better user convenience

### Development Efficiency and Code Quality
- **Riverpod-Based State Management**
  - Implemented testable architecture through `Provider` pattern and dependency injection
  - Achieved consistent management of loading, error, and data states using `AsyncValue`
  - Ensured data integrity and minimized external API dependencies through separation of `DTO` and `Model`

- **Environment Variable Security Management**
  - Secured API keys and separated environment-specific configurations using `flutter_dotenv`
  - Provided a `.env.example` file to guide development environment configuration

- **Reusable Component Design**
  - Implemented independent widget components including `HomeListItem`, `MessageLayout`
  - Eliminated code duplication through common utility classes like `StringFormatUtils`, `SnackbarUtil`
  - Ensured design consistency through unified app theme file and color system

## 🌱 Problem Solving

**iOS Map App Integration Silent Failure**

- **Problem**  
  On iOS, when Naver Map is not installed and `launchUrl()` is called with the `nmap://` custom scheme, it fails silently without any response. The `Apple Maps` fallback configured with `try/catch` never executes, leaving users with no feedback or alternative action.

- **Initial Approach and Reasoning**  
  - I had experienced reliability issues with `canLaunchUrl()` in the Android implementation. It would return `false` even for executable `geo:` URIs:

  ```dart
  if (await canLaunchUrl(Uri.parse('geo:0,0?q=$encoded'))) {
    // Would return false despite being executable
  }
  ```

  - After encountering this Android behavior, I assumed `canLaunchUrl()` would be equally unreliable on iOS, so I used `try/catch` for failure handling on both platforms
<span style="display: block; height: 8px;"></span>
- **Why the Initial Solution Failed**
  ```dart
  static Future<void> openInMap(String queryAddress) async {
    if (Platform.isIOS) { 
      try {
        await launchUrl(naverUri, mode: LaunchMode.externalApplication);
      } catch (e) {
        // This catch block never executes on iOS
        final appleUri = Uri.parse('http://maps.apple.com/?q=$encoded');
        await launchUrl(appleUri, mode: LaunchMode.externalApplication);
      
      }
    }
  }
  ```

  The approach failed because iOS `launchUrl()` doesn't throw exceptions for unavailable apps - it just silently does nothing, so the catch block never executes and Apple Maps never launches.

- **Platform-Specific Behavior Analysis**  
  After reviewing documentation and GitHub issues, I discovered the key differences:
  - **iOS**: Fails silently when no app can handle the URL scheme, requiring pre-validation with `canLaunchUrl()`
  - **Android**: Exception-based handling works reliably for standard schemes like `geo:`
  
- **Final Solution**  
  Implemented platform-specific handling that works with each OS's characteristics:

  ```dart
  static Future<void> openInMap(String queryAddress) async {
    if (Platform.isIOS) { 
      final naverUri = Uri.parse('nmap://search?query=$encoded&appname=$appName');
      if (await canLaunchUrl(naverUri)) {
        await launchUrl(naverUri, mode: LaunchMode.externalApplication);
      } else {
        // Naver Map unavailable, use Apple Maps
        final appleUri = Uri.parse('http://maps.apple.com/?q=$encoded');
        if (await canLaunchUrl(appleUri)) {
          await launchUrl(appleUri, mode: LaunchMode.externalApplication);
        }
      }
    } else {
      // Android: Keep try/catch approach for geo URIs
      try {
        await launchUrl(geoUri, mode: LaunchMode.externalApplication);
      } catch (e) {
        log('Could not launch map: $e');
      }
    }
  }
  ```

- **Key Insights**
  - **Platform-Specific Behavior**: Realized the importance of understanding each platform's unique handling of external app integration in cross-platform development. Experiences from one platform should not be directly applied to another
  - **Importance of canLaunchUrl() on iOS**: Unlike the reliability issues on Android, it's an essential pre-check tool on iOS
  - **Debugging Silent Failures**: Learned approaches for troubleshooting issues where no exceptions occur

- **Results**  
  Resolved issue and achieved reliable map app integration on both platforms: iOS users get Naver Map when available, with Apple Maps fallback, while Android users can choose from their installed map applications

<br><br><br>