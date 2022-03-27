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
  //My hands are freezing
  let result = 0;
  let i = 0;
  while (i < gloves.length-1) {
  let j= i+1;
  while (j < gloves.length){
    if (gloves[i] === gloves[j]) {
      result += 1;
      } else {
      result += 0;
      }
    j++;
  }
  i++;
  }
  return result;
}
```
---
+ **Array Deep Count**
