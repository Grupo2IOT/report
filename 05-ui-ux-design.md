# Capítulo V: Solution UI/UX Design

## 5.1. Style Guidelines.

### 5.1.1. General Style Guidelines.

La experiencia visual de AquaEdge prioriza claridad, confianza y lectura rapida en campo, por lo que se adopta un estilo sobrio y funcional: tipografia sans-serif legible, jerarquia clara (titulos, subtitulos y datos clave), alto contraste para visibilidad en exteriores, espaciado generoso para reducir errores en toques, y uso consistente de iconos simples para estados de humedad, riego y alertas. El color comunica estado (normal, advertencia, critico) y evita saturaciones, mientras que las metricas esenciales se muestran primero con etiquetas cortas y unidades visibles. Todo el contenido mantiene lenguaje directo y tecnico accesible para agricultores e instituciones, asegurando coherencia entre web, mobile e interfaces IoT incluso en contextos de baja conectividad.

<p align="center">
	<img src="assets/gnrlsg.png" alt="style guideline" width="500" />
</p>

### 5.1.2. Web, Mobile and IoT Style Guidelines.

En web, el dashboard prioriza paneles densos pero ordenados para analistas, con tablas filtrables, graficas comparativas y estados por parcela, usando layout de 12 columnas y navegacion lateral persistente. En mobile, la interfaz se reduce a tareas criticas del agricultor: alertas, estado de riego y acciones rapidas, con botones grandes, modo una mano y tarjetas resumidas para conexion intermitente. En IoT (pantallas o indicadores del nodo), se emplean señales minimas y robustas: colores de estado, iconos simples, textos cortos y feedback inmediato de encendido/valvula, evitando animaciones o detalles que consuman energia. Las tres plataformas comparten nomenclatura, iconografia y codigos de estado para que el usuario reconozca el mismo significado sin importar el dispositivo.

<p align="center">
	<img src="assets/websg.png" alt="style guideline" width="500" />
</p>

<p align="center">
	<img src="assets/mobsg.png" alt="style guideline" width="500" />
</p>

<p align="center">
	<img src="assets/iotsg.png" alt="style guideline" width="500" />
</p>

## 5.2. Information Architecture.

### 5.2.1. Organization Systems.

### 5.2.2. Labeling Systems.

Antes de implementar las etiquetas en AquaEdge, definimos los requisitos de claridad, accionabilidad y coherencia entre web, mobile e IoT. Las etiquetas agregan contexto inmediato sobre el estado del riego, la humedad y la operacion del sistema. A continuacion se detalla el sistema de etiquetado implementado:

Etiquetas para parcelas
Etiqueta | Descripcion
[ESTABLE] | Humedad dentro del rango objetivo
[ALERTA] | Humedad cerca del limite, requiere atencion
[CRITICO] | Estres hidrico detectado, riego prioritario

Etiquetas para riego
Etiqueta | Descripcion
[AUTOMATICO] | Riego gestionado por Edge API
[MANUAL] | Riego activado por el usuario
[PAUSADO] | Riego deshabilitado temporalmente

Etiquetas para sensores
Etiqueta | Descripcion
[ONLINE] | Sensor reportando lecturas recientes
[OFFLINE] | Sensor sin comunicacion o bateria baja

Etiquetas para notificaciones del sistema
Etiqueta | Descripcion
[CONFIRMADO] | Operacion completada exitosamente
[ERROR] | Problema durante la operacion

Este sistema de etiquetas brinda contexto visual inmediato y mejora la comprension de la informacion tanto para agricultores como para analistas institucionales.

### 5.2.3. SEO Tags and Meta Tags

La implementacion de etiquetas SEO en AquaEdge busca mejorar la visibilidad de la landing page y presentar informacion clara en buscadores y redes sociales. A continuacion se detallan las etiquetas principales y un ejemplo de uso:

Titulo (55-60 caracteres, descriptivo)

```
<title>AquaEdge - Riego inteligente IoT para agricultura</title>
```

Descripcion (propuesta de valor breve)

```
<meta
  name="description"
  content="AquaEdge optimiza el riego agricola con IoT, Edge Computing y alertas en tiempo real para ahorrar agua en zonas rurales."
/>
```

Robots (indexacion y seguimiento)

```
<meta name="robots" content="index, follow" />
```

Tipo de contenido e idioma

```
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
<meta http-equiv="Content-Language" content="es" />
```

Viewport (adaptacion mobile)

```
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

Open Graph (compartir en redes sociales)

```
<meta property="og:title" content="AquaEdge - Riego inteligente para el agro" />
<meta
  property="og:description"
  content="Sistema IoT y Edge Computing para monitorear humedad y automatizar el riego."
/>
<meta
  property="og:image"
  content="https://aquaedge.pe/images/aquaedge-preview.jpg"
/>
<meta property="og:url" content="https://aquaedge.pe" />
<meta property="og:type" content="website" />
```

Keywords (apoyo semantico)

```
<meta
  name="keywords"
  content="riego inteligente, IoT agricola, edge computing, monitoreo humedad, ahorro de agua, agricultura"
/>
```

### 5.2.4. Searching Systems.

El sistema de busqueda de AquaEdge permite encontrar informacion critica por parcela, sensores y eventos de riego, ayudando tanto al agricultor como al analista institucional. Se plantean dos niveles de busqueda:

Sistema de busqueda para agricultores (mobile)
Nombre del filtro | Descripcion
Parcela | Filtra por nombre o codigo de parcela
Estado de humedad | Muestra solo parcelas en [ESTABLE], [ALERTA] o [CRITICO]
Riego | Filtra por [AUTOMATICO], [MANUAL] o [PAUSADO]
Ultima lectura | Ordena por lecturas mas recientes
Alertas activas | Muestra solo parcelas con alertas vigentes

Sistema de busqueda para analistas (web)
Nombre del filtro | Descripcion
Ubicacion | Filtra por distrito o zona agricola
Consumo de agua | Filtra por rangos de consumo historico
Rango de fechas | Busca eventos de riego por periodo
Estado de sensores | Filtra por [ONLINE] o [OFFLINE]
Riesgo hidrico | Prioriza parcelas con estres hidrico

Caracteristicas adicionales del sistema de busqueda

- Actualizacion casi en tiempo real: resultados refrescados por sincronizacion LoRaWAN.
- Historial de busquedas: guarda los ultimos filtros aplicados para acceso rapido.
- Busqueda tolerante: acepta variaciones de nombres y codigos de parcela.

Este sistema de busqueda mejora la localizacion de informacion clave y acelera la toma de decisiones operativas y financieras.

### 5.2.5. Navigation Systems.

El sistema de navegacion de AquaEdge guia a agricultores y analistas a traves de funciones criticas con rutas claras y consistentes. Se definen los siguientes elementos:

Navegacion global
Nombre | Descripcion
Inicio | Resumen de estado general segun rol
Parcelas | Acceso a listado y detalle por parcela
Alertas | Bandeja de eventos criticos y notificaciones
Perfil | Configuracion personal y preferencias

Navegacion para agricultores (mobile)
Nombre | Descripcion
Estado de riego | Vista rapida de humedad y valvulas
Mis alertas | Alertas activas y acciones inmediatas
Historial | Eventos de riego recientes
Soporte | Guia basica y contacto tecnico

Navegacion para analistas (web)
Nombre | Descripcion
Dashboard | Indicadores clave y comparativas por zona
Auditoria | Consumo, cumplimiento y reportes
Sensores | Estado de dispositivos y fallas
Usuarios | Gestion de cuentas y roles

Elementos y patrones de navegacion

- Menu lateral persistente en web para acceso rapido a modulos.
- Barra inferior en mobile con 3-4 accesos principales.
- Navegacion jerarquica: zona -> parcela -> sensor -> evento.
- Pestañas por categoria en vistas densas (riego, alertas, consumo).
- Acciones rapidas con botones flotantes en mobile para iniciar o pausar riego.

Este sistema asegura una navegacion consistente, intuitiva y adaptada a cada dispositivo, reduciendo el tiempo de acceso a informacion critica.

## 5.3. Landing Page UI Design.

### 5.3.1. Landing Page Wireframe.

En esta seccion se representa una estructura funcional preliminar de la landing page de AquaEdge, organizada por bloques clave (hero con propuesta de valor, beneficios, solucion IoT, casos de uso, testimonios/alianzas y llamado a la accion). El wireframe define la jerarquia informativa y el flujo de navegacion del visitante, priorizando la comprension rapida del problema y la solucion. Esta etapa se centra en la logica y disposicion del contenido, sin aplicar aun colores, imagenes ni estilos graficos.

<p align="center">
	<img src="assets/lndwf1.png" alt="wireframe" width="500" />
</p>

<p align="center">
	<img src="assets/lndwf2.png" alt="wireframe" width="500" />
</p>

<p align="center">
	<img src="assets/lndwf3.png" alt="wireframe" width="500" />
</p>

### 5.3.2. Landing Page Mock-up.

El mock-up de la landing page de AquaEdge presenta una version visual refinada y cercana al resultado final. Siguiendo los General Style Guidelines, se mantiene una paleta sobria, tipografia clara y alto contraste para comunicar confianza y tecnologia aplicada al agro. El contenido resalta el valor principal de AquaEdge: optimizar el riego con IoT y Edge Computing en zonas de baja conectividad. Las secciones explican el problema hidrico, la solucion propuesta, beneficios para agricultores e instituciones, y el flujo de funcionamiento del sistema, incorporando llamados a la accion, evidencias de impacto y un formulario de contacto. El mock-up transmite una experiencia profesional, confiable y orientada a resultados en campo.

<p align="center">
	<img src="assets/lndmk1.png" alt="mock-up" width="500" />
</p>

<p align="center">
	<img src="assets/lndmk2.png" alt="mock-up" width="500" />
</p>

<p align="center">
	<img src="assets/lndmk3.png" alt="mock-up" width="500" />
</p>

<p align="center">
	<img src="assets/lndmk4.png" alt="mock-up" width="500" />
</p>

<p align="center">
	<img src="assets/lndmk5.png" alt="mock-up" width="500" />
</p>

## 5.4. Applications UX/UI Design.

### 5.4.1. Applications Wireframes.

Esta seccion presenta los wireframes de las aplicaciones web y movil de AquaEdge, disenadas para dos perfiles: agricultores (usuario final) y analistas institucionales (cliente B2B). Cada wireframe define la estructura, jerarquia y flujo de los elementos antes de aplicar estilo visual o contenido final. Los primeros wireframes son compartidos por ambos perfiles e incluyen inicio de sesion y registro, con formularios simples, acceso rapido y opciones de recuperacion de cuenta. Luego, para web se muestran vistas de dashboard, auditoria de consumo, estado de sensores y reportes; mientras que en mobile se priorizan alertas, estado de riego, acciones rapidas y resumen por parcela. En todos los casos se busca una navegacion clara, con foco en datos criticos y minima friccion para tareas repetitivas.

<p align="center">
	<img src="assets/awebwf.png" alt="wireframe" width="500" />
</p>

<p align="center">
	<img src="assets/apwf1.png" alt="wireframe" width="200" />
</p>

<p align="center">
	<img src="assets/apwf2.png" alt="wireframe" width="200" />
</p>

<p align="center">
	<img src="assets/apwf3.png" alt="wireframe" width="200" />
</p>

<p align="center">
	<img src="assets/apwf4.png" alt="wireframe" width="200" />
</p>

<p align="center">
	<img src="assets/apwf5.png" alt="wireframe" width="200" />
</p>

### 5.4.2. Applications Wireflow Diagrams.

Los wireflows de AquaEdge ilustran el recorrido del usuario entre pantallas clave y decisiones de navegacion, combinando estructura y flujo de interaccion. Para mobile, se detalla el camino desde la recepcion de una alerta hasta la accion de riego (visualizar estado, confirmar, ejecutar y recibir feedback).

<p align="center">
	<img src="assets/apwfl.png" alt="wireframe" width="500" />
</p>

### 5.4.3. Applications Mock-ups.

Los mock-ups de las aplicaciones de AquaEdge muestran la version visual refinada de las vistas web y mobile, aplicando la paleta, tipografia y jerarquia definidas en las guias de estilo. En web, el dashboard presenta indicadores, comparativas y alertas con enfoque analitico, mientras que en mobile se resaltan estados de humedad, acciones rapidas y notificaciones criticas para el agricultor. Los elementos visuales comunican prioridad y riesgo mediante color y etiquetas, manteniendo consistencia con los estados del sistema.

<p align="center">
	<img src="assets/awebmk.png" alt="mock-up" width="500" />
</p>

<p align="center">
	<img src="assets/apmk1.png" alt="mock-up" width="200" />
</p>

<p align="center">
	<img src="assets/apmk2.png" alt="mock-up" width="200" />
</p>

<p align="center">
	<img src="assets/apmk3.png" alt="mock-up" width="200" />
</p>

<p align="center">
	<img src="assets/apmk4.png" alt="mock-up" width="200" />
</p>

<p align="center">
	<img src="assets/apmk5.png" alt="mock-up" width="200" />
</p>

<p align="center">
	<img src="assets/apmk6.png" alt="mock-up" width="200" />
</p>

<p align="center">
	<img src="assets/apmk7.png" alt="mock-up" width="200" />
</p>

<p align="center">
	<img src="assets/apmk8.png" alt="mock-up" width="200" />
</p>

<p align="center">
	<img src="assets/apmk9.png" alt="mock-up" width="200" />
</p>

### 5.4.4. Applications User Flow Diagrams.

Los diagramas de flujo de usuario de AquaEdge describen la interaccion desde una perspectiva logica, incluyendo decisiones condicionales y respuestas del sistema. En mobile, el flujo principal cubre: recepcion de alerta -> validacion de estado -> confirmacion de accion -> ejecucion de riego -> notificacion de resultado, con caminos alternativos ante fallas de sensor o conectividad.

<p align="center">
	<img src="assets/apufl1.png" alt="mock-up" width="500" />
</p>

<p align="center">
	<img src="assets/apufl2.png" alt="mock-up" width="500" />
</p>

## 5.5. Applications Prototyping.

## 5.6. IoT Device Design

Siguiendo las pautas de la metodología de diseño de soluciones IoT (Paso 9: Device & Component Design), en esta sección se detallan los elementos que componen la capa física **(Physical Layer)** de AquaEdge. El diseño se centra en la capacidad de procesamiento local y la eficiencia en la transmisión de datos hacia la capa de intercambio **(Data Exchange Layer)**.

### 5.6.1. Bill of Materials (BOM)

En concordancia con los componentes fundamentales de un sistema IoT (Microcontroladores y Sensores), se presenta la lista de materiales necesaria para el prototipo. Se ha seleccionado el ESP32 como nodo central debido a su capacidad de procesamiento superior frente a alternativas básicas de Arduino, permitiendo una futura implementación de lógica Edge.

| **Componente** | **Especificacion Tecnica** | **Funcion (Capa Fisica)** | **Cantidad** |
| --- | --- | --- | --- |
| **Microcontrolador** | ESP32-WROOM-32 (Dual Core) | Procesamiento de señales y gestion del ciclo de sueño. | 1 |
| **Modulo de Comunicacion** | Reyax RYLR998 (LoRa) | Interfaz de red para transmision a larga distancia. | 1 |
| **Sensor de Humedad** | Capacitivo Soil Moisture v1.2 | Captura de datos analogicos del sustrato. | 1 |
| **Sensor Nutrientes** | NPK RS485 Industrial | Captura de datos quimicos (N-P-K) via protocolo serial. | 1 |
| **Interfaz Serial** | Adaptador TTL a RS485 (MAX485) | Conversion de senal para compatibilidad con el MCU. | 1 |
| **Gestion Energetica** | Panel Solar 1W + Modulo TP4056 | Sistema de recoleccion y carga de energia. | 1 |
| **Almacenamiento Energia** | Bateria Li-ion 18650 (3.7V) | Fuente de poder para operacion autonoma. | 1 |
| **Proteccion** | Gabinete ABS con sello IP66 | Proteccion fisica contra condiciones ambientales. | 1 |

### 5.6.2. IoT Device Hardware Architecture

La arquitectura de hardware de AquaEdge se ha diseñado siguiendo el modelo de **Capa Física** descrito en la teoría de diseño de soluciones IoT básicas, integrando los siguientes sub-módulos:

1. **Módulo de Procesamiento:** El **ESP32** gestiona el flujo de información. Este componente es el encargado de ejecutar el "Procesamiento de datos en el borde" (Edge) antes de la transmisión, filtrando ruidos en las lecturas de los sensores.

2. **Módulo de Percepción (Inputs): * Lectura Analógica:** El sensor de humedad entrega una señal de voltaje proporcional a la humedad del suelo.

   - **Lectura Digital/Serial:** El sensor NPK utiliza una trama de datos RS485 que es decodificada por el ESP32 para obtener los valores específicos de nutrientes.

3. **Módulo de Comunicación (Output):** Utiliza el puerto UART del ESP32 para enviar los datos procesados al módulo LoRa, estableciendo el enlace hacia el Internet Gateway (Capa de Intercambio de Datos).

### 5.6.3. IoT Device Connectivity Architecture

Bajo el esquema de diseño de soluciones IoT, la conectividad se define por el alcance y el consumo energético:

- **Protocolo de Red:** Se utiliza **LoRa (Long Range)**, ideal para la topología de red en estrella donde los nodos sensores están dispersos en el campo.

- **Modo de Operación:** El dispositivo opera bajo un régimen de "Dispositivo Final" que envía datos periódicamente y entra en modo de bajo consumo (Low Power Mode) para maximizar la vida útil de la batería.

### 5.6.4. IoT Device Physical Design

El diseño físico (Prototipo) responde a los requisitos funcionales de operatividad en exteriores:

- **Protección Ambiental:** El uso de una carcasa **IP66** asegura que los componentes electrónicos (Capa Física) no se vean afectados por el polvo o el agua de riego.

- **Ergonomía de Instalación:** El dispositivo incluye pasacables estancos para que las sondas de los sensores (humedad y NPK) puedan enterrarse mientras el cerebro del dispositivo permanece protegido y elevado.
