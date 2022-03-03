# DnetBlazor
Blazor component library. All components are written in C#. Only 6kb of js related to components.

### Demo
https://www.datalnet.com

### Compatibility
.Net 6.0. Updated to 6.0.2

Server-side Blazor and client-side Blazor

## Using the library
### Installation

1. Install Nuget package Dnet.Blazor
2. Add the following script reference to your Index.html(WASM) or _Host.cshtml (Blazor Server): 

```Html
<script src="_content/Dnet.Blazor/rxjs.min.js"></script>
<script src="_content/Dnet.Blazor/dnet-blazor.js"></script>
```

3. Add the following link reference Index.html (WASM) or _Host.cshtml (Blazor Server): 

```Html
<link href="_content/Dnet.Blazor/dnet-blazor-styles.css" rel="stylesheet" />
```

4. Add the following to the MainLayout.razor

```CSharp
<DnetOverlay BaseZindex="1100"></DnetOverlay>
```
Many of the components in the library are based on the Dnet.Blazor.Overlay component. The overlay provides a way to open floating panels on the screen. Manages positioning, zindex, backdrops, etc. 

BaseZindex: Base z-index use by the Overlay component to display components on the screen. Providing this guarantees that components will open with the correct z-index.

4. Add the following to the Program.cs
```CSharp
using Dnet.Blazor.Infrastructure.Services;
```
```CSharp
builder.Services.AddDnetBlazor();
```



 
