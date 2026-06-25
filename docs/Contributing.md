# Contributing

## Introducción

Este documento describe el flujo de trabajo que debe seguir cualquier integrante del equipo al realizar cambios en el proyecto.

El objetivo es mantener un proceso ordenado, reducir conflictos y asegurar que todos los cambios puedan ser revisados antes de integrarse a la rama principal.

---

## Flujo General de Trabajo

Antes de comenzar una nueva tarea:

1. Actualizar la copia local del proyecto.
2. Crear una nueva rama de trabajo.
3. Realizar los cambios necesarios.
4. Crear commits claros y descriptivos.
5. Subir la rama al repositorio remoto.
6. Abrir un Pull Request.
7. Solicitar revisión.
8. Integrar los cambios a `main` una vez aprobados.

---

## Clonar el Repositorio

Si es la primera vez trabajando en el proyecto:

```bash
git clone <rhttps://github.com/JulianForeroBernal/ProyectoVacaciones.git>
cd CundiReferencias
```

---

## Mantener el Repositorio Actualizado

Antes de iniciar una nueva tarea:

```bash
git checkout main
git pull origin main
```

Esto garantiza que la rama principal local esté actualizada.

---

## Crear una Rama

Ningún cambio debe realizarse directamente sobre `main`.

Crear una nueva rama para cada tarea:

```bash
git checkout -b feature/task-name
```

Ejemplos:

```bash
git checkout -b feature/login
git checkout -b feature/review-system
git checkout -b feature/search-filters
```

Para correcciones:

```bash
git checkout -b fix/login-validation
```

Para documentación:

```bash
git checkout -b docs/update-readme
```

---

## Realizar Cambios

Trabajar únicamente sobre la rama creada para la tarea.

Se recomienda realizar commits pequeños y frecuentes.

---

## Crear Commits

Formato:

```text
type: short description
```

Tipos permitidos:

```text
feat
fix
docs
refactor
test
style
chore
```

Ejemplos:

```bash
git commit -m "feat: add user registration"

git commit -m "fix: validate login credentials"

git commit -m "docs: update project scope"
```

Evitar mensajes como:

```text
Cambios

Update

Correcciones

asdf
```

---

## Subir la Rama

Una vez realizados los cambios:

```bash
git push origin branch-name
```

Ejemplo:

```bash
git push origin feature/login
```

---

## Crear un Pull Request

Después de subir la rama:

1. Abrir GitHub.
2. Crear un Pull Request hacia `main`.
3. Escribir una descripción breve de los cambios realizados.
4. Solicitar revisión a otro integrante del equipo.

---

## Revisión de Código

Antes de aprobar un Pull Request se recomienda verificar:

* El código compila correctamente.
* La funcionalidad cumple el objetivo esperado.
* No existen errores evidentes.
* Se respetan las convenciones del proyecto.

Las revisiones deben realizarse con respeto y con intención de aprendizaje.

---

## Resolución de Conflictos

Si Git informa conflictos:

1. No realizar merge forzado.
2. Identificar los archivos afectados.
3. Resolver los conflictos manualmente.
4. Probar el funcionamiento del proyecto.
5. Crear un nuevo commit con la resolución.

En caso de duda, solicitar ayuda al equipo antes de continuar.

---

## Buenas Prácticas

* Mantener ramas pequeñas y enfocadas.
* Realizar commits frecuentes.
* Escribir mensajes claros.
* No trabajar directamente sobre `main`.
* Comunicar tareas importantes antes de comenzar.
* Mantener una copia local actualizada.
* Revisar el código antes de solicitar un Pull Request.

---

## Objetivo

El propósito de este flujo de trabajo es garantizar que todos los integrantes comprendan el proceso completo de desarrollo colaborativo utilizando Git y GitHub, manteniendo un proyecto organizado y fácil de mantener.
