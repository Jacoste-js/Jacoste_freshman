jihyukim
```js
function solution(s) {
    return s.toLowerCase().replace(/\b[a-z]/g, char => char.toUpperCase());
}
```

jabae
```js
function solution(s) {
    return s.toLowerCase().split(" ").map((x) => {
        if (typeof x[0] === 'string')
            x = x.replace(x[0], x[0].toUpperCase());
        return x;
    }).join(" ")
}
```
