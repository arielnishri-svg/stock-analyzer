# 📊 Stock Analyzer

AI-powered stock research across 30 items in 6 categories, powered by Claude.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/arielnishri-svg/stock-analyzer)

---

## Two ways to use

**Inside Claude.ai (no API key needed)**

Paste the contents of `index.html` into any Claude.ai chat as an artifact. Claude's auth handles the API calls automatically.

**Standalone (Vercel / local)**

Enter your Anthropic API key in the key field on the landing page. It's stored in your browser's localStorage and never leaves your device except to `api.anthropic.com`.

Get a key at [console.anthropic.com](https://console.anthropic.com).

---

## What it does

Enter any ticker or company name → Claude searches the web for current data → generates a scored checklist across 6 categories:

- 🔭 Business Fundamentals
- 💹 Financial Health
- ⚖️ Valuation
- 🛡️ Risk Factors
- 🌡️ Market Sentiment
- 🧩 Portfolio Fit

Outputs an overall score (0–100), BUY / HOLD / SELL verdict, key strengths and risks.

---

## What gets analyzed

Each category scores 0–100. Every item is rated ✅ pass / ⚠️ caution / ❌ fail with a one-line note pulled from current web data.

**🔭 Business Fundamentals**
- *Clear business model* — how the company makes money, whether the revenue logic is simple or convoluted
- *Competitive moat* — patents, network effects, switching costs, brand, cost advantages vs peers
- *Market size & growth potential* — TAM, SAM, growth rate of the end market, runway left
- *Management quality* — track record, capital allocation history, insider alignment, tenure
- *Revenue diversification* — customer concentration, geographic spread, product mix risk

**💹 Financial Health**
- *Revenue growth* — YoY and 3-year CAGR, acceleration or deceleration trend
- *Profit margins* — gross, operating and net margins vs sector benchmarks
- *Debt levels* — debt-to-equity, net debt/EBITDA, maturity schedule, refinancing risk
- *Free cash flow* — FCF margin, FCF conversion from net income, consistency
- *Return on equity* — ROE vs cost of equity, ROIC vs WACC, capital efficiency trend

**⚖️ Valuation**
- *P/E ratio vs sector* — trailing and forward P/E vs sector median and 5-year own average
- *P/S ratio* — price-to-sales vs growth rate (PEG-style), useful when earnings are thin
- *P/B ratio* — price-to-book, especially relevant for financials and asset-heavy businesses
- *Forward earnings* — consensus EPS estimates, revision trend (up or down), beat rate
- *Fair value vs price* — DCF-implied or analyst consensus target vs current price, upside/downside

**🛡️ Risk Factors**
- *Regulatory risks* — pending legislation, antitrust exposure, sector-specific compliance burden
- *Competitive threats* — new entrants, Big Tech encroachment, pricing pressure, market share trend
- *Macro headwinds* — interest rate sensitivity, FX exposure, commodity input costs, cycle position
- *Insider selling* — recent Form 4 filings, selling volume vs compensation, pattern vs one-off
- *Concentration risks* — top customer % of revenue, single-product dependency, key-person risk

**🌡️ Market Sentiment**
- *Analyst ratings* — consensus buy/hold/sell split, number of analysts covering, recent upgrades/downgrades
- *Earnings surprises* — last 4 quarters EPS beat/miss record, magnitude of surprises
- *Institutional ownership* — % held by institutions, recent 13F changes, notable new buyers or exits
- *Short interest* — short % of float, days-to-cover, recent change in short position
- *52-week range position* — where the stock sits in its range, momentum context

**🧩 Portfolio Fit**
- *Investment goals alignment* — growth vs income vs value characteristics
- *Risk tolerance fit* — beta, historical drawdowns, volatility vs market
- *Sector concentration* — how adding this stock changes sector exposure in a typical portfolio
- *Time horizon match* — whether the thesis requires 1 year or 5+ years to play out
- *Position size* — liquidity, market cap, bid-ask spread — whether it's practical to size meaningfully

---

## Deploy to Vercel

1. Fork this repo
2. Go to [vercel.com](https://vercel.com) → **Add New Project**
3. Import your fork — no build config or environment variables needed
4. Deploy

Or click the **Deploy with Vercel** button above.

---

## Run locally

```
git clone https://github.com/arielnishri-svg/stock-analyzer
cd stock-analyzer
open index.html
```

No build step. Pure static HTML.

---

> ⚠️ AI-generated analysis for informational purposes only. Not financial advice.
