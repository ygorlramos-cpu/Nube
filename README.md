from weasyprint import HTML
import base64

# Contenido del README.md en formato de bloque de código Markdown para el PDF
markdown_content = """
# 🏋️ FitLife - Gestión de Gimnasio (Cloud)

Este apartado del proyecto corresponde al módulo de **Fundamentos de Computación en la Nube**. El objetivo es proponer una arquitectura profesional, sencilla y analizar su viabilidad económica.

## 1. Elección de Proveedor Cloud
El proveedor seleccionado para **FitLife** es **Amazon Web Services (AWS)**.

* **Por qué se ha elegido:** Es el proveedor con mayor cuota de mercado y ofrece una infraestructura robusta y escalable.
* **Ventajas:** Permite el uso de servicios gestionados que reducen la carga de administración técnica y ofrece un nivel gratuito (Free Tier) ideal para el inicio del proyecto.

## 2. Arquitectura Cloud Propuesta
Se ha diseñado una arquitectura funcional que garantiza la separación de la lógica de negocio y los datos.

**Flujo de funcionamiento:**
1.  **Usuarios:** Acceden a la plataforma desde sus dispositivos.
2.  **Servidor de Aplicación:** Procesa las solicitudes de reservas y gestión de socios.
3.  **Base de Datos:** Almacena de forma persistente toda la información del gimnasio.

**Esquema:**
`Usuario` ➔ `Instancia de aplicación` ➔ `Base de datos gestionada`.

## 3. Servicios Cloud Utilizados
Para el despliegue se requieren los siguientes servicios:
* **Amazon EC2:** Instancia de servidor virtual para ejecutar la aplicación.
* **Amazon RDS:** Base de datos gestionada para asegurar la integridad de los datos de los socios.
* **Amazon S3:** Almacenamiento para archivos estáticos y copias de seguridad.

## 4. Estimación de Costes Mensuales
Utilizando la calculadora de precios de AWS, se estima el siguiente coste para una operativa básica:

| Recurso | Configuración | Coste Aprox. |
| :--- | :--- | :--- |
| **Computación (EC2)** | t2.micro | 0,00 € (Free Tier) |
| **Base de Datos (RDS)** | db.t3.micro | 0,00 € (Free Tier) |
| **Almacenamiento (S3)** | 5 GB Estándar | < 0,20 € |
| **TOTAL** | | **~ 0,00 € / mes** |

