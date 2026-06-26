# API Design

## Objetivo

Este documento describe los endpoints principales que permitirán la comunicación entre el frontend y el backend.

La API seguirá principios REST.

---

## Authentication

### Register

```http
POST /auth/register
```

Crear una nueva cuenta.

---

### Login

```http
POST /auth/login
```

Autenticar un usuario.

---

## Teachers

### Get Teachers

```http
GET /teachers
```

Obtiene la lista de profesores.

Filtros soportados:

```http
GET /teachers?subject={subject_id}&campus={campus_id}
```

---

### Get Teacher Details

```http
GET /teachers/{teacher_id}
```

Obtiene información detallada de un profesor.

---

## Reviews

### Get Reviews by Teacher

```http
GET /teachers/{teacher_id}/reviews
```

Obtiene todas las referencias de un profesor.

---

### Create Review

```http
POST /reviews
```

Crear una nueva referencia.

Requiere autenticación.

---

### Update Review

```http
PUT /reviews/{review_id}
```

Actualizar una referencia existente.

Requiere autenticación.

---

### Delete Review

```http
DELETE /reviews/{review_id}
```

Eliminar una referencia.

Requiere autenticación.

---

## Subjects

### Get Subjects

```http
GET /subjects
```

Obtiene la lista de materias disponibles.

---

## Campuses

### Get Campuses

```http
GET /campuses
```

Obtiene la lista de sedes disponibles.
