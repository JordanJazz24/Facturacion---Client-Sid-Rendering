# Facturacion---Client-Side-Rendering

**Autor:** [JordanJazz24](https://github.com/JordanJazz24)  
**Repositorio:** [Facturacion---Client-Sid-Rendering](https://github.com/JordanJazz24/Facturacion---Client-Sid-Rendering)  
**Lenguaje Principal:** Java  
**Framework:** Spring Boot (MVC Web)  
**Motor de Plantillas:** Thymeleaf  
**Base de Datos:** MySQL  
**Estado:** En desarrollo

---

## Descripción

Este proyecto implementa un sistema web para la gestión de facturación electrónica, orientado a proveedores de bienes y servicios y sus clientes. El sistema almacena datos en una base de datos MySQL y utiliza el patrón MVC de Spring Boot en la capa de presentación, con renderizado exclusivo del lado del servidor (SSR) y sin el uso de JavaScript, asegurando compatibilidad, seguridad y simplicidad.

---

## Características principales

- **Registro y gestión de proveedores:**  
  Permite a personas físicas o jurídicas registrarse y configurar su perfil, incluyendo datos requeridos por el Ministerio de Hacienda de Costa Rica.
- **Gestión de clientes:**  
  Registro, visualización y administración de clientes asociados a cada proveedor.
- **Gestión de productos/servicios:**  
  Registro y administración de productos o servicios ofrecidos por cada proveedor.
- **Facturación electrónica:**  
  Creación y gestión de facturas electrónicas para clientes, incluyendo visualización en PDF y XML.
- **Control de acceso y roles:**  
  Autenticación por sesión y habilitación de funcionalidades según el rol del usuario (proveedor o administrador).
- **Gestión administrativa:**  
  Permite a administradores aceptar, listar y desactivar proveedores.
- **Arquitectura de tres capas:**  
  Separación en capas de Presentación (MVC/Thymeleaf), Lógica de Negocio (Servicios) y Datos (Repositorios/JPA).
- **Sin JavaScript:**  
  Todo el renderizado y la interacción se realizan del lado del servidor usando Thymeleaf.

---

## Estructura del proyecto

```
Facturacion---Client-Sid-Rendering/
├── src/
│   ├── main/java/com/example/facturacion/
│   │   ├── data/       # Repositorios JPA (Usuarios, Proveedores, Clientes, Productos, Facturas, Detalles)
│   │   ├── logic/      # Lógica de negocio (Service, entidades)
│   │   └── ...         # Controladores y vistas (MVC)
│   └── resources/
│       └── templates/  # Vistas Thymeleaf
└── README.md
```

---

## Principales entidades y flujo

- **Usuario:**  
  Acceso y autenticación al sistema.
- **Proveedor:**  
  Relacionado con usuario, gestiona clientes, productos y facturas.
- **Cliente:**  
  Asociado a un proveedor, destinatario de facturas.
- **Producto:**  
  Bien o servicio registrado por el proveedor.
- **Factura & Detalle:**  
  Facturación electrónica, representación en PDF/XML.

---

## Requerimientos no funcionales y reglas

- Renderizado solo del lado del servidor (SSR).
- Prohibido el uso de JavaScript.
- Uso obligatorio de Spring MVC y Thymeleaf.
- Control de acceso por sesión y roles.
- Menú siempre visible con opciones según usuario logueado.
- Arquitectura en 3 capas bien definida.

---

## Instalación y ejecución

1. **Clona el repositorio:**
   ```bash
   git clone https://github.com/JordanJazz24/Facturacion---Client-Sid-Rendering.git
   cd Facturacion---Client-Sid-Rendering
   ```
2. **Configura la base de datos MySQL** en `application.properties`.
3. **Construye el proyecto:**
   ```bash
   ./mvnw clean install
   ```
4. **Ejecuta la aplicación:**
   ```bash
   ./mvnw spring-boot:run
   ```
   Accede a la aplicación en `http://localhost:8080/`.

---

## Notas y exclusiones

- No se conecta al sistema real del Ministerio de Hacienda de Costa Rica; se recomienda un STUB o validación simulada.
- No implementa el registro real ante ATV ni el uso del Catálogo CABYS.
- El proyecto es de carácter educativo y puede ser extendido para producción.

---

## Contacto

Para dudas, sugerencias o soporte, contacta a [JordanJazz24](https://github.com/JordanJazz24).

---

**Este proyecto demuestra calidad en el diseño MVC, arquitectura por capas y prácticas modernas para aplicaciones empresariales en Java/Spring Boot, maximizando la seguridad y el control del flujo de usuario mediante SSR.**
