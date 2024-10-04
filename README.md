# SuperTrend Indicator

The SuperTrend is a widely used indicator that helps traders identify trend changes across various markets, including equities, cryptocurrencies, forex, and other assets.

This implementation of the SuperTrend differs from traditional versions in two key aspects:

1. **The calculation source can be customized** and is not limited to the closing price. By default, it uses the average of high and low (`hl2`).
2. **The band calculation can be adjusted** to use either Average True Range (ATR) or Standard Deviation. The default setting is Standard Deviation.

While the classic SuperTrend utilizes ATR for its upper and lower band calculations, we believe that Standard Deviation provides a more precise method for determining the bands.

### The indicator offers four primary input parameters:

1. **Source:** The price source for the indicator calculation, which can be set to close, open, high, low, `hl2`, `hlc3`, or `ohlc4`.
2. **Band:** The method for calculating the bands, with options for ATR or StdDev.
3. **Period:** The lookback period for the calculation. It represents the length for standard deviation when using "StdDev" or the period for ATR when "ATR" is selected.
4. **Factor:** A multiplier used to adjust the distance between the bands and the selected source.

Buy and sell signals are generated based on the position of the SuperTrend relative to the price. A **buy signal** occurs when the SuperTrend moves below the closing price, while a **sell signal** is triggered when it shifts above the closing price.
