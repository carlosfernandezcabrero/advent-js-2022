# Reto 21: Creando la tabla de regalos

🔗 [**Enunciado**](https://adventjs.dev/es/challenges/2022/21)

## Solución

``` js
function printTable(gifts) {
  const giftsWithHeader = [...gifts]
  giftsWithHeader.splice(0, 0, { name: 'Gift', quantity: 'Quantity' })

  const giftLen = Math.max(...giftsWithHeader.map(({ name }) => name.length))
  const quantityLen = Math.max(
    ...giftsWithHeader.map(({ quantity }) => `${quantity}`.length)
  )
  const tableLen = giftLen + quantityLen + 7

  return `${'+'.repeat(tableLen)}\n| Gift${' '.repeat(
    giftLen - 'Gift'.length
  )} | Quantity${' '.repeat(quantityLen - 'Quantity'.length)} |\n| ${'-'.repeat(
    giftLen
  )} | ${'-'.repeat(quantityLen)} |\n${gifts.reduce(
    (body, { name, quantity }) => {
      return (body += `| ${name}${' '.repeat(
        giftLen - name.length
      )} | ${quantity}${' '.repeat(quantityLen - `${quantity}`.length)} |\n`)
    },
    ''
  )}${'*'.repeat(tableLen)}`
}
```

🚀 200 puntos
