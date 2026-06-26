# Data Model

## 1. Objetivo

Este documento describe las entidades principales del sistema, sus atributos, relaciones y restricciones de negocio.

El modelo de datos podrá evolucionar durante el desarrollo del proyecto conforme aparezcan nuevos requisitos.

---

## 2. Entidades

### User

Representa un estudiante registrado en la plataforma.

#### Atributos

| Atributo            | Tipo       | Descripción                           |
| ------------------- | ---------- | ------------------------------------- |
| id                  | UUID / INT | Identificador único                   |
| display_name        | String     | Nombre visible del usuario            |
| institutional_email | String     | Correo institucional universitario    |
| password_hash       | String     | Contraseña almacenada de forma segura |

#### Relaciones

* Un usuario puede crear múltiples reviews.
* Una review pertenece a un único usuario.

---

### Teacher

Representa un profesor disponible en la plataforma.

#### Atributos

| Atributo | Tipo       | Descripción                  |
| -------- | ---------- | ---------------------------- |
| id       | UUID / INT | Identificador único          |
| name     | String     | Nombre completo del profesor |

#### Relaciones

* Un profesor puede tener múltiples reviews.
* Un profesor puede estar asociado a múltiples asignaciones académicas.

---

### Subject

Representa una materia académica.

#### Atributos

| Atributo | Tipo       | Descripción          |
| -------- | ---------- | -------------------- |
| id       | UUID / INT | Identificador único  |
| name     | String     | Nombre de la materia |

#### Relaciones

* Una materia puede estar asociada a múltiples asignaciones académicas.

---

### Campus

Representa una sede universitaria.

#### Atributos

| Atributo | Tipo       | Descripción         |
| -------- | ---------- | ------------------- |
| id       | UUID / INT | Identificador único |
| name     | String     | Nombre de la sede   |

#### Relaciones

* Una sede puede estar asociada a múltiples asignaciones académicas.

---

### TeachingAssignment

Representa la asignación de una materia a un profesor dentro de una sede específica.

#### Atributos

| Atributo   | Tipo       | Descripción         |
| ---------- | ---------- | ------------------- |
| id         | UUID / INT | Identificador único |
| teacher_id | FK         | Profesor asociado   |
| subject_id | FK         | Materia asociada    |
| campus_id  | FK         | Sede asociada       |

#### Relaciones

* Pertenece a un profesor.
* Pertenece a una materia.
* Pertenece a una sede.

#### Ejemplo

| Profesor   | Materia    | Sede      |
| ---------- | ---------- | --------- |
| Juan Pérez | Física I   | Zipaquirá |
| Juan Pérez | Física III | Chía      |

---

### Review

Representa una referencia o experiencia compartida por un estudiante sobre un profesor.

#### Atributos

| Atributo   | Tipo       | Descripción                  |
| ---------- | ---------- | ---------------------------- |
| id         | UUID / INT | Identificador único          |
| content    | Text       | Contenido de la referencia   |
| created_at | Datetime   | Fecha de creación            |
| updated_at | Datetime   | Fecha de última modificación |
| user_id    | FK         | Autor de la referencia       |
| teacher_id | FK         | Profesor referenciado        |

#### Relaciones

* Pertenece a un usuario.
* Pertenece a un profesor.

---

## 3. Relaciones del Modelo

### User → Review

```text
User 1 ---- N Review
```

Un usuario puede escribir múltiples referencias.

---

### Teacher → Review

```text
Teacher 1 ---- N Review
```

Un profesor puede recibir múltiples referencias.

---

### Teacher → TeachingAssignment

```text
Teacher 1 ---- N TeachingAssignment
```

Un profesor puede impartir múltiples materias y/o hacerlo en diferentes sedes.

---

### Subject → TeachingAssignment

```text
Subject 1 ---- N TeachingAssignment
```

Una materia puede ser impartida por múltiples profesores.

---

### Campus → TeachingAssignment

```text
Campus 1 ---- N TeachingAssignment
```

Una sede puede tener múltiples profesores y materias asociadas.

---

## 4. Restricciones de Negocio

### Review única por profesor

Un usuario únicamente podrá tener una referencia por profesor.

```text
User + Teacher = único
```

Si el usuario desea modificar su opinión, deberá editar la referencia existente.

---

### Correo institucional obligatorio

Todos los usuarios deberán registrarse utilizando un correo institucional válido de la Universidad de Cundinamarca.

---

### Catálogo controlado

Los usuarios no podrán crear:

* Profesores
* Materias
* Sedes

Estas entidades serán administradas previamente por el sistema.

---

## 5. Consideraciones Futuras

Las siguientes características podrían incorporarse en futuras versiones:

* Calificación numérica de profesores.
* Estadísticas por profesor.
* Facultades.
* Carreras académicas.
* Períodos académicos.
* Moderación de contenido.
* Reporte de referencias.

```
```
