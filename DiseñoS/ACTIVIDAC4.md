11-02
---
#### Daniel Pérez Lozada / Luis Ignacio Bonilla Delgado
---
# Desarrollo Actividad Modelo C4

## Actividad Individual: Modelo C4 para Diseño de Software
## Desarrollo de la Actividad

### 1. Diagrama de Contexto
El diagrama de contexto muestra los actores y sistemas externos que interactúan con la aplicación de gestión de una escuela de conducción.

Descripción General del Sistema
El Sistema de Gestión de Escuela de Conducción permite administrar estudiantes, cursos y pagos. Facilita la comunicación entre instructores y estudiantes, gestiona pagos y proporciona herramientas de seguimiento para administradores.

#### Actores y Relaciones
***Estudiantes***: Se inscriben en cursos, realizan pagos y consultan su progreso.\
***Instructores***: Gestionan cursos, registran evaluaciones y coordinan clases.\
***Administradores***: Gestionan la información de estudiantes e instructores, y supervisan pagos.\
***Pasarela de Pago***: Proceso externo encargado de gestionar transacciones financieras.

![alt text](img1.jpg)

### 2. Diagrama de Contenedores
Este diagrama representa los principales contenedores del sistema.
#### **Elementos:**
***Aplicación Web:*** Interfaz gráfica utilizada por estudiantes e instructores.\
***API Backend:*** Contiene la lógica de negocio y gestiona la comunicación con la base de datos.\
***Base de Datos:*** Almacena información de usuarios, cursos y pagos.\
***Pasarela de Pagos:*** Servicio externo encargado de las transacciones.

![alt text](img2.jpg)

### 3. Diagrama de Componentes
Para el contenedor **Backend (Spring Boot)**, se detallan sus componentes internos:

#### **Elementos:**
#### Componentes del API Backend
***Controlador de Estudiantes:*** Maneja inscripciones y consultas de estudiantes.\
***Controlador de Cursos:*** Gestiona la creación y asignación de cursos.\
***Servicio de Autenticación:*** Administra accesos y permisos de usuarios.\
***Repositorio de Datos:*** Conecta la API con la base de datos.

![alt text](img3.jpg)

### 4. Diagrama de Código (Opcional)
Se presenta un fragmento del **Controlador de Tareas** en Java usando Spring Boot.

![alt text](img4.jpg)

## Explicación de los Diagramas
- **Diagrama de Contexto:** Muestra las interacciones externas con el sistema.
- **Diagrama de Contenedores:** Define la estructura principal del sistema.
- **Diagrama de Componentes:** Describe los elementos internos del backend.
- **Diagrama de Código:** Proporciona un ejemplo específico de implementación.

## Conclusión
El Modelo C4 facilita la comprensión de la arquitectura del software mediante diferentes niveles de abstracción. Este ejercicio ayuda a visualizar cómo se estructura una aplicación de gestión de tareas de manera clara y ordenada.
