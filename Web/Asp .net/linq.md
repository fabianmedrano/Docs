# LINQ:

| Operación | Descripción | Parámetros | Retorno | Ejemplo de uso |
| --- | --- | --- | --- | --- |
| Any | Verifica si una colección está vacía o si tiene al menos un elemento que cumpla con una condición especificada. | Condición especificada. | `bool` | `bool hasAdults = users.Any(u => u.Age >= 18);` |
| Select | Transforma una colección aplicando una función de mapeo a cada elemento. | Función de mapeo. | `IEnumerable<TResult>` | `var names = users.Select(u => u.Name);` |
| All | Verifica si todos los elementos de una colección cumplen con una condición especificada. | Condición especificada. | `bool` | `bool allAdults = users.All(u => u.Age >= 18);` |
| GroupBy | Agrupa los elementos de una colección en función de una clave especificada. | Clave especificada. | `IGrouping<TKey, TElement>` | `var groups = users.GroupBy(u => u.Age);` |
| First y FirstOrDefault | Devuelve el primer elemento de una secuencia que cumple con una condición especificada o un valor predeterminado si no se encuentra ningún elemento. | Condición especificada. | `TSource` o valor predeterminado. | `var firstAdult = users.First(u => u.Age >= 18);` |
| Eliminar | Elimina filas de una base de datos utilizando LINQ to SQL. | Colección relacionada con la tabla. | N/A | `context.Users.DeleteOnSubmit(user);` |
| Editar | Edita los datos en una base de datos utilizando LINQ to SQL. | Propiedades de los objetos LINQ to SQL. | N/A | `user.Name = "Nuevo nombre"; context.SubmitChanges();` |
| Agrupar | Agrupa los elementos de una colección en función de una clave especificada. | Clave especificada. | `IGrouping<TKey, TElement>` | `var groups = users.GroupBy(u => u.Age);` |
| Ordenar | Ordena los elementos de una colección en función de una clave especificada. | Clave especificada. | `IOrderedEnumerable<TSource>` | `var orderedUsers = users.OrderBy(u => u.Name);` |
| Unir | Combina elementos de dos colecciones en función de una clave especificada. | Dos colecciones y una clave especificada. | `IEnumerable<TResult>` | `var joinedData = users.Join(orders, u => u.Id, o => o.UserId, (u, o) => new { u.Name, o.OrderId });` |
| Where | Filtra una secuencia de valores en función de una condición especificada. | Condición especificada. | `IEnumerable<TSource>` | `var adults = users.Where(u => u.Age >= 18);` |
| Count | Devuelve el número de elementos en una secuencia. | N/A o condición especificada. | `int` | `int adultCount = users.Count(u => u.Age >= 18);` |
| Sum | Calcula la suma de una secuencia de valores numéricos. | Función selector. | `TResult` | `int totalAge = users.Sum(u => u.Age);` |
| Average | Calcula el promedio de una secuencia de valores numéricos. | Función selector. | `double` o `Nullable<double>` | `double averageAge = users.Average(u => u.Age);` |
| Min y Max | Devuelve el valor mínimo y máximo de una secuencia de valores, respectivamente. | Función selector. | `TResult` o valor predeterminado. | `int minAge = users.Min(u => u.Age);` |
