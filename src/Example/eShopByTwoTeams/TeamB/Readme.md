# TeamB multiservice

## The multiservice pattern 
This solution follows the [Multiservice pattern for Microsoft Orleans](https://github.com/VincentH-Net/Orleans.Multiservice#readme); it was generated with [Modern.CSharp.Templates 3.0.0](https://www.nuget.org/packages/Modern.CSharp.Templates/3.0.0) by this command:

`dotnet new mcs-orleans-multiservice --RootNamespace InnoWvateDotNet.EShop --Multiservice TeamB --Logicalservice Catalog`

After this, the Catalog logical service [was moved to](https://github.com/VincentH-Net/Orleans.Multiservice#proof-by-example-eshop) the TeamB multiservice solution; the Basket service remains in the TeamA solution.

See the [pattern rules](https://github.com/VincentH-Net/Orleans.Multiservice#pattern-rules) for how to structure code in this solution (this will be supported by a Roslyn code analyzer in a later template version).

Use [`AddLogicalService.ps1 <name>`](AddLogicalService.ps1) to add more logical services to the solution.

## Current sample baseline
This sample currently targets:
- .NET 10
- Microsoft Orleans 10

## Running this solution
- The TeamB API host runs on `http://localhost:5113`
- TeamA's `BasketService` refreshes its checked-in `CatalogService.json` snapshot from TeamB's Swagger document at `http://localhost:5113/swagger/v1/swagger.json`
- Start TeamB before forcing a TeamA OpenAPI refresh or rebuilding TeamA after deleting its cached `CatalogService.json`
