# 8 kyu Challenges

## Even or Odd

```js

function even_or_odd(number) {
  if(number % 2 === 0) {
    return "Even";
  } else {
    return "Odd";
  }
  // ...
}

```

## You're a Square

``` js

var isSquare = function(n){
  return n >= 0 && Math.sqrt(n) % 1 === 0;
  }

  ```

## Sum of Positive

```js

function positiveSum(arr) {
  let sumOfPositiveValues = 0;
  for(let i = 0; i < arr.length; i++) {
    if(arr[i] > 0) {
      sumOfPositiveValues += arr[i];
    }
  }
  return sumOfPositiveValues;
}

```