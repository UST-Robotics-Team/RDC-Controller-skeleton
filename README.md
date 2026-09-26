# RDC Controller

## VS Code CMake settings

The `.vscode` folder contains workspace settings for the installed STM32/CMake Tools extension. These settings can be version-specific and may need to be regenerated after upgrading or reinstalling the extension.

To regenerate the folder:

1. Close the workspace in VS Code.
2. Rename or remove `.vscode` from the project directory. Do not remove `build/` unless you also want a clean rebuild.
3. Reopen the project folder in VS Code.
4. Install or enable the STM32CubeIDE CMake and CMake Tools extensions when prompted.
5. Run `CMake: Select Configure Preset` and select `Debug`.
6. Configure and build from the CMake status bar.

If the status-bar build reports that no usable generator was found, make sure the STM32CubeIDE CMake extension is enabled and that the project has been opened from its root directory. The project also supports a terminal build:

```sh
cmake --preset Debug
cmake --build --preset Debug
```
