# Asp.net


1. **HttpPost**: Puedes decorar una acción del controlador con el atributo `[HttpPost]` para indicar que esta acción debe ser invocada cuando se envía un formulario HTTP POST. Luego, puedes usar el modelo de vista (ViewModel) como parámetro en esta acción para recibir los datos del formulario. Aquí tienes un ejemplo:

```csharp
[HttpPost]
public ActionResult MiAccion(MiViewModel model)
{
    // Tu código aquí
}
```

2. **FormCollection**: Otra opción es usar la clase `FormCollection` como parámetro en tu acción. Esta clase contiene todos los datos del formulario enviados en la solicitud HTTP. Aquí tienes un ejemplo:

```csharp
[HttpPost]
public ActionResult MiAccion(FormCollection form)
{
    string valor = form["miCampo"];
    // Tu código aquí
}
```

3. **Bind Attribute**: Si sólo necesitas algunos campos específicos del formulario, puedes usar el atributo `[Bind]` para especificar qué campos del modelo quieres enlazar. Aquí tienes un ejemplo:

```csharp
[HttpPost]
public ActionResult MiAccion([Bind(Include = "Campo1,Campo2")] MiViewModel model)
{
    // Tu código aquí
}
```

Espero que esto te ayude a entender cómo puedes enviar datos de un formulario al controlador en ASP.NET MVC. Si tienes más preguntas, no dudes en preguntar.
