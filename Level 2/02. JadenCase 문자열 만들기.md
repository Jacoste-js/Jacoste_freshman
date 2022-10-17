jihyukim

```js
function solution(s) {
  return s.toLowerCase().replace(/\b[a-z]/g, (char) => char.toUpperCase());
}
```

jabae

```js
function solution(s) {
  return s
    .toLowerCase()
    .split(' ')
    .map((x) => {
      if (typeof x[0] === 'string') x = x.replace(x[0], x[0].toUpperCase());
      return x;
    })
    .join(' ');
}
```

daekim

```js
function solution(s) {
  var answer = '';
  let arr = [];

  for (let i = 0; i < s.length; i++) arr[i] = s[i];
  answer += arr[0].toUpperCase();
  for (let i = 1; i < s.length; i++) {
    if (arr[i - 1] === ' ') answer += arr[i].toUpperCase();
    else answer += arr[i].toLowerCase();
  }
  return answer;
}
```
