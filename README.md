# OtaRME
4.1.1 with the addition of seeing underground floor (8) while being on the surface (7)
Maybe in the future other changes too, at the moment the above thing was all I needed.

06.04.2023

OTAcademy RME:
https://github.com/OTAcademy/RME
-------------------------------------------------------------
Follow the guide below

### Install Visual Studio (VS 2019 community or later)
https://visualstudio.microsoft.com/vs/

### Install Git Bash
https://gitforwindows.org/

### Install vcpkg
* Start Git Bash
* Go to root directory `cd /c`
* Clone vcpkg `git clone https://github.com/Microsoft/vcpkg`
* Enter the directory `cd vcpkg`
* Run bootstrap `./bootstrap-vcpkg.bat`

### Install dependencies
* Choose 32 or 64 bit or both. This will take some time so be patient.
  * 32 bit: `./vcpkg install wxwidgets freeglut asio nlohmann-json fmt`
  * 64 bit: `./vcpkg install --triplet x64-windows wxwidgets freeglut asio nlohmann-json fmt`
* Make libraries available to Visual Studio `./vcpkg integrate install`

### Clone project
* Create and enter the directory where you want the sources
```
cd /c
mkdir developer
cd developer
```
* Clone RME `git clone https://github.com/hampusborgos/rme.git`

### Build and run
* Open `C:\developer\rme\vcproj\RME.sln` in Visual Studio
* Choose Debug or Release and Win32 or x64 in the toolbar
* Press F5 to start debugging


FURTHERMORE WHAT I NOTICED IS THAT YOU NEED:
```./vcpkg install boost-spirit:x64-windows```
```./vcpkg install libarchive:x64-windows```

