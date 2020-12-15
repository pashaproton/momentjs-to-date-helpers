# [moment.js](https://momentjs.com) to [Date](https://tc39.es/ecma262/#sec-date-objects) helpers
Commonly used patterns to get rid of moment.js

## Get diff of months
```
const monthDiff = (d1, d2) => {
  let months = (d2.getFullYear() - d1.getFullYear()) * 12
  
  months -= d1.getMonth()
  months += d2.getMonth()

  return months <= 0 ? 0 : months
}
```
