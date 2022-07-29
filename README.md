***
[![Build](https://github.com/LucasTesnier/ZAAAAAAAAAAAAppy/actions/workflows/cmake.yml/badge.svg)](https://github.com/LucasTesnier/ZAAAAAAAAAAAAppy/actions/workflows/cmake.yml)
***

The PhysicsUtils project consists of the realization of a utilitary library for simulate some basics physcis principle.

Composed of a ECS logic, the library will  use a component system which permit to add other object very easely.

## Before continuing...

This project is made by an EPITECH student. Don't hesitate to contact me if you have any ideas for improving the project!

### Prerequisites

To use this project, you'll need Cmake 3.17.0 Compiler, SFML-devel library and CXX20.

### Building program

```bash
    cmake -B ./build -G "Unix Makefiles" -DCMAKE_BUILD_TYPE=Release
    cmake --build ./build
```

### Testing program
```bash
    rm -rf ./build 
    cmake -B ./build -G "Unix Makefiles" -DCMAKE_BUILD_TYPE=Debug -DTESTING=ON
    cmake --build ./build
    cd ./build
    ctest --ouput-on-failure
```

### Coding Style

Zappy is developed with C++. I tried to respect the Epitech Coding Style. Or at least an adaptation for C++. ([Check it right here.](https://intra.epitech.eu/file/Public/technical-documentations/epitech_c_coding_style.pdf)

## Thank for reading

Feel free to read the CONTRIBUTING.md

Do not hesitate to contact me for any questions or remarks.

* Mail -> lucas.tesnier@epitech.eu

* Discord -> Waroth#4623

## Authors

* **Lucas Tesnier**
