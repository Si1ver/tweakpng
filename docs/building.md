# TweakPNG: Building Instructions

## Prerequisites

To build the tool from source, install the following:

* `Visual Studio 2022` with MSVC compiler *(choose `Desktop development with C++` workload for easy installation of required components)*;
* `CMake 3.21` *or newer*;
* `Git` *(for installing vcpkg)*.

## Preparing Environment

1. Install vcpkg

    vcpkg is a free and open-source C/C++ package manager used to provide required third-party libraries.

    vcpkg can be installed in any directory. The recommended approach is to install vcpkg to the root directory of this project.

    To install vcpkg, open a [terminal](https://learn.microsoft.com/en-us/windows/terminal/) (or a command prompt) in the desired directory and execute the following commands one by one:

    ```cmd
    git clone https://github.com/microsoft/vcpkg.git
    vcpkg\bootstrap-vcpkg.bat
    set VCPKG_ROOT=%cd%\vcpkg
    set PATH=%PATH%;%VCPKG_ROOT%;
    ```

    **Important:** Run CMake from the same terminal session where the environment variables (`VCPKG_ROOT` and `PATH`) were set.

    More information about installing vcpkg can be found [in the documentation](https://learn.microsoft.com/en-gb/vcpkg/get_started/get-started?pivots=shell-cmd).

## Building

1. Generate Visual Studio solution

    CMake configuration presets for the most common build configurations are defined in the `CMakePresets.json`.

    Execute the following command to generate a Visual Studio solution using CMake:

    ```cmd
    cmake -S . -B build --preset=PRESET_NAME
    ```

    Replace `PRESET_NAME` with one of the following configuration presets:

    | Preset Name | Platform | Generator | Options |
    | ----------- | -------- | --------- | ------- |
    | `windows-x64-vs2022-release` | Windows, x64, release | Visual Studio 2022 | (default) |
    | `windows-x64-vs2022-ansi-release` | Windows, x64, release | Visual Studio 2022 | ENABLE_UNICODE = OFF |

    Generated files will appear in the `build` directory.

2. Build the tool executable

    Open the `tweak_png.sln` solution file in Visual Studio and use `Build -> Build Solution` to produce an executable application.

## CMake Options

The following CMake options are available:

| Option Name | Default Value | Description |
| ----------- | ------------- | ----------- |
| ENABLE_UNICODE | ON | Enables Unicode support. |
