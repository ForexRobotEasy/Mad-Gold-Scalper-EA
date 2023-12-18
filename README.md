# Mad Gold Scalper EA ReadMe File

This ReadMe file provides an overview of the code for the Mad Gold Scalper EA and describes how it works. Please note that ForexRobotEasy is not the official developer of this product. We only provide a sample code that can work as described in the official product.

For detailed reviews and trading results of this product, please visit [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/mad-gold-scalper-ea-review-advanced-risk-management-forex-tool/).

## Quick Trading Strategy

The Mad Gold Scalper EA implements a quick trading strategy on Gold (XAUUSD) to execute trades efficiently. It aims to take advantage of price movements in the gold market.

## Risk Management

The EA provides flexibility for users to choose between higher and lower risk settings. By adjusting the `UseHigherRisk` flag, users can select their preferred risk level. The EA also incorporates a safe stop loss and maximum lot size options to ensure compatibility with funded accounts like FTMO.

## Advanced News Filter

The Mad Gold Scalper EA enables users to configure filters for economic, federal, and job-related news events. By using the `UseNewsFilter` flag, users can choose to enable or disable news filtering. This feature ensures that the EA is always informed and prepared for market fluctuations.

## Real Backtest Data

To avoid manipulation or backtest conditioning, the EA integrates real backtest data with a 99.9% modeling quality. This ensures that the results provided by the EA are accurate and reliable for traders.

## Code Structure

The code is structured as follows:

### Includes

The necessary include files are included at the beginning of the code.

### Global Variables

Global variables such as `StopLossPips`, `MaxLotSize`, `UseHigherRisk`, and `UseNewsFilter` are defined. These variables allow users to customize the EA's behavior and risk management settings.

### Expert Advisor Class

The `MadGoldScalperEA` class is defined, which inherits from the `Expert` class. This class represents the main logic of the EA.

#### Constructor

The constructor initializes the variables for the trading strategy and risk management.

#### OnTick Function

The `OnTick` function is called on each tick of the symbol. It implements the quick trading strategy on Gold (XAUUSD) based on the current risk settings. It also places buy or sell orders based on the price movements and updates the `lastTradePrice` variable.

#### OnChartEvent Function

The `OnChartEvent` function is called when a chart event occurs. If the news filter is enabled (`UseNewsFilter` flag is true) and the chart event is a relevant news event (economic, federal, or job-related), the trading strategy is adjusted accordingly by setting `UseHigherRisk` to true. Otherwise, `UseHigherRisk` is set to false.

### Initialization and Deinitialization Functions

The `OnInit` function initializes the expert advisor by creating an instance of the `MadGoldScalperEA` class. The `OnDeinit` function deinitializes the expert advisor by removing it.

### Entry Point Functions

The `OnTick` and `OnChartEvent` functions are defined as entry points for the expert advisor. These functions call the respective functions of the `MadGoldScalperEA` class.

### Backtesting Function

The `OnTester` function is called during backtesting. It uses real backtest data with a 99.9% modeling quality to simulate trading using the EA.

### Indicator Function

The `OnCalculate` function is called to calculate custom indicators if needed. In this code, no indicator calculation is needed, so the function returns the total number of rates.

## Disclaimer

Please note that ForexRobotEasy is not the official developer of the Mad Gold Scalper EA. We only provide a sample code that can work as described in the official product. To find the official developer of this product, please use MQL5.
