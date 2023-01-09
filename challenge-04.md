# Reto 4: Una caja dentro de otra caja y otra

🔗 [**Enunciado**](https://adventjs.dev/es/challenges/2022/4)

## Solución

``` js
function fitsInOneBox(boxes) {
  return boxes
    .sort(
      (a, b) => Math.min(...Object.values(a)) - Math.min(...Object.values(b))
    )
    .every((box, idx) => {
      if (idx === boxes.length - 1) return true

      const nextBox = boxes[idx + 1]

      if (box.l >= nextBox.l || box.w >= nextBox.w || box.h >= nextBox.h) return false

      return true
    })
}
```

🚀 110 puntos
