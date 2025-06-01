# What is this? 

This is a yet another template for new C++ projects based on [CMake](https://cmake.org/).

# Motivation

Write your motivation here

# How to build

```bash
cd <your-project-dir>
cmake . --preset=debug
cd build/debug
make -j
```

Executables will be written to `./build/debug/bin` folder.

# Example

Do not forget to add example of how to use your library or project

```cpp
#include <tea/asiocommunicator.hpp>
#include <iostream>

using tea::asiocommunicator::Server;
using tea::asiocommunicator::Client;
```


