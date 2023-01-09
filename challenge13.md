# Reto 13: Backup de los archivos de Papa Noel

🔗 [**Enunciado**](https://adventjs.dev/es/challenges/2022/13)

## Solución

``` js
function getFilesToBackup(lastBackup, changes) {
  return [
    ...new Set(
      changes
        .filter((change) => change[1] > lastBackup)
        .map((file) => file[0])
        .sort((a, b) => a - b)
    )
  ]
}
```

🚀 300 puntos
