# Embeddings locales para agrupar, OpenCode Go solo para Resúmenes

Agrupar Artículos en Historias se hace con un modelo de embeddings multilingüe ejecutado dentro del propio GitHub Actions, sin API ni límites. El LLM solo se llama para escribir Resúmenes de Historias nuevas o con Actualización, vía el endpoint compatible con OpenAI de OpenCode Go (suscripción que el usuario ya paga), para mantener el coste en 0 €.

## Consequences

- La documentación de OpenCode Go dice que el servicio está pensado para "tráfico típico de agentes de programación". El usuario lo ha revisado y lo acepta, pero el cliente del LLM debe ser intercambiable (una línea de configuración) para poder pasar a Groq o Gemini (capas gratuitas) si hiciera falta.
- Los límites de OpenCode Go son por modelo (tope mensual, 20 % cada 5 h, 50 % semanal): el volumen de Resúmenes debe mantenerse acotado.
