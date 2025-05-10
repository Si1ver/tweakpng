# List of things to do

## Features

*No plans at the moment.*

## Source Code

* Compile the code with [warnings and strict standards conformance](https://github.com/cpp-best-practices/cppbestpractices/blob/master/02-Use_the_Tools_Available.md#msvc).

* Investigate how much effort is needed to make this tool support more platforms, namely Linux and macOS.

## Documentation

* Add usage documentation based on original docs.

* Add a changelog file with a [curated, chronological list of notable changes for each version of the project](https://keepachangelog.com/en/1.1.0/).

## Building and Automation

* CMake fails to build a project with current build profile due to a build error. Investigate and fix the issue, then document the build command in the readme file.

* Add CMake options for building without libpng and zlib support as described in original documentation.

* Add additional CMake configuration and build profiles. Currently, only the release x64 profile is available.

* Set up a CI workflow to build the project automatically before merging pull requests.
