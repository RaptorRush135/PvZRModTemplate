# 🌱 PvZRModTemplate

> A template for creating MelonLoader mods for Plants vs. Zombies™: Replanted.

## Features

- VSCode support
- Common Polyfills
- Generated ModInfo class
- Auto copy dll to Mods folder
- Release build script
- `.gitignore`, `.gitattributes`, `.editorconfig`
- Analyzers: `StyleCop`, `Sonar`, `Roslynator`

## Getting Started

### Prerequisites

- 🧰 [Git](https://git-scm.com/)
- 🧩 [.NET SDK](https://dotnet.microsoft.com/download), prefer latest stable (currently .NET 10 SDK)
- 🎮 A copy of Plants vs. Zombies™: Replanted
- 🍉 **[MelonLoader](https://github.com/LavaGang/MelonLoader)** - required mod loader.

### Installation

#### First install

```shell
git clone https://github.com/RaptorRush135/PvZRModTemplate.git
cd PvZRModTemplate
dotnet new install ./
```

#### Update

```shell
git pull
dotnet new install ./ --force
```

### Usage

> (Replace `PvZRModName` & `UserName`)

```shell
dotnet new pvzr-mod -n PvZRModName --ModAuthor UserName
```

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

After generating the project, navigate to the `src/<PvZRModName>` directory and run:

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
