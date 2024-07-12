# Aplicación API REST - CRUD en Java

## Descripción

Este proyecto es una aplicación API REST simple que implementa operaciones CRUD (Crear, Leer, Actualizar, Eliminar) en Java. Para el desarrollo se utilizó Spring Boot para el framework, Hibernate para la capa de persistencia y PostgreSQL como base de datos. La aplicación está desplegada en Railway.

## Prueba - Despliegue

<div align="center">
  <img src="https://github.com/RendevMq/MyGIFS/blob/main/CRUD.gif?raw=true" width="700" alt="Final Result">
</div>


## Funcionalidades

- **Crear**: Añadir nuevos registros a la base de datos.
- **Leer**: Obtener uno o todos los registros de la base de datos.
- **Actualizar**: Modificar registros existentes en la base de datos.
- **Eliminar**: Borrar registros de la base de datos.

## Tecnologías Utilizadas

- **Lenguaje de Programación**: Java
- **Framework**: Spring Boot
- **Persistencia**: Hibernate
- **Base de Datos**: PostgreSQL
- **Despliegue**: Railway

## Configuración del Entorno

### Requisitos Previos

- Java 8 o superior
- Maven
- PostgreSQL
- Cuenta en Railway

### Instalación

1. Clonar el repositorio:
    ```bash
    git clone https://github.com/usuario/repositorio.git
    ```
2. Navegar al directorio del proyecto:
    ```bash
    cd repositorio
    ```
3. Configurar la base de datos PostgreSQL en `application.properties`:
    ```properties
    spring.datasource.url=jdbc:postgresql://localhost:5432/nombre_base_datos
    spring.datasource.username=usuario
    spring.datasource.password=contraseña
    spring.jpa.hibernate.ddl-auto=update
    spring.jpa.show-sql=true
    spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect
    ```
4. Compilar y ejecutar la aplicación:
    ```bash
    mvn clean install
    mvn spring-boot:run
    ```

### Despliegue en Railway

1. Crear una cuenta en [Railway](https://railway.app/).
2. Conectar el repositorio de GitHub a Railway.
3. Configurar las variables de entorno en Railway para la conexión a la base de datos.
4. Desplegar la aplicación desde Railway.

## Uso

La aplicación expone las siguientes endpoints para las operaciones CRUD:

- **Crear**:
    ```http
    POST /api/entidades
    ```
- **Leer Todos**:
    ```http
    GET /api/entidades
    ```
- **Leer Uno**:
    ```http
    GET /api/entidades/{id}
    ```
- **Actualizar**:
    ```http
    PUT /api/entidades/{id}
    ```
- **Eliminar**:
    ```http
    DELETE /api/entidades/{id}
    ```



