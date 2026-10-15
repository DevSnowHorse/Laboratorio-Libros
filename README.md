# Laboratorio Full Stack: Spring Boot + ReactJS

Aplicación web para administrar un catálogo de libros. Permite crear, consultar, actualizar, eliminar y buscar libros por nombre.

- **Estudiante:** Daniel Salgado Mazo//Juan David Castro // Duvan Pinilla
- **Docente:** Diego Botia
- **Institución:** Tecnológico de Antioquia, 2026

## Contenido del repositorio

| Carpeta o archivo | Descripción |
|---|---|
| `book/` | Backend: API REST con Spring Boot |
| `catalog-frontend/` | Frontend: interfaz en ReactJS |
| `Informe_Laboratorio_FullStack.docx` | Informe del laboratorio |

## Tecnologías

- **Backend:** Java 17, Spring Boot 3.5.14, Spring Data JPA, base de datos H2 en memoria, Lombok, springdoc-openapi (Swagger)
- **Frontend:** ReactJS, Axios, Bootstrap

## Requisitos

- JDK 17 o superior
- Node.js (versión LTS)

## Cómo ejecutarlo

**1. Backend** (puerto 8080). Dentro de la carpeta `book`:

```
./mvnw spring-boot:run
```

En Windows (CMD), usa `mvnw.cmd spring-boot:run`. También se puede abrir la carpeta en IntelliJ IDEA y ejecutar la clase `BookApplication`.

**2. Frontend** (puerto 3000). En otra terminal, dentro de la carpeta `catalog-frontend`:

```
npm install
npm start
```

Se abre `http://localhost:3000`.

## Direcciones útiles

| Recurso | URL |
|---|---|
| Aplicación (React) | http://localhost:3000 |
| Swagger UI | http://localhost:8080/swagger-ui.html |
| Consola H2 | http://localhost:8080/h2-console |

Datos de la consola H2: JDBC URL `jdbc:h2:mem:book`, usuario `sa`, contraseña `sa`.

## Endpoints de la API

| Método | Ruta | Descripción |
|---|---|---|
| GET | `/api/books` | Lista todos los libros |
| GET | `/api/books/{id}` | Consulta un libro por id |
| POST | `/api/books` | Crea un libro |
| PUT | `/api/books/{id}` | Actualiza un libro |
| DELETE | `/api/books/{id}` | Elimina un libro |
| GET | `/api/books/search?name=` | Busca libros por nombre |

## Nota

La base de datos H2 funciona en memoria, por lo que los datos se pierden al detener el backend.
