
# Capítulo II: Requirements Elicitation & Analysis

## 2.1. Competidores.

Para el desarrollo de nuestra solución, hemos identificado a tres empresas y marcas que representan las alternativas actuales de riego tecnificado e inteligente en el mercado peruano:

1. **Competidor 1 (Directo - Global): Netafim.** Empresa transnacional israelí, líder mundial en riego por goteo y agricultura de precisión, con fuerte presencia en la agroexportación peruana.
2. **Competidor 2 (Directo - Local): Smelpro.** Empresa peruana integradora de soluciones IoT industriales que ofrece sistemas de riego utilizando sensores y tecnología LoRaWAN conectados a la nube.
3. **Competidor 3 (Indirecto - Comercial): Rain Bird.** Corporación global y marca dominante en la venta de hardware de riego tradicional y controladores comerciales basados en Wi-Fi, muy usados a nivel local.

A continuación, se desarrolla el análisis competitivo:

### 2.1.1. Análisis competitivo.

**¿Por qué llevar a cabo este análisis?** Identificar las brechas tecnológicas y comerciales de las empresas de riego actuales en el mercado peruano, para validar cómo nuestra arquitectura Edge Computing representa una ventaja competitiva única para zonas rurales sin internet frente a soluciones que dependen estrictamente de la Nube (Cloud) o Wi-Fi local.

| Perfil | Nuestra Startup | Comp. 1: Netafim | Comp. 2: Smelpro | Comp. 3: Rain Bird |
| --- | --- | --- | --- | --- |
| Overview | Ecosistema de riego de precisión autónomo con procesamiento Edge AI y transmisión LoRaWAN para zonas rurales. | Gigante global que ofrece proyectos "llave en mano" y su plataforma digital GrowSphere para riego y fertirrigación de alta precisión. | Integradora peruana de IoT que utiliza sensores, gateways LoRaWAN y centraliza el control en plataformas cloud (AWS). | Fabricante global de aspersores, válvulas y controladores de riego comerciales que operan mediante Wi-Fi y apps móviles. |
| Ventaja competitiva | ¿Qué valor ofrece a los clientes? Decisiones de riego autónomas sin depender de internet (Edge Computing) en parcelas alejadas. | Soporte agronómico global, altísima precisión y soluciones probadas en miles de hectáreas. | Soporte técnico local (Lima/Perú) y uso de tecnología de largo alcance (LoRaWAN) para la transmisión de datos. | Marca muy confiable, productos fáciles de comprar en ferreterías o distribuidores locales, tecnología muy probada mecánicamente. |
| Perfil de Marketing - Mercado objetivo | Pequeños agricultores (Piura), Juntas de Usuarios y entidades del Estado (Agrobanco/Agroideas). | Grandes agroexportadoras (ej. en Olmos y Piura) y fundos de alto valor. | Medianas empresas agrícolas e industrias peruanas que buscan automatización. | Huertos urbanos, jardinería residencial, parques públicos y pequeña agricultura. |
| Perfil de Marketing - Estrategias de marketing | Alianzas B2B/B2G con Juntas de Riego; demostraciones piloto de ROI en campo. | Venta corporativa B2B, líneas de crédito propias (ej. USD 20 millones para agroindustrias). | Marketing digital, desarrollo de proyectos integrales "a medida" en Perú. | Amplia red de distribuidores autorizados internacionales, venta B2C y B2B. |
| Perfil de Producto - Productos & Servicios | Nodos sensores Edge (TinyML), App móvil, Dashboard Web administrativo para Juntas, red LoRaWAN. | Mangueras de goteo, válvulas, software GrowSphere, servicios técnicos y capacitación. | Sensores de suelo, gateways LoRaWAN, sistema SCADA y plataforma en la nube (AWS). | Controladores Wi-Fi locales, aspersores, válvulas, temporizadores. |
| Perfil de Producto - Precios & Costos | Costo medio-bajo, accesible mediante cofinanciamiento del Estado. | Costos muy elevados por suscripciones de software y hardware de alta gama. | Costo medio, requiere inversión en gateways y suscripciones cloud. | Costo medio-bajo en hardware (S/ 600 - 1,200 por controlador), pero alto costo en consumo de agua si no se calibra bien. |
| Perfil de Producto - Canales de distribución | Venta institucional (B2B/B2G) y portal web. | Venta directa corporativa y distribuidores exclusivos. | Venta directa mediante consultoría técnica en Perú. | Distribuidores de equipos de riego, grandes almacenes. |
| Análisis SWOT - Fortalezas | Funciona 100% offline (Edge), no colapsa si cae el internet. | Músculo financiero enorme, investigación agronómica líder. | Desarrollo de hardware local (PCB a medida), uso de LoRaWAN. | Fácil adopción, equipos de larga durabilidad. |
| Análisis SWOT - Debilidades | Marca nueva, requiere esfuerzo para generar confianza en el agricultor. | Soluciones inalcanzables para el pequeño agricultor de subsistencia. | Depende de la nube (AWS) para tomar decisiones; si se cae la señal celular del Gateway, el riego no se automatiza bien. | Los equipos Wi-Fi son inútiles en el campo rural sin señal de internet. |
| Análisis SWOT - Oportunidades | El déficit del reservorio Poechos obliga a los pequeños agricultores a tecnificarse urgentemente. | Alianzas globales (ej. Bayer, IFC) para expandir sus créditos agrícolas. | Crecimiento de la agricultura inteligente en valles costeros peruanos. | Integración de sus controladores de casa con asistentes inteligentes. |
| Análisis SWOT - Amenazas | Resistencia cultural de los agricultores mayores frente al software. | Surgimiento de startups ágiles y económicas de AgTech. | Competencia de startups que no cobran licencias cloud costosas. | Marcas más baratas o sistemas IoT más avanzados que dejan obsoletos a los temporizadores simples. |

### 2.1.2. Estrategias y tácticas frente a competidores.

- **Frente a Netafim (La corporación global):** Nuestra táctica será la accesibilidad tecnológica. Netafim apunta a las grandes agroexportadoras con alto poder adquisitivo. Nosotros atacaremos el nicho desatendido: la agricultura familiar de Piura, ofreciendo una tecnología TinyML y Edge AI de bajo costo que puede ser cofinanciada por programas del Estado (Agroideas), logrando resultados de precisión corporativa pero con presupuestos acordes a la realidad rural.
- **Frente a Smelpro (El competidor IoT local dependiente de la Nube):** Aplicaremos la táctica de resiliencia de infraestructura (Edge Computing). Aunque Smelpro usa LoRaWAN, su "cerebro" está en la nube (AWS). Si el gateway en el campo pierde la señal de internet para comunicarse con AWS, el sistema pierde autonomía. Nuestra startup gana al procesar las decisiones localmente en el microcontrolador (Edge), asegurando que el cultivo se riegue en el momento exacto incluso ante un corte total de telecomunicaciones.
- **Frente a Rain Bird (La solución de hardware Wi-Fi off-the-shelf):** Nuestra ventaja será el alcance y la descentralización. Los controladores comerciales Wi-Fi de Rain Bird son excelentes para casas o zonas periurbanas, pero son inoperativos en parcelas dispersas rurales sin routers de internet. Reemplazaremos la dependencia del Wi-Fi con una red LoRaWAN de varios kilómetros de alcance, permitiendo controlar cientos de hectáreas desde un solo punto sin requerir internet tradicional.

## 2.2. Entrevistas.

### 2.2.1. Diseño de entrevistas.

Para llevar a cabo la recolección de información que sustentará nuestro proceso de *Needfinding*, hemos diseñado dos guías de entrevistas semiestructuradas, dirigidas específicamente a nuestros dos segmentos objetivo. Las preguntas han sido formuladas aplicando buenas prácticas de investigación cualitativa, con el fin de extraer datos reales sobre datos demográficos, comportamiento tecnológico, objetivos, frustraciones y rutinas diarias.

---

**A. Guía de Entrevista para el Segmento 1: Pequeños y Medianos Agricultores (Usuario Final)**

**Objetivo de la entrevista:** Comprender el impacto de la crisis hídrica (reservorio Poechos) en su día a día, identificar sus métodos de riego actuales, sus frustraciones ante la falta de conectividad en el campo y su nivel de adopción tecnológica para perfilar su User Persona.

**Bloque 1: Perfil Demográfico y Background**

1. ¿Podría indicarme su nombre completo, edad y en qué distrito o comunidad de Piura se ubica su parcela?
2. ¿Quiénes conforman su núcleo familiar y cuántos dependen de la actividad agrícola?
3. ¿Cuántas hectáreas cultiva actualmente y cuáles son sus principales cultivos?
4. Cuénteme un poco de su historia, ¿cuánto tiempo lleva dedicándose a la agricultura y cómo aprendió el oficio?

**Bloque 2: Comportamiento Tecnológico, Marcas y Canales de Interacción**

5. ¿Qué tipo de teléfono celular utiliza (básico o smartphone) y qué aplicaciones usa con más frecuencia en su día a día (ej. WhatsApp, Facebook, radio local)? 
6. Cuando está en su parcela, ¿cómo es la señal de internet o datos móviles? ¿Suele perder la conexión? 
7. ¿Qué marcas de herramientas, insumos agrícolas o tecnología reconoce como confiables en su trabajo diario? 
8. ¿Cómo suele informarse sobre el clima o los avisos de la Junta de Usuarios (radio, boca a boca, WhatsApp)?

**Bloque 3: Tareas, Objetivos y Frustraciones (Pain Points & Goals)**

9. Actualmente, con la reducción de agua del reservorio Poechos, ¿cómo está haciendo para regar sus cultivos? ¿Qué método utiliza (inundación, gravedad, goteo)? 
10. ¿Cómo decide exactamente cuándo y cuánta agua necesita su cultivo? ¿Se basa en la intuición, la experiencia o alguna herramienta? 
11. ¿Cuál es su mayor miedo o frustración cuando piensa en la actual campaña agrícola frente a la sequía? 
12. ¿Alguna vez ha intentado usar sistemas automáticos o tecnología para regar? Si falló o no lo hizo, ¿cuál fue el motivo (costo, complejidad, falta de luz/internet)?

**Bloque 4: Validación de la Solución (Edge Computing y LoRaWAN)** 

13. Si existiera un sistema económico que le avise a su celular que su tierra está seca, pero que además decida por sí solo abrir el agua para salvar su planta incluso cuando usted no tiene internet en el campo, ¿le daría confianza usarlo? ¿Por qué? 
14. Para usted, ¿cuál sería el objetivo principal o el mayor beneficio de usar una tecnología así en su parcela?

---

**B. Guía de Entrevista para el Segmento 2: Juntas de Usuarios e Instituciones (Cliente B2B/B2G)**

**Objetivo de la entrevista:** Identificar cómo auditan el uso del agua y los créditos agrícolas, conocer sus herramientas de gestión actuales y validar si un Dashboard centralizado con tecnología de largo alcance resolvería sus problemas de fiscalización y riesgo crediticio.

**Bloque 1: Perfil Profesional y Background**

1. ¿Cuál es su nombre, qué cargo ocupa y en qué institución labora (Junta de Usuarios / Agrobanco / Agroideas)?
2. ¿Cuáles son sus principales responsabilidades o tareas diarias respecto a la gestión del agua o el financiamiento agrícola?
3. ¿Cuál es su formación profesional y cuántos años de experiencia tiene en el sector agrario?

**Bloque 2: Comportamiento Tecnológico y Herramientas**

4. Para realizar su trabajo de monitoreo o gestión, ¿qué dispositivos y software utiliza regularmente (PC, laptops, tablets, Excel, sistemas internos del Estado)?
5. ¿Tienen actualmente algún software o herramienta digital que les permita saber en tiempo real cuánta agua usa cada agricultor en su parcela?

**Bloque 3: Tareas, Objetivos y Frustraciones (Pain Points & Goals)**

6. Ante la grave crisis hídrica en Piura, ¿cuál es el mayor obstáculo que enfrentan como institución para asegurar que los agricultores no desperdicien la cuota de agua asignada?
7. (Para bancos/Agroideas): ¿Cómo afecta la sequía y el mal uso del agua al riesgo de que los agricultores no puedan pagar sus créditos o fracasen en sus planes de negocio?
8. ¿Qué tan costoso, lento o frustrante es enviar supervisores físicamente al campo para auditar los cultivos o las redes de riego?

**Bloque 4: Validación de la Solución (Dashboard Remoto / Ecosistema IoT)**

9. Si contaran con una plataforma web (Dashboard) que les mostrara un mapa en tiempo real indicando qué parcelas mantienen niveles óptimos de humedad y cuáles desperdician agua (transmitido desde zonas sin internet), ¿cómo cambiaría esto su forma de trabajar? 
10. ¿Cree que su institución estaría dispuesta a financiar o subsidiar este tipo de tecnología para los pequeños agricultores organizados? ¿Qué requisitos pedirían?

### 2.2.2. Registro de entrevistas.

### 2.2.3. Análisis de entrevistas.

## 2.3. Needfinding.

### 2.3.1. User Personas.

### 2.3.2. User Task Matrix.

### 2.3.3. User Journey Mapping.

### 2.3.4. Empathy Mapping.

## 2.4. Big Picture EventStorming.

## 2.5. Ubiquitous Language.
