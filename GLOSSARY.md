# NewsTok

App personal de Android para estar al día de la actualidad (sobre todo de España) deslizando historias, contrastando cómo las cuentan distintos medios. Un único usuario, sin componente social.

## Language

### Contenido

**Historia**:
Un acontecimiento de actualidad, tal y como lo cubren uno o varios Medios. Es la unidad que se muestra en cada tarjeta del Feed.
_Avoid_: Noticia (ambiguo entre Historia y Artículo), evento, cluster

**Artículo**:
Una pieza publicada por un único Medio sobre una Historia, con su titular y enlace al original.
_Avoid_: Noticia, post, entrada

**Resumen**:
Descripción neutral, en pocas líneas, de qué ha pasado en una Historia, independiente de cómo la encuadre cada Medio.
_Avoid_: Sinopsis, entradilla

**Medio**:
Una publicación periodística cuyos Artículos se recogen (p. ej. El País, Marca, Vandal).
_Avoid_: Fuente, periódico, outlet

**Medio generalista**:
Medio que cubre la actualidad general (El País, ABC…), por oposición a un Medio temático (Marca, Xataka, Vandal…). Solo los generalistas tienen Orientación.
_Avoid_: Medio político, periódico

**Orientación**:
Posición política de un Medio en el eje izquierda / centro / derecha.
_Avoid_: Sesgo, ideología

**Tema**:
Área de interés a la que pertenece una Historia (Política, Fútbol, Videojuegos, Influencers, Vivienda y economía…). Cada Historia tiene un único Tema.
_Avoid_: Categoría, sección, tag

**Peso de Tema**:
Preferencia del usuario sobre un Tema: Más, Normal, Menos u Oculto.
_Avoid_: Prioridad, filtro

**Seguido**:
Equipo, competición, deportista o creador concreto por el que el usuario quiere que las Historias que lo mencionen pesen más dentro de su Tema (p. ej. Real Madrid, Champions, Ibai).
_Avoid_: Favorito, suscripción, follow

**Ámbito**:
Dónde ocurre una Historia: España o Internacional. Es independiente del Tema.
_Avoid_: Sección, región; usar "Internacional" como si fuera un Tema

**Tendencia**:
Asunto del que se está hablando masivamente en redes (X) o en búsquedas (Google) en España en un momento dado.
_Avoid_: Trending topic, hashtag, TT

**Tendencia huérfana**:
Tendencia para la que no se encuentra ningún Artículo; solo se muestra por su nombre, agrupada con otras.
_Avoid_: Tendencia sin noticia

**Última hora**:
Historia con una Cobertura excepcional en muy poco tiempo, que justifica avisar al usuario fuera de la app.
_Avoid_: Breaking news, alerta, urgente

**Actualización**:
Reaparición de una Historia ya vista porque tiene hechos nuevos relevantes, con su Resumen rehecho.
_Avoid_: Update, seguimiento, novedad

### Importancia

**Importancia**:
Cuánto merece una Historia estar arriba en el Feed; combina Cobertura, coincidencia con una Tendencia, peso del Tema y frescura.
_Avoid_: Score, relevancia, ranking

**Cobertura**:
Número de Medios distintos que tienen al menos un Artículo sobre una Historia.
_Avoid_: Alcance, repercusión

### Consumo

**Feed**:
La secuencia finita de Historias nuevas desde la última visita, ordenadas por importancia, que se recorre deslizando.
_Avoid_: Timeline, muro, scroll

**Vista**:
Una Historia que el usuario ya ha pasado en el Feed; no vuelve salvo como Actualización.
_Avoid_: Leída

**Guardada**:
Una Historia que el usuario ha marcado para volver a ella más tarde.
_Avoid_: Favorito, marcador, bookmark

**Al día**:
Estado al que se llega tras recorrer todo el Feed: no quedan Historias nuevas.
_Avoid_: Fin del feed, vacío
