# Datos

Este repositorio no incluye los datos. El notebook los descarga directamente de
[SkillCorner Open Data](https://github.com/SkillCorner/opendata) (licencia MIT)
con `kloppy.skillcorner.load_open_data()` y con `requests` para los ficheros
`phases_of_play.csv`.

Partidos utilizados (A-League 2024/25, estado "closed"):
1886347, 1899585, 1925299, 1996435, 2006229, 2011166, 2013725, 2015213 y 2017461.

Por cada partido, SkillCorner publica:

| Fichero | Contenido | Uso en el TFM |
|---|---|---|
| `{id}_match.json` | Metadatos: equipos, jugadores, marcador, dimensiones del campo y sentido de ataque | Equipos, porteros y orientación |
| `{id}_tracking_extrapolated.jsonl` | Una línea por frame (10 fps): balón, posesión y posición (x, y) de los 22 jugadores | Variables espaciales de los dos modelos y posesión del PC-HMM |
| `{id}_phases_of_play.csv` | Fases de juego del proveedor para el equipo con y sin balón | Validación externa (ARI y V-measure) |
