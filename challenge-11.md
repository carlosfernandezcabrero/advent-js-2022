# Reto 11: Papá Noel es Scrum Master

🔗 [**Enunciado**](https://adventjs.dev/es/challenges/2022/11)

## Solución

``` js
function getCompleted(part, total) {
  if (part === total) return '1/1'

  const toSeconds = (time) => {
    const [h, m, s] = time.split(":")  
    return (Number(h) * 3600) + (Number(m) * 60) + Number(s)
  }

  const partSeconds = toSeconds(part)
  const totalSeconds = toSeconds(total)

  const maxDivisor = Math.min(partSeconds, totalSeconds)
  const factors = Array.from({ length: maxDivisor }, (_, index) => index + 1)
  const factorsReversed = factors.reverse()
  const divisor = factorsReversed.reduce(
    (_, current) => {
      if (partSeconds % current === 0 && totalSeconds % current === 0) {
        factors.splice(1)
      }
      return current
    }, 0)

  return `${partSeconds / divisor}/${totalSeconds / divisor}`
}
```

🚀 10 puntos
