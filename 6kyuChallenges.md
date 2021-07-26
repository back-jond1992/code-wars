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

function digital_root(n) {
  if (n < 10) return n;  
  
  return digital_root(
    n.toString().split('').map(Number).reduce((a, b) => a + b, 0))
}
  
```

## Stop gninnipS My sdroW!

```js

function spinWords(string){
  let splitString = string.split(" ");
  let result = splitString.map(function(word) {
    if(word.length >= 5) {
      return word.split("").reverse().join("");
    } else {
    return word}
  }).join(" ")
  return result
}

```

## Palindrome Checker (FREECODECAMP)

```js

function palindrome(str) {
  let str1 = str.toLowerCase().replace(/[\W_]/g,"");
  let str2 = str1.split("").reverse().join("");
  return (str1 === str2)
}

palindrome("not a palindrome");

```

## Roman Numeral Converter (FREE CODE CAMP)

```js

function convertToRoman(num) {
  if(typeof num !== "number") {
    return false;
  }

  let digits = String(+num).split(""),
  key = ["","C","CC","CCC","CD","D","DC","DCC","DCCC","CM",
  "","X","XX","XXX","XL","L","LX","LXX","LXXX","XC",
  "","I","II","III","IV","V","VI","VII","VIII","IX"],
  roman_num = "",
  
  i = 3;
  while(i--)
  roman_num = (key[+digits.pop() + (i * 10)] || "") + roman_num;
  return Array(+digits.join("") + 1).join("M") + roman_num;
}

convertToRoman(36);

```

## Caesars Cipher (FREE CODE CAMP)

```js

function rot13(str) {
let newStr = str.split("");
let cipheredStr = []
  for(let i = 0; i < newStr.length; i++) {
    switch(newStr[i]) {
        case "A":
        cipheredStr.push("N");
        break;
        case "B":
        cipheredStr.push("O")
        break;
        case "C":
        cipheredStr.push("P")
        break;
        case "D":
        cipheredStr.push("Q")
        break;
        case "E":
        cipheredStr.push("R");
        break;
        case "F":
        cipheredStr.push("S")
        break;
        case "G":
        cipheredStr.push("T")
        break;
        case "H":
        cipheredStr.push("U")
        break;
        default:
        case "I":
        cipheredStr.push("V");
        break;
        case "J":
        cipheredStr.push("W")
        break;
        case "K":
        cipheredStr.push("X")
        break;
        case "L":
        cipheredStr.push("Y")
        break;
        case "M":
        cipheredStr.push("Z");
        break;
        case "N":
        cipheredStr.push("A")
        break;
        case "O":
        cipheredStr.push("B")
        break;
        case "P":
        cipheredStr.push("C")
        break;
        case "Q":
        cipheredStr.push("D");
        break;
        case "R":
        cipheredStr.push("E")
        break;
        case "S":
        cipheredStr.push("F")
        break;
        case "T":
        cipheredStr.push("G")
        break;
        case "U":
        cipheredStr.push("H");
        break;
        case "V":
        cipheredStr.push("I")
        break;
        case "W":
        cipheredStr.push("J")
        break;
        case "X":
        cipheredStr.push("K")
        break;
        case "Y":
        cipheredStr.push("L");
        break;
        case "Z":
        cipheredStr.push("M")
        break;
        case " ":
        cipheredStr.push(" ")
        break;
        case "!":
        cipheredStr.push("!")
        break;
        case "?":
        cipheredStr.push("?")
        break;
        case ".":
        cipheredStr.push(".")
        break;
        case ",":
        cipheredStr.push(",")
        break;
    } 
  }
  return cipheredStr.join("")
}

```

## Telephone Number Validator(FREE CODE CAMP)

```js

function telephoneCheck(str) {
  if(str.match(/^(1\s|1|)?((\(\d{3}\))|\d{3})(\-|\s)?(\d{3})(\-|\s)?(\d{4})$/)) {
    return true
  } else {
    return false
  }
}

telephoneCheck("555-555-5555");

```

## Who likes it?

```js

function likes(names) {
  let likes = -2
  for(let i = 0; i < names.length; i ++) {
  likes += 1 
  }
  if(names.length == 0) {
    return 'no one likes this'
  } else if (names.length == 1) {
    return names + ' likes this'
  } else if (names.length == 2) {
    return names[0] + ' and ' + names[1] + ' like this'
  }  else if (names.length == 3) {
    return names[0] + ', ' + names[1] + ' and ' + names[2] + ' like this'
  } else if (names.length > 3) {
    return names[0] + ', ' + names[1] + ' and ' + likes + ' others like this'
  }   
}

```

## Counting Duplicate

```js

function duplicateCount(text){
  let counter = 0
  let sortedString = text.toLowerCase().split("").sort().join("");
  let groupedString = sortedString.match(/([a-z])\1*/g)
  if(groupedString == null) {
    return 0
  } else if (groupedString != null) {
    for(let i = 0; i < groupedString.length; i++) {
      if(groupedString[i].length > 1) {
      counter += 1
      }
    }
  }
  return counter
}

```

## Persistent Bugger