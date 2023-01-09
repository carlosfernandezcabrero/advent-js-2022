# Reto 17: Llevando los regalos en sacos

🔗 [**Enunciado**](https://adventjs.dev/es/challenges/2022/17)

## Solución

``` js
function carryGifts(gifts, maxWeight) {
  let currentWeight = 0

  return gifts
    .filter((gift) => gift.length <= maxWeight)
    .reduce((acc, current) => {
      const currentLength = current.length

      if (currentWeight + currentLength > maxWeight) {
        acc.push([current])
        currentWeight = currentLength
        return acc
      }

      if (currentWeight === 0) acc.push([])

      acc.at(-1).push(current)
      currentWeight += currentLength

      return acc
    }, [])
    .map((bag) => bag.join(' '))
}
```

🚀 140 puntos
