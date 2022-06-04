# Price  
In this section reference price data (open, close, high and low).
Reference: []()  


## Accessing basic price data  
The following references current candle and will run on every candle.  
  
```js  

// This source code is subject to the terms of the Mozilla Public License 2.0 at https://mozilla.org/MPL/2.0/
// © cortabear

//@version=5
indicator(title = "Price By Corta Bear", shorttitle = "cb.price", overlay = false)

// Variables (price data)  
candleOpen = open  
candleHigh = high 
candleLow = low
candleClose = close 

// Analyze Price Data  
candleSize = candleHigh - candleLow

// Draw candle data onto our chart  

// plot(candleOpen, color=color.blue)  
// plot(candleHigh, color=color.red)  
// plot(candleLow, color=color.green)
// plot(candleClose, color=color.purple)   

plot(candleSize, color=color.orange) 
  
 ```  
  
## Accessingn the historical price data operator  
  
**Use Case**  
Reference historical price data from a previous candle. 
Reference 'X' amount of candles back from the current candle. 
Compare the current candle size to the size of the '2 candles ago'.    

```js  
  
// This source code is subject to the terms of the Mozilla Public License 2.0 at https://mozilla.org/MPL/2.0/
// © cortabear

//@version=5
indicator(title = "Price By Corta Bear", shorttitle = "cb.price", overlay = false)  
  
currentCandle = high - low
candleSize10 = high[10] - low[10] // Historical data is referenced using the square brackets.  
candleSizeRatio = currentCandle / candleSize10  // 
  
plot(candleSizeRatio, color=color.red) // Plot on the chart  
  
```  
  
## Access historical volume  
  
```js  
  
// This source code is subject to the terms of the Mozilla Public License 2.0 at https://mozilla.org/MPL/2.0/
// © cortabear

//@version=5
indicator(title = "Historical Volume", shorttitle = "cb.volume", overlay = false)  
  
plot(volume[10], color=color.red) // Plot the volume from 'X' amount of 'candles ago'.  
  
```  
  
## Average True Range (ATR)  
Measures market volatility by decomposing the entire range of an asset price for that period.  
  
```js  
  
// This source code is subject to the terms of the Mozilla Public License 2.0 at https://mozilla.org/MPL/2.0/
// © cortabear

//@version=5
indicator(title = "Average True Range", shorttitle = "cb.avg-true-range", overlay = false)  
  
currentATR = ta.atr(14)  
atr10 = currentATR[10]  
rationATR = currentATR / atr10

plot(rationATR, color=color.red) 
  
``` 