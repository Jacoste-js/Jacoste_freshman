jihyukim

```js
function solution(n, k) {
  function isPrime(n) {
    if (n <= 1 || n.includes(0)) return false;
    for (let i = 2; i <= Math.sqrt(n); i++) if (n % i === 0) return false;
    return true;
  }

  return n
    .toString(k)
    .split('0')
    .filter((el) => isPrime(el)).length;
}
```

daekim

```js
function solution(n, k) {
  let knum = n.toString(k).split('0');
  let tmp;
  let cnt = 0;

  for (let i = 0; i < knum.length; i++) {
    if (+knum[i] === 2) {
      cnt++;
      continue;
    }
    if (+knum[i] % 2 === 0 || +knum[i] === 1 || knum[i] === '') continue;
    tmp = 3;
    while (tmp <= Math.sqrt(+knum[i])) {
      if (+knum[i] % tmp === 0) break;
      tmp += 2;
    }
    if (tmp > Math.sqrt(+knum[i])) cnt++;
  }
  return cnt;
}
```
