# Problems 1 to 100

## Problem 1: Multiples of 3 and 5
[Link](https://projecteuler.net/problem=1)

[fcc link](https://www.freecodecamp.org/learn/project-euler/project-euler-problems-1-to-100/problem-1-multiples-of-3-and-5)
```js
function multiplesOf3and5(number) {
  let res = 0;

  for(let i = 0; i<number; i++) {
    if(i%3==0 && i%5==0) {
      res += i;
    } else if(i%3==0) {
      res += i;
    } else if(i%5==0) {
      res += i;
    }
  }
  return res;
}
```
