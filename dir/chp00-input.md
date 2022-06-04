# Input    
In this section learn about getting user input from your scripts. Various functions to create a settings interface to obtain input from the end user.  


```js  
  
// This source code is subject to the terms of the Mozilla Public License 2.0 at https://mozilla.org/MPL/2.0/
// © cortabear

//@version=5
indicator(title = "User Input", shorttitle = "cb.user-input", overlay = false)  
  
// Get User Input  
booleanCB = input.bool(title="True/False Setting", defval=true)
integerCB = input.int(title="Whole Number Input", defval=0, minval=0, step=1)
floatCB = input.float(title="Decimal Input", defval=0, minval=0, step=0.01)
priceCB = input.price(title="Price Input", defval=0)
timeCB = input.time(title="Time Input", defval=0, confirm=true)  

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
 
1. [Basic User Input](https://youtu.be/HYyuYgPRLpc?list=PLSP_1DBafH-ES8Fw_noPA8d3dNxScysjc&t=5284)  