327a42e673c4b043d30304e77da3afa939678e05## optional 

A fast and simple c++ interface to the TD Ameritrade APIs for stock and options trading.

#### Build Requirements
* boost
* curl
* ncurses

#### Building
* Clone and cd into `optional`.
* `mkdir build && cd build`
* `cmake ../ && make`

#### Dev TODO
* add gtest and switch to tdd. COME ON, TEGAN ._.
* uhh, maybe use curl instead of boost.beast? (if I only need get/put)

***

#### What this is. (Or will be. It's in progress.)
It's two main components:
1. A c++ back-end for algorithmic trading through TD Ameritrade (paper money or live trading).
  * Goal is a modular & fast interface that allows for quick backtesting and algorithm setup.
2. A simple ncurses frontend to provide a basic terminal GUI for order placement/status, account stats, etc.
  * Display list of current positions. 
  * Display list of current orders. 
  * Display balances (Cash & Sweep, Net Liq, Buying Power).
  * Sell and buy options/stock through single line input.

These are both implemented as static libraries. Includes are messy and only work in the scope of this cmake file, but I'll export them to a final package eventually.

#### More Info
User guide (just a text dump at this point tbh) [is on the wiki](https://github.com/tegan-lamoureux/optional/wiki).
