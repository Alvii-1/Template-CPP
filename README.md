I built this template with the idea of a minimal C++ project setup. Just CMake and C++. Feel free to re-use for your own project, its pretty barebones by design. This is only for Windows and the MSVC compiler.

## How to compile and run the project:

Remember to rename this from the template :)

Note: 
- Update any mention of "project" in the CMakeLists.txt file
- Simply ```git clone https://github.com/Alvii-1/Template-CPP.git .``` to copy the template

Organization:
- /src: main c++ files
- /include: header files

### Immediately After Cloning
After running git clone in your specified directory, run ```rm -r -fo .git``` to remove the template's existing git history. Then you're good to go with using the template. This way you have a fresh git history after cloning.

### Manual Way
1. Open VS Code
2. Click the dropdown arrow by the terminal, select ```Command Prompt```
3. Type ```C:\Program Files\Microsoft Visual Studio\2022\Community\Common7\Tools\VsDevCmd.bat``` into cmd
4. To compile code ```cl main.cpp``` to run it ```main.exe```

### CMake Way
1. Ensure the CMakeLists.txt is properly updated with a new project name
2. Type ```cmake -S . -B build``` into PS to configure the project
3. Type ```cmake --build build``` into PS to build the project
4. Type ```.\build\Debug\project.exe``` to run the project, make sure to change "project" to match txt

### Powershell Function (Simplest)
1. Type ```.\run.ps1``` in the terminal and it should accomplish everything from CMake

### Details on .vscode/c_cpp_properties.json
```
{
    "configurations": [
        {
            "name": "Win32",
            "includePath": [
                "${workspaceFolder}/include/**",
                "${workspaceFolder}/src/**"
            ],
            "defines": [
                "_DEBUG",
                "UNICODE",
                "_UNICODE"
            ],
            "windowsSdkVersion": "10.0.26100.0",
            "cStandard": "c17",
            "cppStandard": "c++17",
            "intelliSenseMode": "windows-msvc-x64"
        }
    ],
    "version": 4
}
```
