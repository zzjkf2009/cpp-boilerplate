# C++ Boilerplate
[![Build Status](https://travis-ci.org/dpiet/cpp-boilerplate.svg?branch=master)](https://travis-ci.org/dpiet/cpp-boilerplate)
[![Coverage Status](https://coveralls.io/repos/github/dpiet/cpp-boilerplate/badge.svg?branch=master)](https://coveralls.io/github/dpiet/cpp-boilerplate?branch=master)
---

## Overview

Simple starter C++ project with:

- cmake
- googletest

## Installation

- Checkout the repo (and submodules)
```
$ git clone --recursive https://github.com/dpiet/cpp-boilerplate.git

```

---

## Inorder to make it fully compatible on Elipse

### Using Eclipse CDT4 Generator 

See more detials at: https://cmake.org/Wiki/Eclipse_CDT4_Generator

This generator creates a set of .project/.cproject fiels that can be imported in Eclipse using File>Import>Existing project

* Step one
Add the target_link_libaries to the CMakeLists.txt in the app file (source file)
```
TARGET_LINK_LIBRARIES(shepp-app ${ITK_LIBRARIES}) 
```
* Step two
In the cpp-bolierplate deirectory, compile
```
cmake -G"Eclipse CDT4 - Unix Makefiles" -D CMAKE_BUILD_TYPE=Debug app 		
```
You will now find two eclipse files in your build tree
build/.project
build/.cproject


### Import the created project file into Eclipse

1. Import project using Menu File->Import
2. Select General->Existing projects into workspace:
3. Browse where your build tree is and select the root build tree directory. Keep "Copy projects into workspace" unchecked. 
4. You get a fully functional eclipse project 

