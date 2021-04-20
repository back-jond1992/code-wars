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

## Opposite Number

```js

function opposite(number) {
  return(-number);
}

```

## Return Negative

```js

function makeNegative(num) {
  if(num > 0) {
    return(-num);
  } else {
    return num;
  }
}

```

## Remove First and Last Character

```js

function removeChar(str){
    const removedCharString = str.slice(1, -1);
    return removedCharString;
};

```

## String Repeat

```js

function repeatStr (number, string) {
  return string.repeat(number);
}

```

## Reversed Strings

```js

function solution(str){
    return str
    .split("")
    .reverse()
    .join("")
}

```

## Grasshopper - Summation

```js

var summation = function (num) {
  let sum = 0;
  for(let i = 1; i <= num; i++) {
   sum += i;
  }
  return sum;
}

```

## Find the Smallest Integer in the Array

```js

class SmallestIntegerFinder {
  findSmallestInt(args) {
    return Math.min(...args);
  }
}

```

## Remove String Spaces

```js

function noSpace(str){
   return str.replace(/\s+/g, '');
}

```

## Convert Boolean Values to Strings

```js

function boolToWord( bool ){
  if(bool === true) {
    return "Yes";
  } else {
    return "No";
  }
}

```

## Convert a Number to a String

```js

function numberToString(num) {
  return num.toString();
}

```

## Counting Sheep

```js

function countSheeps(arrayOfSheep) {
  let counter = [];
  for(let i = 0; i < arrayOfSheep.length; i++) {
    if(arrayOfSheep[i] === true) {
      counter.push(arrayOfSheep[i]);
    }
  }
  return counter.;
}

```

## Sqaured Sum

```js

function squareSum(arr){
    let arrayOfSquaredNumbers = arr.map(x => x ** 2)
    let sumOfSquaredNumbers = arrayOfSquaredNumbers.reduce(function(a, b) {
      return a + b;
    }, 0);
  return sumOfSquaredNumbers;
}

```

## Century From Year

```js

function century(year) {
  return Math.ceil(year/100);
}

```