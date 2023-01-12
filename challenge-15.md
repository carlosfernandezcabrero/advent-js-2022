# Reto 15: Decorando el árbol de navidad

🔗 [**Enunciado**](https://adventjs.dev/es/challenges/2022/15)

## Solución

``` js
function decorateTree(base) {
  const rules = {
    BP: 'R',
    RP: 'B',
    BR: 'P',
    PR: 'B',
    RB: 'P',
    PB: 'R',
  }
  const heightOfTree = base.split(' ').length

  return Array.from({ length: heightOfTree - 1 }, (_, i) => i).reduce(
    (result) => {
      const level = result[0].split(' ')

      result.splice(
        0,
        0,
        level
          .reduce((acc, current, idx) => {
            if (idx < level.length - 1) {
              const next = level[idx + 1]

              if (next === current) acc.push(current)
              else acc.push(rules[`${current}${next}`])
            }

            return acc
          }, [])
          .join(' ')
      )

      return result
    },
    [base]
  )
}
```

🚀 10 puntos
