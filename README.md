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

## 📁 Entregables en GitHub
Este documento cumple con los requisitos solicitados en la carpeta:
` /docs/cloud `
"""

html_content = f"""
<!DOCTYPE html>
<html>
<head>
<style>
    @page {{
        size: A4;
        margin: 0;
        background-color: #1e1e1e;
    }}
    body {{
        margin: 0;
        padding: 0;
        font-family: 'Consolas', 'Courier New', monospace;
        background-color: #1e1e1e;
        color: #d4d4d4;
    }}
    .vscode-container {{
        width: 210mm;
        height: 297mm;
        box-sizing: border-box;
        display: block;
        position: relative;
    }}
    .title-bar {{
        background-color: #3c3c3c;
        height: 35px;
        display: flex;
        align-items: center;
        padding-left: 15px;
        font-size: 12px;
        color: #cccccc;
        border-bottom: 1px solid #2b2b2b;
    }}
    .editor-layout {{
        display: flex;
        height: calc(100% - 35px);
    }}
    .sidebar {{
        width: 50px;
        background-color: #333333;
        border-right: 1px solid #2b2b2b;
    }}
    .line-numbers {{
        width: 45px;
        background-color: #1e1e1e;
        color: #858585;
        text-align: right;
        padding-right: 10px;
        padding-top: 15px;
        font-size: 14px;
        line-height: 1.6;
        user-select: none;
    }}
    .code-area {{
        flex-grow: 1;
        padding: 15px;
        font-size: 14px;
        line-height: 1.6;
        white-space: pre-wrap;
        word-wrap: break-word;
    }}
    .keyword {{ color: #569cd6; }}
    .string {{ color: #ce9178; }}
    .comment {{ color: #6a9955; }}
    .header {{ color: #569cd6; font-weight: bold; }}
    .list-bullet {{ color: #d16969; }}
    .table-border {{ color: #808080; }}
</style>
</head>
<body>
    <div class="vscode-container">
        <div class="title-bar">
            README.md — FitLife — Visual Studio Code
        </div>
        <div class="editor-layout">
            <div class="sidebar"></div>
            <div class="line-numbers">
                1<br>2<br>3<br>4<br>5<br>6<br>7<br>8<br>9<br>10<br>11<br>12<br>13<br>14<br>15<br>16<br>17<br>18<br>19<br>20<br>21<br>22<br>23<br>24<br>25<br>26<br>27<br>28<br>29<br>30<br>31<br>32<br>33<br>34<br>35<br>36<br>37<br>38<br>39<br>40<br>41
            </div>
            <div class="code-area">
<span class="header"># 🏋️ FitLife - Gestión de Gimnasio (Cloud)</span>

Este apartado del proyecto corresponde al módulo de <span class="string">**Fundamentos de Computación en la Nube**</span>. El objetivo es proponer una arquitectura profesional, sencilla y analizar su viabilidad económica.

<span class="header">## 1. Elección de Proveedor Cloud</span>
El proveedor seleccionado para <span class="string">**FitLife**</span> es <span class="string">**Amazon Web Services (AWS)**</span>.

<span class="list-bullet">*</span> <span class="keyword">**Por qué se ha elegido:**</span> Es el proveedor con mayor cuota de mercado y ofrece una infraestructura robusta y escalable.
<span class="list-bullet">*</span> <span class="keyword">**Ventajas:**</span> Permite el uso de servicios gestionados que reducen la carga de administración técnica y ofrece un nivel gratuito (Free Tier) ideal para el inicio del proyecto.

<span class="header">## 2. Arquitectura Cloud Propuesta</span>
Se ha diseñado una arquitectura funcional que garantiza la separación de la lógica de negocio y los datos.

<span class="keyword">**Flujo de funcionamiento:**</span>
1.  Usuarios: Acceden a la plataforma desde sus dispositivos.
2.  Servidor de Aplicación: Procesa las solicitudes de reservas y gestión de socios.
3.  Base de Datos: Almacena de forma persistente toda la información del gimnasio.

<span class="keyword">**Esquema:**</span>
`Usuario` ➔ `Instancia de aplicación` ➔ `Base de datos gestionada`.

<span class="header">## 3. Servicios Cloud Utilizados</span>
Para el despliegue se requieren los siguientes servicios:
<span class="list-bullet">*</span> <span class="string">**Amazon EC2:**</span> Instancia de servidor virtual para ejecutar la aplicación.
<span class="list-bullet">*</span> <span class="string">**Amazon RDS:**</span> Base de datos gestionada para asegurar la integridad de los datos de los socios.
<span class="list-bullet">*</span> <span class="string">**Amazon S3:**</span> Almacenamiento para archivos estáticos y copias de seguridad.

<span class="header">## 4. Estimación de Costes Mensuales</span>
Utilizando la calculadora de precios de AWS, se estima el siguiente coste para una operativa básica:

<span class="table-border">| Recurso | Configuración | Coste Aprox. |
| :--- | :--- | :--- |
| **Computación (EC2)** | t2.micro | 0,00 € (Free Tier) |
| **Base de Datos (RDS)** | db.t3.micro | 0,00 € (Free Tier) |
| **Almacenamiento (S3)** | 5 GB Estándar | < 0,20 € |
| **TOTAL** | | **~ 0,00 € / mes** |</span>

<span class="header">## 📁 Entregables en GitHub</span>
Este documento cumple con los requisitos solicitados en la carpeta:
<span class="string">` /docs/cloud `</span>
            </div>
        </div>
    </div>
</body>
</html>
"""

with open("FitLife_README_VSCode.html", "w") as f:
    f.write(html_content)

HTML(filename="FitLife_README_VSCode.html").write_pdf("FitLife_README_VSCode.pdf")
