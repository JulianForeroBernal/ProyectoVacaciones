# Team Rules

## 1. Proposito
Este documento define las normas de trabajo del equipo para garantizar una colaboración organizada, facilitar el aprendizaje conjunto y mantener la calidad del proyecto.

Todos los integrantes participarán en diferentes áreas del desarrollo con el objetivo de comprender el funcionamiento completo del sistema y fortalecer habilidades técnicas y de trabajo en equipo.

## 2. Filosofia de Equipo
El objetivo principal no es únicamente terminar el proyecto, sino aprender durante el proceso.
Por esta razón:
- Todos los integrantes podrán participar en frontend, backend, base de datos y documentación.
- Se priorizará el aprendizaje compartido sobre la especialización temprana.
- Las decisiones importantes se discutirán en equipo.
- Se fomentará la colaboración y el apoyo mutuo cuando algún integrante tenga dificultades técnicas.

## Idioma del proyecto

### Documentacion
La documentación oficial del proyecto se escribirá en español para facilitar la comprensión de todos los integrantes.

### Codigo
Todo el código deberá escribirse en inglés.

Ejemplos:

teacher_name
user_id
review_service

### Commits

Los mensajes de commit deberán escribirse en inglés siguiendo una convención común.

Ejemplos:

feat: add user registration

fix: validate review score

docs: update project scope

### Nombres Tecnicos

Los nombres de clases, funciones, variables, tablas y ramas deberán estar en inglés.

## 4. Comunicación

Las decisiones importantes deberán comunicarse al equipo antes de ser implementadas.

Cuando un integrante comience a trabajar en una tarea, deberá informarlo para evitar trabajo duplicado o conflictos innecesarios. Esto tambien se podra ver reflejado en el repositorio remoto en el paratado de Isusse (github) 

La comunicacion del equipo sera mediante whatsapp por el grupo ("Proyecto Vacaciones")

## 5. Gestion de tareas

Antes de comenzar una funcionalidad:

1. La tarea debe estar definida.
2. Debe existir un responsable principal.
3. El resto del equipo debe conocer que esa tarea está siendo desarrollada.

Mientras una persona esté trabajando activamente en una funcionalidad, los demás integrantes no deberán modificar la misma área sin coordinación previa.

## 6. Uso de Git y Github

### Rama principal (main)
La rama main deberá contener únicamente código estable y funcional.
No se realizarán cambios directamente sobre main.

### Ramas de trabajo 
Toda funcionalidad, corrección o mejora deberá desarrollarse en una rama independiente.
Ejemplos:

- feature/login
- feature/review-system
- feature/search-filters
- fix/login-validation
- docs/update-readme

### Actualizacion de Ramas
Antes de comenzar a trabajar se recomienda actualizar la rama local con los cambios más recientes del repositorio.

## 7. Convencion de Commits
Los commits deberán ser pequeños, claros y representar una única intención.
Formato:

- type: short description

Tipos permitidos:

- feat     -> Nueva funcionalidad
- fix      -> Corrección de errores
- docs     -> Documentación
- refactor -> Mejora interna sin cambiar comportamiento
- test     -> Pruebas
- style    -> Cambios de formato o estilo
- chore    -> Tareas de mantenimiento

Ejemplos:

- feat: add teacher search
- fix: validate login credentials
- docs: update team rules

## 8. Pull Request (PRs)
Todo cambio deberá integrarse mediante Pull Request.
Antes de aprobar un Pull Request se recomienda verificar:
- Que el código funcione correctamente.
- Que siga las convenciones acordadas.
- Que no introduzca errores evidentes.
- Que la funcionalidad cumpla con el objetivo definido.
Nadie hace merge de su propio PR este debe ser revisado al menos por una perosa distinta
El objetivo de la revisión es aprender y mejorar la calidad del proyecto, no criticar a los integrantes.

## 9. Calidad del codigo
Se buscará mantener:
- Código legible.
- Nombres descriptivos.
- Funciones pequeñas y con responsabilidades claras.
- Comentarios únicamente cuando aporten valor.
- Estructura consistente entre módulos.
Siempre que sea posible se intentará aplicar principios de Programación Orientada a Objetos y principios SOLID.

## 10. Resolucion de conflictos
Cuando exista desacuerdo sobre una decisión técnica:
1. Se escucharán las diferentes propuestas.
2. Se analizarán ventajas y desventajas.
3. Se tomará una decisión en equipo.
Una vez tomada la decisión, todos los integrantes la respetarán hasta que exista una razón justificada para revisarla nuevamente.

## 11. Objetivo final
Al finalizar el proyecto, todos los integrantes deberán ser capaces de:
- Comprender la arquitectura general del sistema.
- Utilizar Git y GitHub en un entorno colaborativo.
- Entender el flujo completo de desarrollo de una aplicación web.
- Participar en frontend, backend y base de datos.
- Mantener y extender el proyecto de manera independiente.
El éxito del proyecto se medirá tanto por el funcionamiento de la aplicación como por el aprendizaje obtenido durante su desarrollo.