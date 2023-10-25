`DataAnnotations.Schema`:

1. **Table Attribute**: Especifica a qué tabla de la base de datos se asigna una clase.
```csharp
[Table("MiTabla")]
public class MiClase
{
    //...
}
```

2. **Column Attribute**: Especifica a qué columna de la base de datos se asigna una propiedad.
```csharp
public class MiClase
{
    [Column("Id")]
    public int MiClaseId { get; set; }
    //...
}
```

3. **Complex Type Attribute**: Denota que una clase es un tipo complejo.
```csharp
[ComplexType]
public class Direccion
{
    public string Calle { get; set; }
    public string Ciudad { get; set; }
    //...
}
```

4. **Database Generated Attribute**: Especifica cómo la base de datos genera valores para una propiedad.
```csharp
public class MiClase
{
    [DatabaseGenerated(DatabaseGeneratedOption.Identity)]
    public int MiClaseId { get; set; }
    //...
}
```

5. **Foreign Key Attribute**: Denota una propiedad utilizada como clave foránea en una relación.
```csharp
public class MiOtraClase
{
    public int MiOtraClaseId { get; set; }

    [ForeignKey("MiClase")]
    public int MiClaseId { get; set; }
    public MiClase MiClase { get; set; }
}
```

6. **Inverse Property Attribute**: Especifica el inverso de una propiedad de navegación que representa el otro extremo de la misma relación.
```csharp
public class MiClase
{
    public int MiClaseId { get; set; }

    [InverseProperty("MiClase")]
    public ICollection<MiOtraClase> OtrasClases { get; set; }
}
```

7. **Not Mapped Attribute**: Denota que una propiedad o clase debe ser excluida del mapeo de la base de datos.
```csharp
public class MiClase
{
    [NotMapped]
    public string PropiedadNoMapeada { get; set; }
}
```
`System.ComponentModel.DataAnnotations` 
1. **Key Attribute**: Identifica una o más propiedades como una clave.
```csharp
public class MiClase
{
    [Key]
    public int MiClaseId { get; set; }
    //...
}
```

2. **Required Attribute**: Especifica que el valor de la propiedad es obligatorio.
```csharp
public class MiClase
{
    [Required]
    public string Nombre { get; set; }
    //...
}
```

3. **MaxLength Attribute**: Establece la longitud máxima permitida del valor de la propiedad (cadena o matriz).
```csharp
public class MiClase
{
    [MaxLength(50)]
    public string Nombre { get; set; }
    //...
}
```

4. **StringLength Attribute**: Establece la longitud máxima permitida del valor de la propiedad (cadena).
```csharp
public class MiClase
{
    [StringLength(50)]
    public string Nombre { get; set; }
    //...
}
```

5. **ConcurrencyCheck Attribute**: Especifica que la propiedad se incluye en las comprobaciones de concurrencia.
```csharp
public class MiClase
{
    [ConcurrencyCheck]
    public int Version { get; set; }
    //...
}
```

6. **Timestamp Attribute**: Especifica el tipo de datos de la columna de la base de datos como `rowversion`.
```csharp
public class MiClase
{
    [Timestamp]
    public byte[] RowVersion { get; set; }
    //...
}
```

1. **Key Attribute**: Identifica una o más propiedades como una clave.
```csharp
public class MiClase
{
    [Key]
    public int MiClaseId { get; set; }
}
```

2. **Required Attribute**: Especifica que el valor de la propiedad es obligatorio.
```csharp
public class MiClase
{
    [Required]
    public string Nombre { get; set; }
}
```

3. **MaxLength Attribute**: Establece la longitud máxima permitida del valor de la propiedad (cadena o matriz).
```csharp
public class MiClase
{
    [MaxLength(50)]
    public string Nombre { get; set; }
}
```

4. **StringLength Attribute**: Establece la longitud máxima permitida del valor de la propiedad (cadena).
```csharp
public class MiClase
{
    [StringLength(50)]
    public string Nombre { get; set; }
}
```

5. **ConcurrencyCheck Attribute**: Especifica que la propiedad se incluye en las comprobaciones de concurrencia.
```csharp
public class MiClase
{
    [ConcurrencyCheck]
    public int Version { get; set; }
}
```

6. **Timestamp Attribute**: Especifica el tipo de datos de la columna de la base de datos como `rowversion`.
```csharp
public class MiClase
{
    [Timestamp]
    public byte[] RowVersion { get; set; }
}
```

7. **CompareAttribute**: Proporciona un atributo que compara dos propiedades.
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

8. **RangeAttribute**: Especifica las restricciones del rango numérico para el valor del campo.
```csharp
public class ProductoModelo
{
    [Range(1, 100)]
    public int Cantidad { get; set; }
}
```

9. **RegularExpressionAttribute**: Especifica que el valor del campo debe coincidir con la expresión regular especificada.
```csharp
public class RegistroModelo
{
    [RegularExpression(@"^[a-zA-Z]+$", ErrorMessage = "Solo se permiten letras.")]
    public string NombreUsuario { get; set; }
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

11. **CreditCardAttribute**: Valida un número de tarjeta de crédito.
```csharp
public class PagoModelo
{
    [CreditCard]
    public string NumeroTarjeta { get; set; }
}
```

12. **PhoneAttribute**: Valida un número telefónico.
```csharp
public class ContactoModelo
{
    [Phone]
    public string NumeroTelefono { get; set; }
}
```

13. **UrlAttribute**: Valida una URL.
```csharp
public class SitioWebModelo
{
    [Url]
    public string Url { get; set; }
}
```

14. **DataTypeAttribute**: Especifica el tipo de datos adicional para asociar con un campo de datos.
```csharp
public class UsuarioModelo
{
    [DataType(DataType.EmailAddress)]
    public string Email { get; set; }
}
```

15. **DisplayAttribute**: Proporciona un atributo que te permite especificar cadenas localizables para tipos y miembros de clases parciales de entidad.
```csharp
public class UsuarioModelo
{
    [Display(Name = "Correo Electrónico")]
    public string Email { get; set; }
}
```

16. **DisplayFormatAttribute**: Especifica cómo se muestran y formatean los campos de datos por ASP.NET Dynamic Data.
```csharp
public class ProductoModelo
{
    [DisplayFormat(DataFormatString = "{0:C}")]
    public decimal Precio { get; set; }
}
```

17. **EditableAttribute**: Indica si un campo de datos es editable.
```csharp
public class UsuarioModelo
{
    [Editable(false)]
    public string Id { get; set; }
}
```

18. **EnumDataTypeAttribute**: Permite que una enumeración .NET se asocie a una columna de datos.
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

19. **FileExtensionsAttribute**: Valida las extensiones de nombre de archivo.
```csharp
public class ArchivoModelo
{
    [FileExtensions(Extensions = "jpg,jpeg,png")]
    public IFormFile Archivo { get; set; }
}
```

20. **MaxLengthAttribute**: Establece la longitud máxima permitida del valor de la propiedad (cadena o matriz).
```csharp
public class UsuarioModelo
{
    [MaxLength(50)]
    public string Nombre { get; set; }
}
```

21. **MinLengthAttribute**: Establece la longitud mínima permitida del valor de la propiedad (cadena o matriz).
```csharp
public class UsuarioModelo
{
    [MinLength(5)]
    public string NombreUsuario { get; set; }
}
```

22. **RequiredAttribute**: Especifica que el valor de la propiedad es obligatorio.
```csharp
public class UsuarioModelo
{
    [Required]
    public string NombreUsuario { get; set; }
}
```

23. **StringLengthAttribute**: Establece la longitud máxima permitida del valor de la propiedad (cadena).
```csharp
public class UsuarioModelo
{
    [StringLength(50)]
    public string NombreUsuario { get; set; }
}
```

24. **ScaffoldColumnAttribute**: Especifica si una clase o columna utiliza andamios.
```csharp
public class UsuarioModelo
{
    [ScaffoldColumn(false)]
    public string Id { get; set; }
}
```

1. **AllowedValuesAttribute**: Especifica una lista de valores que deben permitirse en una propiedad. Este atributo no está disponible en .NET Core y .NET 5².

2. **AssociatedMetadataTypeTypeDescriptionProvider**: Extiende la información de metadatos para una clase agregando atributos e información de propiedad que se define en una clase asociada. Este atributo se usa principalmente en el código de infraestructura y no se aplica directamente a las propiedades del modelo².

3. **AssociationAttribute**: Especifica que un miembro de entidad representa una relación de datos, como una relación de clave externa². Este atributo no está disponible en .NET Core y .NET 5².

4. **Base64StringAttribute**: Especifica que el valor de un campo de datos es una cadena Base64 bien formada². Este atributo no está disponible en .NET Core y .NET 5².

5. **BindableTypeAttribute**: Especifica si un tipo se usa normalmente para la vinculación². Este atributo no está disponible en .NET Core y .NET 5².

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

7. **ConcurrencyCheckAttribute**: Especifica que la propiedad se incluye en las comprobaciones de concurrencia.
```csharp
public class MiClase
{
    [ConcurrencyCheck]
    public int Version { get; set; }
}
```

8. **CreditCardAttribute**: Especifica que el valor de un campo de datos es un número de tarjeta de crédito.
```csharp
public class PagoModelo
{
    [CreditCard]
    public string NumeroTarjeta { get; set; }
}
```

9. **CustomValidationAttribute**: Especifica un método de validación personalizado que se utiliza para validar una propiedad o instancia de clase². Este atributo requiere la implementación de un método personalizado para la validación.

10. **DataTypeAttribute**: Especifica el nombre de un tipo adicional para asociar con un campo de datos.
```csharp
public class UsuarioModelo
{
    [DataType(DataType.EmailAddress)]
    public string Email { get; set; }
}
```

11. **DeniedValuesAttribute**: Especifica una lista de valores que no deben permitirse en una propiedad². Este atributo no está disponible en .NET Core y .NET 5².

12. **DisplayAttribute**: Proporciona un atributo que te permite especificar cadenas localizables para tipos y miembros de clases parciales de entidad.
```csharp
public class UsuarioModelo
{
    [Display(Name = "Correo Electrónico")]
    public string Email { get; set; }
}
```

13. **DisplayColumnAttribute**: Especifica la columna que se muestra en la tabla referida como columna de clave externa². Este atributo no está disponible en .NET Core y .NET 5².

14. **DisplayFormatAttribute**: Especifica cómo se muestran y formatean los campos de datos por ASP.NET Dynamic Data.
```csharp
public class ProductoModelo
{
    [DisplayFormat(DataFormatString = "{0:C}")]
    public decimal Precio { get; set; }
}
```

15. **EditableAttribute**: Indica si un campo de datos es editable.
```csharp
public class UsuarioModelo
{
    [Editable(false)]
    public string Id { get; set; }
}
```

16. **EmailAddressAttribute**: Valida una dirección de correo electrónico.
```csharp
public class RegistroModelo
{
    [EmailAddress]
    public string Email { get; set; }
}
```

17. **EnumDataTypeAttribute**: Permite que una enumeración .NET se asocie a una columna de datos.
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

18. **FileExtensionsAttribute**: Valida las extensiones de nombre de archivo.
```csharp
public class ArchivoModelo
{
    [FileExtensions(Extensions = "jpg,jpeg,png")]
    public IFormFile Archivo { get; set; }
}
```

19. **FilterUIHintAttribute**: Representa un atributo que se utiliza para especificar el comportamiento de filtrado para una columna². Este atributo no está disponible en .NET Core y .NET 5².

20. **KeyAttribute**: Denota una o más propiedades que identifican únicamente a una entidad.
```csharp
public class MiClase
{
    [Key]
    public int MiClaseId { get; set; }
}
```

21. **LengthAttribute**: Especifica la longitud mínima y máxima permitida para los datos de colección/cadena en una propiedad². Este atributo no está disponible en .NET Core y .NET 5².

22. **MaxLengthAttribute**: Establece la longitud máxima permitida del valor de la propiedad (cadena o matriz).
```csharp
public class UsuarioModelo
{
    [MaxLength(50)]
    public string Nombre { get; set; }
}
```

23. **MetadataTypeAttribute**: Especifica la clase de metadatos para asociar con una clase modelo de datos². Este atributo se usa principalmente en el código de infraestructura y no se aplica directamente a las propiedades del modelo².

24. **MinLengthAttribute**: Establece la longitud mínima permitida del valor de la propiedad (cadena o matriz).
```csharp
public class UsuarioModelo
{
    [MinLength(5)]
    public string NombreUsuario { get; set; }
}
```

25. **PhoneAttribute**: Especifica que el valor del campo es un número telefónico bien formado.
```csharp
public class ContactoModelo
{
    [Phone]
    public string NumeroTelefono { get; set; }
}
```

26. **RangeAttribute**: Especifica las restricciones del rango numérico para el valor del campo.
```csharp
public class ProductoModelo
{
    [Range(1, 100)]
    public int Cantidad { get; set; }
}
```

27. **RegularExpressionAttribute**: Especifica que el valor del campo debe coincidir con la expresión regular especificada.
```csharp
public class RegistroModelo
{
    [RegularExpression(@"^[a-zA-Z]+$", ErrorMessage = "Solo se permiten letras.")]
    public string NombreUsuario { get; set; }
}
```

28. **RequiredAttribute**: Especifica que el valor de la propiedad es obligatorio.
```csharp
public class UsuarioModelo
{
    [Required]
    public string NombreUsuario { get; set; }
}
```

29. **StringLengthAttribute**: Establece la longitud máxima permitida del valor de la propiedad (cadena).
```csharp
public class UsuarioModelo
{
    [StringLength(50)]
    public string NombreUsuario { get; set; }
}
```

30. **ScaffoldColumnAttribute**: Especifica si una clase o columna utiliza andamios.
```csharp
public class UsuarioModelo
{
    [ScaffoldColumn(false)]
    public string Id { get; set; }
}
```




