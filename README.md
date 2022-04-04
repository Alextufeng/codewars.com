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
+ [**Let's Recycle!**](https://www.codewars.com/kata/5b6db1acb118141f6b000060/train/javascript)
```javascript
function recycle(array) {
  let materials = { "paper": [], "glass": [], "organic": [], "plastic": [] }
  array.forEach(obj => {
    materials[obj.material].push(obj.type);
    if(obj.secondMaterial)
      materials[obj.secondMaterial].push(obj.type);
  });
  return Object.values(materials); 
}
```
---
+ [**Run-length encoding**](https://www.codewars.com/kata/546dba39fa8da224e8000467/train/javascript)
```javascript
function runLengthEncoding(str) {
    let arr = [],
        counter = 1;

    for (let i = 0; i < str.length; i++) {
        if (str[i] === str[i + 1]) {
            counter++;
        } else {
            arr.push([counter, str[i]]);
            counter = 1;
        }
    }
    return arr;
}
```
---
+ [**Can you keep a secret?**](https://www.codewars.com/kata/5351b35ebaeb67f9110012d2/train/javascript)
```javascript
function createSecretHolder(secret) {
  let secr = secret;
  function setSecret(n) {
    secret = n;
  };
  function getSecret() {
    return secret;
  };
  let obj = {
    setSecret: setSecret,
    getSecret: getSecret
  };
  return obj;
};
```
---
+ [**Closures and Scopes**](https://www.codewars.com/kata/526ec46d6f5e255e150002d1)
```javascript
function createFunctions(n) {
  let callbacks = [];

  for (let i=0; i<n; i++) {
    callbacks.push(function() {
      return i;
    });
  }
  return callbacks;
}
```
---
+ [**Sorting by bits**](https://www.codewars.com/kata/59fa8e2646d8433ee200003f/train/javascript)
```javascript
function sortByBit(arr) {
  function countUnits(binaryNum){
  let arr=binaryNum.toString(2).split("");
  let sum=0;
  arr.map(el=>sum+=+el);
  return sum;
}
  arr.sort((a,b)=>{
let res=countUnits(a)-countUnits(b);
if(res<0) return -1;
else if(res===0) return a-b;
else return 1;
  })
 return arr;
}
```
---
+ [Nuclear Missile Manager](https://www.codewars.com/kata/567ed5db4089538eea000010/train/javascript)
```javascript
function launchAll(launchMissile) {
  for(let i = 0; i < 5; i++) {
    setTimeout(function() {
      launchMissile(i);
    }, i * 1000);
  }
}
```
---
+ [**Human readable duration format**](https://www.codewars.com/kata/52742f58faf5485cae000b9a/train/javascript)
```javascript
function formatDuration (seconds) {
  let time = { year: 31536000, day: 86400, hour: 3600, minute: 60, second: 1 },
      res = [];

  if (seconds === 0) return 'now';

  for (let key in time) {
    if (seconds >= time[key]) {
      let val = Math.floor(seconds/time[key]);
      res.push(val += val > 1 ? ' ' + key + 's' : ' ' + key);
      seconds = seconds % time[key];
    }
  }
  return res.length > 1 ? res.join(', ').replace(/,([^,]*)$/,' and'+'$1') : res[0]
}
```
