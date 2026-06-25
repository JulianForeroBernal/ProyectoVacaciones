# Architecture

## 1. Objetivo

Este documento describe la arquitectura general de CundiReferencias y las decisiones técnicas principales tomadas durante la fase de diseño.

La arquitectura podrá evolucionar durante el desarrollo del proyecto conforme aparezcan nuevos requisitos o necesidades técnicas.

---

## 2. Visión General

CundiReferencias seguirá una arquitectura cliente-servidor compuesta por tres capas principales:

1. Frontend
2. Backend
3. Base de Datos

El frontend será responsable de la interacción con el usuario.

El backend será responsable de la lógica de negocio, autenticación, validaciones y acceso a datos.

La base de datos será responsable del almacenamiento persistente de la información.

---

## 3. Arquitectura General

```text
Usuario
    |
    v
Frontend (React + TypeScript)
    |
    v
REST API
    |
    v
Backend (FastAPI)
    |
    v
MySQL Database
```

---

## 4. Componentes Principales

### Frontend

Responsabilidades:

* Mostrar información al usuario.
* Gestionar formularios.
* Consumir la API REST.
* Gestionar navegación entre páginas.
* Gestionar autenticación del usuario.

Tecnologías:

* React
* TypeScript

---

### Backend

Responsabilidades:

* Exponer endpoints REST.
* Gestionar autenticación.
* Validar información.
* Aplicar reglas de negocio.
* Gestionar acceso a la base de datos.

Tecnologías:

* Python
* FastAPI

---

### Base de Datos

Responsabilidades:

* Almacenar usuarios.
* Almacenar referencias.
* Almacenar profesores.
* Almacenar materias.
* Almacenar sedes.

Tecnología:

* MySQL

---

## 5. Flujo General de Información

### Consulta de Referencias

Usuario

Usuario → Frontend → API → Backend → Base de Datos → Backend → Frontend → Usuario

---

### Creación de Referencias

Usuario autenticado
→ Frontend → API → Backend → Validaciones → Base de Datos → Confirmación → Frontend → Usuario

---

## 6. Entidades Principales

### User

Representa a un usuario registrado del sistema.

Responsabilidades:

* Autenticación.
* Creación de referencias.
* Edición de referencias propias.
* Eliminación de referencias propias.

---

### Teacher

Representa un profesor disponible en la plataforma.

Los profesores serán definidos previamente por el sistema.

Los usuarios no podrán crear profesores durante el MVP.

---

### Subject

Representa una materia académica.

Las materias serán definidas previamente por el sistema.

---

### Campus

Representa una sede universitaria.

---

### Review

Representa una referencia o experiencia compartida por un usuario.

Una referencia estará asociada a:

* Un usuario.
* Un profesor.

---

## 7. Decisiones Arquitectónicas

### Consulta Pública

Las referencias podrán visualizarse sin necesidad de autenticación.

Justificación:

Facilitar el acceso a la información y reducir barreras de entrada para los usuarios.

---

### Creación de Referencias Restringida

Únicamente usuarios autenticados podrán crear, editar o eliminar referencias.

Justificación:

Reducir spam y mejorar la trazabilidad de las publicaciones.

---

### Catálogo Controlado

Los profesores, materias y sedes serán gestionados previamente por el sistema.

Los usuarios no podrán crear estas entidades durante el MVP.

Justificación:

Mantener consistencia en la información y evitar duplicados.

---

### API REST

La comunicación entre frontend y backend se realizará mediante una API REST.

Justificación:

Separación clara entre cliente y servidor, facilitando mantenimiento y escalabilidad.

---

## 8. Evolución Futura

Algunas funcionalidades que podrían considerarse en futuras versiones son:

* Sistema de valoración numérica.
* Reacciones o votos.
* Moderación de contenido.
* Aplicación móvil.
* Panel administrativo.
* Notificaciones.
* Estadísticas avanzadas.
* Integración con sistemas universitarios.

```
```
