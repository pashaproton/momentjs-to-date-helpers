# [moment.js](https://momentjs.com) to [Date](https://tc39.es/ecma262/#sec-date-objects) helpers
Commonly used patterns to get rid of moment.js

## Get diff of months
### moment.js example
```
moment(b).diff(a, 'months')
```
### JavaScript example
```
const monthDiff = (a, b) => {
  let months = (b.getFullYear() - a.getFullYear()) * 12
  
  months -= a.getMonth()
  months += b.getMonth()

  return months <= 0 ? 0 : months
}
```
