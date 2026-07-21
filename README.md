# 🌱 PvZRModTemplate

[![NuGet](https://img.shields.io/nuget/v/RaptorRush135.PvZR.ModTemplate.svg)](https://www.nuget.org/packages/RaptorRush135.PvZR.ModTemplate)
[![.NET](https://img.shields.io/badge/.NET-6.0-512BD4)](#)
[![License](https://img.shields.io/github/license/RaptorRush135/PvZRModTemplate.svg)](LICENSE)

> A template for creating MelonLoader mods for Plants vs. Zombies™: Replanted.

## Features

- [PvZR.Sdk](https://github.com/RaptorRush135/PvZRSdk)
- VSCode support
- `.gitignore`, `.gitattributes`, `.editorconfig`

## Getting Started

### Prerequisites

- 🧰 [Git](https://git-scm.com/)
- 🧩 [.NET SDK](https://dotnet.microsoft.com/download), prefer latest stable (currently .NET 10 SDK)
- 🎮 A copy of Plants vs. Zombies™: Replanted
- 🍉 **[MelonLoader](https://github.com/LavaGang/MelonLoader)**, required mod loader.

### Installation & Updates

> [!WARNING]
> **If you are updating from v1.0.0, uninstall the old template first.**
>
> Run the **Uninstall Command** shown by:
>
> ```shell
> dotnet new uninstall
> ```
> After upgrading from **v1.0.0**, this manual uninstall is no longer necessary.

Install or update the template with:

```shell
dotnet new install RaptorRush135.PvZR.ModTemplate
```

### Usage

> (Replace `PvZRModName` & `UserName`)

```shell
dotnet new pvzr-mod -n PvZRModName --ModAuthor UserName
```

> [!IMPORTANT]  
> To configure the build see [PvZR.Sdk](https://github.com/RaptorRush135/PvZRSdk).

> [!WARNING]
> **The default Replanted installation directory (`PvzReDir`) assumes a standard Windows Steam installation:**
>
> `C:\Program Files (x86)\Steam\steamapps\common\PVZ Replanted`

If your game is installed elsewhere (e.g., different drive, or non-Steam version), you must override this path.

Set the `PvzReDir` environment variable to point to your installation directory.

## Verify setup

```
📁 <PvZRModName>/
├── 🔢 ...
└── 📁 src/
    └── 📁 <PvZRModName>/
        ├── 🧩 <PvZRModName>.slnx
        └── 📁 Core/
            ├── 📄 Core.cs
            └── ⚙️ <PvZRModName>.csproj
```

After generating the project, navigate to the directory with the solution (.slnx) (`src/<PvZRModName>`) and run:

```shell
dotnet build
```

The build should complete successfully.

On success, the built mod .dll will be automatically copied to the Mods directory.

## Open in editors

### 🟦 VS Code

Open the project folder (`src/<PvZRModName>`) using one of the following:

- Context menu: `Right-click the folder → Open with Code`

- Command line: `code .`

### 🟪 Visual Studio

Open the solution by double-clicking: `<PvZRModName>.slnx`
