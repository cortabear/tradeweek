# TradeWEEK  


1. [Variables](#variables) : In 100 characters describe the purpose of setting variables in this indicator.



```js  
/**
 * This indicator is owned by Corta Bear Capital. This code is provided for educational and non-commercial use only. It should not be distributed for monetary purposes without explicit permission from Corta Bear Capital. All rights reserved.
 * This Pine Script™ code is subject to the terms of the Mozilla Public License 2.0 at https://mozilla.org/MPL/2.0/
 * © 2024 Corta Bear Capital
 */

//@version=5
indicator("TradeWEEK v.2.0.1", overlay=true)

```  


## Variables  

```js  

// Define Day Background Color.
sundayColor = color.new(#fbfff8, 0)
mondayColor = color.new(#f8fff0, 0)
tuesdayColor = color.new(#f4ffe9, 0)
wednesdayColor = color.new(#f1ffe1, 0)
thursdayColor = color.new(#edffd9, 0)
fridayColor = color.new(#e9ffd1, 0)
  
```  

## Checks  
```js  

// Check bar's day of the week.
isSunday = (dayofweek == dayofweek.sunday)
isMonday = (dayofweek == dayofweek.monday)
isTuesday = (dayofweek == dayofweek.tuesday)
isWednesday = (dayofweek == dayofweek.wednesday)
isThursday = (dayofweek == dayofweek.thursday)
isFriday = (dayofweek == dayofweek.friday)  

```  

## Application  
```js  
// Apply background color for all Sundays
bgcolor(isSunday ? sundayColor : na)
bgcolor(isMonday ? mondayColor : na)
bgcolor(isTuesday ? tuesdayColor : na)
bgcolor(isWednesday ? wednesdayColor : na)
bgcolor(isThursday ? thursdayColor : na)
bgcolor(isFriday ? fridayColor : na)
```  