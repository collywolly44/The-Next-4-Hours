# 4H Call

A home-screen web app that gives a long / no edge / bearish call for SPY over the next 4 hours of the stock session. SPY stands in for ES/MES. It also shows how those calls have scored over the past year.

## Host it (GitHub Pages, free)
1. Create a new public repo on github.com, e.g. `4h-call`.
2. Upload all 6 files here (Add file → Upload files) and commit.
3. Settings → Pages → Source: "Deploy from a branch" → `main` / root → Save.
4. Wait about a minute, then open `https://<your-username>.github.io/4h-call/`.

## Install on iPhone
Open the link in Safari → Share → Add to Home Screen.

## First run
Get a free API key at twelvedata.com, paste it in Settings, and tap Save. The key stays on your phone only.

## How it decides
- Pulls up to 5,000 hourly SPY bars (about 2.5 years).
- Sorts every past 4-hour window by four conditions: trend vs the 50-hour average, higher or lower than a day ago, choppy or calm volatility, and whether the window is a full 4 hours or ends at the close.
- Says LONG if the current setup rose 55% or more of the time, BEARISH if 45% or less, and NO EDGE in between. A setup needs at least 30 past cases.
- The track record is walk-forward: each past call used only data available at that moment.

These are statistics, not advice.
