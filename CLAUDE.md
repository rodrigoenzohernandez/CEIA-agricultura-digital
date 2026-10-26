# CLAUDE.md

Repo de estudio de la materia Agricultura Digital (CEIA, FIUBA). Todo en español.

## Convenciones

- Una carpeta por clase: `clases/NN-tema-corto/` con `resumen.md` y `material/`.
- Material original renombrado en kebab-case: `slides-<tema>.pdf`, `notas-gemini.docx`, `transcripcion.txt` (texto plano extraído de las notas de Gemini con `pandoc -t plain`, desde la línea "Transcripción").
- Al agregar una clase: completar la fila del cronograma en `README.md` (link al resumen y a la grabación) y sumar ideas para el TP en `tp-final/README.md`.

## Resúmenes

Cada clase tiene un multiple choice al inicio de la siguiente: el resumen tiene que cubrir **todos** los temas de la clase.

- Fuentes: leer la **transcripción completa** (no alcanza con las notas de Gemini, que omiten detalles) y las slides **como imágenes** (pdftotext pierde gráficos, mapas y diagramas).
- Estructura de `resumen.md`: datos de la clase → repaso rápido para el examen → desarrollo por tema en el orden de la clase (slides + todo lo dicho: ejemplos, cifras, herramientas) → tabla de correcciones de la transcripción automática → ✎ relevancia para IA / ideas de TP → ✎ glosario → ✎ preguntas de práctica con respuestas en `<details>`.
- Timestamps `(hh:mm:ss)` de la transcripción al inicio de cada tema.
- Marcar con ✎ todo lo que sea elaboración propia y no se dijo en clase.
