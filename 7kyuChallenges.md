## Vowel Count

```js

function getCount(str) {
  return str.replace(/[^aeiou]/gi, "").length;
  }

  ```

## Mumbling

```js

function accum(str) {
  let letters = str.split('');
  let result = [];
  for (let i = 0; i < letters.length; i++) {
    result.push(letters[i].toUpperCase() + Array(i + 1).join(letters[i].toLowerCase()));
  }
  return result.join('-');
}

```

## Disemvowel Trolls

```js

function disemvowel(str) {
  return str.replace(/[aeiou]/gi, "");
}

```

## Highest and Lowest

```js

function highAndLow(numbers){
  let numbersArray = numbers.split(' ').map(Number);
  let min = Math.min(...numbersArray)
  let max = Math.max(...numbersArray)
  let result = max.toString() + " " + min.toString();
  return result;
}

```

## Square Every Digit

```js

function squareDigits(num){
  let arrayOfSquaredDigits = [];
  let digits = num.toString().split("").map(Number);
  for(let i = 0; i < digits.length; i++) {
    arrayOfSquaredDigits.push(digits[i] ** 2);
  }
  return Number(arrayOfSquaredDigits.join(""));
}

```

## Descending Order

```js

function descendingOrder(n){
  return Number(n.toString().split("").sort(function(a, b) {return b-a}).join(""));
}

```
