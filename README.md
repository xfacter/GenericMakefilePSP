GenericMakefile
===============

A generic makefile for use with small/medium C and C++ projects using the [PSPSDK](https://github.com/pspdev/pspsdk). Allows for easy project setup without the need to create tedious build rules or dependency lists.

# Building
1. Install [psptoolchain](https://github.com/pspdev/psptoolchain/)
1. `make (release|debug)`
1. `make install`
  - Installs to `$DESTDIR` or `$PSP_ROOT` or `~/psproot`

# Features:
* Automatically finds and compiles all source files within the source directory.
* Automatically generates dependecies as files are compiled, ensuring that files are correctly recompiled when dependecies have updated.
* Includes configurations for normal (release) build and debug build suitable for GDB debugging.

# Limitations:
* Doesn't really support multiple types of source files in the same project.
* No easy way to exclude files from the build. You can either change the extension of files to be excluded, or use preprocessor flags for conditional compilatio.

# Thanks to:
* This project is partially based on [GenericMakefile](https://github.com/mbcrawfo/GenericMakefile).
