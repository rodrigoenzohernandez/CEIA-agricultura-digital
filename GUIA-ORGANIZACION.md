# Guía de organización del repo

Cómo está armado este repo de estudio y cómo replicarlo para otra materia. El ejemplo concreto es la [clase 1](clases/01-introduccion-sistemas/resumen.md).

## Idea general

- **Un repo por materia**, todo en español.
- **Una carpeta por clase** con el material original y un resumen propio.
- El resumen está pensado para el **multiple choice del inicio de la clase siguiente**: tiene que cubrir todos los temas, no solo los principales.
- El `README.md` es la portada: datos de la materia, cronograma con links y evaluación.
- El `CLAUDE.md` guarda las convenciones, así cualquier sesión con Claude (o cualquier persona) arma los resúmenes igual.

## Estructura

```
README.md                     portada: datos de la materia, cronograma, evaluación
CLAUDE.md                     convenciones del repo (las lee Claude Code)
GUIA-ORGANIZACION.md          esta guía
.gitignore                    .DS_Store y archivos temporales de Office (~$*)
clases/
  01-introduccion-sistemas/
    resumen.md                resumen de la clase
    red-conceptual.md         (opcional) mapas conceptuales en Mermaid
    material/                 material original, renombrado
      slides-introduccion-sistemas.pdf
      presentacion-curso.pdf
      notas-gemini.docx
      transcripcion.txt
    img/                      slides que usa el resumen
      slide-05-entradas-procesos-salidas.jpg
      ...
tp-final/
  README.md                   consigna, recomendaciones e ideas que van surgiendo
```

### Nombres

| Qué | Formato | Ejemplo |
|---|---|---|
| Carpeta de clase | `NN-tema-corto` (número con dos dígitos) | `01-introduccion-sistemas` |
| Slides | `slides-<tema>.pdf` | `slides-introduccion-sistemas.pdf` |
| Notas automáticas de Meet | `notas-gemini.docx` | |
| Transcripción | `transcripcion.txt` | |
| Imágenes | `slide-NN-tema.jpg` (NN = número de slide) | `slide-56-ndvi.jpg` |

Todo en kebab-case, sin tildes ni espacios: así los links de Markdown no se rompen.

## Flujo por clase

1. **Crear la carpeta** `clases/NN-tema/` con `material/` e `img/`.
2. **Bajar el material** (slides, notas de Gemini) a `material/` y renombrarlo.
3. **Extraer la transcripción** en texto plano desde las notas de Gemini (la parte que arranca en "Transcripción"):

   ```bash
   pandoc material/notas-gemini.docx -t plain | sed -n '/^Transcripción/,$p' > material/transcripcion.txt
   ```

4. **Exportar las slides como imágenes** para leerlas y para insertarlas en el resumen:

   ```bash
   pdftoppm -jpeg -scale-to-x 1280 -scale-to-y -1 material/slides-tema.pdf img/slide
   ```

   Después se renombran las que se usan (`slide-56-ndvi.jpg`) y se borran las demás. Si una slide apila varias fotos o capturas (animaciones), el render las superpone: en ese caso se extraen con `pdfimages -j` y se rearman una al lado de la otra.
5. **Escribir el resumen** (ver abajo).
6. **(Opcional) Red conceptual** con mapas en Mermaid.
7. **Actualizar el `README.md`**: completar la fila del cronograma con el link al resumen y a la grabación.
8. **Sumar ideas al `tp-final/README.md`**, indicando de qué clase salen.
9. **Commit** por clase (o por paso grande: resumen, imágenes, red conceptual).

## Fuentes: qué leer

- **La transcripción completa.** Las notas de Gemini resumen demasiado y se pierden ejemplos, cifras y herramientas que después aparecen en el multiple choice.
- **Las slides como imágenes**, no con `pdftotext`: el texto extraído pierde gráficos, mapas, diagramas y los datos de las capturas (umbrales, leyendas, escalas).

## Estructura del `resumen.md`

1. **Datos de la clase:** docente, fecha, duración, link a la grabación y al material.
2. **Repaso rápido para el examen:** bullets con definiciones, clasificaciones y cifras clave. Es lo que se lee 10 minutos antes de la clase.
3. **Desarrollo por tema**, en el orden de la clase:
   - Cada tema con su timestamp de la grabación: `## 9. Factores clave (01:19:08)`.
   - Todo lo que se dijo, no solo lo de las slides: ejemplos, anécdotas, cifras, nombres de herramientas.
   - Las slides con información visual insertadas con su pie:

     ```markdown
     ![Mapa de NDVI](img/slide-56-ndvi.jpg)

     *Slide 56: NDVI y anomalías del índice verde.*
     ```

   - Los datos que aparecen en las capturas (umbrales, leyendas) también pasados a texto.
4. **Correcciones de la transcripción automática:** tabla "Dice la transcripción | Es" para nombres propios y siglas mal reconocidos (ej. "Iña" → INIA, "NDBI" → NDVI).
5. **✎ Relevancia para IA / ideas de TP.**
6. **✎ Glosario.**
7. **✎ Preguntas de práctica**, con las respuestas ocultas:

   ```markdown
   <details>
   <summary>Respuestas</summary>

   1. ...
   </details>
   ```

**Regla del ✎:** todo lo que es elaboración propia (no se dijo en clase) se marca con ✎. Así queda claro qué es "lo que dijo el docente" y qué es agregado.

## Red conceptual (opcional)

`red-conceptual.md` complementa el resumen con mapas en Mermaid (GitHub los renderiza):

- Una **vista general** de toda la clase y después un mapa por bloque de temas, con referencia a las secciones del resumen (§).
- Las flechas forman frases: *Sistema agropecuario → tiene → 6 componentes*.
- Colores fijos: azul = tema, verde = herramienta, amarillo = dato para memorizar, gris punteado = concepto desarrollado en otro mapa.

## Para usarlo en otra materia

1. Crear el repo nuevo con `README.md`, `CLAUDE.md`, `.gitignore`, `clases/` y `tp-final/` (o la evaluación que tenga la materia).
2. Copiar el `CLAUDE.md` de este repo y cambiar el nombre de la materia y lo que no aplique. Por ejemplo, si no hay notas de Gemini, la transcripción puede salir de otra fuente, o si no hay multiple choice, el "repaso rápido" puede apuntar al parcial.
3. En el `README.md`, armar el cronograma completo desde el primer día con las columnas vacías de resumen y grabación, y completarlas clase a clase.
4. Seguir el flujo por clase de arriba.

### `CLAUDE.md` base

```markdown
# CLAUDE.md

Repo de estudio de la materia <Materia> (<carrera>). Todo en español.

## Convenciones

- Una carpeta por clase: `clases/NN-tema-corto/` con `resumen.md`, `material/` e `img/` (imágenes de las slides que usa el resumen, `slide-NN-tema.jpg`).
- Material original renombrado en kebab-case: `slides-<tema>.pdf`, `notas-gemini.docx`, `transcripcion.txt`.
- Al agregar una clase: completar la fila del cronograma en `README.md` y sumar ideas para el TP en `tp-final/README.md`.

## Resúmenes

- Fuentes: leer la transcripción completa y las slides como imágenes.
- Estructura de `resumen.md`: datos de la clase → repaso rápido para el examen → desarrollo por tema en el orden de la clase → tabla de correcciones de la transcripción → ✎ relevancia / ideas de TP → ✎ glosario → ✎ preguntas de práctica con respuestas en `<details>`.
- Imágenes: insertar las slides con información visual con un pie `*Slide N: ...*`. Exportarlas con `pdftoppm -jpeg -scale-to-x 1280`.
- Timestamps `(hh:mm:ss)` de la transcripción al inicio de cada tema.
- Marcar con ✎ todo lo que sea elaboración propia y no se dijo en clase.
```

Con eso alcanza con pedirle a Claude "armá el resumen de la clase N" para que siga el mismo formato.

## Herramientas

- `pandoc`: pasar las notas de Gemini (`.docx`) a texto plano.
- `poppler` (`pdftoppm`, `pdfimages`): exportar slides e imágenes de los PDF. En macOS: `brew install pandoc poppler`.
- Git + GitHub: un commit por paso, el README como índice navegable.
