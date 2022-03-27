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
+ **Array Deep Count**
