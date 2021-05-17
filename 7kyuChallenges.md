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

## Complementary DNA

```js

function DNAStrand(dna){
 let dnaArray = dna.split("");
 let oppossiteStrand = []
  for(let i = 0; i < dnaArray.length; i++) {
    switch(dnaArray[i]) {
        case "A":
        oppossiteStrand.push("T");
        break;
        case "T":
        oppossiteStrand.push("A")
        break;
        case "G":
        oppossiteStrand.push("C")
        break;
        case "C":
        oppossiteStrand.push("G")
        break;
        default:
        return "This is not DNA"
    } 
  }
  return oppossiteStrand.join("")
}

```

## List Filtering 

```js

function filter_list(list) {
  return list.filter((value) => typeof value === "number");
}

```

## Sum of Numbers

```js

function getSum(a,b){
  let min = Math.min(a,b);
  let max = Math.max(a,b);
  let result = 0;
  for(let i = min; i <= max; i++) {
    result += i;
  }
  return result
}

```

## Credit Card Mask

```js

function maskify(cc) {
  if(cc.length > 4) {
    return cc.split("").slice(0, -4).map((value) => value = "#").join("") + cc.slice(-4)
    } else {
      return cc;
    }
  }

  ```

## Growth of Population

```js

function nbYear(p0, percent, aug, p) {
  let numberOfYears = 0;
  while(p0 < p) {
  p0 = p0 + p0 * (percent/100) + aug;
  numberOfYears ++
  }
  return numberOfYears;
}

```

## Sum of Two Lowest Integers

```js

function sumTwoSmallestNumbers(numbers) {  
  let sortedNumbers = numbers.sort((a, b) => a - b);
  return sortedNumbers[0] + sortedNumbers[1];
}

```

## Two to One

```js

function longest(s1, s2) {
  return s1.concat(s2).replace(/(.)(?=.*\1)/g, "").split("").sort().join("");
}

```

## Sum of Odd Numbers

```js

function rowSumOddNumbers(n) {
	return Math.pow(n, 3);
}

```

## Regex Validate Pin Code

```js

function validatePIN (pin) {
  if(pin.match(/^\d{4}$/) || pin.match(/^\d{6}$/)) {
    return true
  } else {
    return false
  }
}

```

## Printer Errors

```js

function printerError(s) {
  let total = s.length;
  let good = s.match(/[a-m]/g).length;
  let bad = s.length - good;
  return bad + '/' + total;
}

```

## Find The Next Perfect Square

```js

function findNextSquare(sq) {
  if(Math.sqrt(sq) % 1 === 0) {
    let squareRoot = Math.sqrt(sq);
    return (squareRoot + 1) ** 2;
  } else {
  return -1;
  }
}

```

## Categorize New Member

```js

function openOrSenior(data){
  let membersList = [];
  for(let i = 0; i < data.length; i++) {
   if(data[i][0] >= 55 && data[i][1] > 7) {
     membersList.push('Senior')
  }else {
    membersList.push('Open')
    }
  }
  return membersList;
}

```

## Ones and Zeros

```js

const binaryArrayToNumber = arr => {
  const binaryString = arr.join("");
  return parseInt(binaryString, 2);
};

```

## Friends or Foe

```js

function friend(friends){
   return friends.filter((friend) => friend.length == 4)
}

```