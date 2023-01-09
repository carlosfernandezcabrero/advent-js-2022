# Reto 7: Haciendo inventario de regalos

🔗 [**Enunciado**](https://adventjs.dev/es/challenges/2022/7)

## Solución

``` js
function getGiftsToRefill(a1, a2, a3) {
  const array = [...new Set(a1), ...new Set(a2), ...new Set(a3)]

  return array.reduce((acc, current) => {
    const arrayJoined = array.join('')

    if (
    arrayJoined.length - current.length ===
    arrayJoined.replaceAll(current, '').length
    ) {
      acc.push(current)
    }
    
    return acc
  }, [])
}
```

🚀 120 puntos
