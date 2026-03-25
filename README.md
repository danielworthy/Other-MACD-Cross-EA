# MACD-Cross-EA

I am sunsetting this trend-based MACD crossover EA after several years of testing, so I thought I may as well put it here in case someone finds it useful or interesting. Over roughly five years it made about 40% on a long-lived demo account. Most of that performance came in the first year, and after that it spent a lot of time mostly flapping around rather than compounding meaningfully. Even so, I still think that is moderately impressive for a very simple EA that I basically set and forgot about. It would likely do better with discretionary trade selection and manual management, but as a hands-off experiment it held up well enough to be worth sharing. The pairs I ran it on changed over time, and I am still a little surprised the broker let me keep the same demo account alive for that long, but there you have it.

This is a MetaTrader 4 Expert Advisor built around MACD crossovers with a trend-following bias. In practice it looks for MACD crosses around recent fractal structure, then filters entries with ADX, volume, and accumulation/distribution before placing stop orders at the breakout level. Stops and trailing stops are driven mainly by ATR and recent fractal range, and profitable trades can also be closed when MACD turns back the other way. I ran it on the H4 timeframe only, and that is really the intended home for it. If you want to experiment elsewhere, daily is the only other timeframe I would seriously consider, but it may not take many trades there.

To use it, open the project in MetaEditor, compile [`other simple macd cross.mq4`](/Users/tigga/Documents/GitHub/MACD-Cross-EA/other%20simple%20macd%20cross.mq4), and attach the EA to an H4 chart in MT4. I would not use it on lower timeframes. If you want to try anything else, stick to D1 and expect far fewer trades. Start on demo, use conservative sizing, and inspect the constants in the source before running it anywhere important. The current code auto-sizes lots when `cLOTS` is `0`, adapts position size based on recent win rate, and relies on the chart timeframe for behaviour, so test the exact symbol and timeframe combination you care about before trusting it.

## Screenshots

### Overview

![Overview](./macd%20cross%20-%20overview.png)

![Summary](./macd%20cross%20-%20summary%201.png)

### Year by year

![2021](./macd%20cross%202021.png)

![2022](./macd%20cross%202022.png)

![2023](./macd%20cross%202023.png)

![2024](./macd%20cross%202024.png)

![2025](./macd%20cross%202025.png)

![2026](./macd%20cross%202026.png)

*I had ChatGPT have a final blast at the code before I uploaded it here. It compiles, but it may also have introduced new bugs.*
