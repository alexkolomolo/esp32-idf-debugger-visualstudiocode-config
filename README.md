#VS Code configuration template for ESP-IDF development

Template configuration of Microsoft Code editor for ESP32 development using ESP-IDF SDK with completion and debugging. As of right now this works only under Linux.

#### Requirements ####
|Name          |Version used in tests|
|--------------|---------------------|
|ESP-IDF SDK   |3.0 and latest       |
|Microsoft Code|1.22.2 (OSS version) |
|bear          |2.3.11               |

#### VS Code plugins ####
* C/C++ (*ms-vscode.cpptools*)
* Native Debug (*webfreak.debug*)

#### Instructions ####
1. Set up ESP-IDF like you normally would
2. Create a new environment variable *ESP32_TOOLCHAIN_PATH* and point it to your *xtensa-esp32-elf* toolchain directory
3. Select the root directory of your project in Microsoft Code (so that the *Makefile* file is in the root directory)
4. Copy all files from this directory into *.vscode* directory inside your project directory
5. In *launch.json* change the *executable* and *autorun* fields so that they reflect your project name (default is *app_project*)

You can now start debugging your projects. To get completion, run the *build compile db* task. You also will need to *clean* and re-run that task every time you add a new file, component or update the *sdkconfig*. This is the only way to get accurate completion.

For easier access to tasks you can use the Status Bar Tasks plugin (*GuardRex.status-bar-tasks*).