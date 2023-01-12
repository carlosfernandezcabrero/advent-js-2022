# Reto 12: Trineos eléctricos, ¡guau

🔗 [**Enunciado**](https://adventjs.dev/es/challenges/2022/12)

## Solución

``` js
function selectSleigh(distance, sleighs) {
  const result = sleighs
    .reverse()
    .find((sleigh) => sleigh.consumption * distance <= 20)
  return result ? result.name : null
}
```

🚀 260 puntos
