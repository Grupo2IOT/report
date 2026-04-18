
# Capítulo I: Introducción

## 1.1. Startup Profile

### 1.1.1. Descripción de la Startup

### 1.1.2. Perfiles de integrantes del equipo

## 1.2. Solution Profile

### 1.2.1 Antecedentes y problemática

A continuación, se expone el análisis del contexto actual que enmarca la crisis hídrica en la pequeña agricultura de la costa norte del Perú, específicamente en la región Piura. Para comprender a profundidad la magnitud de este desafío, identificar a los actores afectados y establecer las bases justificables de nuestra propuesta tecnológica, se ha aplicado la técnica de análisis de problemas de las 5 'W's y 2 'H's (Who, What, Where, When, Why, How & How Much)

1. **What (Cuál es el problema real):** Existe un déficit hídrico extremo y una latente amenaza de sequía que pone en peligro la campaña agrícola 2024-2025. Este problema natural se agrava drásticamente por una ineficiencia humana: en el Perú, el 80% del agua disponible se destina al sector agrícola, pero solo el 30% de este recurso se distribuye y utiliza correctamente. Además, el uso de sistemas de riego tradicionales por gravedad o inundación desperdicia agua y lava los nutrientes esenciales del suelo.
2. **Why (Por qué ocurre y por qué es necesario resolverlo)** Ocurre porque el clima se ha vuelto impredecible y los agricultores carecen de herramientas tecnológicas para optimizar el poco recurso hídrico que tienen. Es necesario resolverlo porque la falta de agua o su mala gestión frena el desarrollo rural. La actual infraestructura de comunicación en el campo suele ser inestable y de alto costo operativo, lo que impide un monitoreo confiable y vuelve lenta la toma de decisiones.
3. **Who (Quiénes están involucrados / afectados):** El problema afecta directamente a los pequeños y medianos productores agrícolas de la costa norte, específicamente de la región Piura, cuyas familias dependen de esta actividad como principal fuente de ingresos y subsistencia. La crisis también impacta a las juntas de usuarios y asociaciones agrícolas que no cuentan con la tecnología o el capital para soportar la escasez del recurso.
4. **Where (Dónde ocurre):** El problema se concentra en el departamento de Piura y los valles agrícolas del norte peruano, los cuales dependen críticamente de las lluvias y de las reservas de agua almacenadas en reservorios vitales, como Poechos y San Lorenzo, que actualmente se encuentran amenazados. A esto se suma que son zonas rurales con deficiente cobertura celular y escasa infraestructura eléctrica.
5. **When (Cuándo ocurre):** La situación es una crisis actual y urgente que amenaza la presente campaña agrícola 2024-2025. Se agudiza severamente durante los meses de estiaje y por los constantes cambios en los patrones de precipitación provocados por el cambio climático y fenómenos como El Niño/La Niña, que hacen imposible predecir el clima de forma tradicional.
6. **How (Cómo se resolverá el problema):** Se resolverá mediante el diseño de un sistema de riego de precisión automatizado que no dependa de la conectividad a internet tradicional.

    - Se utilizarán sensores de suelo para medir con exactitud variables críticas como la humedad y los niveles de macronutrientes (NPK), evitando el exceso o déficit de agua y fertilizantes.

    - Para superar la falta de señal celular en el campo, la transmisión de datos utilizará la tecnología de conectividad LoRaWAN, que permite enviar información a largas distancias (hasta 15 km en campo abierto) con un consumo de batería mínimo.

    - La "inteligencia" del sistema aplicará una arquitectura Edge AI o TinyML, permitiendo que el microcontrolador local procese los datos de los sensores y decida accionar las válvulas de riego de manera autónoma, resolviendo el problema de la falta de internet rural.

7. **How Much (Cuánto es el impacto / magnitud del problema):** El costo de no actuar ya se está cuantificando en pérdidas reales: la sequía pone en riesgo cientos de hectáreas, como las 100 hectáreas de banano orgánico amenazadas en Piura. Incluso, medianas empresas agrícolas se han visto obligadas a comprar agua de cisternas a costos elevadísimos o sacrificar y suspender el riego hasta en un 20% de sus lotes cosechados para intentar salvar la fruta en maduración. Tu solución busca reducir estas pérdidas millonarias y aumentar la eficiencia del riego hasta en un 30%.

Como se ha evidenciado, la ineficiencia en la distribución del recurso hídrico y la falta de conectividad en zonas rurales exigen una solución tecnológica que sea autónoma e inteligente. Sin embargo, para asegurar que el diseño de este sistema de riego IoT basado en Edge Computing realmente resuelva los problemas reales de los agricultores y tenga viabilidad como modelo de negocio, es necesario centrarse en el usuario. Por ello, a continuación se aplicará el Lean UX Process, una metodología que nos permitirá alinear las necesidades urgentes del sector agrícola con la visión y estrategia de nuestra startup, definiendo claramente el problema del negocio, nuestras suposiciones e hipótesis.

### 1.2.2 Lean UX Process

#### 1.2.2.1. Lean UX Problem Statements

Para definir el problema de nuestra startup, analizamos el contexto actual basándonos en los siguientes aspectos:

- **Domain:** El sector agrícola en el Perú, específicamente la gestión y optimización de recursos hídricos frente a escenarios de sequía, donde actualmente del 80% del agua destinada al sector, solo el 30% se distribuye de manera eficiente por métodos tradicionales.

- **Customer Segments e Initial Segment:** Nuestro segmento inicial son los pequeños y medianos productores agrícolas de la región Piura (costa norte del Perú), cuyas parcelas sufren estrés hídrico.

- **Pain Points (Puntos de dolor):** Los agricultores se enfrentan a un déficit hídrico crítico originado por el bajo nivel del reservorio Poechos y las irregularidades climáticas. Al no tener herramientas tecnológicas para medir la humedad del suelo, riegan por inundación, desperdiciando el poco recurso disponible y poniendo en riesgo de pérdida total su campaña agrícola.

- **Gap (Brecha tecnológica):** Los sistemas IoT de riego inteligente actuales en el mercado dependen de plataformas en la nube (Cloud), lo que los hace inoperativos en las zonas rurales agrícolas del Perú donde la conectividad a internet es inestable o nula.

- **Vision / Strategy (Visión y Estrategia):** Proveer un sistema de riego de precisión descentralizado mediante arquitectura Edge Computing que tome decisiones localmente, asegurando la autonomía del agricultor incluso sin internet.

> [!NOTE] Problem Statement:
> *"Nuestra startup ha observado que los pequeños productores agrícolas de Piura están sufriendo graves pérdidas económicas debido al estrés hídrico y a la ineficiencia de sus métodos tradicionales de riego. Las soluciones de agricultura inteligente existentes en el mercado no logran escalar en el campo porque dependen de una conexión constante a la nube, la cual es inexistente en zonas rurales. ==**¿Cómo podríamos diseñar e implementar un sistema de riego de precisión basado en Edge Computing (para la toma de decisiones locales) y conectividad de largo alcance (LoRaWAN), para que los agricultores puedan automatizar su riego de forma autónoma sin depender de internet, logrando reducir el consumo de agua y asegurando la supervivencia de sus cultivos durante las sequías?**=="*

#### 1.2.2.2. Lean UX Assumptions

#### 1.2.2.3. Lean UX Hypothesis Statements

#### 1.2.2.4. Lean UX Canvas

## 1.3. Segmentos objetivo
