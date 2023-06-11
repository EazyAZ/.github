## Architectural pattern for .NET Web applications

Creating Web **A**pplications referencing a **B**usiness and a **C**ore projects should be as easy as **ABC**.

- **A**pplications (.NET)
  - MVC.
  - Razor Pages.
  - Web Api.
  - Blazor Server.
  - Blazor WASM.
- **B**usiness 
  - Services.
- **C**ore
  - Configuration, Constants.
  - Entities, Enums, Models.
  - Extensions, Helpers.
  - Interfaces (Ex: `I...Service`).

## Structure and dependencies

- The **A**pplication project has a dependency on the **B**usiness project which has a dependency on the **C**ore project.

## Program

`Program.cs` in the **A**pplication is in charge of:

- Add Logging provider:
  - Ex: `builder.AddSerilog();`
- Adding dependency injection: 
  - Ex: **B**usiness Services `builder.Services.AddBusinessServices();`.
- Bind `App` section to the **C**ore `Configuration.AppSettings`. 
  - Ex: `ConfigureAppSettingsSection(builder.Configuration);`.

Have fun 🍿 and create magical 🧙 apps.

> " What is conceived well is expressed clearly. " - *Nicolas Boileau, French writer.*  
" Ce que l'on conçoit bien s'énonce clairement, et les mots pour le dire arrivent aisément. "
