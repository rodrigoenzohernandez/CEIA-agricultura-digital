# Red conceptual — Clase 2: Horticultura

Complemento del [resumen](resumen.md). Primero hay una vista general de toda la clase y después un mapa por tema, en el orden en que se dieron. Los números de sección (§) remiten al resumen.

**Cómo leerla**
- Cada flecha forma una frase: *Horticultura → tiene → postcosecha corta*. Una flecha sin texto quiere decir "incluye".
- Las flechas punteadas unen conceptos de temas distintos.
- Colores: azul = tema · verde = herramienta, tecnología o caso real · amarillo = dato para memorizar · gris punteado = concepto que se desarrolla en otro mapa.

> Todo el contenido sale de la clase. La organización y las frases de las flechas son propias.

## Vista general

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 30, "rankSpacing": 40, "padding": 10}}}%%
flowchart TD
    HOR["① Horticultura<br>cultivo intensivo ·<br>herbáceos de ciclo corto"]
    ARG["Horticultura argentina<br>600.000 ha · 10 M t ·<br>heterogénea"]
    ORG["Órganos de consumo<br>de frutos a yemas"]
    POS["② Postcosecha<br>la calidad solo empeora"]
    MAN["③ Tipos de manejo<br>convencional · orgánico ·<br>agroecológico"]
    TIP["Tipología<br>cinturones · especializada ·<br>extensivos · industria"]
    CIN["④ Cinturón hortícola familiar<br>manual · diversificado ·<br>sin tecnología a su escala"]
    TEC["⑤ Tecnología por tipo<br>de producción"]
    EJE["Ejercicio: propuestas<br>de los alumnos"]
    IOT["⑥ IoT en horticultura<br>Huerta IoT + SensorWave"]
    DES["7 desafíos del IoT"]
    APR["Diseñar para<br>la desconexión"]

    HOR -->|en Argentina| ARG
    HOR -->|consume distintos| ORG
    HOR -->|es perecedera:<br>es clave la| POS
    ARG -->|se produce con<br>distintos| MAN
    ARG -->|se clasifica en| TIP
    TIP -->|la ensalada diaria<br>viene del| CIN
    TIP -->|cada tipo tiene su| TEC
    CIN -->|demanda| TEC
    TEC -->|inspiró el| EJE
    TEC -->|un caso real| IOT
    IOT -->|enfrenta| DES
    IOT -->|lección principal| APR
    POS -.->|visión para detectar<br>fruta dañada| TEC
    MAN -.->|la transición agroecológica<br>tiene pocas herramientas| CIN

    classDef tema fill:#dbeafe,stroke:#1e40af,color:#0b1b3f
    classDef herr fill:#dcfce7,stroke:#166534,color:#052e16
    classDef dato fill:#fef9c3,stroke:#a16207,color:#3b2405
    class HOR,POS,MAN,CIN,TEC,IOT tema
    class EJE herr
    class APR dato
```

## 1. Qué es la horticultura y qué se produce en Argentina (§1 a §3)

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 30, "rankSpacing": 40, "padding": 10}}}%%
flowchart LR
    HOR["Horticultura<br>sistema de cultivos intensivo"]
    HOR -->|son cultivos| HER["Herbáceos<br>anuales o bianuales"]
    HER -->|de| CIC["Ciclos cortos<br>rúcula: ~45 días"]
    CIC -->|permiten la| ROT["Rotación rápida<br>rabanito, lechuga y tomate<br>en un mismo año"]
    HOR -->|tiene| DIS["Alta frecuencia de disturbios"]
    DIS -->|provoca| DEQ["Desequilibrio:<br>plagas y enfermedades"]
    DEQ -->|se compensa con el| MNJ["Manejo<br>qué sembrar después de qué"]
    HOR -->|tiene| PCO["Postcosecha corta<br>salvo papa, cebolla,<br>batata y zapallo"]
    HOR -->|exige| MOI["Mucha mano de obra e insumos<br>herbicidas · insecticidas ·<br>fungicidas"]
    HOR -->|se diferencia de la| FRU["Fruticultura<br>leñosos · hasta 20 años ·<br>todo en nivel medio"]
    HOR -->|en Argentina| ARG["600.000 ha · 10 M t por año<br>familiar y empresarial"]
    ARG -->|se produce en| CV["Cinturones verdes<br>La Plata · Córdoba · Rosario ·<br>la hoja no aguanta el viaje"]
    ARG -->|y en| ZON["Zonas específicas<br>Mendoza: ajo, cebolla, papa<br>Balcarce: papa<br>Corrientes: tomate, pimiento"]
    ARG -->|se compone de| COM["65 %: papa, tomate, cebolla,<br>batata, zapallo, zanahoria,<br>lechuga y ajo<br>20 %: acelga, mandioca, choclo…<br>15 %: el resto"]
    HOR -->|consume distintos| ORG["Órganos"]
    ORG --> O1["Frutos<br>tomate · berenjena ·<br>zapallo · melón"]
    ORG --> O2["Tallo subterráneo: papa<br>Bulbos: cebolla, ajo, puerro"]
    ORG --> O3["Hojas<br>lechuga · acelga ·<br>espinaca · repollo"]
    ORG --> O4["Raíces<br>batata · zanahoria"]
    ORG --> O5["Hipocótilo engrosado<br>remolacha · rabanito"]
    ORG --> O6["Flores: brócoli, coliflor, alcaucil<br>Yemas: repollitos de Bruselas"]
    ORG --> O7["Semillas: arveja, garbanzo,<br>lenteja · Argentina es<br>fuerte en garbanzo"]

    classDef tema fill:#dbeafe,stroke:#1e40af,color:#0b1b3f
    classDef dato fill:#fef9c3,stroke:#a16207,color:#3b2405
    class HOR,ARG,ORG tema
    class CIC,COM,O5 dato
```

## 2. Postcosecha (§4)

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 30, "rankSpacing": 40, "padding": 10}}}%%
flowchart LR
    POS["Postcosecha<br>la calidad no mejora:<br>solo puede empeorar"]
    POS -->|la degradan| PRO["Tres procesos"]
    PRO --> RES["Respiración<br>degrada las reservas"]
    PRO --> TRA["Transpiración<br>pierde agua y peso"]
    PRO --> SEN["Senescencia<br>los tejidos se ablandan"]
    POS -->|los aceleran| FAC["Factores"]
    FAC --> TEM["Temperatura elevada<br>el más crítico"]
    FAC --> HUM["Baja humedad<br>calor + seco =<br>secador de pelo"]
    FAC --> DAN["Daño mecánico<br>jugo celular →<br>hongos y bacterias"]
    FAC --> ETI["Etileno<br>hormona gaseosa<br>de la maduración"]
    TEM -->|ejemplo| BRO["Brócoli a 20 °C<br>respiración muy alta ·<br>se pone amarillo"]
    DAN -->|ejemplo| TOM["Un tomate golpeado<br>contagia a los vecinos<br>con hifas y etileno"]
    ETI -->|actúa sobre los| CLI["Frutos climatéricos<br>tomate · palta ·<br>banana · pera"]
    CLI -->|la reina del etileno| BAN["Banana<br>viene con sobres<br>inhibidores"]
    POS -->|se controla con| CTL["Heladera y cadena de frío ·<br>registradores de T y HR ·<br>atmósfera controlada<br>en productos de más valor"]
    POS -->|oportunidad| VIS["Visión por computadora<br>detecta fruta dañada<br>que el ojo no ve"]
    VIS -->|clave en la| EXP["Exportación<br>una fruta podrida<br>hace rechazar la carga"]
    ETI -.->|el sensor es caro:<br>se estima con| SNT["Sensor de temperatura"]

    classDef tema fill:#dbeafe,stroke:#1e40af,color:#0b1b3f
    classDef herr fill:#dcfce7,stroke:#166534,color:#052e16
    classDef dato fill:#fef9c3,stroke:#a16207,color:#3b2405
    class POS,PRO,FAC tema
    class VIS,SNT,CTL herr
    class TEM,BAN dato
```

## 3. Manejo y tipología de la producción (§5, §6 y §10)

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 30, "rankSpacing": 40, "padding": 10}}}%%
flowchart LR
    MAN["Tipos de manejo"]
    MAN --> CON["Convencional<br>síntesis química ·<br>maximiza la producción ·<br>domina el mercado"]
    MAN --> ORGN["Orgánico<br>sin síntesis química ·<br>auditado y certificado ·<br>puede ser solo sustitución"]
    MAN --> AGR["Agroecológico<br>enfoque sistémico ·<br>equilibrio del agroecosistema"]
    CON -->|destino| CDE["90 % mercado interno"]
    ORGN -->|destino| ODE["99 % exportación"]
    AGR -->|destino| ADE["100 % mercado interno<br>venta directa y cercana"]
    CON -->|demanda| CTE["Menos agroquímicos ·<br>monitoreo ambiental ·<br>eficiencia energética"]
    ORGN -->|demanda| OTE["Trazabilidad digital ·<br>sensores de residuo cero ·<br>monitoreo de biodiversidad"]
    AGR -->|demanda| ATE["Tecnologías apropiadas ·<br>energías limpias ·<br>manejo participativo de datos"]
    CON -.->|la transición dura años<br>y es lo más difícil| AGR

    TIP["Tipología de la<br>producción hortícola"]
    TIP --> CIN["Cinturones hortícolas familiares<br>diversificados · cerca del consumo ·<br>chicos e intensivos"]
    TIP --> ESP["Producción especializada<br>zonas con aptitud específica ·<br>alto valor"]
    ESP -->|caso| CEB["Cebolla en el sur de Buenos Aires<br>el fotoperíodo activa<br>la bulbificación"]
    ESP -->|otras zonas| ESR["Ajo y zanahoria: Mendoza ·<br>melón: San Juan ·<br>batata: Córdoba y Formosa"]
    TIP --> EXT["Cultivos mecanizados<br>20 a 300 ha de monocultivo"]
    EXT -->|ejemplos| EXR["Papa: Balcarce ·<br>batata: San Pedro ·<br>mandioca: Misiones y Formosa ·<br>legumbres: sur de Santa Fe"]
    TIP --> IND["Producción para la industria<br>altamente mecanizada"]
    IND -->|se firma un| CTR["Contrato<br>rendimiento en peso fresco ·<br>% de materia seca ·<br>venta asegurada, precio bajo"]
    CIN -.->|se detalla en| CINb["Cinturón familiar · mapa 4"]

    classDef tema fill:#dbeafe,stroke:#1e40af,color:#0b1b3f
    classDef dato fill:#fef9c3,stroke:#a16207,color:#3b2405
    classDef puente fill:#f3f4f6,stroke:#6b7280,color:#374151,stroke-dasharray:4 3
    class MAN,CON,ORGN,AGR,TIP,CIN,ESP,EXT,IND tema
    class CDE,ODE,ADE,CEB,CTR dato
    class CINb puente
```

## 4. El cinturón verde y los productores familiares (§7 a §9 y §12)

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 30, "rankSpacing": 40, "padding": 10}}}%%
flowchart LR
    CIN["Cinturón hortícola familiar<br>pone la ensalada<br>de todos los días"]
    CIN -->|tiene una vida| VID["Sacrificada y de baja<br>rentabilidad · el precio<br>castiga la mala calidad"]
    VID -->|anécdota| ACE["Laterales del invernáculo<br>bajarlos con frío y viento,<br>subirlos con calor ·<br>no van a cumpleaños"]
    ACE -->|se podría| AUT["Automatizar con sensores"]
    CIN -->|prácticas| PRA["Diversificación · rotación ·<br>laboreo permanente ·<br>invernáculos · semillas propias"]
    PRA --> RIE["Riego<br>bajo cubierta, siempre ·<br>regar de más enferma"]
    PRA --> HID["Hidroponía<br>sin sustrato · control de<br>temperatura, nutrientes y pH"]
    CIN -->|labores| LAB["Manuales: siembra, desmalezado,<br>cosecha y lavado ·<br>insumos: cama de pollo<br>y agroquímicos"]
    CIN -->|necesita un| CAN["Canal de comercialización<br>cercano y fluido, por la<br>alta perecibilidad"]
    CIN -->|caso real| HOL["Hola Sabor<br>Parque Pereyra Iraola ·<br>100 % agroecológicos desde 2009"]
    HOL -->|ganaron| BEN["Salud · autonomía de insumos ·<br>semillas propias ·<br>rotación y asociación"]
    HOL -->|trabajan con| HER["Azada y piletas de lavado<br>no hay tecnología<br>apropiada para su escala"]
    HER -->|alternativa| COMP["Asociarse y compartir<br>maquinaria"]
    CIN -->|sondeo de la docente:<br>requieren| REQ["Accesibilidad económica ·<br>energías limpias ·<br>eficiencia energética ·<br>bienestar humano"]
    CIN -->|sus desafíos críticos| DCR["Malezas · cosecha y lavado ·<br>sanidad: detección temprana ·<br>automatizar invernáculos y riego"]
    DCR -->|plagas| PLA["Pulgones · nematodos ·<br>orugas · babosas ·<br>hormigas · aves"]
    DCR -->|la visión detecta mejor| ENF["Enfermedades<br>manchas que cambian<br>de color"]
    TRAb["Transición agroecológica · mapa 3"] -.->|la etapa con<br>menos herramientas| HOL

    classDef tema fill:#dbeafe,stroke:#1e40af,color:#0b1b3f
    classDef herr fill:#dcfce7,stroke:#166534,color:#052e16
    classDef dato fill:#fef9c3,stroke:#a16207,color:#3b2405
    classDef puente fill:#f3f4f6,stroke:#6b7280,color:#374151,stroke-dasharray:4 3
    class CIN,PRA,DCR tema
    class HOL,HID herr
    class AUT,ENF dato
    class TRAb puente
```

## 5. Tecnología por tipo de producción y ejercicio (§11 y §13)

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 30, "rankSpacing": 40, "padding": 10}}}%%
flowchart LR
    TEC["Tecnología por tipo<br>de producción"]
    TEC --> T1["Cinturones familiares<br>riego · temperatura ·<br>humedad · plagas"]
    T1 -->|oportunidad| O1["Sensores low-cost ·<br>estaciones agrometeorológicas ·<br>apps · visión computarizada"]
    TEC --> T2["Especializada<br>riego y fertilización ·<br>predicción fenológica"]
    T2 -->|oportunidad| O2["Sensores de humedad<br>y conductividad · modelos<br>predictivos · fertirriego"]
    TEC --> T3["Extensivos hortícolas<br>logística · trazabilidad ·<br>rendimiento"]
    T3 -->|oportunidad| O3["Sensores remotos ·<br>imágenes satelitales · IA"]
    TEC --> T4["Agroindustria<br>calidad · sincronizar<br>cosecha y procesado"]
    T4 -->|oportunidad| O4["IoT en planta · NIR ·<br>blockchain"]
    TEC -->|desafío transversal| CPT["Compostaje<br>mal hecho trae<br>patógenos y metano"]
    TEC -->|se practicó en el| EJE["Ejercicio<br>innovación · factibilidad ·<br>usabilidad · inversión"]
    EJE --> P1["Gonzalo: app de balcón<br>foto + riego + sensores ·<br>venta en viveros"]
    EJE --> P2["Tomás: marketplace<br>escalonar cosechas<br>y estabilizar precios"]
    EJE --> P3["Rodrigo: cámaras y trampas<br>solo para insectos que se mueven ·<br>no sirve para la cochinilla"]
    EJE --> P4["Facundo: conteo de racimos<br>y botritis al madurar"]
    P3 -->|clasificar frutos sirve en el| ALM["Almacenamiento<br>en la planta ya es tarde"]
    O1 -.->|un caso real| IOTb["Huerta IoT · mapas 6 y 7"]

    classDef tema fill:#dbeafe,stroke:#1e40af,color:#0b1b3f
    classDef herr fill:#dcfce7,stroke:#166534,color:#052e16
    classDef dato fill:#fef9c3,stroke:#a16207,color:#3b2405
    classDef puente fill:#f3f4f6,stroke:#6b7280,color:#374151,stroke-dasharray:4 3
    class TEC,EJE tema
    class O1,O2,O3,O4 herr
    class ALM dato
    class IOTb puente
```

## 6. IoT en el campo: desafíos y Huerta IoT v1 (§14 a–d)

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 30, "rankSpacing": 40, "padding": 10}}}%%
flowchart LR
    IOT["IoT en horticultura<br>Claudio Biale · UNaM y FIUBA"]
    IOT -->|se aplicó en| COL["Colonia Liebig, Corrientes<br>2.ª provincia bajo cubierta ·<br>+2.100 ha · tomate y pimiento ·<br>primicias"]
    IOT -->|es parte de la| AIN["Agricultura inteligente 4.0<br>IoT + nube · decide por<br>contexto y eventos"]
    AIN -->|mercado de invernaderos<br>inteligentes| MER["USD 1.380 M en 2020 →<br>USD 2.820 M en 2028"]
    IOT -->|enfrenta| DES["7 desafíos"]
    DES --> D1["Conectividad<br>caídas del proveedor"]
    DES --> D2["Energía<br>transmitir es lo que<br>más consume"]
    DES --> D3["Interoperabilidad<br>formatos, nubes y protocolos"]
    DES --> D4["Seguridad<br>una bomba de riego hackeada"]
    DES --> D5["Calidad de datos<br>deriva de los sensores"]
    DES --> D6["Costos<br>instalación, conectividad,<br>mantenimiento, capacitación"]
    DES --> D7["Mantenimiento<br>la flota de nodos"]
    DES -->|en el campo| ARQ["La desconexión es la norma<br>borde: lo urgente y local ·<br>nube: lo histórico y global"]
    IOT -->|primera versión| V1["Huerta IoT v1<br>ESP32 → EMQX → Fastify →<br>CouchDB → Svelte ·<br>DigitalOcean + Docker Swarm"]
    V1 -->|evaluaba| REG["Reglas en la nube<br>suelo con menos de 40 % de<br>humedad y T ≥ 20 → bomba"]
    V1 -->|le faltaba| FAL["Multiprotocolo · funcionar<br>sin internet · reglas sobre<br>varios sensores · objetos"]
    FAL -->|de ahí nace| SWb["SensorWave · mapa 7"]
    D1 -.->|sin borde, se<br>perdían las reglas| FAL

    classDef tema fill:#dbeafe,stroke:#1e40af,color:#0b1b3f
    classDef herr fill:#dcfce7,stroke:#166534,color:#052e16
    classDef dato fill:#fef9c3,stroke:#a16207,color:#3b2405
    classDef puente fill:#f3f4f6,stroke:#6b7280,color:#374151,stroke-dasharray:4 3
    class IOT,DES,AIN tema
    class V1 herr
    class COL,MER dato
    class SWb puente
```

## 7. SensorWave y Huerta IoT v2 (§14 e–m)

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 30, "rankSpacing": 40, "padding": 10}}}%%
flowchart LR
    SW["SensorWave<br>series temporales<br>distribuidas · en Go"]
    SW --> BOR["Nodo de borde<br>MQTT, CoAP y HTTP ·<br>compresión · reglas"]
    SW --> OBJ["Almacenamiento S3<br>bloques comprimidos ·<br>catálogo de series"]
    SW --> DSP["Despachador sin estado<br>une lo reciente del borde<br>con lo histórico de S3"]
    BOR -->|al vencer el tiempo<br>de almacenamiento| OBJ
    BOR -->|guarda en| PEB["Pebble<br>puntos sin comprimir →<br>bloques comprimidos"]
    PEB -->|comprime por tipo| CMP["Gorilla · delta de delta ·<br>RLE · diccionario<br>+ LZ4"]
    BOR -->|sin internet| SIG["Sigue midiendo y actuando ·<br>reintenta subir"]
    DSP -->|como no tiene estado| ESC["Escala con varias réplicas"]
    SW -->|es la base de| V2["Huerta IoT v2"]
    V2 --> EDG["huerta-iot-edge<br>Go + broker MQTT local"]
    V2 --> BRK["NanoMQ en Fly.io<br>federación"]
    V2 --> BCK["Backend en Go + despachador<br>API REST con JWT · bcrypt"]
    V2 --> FRO["Frontend SvelteKit<br>Cloudflare Workers ·<br>Leaflet y ECharts"]
    V2 --> RDS["Cloudflare R2<br>usuarios · nodos · bloques"]
    V2 -->|el tópico define la| SER["Serie<br>nodo/zona/dispositivo/tipo/métrica ·<br>mensaje mínimo con el valor"]
    FRO -->|se navega| NAV["Mapa → nodo → zonas →<br>dispositivo → mediciones"]
    V2 -->|le falta| PEN["Cortes largos · sleep del ESP32 ·<br>acceso en borde y broker ·<br>SenML o NGSI-LD · calidad ·<br>firmware remoto"]
    V2 -->|aprendizajes| APR["Diseñar para la desconexión ·<br>nombre jerárquico único ·<br>separar reciente de histórico ·<br>seguridad desde el inicio"]

    classDef tema fill:#dbeafe,stroke:#1e40af,color:#0b1b3f
    classDef herr fill:#dcfce7,stroke:#166534,color:#052e16
    classDef dato fill:#fef9c3,stroke:#a16207,color:#3b2405
    class SW,V2 tema
    class BOR,OBJ,DSP,EDG,BRK,BCK,FRO,RDS,PEB herr
    class SER,APR dato
```
