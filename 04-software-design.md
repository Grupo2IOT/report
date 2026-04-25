
# Capítulo IV: Solution Software Design

## 4.1. Strategic-Level Domain-Driven Design.

### 4.1.1. Design-Level EventStorming.

Con el propósito de lograr una comprensión profunda del dominio del sistema, se realizó una sesión de Event Storming con una duración aproximada de una hora. Esta actividad permitió al equipo estructurar y analizar sus ideas desde distintas perspectivas, incluyendo el enfoque de negocio, el usuario final, la administración y la experiencia general del sistema.

A través de esta dinámica, se identificaron elementos clave como eventos, comandos, actores y agregados, lo que facilitó la construcción de una primera visión integral del sistema. Durante la sesión, se abordaron los siguientes aspectos:

**Exploración del dominio general**
El análisis inició desde la interacción del usuario con la plataforma, considerando su recorrido desde el acceso inicial hasta las principales funcionalidades del sistema, incluyendo los procesos de registro, autenticación y uso de los servicios disponibles.

**Identificación de eventos y comandos clave**
Se emplearon notas adhesivas para representar los eventos (en color naranja) y los comandos (en color azul), tomando como base las User Stories previamente definidas, lo que permitió mantener coherencia en el flujo de la solución.

**Asignación de roles y responsables**
Se identificaron y diferenciaron los distintos actores del sistema, con el fin de delimitar sus responsabilidades e interacciones. Esta segmentación facilitó la detección de posibles mejoras y puntos críticos dentro del sistema.

**Evidencia de la sesión**
Finalmente, se recopiló evidencia del trabajo realizado durante la sesión como respaldo del proceso de análisis y modelado del dominio.

<p align="center">
	<img src="assets/EventStorming.png" alt="Event atorming evidence" width="920" />
</p>

#### 4.1.1.1 Candidate Context Discovery.

La identificación de contextos candidatos constituye una etapa fundamental para gestionar la complejidad en el desarrollo de sistemas. Este proceso implica un análisis detallado orientado a reconocer los elementos principales del dominio y sus relaciones. A partir de ello, dichos elementos se organizan en contextos delimitados que mantienen coherencia lógica. Esta estructuración no solo simplifica el diseño y la implementación, sino que también contribuye a mejorar la escalabilidad, el rendimiento y la mantenibilidad del sistema.

<p align="center">
	<img src="assets/evidencia_EventStorming.png" alt="Event Stormind" width="920" />
</p>

#### 4.1.1.2 Domain Message Flows Modeling.

El Modelado de Flujos de Mensajes de Dominio es una técnica empleada para analizar y diseñar sistemas de software, la cual permite representar el intercambio de información entre los distintos componentes mediante mensajes. Este enfoque se centra en definir los mensajes que los actores del sistema envían y reciben, así como en comprender las relaciones entre ellos. Su aplicación facilita la visualización de los flujos de información, lo que contribuye a identificar posibles problemas y a mejorar la estructura del diseño. A continuación, se presentan algunos diagramas ilustrativos aplicados al sistema propuesto.

<p align="center">
	<img src="assets/Strategic Domain-Driven Design.jpg" alt="Event Stormind" width="920" />
</p>

#### 4.1.1.3 Bounded Context Canvases.

### 4.1.2. Context Mapping.

### 4.1.3. Software Architecture.

#### 4.1.3.1. Software Architecture System Landscape Diagram.

#### 4.1.3.2. Software Architecture Context Level Diagrams.

#### 4.1.3.3. Software Architecture Container Level Diagrams.

#### 4.1.3.4. Software Architecture Deployment Diagrams.

## 4.2. Tactical-Level Domain-Driven Design

### 4.2.X. Bounded Context: <Bounded Context Name>

#### 4.2.X.1. Domain Layer.

#### 4.2.X.2. Interface Layer.

#### 4.2.X.3. Application Layer.

#### 4.2.X.4. Infrastructure Layer.

#### 4.2.X.5. Bounded Context Software Architecture Component Level Diagrams.

#### 4.2.X.6. Bounded Context Software Architecture Code Level Diagrams.

##### 4.2.X.6.1. Bounded Context Domain Layer Class Diagrams.

##### 4.2.X.6.2. Bounded Context Database Design Diagram.
