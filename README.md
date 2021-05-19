```javascript
const ropeLength = process.argv[4] || 10

const parts = n => {

    if (n == 0 || n == 1) return 0

    let max = 0

    for (let i = 1; i < n; i++) {
        max = Math.max(max, Math.max(i * (n - i), parts(n - i) * i))
    }

    return max

}

console.log(`Rope length ${ropeLength}: ${parts(ropeLength)} combinations`)
```
