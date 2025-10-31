# Installation for Windows Developers

The following is a Windows developer installation guide for OceanEye.

## Requirements

### [Msys2 and MinGW Compiler](https://www.msys2.org/)

Download the msys2 installer.
Once done, open the MinGW shell and run the following:

```
$ pacman -S mingw-w64-x86_64-gcc
```
After this, put the path to the MinGW compiler on the Path environment variable. An example directory is: C:\msys64\mingw64\bin

<!-- Other packages that may be needed: perl-modules libraries base-devel mingw-w64-x86_64-gdb mingw-w64-x86_64-gdb-multiarch mingw-w64-x86_64-postgresql -->

### [Ninja](https://github.com/ninja-build/ninja/releases)

1. Download ninja-win.zip
2. Extract it
3. Put path to the folder the ninja.exe is in onto the Path environment variable

### [CMake](https://cmake.org/download/)

Install using installer.
CMake will automatically put itself into the Path environment variable, but you must make sure that its Path comes before the MinGW compiler Path. Otherwise, issues may occur.

### [VCPKG](https://github.com/microsoft/vcpkg)

```
git clone https://github.com/microsoft/vcpkg
cd ./vcpkg
./vcpkg-bootstrap.bat
```
Follow this up by putting the path to the vcpkg folder in the path environment variable.

A good introduction for vcpkg is [here](https://learn.microsoft.com/en-us/vcpkg/get_started/get-started?pivots=shell-powershell).

### [OpenCV](https://github.com/opencv/opencv/releases/tag/4.11.0)

Need to install this to get the opencv_videoio_ffmpeg4110_64.dll. Download the .exe installer and run it. It doesn't matter where you install opencv to, all we need is the dll it provides.

## Installation and Building

Download the OceanEye repository.

```
git clone https://github.com/OceanEye-Project/OceanEye-QT
```

Inside the project directory, to build the project you'll need run cmake using the CMakePresets.json. This step will take a while as VCPKG has to download and compile all the libraries that OceanEye will need.

```
cmake --preset=default
```

After that, we link the code together to the OceanEye executable.

```
cmake --build build
```

After this, OceanEye is almost ready to use. lastly, we have to put the opencv ffmpeg dll into the same folder as the OceanEye executable so that OceanEye can properly detect objects in videos.

Access the opencv_videoio_ffmpeg4110_64.dll file by going to extracted folder opencv > build > bin. Copy the file into OceanEye build folder.

After this, OceanEye is ready to use!

## Tips

- Having more than one C/C++ compiler on your Path can cause Windows to try and use the wrong compiler for the project. The same goes for multiple installations of CMake.
- Keep your paths short, otherwise there will be issues building some of the packages.