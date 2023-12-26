

1. **Componente**: En Angular, un componente es una combinación de una plantilla HTML, estilos CSS y lógica TypeScript. Representa una parte de la interfaz de usuario y puede tener su propio comportamiento y datos. Los componentes se utilizan para crear elementos visuales interactivos y reutilizables en una aplicación Angular¹. Un ejemplo de cómo crear un componente en Angular sería el siguiente:
```typescript
ng generate component nombre-del-componente
```
Esto generará los archivos necesarios para el nuevo componente, incluyendo la plantilla HTML, los estilos CSS y el código TypeScript¹.

2. **Módulo**: Un módulo en Angular es uno de los elementos principales con los que podemos organizar el código de las aplicaciones. Podemos desarrollar diferentes módulos y agrupar distintos elementos (como componentes, directivas o pipes) en unos u otros⁶. Un ejemplo de cómo crear un módulo en Angular sería el siguiente:
```typescript
ng generate module nombre
```
Esto generará un nuevo módulo con el nombre especificado⁶.

3. **Pipe**: Los pipes son una herramienta de Angular que nos permite transformar visualmente la información, por ejemplo, cambiar un texto a mayúsculas o minúsculas, o darle formato de fecha y hora¹⁵. Un ejemplo de cómo usar un pipe en Angular sería el siguiente:
```typescript
let name = 'sheldon';
{{ name | uppercase }}
```
Esto transformará el texto 'sheldon' a mayúsculas¹⁶.

4. **Servicio**: Un servicio en Angular es una clase que contiene métodos y campos como una clase normal de TypeScript, pero sus métodos y campos pueden ser compartidos por componentes. Un servicio es anotado con la anotación @Injectable y se inyecta directamente en el componente que desea usarlo³. Un ejemplo de cómo crear un servicio en Angular sería el siguiente:
```typescript
ng generate service clientes
```
Esto generará el servicio llamado "ClientesService"³.

