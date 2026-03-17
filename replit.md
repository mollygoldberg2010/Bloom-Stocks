# Capra Trader

A client-side stock analysis and picker web application.

## Overview

Capra Trader is a single-page HTML application that provides:
- **Stock Analyzer**: Analyze individual stocks with stop-loss and target price calculations
- **Stock Picker**: AI-powered stock recommendations based on holding period and risk tolerance
- **Market Movers Sidebar**: Real-time display of gaining and declining stocks

## Architecture

- **Type**: Static HTML — no build system, no backend, no package manager
- **Entry Point**: `index.html` (single file containing all HTML, CSS, and JavaScript)
- **External Dependencies** (CDN):
  - Chart.js 4.4.1 for price history charts
  - Google Fonts (Poppins)
- **APIs Used**:
  - Anthropic Claude API (called directly from the browser) for stock data and recommendations
  - Finnhub API (optional, for live price data — user-provided key stored in localStorage)

## Development

The app is served via Python's built-in HTTP server:

```
python3 -m http.server 5000
```

## Deployment

Configured as a **static** deployment. The root directory (`.`) is the public directory since `index.html` is at the root.
