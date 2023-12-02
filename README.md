# Sun USDCAD Trading Robot

This is a trading robot developed by the Forex Robot Easy Team. The robot is designed to trade the USDCAD currency pair on the M1 timeframe. It uses a multi-cycle scalping strategy to open and close positions based on predefined parameters.

## Input Parameters

The following input parameters can be adjusted to customize the robot's trading behavior:

- **TakeProfit**: The take profit level in pips.
- **StopLoss**: The stop loss level in pips.
- **LotSize**: The lot size for trading.
- **MaxCycles**: The maximum number of trading cycles.
- **MaxPositions**: The maximum number of positions per cycle.
- **MartingaleMultiplier**: The multiplier for the martingale system.

## Global Variables

The robot uses the following global variables to keep track of the trading process:

- **TotalPositions**: The total number of open positions.
- **PreviousClose**: The previous close price.

## Initialization

The robot's initialization function, `OnInit()`, simply prints a message to indicate that the robot has been initialized.

## Trading

The robot's main trading function, `OnTick()`, is called on each tick of the market. It retrieves the current price of the USDCAD currency pair and performs the following actions:

1. Checks if a new cycle should be started based on the number of open positions.
2. If no positions are open, it opens positions for a new cycle.
3. If positions are open, it checks if any positions should be closed based on the take profit or stop loss levels.
4. If the maximum number of positions per cycle has not been reached, it opens new positions.

The functions `OpenPositions()` and `ClosePositions()` handle the opening and closing of positions respectively. The `OpenPositions()` function loops through the maximum number of positions per cycle and opens buy positions at calculated entry prices. The `ClosePositions()` function loops through all open positions and checks if the take profit or stop loss levels have been reached. If so, it closes the position.

## Cleanup

The robot's cleanup function, `OnDeinit()`, is called when the robot is stopped. It simply prints a message to indicate that the robot has been stopped.

Please note that Forex Robot Easy is not the official developer of this product. This code is only a sample that demonstrates how the robot can work as described. To find the official developer of this product, please use MQL5.

For detailed reviews and trading results of this product, please visit [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/review-sun-usdcad-a-powerful-multi-cycle-scalper-for-usdcad-m1/).
