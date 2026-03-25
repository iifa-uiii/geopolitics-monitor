# IIFA Geoeconomics & Geopolitics Monitor

> An AI-powered, live intelligence dashboard tracking global geoeconomic and geopolitical developments with a focus on Indonesia's strategic exposure.

**Built by:** Indonesian Institute for Foreign Affairs (IIFA) at Universitas Islam Internasional Indonesia (UIII)  
**Faculty:** Faculty of Social Sciences  
**Live dashboard:** [iifa-uiii.github.io/geopolitics-monitor](https://iifa-uiii.github.io/geopolitics-monitor) 

---

## What This Is

This dashboard is an open-source intelligence tool designed for researchers, analysts, and policymakers at IIFA. It combines live market data, AI-generated conflict intelligence, and structural geopolitical data into a single, deployable web interface — no server, no backend, no installation required.

The dashboard is built as a single self-contained HTML file. It runs entirely in the browser.

---

## Features

### Conflict Intelligence Tab
- Six active conflict zones monitored: South China Sea, Strait of Hormuz & Iran, Gaza & Red Sea, Russia–Ukraine, Taiwan Strait, Myanmar
- AI-generated intelligence briefs synthesized by Claude (Anthropic API), focused on Indonesia's specific exposure — trade, energy, diplomacy, and domestic political pressure
- Representative headlines per conflict zone
- Per-zone refresh timestamps in WIB (Western Indonesia Time)
- Auto-refresh every 4 hours, with a live countdown timer and manual override button

### Live Markets Tab
- Real-time IDR/USD, IDR/CNY, IDR/JPY exchange rates via Open Exchange Rates API
- Indicative commodity prices for Indonesia's key exports and imports: coal, palm oil, nickel, natural gas, gold, Brent crude
- Live ticker bar scrolling market data across the top of the dashboard

### Trade & Economy Tab
- Indonesia's top trade partners (2024, BPS Indonesia / UN Comtrade)
- Top export commodities by value
- Economic coercion and sanctions exposure table — including EUDR, US-China tariffs, Red Sea disruption, Hormuz risk

### Alliance Blocs Tab
- Indonesia's membership status and strategic position across NATO+, BRICS+, ASEAN, RCEP, Quad, and BRI
- Strategic hedging score by partner — composite of trade dependence, arms imports, diplomatic engagement, and FDI

### Power Indices Tab
- Composite power index across 10 global actors: economic, military, and diplomatic dimensions
- Indonesia's power profile: GDP rank, population, Lowy Power Index score, military spend, naval capacity
- Global defense expenditure chart (SIPRI 2024)


---

## Data Sources

| Data | Source |
|------|--------|
| Exchange rates | [Open Exchange Rates API](https://open.er-api.com) (live) |
| Conflict summaries | Claude by Anthropic (AI-generated, open-source news synthesis) |
| Trade data | BPS Indonesia, UN Comtrade (2024) |
| Military expenditure | SIPRI Military Expenditure Database (2024) |
| Power indices | Lowy Institute Asia Power Index (2024) |
| Commodity prices | Indicative market approximations |
| Conflict tracking | ACLED, IISS Armed Conflict Survey, UN OCHA, Reuters, Al Jazeera |
| Alliance data | ASEAN Secretariat, World Bank, SIPRI |

---

## How to Use

### View the live dashboard
Open the link above in any modern browser. No installation needed.

### Run locally
Download `index.html` and open it directly in your browser. Exchange rates and AI conflict summaries will load automatically on page open.

### Update the dashboard
1. Edit `index.html` locally
2. Push the updated file to this repository
3. GitHub Pages will redeploy automatically within ~60 seconds

### Export data
Go to the **Export Data** tab in the dashboard. Download as JSON (for Python/R) or CSV (for Excel). Trigger a conflict refresh first to ensure AI summaries are included in the export.

---

## Technical Notes

- **Stack:** Vanilla HTML, CSS, JavaScript — zero frameworks, zero dependencies except Chart.js (loaded via CDN)
- **AI:** Anthropic API (Claude Sonnet) called client-side for conflict intelligence briefs
- **Exchange rates:** Open Exchange Rates free tier, called on page load
- **Deployment:** GitHub Pages (static hosting) — single `index.html` file
- **Refresh cycle:** Conflict intelligence auto-refreshes every 4 hours; exchange rates refresh on page load
- **No backend required:** All API calls are made directly from the browser

---

## Limitations

- Commodity prices are indicative approximations, not live feed data. A paid commodity data API (e.g. Alpha Vantage, Quandl) can be integrated for live prices.
- AI conflict summaries are synthesized from the model's training knowledge plus contextual prompting — they are not scraped from live news in real time. For production use, integrate a live news API (e.g. NewsAPI, GDELT) as context for the AI calls.
- The Anthropic API key is called client-side, which is acceptable for internal/research use but should be proxied through a backend for fully public deployment.

---

## Roadmap

- [ ] Live news API integration for real-time headline sourcing (NewsAPI / GDELT)
- [ ] Backend proxy for Anthropic API calls
- [ ] Live commodity price feed
- [ ] Historical data archiving (store each export snapshot)
- [ ] Bahasa Indonesia language toggle
- [ ] IIFA policy brief auto-generation from conflict intelligence data

---

## Citation

If you use data or outputs from this dashboard in research or publications, please cite:

> Indonesian Institute for Foreign Affairs (IIFA). (2025). *IIFA Geoeconomics & Geopolitics Monitor* [Dashboard]. Universitas Islam Internasional Indonesia. https://iifa-uiii.github.io/geopolitics-monitor

---

## Contact

**Indonesian Institute for Foreign Affairs (IIFA)**  
Faculty of Social Sciences  
Universitas Islam Internasional Indonesia (UIII)  
[uiii.ac.id](https://uiii.ac.id)

---

*This dashboard is for research and policy analysis purposes. AI-generated conflict summaries should be verified with primary sources before formal publication.*
