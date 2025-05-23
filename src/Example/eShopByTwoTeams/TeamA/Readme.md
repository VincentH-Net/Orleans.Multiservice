﻿# TeamA multiservice

## The multiservice pattern 
This solution follows the [Multiservice pattern for Microsoft Orleans](https://github.com/VincentH-Net/Orleans.Multiservice#readme); it was generated with [Modern.CSharp.Templates 3.0.0](https://www.nuget.org/packages/Modern.CSharp.Templates/3.0.0) by this command:

`dotnet new mcs-orleans-multiservice --RootNamespace InnoWvateDotNet.EShop --Multiservice TeamA --Logicalservice Catalog`

The `BasketService` was added with this PowerShell command:

`.\AddLogicalService.ps1 Basket`

After this, the Catalog logical service [was moved to](https://github.com/VincentH-Net/Orleans.Multiservice#proof-by-example-eshop) the TeamB multiservice solution; the Basket service remains in the TeamA solution.

See the [pattern rules](https://github.com/VincentH-Net/Orleans.Multiservice#pattern-rules) for how to structure code in this solution (this will be supported by a Roslyn code analyzer in a later template version).

Use [`AddLogicalService.ps1 <name>`](AddLogicalService.ps1) to add more logical services to the solution.