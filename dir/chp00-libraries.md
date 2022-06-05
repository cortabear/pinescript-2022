# Libraries  
A key addition to Pine Script v5 us **libraries**. Libraries are a new type of publication that allos you to create custom functions to be reused in other scripts.  
  
## Export    
  
Libraries must have the export function to indicate this library needs to be accessible by other scripts.
```js  
  
// Mandatory keywords  
export high() =>  
...  

```  
  
## Data Types  
  
Libraries are required to define their data types.  
```js  
  
var float alphaVariable = 0.1  
  
```  
  
## Compiler Directives  
  
They document the library's code and provide description authors use when publishing. Compiler directives are optional.   
```js  

// @description 

// @function  

// @param  
 
// @returns  

```  
  
## What Can Not Be Used?  
  
### Requests  
### Input  
### Plot  
### Fill  
### Background Color  
  
## Sample Library  
```js
// @description This is where the library desciption goes.  
library(title, overlay)

// @function This is where the function desciption goes.    
// @param <parameter> This is where the parameter desciption goes.     
// @returns This is where the return value desciption goes. 
  
```  


## References  
  

### Modules & Classes 
Self contained script. Libraries are similar to modules or classes used in your traditional coding languages.

### Pine Script   

See **Concepts** / Libraries for more information.   
1. [Pine Script™ v5 User Manual](https://www.tradingview.com/pine-script-docs/en/v5/index.html) 

### The Art Of Trading  
**Author**: Matthew J. Slabosz  
**Location**: Queensland, Australia  
  
1. [How to use LIBRARIES in Pine Script V5](https://youtu.be/xFBvITwLoKg)  