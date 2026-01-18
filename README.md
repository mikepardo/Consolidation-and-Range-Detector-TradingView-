# Consolidation and Range Detector for TradingView

A powerful Pine Script V6 indicator that automatically detects and visualizes consolidation ranges and price breakouts on TradingView charts.

## Features

### 🎯 Core Functionality
- **Automatic Range Detection**: Identifies consolidation zones based on price movement
- **Breakout Detection**: Alerts when price breaks above or below consolidation ranges
- **Real-time Monitoring**: Continuously tracks price action within identified ranges
- **Customizable Parameters**: Adjust sensitivity and detection criteria to match your trading style

### 📊 Visual Elements
- **Range Boxes**: Highlighted rectangular zones showing consolidation areas
- **Range Lines**: Upper and lower boundary lines
- **Mid-Line**: Center line of the consolidation range
- **Breakout Signals**: Triangle markers indicating bullish/bearish breakouts
- **Information Table**: Real-time statistics displayed on the chart
- **Background Coloring**: Subtle background shading during consolidation periods

### 🔔 Alert System
- Bullish breakout alerts
- Bearish breakout alerts
- New consolidation detection alerts

## Installation

1. Open TradingView and navigate to the Pine Editor
2. Create a new indicator
3. Copy the contents of `consolidation_range_detector.pine`
4. Paste into the Pine Editor
5. Click "Add to Chart"

## Parameters

### Range Detection Settings

| Parameter | Default | Range | Description |
|-----------|---------|-------|-------------|
| **Lookback Period** | 20 | 5-200 | Number of bars to analyze for range detection |
| **Range Threshold %** | 2.0 | 0.1-10.0 | Percentage threshold for identifying consolidation |
| **Minimum Bars in Range** | 10 | 3-100 | Minimum consecutive bars required to confirm consolidation |

### Visual Settings

- **Show Range Boxes**: Display rectangular boxes around consolidation zones
- **Show Range Lines**: Display upper and lower boundary lines
- **Show Mid Line**: Display the midpoint of the range
- **Show Labels**: Display text labels on consolidations and breakouts
- **Box Transparency**: Adjust the transparency of range boxes (0-100)

### Color Settings

- **Bullish Breakout Color**: Color for upward breakout signals (default: green)
- **Bearish Breakout Color**: Color for downward breakout signals (default: red)
- **Consolidation Color**: Color for range boxes and lines (default: blue)

## How It Works

### Consolidation Detection Algorithm

1. **Calculate Range**: The indicator calculates the highest high and lowest low over the lookback period
2. **Measure Range Size**: Determines the range as a percentage of the current price
3. **Identify Consolidation**: If the range size is below the threshold percentage, it's considered a consolidation
4. **Confirm Pattern**: The consolidation must persist for the minimum number of bars to be confirmed
5. **Track Breakouts**: Monitors price action to detect when price breaks out of the range

### Breakout Logic

- **Bullish Breakout**: Occurs when the close price exceeds the range high
- **Bearish Breakout**: Occurs when the close price falls below the range low

## Usage Examples

### For Day Traders
```
Lookback Period: 10-20
Range Threshold: 1.0-2.0%
Minimum Bars: 5-10
```

### For Swing Traders
```
Lookback Period: 30-50
Range Threshold: 2.0-3.0%
Minimum Bars: 15-25
```

### For Position Traders
```
Lookback Period: 50-100
Range Threshold: 3.0-5.0%
Minimum Bars: 20-40
```

## Interpretation Guide

### When in Consolidation
- Price is moving sideways within a defined range
- Good opportunity to prepare for a breakout trade
- Watch for volume increase as a breakout signal
- Consider range-bound strategies (buy at support, sell at resistance)

### Bullish Breakout (Triangle Up ▲)
- Price has broken above the consolidation range
- Potential start of an uptrend
- Consider long positions or closing short positions
- Use the range high as support level

### Bearish Breakout (Triangle Down ▼)
- Price has broken below the consolidation range
- Potential start of a downtrend
- Consider short positions or closing long positions
- Use the range low as resistance level

## Information Table

The indicator displays a real-time table in the top-right corner showing:

| Metric | Description |
|--------|-------------|
| **In Consolidation** | Whether price is currently in a confirmed consolidation |
| **Range Size** | The percentage size of the current range |
| **Bars in Range** | Number of consecutive bars in the consolidation |
| **Range Width** | Absolute price width of the range |

## Best Practices

1. **Combine with Volume**: Use volume indicators to confirm breakouts
2. **Multiple Timeframes**: Check consolidations on higher timeframes for more significant ranges
3. **Wait for Confirmation**: Don't trade immediately on breakout signals; wait for candle close
4. **Use Stop Losses**: Place stops just inside the range to manage risk
5. **Consider Market Context**: Be aware of major news events that might cause false breakouts

## Customization Tips

- **Tight Ranges**: Lower the Range Threshold % (0.5-1.5%) for scalping
- **Wide Ranges**: Increase the Range Threshold % (3.0-5.0%) for longer-term analysis
- **Reduce Noise**: Increase Minimum Bars in Range to filter out short-term fluctuations
- **More Sensitivity**: Decrease Minimum Bars in Range to catch smaller consolidations

## Troubleshooting

### Not Detecting Ranges
- Decrease the Range Threshold %
- Decrease the Minimum Bars in Range
- Increase the Lookback Period

### Too Many False Signals
- Increase the Range Threshold %
- Increase the Minimum Bars in Range
- Decrease the Lookback Period

### Boxes Not Showing
- Ensure "Show Range Boxes" is enabled
- Check that Box Transparency is not set to 100
- TradingView limits boxes to 500; older boxes may be removed

## Technical Details

- **Pine Script Version**: 6
- **Indicator Type**: Overlay
- **Max Boxes**: 500
- **Max Lines**: 500
- **Repainting**: This indicator does not repaint; signals are confirmed on bar close

## License

This project is licensed under the Mozilla Public License 2.0 - see the LICENSE file for details.

## Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

## Disclaimer

This indicator is for educational and informational purposes only. It should not be considered financial advice. Always do your own research and consider consulting with a financial advisor before making trading decisions. Past performance does not guarantee future results.

## Version History

### v1.0.0 (Initial Release)
- Consolidation range detection
- Breakout signals
- Customizable visual elements
- Real-time information table
- Alert system
- Pine Script V6 compatibility

## Support

For questions, issues, or suggestions, please open an issue on the GitHub repository.

---

**Happy Trading! 📈📉**
