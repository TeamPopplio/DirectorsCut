<div align="center">
  <a href="https://github.com/DirectorsCutMod/DirectorsCut" title="Director's Cut"><img width="400px" height="77px" alt="Director's Cut logo" src="https://i.imgur.com/71ceAUU.png"></a>
  <br>
  ———  <i><b>Pre-Alpha</b></i> ——
  <a href="https://github.com/DirectorsCutMod/DirectorsCut" title="Github repository"><img alt="Github logo" src="https://i.imgur.com/mrQcZY9.png"/></a>
  <a href="https://bsky.app/profile/directorscut.bsky.social" title="Bluesky profile"><img alt="Bluesky logo" src="https://i.imgur.com/nQy9dJ8.png"/></a>
  <a href="https://discord.com/invite/zrjApe5gkk" title="Discord server"><img alt="Discord logo" src="https://i.imgur.com/pgLNitm.png"/></a>
  <a href="https://www.reddit.com/r/DirectorsCut" title="Reddit community"><img alt="Reddit logo" src="https://i.imgur.com/falKST9.png"/></a>
  <a href="https://youtube.com/@DirectorsCutMod" title="YouTube channel"><img alt="YouTube logo" src="https://i.imgur.com/76FljEy.png"/></a>
  <a href="https://developer.valvesoftware.com/wiki/Director's_Cut" title="Valve Developer Wiki page"><img alt="Source Engine logo" src="https://i.imgur.com/6elUXWS.png"/></a>
  ———
</div>
<hr>

A community-driven filmmaking tool built on Source. A spiritual successor to **SFM**, if you will.

The goal is to recreate **Source Filmmaker** and eventually release on **Steam**.

## Contributors
Programming: [KiwifruitDev](https://github.com/KiwifruitDev), [ashifolfi](https://github.com/ashifolfi)

Graphic Design: [FLARE145](https://flare145.com/)

Moderation: [Flynnyt03](https://github.com/flynnyt03), [nuppington](https://github.com/nuppington-bit)

<div align="center">
  <a href="https://github.com/KiwifruitDev" title="KiwifruitDev (GitHub profile)"><img width="64px" alt="KiwifruitDev avatar" src="https://avatars.githubusercontent.com/u/25839651?v=4"></a>
  <a href="https://github.com/ashifolfi" title="ashifolfi (GitHub profile)"><img width="64px" alt="ashifolfi avatar" src="https://avatars.githubusercontent.com/u/29577987?v=4"></a>
  <a href="https://flare145.com/" title="FLARE145 (flare145.com)"><img width="64px" alt="FLARE145 avatar" src="https://flare145.com/flarehost/flare145image.png"></a>
  <a href="https://github.com/flynnyt03" title="Flynnyt03 (GitHub profile)"><img width="64px" alt="Flynnyt03 avatar" src="https://avatars.githubusercontent.com/u/129870126?v=4"></a>
  <a href="https://github.com/nuppington-bit" title="nuppington (GitHub profile)"><img width="64px" alt="nuppington avatar" src="https://avatars.githubusercontent.com/u/55516022?v=4"></a>
</div>

## Development
Director's Cut is built on the **Source SDK 2013 Multiplayer** codebase, which uses the **Team Fortress 2** branch of the **Source Engine**. The project is developed in **C++** using **Visual Studio 2022** and **Qt 5.15.2**.

### Pre-requisites
The following software is required to build Director's Cut from source:

- **Visual Studio 2022** with the following components:
  - **Desktop development with C++**
- **Qt 5.15.2 (MSVC 2019 64-bit)** installed to `C:\Qt\5.15.2\msvc2019_64`:
  - Download the Windows x64 version of **Qt Community Edition** from [Qt's official website](https://www.qt.io/download-qt-installer-oss).
  - Open the installer and log into your Qt account or create a new one.
  - Toggle the **Archive** checkbox in the **Select Components** page.
  - Expand the `Qt 5.15.2` section and select the following components:
    - **MSVC 2019 64-bit**
    - **Qt Debug Information Files**
  - Install to `C:\Qt`.
- **Steam** installed to `C:\Program Files (x86)\Steam`: 
  - Download the [Steam installer](https://store.steampowered.com/about/).
  - Install Steam to `C:\Program Files (x86)\Steam`.
- **Source SDK Base 2013 Multiplayer** installed to `C:\Program Files (x86)\Steam\steamapps\common\Source SDK Base 2013 Multiplayer`:
  - Open Steam and install **Source SDK Base 2013 Multiplayer** from the **Tools** section in the **Library**.

These instructions are only relevant for **Windows**. If you are developing using **Linux** and would like to contribute, please consider making a [pull request](https://github.com/DirectorsCutMod/DirectorsCut/pulls) to update this section and any other relevant parts of the repository.

### Setup
Follow these steps to set up the development environment for Director's Cut:

1. **Clone the Repository**:
  - When cloning the Git repository, make sure to clone the submodules as well:
    ```sh
    git clone --recurse-submodules https://github.com/DirectorsCutMod/DirectorsCut.git
    ```
2. **Solution Setup**:
  - Run `createdirectorscutproject.bat` to check for the required dependencies and set up the project.
 - Once the project is created, open `directorscut.sln` with Visual Studio 2022.

### Building
To build Director's Cut, press Ctrl+Shift+B in Visual Studio 2022 or click **Build > Build Solution** in the menu.

`directorscut.dll` will be placed in `game\bin\directorscut\x64` once the build is complete.

### Testing
You'll need to build the SDK's binaries before you can run Director's Cut. To do this, follow these steps:

1. **Solution Setup**:
  - Run `sdk\src\createallprojects.bat` to generate the SDK's project files.
  - Open `sdk\src\everything.sln` with Visual Studio 2022 once the project files are generated.
2. **Building**:
  - Press Ctrl+Shift+B in Visual Studio 2022 or click **Build > Build Solution** in the menu.
  - Building the SDK will take a very long time, so be patient.

With the SDK and junctions ready, you can easily launch **Source SDK 2013 Multiplayer** under `mod_tf` (Frog Fortress 2) with `-tools` mode by running `src\startdirectorscut.bat`. Director's Cut will be loaded as an engine tool once the game is fully loaded.

## Attributions
Director's Cut is licensed under the [Source 1 SDK License](LICENSE). See [thirdpartylegalnotices.txt](thirdpartylegalnotices.txt) for additional licensing information.

Additionally, Director's Cut shares code with the following repositories:
- [ValveSoftware/source-sdk-2013](https://github.com/ValveSoftware/source-sdk-2013), [mapbase-source/source-sdk-2013](https://github.com/mapbase-source/source-sdk-2013), [ashifolfi/source-sdk-2013](https://github.com/ashifolfi/source-sdk-2013/)
- [Source-SDK-Resources/source-sdk-example-qt](https://github.com/Source-SDK-Resources/source-sdk-example-qt)
- [Biohazard90/source-shader-editor](https://github.com/Biohazard90/source-shader-editor/)

Director's Cut requires [Qt 5.15.2](https://www.qt.io/), which is licensed under [LGPLv3](https://www.qt.io/licensing/open-source-lgpl-obligations).

> [!NOTE]
> Some portions of Director's Cut were contributed using [GitHub Copilot](https://copilot.github.com/).

The Director's Cut logo was created by [FLARE145](https://flare145.com/).

Valve, Source, and the Source logo are trademarks and/or registered trademarks of Valve Corporation. **Director's Cut is not affiliated with Valve Corporation.**
