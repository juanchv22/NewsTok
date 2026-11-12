# Pipeline estático en GitHub Actions, estado personal solo en el móvil

No hay servidor: un workflow de GitHub Actions en un repositorio público se ejecuta cada hora, recoge los RSS de los Medios y las Tendencias, agrupa los Artículos en Historias, genera los Resúmenes, puntúa la importancia y publica en GitHub Pages un JSON con las Historias de las últimas ~48 h. La app descarga ese JSON y todas las imágenes en segundo plano y monta el Feed en local, de modo que deslizar nunca toca la red. Lo personal (Historias vistas, guardadas, pesos de Tema) vive solo en el móvil, así que el repo puede ser público sin exponer nada del usuario.

## Considered Options

- **VPS / backend propio**: descartado por coste (requisito: 0 €).
- **Repo privado**: los ~2.000 min/mes gratuitos no alcanzan para una ejecución horaria.
- **Cloudflare Workers cron**: 10 ms de CPU y 50 subrequests por invocación, insuficiente para leer ~20 feeds y agrupar.
- **Todo en el móvil (WorkManager)**: posible, pero el procesado periódico en segundo plano en Android es poco fiable y gasta batería; además la latencia entre swipes exige tener el Feed ya preparado.

## Consequences

- Los workflows programados en repos públicos se desactivan tras 60 días sin actividad; el propio workflow hace commit de su salida, lo que debería contar como actividad.
- El cron de GitHub puede retrasarse o saltarse ejecuciones; usar minutos impares (p. ej. `17 * * * *`).
