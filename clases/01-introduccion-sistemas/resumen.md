# Clase 1 — Introducción a los sistemas agropecuarios

- **Docente:** Lic. Biol. Guadalupe Tiscornia (Mag. Dra.) — área Sistemas de Información y Transformación Digital, INIA Uruguay
- **Fecha:** 20/10/2026 (la grabación figura como 21/10)
- **Grabación:** [Google Drive](https://drive.google.com/file/d/18BGqsrmyBp-I0znhr0XbOmUqmCRLFYeS/view)
- **Material:** [slides](material/slides-introduccion-sistemas.pdf) · [presentación del curso](material/presentacion-curso.pdf) · [notas Gemini](material/notas-gemini.docx) · [transcripción](material/transcripcion.txt)

## Ideas clave

1. Un **sistema agropecuario** es un conjunto organizado de elementos interrelacionados (recursos naturales, biológicos, humanos, tecnológicos, infraestructura, mercados) que produce bienes agropecuarios. Se analiza como **entradas → procesos → salidas**.
2. El objetivo del productor **no siempre es maximizar rendimiento**: también calidad de vida, seguridad, reducir riesgo, "caja de ahorro". Una solución tecnológica tiene que encajar en esos objetivos.
3. Cada sistema productivo (extensivo, intensivo, ganadero, lechero, mixto) tiene escalas, riesgos, mano de obra y necesidades distintas → **las soluciones digitales no son universales**.
4. **Baja adopción digital** en el agro: miedo al riesgo tecnológico, usabilidad, costos, conectividad, perfiles educativos muy diversos.
5. Cambio climático, exigencias ambientales de los mercados y **despoblamiento rural** empujan la digitalización.
6. Digitalizar ≠ tener apps: es **integrar datos, procesos y decisiones** en un ecosistema conectado.
7. Mensaje final: **"El agro no necesita más apps, necesita más valor"**. Innovar desde necesidades reales, no desde la tecnología buscando un problema.

---

## 1. Presentación del curso (00:00–00:33)

- 8 módulos; cada clase arranca con un **multiple choice (5–7 preguntas)** + encuesta de terminología. Ver [README](../../README.md#evaluación).
- **TP final** con Martín Horn: arrancar a más tardar en la clase 3–4 para aprovechar el feedback iterativo (00:16:56). Detalle en [tp-final](../../tp-final/README.md).
- Presentación de alumnos (00:22:34): intereses variados — IA en drones, cosechadoras autónomas de frutales, ERP para fabricantes de maquinaria, estimación de materia seca en Córdoba, modelo predictivo para feedlots en Tucumán.

## 2. Sistemas agropecuarios (00:33:46)

**Componentes básicos:** recursos naturales (suelo, clima, agua) · componentes biológicos (cultivos, pasturas, animales) · capital humano (cantidad y calidad) · capital tecnológico · infraestructura · mercados.

**Enfoque de sistemas:** importan las relaciones entre las partes.
- *Entradas:* energía, semilla, animales, maquinaria.
- *Procesos:* preparación de tierra, siembra, cosecha.
- *Salidas:* productos y residuos.

Las poblaciones de plantas, animales y microorganismos interactúan entre sí y con el ambiente → **el manejo sanitario y nutricional es clave**.

**Objetivo de la empresa agropecuaria (00:39:36):** la unidad productiva es un medio para los fines del productor. Producción física por hectárea es *un* objetivo, no el único: calidad de vida, seguridad alimentaria, ingreso, "caja de ahorro" (ej. ganado como reserva de valor), aceptación social, garantizar un volumen mínimo anual limitando riesgo de catástrofe.

## 3. Tipología de sistemas productivos (00:42:12)

```
Sistema agropecuario
├── Cultivos ──── Extensivos (anuales, arroz, forestal)
│             └── Intensivos (horticultura, fruticultura)
├── Mixtos
└── Ganaderos ─── Ganadería extensiva
              ├── Ganadería intensiva
              └── Lechería
```

| Sistema | Rasgos | Puntos críticos |
|---|---|---|
| **Extensivo anual** (trigo, maíz, sorgo, cebada, avena; soja, girasol, colza) | Grandes superficies, cielo abierto, alto riesgo climático, poca mano de obra/ha, muy mecanizado. Mayormente secano; si hay riego, por pivot | Humedad en cosecha |
| **Arroz** | Extensivo con inundación en etapas de crecimiento | Riego fundamental, humedad en almacenamiento |
| **Forestal** | Ciclos largos (~10 años), madera o celulosa, manejado por empresas con genética propia | Planificación de largo plazo |
| **Horticultura** | Ciclos cortos, gran diversidad; cielo abierto, invernáculos, túneles, hidroponía | Mano de obra intensiva, postcosecha |
| **Fruticultura** | Consumo fresco o industria; ciclos largos (años hasta producir) | **Polinización** |
| **Ganadería extensiva** | Pastizales naturales, baja carga, pocos insumos y mano de obra | Manejo de potreros |
| **Ganadería intensiva** (feedlot, aves, cerdos, conejos; cabras semi-intensivo) | Alta densidad, ciclos cortos, muchos insumos, ambiente controlado | Sanidad (contagio), residuos, impacto ambiental |
| **Lechería** | Razas lecheras (Holando), pastoreo de pasturas cultivadas; desde familiares a miles de vacas | Manejo reproductivo, calidad de leche, **efluentes**; ordeñe diario sin feriados |
| **Apicultura** | Miel, polen, cera, propóleo; cualquier escala | Sanidad de colmenas; aporta polinización |
| **Mixtos** | Rotación agrícola–pasturas, arroz–ganadería, silvopastoriles, fruticultura + ovejas (con bozal para no dañar brotes) | Integración de subsistemas |

**Escala de predios (cultivos extensivos, 01:11:58):** pequeño < 50 ha · mediano 50–500 ha · grande > 500 ha. Varía mucho según sistema (horticultura/lechería usan predios mucho menores) y según fertilidad del suelo.

## 4. Personas involucradas (01:13:39)

- **Productores:** nivel educativo muy variado (primaria incompleta a doctorado). Adoptan si les sirve, pero hay baja adopción digital (riesgo tecnológico, necesidades básicas primero). La **familia** pesa en las decisiones.
- **Técnicos asesores** (agrónomos, veterinarios): entienden la tecnología hasta cierto punto; pueden ser **aliados o barreras** para la adopción.
- **Trabajadores rurales:** nivel educativo generalmente bajo → soluciones simples y fáciles de capacitar.

## 5. Factores clave: cambio climático y ambiente (01:20:33)

- **Cambio climático** (CMNUCC art. 1): cambio atribuible a la actividad humana que se suma a la variabilidad natural. Se estudia en dos etapas: *detección* y *atribución*.
- No solo cambian las medias: aumenta **frecuencia e intensidad de extremos** (sequías, olas de calor, lluvias intensas), cambian regímenes de lluvia, sube la temperatura, afecta disponibilidad/calidad de agua, más plagas y enfermedades → clave **adaptación y mitigación**.
- La **variabilidad climática** es el principal factor a contemplar en producción a cielo abierto.
- **Cuidado del ambiente:** reducir GEI, pérdida de biodiversidad, erosión; uso eficiente de recursos e insumos; conservar servicios ecosistémicos. Ej.: pulverización selectiva que detecta malezas → menos herbicida y menos costo (01:25:19).
- **Mercados** exigen cumplimientos ambientales; incumplir puede cerrar el acceso (01:28:08).
- **Menos gente en el campo:** la población rural cae → hacer el trabajo rural más amigable.

## 6. AgroTIC: qué promueve su uso (01:46:15)

a) Mejor conectividad y móviles (ej. Starlink) · b) abaratamiento de sensores y equipos (estaciones meteorológicas de ~USD 200) · c) madurez de software de gestión · d) recambio generacional · e) escasez de mano de obra · f) demanda de mejores condiciones laborales · g) reducir trabajo rutinario.

**¿Qué es digitalizar?** Sensores, drones, satélites, IoT; plataformas de gestión y big data; IA para predicciones; blockchain y trazabilidad — **integrados** en un ecosistema que transforma la forma de producir.

## 7. AgroTIC a nivel predio — ejemplos (01:48:52)

| Aplicación | Ejemplos de la clase |
|---|---|
| **IoT** | Equipos, iluminación, bombas, refrigeración |
| **Monitoreo** | Red de estaciones automáticas de INIA → mapas de anomalías de lluvia y balance hídrico; **NDVI** satelital para vigor vegetal |
| **Alertas** (01:57:30) | *Alerta Ovina* (índice de frío "chill index" para corderos en sus primeras 72 h: frío + viento + lluvia); **estrés térmico** en bovinos de leche y carne (5–7 días de anticipación; medidas: no mover ganado, agua, aspersión); **INIA Termoestrés**, **INIA Termomín** (heladas < 0–2 °C). Cada alerta debe ir asociada a una **medida de manejo concreta** |
| **Apoyo a la gestión** | Fertilización (P, N, arroz), riego según fase del cultivo, alertas de enfermedades. **INIA Móvil**: "super app" que centraliza todo, el productor carga su ubicación una vez (02:06:05). **Auravant**: índices de vegetación por chacra → fertilización diferenciada (02:08:58) |
| **Análisis de datos** | Modelos predictivos, IA, **gemelos digitales** para simular sin esperar tiempos biológicos — requieren datos robustos (02:11:59) |
| **Automatización** | Riego automático de pasturas con energía solar (empresa uruguaya + ANII + Fagro + INIA); **alambrados virtuales** con collares Halter (estímulos, protege zonas sensibles) (02:19:10) |
| **Robotización** | **Ordeñe voluntario robotizado** en sistemas pastoriles (INIA Las Brujas y La Estanzuela): la vaca va sola, el collar la identifica; alto costo (02:14:59) |
| **Decisión inteligente** | Integrar monitoreo animal, ambiental, riego, cultivos/pasturas, vigilancia, maquinaria (telemetría) y pronósticos → **gestión remota y decisiones** |

**Requisitos de un sistema inteligente (02:22:02):** integrar fuentes y escalas, devolver resultados **simples**, datos **robustos** (un chatbot con malos datos recomienda mal), **interoperabilidad** (evitar islas de información), **capacitación** acorde al usuario.

Difusión: [GRAS – INIA](http://www.inia.uy/gras), [Converge – INIA](https://inia.uy/converge) (programa de 3 años que evalúa soluciones digitales de forma imparcial: verifica funcionamiento y valida usabilidad con productores, para bajar el riesgo tecnológico) (02:27:49).

## 8. Oportunidades (02:30:46)

Digitalizar solo tiene sentido si ayuda a **producir más con menos, adaptarse al cambio climático, abrir mercados, ser sostenibles e incluir a pequeños y grandes productores**.

- **Eficiencia de recursos:** riego de precisión, fertilización diferenciada, control selectivo de plagas.
- **Productividad y decisiones:** datos, modelos de simulación/pronóstico, gestión y transferencia de riesgo (seguros).
- **Resiliencia y sostenibilidad:** menor huella por eficiencia de insumos; monitoreo de suelo y vegetación.
- **Democratización de la información:** recomendaciones personalizadas vía chatbots.
- **Mercados y trazabilidad:** comercio digital, mercados diferenciados.
- **Logística, cumplimiento regulatorio y certificación.**
- En **investigación** se usan tecnologías más intensivas (sensores de nutrientes, radar, térmico, monitoreo de agua en suelo) que luego migran a productores avanzados (02:33:53).

## 9. Desafíos (02:35:41)

Conectividad e infraestructura · capacitación y usabilidad · costos · aversión al cambio y riesgo tecnológico · **aumento de brechas** entre chicos y grandes · transformación (no reemplazo) de la mano de obra · poca integración en la cadena · **propiedad y uso comercial de los datos** · datos no interoperables · falta de herramientas para promover adopción.

## 10. Cierre (02:41:15)

> La digitalización no es un fin en sí mismo; es un medio para generar valor real económico, ambiental y social. La innovación en el agro debe partir de **necesidades, no de modas**.

---

## Relevancia para IA / ideas de TP

- **Visión por computadora:** detección de malezas para aplicación selectiva; conteo/estado de frutos; drones.
- **Teledetección:** NDVI y otros índices satelitales → mapas de vigor, zonas de manejo, estimación de biomasa / materia seca.
- **Series temporales y pronóstico:** alertas agroclimáticas (heladas, estrés térmico, chill index), balance hídrico, demanda de riego.
- **LLMs / chatbots** de recomendación para productores sin asesor — el problema central es la **calidad de los datos** y la usabilidad para usuarios con baja alfabetización digital.
- **Integración / interoperabilidad** de fuentes heterogéneas (sensores, satélite, telemetría de maquinaria) como problema de ingeniería de datos.
- Criterio de evaluación implícito de la docente: ¿resuelve una necesidad real?, ¿asocia la predicción a una **acción de manejo**?, ¿es usable por el perfil del productor?

## Glosario

- **Secano:** cultivo que solo usa agua de lluvia.
- **Riego por pivot (pivote central):** sistema de riego circular sobre ruedas.
- **Carga ganadera:** cantidad de animales por unidad de superficie.
- **Potrero:** subdivisión del campo para manejar el pastoreo.
- **Feedlot:** engorde a corral, ganadería intensiva.
- **Efluentes:** residuos líquidos (ej. del tambo/ordeñe) que deben tratarse para no contaminar cursos de agua.
- **Silvopastoril:** integración de árboles, pasturas y ganado.
- **Majada:** rebaño de ovejas.
- **NDVI:** índice de vegetación de diferencia normalizada, mide vigor vegetal a partir de bandas roja e infrarroja cercana.
- **Gemelo digital:** modelo que simula un sistema real para probar escenarios.
- **Alambrado virtual:** confinamiento del ganado con collares GPS y estímulos, sin cerco físico.
- **INIA:** Instituto Nacional de Investigación Agropecuaria (Uruguay).

## Posibles preguntas de multiple choice

1. ¿Cuáles son los componentes básicos de un sistema agropecuario? → recursos naturales, biológicos, capital humano, capital tecnológico, infraestructura, mercados.
2. ¿Cuál NO es característica de los cultivos extensivos? → alta mano de obra por hectárea (es de los intensivos).
3. ¿Qué factor es clave en fruticultura? → polinización.
4. ¿Qué rango define un predio mediano en cultivos extensivos? → 50–500 ha.
5. ¿Qué significa digitalizar según la clase? → integrar datos, procesos y decisiones en un ecosistema conectado (no solo tener apps).
6. ¿Cuál es un desafío de la digitalización? → propiedad de los datos / interoperabilidad / brechas entre productores.
7. ¿El objetivo del productor es siempre maximizar la producción por hectárea? → No.
