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
