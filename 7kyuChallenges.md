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
