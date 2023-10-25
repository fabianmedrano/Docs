
# Anotaciones de relación 

1. **[ForeignKey]**: Esta anotación se utiliza para establecer una relación de clave externa con otra entidad¹².
```csharp
public class Order
{
    public int OrderId { get; set; }
    public string Product { get; set; }

    [ForeignKey("Customer")]
    public int CustomerId { get; set; }
    public Customer Customer { get; set; }
}
```
En este ejemplo, la propiedad `CustomerId` en la entidad `Order` tiene una relación de clave externa con la entidad `Customer`.

2. **[InverseProperty]**: Esta anotación se utiliza para denotar el extremo inverso de una relación cuando hay más de una relación entre dos entidades¹.
```csharp
public class Post
{
    public int PostId { get; set; }
    public string Title { get; set; }

    [InverseProperty("WrittenPosts")]
    public User Author { get; set; }

    [InverseProperty("EditedPosts")]
    public User Editor { get; set; }
}
```
En este ejemplo, la entidad `Post` tiene dos relaciones con la entidad `User`: una para el autor del post y otra para el editor.

3. **[Required]**: Aunque no es específicamente una anotación de relación, se utiliza a menudo en relaciones para indicar que una entidad no puede existir sin una entidad relacionada¹.
```csharp
public class Order
{
    public int OrderId { get; set; }

    [Required]
    public string Product { get; set; }
}
```
En este ejemplo, cada `Order` debe tener un `Product`.

4. **[Navigation Property]**: Las propiedades de navegación proporcionan una manera de navegar y administrar las relaciones en ambas direcciones².
```csharp
public class Blog 
{
    public int BlogId { get; set; }
    public string Name { get; set; }

    public virtual ICollection<Post> Posts { get; set; }
}
```
En este ejemplo, la propiedad `Posts` en la entidad `Blog` es una propiedad de navegación que permite acceder a todos los posts asociados a un blog en particular.

----
----

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

------
------


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

------
------


# Anotaciones personalizada

 Para crear una anotación de validación personalizada, debes crear una clase que herede de `ValidationAttribute` y sobrescribir el método `IsValid`.

```csharp
public class StringLengthRangeAttribute : ValidationAttribute
{
    public int Minimum { get; set; }
    public int Maximum { get; set; }

    public StringLengthRangeAttribute()
    {
        this.Minimum = 0;
        this.Maximum = int.MaxValue;
    }

    public override bool IsValid(object value)
    {
        string strValue = value as string;
        if (!string.IsNullOrEmpty(strValue))
        {
            int len = strValue.Length;
            return len >= this.Minimum && len <= this.Maximum;
        }
        return true;
    }
}
```

En este ejemplo, `StringLengthRangeAttribute` es una anotación personalizada que valida que la longitud de una cadena esté dentro de un rango especificado. Puedes usarlo en tu modelo de la siguiente manera:

```csharp
public class MiModelo
{
    [StringLengthRange(Minimum = 5, Maximum = 100)]
    public string MiPropiedad { get; set; }
}
```

Este código garantiza que el valor de `MiPropiedad` tenga al menos 5 caracteres y no más de 100 caracteres⁴.


