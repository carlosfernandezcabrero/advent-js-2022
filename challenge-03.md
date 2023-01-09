# Reto 3: ¿Cuántas cajas de regalos puede llevar Papá Noel?

🔗 [**Enunciado**](https://adventjs.dev/es/challenges/2022/3)

## Solución

``` js
function distributeGifts(packOfGifts, reindeers) {
  const giftsWeight = packOfGifts.reduce((acc, gift) => acc + gift.length, 0)
  const reindeersLimitWeight = reindeers.reduce(
    (acc, reindeer) => acc + reindeer.length * 2,
    0
  )

  return Math.trunc(reindeersLimitWeight / giftsWeight)
}
```

🚀 142 puntos
