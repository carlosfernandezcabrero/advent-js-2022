# Reto 8: ¡Necesitamos un mecánico

🔗 [**Enunciado**](https://adventjs.dev/es/challenges/2022/8)

## Solución

``` js
function checkPart(part) {
  const partSeparated = part.split('')

  if (part === [...partSeparated].reverse().join('')) return true

  return partSeparated.some((_, idx) => {
    const possiblePalindrome = [...partSeparated]
    possiblePalindrome.splice(idx, 1)

    return possiblePalindrome.join('') === possiblePalindrome.reverse().join('')
  })
}
```

🚀 160 puntos
