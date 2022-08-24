# standard-deviation
Simple standard deviation function

```javascript
function std(numArray, stdOnly = true) {
    // N the size of the population
    // x each value from the population
    // μ the population mean
    // σ population standard deviation
    const N = numArray.length;
    const μ = numArray.reduce((curr, x) => curr + x) / N;
    const σ = Math.sqrt(
        numArray.reduce((curr, x) => curr + (x - μ) ** 2, 0) / N
    )

    return stdOnly ? σ : { std: σ, mean: μ, populationSize: N }
}
```
