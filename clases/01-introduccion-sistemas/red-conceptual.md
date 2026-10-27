# Red conceptual — Clase 1: Introducción a los sistemas agropecuarios

Complemento del [resumen](resumen.md). Primero hay una vista general de toda la clase y después un mapa por tema, en el orden en que se dieron. Los números de sección (§) remiten al resumen.

**Cómo leerla**
- Cada flecha forma una frase: *Sistema agropecuario → tiene → 6 componentes*. Una flecha sin texto quiere decir "incluye".
- Las flechas punteadas unen conceptos de temas distintos.
- Colores: azul = tema · verde = herramienta, app o programa · amarillo = dato para memorizar · gris punteado = concepto que se desarrolla en otro mapa.

> Todo el contenido sale de la clase. La organización y las frases de las flechas son propias.

## Vista general

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 30, "rankSpacing": 40, "padding": 10}}}%%
flowchart TD
    SA["① Sistema agropecuario"]
    COMP["6 componentes"]
    TIP["Tipos<br>cultivos · mixtos · ganaderos"]
    OBJ["Objetivo del productor<br>no siempre es maximizar"]
    PER["Personas<br>productores · técnicos ·<br>trabajadores"]
    FCL["② Factores clave<br>cambio climático · ambiente ·<br>menos gente en el campo"]
    FAC["③ Factores que<br>promueven las AgroTIC"]
    DIG["Digitalizar<br>integrar datos, procesos<br>y decisiones"]
    AP["AgroTIC a nivel predio<br>monitoreo · alertas · gestión ·<br>automatización · decisión"]
    CNV["Converge<br>verificación y validación"]
    VAL["④ Agregar valor<br>más con menos · clima ·<br>mercados · sostenibilidad ·<br>inclusión"]
    OPP["Oportunidades"]
    DES["Desafíos"]
    CIE["El agro no necesita más apps,<br>necesita más valor"]

    SA -->|tiene| COMP
    SA -->|se clasifica en| TIP
    SA -->|es un medio para el| OBJ
    SA -->|involucra a| PER
    SA --->|enfrenta| FCL
    OBJ ~~~ FCL
    PER ~~~ FCL
    FCL -->|impulsan| FAC
    FAC -->|promueven| DIG
    DIG -->|se concreta en| AP
    AP -->|se verifican y<br>validan en| CNV
    DIG -->|solo si logra| VAL
    DIG -->|abre| OPP
    DIG -->|enfrenta| DES
    VAL -->|mensaje final| CIE

    OBJ -.->|la decisión<br>final es suya| AP
    PER -.->|temen el riesgo<br>tecnológico: lo baja| CNV

    classDef tema fill:#dbeafe,stroke:#1e40af,color:#0b1b3f
    classDef herr fill:#dcfce7,stroke:#166534,color:#052e16
    classDef dato fill:#fef9c3,stroke:#a16207,color:#3b2405
    class SA,FCL,FAC,DIG,AP,VAL tema
    class CNV herr
    class CIE dato
```

## 1. ¿Qué es un sistema agropecuario? (§1, §2 y §7)

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 30, "rankSpacing": 40, "padding": 10}}}%%
flowchart LR
    SA["Sistema agropecuario<br>elementos interrelacionados<br>que producen bienes<br>agropecuarios"]
    SA -->|tiene| COMP["6 componentes"]
    COMP --> RN["Recursos naturales<br>suelo · clima · agua"]
    COMP --> BIO["Componentes biológicos<br>cultivos · pasturas · animales"]
    COMP --> CH["Capital humano<br>en cantidad y calidad"]
    COMP --> CT["Capital tecnológico"]
    COMP --> INF["Infraestructura"]
    COMP --> MER["Mercados<br>terminan regulando el sistema"]
    SA -->|funciona con| EPS["Entradas → procesos → salidas<br>las salidas incluyen residuos"]
    SA -->|reúne| SUB["Subsistemas<br>plantas · animales · microorganismos<br>interactúan entre sí y con el ambiente"]
    SUB -->|por eso es clave el| MSN["Manejo sanitario<br>y nutricional"]
    SA -->|es un medio para el| OBJ["Objetivo del productor"]
    OBJ -->|no siempre es| MAX["Maximizar la producción"]
    OBJ -->|también pesan| OTR["Calidad de vida ·<br>seguridad alimentaria ·<br>caja de ahorro · aceptación social ·<br>volumen mínimo con poco riesgo"]
    SA -->|sus predios varían en| TAM["Tamaño del predio<br>según el sistema y<br>la fertilidad del suelo"]
    TAM -->|en extensivos| ESC["Pequeño: menos de 50 ha<br>Mediano: 50–500 ha<br>Grande: más de 500 ha"]
    TAM -->|en horticultura| H50["50 ha ya es enorme"]
    SA -->|se clasifica en| TIPb["Tipos de sistemas · mapa 2"]

    classDef tema fill:#dbeafe,stroke:#1e40af,color:#0b1b3f
    classDef dato fill:#fef9c3,stroke:#a16207,color:#3b2405
    classDef puente fill:#f3f4f6,stroke:#6b7280,color:#374151,stroke-dasharray:4 3
    class SA,COMP,OBJ,TAM tema
    class MAX,ESC dato
    class TIPb puente
```

## 2. Tipos de sistemas productivos (§3 a §6)

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 30, "rankSpacing": 40, "padding": 10}}}%%
flowchart LR
    SA["Sistema agropecuario"]
    SA -->|se clasifica en| CULT
    SA -->|se clasifica en| GANS
    SA -->|se clasifica en| MIXS
    subgraph CULT["Sistemas de cultivos"]
        direction LR
        EXT["Extensivos<br>grandes superficies ·<br>alto riesgo climático ·<br>menos producción y mano<br>de obra por ha ·<br>mucha mecanización"]
        EXT -->|en general| SEC["Secano<br>si se riega, por pivot central"]
        EXT --> ANU["Anuales: cereales y oleaginosas<br>controlar la humedad<br>en cosecha y almacenaje"]
        EXT --> ARR["Arroz<br>inundación ·<br>chacra sistematizada"]
        EXT --> FOR["Forestal<br>ciclos de ~10 años ·<br>madera o celulosa ·<br>empresas grandes"]
        INT["Intensivos<br>alta producción por ha ·<br>superficies chicas ·<br>mucha mano de obra ·<br>riego · postcosecha"]
        INT --> HOR["Horticultura<br>ciclos cortos · invernáculo,<br>túnel o hidroponía ·<br>cosecha manual · familiares"]
        INT --> FRU["Fruticultura<br>ciclos largos ·<br>implantación cara ·<br>polinización clave"]
    end
    subgraph GANS["Sistemas ganaderos"]
        direction LR
        GEX["Ganadería extensiva<br>campo natural · cargas bajas ·<br>poca mano de obra e insumos ·<br>bovinos y ovinos: carne y lana"]
        GIN["Ganadería intensiva<br>feedlot · aves, cerdos, conejos ·<br>sanidad y residuos ·<br>más impacto ambiental"]
        LEC["Lechería<br>Holando · pasturas + grano ·<br>reproducción · calidad de leche ·<br>efluentes · ordeñe diario ·<br>incorpora tecnología"]
        API["Apicultura<br>miel, polen, cera, propóleo ·<br>poliniza frutales y extensivos ·<br>sanidad crítica"]
    end
    subgraph MIXS["Sistemas mixtos"]
        direction LR
        MXD["Integran cultivos y ganado"]
        ROT["Rotaciones<br>agricultura–pasturas ·<br>arroz–ganadería"]
        SIL["Silvopastoril<br>forestación + ganado"]
        BOZ["Frutales o viña con ovejas<br>el bozal deja comer pasto,<br>no brotes"]
    end

    classDef tema fill:#dbeafe,stroke:#1e40af,color:#0b1b3f
    classDef dato fill:#fef9c3,stroke:#a16207,color:#3b2405
    class SA,EXT,INT,GEX,GIN,LEC,API tema
    class SEC,MXD dato
```

## 3. Personas y factores clave (§8 y §9)

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 30, "rankSpacing": 40, "padding": 10}}}%%
flowchart LR
    PER["Personas del sistema"]
    PER --> PRO["Productores<br>de primaria incompleta a doctorado ·<br>incorporan tecnología de manejo<br>si resuelve un problema"]
    PRO -->|pero tienen| BAJ["Baja adopción digital<br>miedo al riesgo tecnológico ·<br>costos · otras prioridades"]
    PRO -->|para adoptar<br>necesitan| CON["Conocer la solución<br>y que les aporte valor"]
    PRO -->|deciden con la| FAM["Familia<br>puertas adentro, muchas<br>veces decide la esposa"]
    PER --> TEC["Técnicos asesores<br>agrónomos · veterinarios"]
    TEC -->|pueden ser| ALI["Aliados o barreras<br>temen ser sustituidos"]
    PER --> TRA["Trabajadores rurales<br>nivel educativo bajo"]
    TRA -->|necesitan| SIM["Soluciones sencillas ·<br>capacitación simple ·<br>sin trabajo extra"]
    CNVb["Converge · mapa 6"] -.->|baja el| BAJ

    FCL["Factores clave"]
    FCL --> CC["Cambio climático"]
    CC -->|definición| CMN["CMNUCC art. 1<br>atribuible a la actividad humana ·<br>se suma a la variabilidad natural"]
    CC -->|se estudia en| DET["Detección → atribución"]
    CC -->|no incluye a| NIN["El Niño<br>fenómeno natural"]
    CC -->|trae| EXT["Eventos extremos<br>sequías · olas de calor ·<br>lluvias intensas · heladas ·<br>inundaciones · más plagas"]
    CC -->|exige| ADA["Adaptación y mitigación<br>monitoreo y decisión a tiempo"]
    FCL --> AMB["Cuidado del ambiente"]
    AMB --> AML["Menos GEI · biodiversidad ·<br>agua · servicios ecosistémicos ·<br>erosión"]
    AMB --> INS["Optimizar insumos<br>aplicación selectiva<br>de herbicidas"]
    AMB -->|define el acceso a| MER["Mercados<br>no te pagan más:<br>te dejan de comprar"]
    FCL --> POB["Menos gente en el campo"]
    POB -->|población rural<br>mundial| RUR["63 % en 1970 → 53 % en 2000<br>→ 40 % proyectado en 2030"]
    POB -->|se mitiga con un| AMI["Ambiente rural<br>más amigable"]
    POB -.->|impulsa las| FACb["AgroTIC · mapa 4"]

    classDef tema fill:#dbeafe,stroke:#1e40af,color:#0b1b3f
    classDef dato fill:#fef9c3,stroke:#a16207,color:#3b2405
    classDef puente fill:#f3f4f6,stroke:#6b7280,color:#374151,stroke-dasharray:4 3
    class PER,PRO,TEC,TRA,FCL,CC,AMB,POB tema
    class BAJ,CMN,DET,NIN,RUR dato
    class CNVb,FACb puente
```

## 4. Por qué y qué es digitalizar (§10 y §11)

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 30, "rankSpacing": 40, "padding": 10}}}%%
flowchart LR
    FAC["Factores que promueven<br>las AgroTIC"]
    FAC -->|en un contexto de| POBb["Menos gente en el campo · mapa 3"]
    FAC -->|y de la tendencia a| OBJT["Objetivar lo que se registra<br>de subjetivo e inconsistente<br>a objetivo y consistente"]
    FAC --> FA["Conectividad y celulares<br>Starlink llega a zonas remotas"]
    FAC --> FB["Equipos y sensores más baratos<br>estación meteorológica ~USD 200"]
    FAC --> FS["Software de gestión maduro"]
    FAC --> FD["Recambio generacional<br>nativos digitales"]
    FAC --> FE["Escasez de mano de obra<br>por ejemplo, para cosechar"]
    FAC --> FF["Mejores condiciones laborales<br>el tambo a las 3 de la mañana"]
    FAC --> FG["Menos trabajo rutinario"]
    FAC -->|promueven| DIG["Digitalizar<br>integrar datos, procesos<br>y decisiones en un<br>ecosistema conectado"]
    DIG -->|no es| NOA["Tener tres aplicaciones<br>y un WhatsApp"]
    DIG -->|usa| HER["Sensores · drones · satélites ·<br>IoT · big data · IA para predecir ·<br>blockchain y trazabilidad"]
    DIG -->|en el predio| APL["AgroTIC a nivel predio · mapas 5 y 6<br>IoT · monitoreo · alertas ·<br>apoyo a la gestión · análisis de datos ·<br>automatización · robotización ·<br>sistemas inteligentes de decisión"]

    classDef tema fill:#dbeafe,stroke:#1e40af,color:#0b1b3f
    classDef dato fill:#fef9c3,stroke:#a16207,color:#3b2405
    classDef puente fill:#f3f4f6,stroke:#6b7280,color:#374151,stroke-dasharray:4 3
    class FAC,DIG tema
    class NOA dato
    class POBb,APL puente
```

## 5. AgroTIC: IoT, monitoreo y alertas (§12 a–c)

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 30, "rankSpacing": 40, "padding": 10}}}%%
flowchart LR
    IOT["IoT"]
    IOT -->|conecta| IOE["Equipos, luces, bombas<br>y refrigeración que se<br>manejan desde el celular"]

    MON["Monitoreo<br>clima · suelo · agua ·<br>animales · vegetación"]
    MON -->|para| AYP["Analizar y después predecir"]
    MON -.->|ayuda a enfrentar el| CCb["Cambio climático · mapa 3"]
    MON --> EST["Estaciones automáticas INIA<br>lluvia y temperatura cada hora"]
    EST -->|con el histórico| ANO["Anomalía<br>mes actual vs. promedio<br>del mismo mes ·<br>verde = más lluvia, rojo = menos"]
    MON --> BH["Balance hídrico<br>lluvia + tipo de suelo"]
    BH -->|estima el| PAD["PAD<br>% de agua disponible en el suelo ·<br>condiciona la productividad"]
    MON --> NDV["NDVI<br>bandas roja + infrarroja → vigor ·<br>por décadas de 10 días ·<br>anomalía: gris = promedio"]
    MON -->|permite una| PRE["Previsión probabilística<br>reducir carga · comprar ración"]

    ALE["Alertas<br>plagas · enfermedades ·<br>ambiente · seguridad"]
    ALE -->|regla| REG["Toda alerta va asociada<br>a una medida de manejo ·<br>contraejemplo: granizo"]
    ALE --> AO["Alerta Ovina<br>corderos en sus primeras 72 h"]
    AO -->|usa el| CHI["Chill index<br>frío + viento + lluvia ·<br>crítico: más de 1200 kJ/m²/h"]
    AO -->|medida| AOM["Majada a resguardo<br>en pariciones"]
    ALE --> TE["INIA Termoestrés<br>lechería y carne intensiva"]
    TE -->|usa el| ITH["ITH<br>temperatura y humedad ·<br>aviso con 5–7 días ·<br>alerta 68–72 · peligro 72–79 ·<br>emergencia: más de 79"]
    TE -->|medidas| TEM["No mover el ganado ·<br>agua · aspersión"]
    ALE --> TM["INIA Termomín<br>mínimas a 5 días ·<br>proxy de helada"]
    TM -->|umbral| TMU["Lo elige el usuario<br>por ejemplo bajo 0 °C<br>o bajo 2 °C"]
    REG -.->|se cumple con| AOM
    REG -.->|se cumple con| TEM

    classDef tema fill:#dbeafe,stroke:#1e40af,color:#0b1b3f
    classDef herr fill:#dcfce7,stroke:#166534,color:#052e16
    classDef dato fill:#fef9c3,stroke:#a16207,color:#3b2405
    classDef puente fill:#f3f4f6,stroke:#6b7280,color:#374151,stroke-dasharray:4 3
    class IOT,MON,ALE tema
    class EST,AO,TE,TM herr
    class ANO,PAD,NDV,REG,CHI,ITH,TMU dato
    class CCb puente
```

## 6. AgroTIC: gestión, datos, automatización, decisión y difusión (§12 d–j)

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 30, "rankSpacing": 40, "padding": 10}}}%%
flowchart LR
    GES["Apoyo a la gestión"]
    GES --> FER["Fertilización<br>OptiFert-P: fósforo en pasturas<br>OptiFert-N: nitrógeno en trigo<br>Fertiliz-Arr: N, P y K en arroz"]
    GES --> GSR["GESIR: riego<br>balance hídrico FAO-56"]
    GSR -->|el agua depende de la| FAS["Fase del cultivo<br>y de si llovió"]
    GES --> SAR["SARAS<br>roya asiática de la soja ·<br>avisa focos a menos de 100 km"]
    GES --> MOV["INIA Móvil<br>super app con todas las<br>apps de INIA · la ubicación<br>se carga una vez"]
    GES --> AUR["Auravant<br>índices de vegetación<br>por chacra"]
    AUR -->|permite| SEL["Aplicar solo en zonas<br>comprometidas · menos<br>insumos y menos costo"]
    ALEb["Alertas de INIA · mapa 5"] -.->|se reúnen en| MOV

    DAT["Análisis de datos"]
    DAT -->|requiere| ROB["Datos suficientes y robustos<br>si entra basura, sale basura"]
    DAT --> MPR["Modelos predictivos<br>sobre series históricas"]
    DAT --> GEM["Gemelos digitales<br>probar sin esperar<br>tiempos biológicos"]

    AUT["Automatización<br>porteras · bombas · riego ·<br>climatización"]
    AUT --> RAP["Riego automático de pasturas<br>empresa nacional + ANII +<br>Fagro + INIA"]
    RAP -->|su enemigo principal| VIE["El viento<br>afecta la uniformidad"]
    AUT --> HAL["Alambrados virtuales: Halter<br>collares con estímulos<br>positivos y negativos"]
    HAL -->|ventajas| HAV["Sin alambrado físico ·<br>el potrero se mueve<br>digitalmente · protege<br>zonas sensibles"]

    RBZ["Robotización<br>invernáculos · ordeñe ·<br>maquinaria"]
    RBZ --> VMS["Ordeñe voluntario VMS<br>INIA Las Brujas<br>y La Estanzuela"]
    VMS -->|cómo funciona| VMC["La vaca va sola, atraída<br>por comida · un collar<br>la identifica · muy caro"]
    VMS -.->|transforma la| MOb["Mano de obra · mapa 7"]

    SID["Sistemas inteligentes<br>de decisión<br>integran toda la<br>información predial"]
    SID -->|pero| DEC["La decisión final<br>es del productor"]
    DEC -.->|porque tiene<br>otras lógicas| OBJb["Objetivo del productor · mapa 1"]
    SID -->|deben| REQ["Integrar fuentes y escalas ·<br>dar resultados sencillos ·<br>estimar el futuro"]
    SID -->|incluyen| CHA["Chatbots y agentes<br>solo sirven con<br>información robusta"]
    SID -->|exigen| ITO["Interoperabilidad<br>sin islas de información"]
    SID -->|exigen| CAP["Capacitación<br>según el público objetivo"]

    DIF["Difusión y adopción"]
    DIF --> GRA["GRAS de INIA<br>clima · monitoreo ambiental ·<br>seguros"]
    GRA --> SEG["Seguro de sequía para soja<br>del BSE · según el PAD paga<br>15, 25 o 40 % del capital"]
    DIF --> CNV["Converge<br>INIA + BID Lab ·<br>apoyo de ANII"]
    CNV -->|baja el| RTE["Riesgo tecnológico"]
    CNV --> VER["Verificación<br>¿hace lo que dice?"]
    CNV --> VLD["Validación<br>¿es usable? entrevistas<br>a productores"]

    classDef tema fill:#dbeafe,stroke:#1e40af,color:#0b1b3f
    classDef herr fill:#dcfce7,stroke:#166534,color:#052e16
    classDef dato fill:#fef9c3,stroke:#a16207,color:#3b2405
    classDef puente fill:#f3f4f6,stroke:#6b7280,color:#374151,stroke-dasharray:4 3
    class GES,DAT,AUT,RBZ,SID,DIF tema
    class FER,GSR,SAR,MOV,AUR,RAP,HAL,VMS,GRA,CNV herr
    class ROB,DEC,SEG,VER,VLD dato
    class ALEb,MOb,OBJb puente
```

## 7. Valor, oportunidades y desafíos (§13 a §17)

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 30, "rankSpacing": 40, "padding": 10}}}%%
flowchart LR
    VAL["Digitalizar tiene sentido<br>solo si agrega valor"]
    VAL --> VVS["Producir más con menos ·<br>adaptarse al cambio climático ·<br>abrir mercados · ser sostenibles"]
    VAL --> INC["Incluir a pequeños y grandes"]
    INC -->|los pequeños son| PEQ["Muchos: mercado potencial<br>y soberanía alimentaria"]
    VAL -->|abre| OPP["Oportunidades"]
    OPP --> O1["Eficiencia de recursos<br>riego de precisión ·<br>fertilización diferenciada ·<br>control selectivo de plagas"]
    OPP --> O2["Productividad y decisiones<br>datos · modelos predictivos ·<br>gemelos digitales"]
    OPP --> O3["Gestión y transferencia<br>del riesgo<br>seguros agropecuarios"]
    OPP --> O4["Resiliencia y sostenibilidad<br>menos huella · salud del<br>suelo y la vegetación"]
    OPP --> O5["Democratizar la información<br>chatbots confiables para<br>quien no tiene asesor"]
    OPP --> O6["Mercados y trazabilidad<br>exportación ·<br>comercio digital local"]
    OPP --> O7["Eficiencia logística<br>ante la falta de mano de obra"]
    OPP --> O8["Cumplimiento regulatorio<br>y certificación"]
    VAL -->|enfrenta| DES["Desafíos"]
    DES --> D1["Infraestructura y conectividad"]
    DES --> D2["Capacitación y usabilidad<br>botones chicos, dedos grandes"]
    DES --> D3["Costos"]
    DES --> D4["Aversión al cambio<br>y riesgo tecnológico"]
    DES --> D5["Brechas entre productores<br>familiares y avanzados"]
    DES --> D6["Transformación de la<br>mano de obra, no sustitución"]
    DES --> D7["Poca integración en la cadena<br>silos de información"]
    DES --> D8["Propiedad de los datos<br>uso comercial no autorizado"]
    DES --> D9["Datos no interoperables"]
    DES --> D10["Falta de herramientas<br>para promover la adopción"]
    CNVb["Converge · mapa 6"] -.->|intenta reducir la| D4
    VMSb["Robot de ordeñe · mapa 6"] -.->|es un ejemplo de| D6
    VAL -->|porque| CIE["La digitalización no es un fin:<br>es un medio para generar valor<br>económico, ambiental y social"]
    CIE -->|en una frase| LEM["El agro no necesita más apps,<br>necesita más valor"]
    CIE -->|hay que partir de| NEC["Necesidades reales, no modas ·<br>una solución que busca<br>su problema suele fracasar"]

    APb["AgroTIC · mapas 5 y 6"] -.->|también se usan en| INV["Investigación<br>público objetivo más<br>abierto a probar"]
    INV -->|sus soluciones<br>migran a| AVZ["Productores de avanzada"]
    INV -->|ejemplos| INE["Nodos de sensores ·<br>imágenes térmicas y radar ·<br>sensores de nutrientes ·<br>trampa electrónica que<br>identifica polillas ·<br>monitoreo por ambiente"]

    classDef tema fill:#dbeafe,stroke:#1e40af,color:#0b1b3f
    classDef dato fill:#fef9c3,stroke:#a16207,color:#3b2405
    classDef puente fill:#f3f4f6,stroke:#6b7280,color:#374151,stroke-dasharray:4 3
    class VAL,OPP,DES,INV,CIE tema
    class LEM dato
    class CNVb,VMSb,APb puente
```
