jihyukim
```js
function solution(n, k) {
    function isPrime(n) {
        if (n <= 1 || n.includes(0)) return false;
        for (let i = 2; i <= Math.sqrt(n); i++)
            if (n % i === 0) return false;
        return true;
    }
    
    return n.toString(k).split("0").filter(el => isPrime(el)).length;
}
```
