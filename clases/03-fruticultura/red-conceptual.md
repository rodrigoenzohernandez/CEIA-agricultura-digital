# Red conceptual — Clase 3: Fruticultura

Complemento del [resumen](resumen.md). Primero hay una vista general de toda la clase y después un mapa por tema, en el orden en que se dieron. Los números de sección (§) remiten al resumen.

**Cómo leerla**
- Cada flecha forma una frase: *Fruticultura → tiene → baja frecuencia de disturbios*. Una flecha sin texto quiere decir "incluye".
- Las flechas punteadas unen conceptos de temas distintos.
- Colores: azul = tema · verde = herramienta, tecnología o caso real · amarillo = dato para memorizar · gris punteado = concepto que se desarrolla en otro mapa.

> Todo el contenido sale de la clase. La organización y las frases de las flechas son propias.

## Vista general

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 30, "rankSpacing": 40, "padding": 10}}}%%
flowchart TD
    FIS["① Fisiología<br>economía del carbono<br>y del agua"]
    AMB["Las plantas sensan<br>el ambiente · G × A"]
    FRU["② Fruticultura<br>leñosas permanentes ·<br>pocos disturbios"]
    ARG["Fruticultura argentina<br>514.701 ha · 1,4 % ·<br>economías regionales"]
    ESP["Vid · cítricos · olivo ·<br>pepita · carozo"]
    CIC["③ Ciclo anual<br>otoño · invierno ·<br>primavera · verano"]
    PRA["Prácticas<br>poda · cosecha · riego"]
    POS["④ Postcosecha<br>climatéricas · empaque ·<br>atmósfera controlada"]
    ROB["Robots de cosecha<br>plataforma · drones"]
    TIE["⑤ Técnica del<br>insecto estéril"]
    SIT["⑥ SITIA<br>visión + CNN + láser"]

    FIS -->|explica el crecimiento de la| FRU
    FIS -->|las plantas responden con| AMB
    AMB -->|elegir la variedad<br>según el lugar| ESP
    FRU -->|en Argentina| ARG
    ARG -->|se cultiva| ESP
    FRU -->|se repite cada año| CIC
    CIC -->|marca el momento de las| PRA
    ESP -->|una sola cosecha:<br>hay que guardarla| POS
    PRA -->|la cosecha a mano<br>es un problema| ROB
    FRU -->|las plagas se combaten<br>con la| TIE
    TIE -->|necesita separar sexos:<br>lo resuelve| SIT
    POS -.->|visión para detectar<br>fruta enferma| SIT

    classDef tema fill:#dbeafe,stroke:#1e40af,color:#0b1b3f
    classDef herr fill:#dcfce7,stroke:#166534,color:#052e16
    classDef dato fill:#fef9c3,stroke:#a16207,color:#3b2405
    class FIS,FRU,CIC,POS,TIE tema
    class SIT,ROB herr
    class ARG dato
```

## 1. Fisiología: carbono, agua y ambiente (§1 a §5)

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 30, "rankSpacing": 40, "padding": 10}}}%%
flowchart LR
    PLA["Plantas<br>productores primarios ·<br>base de la red trófica"]
    PLA -->|hacen| FOT["Fotosíntesis<br>luz + CO₂ + poca agua →<br>azúcares + O₂"]
    FOT -->|ocurre en| VER["Órganos verdes<br>clorofila"]
    FOT -->|retiene carbono:| CAP["Captura de carbono<br>en frutos y raíces"]
    FOT -->|da lugar a la| ECC["Economía del carbono"]
    ECC -->|depende de la| RIN["Radiación interceptada<br>no la incidente"]
    RIN -->|se maneja con| DEN["Densidad de plantación<br>y poda"]
    ECC -->|la regulan los| EST["Estomas · en el envés<br>abiertos: entra CO₂ y se<br>pierde agua · una canilla"]
    PLA -->|dependen de la| ECA["Economía del agua"]
    ECA -->|el agua sube por| POT["Diferencia de<br>potencial hídrico"]
    ECA -->|la célula crece por| TUR["Turgencia<br>el globo empuja la caja"]
    TUR -->|sin agua| PRI["Primero se frena<br>el crecimiento · la fotosíntesis,<br>mucho después"]
    EST -.->|se cierran ante<br>el déficit hídrico| ECA
    PLA -->|son sésiles y sensan| SEN["Calidad e intensidad de luz ·<br>fotoperíodo · estrés y<br>exceso hídrico"]
    SEN -->|responden con| RES["Hormonas · morfología ·<br>modulación del crecimiento"]
    RES -->|distinto según la variedad:| GXA["Interacción genotipo × ambiente<br>B gana en el restrictivo,<br>A en el favorable"]
    GXA -->|aplicación| TES["Tesis con el INTA<br>variables para elegir<br>variedades de duraznero"]

    classDef tema fill:#dbeafe,stroke:#1e40af,color:#0b1b3f
    classDef herr fill:#dcfce7,stroke:#166534,color:#052e16
    classDef dato fill:#fef9c3,stroke:#a16207,color:#3b2405
    class PLA,FOT,ECC,ECA,GXA tema
    class TES herr
    class PRI,RIN dato
```

## 2. La fruticultura en Argentina (§6 a §12)

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 30, "rankSpacing": 40, "padding": 10}}}%%
flowchart LR
    INT["Cultivos intensivos<br>alta densidad · rinde por ha ·<br>riego · postcosecha"]
    INT -->|incluye la| FRU["Fruticultura<br>especies leñosas y semileñosas<br>que producen frutas"]
    FRU -->|tiene| PER["Estructuras permanentes<br>20 a 100 años · pocos disturbios ·<br>mano de obra media"]
    FRU -->|en Argentina| ARG["514.701 ha · 1,4 % de la<br>superficie agrícola · 22 provincias<br>Mendoza, San Juan, Tucumán,<br>Entre Ríos y Río Negro"]
    ARG --> VID["Vid 38,7 %<br>215.000 ha · Mendoza ·<br>vino (883 bodegas), pasas,<br>uva de mesa · Malbec"]
    ARG --> CIT["Cítricos 23,8 %<br>hasta San Pedro · limón en<br>Tucumán · 2.º exportador<br>de limón fresco"]
    ARG --> OLI["Olivo 14,6 %<br>85.000 ha en Cuyo y NOA"]
    ARG --> PEP["Pepita 8,4 %<br>manzana y pera · valle del<br>Río Negro y Mendoza"]
    ARG --> CAR["Carozo 6,3 %<br>durazno y ciruela ·<br>Mendoza 84 %"]
    ARG --> OTR["Frutos secos 5,3 % (pecán,<br>pistacho) · tropicales 1,4 %"]
    VID -->|conducción| CON["Parral con acequia (árido) ·<br>espaldera con goteo (húmedo)"]
    CIT -->|se aprovecha todo| IND["Jugo · cáscara abrillantada ·<br>esencias · 1.º en esencia y jugo"]
    OLI --> ARB["Arbequina<br>la más plantada · aceite suave"]
    OLI --> ARA["Arauco · cultivar nacional<br>punta torcida: no se puede<br>descarozar a máquina"]
    PEP -->|la más buscada| RED["Red Delicious"]
    PEP -->|Argentina, 1.º exportador<br>mundial de| PER2["Pera fresca<br>a Brasil y Rusia"]
    CAR -->|postcosecha corta:| VAR["Muchas variedades<br>para cubrir el verano"]
    PEP -.->|una sola cosecha:<br>manzanas de cámara| POSb["Postcosecha · mapa 4"]

    classDef tema fill:#dbeafe,stroke:#1e40af,color:#0b1b3f
    classDef herr fill:#dcfce7,stroke:#166534,color:#052e16
    classDef dato fill:#fef9c3,stroke:#a16207,color:#3b2405
    classDef puente fill:#f3f4f6,stroke:#6b7280,color:#374151,stroke-dasharray:4 3
    class INT,FRU,VID,CIT,OLI,PEP,CAR tema
    class CON,IND herr
    class ARG,ARA,PER2,RED dato
    class POSb puente
```

## 3. Ciclo anual y prácticas de manejo (§13 y §14)

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 30, "rankSpacing": 40, "padding": 10}}}%%
flowchart LR
    CIC["Ciclo anual<br>se repite cada año ·<br>fenología del cultivo"]
    CIC --> OTO["Otoño<br>caen las hojas (salvo cítricos<br>y olivo) · reservas a ramas<br>y raíces · dormición"]
    OTO -->|señal segura| FOT["Acortamiento del fotoperíodo<br>la temperatura engaña"]
    CIC --> INV["Invierno<br>acumulación de horas de frío"]
    INV -->|evita| BRO["Brotar con el<br>primer veranito"]
    CIC --> PRI["Primavera<br>brotación · floración · cuajado"]
    PRI -->|de la flor sale el fruto| FEC["Ovario → pulpa · óvulos → semillas<br>el embrión manda las hormonas"]
    FEC --> KIW["Kiwi: se vende polen<br>más semillas, más tamaño"]
    FEC --> PAR["Partenocárpicos<br>sin semilla: hormonas<br>o variedad"]
    CIC --> VER["Verano<br>crecimiento y maduración"]
    CIC -->|ordena las| PRA["Prácticas"]
    PRA --> RAL["Raleo de flores<br>menos frutos, más grandes"]
    PRA --> POD["Poda<br>manual: selectiva ·<br>mecánica: corta como una pared"]
    PRA --> COS["Cosecha<br>manual · cabalgante ·<br>shaker con paraguas (el más usado)"]
    PRA --> RIE["Riego<br>acequia por turno → goteo ·<br>fertirriego · sensores"]
    CIC -->|se mide con la| ESC["Escala fenológica<br>del manzano, de A a J"]
    ESC -->|helada en D, E<br>o floración| HEL["Se pierde la<br>fruta del año"]
    COS -.->|cuadrillas temporarias:<br>urge mecanizar| ROBb["Robots de cosecha · §17"]

    classDef tema fill:#dbeafe,stroke:#1e40af,color:#0b1b3f
    classDef herr fill:#dcfce7,stroke:#166534,color:#052e16
    classDef dato fill:#fef9c3,stroke:#a16207,color:#3b2405
    classDef puente fill:#f3f4f6,stroke:#6b7280,color:#374151,stroke-dasharray:4 3
    class CIC,PRA,OTO,INV,PRI,VER tema
    class POD,COS,RIE herr
    class FOT,HEL dato
    class ROBb puente
```

## 4. Postcosecha: maduración, empaque y almacenamiento (§15 a §17)

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 30, "rankSpacing": 40, "padding": 10}}}%%
flowchart LR
    MAD["Maduración<br>color · textura · sabor"]
    MAD --> CLI["Climatéricas<br>se cosechan verdes ·<br>pico de etileno y de respiración"]
    MAD --> NOC["No climatéricas<br>se cosechan maduras ·<br>etileno bajo y constante"]
    CLI -->|ejemplos| CLE["Banana · palta · manzana ·<br>pera · arándano · durazno ·<br>pelón · ciruela · kiwi"]
    NOC -->|ejemplos| NOE["Cítricos · uva · cereza"]
    CLI -->|una fruta golpeada| CON["Contagia a las vecinas<br>efecto exponencial ·<br>no exhibirlas juntas"]
    CLI -->|en el pico, la fruta| CON2["Se consume a sí misma<br>controlar etileno y respiración"]
    MAD -->|la fruta pasa por la| EMP["Planta de empaque<br>lavado · tamaño · fungicidas<br>y ceras"]
    EMP -->|clasificar defectos con| VIS["Visión por computadora<br>una fruta enferma puede<br>cerrar la exportación"]
    EMP -->|después va al| ALM["Almacenamiento<br>la manzana de marzo<br>llega a diciembre"]
    ALM --> AC["Atmósfera controlada<br>frío · menos O₂ (nitrógeno) ·<br>más CO₂ · absorbedores ·<br>humedad y aire"]
    ALM --> MCP["1-MCP<br>ocupa el receptor del etileno ·<br>maduración lenta"]
    CON2 -.->|lo que buscan| AC
    MAD -.->|cosecha a mano, cara<br>y con cuadrillas| ROB["Gonzalo: plataforma autónoma<br>+ brazo de 2 GDL + red ·<br>drones pulpo: lentos"]

    classDef tema fill:#dbeafe,stroke:#1e40af,color:#0b1b3f
    classDef herr fill:#dcfce7,stroke:#166534,color:#052e16
    classDef dato fill:#fef9c3,stroke:#a16207,color:#3b2405
    class MAD,CLI,NOC,EMP,ALM tema
    class VIS,AC,MCP,ROB herr
    class CON2 dato
```

## 5. La plaga y la técnica del insecto estéril (§19 a–i)

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 30, "rankSpacing": 40, "padding": 10}}}%%
flowchart LR
    SUZ["Drosophila suzukii<br>mosca de las alas manchadas"]
    SUZ -->|pariente de| MEL["D. melanogaster<br>la de la cocina · no es plaga"]
    SUZ -->|es plaga por el| OVI["Ovipositor aserrado<br>perfora fruta sana"]
    SUZ -->|y porque pone| HUE["Hasta 380 huevos<br>40 por día"]
    SUZ -->|el macho tiene| MAC["Manchas en las alas ·<br>peines sexuales"]
    SUZ -->|ciclo de 25 a 55 días| CIC["Huevo 12–72 h · larva 5–7 d<br>dentro de la fruta · pupa 4–15 d ·<br>adulto 15–30 d"]
    SUZ -->|se expandió| EXP["Japón 1916 → EE. UU., España<br>e Italia 2008 → Brasil y<br>Argentina 2015"]
    SUZ -->|daña| DAN["Hasta 65 % de pérdida ·<br>contenedores perdidos al 100 %"]
    DAN -->|métodos que no alcanzan| CTR["Pesticidas · trampas ·<br>métodos culturales ·<br>control biológico (la avispa<br>no se puede traer)"]
    CTR -->|alternativa| TIE["Técnica del insecto estéril<br>criar → irradiar pupas (gamma) →<br>liberar machos 10 a 1"]
    TIE -->|la hembra pone| INV["Huevos inviables<br>la población baja casi a cero"]
    TIE -->|necesita| SOL["Solo machos"]
    SOL -->|mosquitos: suben la<br>temperatura del reactor| MOS["Mueren las hembras ·<br>mosquitos rojos del ISCAMEN"]
    SOL -->|D. suzukii: no hay método| SITb["SITIA · mapa 6"]

    classDef tema fill:#dbeafe,stroke:#1e40af,color:#0b1b3f
    classDef herr fill:#dcfce7,stroke:#166534,color:#052e16
    classDef dato fill:#fef9c3,stroke:#a16207,color:#3b2405
    classDef puente fill:#f3f4f6,stroke:#6b7280,color:#374151,stroke-dasharray:4 3
    class SUZ,TIE,SOL tema
    class MOS herr
    class HUE,CIC,EXP,DAN dato
    class SITb puente
```

## 6. SITIA: visión, IA y láser (§19 j–r)

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 30, "rankSpacing": 40, "padding": 10}}}%%
flowchart LR
    SIT["SITIA<br>Luciano Ciminari Smith ·<br>INTA y CONICET Bariloche"]
    SIT --> ADQ["Adquisición<br>cámara 12 MP · lente 16 mm ·<br>aro de luz · fondo blanco"]
    ADQ -->|moscas dormidas en la| PLA["Placa de anestesia<br>laberinto de acrílico con CO₂"]
    SIT --> DET["Detección<br>brillo · grises · desenfoque<br>gaussiano · binarización ·<br>erosión y dilatación · contornos"]
    SIT --> CLA["Clasificación<br>CNN de 6 capas · 150 × 150 × 3 ·<br>4 conv + ReLU + max pooling ·<br>2 fully connected"]
    CLA -->|¿qué mira la red?| RIS["RISE: mapas de calor<br>hembra: cabeza y ovipositor ·<br>macho: manchas y abdomen"]
    SIT --> ELI["Eliminación de hembras<br>láser NEJE 3"]
    ELI -->|ordenar el recorrido<br>con metaheurísticas| REC["Greedy −55,9 % · búsqueda local<br>−58,6 % en 0,49 s (la elegida) ·<br>hormigas −66,6 % en 5,4 s"]
    SIT -->|resultados| RES["144 moscas, 1 error ·<br>precisión > 98 % ·<br>−96 % de tiempo"]
    RES -->|ejemplo| EJE["100 ha → 300.000 machos<br>por semana · 100 h a mano<br>vs. 4 h con SITIA"]
    SIT -->|se publicó en| PAP["Insects (MDPI)<br>y se está patentando"]
    SIT -->|se vendió a Chile| CHI["Cinta transportadora<br>con servos y carriles ·<br>todavía con errores"]
    ADQ -.->|controlar la captura<br>simplifica el modelo| CLA

    classDef tema fill:#dbeafe,stroke:#1e40af,color:#0b1b3f
    classDef herr fill:#dcfce7,stroke:#166534,color:#052e16
    classDef dato fill:#fef9c3,stroke:#a16207,color:#3b2405
    class SIT tema
    class ADQ,DET,CLA,ELI,PLA,RIS,CHI herr
    class REC,RES,EJE dato
```
