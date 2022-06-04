# Alerts  
In this section learn about how to trigger alerts in Pine Script.  
  
## Alert Function  
Triggers an alert as soon as it is called.  
  
```js
  
// This source code is subject to the terms of the Mozilla Public License 2.0 at https://mozilla.org/MPL/2.0/
// © cortabear

//@version=5
indicator(title = "Alert Function", shorttitle = "cb.alerts", overlay = false)  
  
// Alert Function  
highCandle = close > high[1]
lowCandle = close < low [1] 
  
// Only fire the alert after the candle has closed.
if highCandle
    alert(message="Alert message goes here", freq=alert.freq_once_per_bar_close)

// OR...
if highCandle
    alert("Alert message goes here", alert.freq_once_per_bar_close)

// Plot  
plot(close)  

// ------------------------------- 
// DISCLAIMER  
// -------------------------------
  
```  
  
## Alert Condition    
```js
  
// This source code is subject to the terms of the Mozilla Public License 2.0 at https://mozilla.org/MPL/2.0/
// © cortabear

//@version=5
indicator(title = "Alert Conditions", shorttitle = "cb.alerts", overlay = false)  

// Variables  
highCandle = close > high[1]
lowCandle = close < low [1] 

// Alert - 
alertcondition(lowCandle, "Lower Close Alert", "This candle closed lower than the previous candle. Current closing price: {{close}}")

// Plot  
plot(na)  

// ------------------------------- 
// DISCLAIMER  
// -------------------------------
  
```  
  

## References  
  
### Pine Script    
1. [Pine Script™ v5 User Manual](https://www.tradingview.com/pine-script-docs/en/v5/index.html) 

### The Art Of Trading  
**Author**: Matthew J. Slabosz  
**Location**: Queensland, Australia  
  
1. [Generating Alerts](https://youtu.be/HYyuYgPRLpc?list=PLSP_1DBafH-ES8Fw_noPA8d3dNxScysjc&t=5753)  