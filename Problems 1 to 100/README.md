# Problems 1 to 100

## Problem 1: Multiples of 3 and 5
[Link](https://projecteuler.net/problem=1), [fcc link](https://www.freecodecamp.org/learn/project-euler/project-euler-problems-1-to-100/problem-1-multiples-of-3-and-5)
```js
function multiplesOf3and5(number) {
  let res = 0;

  for(let i = 3; i < number; i++) {
    if(i % 3 == 0 || i % 5 == 0) {
      res += i;
    }
  }
  return res;
}
```

## Problem 2: Even Fibonacci Numbers
[Link](https://projecteuler.net/problem=2), [fcc link](https://www.freecodecamp.org/learn/project-euler/project-euler-problems-1-to-100/problem-2-even-fibonacci-numbers)
```js
function fiboEvenSum(n) {
  let res = 0;

  let temp1 = 1, temp2 = 1;
  for(let i = 1; i <= n;) {
    if(i % 2 == 0) {
      res += i;
    }
    i = temp1 + temp2;
    temp1 = temp2;
    temp2 = i;
    // console.log(i);
  }
  return res;
}
```

## Problem 3: Largest prime factor
[Link](https://projecteuler.net/problem=3), [fcc link](https://www.freecodecamp.org/learn/project-euler/project-euler-problems-1-to-100/problem-3-largest-prime-factor)
```js
function largestPrimeFactor(number) {
  let n = number;
  let ans = 1;

  if(n <= 1) return 1;

  while(n % 2 == 0) { 
    ans = 2; 
    n /= 2;
  }

  while(n % 3 == 0) { 
    ans = 3;
    n /= 3 
  }

  for(let i = 5; i * i <= n; i += 6) {
    while(n % i == 0) {
      ans = i;
      n /= i;
    }
    while(n % (i+2) == 0) {
      ans = i + 2;
      n /= (i + 2);
    }
  }

  // edge cases: 13, 52
  if(n > 3) ans = n;

  // console.log(ans);
  return ans;
}
```
