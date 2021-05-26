# 6kyu Challenges

## Multiples of 3 or 5

```js

function solution(number){
  let sumOfMultiplesOfThreeAndFive = 0;
  for(let i = 1; i < number; i++) {
    if(i % 3 === 0 || i % 5 === 0) {
      sumOfMultiplesOfThreeAndFive += i;
    }
  }
  return sumOfMultiplesOfThreeAndFive;
}

```

## Find The Odd Int

```js

function findOdd(A) {
  let count = 0;
  for(let i = 0; i < A.length; i++) {
    for(let j = 0; j < A.length; j++) {
      if(A[i] == A[j]) {
        count ++
      }
    }
    if(count % 2 != 0) {
      return A[i]
    }
  }
}

```

## Sum of Digits/Digital Roots

```js

function digital_root(N) {
  let sumOfDigits = N.toString().split('').map(Number).reduce((a, b) => a + b, 0)
  let counter = 10
  if(sumOfDigits < counter) {
    return sumOfDigits
  } else if(sumOfDigits >= sumOfDigits) {
    return sumOfDigits.toString().split('').map(Number).reduce((a, b) => a + b, 0)
  }
}
  
```