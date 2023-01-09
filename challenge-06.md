# Reto 6: Creando adornos navideños

🔗 [**Enunciado**](https://adventjs.dev/es/challenges/2022/6)

## Solución

``` js
function createCube(size) {
  let basicStructure = ''

  Array.from({ length: size }, (_, i) => i + 1).forEach((i) => {
    basicStructure +=
      ' '.repeat(size - i) + '/\\'.repeat(i) + '_\\'.repeat(size) + '\n'
  })
  Array.from({ length: size }, (_, i) => size - i).forEach((i) => {
    basicStructure += ' '.repeat(size - i) + '\\/'.repeat(i) + '_/'.repeat(size)
    if (i !== 1) basicStructure += '\n'
  })

  return basicStructure
}
```

🚀 120 puntos
