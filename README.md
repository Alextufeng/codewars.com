## codewars.com
my solutions

---
+ [**Multiples of 3 or 5**](https://www.codewars.com/kata/514b92a657cdc65150000006/train/javascript)
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
+ [**Pair of gloves**](https://www.codewars.com/kata/58235a167a8cb37e1a0000db/train/javascript)
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
+ [**Isograms**](https://www.codewars.com/kata/54ba84be607a92aa900000f1/train/javascript)
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
+ [**Digits explosion**](https://www.codewars.com/kata/585b1fafe08bae9988000314/train/javascript)
```javascript
function explode(s) {
  let str = '';
  for (let i = 0; i < s.length; i++){
    let j = 1;
    while (j <= s[i]) {
      str += s[i];
      j++;
    }
  }
  return str;
}
```
---
+ [**Handshake problem**](https://www.codewars.com/kata/5574835e3e404a0bed00001b/train/javascript)
```javascript
function getParticipants(handshakes){
  let sum=0;
  let i=1;
  while (sum < handshakes) {
    sum += i++;
    }
  return i;
}
```
---
+ [**N-th Fibonacci**](https://www.codewars.com/kata/522551eee9abb932420004a0/train/javascript)
```javascript
function nthFibo(n) {
  if (n == 1) return 0;
  let a = 1;
  let b = 1;
  for (let i = 3; i < n; i++) {
    let c = a + b;
    a = b;
    b = c;
  }
  return b;
}
```
---
+ [**Javascript Mathematician**](https://www.codewars.com/kata/55c211cce1ef691d9b000061/train/javascript)
```javascript
function calculate() {
  
  let resOne = 0;
  for (let i=0; i<arguments.length; i++){
    resOne += arguments[i];
  };
  
  let res = resOne;
  return function() {
  for (let i=0; i<arguments.length; i++){
    res += arguments[i];
  };
    
    return res;
  };
};
```
---
+ [**Array Deep Count**](https://www.codewars.com/kata/596f72bbe7cd7296d1000029/train/javascript)
```javascript
function deepCount(a) {
  let result = 0;
  
  function ifArray(arr) {
      result = result + arr.length
      arr.forEach(item => {
        if (Array.isArray(item)) ifArray(item);
      });
    };
  
  ifArray(a);
  return result;
}
```
---
+ [**Length of missing array**](https://www.codewars.com/kata/57b6f5aadb5b3d0ae3000611/train/javascript)
```javascript
function getLengthOfMissingArray(arrayOfArrays) {
  let min = 0;
  let max = 0;
  let result = 0;

  if (!arrayOfArrays || arrayOfArrays.length === 0 || arrayOfArrays.includes(null)) {
    return 0;
  }

  arrayOfArrays = arrayOfArrays.map(arr => arr = arr.length);
  min = Math.min(...arrayOfArrays);
  max = Math.max(...arrayOfArrays);

  for (let i = min; i <= max; i++) {
    if (!arrayOfArrays.includes(i)) {
      result = i;
    }
  }

  if (arrayOfArrays.includes(0)) {
    result = 0;
  }

  return result;
}
```
---
+ [**The Coupon Code**](https://www.codewars.com/kata/539de388a540db7fec000642/train/javascript)
```javascript
function checkCoupon(enteredCode, correctCode, currentDate, expirationDate){
  let current_date = Date.parse(currentDate);
  let expiration_date = Date.parse(expirationDate);
  if( (enteredCode === correctCode) && (expiration_date >= current_date) ){
    return true;
    }
    else {
      return false;
    }
}
```
---
+ [**Unlucky Days**](https://www.codewars.com/kata/56eb0be52caf798c630013c0/train/javascript)
```javascript
function unluckyDays(year) {
  let count = 0;
  for(let i = 0; i < 12; i++) {
    if(new Date(year, i, 13).getDay() === 5) {
      count++;
    }
  }  
  return count;
}
```
---
