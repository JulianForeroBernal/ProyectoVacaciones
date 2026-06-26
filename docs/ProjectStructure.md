# Project Structure

## Objetivo

Este documento define la estructura de carpetas del proyecto y el propósito de cada directorio.

El objetivo es mantener una organización consistente durante el desarrollo y facilitar que todos los integrantes del equipo puedan localizar archivos y comprender sus responsabilidades.

---

# Estructura General

```text
CundiReferencias/
│
├── frontend/
├── backend/
├── docs/
├── .gitignore
└── README.md
```

---

## frontend/

Contiene toda la aplicación del lado del cliente.

Tecnologías:

* React
* TypeScript

Estructura:

```text
frontend/
│
├── public/
│
├── src/
│   │
│   ├── pages/
│   ├── components/
│   ├── services/
│   ├── hooks/
│   ├── types/
│   ├── assets/
│   ├── App.tsx
│   └── main.tsx
│
├── package.json
└── README.md
```

### pages/

Contiene las páginas completas de la aplicación.

Ejemplos:

```text
HomePage
TeacherPage
LoginPage
RegisterPage
```

Una página es responsable de ensamblar componentes y mostrar una pantalla completa.

---

### components/

Contiene componentes reutilizables de la interfaz.

Ejemplos:

```text
Navbar
SearchBar
ReviewCard
TeacherCard
Button
```

Los componentes deben ser reutilizables siempre que sea posible.

---

### services/

Contiene la comunicación con la API del backend.

Ejemplos:

```text
authService
teacherService
reviewService
```

El resto del frontend no debe realizar peticiones HTTP directamente.

Toda la comunicación con la API debe centralizarse aquí.

---

### hooks/

Contiene hooks personalizados de React.

Ejemplos:

```text
useAuth
useTeachers
```

---

### types/

Contiene tipos e interfaces de TypeScript.

Ejemplos:

```text
User
Teacher
Review
```

---

### assets/

Contiene recursos estáticos.

Ejemplos:

```text
Imágenes
Iconos
Logos
```

---

## backend/

Contiene toda la aplicación del lado del servidor.

Tecnologías:

* Python
* FastAPI

Estructura:

```text
backend/
│
├── app/
│   │
│   ├── api/
│   ├── models/
│   ├── schemas/
│   ├── services/
│   ├── repositories/
│   └── main.py
│
├── tests/
├── requirements.txt
└── README.md
```

---

### api/

Contiene los endpoints de la API REST.

Ejemplos:

```text
auth_routes
teacher_routes
review_routes
```

Es responsable de recibir solicitudes y devolver respuestas.

---

### models/

Contiene los modelos de base de datos.

Ejemplos:

```text
User
Teacher
Review
TeachingAssignment
```

Representan la estructura de datos del sistema.

---

### schemas/

Contiene los esquemas de entrada y salida de datos.

Ejemplos:

```text
UserCreate
UserResponse
ReviewCreate
ReviewResponse
```

Son responsables de validar la información recibida y enviada por la API.

---

### services/

Contiene la lógica de negocio.

Ejemplos:

```text
AuthenticationService
TeacherService
ReviewService
```

Los servicios contienen las reglas de funcionamiento de la aplicación.

---

### repositories/

Es responsable del acceso a la base de datos.

Ejemplos:

```text
UserRepository
TeacherRepository
ReviewRepository
```

Únicamente los repositorios deben comunicarse directamente con la base de datos.

---

### tests/

Contiene las pruebas automatizadas.

Ejemplos:

```text
test_auth
test_reviews
```

Toda nueva funcionalidad debería incluir pruebas cuando sea posible.

---

## docs/

Contiene la documentación del proyecto.

Estructura:

```text
docs/
│
├── README.md
├── ProjectScope.md
├── TeamRules.md
├── CONTRIBUTING.md
├── Architecture.md
├── DataModel.md
├── UseCases.md
├── APIDesign.md
└── diagrams/
```

---

### diagrams/

Contiene diagramas UML y diagramas de arquitectura.

Ejemplos:

```text
Use Case Diagram
Class Diagram
Component Diagram
ER Diagram
```

Los diagramas deberán actualizarse cuando existan cambios arquitectónicos importantes.

---

# Principios Generales

## Separación de Responsabilidades

Cada carpeta debe tener una responsabilidad clara y única.

Evitar colocar archivos en directorios que no correspondan a su función.

---

## Nomenclatura Consistente

Se utilizará inglés para:

* Nombres de carpetas.
* Nombres de archivos.
* Variables.
* Funciones.
* Clases.
* Commits.

---

## Documentación

Las decisiones arquitectónicas importantes deberán documentarse antes de su implementación siempre que sea posible.

---

## Escalabilidad

La estructura debe permitir el crecimiento futuro del proyecto sin requerir reorganizaciones importantes.
