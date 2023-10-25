# Anotaciones de validación

1. **Required Attribute**: Especifica que el valor de la propiedad es obligatorio.
```csharp
public class MiClase
{
    [Required]
    public string Nombre { get; set; }
}
```

2. **MaxLength Attribute**: Establece la longitud máxima permitida del valor de la propiedad (cadena o matriz).
```csharp
public class MiClase
{
    [MaxLength(50)]
    public string Nombre { get; set; }
}
```

3. **MinLength Attribute**: Establece la longitud mínima permitida del valor de la propiedad (cadena o matriz).
```csharp
public class MiClase
{
    [MinLength(5)]
    public string NombreUsuario { get; set; }
}
```

4. **StringLength Attribute**: Establece la longitud máxima permitida del valor de la propiedad (cadena).
```csharp
public class MiClase
{
    [StringLength(50)]
    public string NombreUsuario { get; set; }
}
```

5. **CompareAttribute**: Proporciona un atributo que compara dos propiedades.
```csharp
public class RegistroModelo
{
    [Required]
    [DataType(DataType.Password)]
    public string Password { get; set; }

    [DataType(DataType.Password)]
    [Compare("Password")]
    public string ConfirmPassword { get; set; }
}
```

6. **RangeAttribute**: Especifica las restricciones del rango numérico para el valor del campo.
```csharp
public class ProductoModelo
{
    [Range(1, 100)]
    public int Cantidad { get; set; }
}
```

7. **RegularExpressionAttribute**: Especifica que el valor del campo debe coincidir con la expresión regular especificada.
```csharp
public class RegistroModelo
{
    [RegularExpression(@"^[a-zA-Z]+$", ErrorMessage = "Solo se permiten letras.")]
    public string NombreUsuario { get; set; }
}
```

8. **EmailAddressAttribute**: Valida una dirección de correo electrónico.
```csharp
public class RegistroModelo
{
    [EmailAddress]
    public string Email { get; set; }
}
```

9. **PhoneAttribute**: Especifica que el valor del campo es un número telefónico bien formado.
```csharp
public class ContactoModelo
{
    [Phone]
    public string NumeroTelefono { get; set; }
}
```

10. **CreditCardAttribute**: Valida un número de tarjeta de crédito.
```csharp
public class PagoModelo
{
    [CreditCard]
    public string NumeroTarjeta { get; set; }
}
```

11. **CompareAttribute**: Proporciona un atributo que compara dos propiedades.
```csharp
public class RegistroModelo
{
    [Required]
    [DataType(DataType.Password)]
    public string Password { get; set; }

    [DataType(DataType.Password)]
    [Compare("Password")]
    public string ConfirmPassword { get; set; }
}
```

12. **CreditCardAttribute**: Especifica que el valor de un campo de datos es un número de tarjeta de crédito.
```csharp
public class PagoModelo
{
    [CreditCard]
    public string NumeroTarjeta { get; set; }
}
```

13. **CustomValidationAttribute**: Especifica un método de validación personalizado que se utiliza para validar una propiedad o instancia de clase². Este atributo requiere la implementación de un método personalizado para la validación.

14. **DataTypeAttribute**: Especifica el nombre de un tipo adicional para asociar con un campo de datos.
```csharp
public class UsuarioModelo
{
    [DataType(DataType.EmailAddress)]
    public string Email { get; set; }
}
```

15. **EmailAddressAttribute**: Valida una dirección de correo electrónico.
```csharp
public class RegistroModelo
{
    [EmailAddress]
    public string Email { get; set; }
}
```

16. **EnumDataTypeAttribute**: Permite que una enumeración .NET se asocie a una columna de datos.
```csharp
public enum Generos 
{ 
   Masculino, 
   Femenino 
}

public class UsuarioModelo 
{ 
   [EnumDataType(typeof(Generos))] 
   public Generos Genero { get; set; } 
}
```

17. **FileExtensionsAttribute**: Valida las extensiones de nombre de archivo.
```csharp
public class ArchivoModelo
{
    [FileExtensions(Extensions = "jpg,jpeg,png")]
    public IFormFile Archivo { get; set; }
}
```

18. **MaxLengthAttribute**: Establece la longitud máxima permitida del valor de la propiedad (cadena o matriz).
```csharp
public class UsuarioModelo
{
    [MaxLength(50)]
    public string Nombre { get; set; }
}
```

19. **MinLengthAttribute**: Establece la longitud mínima permitida del valor de la propiedad (cadena o matriz).
```csharp
public class UsuarioModelo
{
    [MinLength(5)]
    public string NombreUsuario { get; set; }
}
```

20. **PhoneAttribute**: Especifica que el valor del campo es un número telefónico bien formado.
```csharp
public class ContactoModelo
{
    [Phone]
    public string NumeroTelefono { get; set; }
}
```

21. **RangeAttribute**: Especifica las restricciones del rango numérico para el valor del campo.
```csharp
public class ProductoModelo
{
    [Range(1, 100)]
    public int Cantidad { get; set; }
}
```

22. **RegularExpressionAttribute**: Especifica que el valor del campo debe coincidir con la expresión regular especificada.
```csharp
public class RegistroModelo
{
    [RegularExpression(@"^[a-zA-Z]+$", ErrorMessage = "Solo se permiten letras.")]
    public string NombreUsuario { get; set; }
}
```

23. **RequiredAttribute**: Especifica que el valor de la propiedad es obligatorio.
```csharp
public class UsuarioModelo
{
    [Required]
    public string NombreUsuario { get; set; }
}
```

24. **StringLengthAttribute**: Establece la longitud máxima permitida del valor de la propiedad (cadena).
```csharp
public class UsuarioModelo
{
    [StringLength(50)]
    public string NombreUsuario { get; set; }
}
```

# Atributos de presentación 

1. **DataTypeAttribute**: Especifica el nombre de un tipo adicional para asociar con un campo de datos.
```csharp
public class UsuarioModelo
{
    [DataType(DataType.EmailAddress)]
    public string Email { get; set; }
}
```

2. **DisplayAttribute**: Proporciona un atributo que te permite especificar cadenas localizables para tipos y miembros de clases parciales de entidad.
```csharp
public class UsuarioModelo
{
    [Display(Name = "Correo Electrónico")]
    public string Email { get; set; }
}
```

3. **DisplayFormatAttribute**: Especifica cómo se muestran y formatean los campos de datos por ASP.NET Dynamic Data.
```csharp
public class ProductoModelo
{
    [DisplayFormat(DataFormatString = "{0:C}")]
    public decimal Precio { get; set; }
}
```

4. **EditableAttribute**: Indica si un campo de datos es editable.
```csharp
public class UsuarioModelo
{
    [Editable(false)]
    public string Id { get; set; }
}
```

5. **UIHintAttribute**: Proporciona una pista sobre la forma en que se debe mostrar un campo de datos¹. Este atributo no está disponible en .NET Core y .NET 5¹.



6. **CompareAttribute**: Proporciona un atributo que compara dos propiedades.
```csharp
public class RegistroModelo
{
    [Required]
    [DataType(DataType.Password)]
    public string Password { get; set; }

    [DataType(DataType.Password)]
    [Compare("Password")]
    public string ConfirmPassword { get; set; }
}
```

7. **CreditCardAttribute**: Especifica que el valor de un campo de datos es un número de tarjeta de crédito.
```csharp
public class PagoModelo
{
    [CreditCard]
    public string NumeroTarjeta { get; set; }
}
```

8. **CustomValidationAttribute**: Especifica un método de validación personalizado que se utiliza para validar una propiedad o instancia de clase². Este atributo requiere la implementación de un método personalizado para la validación.

9. **DataTypeAttribute**: Especifica el nombre de un tipo adicional para asociar con un campo de datos.
```csharp
public class UsuarioModelo
{
    [DataType(DataType.EmailAddress)]
    public string Email { get; set; }
}
```

10. **EmailAddressAttribute**: Valida una dirección de correo electrónico.
```csharp
public class RegistroModelo
{
    [EmailAddress]
    public string Email { get; set; }
}
```

11. **EnumDataTypeAttribute**: Permite que una enumeración .NET se asocie a una columna de datos.
```csharp
public enum Generos 
{ 
   Masculino, 
   Femenino 
}

public class UsuarioModelo 
{ 
   [EnumDataType(typeof(Generos))] 
   public Generos Genero { get; set; } 
}
```

12. **FileExtensionsAttribute**: Valida las extensiones de nombre de archivo.
```csharp
public class ArchivoModelo
{
    [FileExtensions(Extensions = "jpg,jpeg,png")]
    public IFormFile Archivo { get; set; }
}
```

13. **MaxLengthAttribute**: Establece la longitud máxima permitida del valor de la propiedad (cadena o matriz).
```csharp
public class UsuarioModelo
{
    [MaxLength(50)]
    public string Nombre { get; set; }
}
```

14. **MinLengthAttribute**: Establece la longitud mínima permitida del valor de la propiedad (cadena o matriz).
```csharp
public class UsuarioModelo
{
    [MinLength(5)]
    public string NombreUsuario { get; set; }
}
```

15. **PhoneAttribute**: Especifica que el valor del campo es un número telefónico bien formado.
```csharp
public class ContactoModelo
{
    [Phone]
    public string NumeroTelefono { get; set; }
}
```

16. **RangeAttribute**: Especifica las restricciones del rango numérico para el valor del campo.
```csharp
public class ProductoModelo
{
    [Range(1, 100)]
    public int Cantidad { get; set; }
}
```

17. **RegularExpressionAttribute**: Especifica que el valor del campo debe coincidir con la expresión regular especificada.
```csharp
public class RegistroModelo
{
    [RegularExpression(@"^[a-zA-Z]+$", ErrorMessage = "Solo se permiten letras.")]
    public string NombreUsuario { get; set; }
}
```

18. **RequiredAttribute**: Especifica que el valor de la propiedad es obligatorio.
```csharp
public class UsuarioModelo
{
    [Required]
    public string NombreUsuario { get; set; }
}
```

19. **StringLengthAttribute**: Establece la longitud máxima permitida del valor de la propiedad (cadena).
```csharp
public class UsuarioModelo
{
    [StringLength(50)]
    public string NombreUsuario { get; set; }
}
```


