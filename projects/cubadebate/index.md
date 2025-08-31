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
    <a href="/projects/cubadebate">EN</a>
    <a href="/kr/projects/cubadebate">KR</a>
  </div>

<span id="nav-menu-toggle">☰</span>
  <div id="nav-links">
    <!-- Navigation Links will be dynamically populated -->
  </div>
</div>

<div style="position: relative; margin-bottom: 40px;">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=300&section=header&fontSize=45&animation=fadeIn&fontAlignY=38&desc=&descAlignY=51&descAlign=62" alt="Header" style="display: block; width: 100%; height: auto; margin: 0; padding: 0; border-radius: 8px;" />

<img src="../../images/cubadebate/categories.png" alt="Project Icon" style="position: absolute; left: 40px; bottom: -10px; width: 80px; height: 80px; border-radius: 12px; border: 4px solid white; object-fit: cover;" />

</div>

# Cubadebate News App

## 📝 Overview
**📌 App Introduction:** News reader app with personalized content delivery and offline storage capability  
**🕒 Duration:** March 15, 2021 ~ June 30, 2021 (3.5 months)  
**📱 Platform:** Native Android app  
**🏢 Company:** Desoft (Cuba's national software development company)  
**👥 Team Size:** 1 developer  
**💼 Role:** UI/UX design and complete Android app development  
**🛠️ Key Technologies:** `Android` `Kotlin` `Coroutines` `MVVM` `Room` `Retrofit` `Moshi` `Navigation` `Material Design` `Glide` `Lottie` `ViewBinding`  
**🔗 GitHub:** [daehan-lim/cubadebate-app](https://github.com/daehan-lim/cubadebate-app)

<div class="image-row">
  <!--
  <a href="https://www.youtube.com/watch?v=4SEpMDPFkHw" target="_blank" class="linked-image">
    <img src="../images/gas/main.png" alt="Watch the Video" class="image-item" />
  </a>
  -->
  <img src="../../images/cubadebate/news_feed.svg" alt="Cubadebate news feed screen" class="image-item" />
  <img src="../../images/cubadebate/news_article.svg" alt="Cubadebate news article screen" class="image-item" />
  <img src="../../images/cubadebate/replies.png" alt="Cubadebate replies screen" class="image-item" />
  <img src="../../images/cubadebate/categories.png" alt="Cubadebate categories screen" class="image-item" />
  <img src="../../images/cubadebate/topics.png" alt="Cubadebate topics screen" class="image-item" />
  <img src="../../images/cubadebate/sms.png" alt="Cubadebate SMS screen" class="image-item" />
  <img src="../../images/cubadebate/search.svg" alt="Cubadebate search screen" class="image-item" />
  <img src="../../images/cubadebate/saved.png" alt="Cubadebate saved articles screen" class="image-item" />
</div>
<span style="display: block; height: 11px;"></span>

## 📖 Project Background

- Identified the need to develop a mobile-optimized news app to overcome Cuba's challenging network environment (high data costs, unstable connections) and the limitations of the existing website-based news platform
- The existing website required users an average of over 2 minutes to find articles of interest, with no way to customize content based on user preferences
- Planned a transition to an native Android app that could provide data usage savings, offline accessibility, and personalization features
- Aimed to help Cuban users access relevant news more easily through intuitive, accessible mobile UX including offline storage and voice support

## 🛠️ Tech Stack

![Kotlin](https://img.shields.io/badge/Kotlin-1.5.0-blue.svg)
![MVVM](https://img.shields.io/badge/Architecture-MVVM-brightgreen.svg)
![Room](https://img.shields.io/badge/Room-2.3.0-green.svg)
![Coroutines](https://img.shields.io/badge/Coroutines-1.5.0-blue.svg)
![Retrofit](https://img.shields.io/badge/Retrofit-2.9.0-orange.svg)
![Moshi](https://img.shields.io/badge/Moshi-1.11.0-red.svg)
![Material Design](https://img.shields.io/badge/Material%20Design-1.3.0-purple.svg)
![Navigation](https://img.shields.io/badge/Navigation-2.3.5-yellow.svg)
![ViewBinding](https://img.shields.io/badge/ViewBinding-Enabled-success.svg)
![DataBinding](https://img.shields.io/badge/DataBinding-Enabled-success.svg)
![Glide](https://img.shields.io/badge/Glide-4.11.0-blue.svg)
![JSoup](https://img.shields.io/badge/JSoup-1.13.1-green.svg)
![Material Dialogs](https://img.shields.io/badge/Material%20Dialogs-3.3.0-purple.svg)

## 📋 Project Structure

```
├── database/                        # Local database related classes
│   ├── CubadebateDatabase.kt        # Room database main class
│   ├── converters/                  # Data type converters
│   ├── dao/                         # Data access objects
│   │   ├── PostDao.kt               # Post-related data access
│   │   ├── RecentCategoryDao.kt     # Recent category data access
│   │   └── TagDao.kt                # Tag-related data access
│   └── model/                       # Database entity models
│       ├── post/                    # Post-related entities
│       │   ├── DatabasePost.kt      # Post main entity
│       │   ├── DatabaseCategory.kt  # Category entity
│       │   └── ...(other post entities)
│       ├── savedpost/               # Saved post entities
│       │   ├── SavedPost.kt         # Saved post main entity
│       │   ├── SavedCategory.kt     # Saved post category
│       │   └── ...(other saved post entities)
│       ├── ...(other entities)
│
├── model/                           # Data model classes
│   ├── api/                         # API response models
│   │   ├── comment/                 # Comment API models
│   │   │   ├── Content.kt           # Comment content
│   │   │   └── ResponseComment.kt   # Comment response model
│   │   ├── post/                    # Post API models
│   │   │   ├── NetworkPost.kt       # Network post model
│   │   │   └── ...(other API models)
│   ├── categories/                  # Category-related models
│   │   └── MyCategoriesGridViewItem.kt
│   ├── comment/                     # Comment domain models
│   │   └── Comment.kt               # Comment information
│   └── post/                        # Post domain models
│       ├── Post.kt                  # Post main model
│       ├── Category.kt              # Category model
│       └── ...(other post models)
│
├── network/                         # Network communication classes
│   └── CubadebateApiService.kt      # Retrofit API service interface
│
├── repository/                      # Data repository (Repository pattern)
│   ├── PostRepository.kt            # Post data management
│   ├── RecentCategoryRepository.kt  # Recent category data management
│   └── TagRepository.kt             # Tag data management
│
├── ui/                              # User interface classes
│   ├── CoroutineBaseViewModel.kt    # Coroutine-based base view model
│   ├── PostsViewModel.kt            # Common post view model
│   ├── HeadingsAdapter.kt           # Post list adapter
│   ├── EndlessRecyclerViewScrollListener.kt  # Infinite scroll listener

│   ├── main/                        # Main screen classes
│   │   ├── MainActivity.kt          # Main activity
│   │   ├── MainActivityViewModel.kt # Main activity view model
│   ├── categories/                  # Category screens
│   │   ├── BaseCategoryFragment.kt  # Category base fragment
│   │   ├── HomeFragment.kt          # Home fragment
│   ├── details/                     # Post detail screen
│   ├── comments/                    # Comment-related screens
│   │   ├── CommentsActivity.kt      # Comments activity
│   │   ├── CommentsFragment.kt      # Comments fragment
│   │   ├── RepliesFragment.kt       # Comment replies fragment
│   │   └── ...(ViewModels and other classes)
│   ├── search/                      # Search screens
│   ├── saved/                       # Saved posts screen
│   ├── forme/                       # Personalized recommendation screen
│   │   ├── ForMeFragment.kt         # Recommendation main fragment
│   │   ├── MyCategoriesFragment.kt  # My categories fragment
│   │   ├── MyTopicsFragment.kt      # My topics fragment
│   │   └── ...(ViewModels and other classes)
│   │
│   ├── headingspertag/              # Posts by tag screen
│   ├── subscription/                # Subscription screens
│   └── settings/                    # Settings screens
│       ├── categories/              # Category management
│       └── topics/                  # Topic management
│
└── util/                            # Utility classes and helper functions
    ├── ActivityUtils.kt             # Activity utilities
    ├── BindingUtils.kt              # Data binding utilities
    ├── MappingUtils.kt              # Data mapping utilities
    ├── PostUtils.kt                 # Post utilities
    ├── PreferenceManager.kt         # Settings management utilities
    └── Util.kt                      # General utility functions
```

## 🌟 Implementation & Achievements
- Built customizable news feed system with dynamic category/topic selection and real-time management by analyzing existing website usage patterns and user feedback 
  - Implemented real-time topic management system with dynamic search, post count display, and automatic list reordering
  - Reduced average content discovery time **by 75%** (from 2 minutes to 30 seconds)
- Implemented robust offline storage for articles and images using Room DB, reducing data usage by **up to 30%**
- Integrated in-article text search, text-to-speech (TTS), and voice recognition features
- Implemented real-time article search/filtering, multi-level commenting interface, and infinite scroll, improving user engagement
- Built navigation drawer that tracks recently visited categories for easy navigation
- Designed Material Design-based UI with smooth animations
- Improved accessibility **by 40%** compared to the website

## 🧭 Technical Decision-Making

**1. Offline Storage Architecture Selection**

- **Requirements**  
  Users needed reliable offline access to news articles even in unstable network environments

- **Decision**  
  Implemented robust offline storage using `Room Database`
  - Leveraged SQLite's reliability and Android Jetpack's type safety for stable data operations with compile-time verification
  - Built architecture to store article text, content, and images locally
  - Enabled complete offline access to user-selected content through bookmark functionality

```kotlin
@Entity(tableName = "posts")
data class DatabasePost(
    @PrimaryKey val id: Long,
    val title: String,
    val content: String,
    val imageUrl: String?,
    val publishedDate: String,
    val isSaved: Boolean = false
)
```

**2. MVVM Architecture Implementation**

- **Requirements**  
  Needed systematic management of complex news data flows and UI states while efficiently integrating network and local data sources

- **Decision**  
  Built layered architecture combining `MVVM` with `Repository` pattern
  - **Separation of concerns**: Clear responsibility division across View-ViewModel-Repository structure improved code maintainability
  - **LiveData utilization**: Lifecycle-aware observable data prevented memory leaks and ensured automatic UI updates
  - **Repository pattern**: Abstracted network and local database access following Single Source of Truth principle for unified data access logic management

```kotlin
class PostRepository(private val database: CubadebateDatabase) {
    suspend fun getPosts(categoryId: Long?): MutableList<Post> {
        return withContext(Dispatchers.IO) {
            try {
                // Attempt to fetch latest data from network
                val networkPosts = when(categoryId) {
                    null -> CubadebateApi.retrofitService.getPostsAsync()
                    else -> CubadebateApi.retrofitService.getPostsByCategoryAsync(categoryId)
                }.await()
                
                // Save to local DB and return
                networkPosts.map { it.mapToPost() }
            } catch (e: Exception) {
                // Return local data on network failure
                getPostsFromDb(categoryId)
            }
        }
    }
}
```

## 🌱 Problem Solving

**1. User-Centric Content Discovery Enhancement**

- **Problem**  
  Users found it difficult to freely explore or subscribe to news on topics of interest through the existing website, with no way to customize content based on user preferences

- **Analysis**
  - Analyzed website usage patterns and user feedback, identifying that finding specific topic content took an average of over 2 minutes
  - Designed an interface enabling users to browse all topics at once with real-time search capabilities
  - Implemented intuitive UI showing post counts by topic with selected topics automatically moving to the top
  - Developed personalized feed system using `RecyclerView` and `Room Database` to aggregate news from user-selected topics

- **Results**  
  Reduced average content discovery time to 30 seconds, achieving approximately **75% improvement** over the website, while significantly enhancing platform usability with personalized content features

## 🎞️ Video
<div align="center"> 
<a href="https://www.youtube.com/watch?v=4SEpMDPFkHw">
  <img src="../../images/cubadebate/video_preview.png" alt="Watch the Video" width="230" />
</a>
</div>
<br>
