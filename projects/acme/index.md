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
    <a href="/projects/acme">EN</a>
    <a href="/kr/projects/acme">KR</a>
  </div>

<span id="nav-menu-toggle">☰</span>
  <div id="nav-links">
    <!-- Navigation Links will be dynamically populated -->
  </div>
</div>

<div style="position: relative; margin-bottom: 40px;">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=300&section=header&fontSize=45&animation=fadeIn&fontAlignY=38&desc=&descAlignY=51&descAlign=62" alt="Header" style="display: block; width: 100%; height: auto; margin: 0; padding: 0; border-radius: 8px;" />

<div style="position:absolute;left:40px;bottom:-10px;width:80px;height:80px;background:white;border-radius:20px;display:flex;align-items:center;justify-content:center;box-shadow:0 2px 6px rgba(0,0,0,0.15);">
<img src="../../images/acme/app_icon.png" alt="Project Icon" style="max-width:100%;max-height:100%;object-fit:contain;" />
</div>

</div>

# ACME - Field service management app

## 📝 Overview
**📌 App Introduction:** Android field management app integrating custom calendar functionality, offline capabilities, and navigation features  
**🕒 Duration:** May 2021 ~ June 2021  
**📱 Platform:** Native Android app  
**👥 Team Size:** 1 developer  
**💼 Role:** Full Android app development  
**🛠️ Key Technologies:** `Android` `Kotlin` `MVVM` `Jetpack` `Room` `Calendar Provider API` `Data Binding` `WebView`  
**🔗 GitHub:** [daehan-lim/acme](https://github.com/daehan-lim/acme)

<div style="display: flex; overflow-x: auto; border: 2px solid #ccc; padding: 6px; border-radius: 8px;">
  <img src="../../images/acme/dashboard.png" width="240" style="margin-right: 5px;" alt="ACME app dashboard screen" />
  <img src="../../images/acme/ticket_details.png" width="240" style="margin-right: 5px;" alt="ACME app ticket details screen" />
  <img src="../../images/acme/calendar.png" width="240" style="margin-right: 5px;" alt="ACME app calendar screen" />
  <img src="../../images/acme/calendar_sync.png" width="240" style="margin-right: 5px;" alt="ACME app calendar sync screen" /> 
  <img src="../../images/acme/login.png" width="240" style="margin-right: 5px;" alt="ACME app login screen" />
  <img src="../../images/acme/signup.png" width="240" style="margin-right: 5px;" alt="ACME app signup screen" />
  <img src="../../images/acme/edit.png" width="240" style="margin-right: 5px;" alt="ACME app edit screen" />
  <img src="../../images/acme/maps.png" width="240" alt="ACME app maps screen" />
</div>
<span style="display: block; height: 11px;"></span>

## 🛠️ Tech Stack

[![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?logo=kotlin&logoColor=white&style=for-the-badge)](https://kotlinlang.org)
[![MVVM](https://img.shields.io/badge/MVVM-FF5252?style=for-the-badge)](https://developer.android.com/topic/architecture)
[![Room](https://img.shields.io/badge/Room-00796B?logo=android&logoColor=white&style=for-the-badge)](https://developer.android.com/training/data-storage/room)
[![Jetpack](https://img.shields.io/badge/Jetpack-F57C00?logo=android&logoColor=white&style=for-the-badge)](https://developer.android.com/jetpack)
[![Coroutines](https://img.shields.io/badge/Coroutines-7F52FF?logo=kotlin&logoColor=white&style=for-the-badge)](https://kotlinlang.org/docs/coroutines-overview.html)
[![Navigation](https://img.shields.io/badge/Navigation-AB47BC?logo=android&logoColor=white&style=for-the-badge)](https://developer.android.com/guide/navigation)
[![Material Dialogs](https://img.shields.io/badge/Material%20Dialogs-795548?style=for-the-badge)](https://github.com/afollestad/material-dialogs)
[![Calendar View](https://img.shields.io/badge/Calendar%20View-F4511E?style=for-the-badge)](https://github.com/kizitonwose/CalendarView)
[![ViewBinding](https://img.shields.io/badge/ViewBinding-7CB342?style=for-the-badge)](https://developer.android.com/topic/libraries/view-binding)
[![DataBinding](https://img.shields.io/badge/DataBinding-7CB342?style=for-the-badge)](https://developer.android.com/topic/libraries/data-binding)
[![Google Maps](https://img.shields.io/badge/Google%20Maps-2196F3?style=for-the-badge)](https://maps.google.com)
[![Lottie](https://img.shields.io/badge/Lottie-029C87?logo=lottie&logoColor=white&style=for-the-badge)](https://airbnb.io/lottie/#/)
[![CardView](https://img.shields.io/badge/CardView-FF6F61?logo=android&logoColor=white&style=for-the-badge)](https://developer.android.com/jetpack/androidx/releases/cardview)
[![LiveData](https://img.shields.io/badge/LiveData-3F51B5?style=for-the-badge)](https://developer.android.com/topic/libraries/architecture/livedata)
[![Material Design](https://img.shields.io/badge/Material%20Design-4285F4?logo=material-design&logoColor=white&style=for-the-badge)](https://material.io/design)

## 📋 Project Structure

```
├── database/                         # Room database layer
│   ├── AcmeDatabase.kt               # Main database configuration
│   ├── dao/                          # Data access objects
│   │   ├── TicketDao.kt              # Ticket CRUD operations
│   │   └── UserDao.kt                # User authentication operations
│   └── model/                        # Database entities
│       ├── Ticket.kt                 # Service ticket data model
│       └── User.kt                   # User account data model
├── repository/                       # Repository pattern implementation
│   ├── TicketRepository.kt           # Ticket data abstraction layer
│   └── UserRepository.kt             # User data abstraction layer
├── ui/                               # MVVM architecture-based UI layer
│   ├── DbAccessViewModel.kt          # Common ViewModel base class
│   ├── login/                        # Authentication features
│   │   ├── LoginActivity.kt          # Login screen
│   │   ├── SignUpActivity.kt         # Registration screen
│   │   ├── LoginSignupViewModel.kt   # Authentication business logic
│   │   └── LoginSignUpFormState.kt   # Form validation state management
│   ├── dashboard/                    # Main dashboard
│   │   ├── MainActivity.kt           # Ticket list and main features
│   │   ├── MainViewModel.kt          # Dashboard data management
│   │   └── TicketsAdapter.kt         # RecyclerView adapter
│   ├── newticket/                    # Ticket creation feature
│   │   ├── NewTicketActivity.kt      # New ticket registration screen
│   │   ├── NewTicketViewModel.kt     # Ticket creation logic
│   │   └── ManageTicketFormState.kt  # Form validation and state management
│   ├── editticket/                   # Ticket modification feature
│   │   ├── EditTicketActivity.kt     # Ticket editing screen
│   │   └── EditTicketViewModel.kt    # Ticket modification logic
│   ├── workticket/                   # Ticket detail management
│   │   ├── WorkTicketActivity.kt     # Ticket details and work screen
│   │   └── OverviewFragment.kt       # Ticket overview fragment
│   ├── calendar/                     # Schedule management feature
│   │   ├── CalendarActivity.kt       # Calendar view screen
│   │   ├── CalendarViewModel.kt      # Schedule data management
│   │   ├── EventsAdapter.kt          # Event list adapter
│   │   └── Extensions.kt             # Calendar extension functions
│   └── directions/                   # Maps and navigation
│       └── GetDirectionsActivity.kt  # WebView-based Google Maps integration
├── model/                            # Business models
│   └── DueTicket.kt                  # Due ticket model
└── util/                             # Utilities and common features
    ├── BindingUtils.kt               # Data binding adapters
    ├── CalendarUtil.kt               # Device calendar integration
    └── Util.kt                       # Common utility functions
```

## 🌟 Implementation Details
- Implemented offline service ticket management app with responsive design
- Developed interactive calendar with custom event visualization and Android Calendar Provider API integration for syncing events to device calendar
- Built ticket location address search and navigation functionality through embedded Google Maps integration via WebViews
- Created user registration and authentication flows with input validation and error feedback

## 🚀 Results and Impact
- 20% reduction in ticket location search and navigation time
- Improved task scheduling efficiency through calendar integration

<br><br><br>