
# Servicios web en C#

En C# puedes crear servicios web utilizando **Visual C#** y **ASP.NET**. Puedes escribir un servicio web utilizando **Visual C# .NET**. Para hacerlo, necesitarás tener instalado **Microsoft Windows Internet Information Server** y **Visual Studio .NET**. En Visual Studio, puedes seleccionar la opción de **ASP.NET servicio web** en Plantillas para crear un nuevo proyecto. Una vez que hayas creado el proyecto, puedes definir métodos que encapsulan la funcionalidad del servicio. Cada método que se expondrá desde el servicio debe marcarse con un atributo **WebMethod** delante de él.

También puedes crear una aplicación web de **ASP.NET Core de C#** en Visual Studio. Para hacerlo, necesitarás tener instalado Visual Studio y seleccionar la plantilla de **Aplicación web de ASP.NET Core** al crear un nuevo proyecto.

Además, puedes consumir servicios web de asmx creados en .Net desde una aplicación web ASP Webform o MVC con C# u otro lenguaje. Un servicio web permite que las aplicaciones se conecten a él para realizar operaciones sin depender del lenguaje de programación.

## Diferencias entre servicios web, WCF y RESTful

Un **servicio web** es una aplicación que se comunica con otras aplicaciones a través de la red utilizando protocolos estándar como HTTP y XML. Los servicios web permiten que las aplicaciones se conecten entre sí para realizar operaciones sin depender del lenguaje de programación o la plataforma.

### Para crear un servicio web en Visual Studio 2022, puedes seguir estos pasos:

1. Abre Visual Studio 2022.
2. En la ventana de inicio, elige **Crear un proyecto nuevo**.
3. Escribe **biblioteca de servicios wcf** en el cuadro de búsqueda de la página **Crear un proyecto**.
4. Selecciona la plantilla de **C#** o **Visual Basic** para la biblioteca de servicios WCF y haz clic en **Siguiente**².
5. En la página **Configurar el nuevo proyecto**, haz clic en **Crear**².

Una vez que hayas creado el proyecto, puedes definir métodos que encapsulan la funcionalidad del servicio. Cada método que se expondrá desde el servicio debe marcarse con un atributo **WebMethod** delante de él¹.


**Windows Communication Foundation (WCF)** es un marco para crear aplicaciones orientadas a servicios. Con WCF, puedes enviar datos como mensajes asincrónicos de un punto de conexión de servicio a otro. Un extremo de servicio puede formar parte de un servicio disponible continuamente hospedado por IIS, o puede ser un servicio hospedado en una aplicación. Un extremo puede ser un cliente de un servicio que solicita datos de un extremo de servicio. Los mensajes pueden ser tan simples como un carácter o una palabra que se envía como XML, o tan complejos como una secuencia de datos binarios.

### Para crear un servicio WCF en Visual Studio 2022, puedes seguir estos pasos:

1. Abre Visual Studio 2022.
2. En la ventana de inicio, elige **Crear un proyecto nuevo**.
3. Escribe **biblioteca de servicios wcf** en el cuadro de búsqueda de la página **Crear un proyecto**.
4. Selecciona la plantilla de **C#** o **Visual Basic** para la biblioteca de servicios WCF y haz clic en **Siguiente**².
5. En la página **Configurar el nuevo proyecto**, haz clic en **Crear**².

Una vez que hayas creado el proyecto, puedes definir métodos que encapsulan la funcionalidad del servicio. Cada método que se expondrá desde el servicio debe marcarse con un atributo **OperationContractAttribute**¹.

**RESTful** es un estilo de arquitectura para crear servicios web. REST significa **Representational State Transfer** y se basa en el uso de los verbos HTTP estándar (GET, POST, PUT, DELETE) para realizar operaciones en recursos identificados por URIs. Los servicios RESTful son fáciles de consumir por cualquier cliente que pueda realizar solicitudes HTTP y son ampliamente utilizados en aplicaciones web y móviles.

### Para crear un servicio RESTful en Visual Studio 2022, puedes seguir estos pasos:

1. Abre Visual Studio 2022.
2. En la ventana de inicio, elige **Crear un proyecto nuevo**.
3. Escribe **aplicación web ASP.NET Core** en el cuadro de búsqueda de la página **Crear un proyecto**.
4. Selecciona la plantilla para una aplicación web ASP.NET Core y haz clic en **Siguiente**.
5. En la página **Configurar el nuevo proyecto**, haz clic en **Crear**.

Una vez que hayas creado el proyecto, puedes definir métodos que encapsulan la funcionalidad del servicio utilizando los verbos HTTP estándar (GET, POST, PUT, DELETE) para realizar operaciones en recursos identificados por URIs.

En resumen, los servicios web son aplicaciones que se comunican a través de la red utilizando protocolos estándar. WCF es un marco para crear aplicaciones orientadas a servicios y RESTful es un estilo de arquitectura para crear servicios web. Cada uno tiene sus propias características y se utilizan en diferentes casos según las necesidades del proyecto.


