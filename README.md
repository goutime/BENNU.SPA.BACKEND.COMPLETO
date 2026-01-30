### 📝 Control de Notas - Backend (Quarkus)
Backend API desarrollado con Quarkus 3.13 para un sistema de gestión de notas. Implementa una arquitectura moderna, eficiente y lista para despliegue nativo.

🚀 Tecnologías Principales
Java 17 - Lenguaje base

Quarkus 3.13.0 - Framework Supersonic Subatomic Java

PostgreSQL - Base de datos (controlador JDBC incluido)

MyBatis Quarkiverse 2.2.3 - Mapeo objeto-relacional

Lombok 1.18.34 - Reducción de código boilerplate

RESTEasy + Jackson - API REST con serialización JSON

🏗️ Arquitectura
text
Backend Quarkus
├── API REST (JAX-RS)
├── MyBatis (Persistencia)
├── PostgreSQL (Base de datos)
├── Inyección de dependencias (Arc)
└── Configuración optimizada para cloud
📦 Dependencias Clave
Core
quarkus-arc - Inyección de dependencias CDI

quarkus-rest + quarkus-rest-jackson - API REST con JSON

quarkus-mybatis - Integración MyBatis para Quarkus

quarkus-jdbc-postgresql - Conector PostgreSQL

Desarrollo
lombok - Anotaciones para reducir código

quarkus-junit5 - Testing

rest-assured - Pruebas de endpoints REST

⚙️ Características Técnicas
Rendimiento
Arranque ultrarrápido (~0.05s en desarrollo)

Memoria reducida (optimizado para contenedores)

Compilación nativa compatible (perfil native)

Seguridad y Calidad
Configuración type-safe

Testing integrado con JUnit 5

Parámetros de método conservados (-parameters)

Cloud Ready
Empaquetado como JAR ejecutable

Perfil nativo para GraalVM

Health checks integrados (por agregar)

Métricas (por agregar)

🛠️ Comandos de Desarrollo
bash
# Modo desarrollo (hot reload)
./mvnw quarkus:dev

# Construir JAR normal
./mvnw clean package

# Construir ejecutable nativo
./mvnw clean package -Pnative

# Ejecutar tests
./mvnw test
./mvnw verify -DskipTests=false
📁 Estructura del Proyecto
text
src/main/java/cl/bennu/note/
├── controllers/    # Endpoints REST
├── services/       # Lógica de negocio
├── mappers/        # MyBatis mappers
├── entities/       # Entidades/Modelos
└── dtos/           # Objetos de transferencia
🔧 Configuración
properties
# application.properties
quarkus.datasource.db-kind=postgresql
quarkus.datasource.username=${DB_USER}
quarkus.datasource.password=${DB_PASSWORD}
quarkus.datasource.jdbc.url=${DB_URL}
quarkus.mybatis.enabled=true
🧪 Testing
Tests unitarios con JUnit 5

Tests de integración con REST Assured

Tests nativos (perfil native)

Cobertura configurable

☁️ Despliegue
Opciones
JAR tradicional (java -jar back-0.0.1-runner.jar)

Imagen nativa (Docker + GraalVM)

Plataformas cloud: Kubernetes, OpenShift, AWS Lambda

Variables de Entorno Requeridas
text
DB_URL=jdbc:postgresql://host:port/database
DB_USER=usuario
DB_PASSWORD=contraseña
📈 Próximas Mejoras
Autenticación JWT

OpenAPI/Swagger documentation

Health checks y métricas

Cache distribuido (Redis)

Mensajería asíncrona

🎯 Propósito del Proyecto
Este backend sirve como base escalable para aplicaciones educativas o de productividad, demostrando mejores prácticas en:

Desarrollo moderno con Quarkus

APIs REST eficientes

Integración con bases de datos relacionales

Preparación para entornos cloud nativos

✨ "Supersonic Subatomic Java" - Optimizado para la nube y el desarrollo productivo.
