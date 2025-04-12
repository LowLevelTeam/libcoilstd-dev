# COIL Standard Development Library

libcoilstd-dev contains functionality for the COIL standard library specification.

The standard library specification defines a standard interface for runtime system functionality like the operating system.

This standard library follows a versioning scheme using the major.minor.patch system for fixing bugs in the library without changing the interface, adding to the library without major additions (files, dirs) or removal of functions however some functions may be given a deprecated warning and major which are for major additions like adding new files and functionality, removing functionality, files or dirs and fully removing deprecated features.

Apart from the versioning scheme the COIL Standard Library is further split into static, runtime, hetregenous.

## The 3 major sections
As defined above the 3 major sections are the static library for features with no outside interaction including functionality like string manipulation (no allocation), math functionality and certain other features.

The runtime library contains standard communication with the operating system. This mainly contains sections like memory allocation, thread management/scheduling, IO and other operating system functionality accessible under a standard interface.

The Advanced Runtime library is the multi-device section of the standard library for driver communication and extended operating system functionality like graphics, general purpose computing between multiple devices, extended allocation and much more.

#### Static

Features:
- String
- Math
- Complex
- Algorithm
- Containers

#### Runtime

Features:
- IO
- Memory
- Time
- Signal
- Thread
- Filesystem
- DNS / URI / Network Addresses

#### Advanced Runtime

Advanced COIL features like JIT and interpreting support as well as more advanced features of operating systems like driver communications for extended devices both processing and default.

The advanced runtime section has special made features for some special devices like GPUs, Input devices, Audio devices and more in attempt to make the programmers like easier.

Features:
- JIT
- Dynamic Byte Code
- Device communication
- Device Querying
- Graphics
- Keyboard / Mouse

## Versioning / Roadmap
The standard library will be built first and foremost for a complete way to debug and test applications with basic stdout functinality and system call wrappers with specific ABIs. From here more advanced ABIs will be supported with custom name mangler functions.



## Language
The COIL standard library is written is a polygot project written in multiple compiled and low level languages. Any language can be used to contribute like C, C++ and Rust if there is a compiler to COIL for this language.

The main section is written in CASM for direct compilation and semi-self-hosted standard library.

The binary COIL archive for the library will be read by specific tools to reconstruct a group of headers for the COIL standard library.

A COIL C Compiler may want to make use of the COIL standard library to make a cross platform C standard library and remove some of the work in cross platform compilers.






