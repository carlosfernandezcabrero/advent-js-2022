# Reto 2: Nadie quiere hacer horas extras

🔗 [**Enunciado**](https://adventjs.dev/es/challenges/2022/2)

## Solución

``` js
function countHours(year, holidays) {
  return holidays.reduce((acc, current) => {
    const parts = current.split('/')
    const workDay = new Date(year, parts[0] - 1, parts[1]).getDay()

    if ([1, 2, 3, 4, 5].includes(workDay)) return acc + 2

    return acc
  }, 0)
}
```

🚀 101 puntos
