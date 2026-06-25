# Use Cases

## Objetivo

Este documento describe las principales interacciones que los usuarios tendrán con el sistema.

Su propósito es definir qué funcionalidades debe ofrecer la aplicación antes de diseñar la API o implementar código.

---

## UC-01 Buscar Profesores por Materia y Sede

### Actor

Estudiante

### Descripción

Permite consultar los profesores que imparten una determinada materia en una sede específica.

### Flujo Principal

1. El estudiante accede a la plataforma.
2. Selecciona una materia.
3. Selecciona una sede.
4. El sistema busca los profesores asociados.
5. El sistema muestra los resultados.
6. El estudiante selecciona un profesor para consultar sus referencias.

### Resultado Esperado

El estudiante puede encontrar profesores relevantes para la materia y sede seleccionadas.

---

## UC-02 Consultar Referencias de un Profesor

### Actor

Estudiante

### Descripción

Permite visualizar las referencias asociadas a un profesor.

### Flujo Principal

1. El estudiante selecciona un profesor.
2. El sistema muestra todas las referencias disponibles.
3. El estudiante lee las experiencias compartidas por otros usuarios.

### Resultado Esperado

El estudiante obtiene información para tomar una decisión informada.

---

## UC-03 Registrarse

### Actor

Estudiante

### Descripción

Permite crear una cuenta utilizando un correo institucional.

### Flujo Principal

1. El estudiante accede al formulario de registro.
2. Ingresa nombre visible.
3. Ingresa correo institucional.
4. Ingresa contraseña.
5. El sistema valida la información.
6. Se crea la cuenta.

### Resultado Esperado

El estudiante queda registrado en la plataforma.

---

## UC-04 Iniciar Sesión

### Actor

Estudiante

### Descripción

Permite autenticarse en la plataforma.

### Flujo Principal

1. El estudiante ingresa correo institucional.
2. Ingresa contraseña.
3. El sistema valida credenciales.
4. El sistema inicia sesión.

### Resultado Esperado

El estudiante obtiene acceso a funcionalidades protegidas.

---

## UC-05 Crear Referencia

### Actor

Usuario autenticado

### Descripción

Permite publicar una referencia sobre un profesor.

### Flujo Principal

1. El usuario selecciona un profesor.
2. Escribe la referencia.
3. Envía la información.
4. El sistema valida la solicitud.
5. La referencia queda registrada.

### Resultado Esperado

La referencia aparece asociada al profesor.

---

## UC-06 Editar Referencia

### Actor

Usuario autenticado

### Descripción

Permite modificar una referencia previamente creada.

### Flujo Principal

1. El usuario accede a su referencia.
2. Modifica el contenido.
3. Guarda los cambios.
4. El sistema actualiza la información.

### Resultado Esperado

La referencia queda actualizada.

---

## UC-07 Eliminar Referencia

### Actor

Usuario autenticado

### Descripción

Permite eliminar una referencia propia.

### Flujo Principal

1. El usuario selecciona una referencia propia.
2. Solicita la eliminación.
3. El sistema elimina la referencia.

### Resultado Esperado

La referencia deja de estar disponible.
