# Reto 19: Ordenando los regalos

🔗 [**Enunciado**](https://adventjs.dev/es/challenges/2022/19)

## Solución

``` js
function sortToys(toys, positions) {
  return positions
    .map((position, index) => ({ position, toy: toys[index] }))
    .sort((a, b) => a.position - b.position)
    .map(({ toy }) => toy)
}
```

🚀 300 puntos
