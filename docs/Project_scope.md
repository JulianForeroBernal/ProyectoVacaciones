# Project Scope
En este archivo se detalla el alcance del proyecto, es decir, que se va a realizar y que no.

## Descripcion general
CundiReferencias es una plataforma web orientada a estudiantes universitarios que permite consultar y compartir referencias sobre profesores y materias. Su propósito es centralizar experiencias académicas de los estudiantes para facilitar la toma de decisiones al momento de inscribir asignaturas o seleccionar docentes.

La plataforma estará disponible para consulta pública, permitiendo que cualquier visitante pueda acceder a las referencias existentes. Sin embargo, únicamente los usuarios registrados podrán crear, editar o eliminar sus propias referencias.

## Objetivo del proyecto
El proyecto busca realizar un aplicativo web donde el usuario (estudiantes principalmente) pueda consultar referencias (opiciones - experincias - recomendaciones) de otros estudiantes hacia los profesores universitarios, y de la misma manera cada usuario tiena la posibilidad de dejar su propio comentario/referencias sobre algun profesor.
A su vez este Proyecto es una oportunidad para el equipo de desarrollo para fortalicer competencias de trabajo colaborativo, control de versiones, arquitectura de software, POO, principios SOLID, testing y desarrollo full stack.

## Alcance del MVP 
La primera version del MVP (Minimum Viable Product - Producto Minimo Viable) estara enfocada en proporcionar las funcionalidades esenciales necesarias para consultar y compartir referencias academicas.
el MVP buscara validar la idea principal del sistema antes de considerar funcionlidades adicionles.

## Funcionalidades incluidas

### Consulta de referencias 

- Visualizar referencias existentes
- Consultar informacion asociada a profesores (facultad, sede, materias)
- Consultar info asociada a materias (profesor - facultad - sede)
- Vizalizacion de contenido sin necesidad de registro y/o autenticacion.

### Gestion de usuarios
- Registro de usuiarios
- Login de usuarios
- Cierre de sesion

### Gestion de referencias
- Crear referencia asociada a un profesor
- Editar referencia propia
- Eliminar referencia propia

### Busqueda y filtros
- Buscar profesor por nombre
- Buscar materias
- Filtrar profesores por materia
- Filtrar profesores por sede 
- Filtrar profesores por facultad

## Funcionalidades fuera del alcance (NO se va a realizar)
las siguientes funcionalidades no forman parte del MVP, sin embargo pueden ser funcionalides adicioneles, incluidas mas adelante el la creacion del proyecto: 
- Recomendaciones de profesores mediante IA 
- Chats
- Notificaciones
- Rankings
- IA en general
- Aplicacion movil
- Integracion con pagina de la universidad
- Recuperacion de contraseña 
- validacion del correo electronico universitario
- Likes
- Respuesta a comentarios
- Subida de imagenes
- Perfiles publicos 

## Usuarios objetivo

### Visitantes
Culquier usuario de la pagina podra consultar referencias academicas sin neceidad de registrarse en la pagina.
### Estudiantes Registrados
Usuarios (Estudiantes) registrados(autenticados mas adelante) podran podran publicar, editar y eliminar sus propias referencias.

## Restricciones y suposiciones

### Restricciones
- El proyecto sera desarrollado con fines academicos y de aprendizaje
- El tiempo de desarrollo esta limitado al periodo definido por el equipo (vacaciones de junio y julio por ahora)
- El sistema sera desarrollado usando tecnologias selecionadas por el equipo

### Suposiciones
- Los usuarios prporcionaran informacion de manera respetuosa y responsable 
- Existira una lista inicial de profesores, materia, facultades y sedes para realizar pruebas del sistema
- la plataforma será utilizada principalmente desde navegadores web modernos

## Criterios de exito
Se conseiderara que el MVP habra sido completado de manera exitosa cuando:
- un visitante pueda comentar referencias sin autenticarese
- Un usuario pueda registrarse e iniciar sesion
- Un usuario registrado pueda crear una referencia
- Un usuario registrado pueda editar y eliminar sus propias referencias
- Los usuarios en general puedan buscar y filtrar informacion (las materias) mediante criterios definidos
- El sistema funcione correcetamente integrando frontend, backend y database. 