## codewars.com
my solutions

---
+ **Multiples of 3 or 5**
```javascript
function solution(number) {
  let sum = 0;
  if (number < 0) return 0;
  for(n = 0; n < number; n++) {
    if(n%3 === 0 || n%5 === 0) sum += n;
  }
  return sum;
}
```
---
+ **Pair of gloves**
```javascript
function numberOfPairs(gloves) {
    let count = 0;
    let arr = [].concat(...gloves);
    for (let i = 0; i < arr.sort().length - 1; i++) {
        if (arr[i] === arr[i + 1]) {
            count += 1;
            i++;
        }
    }
    return count;
}
```
---
+ **Isograms**
```javascript
function isIsogram(str){
  str = str.toLowerCase();
  for(let i = 0; i < str.length; ++i){
    for(let j = i+1; j < str.length; ++j){
      if(str[i]===str[j]) return false; 
    }
  }
   return true;
}
```
---



