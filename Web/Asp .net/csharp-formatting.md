# caracteres de escape

### salto de linea
```csharp
  Console.WriteLine("Hello\nworld"); 
```

### tabulacion
```csharp
  Console.WriteLine("Hello\t \"world\"");
```
### comillas 
```csharp
Console.WriteLine("c:\\source\\repos"); 
```

## Literal de cadena textual

Un literal de cadena textual conservará todos los espacios en blanco y los caracteres sin necesidad de usar una secuencia de escape para la barra diagonal inversa. Para crear una cadena textual, use la directiva ´@´ antes de la cadena literal.

## Caracteres de escape Unicode

```html
\u
```
```csharp
Console.WriteLine("\u3053\u3093\u306B\u3061\u306F World!");
```
