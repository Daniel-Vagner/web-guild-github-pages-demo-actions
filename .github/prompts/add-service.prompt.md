---
description: "Add a new service with DI registration"
---
# Add Service

Create a new service following clean architecture principles:

1. Ask the user for:
   - Service purpose
   - Whether it needs async operations
   - Dependencies it requires

2. Implementation steps:
   - Create an interface in a `Services/` folder (or appropriate namespace)
   - Create the implementation class
   - Register in DI container in `Program.cs` using `AddScoped<TInterface, TImplementation>()`
   - Add XML documentation on the interface methods

3. Conventions:
   - Use `async`/`await` for I/O-bound operations
   - Suffix async methods with `Async`
   - Accept `CancellationToken` where appropriate
   - Use constructor injection for dependencies
   - Throw descriptive exceptions on failure

4. Build to verify compilation succeeds.
