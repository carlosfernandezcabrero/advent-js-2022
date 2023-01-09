# Reto 22: La iluminación en sintonía

🔗 [**Enunciado**](https://adventjs.dev/es/challenges/2022/22)

## Solución

``` js
function checkStepNumbers(systemNames, stepNumbers) {
  return Object.values(
    systemNames.reduce((systems, name, idx) => {
      if (Object.hasOwn(systems, name)) systems[name].push(stepNumbers[idx])
      else if (!Object.hasOwn(systems, name)) systems[name] = [stepNumbers[idx]]

      return systems
    }, {})
  ).every(
    (system) =>
      system.join('') === system.sort().join('') &&
      system.length === new Set(system).size
  )
}
```

🚀 140 puntos
