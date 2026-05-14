# Capítulo VI: Product Implementation, Validation & Deployment

## 6.1. Software Configuration Management.

### 6.1.1. Software Development Environment Configuration.

Project Management:
![WhatsApp](https://img.shields.io/badge/WhatsApp-25D366?logo=whatsapp&logoColor=white) WhatsApp: Se utilizo como canal de comunicacion para coordinar reuniones, compartir avances y resolver bloqueos rapidos.

![Trello](https://img.shields.io/badge/Trello-0052CC?logo=trello&logoColor=white) Trello: Se uso con enfoque Kanban para organizar tareas por etapas y dar seguimiento al progreso del equipo.

Requirements and Documentation:
![Lucidchart](https://img.shields.io/badge/Lucidchart-FF6F00?logo=lucidchart&logoColor=white) Lucidchart: Se utilizo para elaborar diagramas del sistema y apoyar la documentacion tecnica.

![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=white) GitHub: Plataforma central para versionado, control de cambios y documentacion del proyecto mediante README.

Product UX/UI Design:
![Figma](https://img.shields.io/badge/Figma-F24E1E?logo=figma&logoColor=white) Figma: Se empleo para la creacion de wireframes, mock-ups y prototipos de la landing page y aplicaciones.

![Canva](https://img.shields.io/badge/Canva-00C4CC?logo=canva&logoColor=white) Canva: Se utilizo para recursos graficos de apoyo en presentaciones y material visual.

Software Development:
![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?logo=visualstudiocode&logoColor=white) IDE: Visual Studio Code se uso como entorno principal por su soporte para desarrollo web y extensiones.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black) Frontend Web: HTML5, CSS y JavaScript para la landing page y prototipos web.

![Angular](https://img.shields.io/badge/Angular-DD0031?logo=angular&logoColor=white) Web App: Angular para el dashboard institucional.

![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?logo=kotlin&logoColor=white) ![Swift](https://img.shields.io/badge/Swift-F05138?logo=swift&logoColor=white) Mobile App: Kotlin/Swift para la aplicacion del agricultor (segun plataforma).

![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?logo=springboot&logoColor=white) Backend Cloud: Spring Boot (Java) para la API Gateway.

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white) ![SQLite](https://img.shields.io/badge/SQLite-003B57?logo=sqlite&logoColor=white) Databases: PostgreSQL (cloud) y SQLite (edge) para persistencia.

### 6.1.2. Source Code Management.

Para garantizar la eficiencia y evitar conflictos en el desarrollo de AquaEdge, los proyectos se gestionaron en una organizacion de GitHub. Dentro de esta organizacion se alojan los repositorios correspondientes a cada componente. A continuacion se listan los enlaces (pendientes de completar):

Report: [https://github.com/Grupo2IOT/report](https://github.com/Grupo2IOT/report)
Landing page: [https://github.com/Grupo2IOT/landing-page](https://github.com/Grupo2IOT/landing-page)
Web: [https://github.com/Grupo2IOT/appweb](https://github.com/Grupo2IOT/appweb)

En cuanto al manejo de Gitflow, se utilizo un esquema con ramas principales `main` y `develop` para versiones estables y de integracion, respectivamente. Cada integrante trabajo en su propia rama de feature, y los cambios se integraron mediante pull requests. Los commits siguieron el formato de Conventional Commits, lo que facilito la trazabilidad de cambios y el seguimiento del avance del proyecto.

### 6.1.3. Source Code Style Guide & Conventions.

Nuestro equipo adopto convenciones para asegurar codigo coherente, legible y mantenible en las tecnologias usadas:

HTML:

- Etiquetas y atributos en minusculas.
- Cierre explicito de elementos y uso de atributos `alt` en imagenes.
- Lineas cortas y estructura semantica (header, main, section, footer).

CSS:

- Nombres de clases en kebab-case y descriptivos.
- Un espacio despues de los dos puntos y punto y coma al final.
- Agrupacion de reglas relacionadas y separacion por bloques.

JavaScript/TypeScript (React):

- Preferencia por `const` y `let` sobre `var`.
- Componentes con archivos separados (template, style, logic).
- Nombres en camelCase y PascalCase segun tipo (variables vs clases).


### 6.1.4. Software Deployment Configuration.

El despliegue de AquaEdge se realizo con Vercel para el frontend y Supabase para el backend y base de datos, priorizando simplicidad, velocidad de despliegue y escalabilidad. Los pasos principales fueron:

1. Crear el proyecto en Vercel y vincular el repositorio del frontend (landing y/o web).
2. Definir variables de entorno en Vercel (URL y claves publicas necesarias).
3. Configurar el comando de build y el directorio de salida segun el framework.
4. Desplegar automaticamente por cada push a la rama principal.
5. Crear el proyecto en Supabase y habilitar la base de datos PostgreSQL.
6. Configurar tablas, relaciones y politicas de seguridad (RLS) segun roles.
7. Generar claves y configurar el cliente SDK en el frontend.
8. Verificar endpoints, reglas de acceso y pruebas de autenticacion.
9. Activar HTTPS por defecto y revisar limites de uso.
10. Monitorear logs y rendimiento desde los paneles de Vercel y Supabase.

## 6.2. Landing Page, Services & Applications Implementation.

### 6.2.X. Sprint n

#### 6.2.X.1. Sprint Planning n.

#### 6.2.X.2. Aspect Leaders and Collaborators.

#### 6.2.X.3. Sprint Backlog n.

#### 6.2.X.4. Development Evidence for Sprint Review.

#### 6.2.X.5. Testing Suite Evidence for Sprint Review.

#### 6.2.X.6. Execution Evidence for Sprint Review.

#### 6.2.X.7. Services Documentation Evidence for Sprint Review.

#### 6.2.X.8. Software Deployment Evidence for Sprint Review.

#### 6.2.X.9. Team Collaboration Insights during Sprint.

## 6.3. Validation Interviews.

### 6.3.1. Diseño de Entrevistas.

### 6.3.2. Registro de Entrevistas.

### 6.3.3. Evaluaciones según heurísticas.

## 6.4. Video About-the-Product.
