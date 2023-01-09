# Reto 9: Las locas luces de navidad

🔗 [**Enunciado**](https://adventjs.dev/es/challenges/2022/9)

## Solución

``` js
function countTime(leds) {
  const turnOnLeds = (leds) => {
    const actualLeds = leds.map((led, idx) => {
      if (
        led === 0 &&
        ((idx === 0 && leds.at(-1) === 1) || leds[idx - 1] === 1)
      )
        return 1

      return led
    })

    if (new Set(actualLeds).size > 1) return 1 + turnOnLeds(actualLeds)

    return 1
  }

  if (leds.some((l) => l === 0)) return turnOnLeds(leds) * 7

  return 0
}
```

🚀 10 puntos
