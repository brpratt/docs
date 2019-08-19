# Ionide

Ionide is a [Visual Studio Code](https://code.visualstudio.com/) (VS Code) package suite for cross-platform F# development.

## Overview

Ionide for VS Code is a set of 3 plugins available in the Visual Studio Marketplace.

* [Ionide-fsharp](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp) - provides F# specific features including advanced editor features (autocomplete, go-to definition, tooltips, rename, various refactorings and quick fix suggestions), integration with the .NET project system, project explorer for project file visualization and manipulation, integration with MSBuild for building and running applications, debugger integration and more.

* [Ionide-Paket](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-Paket) - provides integration with [Paket](https://fsprojects.github.io/Paket/), a package dependency manager for .NET with support for NuGet packages and GitHub repositories.

* [Ionide-FAKE](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fake) - provides integration with [FAKE](https://fake.build) (F# Make), a popular F# tool and DSL for build orchestration.

## Requirements

* Visual Studio Code - a lightweight and powerful source code editor created by Microsoft. It is available for Windows, macOS and Linux. For detailed documentation of the editor, including getting-started guides, visit the [official documentation](https://code.visualstudio.com/docs).

* F# - a mature, open-source, cross-platform, functional-first programming language. It empowers users and organizations to tackle complex computing problems with simple, maintainable and robust code. Ionide supports any version of F# >= 3.0 but we do recommend using F# 4.1 or above. Detailed installation instructions can be found on the F# Software foundation webpage - for [Windows](http://fsharp.org/use/windows/), [macOS](http://fsharp.org/use/mac/), and [Linux](http://fsharp.org/use/linux/)

* .NET Core SDK - .NET Core is a lightweight, cross-platform, modern implementation of .NET. We strongly recommend installing it since some advanced Ionide features such as debugging and project scaffolding depends on the .NET Core SDK and `dotnet` CLI tooling even if your application is targetting .NET Framework ("Full Framework"). For detailed instructions on installing .NET Core, visit the [official step-by-step installation guide](https://www.microsoft.com/net/core)

* VS Code C# plugin (optional) - Ionide's debugging capabilities relies on the debugger provided by the [OmniSharp](http://www.omnisharp.net) team. To get it, install the [C# extension from the VS Code marketplace](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp)

* MSBuild 2015 (Windows only, optional) - For old, verbose `.fsproj` files on Windows, MSBuild 2015 (14.0) needs to be additionally installed. You can download it [here](https://www.microsoft.com/en-us/download/details.aspx?id=48159). However, we highly recommend using new, SDK-based project files.

## Plugin installation

Any VS Code extension can be installed using the UI inside VS Code. Bring up the Extensions view by clicking on the Extensions icon in the Activity Bar on the side of VS Code or the `View: Extensions` command (`Ctrl+Shift+X`). Then, in the search box, type `Ionide` to find all 3 extensions we provide. Click the `Install` button and after a successful install you'll see a `Reload` button which will prompt you to restart VS Code to enable the new extension. For more detailed information about plugin installation, visit the [VS Code documentation](https://code.visualstudio.com/docs/editor/extension-gallery)

## Plugin activation

VS Code plugins run in external processes (which means they should never impact editor performance) and are activated lazily when certain activation events occur. This means that plugins are not loaded unnecessarily when you work on projects in other programming environments.

Ionide plugins are activated when:

* Any workspace is opened which contains an `.fsproj`, `.fs`, or `.fsx` file

* A new `.fsproj`, `.fs`, or `.fsx` file is created in the current workspace
