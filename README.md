# 🚪 BFF Gateway - Inovatech

Backend For Frontend (BFF) encargado de centralizar las peticiones entre el Frontend realizado en React + Vite y los microservicios del sistema.

---

# 📌 Tecnologías utilizadas

- Java 21
- Spring Boot 3
- Spring Cloud Gateway
- Maven
- Netty
- CORS Configuration
- JWT
- Postman
- IntelliJ IDEA

---

# 📦 Dependencias utilizadas

## Spring Boot
- Spring Reactive Web
- Spring Cloud Gateway
- Lombok
- Spring Boot DevTools
- Spring Boot Starter Test

## Spring Cloud
- Spring Cloud Gateway

---

# 🛠 Requisitos previos

Antes de ejecutar el proyecto debes instalar:

## ✅ Java 21

Oracle JDK 21:
https://www.oracle.com/java/technologies/javase/jdk21-archive-downloads.html

Verificar instalación:

java -version

---

## ✅ Maven

Apache Maven:
https://maven.apache.org/download.cgi

Verificar instalación:

mvn -version

---

## ✅ IntelliJ IDEA

https://www.jetbrains.com/idea/download/

---

## ✅ Postman

https://www.postman.com/downloads/

---

# ⚙ Configuración

## Puerto del BFF

server.port=9090

---

# 🔀 Rutas configuradas

## Register Service

spring.cloud.gateway.routes[0].id=register-service
spring.cloud.gateway.routes[0].uri=http://localhost:9091
spring.cloud.gateway.routes[0].predicates[0]=Path=/api/register/**

## Login Service

spring.cloud.gateway.routes[1].id=login-service
spring.cloud.gateway.routes[1].uri=http://localhost:9092
spring.cloud.gateway.routes[1].predicates[0]=Path=/api/login/**

---

# 🌐 Configuración CORS

spring.cloud.gateway.server.webflux.globalcors.cors-configurations.[/**].allowedOrigins=http://localhost:5173
spring.cloud.gateway.server.webflux.globalcors.cors-configurations.[/**].allowedMethods=GET,POST,PUT,DELETE,OPTIONS
spring.cloud.gateway.server.webflux.globalcors.cors-configurations.[/**].allowedHeaders=*
spring.cloud.gateway.server.webflux.globalcors.add-to-simple-url-handler-mapping=true

---

# ▶ Cómo ejecutar el proyecto

1️⃣ Clonar repositorio

git clone URL_DEL_REPOSITORIO

---

2️⃣ Abrir proyecto en IntelliJ

- File
- Open
- Seleccionar carpeta del proyecto

---

3️⃣ Ejecutar aplicación

BffGatewayApplication

---

# 🧪 Tests

mvn test

O desde IntelliJ:

- Click derecho carpeta test
- Run Tests

---

# 📡 Endpoints disponibles

## Register

POST http://localhost:9090/api/register

## Login

POST http://localhost:9090/api/login

## Obtener usuarios

GET http://localhost:9090/api/login/users

---

# 🧠 Función del BFF

El BFF actúa como intermediario entre el frontend y los microservicios.

## Beneficios:
- Centraliza las peticiones
- Maneja CORS
- Oculta puertos internos
- Facilita escalabilidad
- Simplifica conexión Frontend ↔ Backend

---

# 👨‍💻 Autores

Camilo Leiva (cc.leiva@duocuc.cl)
Nicolas Rivera (nico.veraf@duocuc.cl)
Ramiro Gomez (ra.gomezv@duocuc.cl)
Laura Fontecilla (la.fontecilla@duocuc.cl)

Proyecto desarrollado para Inovatech.

