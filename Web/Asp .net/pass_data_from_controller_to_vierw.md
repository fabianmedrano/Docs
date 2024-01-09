

```markdown
# Pasar datos del controlador a la vista en ASP.NET Core MVC

En ASP.NET Core MVC, existen varias formas de pasar datos del controlador a la vista. Aquí te menciono algunas:

## Modelo de vista fuertemente tipado

Puedes crear una clase de modelo de vista que contenga todas las propiedades que necesitas pasar a la vista. Luego, puedes pasar una instancia de esta clase al método `View()`. Por ejemplo:

```csharp
public class MiModeloDeVista
{
    public List<PlanHistory> PlanHistory { get; set; }
    public Plan Plan { get; set; }
    // otras propiedades
}
```

Y luego en tu acción del controlador:

```csharp
var modelo = new MiModeloDeVista
{
    PlanHistory = await _context.PlanHistory.Where(plan => plan.Id == id).Include(a => a.Plan).ToListAsync(),
    Plan = await _context.Plan.FirstOrDefaultAsync(m => m.Id == id)
};
return View(modelo);
```

## ViewData o ViewBag

`ViewData` es un diccionario que te permite pasar datos al método `View()`. `ViewBag` es un contenedor dinámico que también puedes usar para pasar datos a la vista. Por ejemplo:

```csharp
ViewData["PlanHistory"] = await _context.PlanHistory.Where(plan => plan.Id == id).Include(a => a.Plan).ToListAsync();
ViewBag.Plan = await _context.Plan.FirstOrDefaultAsync(m => m.Id == id);
return View();
```

## Tuplas

Si solo necesitas pasar unas pocas propiedades y no quieres crear una clase de modelo de vista completa, puedes usar una tupla. Por ejemplo:

```csharp
var planHistory = await _context.PlanHistory.Where(plan => plan.Id == id).Include(a => a.Plan).ToListAsync();
var plan = await _context.Plan.FirstOrDefaultAsync(m => m.Id == id);
return View((PlanHistory: planHistory, Plan: plan));
```


