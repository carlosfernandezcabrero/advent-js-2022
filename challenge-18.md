# Reto 18: ¡Nos quedamos sin tinta

🔗 [**Enunciado**](https://adventjs.dev/es/challenges/2022/18)

## Solución

``` js
function dryNumber(dry, numbers) {
  return Array.from({ length: numbers }, (_, i) => i)
    .filter((number) => `${number + 1}`.includes(dry))
    .map((number) => number + 1)
}
```

🚀 200 puntos
