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