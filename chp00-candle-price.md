# Price  
In this section reference price data (open, close, high and low).
Reference: []()  

```js  

// This source code is subject to the terms of the Mozilla Public License 2.0 at https://mozilla.org/MPL/2.0/
// © cortabear

//@version=5
indicator(title = "Price By Corta Bear", shorttitle = "cb.price", overlay = false)

// Variables  
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
