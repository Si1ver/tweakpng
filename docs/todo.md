# TweakPNG: List of Things To Do

This document contains a list of planned changes.

The list reflects personal interests and is not necessarily based on the project's functional development needs. Before implementing any of the changes listed below, consider whether they **align with your goals or values**.

There is no guarantee that any of these changes will actually be implemented.

## Features

*No plans at the moment.*

## Source Code

* Compile the code with [warnings and strict standards conformance](https://github.com/cpp-best-practices/cppbestpractices/blob/master/02-Use_the_Tools_Available.md#msvc).

* Investigate how much effort is needed to make this tool support more platforms, namely Linux and macOS.

## Documentation

* Add usage documentation based on original docs.

* Add a changelog file with a [curated, chronological list of notable changes for each version of the project](https://keepachangelog.com/en/1.1.0/).

## Building and Automation

* CMake fails to build the project with the current build profile due to a build error. Investigate and fix the issue, then describe the build command in the documentation.

* Add CMake options for building without libpng and zlib support as described in original documentation.

* Add additional CMake configuration and build profiles. Currently, only the release x64 profile is available.

* Set up a CI workflow to build the project automatically before merging pull requests.
