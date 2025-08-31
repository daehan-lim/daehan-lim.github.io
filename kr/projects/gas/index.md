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
    font-family: 'Noto Sans KR', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif !important;
    font-weight: 400 !important;
    word-break: keep-all !important;
    letter-spacing: -0.3px !important;
    line-height: 1.8 !important;
    font-size: 17px !important;
}

#nav-menu a {
  margin: 0 15px;
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
<img src="../../../images/gas/app_icon.png" alt="Project Icon" style="max-width:90%;max-height:90%;object-fit:contain;" />
</div>

</div>

# 가스 소비 관리 앱

## 📝 개요
**📌 앱 소개:** 국영 가스 공사의 수기식 가스 사용량 관리를 자동화하는 안드로이드 앱  
**🕒 기간:** 2021.02.20 ~ 2021.03.18 (1개월)  
**📱 플랫폼:** Android 네이티브 앱  
**🏢 회사명:** Desoft (쿠바 국영 소프트웨어 개발사)  
**👥 개발 인원:** 1명  
**💼 역할:** 전체 안드로이드 앱 개발 담당  
**🛠️ 사용 기술:** `Android` `Kotlin` `Coroutines` `MVVM` `Room` `VideoView` `Jetpack` `Material Design` `Data Binding` `Navigation` `MPAndroidChart`  
**🔗 GitHub:** [daehan-lim/gas-consumption-manager](https://github.com/daehan-lim/gas-consumption-manager)

<div style="display: flex; overflow-x: auto; border: 2px solid #ccc; padding: 6px; border-radius: 8px;">
  <img src="../../../images/gas/main.png" width="240" style="margin-right: 5px;" alt="Gas consumption manager main screen" />
  <img src="../../../images/gas/calendar.png" width="240" style="margin-right: 5px;" alt="Gas consumption manager calendar screen" />
  <img src="../../../images/gas/chart.png" width="240" style="margin-right: 5px;" alt="Gas consumption manager chart screen" />
  <img src="../../../images/gas/filter.png" width="240" style="margin-right: 5px;" alt="Gas consumption manager filter screen" />
  <img src="../../../images/gas/offices.png" width="240" style="margin-right: 5px;" alt="Gas consumption manager offices screen" />
  <img src="../../../images/gas/video.png" width="240" alt="Gas consumption manager video screen" />
</div>
<span style="display: block; height: 11px;"></span>

## 📖 프로젝트 배경

쿠바 국영 가스 공사에서 기존의 수기식 가스 사용량 기록 및 계산 프로세스로 인한 업무 효율성 저하와 사용자 불편을 해결하기 위해 모바일 자동화 솔루션의 필요성이 대두되었습니다. 기존 시스템은 가스 계량기 검침부터 요금 계산까지 모든 과정이 수동으로 이루어져 시간이 많이 소요되고 계산 오류가 발생할 가능성이 높았습니다. 또한 가스 계량기 검침 방법에 대한 교육 자료와 고객 지원 체계가 체계적으로 구축되지 않아 사용자들이 어려움을 겪고 있었습니다. 이에 따라 사용량 자동 계산, 데이터 시각화, 오프라인 우선 설계를 통한 종합적인 가스 소비 관리 앱 개발 프로젝트를 기획하게 되었습니다.

## 🛠️ Tech Stack

[![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?logo=kotlin&logoColor=white&style=for-the-badge)](https://kotlinlang.org)
[![Android](https://img.shields.io/badge/Android-3DDC84?logo=android&logoColor=white&style=for-the-badge)](https://developer.android.com)
[![MVVM](https://img.shields.io/badge/MVVM-FF5252?style=for-the-badge)](https://developer.android.com/topic/architecture)
[![Material Design](https://img.shields.io/badge/Material%20Design-%234285F4?logo=material-design&logoColor=white&style=for-the-badge)](https://m3.material.io)
[![Jetpack](https://img.shields.io/badge/Jetpack-F57C00?logo=android&logoColor=white&style=for-the-badge)](https://developer.android.com/jetpack)
[![Coroutines](https://img.shields.io/badge/Coroutines-7F52FF?logo=kotlin&logoColor=white&style=for-the-badge)](https://kotlinlang.org/docs/coroutines-overview.html)
[![Navigation](https://img.shields.io/badge/Navigation-AB47BC?logo=android&logoColor=white&style=for-the-badge)](https://developer.android.com/guide/navigation)
[![LiveData](https://img.shields.io/badge/LiveData-3F51B5?style=for-the-badge)](https://developer.android.com/topic/libraries/architecture/livedata)
[![Room Database](https://img.shields.io/badge/Room-3DDC84?logo=android&logoColor=white&style=for-the-badge)](https://developer.android.com/training/data-storage/room)
[![Lifecycle](https://img.shields.io/badge/Lifecycle-2196F3?logo=android&logoColor=white&style=for-the-badge)](https://developer.android.com/jetpack/androidx/releases/lifecycle)
[![MPAndroidChart](https://img.shields.io/badge/MP%20Android%20Chart-2196F3?style=for-the-badge)](https://github.com/PhilJay/MPAndroidChart)

## 📋 프로젝트 구조

```
├── features/                          # 기능별 모듈 구조
│   ├── consumption/                   # 가스 소비량 계산 기능
│   │   ├── ConsumptionFragment.kt     # 소비량 입력 및 계산 UI
│   │   ├── ConsumptionViewModel.kt    # 소비량 계산 비즈니스 로직
│   │   └── ConsumptionViewModelFactory.kt
│   ├── history/                       # 사용량 이력 및 차트 분석
│   │   ├── HistoryActivity.kt         # 차트 기반 분석 화면
│   │   ├── HistoryViewModel.kt        # 차트 데이터 처리 로직
│   │   └── HistoryViewModelFactory.kt
│   ├── offices/                       # 영업소 연락처 디렉터리
│   │   ├── ComercialOfficesFragment.kt # 영업소 목록 UI
│   │   ├── ComercialOfficesAdapter.kt  # RecyclerView 어댑터
│   │   └── ComercialOfficesViewModel.kt
│   ├── readcounter/                   # 계량기 검침 가이드
│   │   ├── ReadCounterFragment.kt     # 동영상 가이드 화면
│   │   └── ReadCounterViewModel.kt
│   ├── about/                         # 앱 정보 및 연락처
│   │   └── AboutActivity.kt
│   └── splash/                        # 스플래시 화면
│       └── SplashActivity.kt
├── database/                          # Room 데이터베이스 레이어
│   ├── Consumption.kt                 # 소비량 데이터 엔티티
│   ├── ConsumptionDao.kt             # 데이터 액세스 객체
│   └── ConsumptionDatabase.kt        # 데이터베이스 설정
├── model/                            # 데이터 모델
│   └── ComercialOffice.kt           # 영업소 정보 모델
├── util/                             # 유틸리티 클래스
│   ├── BindingUtils.kt              # 데이터 바인딩 어댑터
│   └── Util.kt                      # 공통 유틸리티 함수
└── MainActivity.kt                   # 메인 액티비티 및 네비게이션
```

## 🌟 수행 내용

### Room 데이터베이스 기반 오프라인 데이터 관리 및 사용량 데이터 저장
- **MVVM 아키텍처와 Repository 패턴 적용**
  - `ConsumptionDao`를 통한 데이터 액세스 레이어 추상화 및 비즈니스 로직 분리
  - `Coroutines`와 `suspend` 함수를 활용한 비동기 데이터베이스 작업 처리로 UI 스레드 블로킹 방지
  - `LiveData`와 `ViewModel`을 통한 반응형 UI 구현 및 생명주기 인식 데이터 바인딩
  - Singleton 패턴과 `fallbackToDestructiveMigration()`을 적용한 안정적인 데이터베이스 관리

- **효율적인 데이터 CRUD 작업 구현**
  - 월별 소비량 조회, 연도별 데이터 필터링, 최신 검침값 자동 연동 등 복합 쿼리 최적화
  - 이전 달 검침값 자동 연동으로 연속성 있는 데이터 입력 환경 구현

### 가스 사용량 자동 계산 및 검증 시스템 개발
- **실시간 입력 검증 및 오류 방지**
  - 이전 검침값보다 현재 검침값이 작을 경우 즉시 오류 알림 및 입력 차단 기능
  - `TextInputLayout`의 `errorEnabled` 속성을 활용한 실시간 필드 검증 UI 구현
  - 필수 입력값 누락 시 즉시 피드백 제공으로 사용자 입력 오류 최소화

- **자동 사용량 계산 및 요금 산정**
  - `PAYMENT_COEFFICIENT` 상수(2.5)를 활용한 일관된 요금 계산 로직 구현
  - 가스 사용량(㎥)과 요금(페소) 간 실시간 변환 계산으로 즉시 결과 확인 가능
  - HTML 포맷팅을 통한 계산 결과의 표시 및 `AlertDialog`를 통한 결과 제시

### MPAndroidChart 기반 인터랙티브 데이터 시각화 구현
- **연도별/월별 소비 패턴 분석 차트**
  - `BarChart`를 활용한 월별 가스 소비량 시각화 및 애니메이션 효과로 사용자 경험 향상
  - 페소/㎥ 단위 전환 필터링 기능으로 다양한 관점의 데이터 분석 지원

- **반응형 차트 UI 및 사용자 인터랙션**
  - 세로/가로 모드에 따른 차트 레이아웃 자동 조정 및 라벨 밀도 최적화
  - `MonthPickerDialog`를 활용한 직관적인 연도 선택 인터페이스 구현

### VideoView 기반 가스 계량기 검침 방법 학습을 위한 동영상 가이드
- **전체화면 지원 동영상 플레이어 개발**
  - `MediaController`를 커스터마이징하여 전체화면 버튼 추가 및 화면 회전 제어 구현
  - 세로/가로 모드 자동 전환 시 `SystemUI` 숨김 처리로 몰입형 시청 환경 제공
  - 동영상 재생 위치 저장 및 복원 기능으로 끊김 없는 사용자 경험 구현

- **생명주기 인식 미디어 관리**
  - `onStart()`, `onStop()`, `onPause()`에서의 적절한 동영상 리소스 관리로 메모리 누수 방지
  - 동영상 완료 시 자동 세로 모드 복원 및 플레이스홀더 화면 표시
  - `raw` 리소스를 활용한 오프라인 동영상 재생으로 네트워크 의존성 제거

### RecyclerView 기반 영업소 연락처 디렉터리 구현
  - 고객 지원을 위한 영업소 연락처 디렉터리 통합으로 고객 문의 처리 과정 단순화
  - `Intent.ACTION_CALL`과 `Intent.ACTION_SENDTO`를 활용한 네이티브 앱 연동
  - `CALL_PHONE` 권한 동적 요청 및 권한 거부 시 대체 다이얼 액션 제공
  - `@BindingAdapter`를 활용한 재사용 가능한 뷰 바인딩 로직 구현

### 사용자 경험 최적화 및 접근성 향상
  - Bottom Navigation과 Fragment 기반 화면 전환
    - `setupWithNavController()`를 통한 자동 네비게이션 상태 관리
    - `onBackPressed()` 오버라이드를 통한 앱 종료 확인 다이얼로그 구현
  - Toolbar 기반 일관된 액션바 설계
    - History, About 기능으로의 즉시 접근을 위한 옵션 메뉴 등 구현
  - Custom Font(`segoe_ui`, `seguisb`) 적용으로 차별화된 타이포그래피 구현
  - 가스 공사 로고와 브랜드 컬러를 활용한 스플래시 화면 구현
  - Facebook, Instagram, Twitter, Telegram, LinkedIn 등 6개 소셜 미디어 플랫폼 연동
  - `Intent.ACTION_VIEW`를 통한 외부 브라우저 연동으로 추가 정보 접근 경로 제공

### 개발 효율성 및 코드 품질 향상
- **Data Binding과 ViewBinding 적용**
  - XML 레이아웃과 Kotlin 코드 간 타입 안전성 확보 및 `findViewById()` 제거
  - `@{viewModel.property}` 문법을 통한 선언적 UI 업데이트 구현
  - `executePendingBindings()`를 활용한 즉시 바인딩 처리로 UI 깜빡임 방지

## 🚀 성과 및 개선 효과
- **업무 처리 시간 70% 단축**: 수기 계산에서 자동 계산으로 전환하여 가스 요금 산정 시간 대폭 감소
- **오프라인 우선 설계**: Room 로컬 데이터베이스를 통해 네트워크 연결 없이도 모든 핵심 기능 사용 가능
- **사용자 만족도 향상**: 직관적인 UI/UX와 동영상 가이드를 통한 계량기 검침 방법 학습 지원
- **고객 지원 개선**: 통합된 영업소 연락처로 고객 문의 처리 과정 단순화 및 접근성 강화

<br><br><br>