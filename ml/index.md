<!--suppress CssUnusedSymbol, JSUnusedLocalSymbols -->
<style>
/* Navigation Menu Styles */
#nav-menu {
  padding: 19px 0; /* Navbar height */
}

#nav-menu a {
  margin: 0 15px;
  font-size: 14px;
}

</style>

<div id="nav-menu">
  <div style="margin-left: 20px;">
  </div>

<span id="nav-menu-toggle">☰</span>
  <div id="nav-links">
    <!-- Navigation Links will be dynamically populated -->
  </div>
</div>

# Penjan Antonio Eng Lim

[![Typing SVG](https://readme-typing-svg.herokuapp.com?color=%230077B5&size=24&width=600&height=45&lines=Welcome+to+my+portfolio!;I'm+Penjan%2C+innovating+digital+solutions)](https://git.io/typing-svg)

<div align="center"> 
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

## 👋 About Me
Innovative machine learning engineer with expertise in deep learning architectures and privacy-preserving algorithms, combining academic research with hands-on development of cutting-edge AI solutions. My technical approach emphasizes creating robust systems that balance high performance with interpretability, particularly in NLP and federated learning environments. Driven by a commitment to developing ethical AI applications, I leverage my versatile programming skills and problem-solving abilities to transform complex data challenges into practical, impactful solutions for real-world implementation.

## 📂 Projects Overview

**Machine Learning Models**
- [Privacy-Preserving Federated Random Forest](#privacy-preserving-federated-random-forest) - Privacy-preserving distributed learning system (2023)<a href="https://arxiv.org/abs/2407.19193" style="color: #21427D; font-size: 20px; text-decoration: none;">&thinsp;&thinsp;⎆</a>
- [RoBERTa News Classification](#roberta-news-classification) - Enhanced topic classification with synthetic data (2024)<a href="https://github.com/daehan-lim/roberta-sport-news-classifier" style="color: #21427D; font-size: 20px; text-decoration: none;">&thinsp;&thinsp;⎆</a>
- [Medical Data Classifier](#medical-data-classifier) - Patient mortality prediction system (2023)<a href="https://github.com/daehan-lim/associative-classifier-mortality-prediction" style="color: #21427D; font-size: 20px; text-decoration: none;">&thinsp;&thinsp;⎆</a>
- [Information Retrieval System](#information-retrieval-system) - Document indexing and search system (2024)<a href="../assets/information_retrieval_report.pdf" style="color: #21427D; font-size: 20px; text-decoration: none;">&thinsp;&thinsp;⎆</a>

**Mobile Applications**
- [Cubadebate News Reader](#cubadebate-news-reader) - News app with personalized content delivery (2021)<a href="https://github.com/daehan-lim/cubadebate-app" style="color: #21427D; font-size: 20px; text-decoration: none;">&thinsp;&thinsp;⎆</a>
- [Gas Consumption Manager](#gas-consumption-manager) - National utility tracking system (2021)<a href="https://github.com/daehan-lim/gas-consumption-manager" style="color: #21427D; font-size: 20px; text-decoration: none;">&thinsp;&thinsp;⎆</a>
- [ACME App](#acme-app) - Service ticket management solution (2021)<a href="https://github.com/daehan-lim/acme" style="color: #21427D; font-size: 20px; text-decoration: none;">&thinsp;&thinsp;⎆</a>
- [Yellow Pages](#yellow-pages) - Enterprise directory with offline mapping (2020)<a href="https://github.com/daehan-lim/cuban-yellow-pages" style="color: #21427D; font-size: 20px; text-decoration: none;">&thinsp;&thinsp;⎆</a>

## 🔬 Machine Learning Models

### [Privacy-Preserving Federated Random Forest](https://arxiv.org/abs/2407.19193)
*Privacy-preserving distributed learning system for collaborative model training (2023)*

<img src="../images/random_forest.png" width="650" alt="Training process for the privacy-preserving federated random forest model">

**Overview:**

- Designed and implemented a federated learning system for random forests enabling privacy-preserving distributed model training across multiple clients
- Implemented parallel processing pipeline using Python's ProcessPoolExecutor for efficient multi-client simulation and simultaneous model training, reducing training time by 60%
- Introduced incremental learning mechanism that enables efficient integration of new clients without full model retraining, improving system scalability
- Demonstrated system effectiveness through extensive testing across 7 benchmark datasets with sizes ranging up to 88,000 samples and 54 features, achieving a 10% performance improvement compared to the baseline approach
- Published research in [Expert Systems with Applications](https://www.sciencedirect.com/science/article/pii/S0957417424016099) (SCIE Journal) and resulted in patent filing (Appl. No. 10-2024-0001659)
- **Tech Stack**: Python, NumPy, Pandas, scikit-learn, Matplotlib, multiprocessing, Graphviz

[🔗 View Details](https://arxiv.org/abs/2407.19193)

---

### [RoBERTa News Classification](https://github.com/daehan-lim/roberta-sport-news-classifier)
*Enhanced topic classification model with synthetic data augmentation (2024)*

<img src="../images/roberta_architecture.png" width="350" alt="RoBERTa model architecture">

**Overview:**
- Developed machine learning model for classifying sports news articles into 5 distinct categories using [RoBERTa](https://huggingface.co/docs/transformers/en/model_doc/roberta) and [BBC Sport dataset](http://mlg.ucd.ie/datasets/bbc.html)
- Augmented limited training data using GPT-4 generated articles and prompt engineering techniques, improving classification accuracy to 99.5%
- Employed zero-shot learning strategy to enhance diversity and versatility of the LLM generated articles
- Executed comprehensive experiments evaluating model performance under various data configurations and training conditions
- Developed and deployed web application using Streamlit, enabling real-time article classification with detailed performance visualizations
- **Tech Stack**: Python, PyTorch, Hugging Face Transformers, GPT-4, Streamlit

[🔗 View on GitHub](https://github.com/daehan-lim/roberta-sport-news-classifier)

---

### [Medical Data Classifier](https://github.com/daehan-lim/associative-classifier-mortality-prediction)
*Novel classification system for patient mortality prediction using electronic health records (2023)*

<img src="../images/associative_classifier.png" width="420px" alt="Associative classifier - rule generation algorithm">

**Overview:**
- Developed custom associative classifier tailored for unbalanced healthcare datasets
- Generated interpretable rules for medical decision-making, enabling healthcare experts to validate model predictions
- Implemented efficient rule-pruning strategy, reducing rule set by 80% for enhanced model interpretability
- Achieved superior performance metrics compared to traditional classifiers on real-world hospital data
- **Tech Stack**: Python, NumPy, Pandas, scikit-learn, Jupyter

[🔗 View on GitHub](https://github.com/daehan-lim/associative-classifier-mortality-prediction)

---

### [Information Retrieval System](../assets/information_retrieval_report.pdf)
*Efficient implementation of Boolean and ranked document retrieval (2024)*

**Overview:**
- Reduced document processing time by 65% compared to sequential search by implementing SPIMI-based inverted indexing
- Enhanced search precision through Boolean operator (AND, OR, NOT) based filtering
- Implemented ranked retrieval using TF-IDF weighting and cosine similarity, improving search result relevance
- Achieved 0.3 second average search response time for 466 English documents
- Implemented system with optimized memory usage of 2.5MB
- **Tech Stack**: Python, NLTK, SpaCy, NumPy, contractions

[🔗 View Details](../assets/information_retrieval_report.pdf)

---

## 📱 Mobile Applications

### [Cubadebate News Reader](https://github.com/daehan-lim/cubadebate-app)
*Feature-rich news reader app enabling personalized content delivery and comprehensive offline access (2021)*

<div style="display: flex; overflow-x: auto; border: 2px solid #ccc; padding: 6px; border-radius: 8px;">
  <img src="../images/cubadebate/news_feed.svg" width="240" style="margin-right: 5px;" alt="Cubadebate news feed screen" />
  <img src="../images/cubadebate/news_article.svg" width="240" style="margin-right: 5px;" alt="Cubadebate news article screen" />
  <img src="../images/cubadebate/replies.png" width="240" style="margin-right: 5px;" alt="Cubadebate replies screen" />
  <img src="../images/cubadebate/categories.png" width="240" style="margin-right: 5px;" alt="Cubadebate categories screen" />
  <img src="../images/cubadebate/topics.png" width="240" style="margin-right: 5px;" alt="Cubadebate topics screen" />
  <img src="../images/cubadebate/sms.png" width="240" style="margin-right: 5px;" alt="Cubadebate SMS screen" />
  <img src="../images/cubadebate/search.svg" width="240" style="margin-right: 5px;" alt="Cubadebate search screen" />
  <img src="../images/cubadebate/saved.png" width="240"  alt="Cubadebate saved articles screen" />
</div>
<br>

<!--
**Video Walkthrough**
<div style="border: 4px solid #ccc; border-radius: 12px; padding: 4px; width: fit-content; margin: 0 auto;">
  <iframe width="236" height="486" src="https://www.youtube.com/embed/4SEpMDPFkHw" frameborder="0" allowfullscreen></iframe>
</div>
<br><br>
-->

**Overview:**
- Built customizable news feed system with dynamic category and topic selection interfaces, enabling personalized content delivery
- Implemented offline caching for bookmarking full articles including images, reducing data usage by up to 30%
- Designed real-time topic management system with dynamic search, post count display, and automatic list reordering, reducing average content discovery time from 2 minutes to 30 seconds
- Integrated in-article text search, text-to-speech capability and voice recognition capabilities, increasing content accessibility by 40%
- Built multi-level commenting interface, infinite scroll with efficient data loading, and SMS subscriptions, improving user engagement
- **Tech Stack:** Android, Kotlin, MVVM, Room, Retrofit, Moshi, Navigation, Material Design, Glide, JSoup, Coroutines, ViewBinding

[🔗 View on GitHub](https://github.com/daehan-lim/cubadebate-app)

---

### [Gas Consumption Manager](https://github.com/daehan-lim/gas-consumption-manager)
*National utility tracking system for automated consumption management (2021)*

<div style="display: flex; overflow-x: auto; border: 2px solid #ccc; padding: 6px; border-radius: 8px;">
  <img src="../images/gas/main.png" width="240" style="margin-right: 5px;" alt="Gas consumption manager main screen" />
  <img src="../images/gas/calendar.png" width="240" style="margin-right: 5px;" alt="Gas consumption manager calendar screen" />
  <img src="../images/gas/chart.png" width="240" style="margin-right: 5px;" alt="Gas consumption manager chart screen" />
  <img src="../images/gas/filter.png" width="240" style="margin-right: 5px;" alt="Gas consumption manager filter screen" />
  <img src="../images/gas/offices.png" width="240" style="margin-right: 5px;" alt="Gas consumption manager offices screen" />
  <img src="../images/gas/video.png" width="240" alt="Gas consumption manager video screen" />
</div>
<br>

**Overview:**
- Engineered comprehensive utility management app for the National Manufactured Gas Company
- Implemented offline data persistence with automated consumption calculations
- Created interactive visualization tools and reporting system, reducing operational times by 70%
- Built streamlined communication channels with company offices, simplifying the customer support process
- **Tech Stack**: Android, Kotlin, MVVM, Room, Jetpack, MPAndroidChart, Material Design, Coroutines

[🔗 View on GitHub](https://github.com/daehan-lim/gas-consumption-manager)

---

### [ACME App](https://github.com/daehan-lim/acme)
*Android ticket management app with custom calendar, offline functionality, and location services (2021)*

<div style="display: flex; overflow-x: auto; border: 2px solid #ccc; padding: 6px; border-radius: 8px;">
  <img src="../images/acme/login.png" width="240" style="margin-right: 5px;" alt="ACME app login screen" />
  <img src="../images/acme/signup.png" width="240" style="margin-right: 5px;" alt="ACME app signup screen" />
  <img src="../images/acme/dashboard.png" width="240" style="margin-right: 5px;" alt="ACME app dashboard screen" />
  <img src="../images/acme/ticket_details.png" width="240" style="margin-right: 5px;" alt="ACME app ticket details screen" />
  <img src="../images/acme/edit.png" width="240" style="margin-right: 5px;" alt="ACME app edit screen" />
  <img src="../images/acme/calendar.png" width="240" style="margin-right: 5px;" alt="ACME app calendar screen" />
  <img src="../images/acme/calendar_sync.png" width="240" style="margin-right: 5px;" alt="ACME app calendar sync screen" /> 
  <img src="../images/acme/maps.png" width="240" alt="ACME app maps screen" />
</div>
<br>

**Overview:**
- Fully offline-capable service ticket management app with responsive design implementation
- Implemented interactive calendar with custom event visualization and Android Calendar Provider API integration, improving task scheduling efficiency
- Embedded Google Maps functionality for address search and directions, reducing address lookup and navigation time by approximately 20%
- Created user registration and authentication flows with input validation and error feedback
- **Tech Stack**: Android, Kotlin, MVVM, Jetpack, Google Maps, Room, Material Design.

[🔗 View on GitHub](https://github.com/daehan-lim/acme)

---

### [Yellow Pages](https://github.com/daehan-lim/cuban-yellow-pages)
*Mobile business directory app for Cuba's telecommunications company combining business search with essential telecom services (2020)*

<div style="background: linear-gradient(135deg, #1e3c72, #2a5298); padding: 15px; border-radius: 15px; box-shadow: 0px 6px 12px rgba(0, 0, 0, 0.3);">
  <div style="display: flex; overflow-x: auto; gap: 30px; padding: 10px 5px;">
    <!-- Home -->
    <div style="text-align: center; min-width: 220px;">
      <p style="color: #f0f0f0; font-size: 16px; font-weight: bold; margin: 0 0 15px 0; line-height: 1.4;">Search businesses, access emergency numbers and business directories</p>
      <img src="../images/yellow_pages/main.jpg" alt="Main screen" style="width: 100%; height: auto; max-width: 220px; border-radius: 12px; box-shadow: 0px 8px 16px rgba(0, 0, 0, 0.3);">
    </div>
    <!-- Green Pages -->
    <div style="text-align: center; min-width: 220px;">
      <p style="color: #f0f0f0; font-size: 16px; font-weight: bold; margin: 0 0 15px 0; line-height: 1.4;">Find government procedures, requirements and service schedules</p>
      <img src="../images/yellow_pages/green_home.jpg" alt="Green Pages" style="width: 100%; height: auto; max-width: 220px; border-radius: 12px; box-shadow: 0px 8px 16px rgba(0, 0, 0, 0.3);">
    </div>
    <!-- Info Home -->
    <div style="text-align: center; min-width: 220px;">
      <p style="color: #f0f0f0; font-size: 16px; font-weight: bold; margin: 0 0 15px 0; line-height: 1.4;">Browse phone services, customer support and international calls</p>
      <img src="../images/yellow_pages/information_home.jpg" alt="Information Pages" style="width: 100%; height: auto; max-width: 220px; border-radius: 12px; box-shadow: 0px 8px 16px rgba(0, 0, 0, 0.3);">
    </div>
    <!-- Mobile Internet -->
    <div style="text-align: center; min-width: 220px;">
      <p style="color: #f0f0f0; font-size: 16px; font-weight: bold; margin: 0 0 15px 0; line-height: 1.4;">Explore mobile internet plans, connection settings and service options</p>
      <img src="../images/yellow_pages/information_mobile_internet.jpg" alt="Mobile Internet" style="width: 100%; height: auto; max-width: 220px; border-radius: 12px; box-shadow: 0px 8px 16px rgba(0, 0, 0, 0.3);">
    </div>
    <!-- Ad Space -->
    <div style="text-align: center; min-width: 220px;">
      <p style="color: #f0f0f0; font-size: 16px; font-weight: bold; margin: 0 0 15px 0; line-height: 1.4;">Request advertising space, promote business and increase visibility</p>
      <img src="../images/yellow_pages/publicity.jpg" alt="Advertising Portal" style="width: 100%; height: auto; max-width: 220px; border-radius: 12px; box-shadow: 0px 8px 16px rgba(0, 0, 0, 0.3);">
    </div>
  </div>
</div>
<br>

**Overview:**
- Developed Cuba's first Yellow Pages mobile app, implementing enterprise-grade API integration for real-time business search
- Engineered offline vector mapping system reducing data usage by 85% through embedded map files for business geolocalization
- Implemented automated background synchronization for offline access to government services and telephone information sections
- Built responsive search interface with dynamic filters and efficient pagination handling
- Executed comprehensive software testing, including unit, UI and compatibility tests, optimizing reliability and user experience
- **Tech Stack**: Android, Java, SQLite, VTM Maps, WebView, HTML, JavaScript, SharedPreferences, JUnit

[🔗 View on GitHub](https://github.com/daehan-lim/cuban-yellow-pages)

<br>

## 📫 Contact Information

Feel free to reach out through LinkedIn or email for professional opportunities.

<div align="center"> 
  <a href="https://linkedin.com/in/penjan-a-eng-lim">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge">
  </a>
  <a href="mailto:penjan.eng@gmail.com">
    <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email Badge">
  </a>
</div>
<br>
