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

## Get the Middle Character

```js

function getMiddle(s) {
  let length = s.length;
  let middle = Math.floor(length / 2);
  if(length % 2 === 0) {
    return s[middle - 1] + s[middle];
  } else {
    return s[middle];
  }
}

```

## Isograms

```js

function isIsogram(str){
  let result = str.toLowerCase().split("").sort().join("").match(/(.)\1+/g);
  if(result === null) {
    return true;
  } else {
    return false;
  }
}

```

## Shortest Word

```js

function findShort(str){
  let arrayOfWords = str.split(" ");
  let shortestWord = 100;
  
  for(let i = 0; i < arrayOfWords.length; i++) {
    if(arrayOfWords[i].length < shortestWord) {
      shortestWord = arrayOfWords[i].length;
    }
  }
  return shortestWord;
}

```

## Jaden Casing Strings

```js

String.prototype.toJadenCase = function () {
  return this.replace(/(^\w{1})|(\s+\w{1})/g, letter => letter.toUpperCase());
};

```

## Exes and Ohs

```js

function XO(str) {
  let X = [];
  let O = [];
  let arr = str.toLowerCase().split("");
  for(let i = 0; i < arr.length; i++)
    if(arr[i] === 'x') {
      X.push(arr[i]);
    } else if(arr[i] === 'o') {
      O.push(arr[i]);
    } 
  
  if(X.length === O.length) {
    return true;
  } else{
    return false;
  }
}

```
