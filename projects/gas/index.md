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
    <a href="/projects/gas">EN</a>
    <a href="/kr/projects/gas">KR</a>
  </div>

<span id="nav-menu-toggle">☰</span>
  <div id="nav-links">
    <!-- Navigation Links will be dynamically populated -->
  </div>
</div>

<div style="position: relative; margin-bottom: 40px;">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=300&section=header&fontSize=45&animation=fadeIn&fontAlignY=38&desc=&descAlignY=51&descAlign=62" alt="Header" style="display: block; width: 100%; height: auto; margin: 0; padding: 0; border-radius: 8px;" />

<div style="position:absolute;left:40px;bottom:-10px;width:80px;height:80px;background:#fafafa;border-radius:20px;display:flex;align-items:center;justify-content:center;box-shadow:0 2px 6px rgba(0,0,0,0.15);">
<img src="../../images/gas/app_icon.png" alt="Project Icon" style="max-width:90%;max-height:90%;object-fit:contain;" />
</div>

</div>

# Gas Consumption Manager

## 📝 Overview
**📌 App Introduction:** Android application automating manual gas usage management for Cuba's national Manufactured Gas Company  
**🕒 Duration:** February 20, 2021 ~ March 18, 2021 (1 month)  
**📱 Platform:** Native Android app  
**🏢 Company:** Desoft (Cuba's national software development company)  
**👥 Team Size:** 1 developer  
**💼 Role:** Full Android app development  
**🛠️ Key Technologies:** `Android` `Kotlin` `Coroutines` `MVVM` `Room` `VideoView` `Jetpack` `Material Design` `Data Binding` `Navigation` `MPAndroidChart`  
**🔗 GitHub:** [daehan-lim/gas-consumption-manager](https://github.com/daehan-lim/gas-consumption-manager)

<div style="display: flex; overflow-x: auto; border: 2px solid #ccc; padding: 6px; border-radius: 8px;">
  <img src="../../images/gas/main.png" width="240" style="margin-right: 5px;" alt="Gas consumption manager main screen" />
  <img src="../../images/gas/calendar.png" width="240" style="margin-right: 5px;" alt="Gas consumption manager calendar screen" />
  <img src="../../images/gas/chart.png" width="240" style="margin-right: 5px;" alt="Gas consumption manager chart screen" />
  <img src="../../images/gas/filter.png" width="240" style="margin-right: 5px;" alt="Gas consumption manager filter screen" />
  <img src="../../images/gas/offices.png" width="240" style="margin-right: 5px;" alt="Gas consumption manager offices screen" />
  <img src="../../images/gas/video.png" width="240" alt="Gas consumption manager video screen" />
</div>
<span style="display: block; height: 11px;"></span>

## 📖 Project Background

Cuba's national Manufactured Gas Company faced operational inefficiencies due to their manual gas consumption recording and billing calculation. All procedures from gas meter readings to billing calculations required manual work, leading to time-intensive operations and increased risk of calculation errors. Additionally, customers lacked systematic educational resources for gas meter reading methods and had limited access to customer support. This project developed a comprehensive mobile solution to automate usage calculations, provide educational resources through a video guide, and implement offline-first design for reliable operation.

## 📋 Project Structure

```
├── features/                           # Feature-based modular structure
│   ├── consumption/                    # Gas consumption calculation feature
│   │   ├── ConsumptionFragment.kt      # Consumption input and calculation UI
│   │   ├── ConsumptionViewModel.kt     # Consumption calculation business logic
│   │   └── ConsumptionViewModelFactory.kt
│   ├── history/                        # Usage history and chart analytics
│   │   ├── HistoryActivity.kt          # Chart-based analysis screen
│   │   ├── HistoryViewModel.kt         # Chart data processing logic
│   │   └── HistoryViewModelFactory.kt
│   ├── offices/                        # Branch office contact directory
│   │   ├── ComercialOfficesFragment.kt # Branch office list UI
│   │   ├── ComercialOfficesAdapter.kt  # RecyclerView adapter
│   │   └── ComercialOfficesViewModel.kt
│   ├── readcounter/                    # Meter reading guide
│   │   ├── ReadCounterFragment.kt      # Video guide screen
│   │   └── ReadCounterViewModel.kt
│   ├── about/                          # App information and contacts
│   │   └── AboutActivity.kt
│   └── splash/                         # Splash screen
│       └── SplashActivity.kt
├── database/                           # Room database layer
│   ├── Consumption.kt                  # Consumption data entity
│   ├── ConsumptionDao.kt               # Data access object
│   └── ConsumptionDatabase.kt          # Database configuration
├── model/                              # Data models
│   └── ComercialOffice.kt              # Branch office information model
├── util/                               # Utility classes
│   ├── BindingUtils.kt                 # Data binding adapters
│   └── Util.kt                         # Common utility functions
└── MainActivity.kt                     # Main activity and navigation
```

## 🌟 Implementation Details

### Room Database-based Offline Data Management and Storage
- **Implemented MVVM architecture with Repository pattern**
  - Created data access layer abstraction through `ConsumptionDao` to separate business logic
  - Used `Coroutines` and `suspend` functions for asynchronous database operations, preventing UI thread blocking
  - Built reactive UI with `LiveData` and `ViewModel` for lifecycle-aware data binding
  - Applied Singleton pattern with `fallbackToDestructiveMigration()` for stable database management

- **Implemented Efficient Data CRUD Operations**
  - Implemented monthly consumption retrieval, yearly data filtering, and automatic integration of latest meter readings
  - Ensured data continuity by automatically loading previous month's meter readings

### Automated Gas Usage Calculation with Real-Time Validation
- **Real-time Input Validation and Error Prevention**
  - Implemented immediate error alerts and input blocking when current meter readings are lower than previous readings
  - Created real-time field validation UI using `TextInputLayout`'s `errorEnabled` property
  - Provided instant feedback for missing required fields, minimizing user input errors

- **Developed automated billing calculation system**
  - Implemented consistent fee calculation using `PAYMENT_COEFFICIENT` constant (2.5)
  - Enabled immediate result verification through real-time conversion between gas usage (㎥) and fees (pesos)
  - Presented calculation results through formatted HTML display and `AlertDialog` interface

### Interactive Data Visualization Using MPAndroidChart
- **Built annual and monthly consumption analysis charts**
  - Implemented `BarChart` visualization for monthly gas consumption patterns with animation effects, enhancing user experience
  - Added peso/㎥ unit conversion filtering for multi-perspective data analysis

- **Created responsive chart interface**
  - Implemented responsive chart design that adapts to device orientation with optimized label spacing
  - Integrated `MonthPickerDialog` for intuitive year selection interface

### VideoView-based Educational Video Guide
- **Developed full-screen video player for meter reading tutorial**
  - Customized `MediaController` with full-screen button and screen rotation controls
  - Implemented immersive viewing experience with automatic `SystemUI` hiding during orientation changes
  - Built video playback position saving and restoration for uninterrupted user experience

- **Lifecycle-aware Media Management**
  - Prevented memory leaks through proper video resource management across `onStart()`, `onStop()`, and `onPause()` lifecycle events
  - Added automatic portrait mode restoration and placeholder screen display when video completes
  - Used `raw` resources for offline video playback, eliminating network dependencies

### Customer Support Directory with Direct Communication
- **Built branch office contact directory**
  - Integrated contact information to streamline customer inquiry processes
  - Implemented direct calling functionality using `Intent.ACTION_CALL` and SMS via `Intent.ACTION_SENDTO`
  - Added dynamic `CALL_PHONE` permission handling with fallback to dialer app when permission is denied
  - Built reusable view binding logic using `@BindingAdapter`

### User Experience Optimization & Accessibility Improvements
- Built Bottom Navigation with Fragment-based screen transitions
  - Automated navigation state management using `setupWithNavController()`
  - Added exit confirmation dialog through `onBackPressed()` override
- Designed consistent Toolbar-based action bar
  - Included option menus for quick access to features like History and About
- Applied custom typography using `segoe_ui` and `seguisb` fonts for distinctive branding
- Designed splash screen with company logo and brand colors
- Integrated social media platform links for Facebook, Instagram, Twitter, Telegram, LinkedIn
- Enabled access to external resources through browser integration with `Intent.ACTION_VIEW`

### Development Best Practices and Code Quality
- **Applied Data Binding and ViewBinding**
  - Ensured type safety between XML layouts and Kotlin code while eliminating `findViewById()` calls
  - Implemented declarative UI updates using `@{viewModel.property}` syntax
  - Used `executePendingBindings()` for immediate binding processing to prevent UI flickering

## 🚀 Results and Impact
- **70% reduction in operational times**: Significantly reduced gas company's operational times through transition from manual to automated gas billing calculations
- **Offline-first design**: All core features operate without network connectivity through Room local database
- **Enhanced user satisfaction**: Video tutorials and intuitive UI/UX improved meter reading comprehension
- **Streamlined customer support**: Integrated branch office contacts simplified customer inquiry handling and improved accessibility

<br><br><br>