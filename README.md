# Shin Megami Tensei IV: Apocalypse — Traducción al castellano

Traducción al español de España de **Shin Megami Tensei IV: Apocalypse** para Nintendo 3DS, realizada sobre la **edición USA en inglés**.

La primera opción es el parche **LayeredFS**; también hay un **XDELTA** alternativo. Necesitas tu propia copia del juego: ninguna descarga incluye una ROM.

## Estado

Versión **1.0**: guion, interfaz de texto y subtítulos narrativos.

| Contenido | Alcance |
|---|---|
| Guion extraído | 36.682 entradas traducidas; 283 entradas vacías en la fuente |
| Tablas | 5.309 campos traducidos de objetos, habilidades, misiones e interfaz |
| Ejecutable | 910 cadenas traducidas mediante `code.ips` |
| Escenas de vídeo | 53 subtítulos en 12 vídeos, incluidos los mensajes del móvil del epílogo |
| Fuente | Caracteres españoles en los cuatro tamaños originales |
| Gráficos | «FIN DE PARTIDA»; se conserva el resto del diseño de marca |

Las cifras incluyen repeticiones y recursos residuales: no son un porcentaje del juego visible. Se mantienen nombres propios, nombres de hechizos y términos de la saga según la biblia editorial. La revisión ha unificado PS/PM y corregido maquetación y expresiones ambiguas.

Los vídeos mantienen ambos ojos del 3D. El audio se conserva como PCM con muestras idénticas al original; para cubrir los subtítulos ingleses se añade una banda negra con la fuente del juego. La recompresión puede suavizar la imagen.

### Comprobaciones y límites

Se han comprobado la reinserción de todo el corpus, los controles, los tamaños de las tablas, el parche del ejecutable y los glifos. Los 53 subtítulos se han revisado después de decodificar los vídeos generados, y se han contrastado sus fotogramas y el audio con las fuentes.

La prueba jugable en **Azahar 2126.0** cubre el arranque, menús iniciales, introducción y primeros diálogos. **La revisión de una partida completa y la prueba en consola física siguen pendientes.** No se certifican todas las ventanas, elecciones ni contenido descargable.

Se conservan logotipos, rótulos grandes, botones gráficos como Back/OK y algunas cartelas ambientales en su idioma original. En el epílogo, los mensajes del móvil llevan traducción como subtítulos y conservan su gráfico original. Las voces siguen en inglés.

La traducción y la revisión editorial se han realizado con asistencia de modelos; no se atribuye una revisión humana independiente.

## Descarga

1. **LayeredFS — primera opción:** [shinivapoc-es-v1.0.zip](https://github.com/johanderohan/shin-megami-tensei-iv-apocalypse-traduccion-es/releases/download/v1.0/shinivapoc-es-v1.0.zip), para Luma3DS o Azahar.
2. **XDELTA — alternativa:** [shinivapoc-es-v1.0.xdelta](https://github.com/johanderohan/shin-megami-tensei-iv-apocalypse-traduccion-es/releases/download/v1.0/shinivapoc-es-v1.0.xdelta), para crear una ROM `.3ds` ya traducida.

Ambos contienen la misma traducción. Elige uno de los dos métodos.

SHA-256 del ZIP: `e3343dd54e294e1546197a419f313b4775a6a7c59b9f0a3e0c0e5b2ff6c9464b`.

SHA-256 del XDELTA: `3b747c694c261202262a95a8c9c6d408acf745aea5eb0241ac7d076d5db23bac`.

## Versión necesaria

| Dato | Valor |
|---|---|
| Edición | USA, juego base sin otros parches |
| Código de producto | `CTR-P-BG4E` |
| Title ID | `000400000019A200` |
| ROM usada en las pruebas | `Shin Megami Tensei IV - Apocalypse (USA).3ds` |
| Tamaño de esa ROM | 2.147.483.648 bytes |
| SHA-256 de esa ROM descifrada | `aebfb99b1f63c3f34ac5a11f8c90b3acd0a5dbc1f56cc436e0d521dbab5128eb` |

El **XDELTA exige esta ROM exacta** y su SHA-256 debe coincidir. Para LayeredFS, la huella identifica el volcado de prueba; una instalación digital o un contenedor distinto no tendrán necesariamente esa huella. El parche está dirigido al juego base USA; no es compatible con la edición japonesa ni europea y no se ha verificado con actualizaciones u otros mods.

## Cómo instalar

### Opción 1: LayeredFS en Nintendo 3DS con Luma3DS

1. Extrae el ZIP y copia la carpeta `luma` a la raíz de la tarjeta SD.
2. Comprueba que queden `luma/titles/000400000019A200/romfs/` y `luma/titles/000400000019A200/code.ips`.
3. En la configuración de Luma3DS, activa **Enable game patching** y guarda los cambios.
4. Inicia tu copia USA del juego.

### Opción 1: LayeredFS en Azahar

1. Haz clic derecho sobre el juego USA y abre su carpeta de modificaciones.
2. Copia allí **el contenido** de `luma/titles/000400000019A200/` del ZIP: la carpeta `romfs` y el archivo `code.ips`.
3. Cierra y vuelve a iniciar el juego. No cargues un estado rápido creado con otra versión del parche.

Para LayeredFS, ambas partes, `romfs` y `code.ips`, son necesarias. Retira primero otros parches de ese juego para evitar mezclar archivos. Este método no requiere modificar la ROM. Para desinstalarla, elimina únicamente los archivos de esta traducción de la carpeta de modificaciones.

### Opción 2: XDELTA para una ROM traducida

1. Comprueba que la ROM USA original tenga el tamaño y SHA-256 indicados arriba.
2. Aplica el `.xdelta` sobre esa ROM limpia con [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher) o con:

```sh
xdelta3 -d -s "Shin Megami Tensei IV - Apocalypse (USA).3ds" shinivapoc-es-v1.0.xdelta "Shin Megami Tensei IV - Apocalypse (ES).3ds"
```

3. La ROM resultante ocupa **2.147.483.648 bytes** y su SHA-256 debe ser `693c83482860653ba204a65d03fd454bef788676970c9d3afb408ed33e1b066f`.
4. Abre el resultado en Azahar con la carpeta de mods del juego vacía. La traducción ya está integrada: no añadas el ZIP ni un `code.ips` externo.

El XDELTA se ha reaplicado a la ROM original y se ha comparado byte a byte con la imagen reconstruida. Se ha probado su arranque, introducción y retorno al diálogo sin LayeredFS. Se mantienen los límites de revisión de partida y hardware indicados arriba.

## Créditos y aviso

Proyecto de **johanderohan / Parches en Castellano**. Juego y materiales originales de **ATLUS** y sus titulares. Traducción de aficionados, sin relación oficial con ellos.

Herramientas: utilidades propias de extracción y reinserción, [Azahar](https://github.com/azahar-emu/azahar), [FFmpeg](https://ffmpeg.org/) y [mobipeg](https://github.com/quatric/mobipeg) para los vídeos. Para la alternativa XDELTA: [3dstool](https://github.com/dnasdw/3dstool), [ctrtool](https://github.com/3DSGuy/Project_CTR) y xdelta3. Las letras castellanas y los subtítulos reutilizan la fuente del juego. El rótulo «FIN DE PARTIDA» procede de una propuesta gráfica asistida por generación de imágenes, adaptada al formato de consola.

El repositorio contiene solo este README; el parche está en Releases. No se publican ROMs, partidas, ejecutables completos ni el guion extraído. Si detectas un problema, abre una incidencia indicando región, versión del parche, emulador o consola y una captura de la pantalla afectada.
