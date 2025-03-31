Half-Life 2 Beta HUD for HL 25th Anniversary update
======================

This is the source code for my unofficial build of SiPlus's *HL2 beta HUD for HL1* mod, updated to work with Half-Life's 25th Anniversary update. I'm not a C++ programmer, so it's not going to be perfect.

Currently Known Issues
-------
Currently, changing the resolution with the modified libraries will result in a crash, I don't know why this issue is being caused, but the resolution will be changed to what you've set when the changes were being applied so it's only a minor annoyance.

I also haven't made the proper assets for the HUD elements at 1080p and above resolutions yet, so the HUD will be completely broken once you've set the resolution to be higher than 720p.

Building the SDK code
-------

[Visual Studio](https://visualstudio.microsoft.com/) 2019 is required to build mod DLLs on Windows. In the Visual Studio installer, install "**Desktop development with C++**" under "**Workloads**" and "**C++ MFC for latest v142 build tools (x86 & x64)**" under "**Individual components**". VS2019 projects can be found in the `projects\vs2019` folder.

Tools have not yet been updated for VS2019, but can be built using the VS2010 projects in the `projects\vs2010` folder. See the `readme.txt` file there.

Linux binaries can be built using Makefiles found in the `linux` folder. They expect to be built / run in the [Steam Runtime "scout" environment](https://gitlab.steamos.cloud/steamrt/scout/sdk). The built binaries are copied to a directory called `game` at the same level as the root directory for the git repository. You can set `CREATE_OUTPUT_DIRS=1` while building to create the output directory structure automatically.
