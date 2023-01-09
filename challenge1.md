# Reto 1: ¡Automatizando envolver regalos de navidad

🔗 [**Enunciado**](https://adventjs.dev/es/challenges/2022/1)

## Solución

``` js
function wrapping(gifts) {
  const WRAPPER_CHARACTER = '*'

  return gifts.map((gift) => {
    const lengthOfWrapper = gift.length + 2
    const wrapper = WRAPPER_CHARACTER.repeat(lengthOfWrapper)

    return `${wrapper}\n${WRAPPER_CHARACTER}${gift}${WRAPPER_CHARACTER}\n${wrapper}`
  })
}
```

🚀 131 puntos
