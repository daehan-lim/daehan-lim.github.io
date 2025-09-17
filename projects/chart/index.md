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


<br><br>
<nav id="ticker-tape">
    <!-- TradingView Widget BEGIN -->
    <div class="tradingview-widget-container">
        <div class="tradingview-widget-container__widget"></div>
        <script
            type="text/javascript"
            src="https://s3.tradingview.com/external-embedding/embed-widget-ticker-tape.js"
            async
>
            {
            "symbols": [
              {
                "description": "",
                "proName": "NASDAQ:TSLA"
              },
              {
                "description": "",
                "proName": "NASDAQ:AAPL"
              },
              {
                "description": "",
                "proName": "NASDAQ:NVDA"
              },
              {
                "description": "",
                "proName": "NASDAQ:MSFT"
              },
              {
                "description": "",
                "proName": "NASDAQ:AMZN"
              },
              {
                "description": "",
                "proName": "NASDAQ:GOOGL"
              },
              {
                "description": "",
                "proName": "NASDAQ:META"
              },
              {
                "description": "",
                "proName": "NYSE:BRK.B"
              },
              {
                "description": "",
                "proName": "NYSE:LLY"
              },
              {
                "description": "",
                "proName": "NYSE:UNH"
              },
              {
                "description": "",
                "proName": "NYSE:V"
              },
              {
                "description": "",
                "proName": "NYSE:WMT"
              }
            ],
            "showSymbolLogo": true,
            "colorTheme": "light",
            "isTransparent": false,
            "displayMode": "adaptive",
            "locale": "en"
             }
        </script>
    </div>
    <!-- TradingView Widget END -->
</nav>

<br><br>
<div class="tradingview-widget-container">
    <div class="tradingview-widget-container__widget"></div>
    <script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-tickers.js" async>
        {
            "symbols": [
            {
                "proName": "FOREXCOM:SPXUSD",
                "title": "S&P 500 Index"
            },
            {
                "proName": "FOREXCOM:NSXUSD",
                "title": "US 100 Cash CFD"
            },
            {
                "proName": "FX_IDC:EURUSD",
                "title": "EUR to USD"
            },
            {
                "proName": "BITSTAMP:BTCUSD",
                "title": "Bitcoin"
            },
            {
                "proName": "BITSTAMP:ETHUSD",
                "title": "Ethereum"
            }
        ],
            "colorTheme": "light",
            "locale": "en",
            "largeChartUrl": "",
            "isTransparent": false,
            "showSymbolLogo": true,
            "displayMode": "adaptive"
        }
    </script>
</div>

<br><br>
<!-- TradingView Widget BEGIN -->
<div class="tradingview-widget-container">
  <div class="tradingview-widget-container__widget"></div>
  <div class="tradingview-widget-copyright"><a href="https://www.tradingview.com/symbols/BITSTAMP-BTCUSD/?exchange=BITSTAMP" rel="noopener nofollow" target="_blank"><span class="blue-text">BTCUSD chart by TradingView</span></a></div>
  <script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-mini-symbol-overview.js" async>
  {
  "symbol": "BITSTAMP:BTCUSD",
  "chartOnly": false,
  "dateRange": "12M",
  "noTimeScale": false,
  "colorTheme": "light",
  "isTransparent": false,
  "locale": "en",
  "width": "100%",
  "autosize": true,
  "height": "100%",
  "displayMode": "adaptive"
}
  </script>
</div>
<!-- TradingView Widget END -->

<br><br>
<!-- TradingView Widget BEGIN -->
<div class="tradingview-widget-container">
  <div class="tradingview-widget-container__widget"></div>
  <div class="tradingview-widget-copyright"><a href="https://www.tradingview.com/" rel="noopener nofollow" target="_blank"><span class="blue-text">Apple,Google and Microsoft quotes by TradingView</span></a></div>
  <script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-symbol-overview.js" async>
  {
  "lineWidth": 2,
  "lineType": 0,
  "chartType": "area",
  "fontColor": "rgb(106, 109, 120)",
  "gridLineColor": "rgba(46, 46, 46, 0.06)",
  "volumeUpColor": "rgba(34, 171, 148, 0.5)",
  "volumeDownColor": "rgba(247, 82, 95, 0.5)",
  "backgroundColor": "#ffffff",
  "widgetFontColor": "#0F0F0F",
  "upColor": "#22ab94",
  "downColor": "#f7525f",
  "borderUpColor": "#22ab94",
  "borderDownColor": "#f7525f",
  "wickUpColor": "#22ab94",
  "wickDownColor": "#f7525f",
  "colorTheme": "light",
  "isTransparent": false,
  "locale": "en",
  "chartOnly": false,
  "scalePosition": "right",
  "scaleMode": "Normal",
  "fontFamily": "-apple-system, BlinkMacSystemFont, Trebuchet MS, Roboto, Ubuntu, sans-serif",
  "valuesTracking": "1",
  "changeMode": "price-and-percent",
  "displayMode": "adaptive"
  "symbols": [
    [
      "Apple",
      "AAPL|1D"
    ],
    [
      "Google",
      "GOOGL|1D"
    ],
    [
      "Microsoft",
      "MSFT|1D"
    ]
  ],
  "dateRanges": [
    "1d|1",
    "1m|30",
    "3m|60",
    "12m|1D",
    "60m|1W",
    "all|1M"
  ],
  "fontSize": "10",
  "headerFontSize": "medium",
  "autosize": true,
  "width": "100%",
  "height": "100%",
  "noTimeScale": false,
  "hideDateRanges": false,
  "hideMarketStatus": false,
  "hideSymbolLogo": false
}
  </script>
</div>
<!-- TradingView Widget END -->