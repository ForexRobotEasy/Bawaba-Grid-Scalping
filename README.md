# Bawaba Grid Scalping

Bawaba Grid Scalping is a forex trading robot developed by the Forex Robot Easy Team and is available for use on the MQL5 platform. This code is a sample implementation of the Bawaba Grid Scalping strategy.

## Features

The Bawaba Grid Scalping robot offers the following features:

- Take profit level: Traders can define the desired take profit level in points.
- Stop loss level: Traders can define the desired stop loss level in points.
- Trailing stop: Traders can enable a trailing stop feature with a specified trailing stop level in points.
- Dynamic lots: Traders can choose to use dynamic lots, where the lot size is calculated based on the account balance and maximum risk percentage, or fixed lots.
- Fixed lot size: If dynamic lots are disabled, traders can specify a fixed lot size.

## How it Works

The Bawaba Grid Scalping robot operates by placing grid orders based on the specified parameters. Here is a step-by-step breakdown of how it works:

1. OnInit function: This function is called when the robot is initialized. It sets the initial price, calculates the grid step size based on the price, and calculates the total number of orders for the grid. It also prints the grid parameters for reference.

2. OnTick function: This function is called on each tick of the price. It performs the following actions:

   - Checks if the current price has moved in favor of the trade.
   - If a position is selected for the symbol, it checks if the trailing stop feature is enabled and adjusts the stop loss accordingly.
   - Checks if the grid needs to be adjusted by comparing the absolute difference between the current price and the bid price with the grid step size.
   - If the grid needs adjustment, it calculates new grid levels (upper and lower levels) based on the current price and grid step size.
   - Places new orders for the grid. For each order, it alternates between buying and selling based on the order index. The lot size is determined either dynamically or using a fixed lot size.
   - Updates the current price.

3. CalculateLotSize function: This function calculates the lot size based on the account balance, maximum risk percentage, total number of orders, stop loss, and symbol point. It returns the calculated lot size.

## Product Description

Bawaba Grid Scalping is a professional forex trading robot developed by the Forex Robot Easy Team. It utilizes a grid trading strategy to take advantage of market price fluctuations.

By setting the desired take profit and stop loss levels, traders can define their risk-reward ratio. The trailing stop feature allows for potential profit maximization by adjusting the stop loss as the trade moves in favor.

Traders have the option to use dynamic lots, where the lot size is calculated based on the account balance and maximum risk percentage, or fixed lots. This flexibility allows traders to adapt the robot's trading strategy to their risk tolerance and account size.

Please note that ForexRobotEasy is not the official developer of this product. We only provide this sample code as an illustration of how the Bawaba Grid Scalping strategy can be implemented. For detailed reviews and trading results of this product, please visit [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/bawaba-grid-scalping-a-professional-review-of-forex-software-with-real-results/). To find the official developer and obtain the official version of this product, please visit the MQL5 platform.
