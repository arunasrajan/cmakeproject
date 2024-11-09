# Notes on CMake

## Reference
[Cmake Tutorial](https://cmake.org/cmake/help/book/mastering-cmake/cmake/Help/guide/tutorial/index.html#id1)

## Step1: A Basic Starting Point 
Created a main that prints _Hello World_.

Also created a very basic CMakeLists.txt file

**CMakelists.txt**
```
cmake_minimum_required(VERSION 3.28)
project(firstprogram)

add_executable(firstprogram main.c)
```
**main.c**
```
#include <stdio.h>

void main(void)
{
    printf("Hello World");
}
```
The CmakeLists.txt contains the version of the CMake to be supported, project name which is _firstprogram_. Its also links the executable _firstprogram.exe_ to _main.c_.
This is compiled in VS Code where CMake is already setup using the STM32CLT tools. So as soon as CMakeLists.txt is created several other files and a _build_ folder is created. Compile the code in VS Code. If compiling through command prompt, go into the build folder and give the command

    > cmake ..
    > make

When cmake command is given, a _MakeFile_ is generated in build folder. Run make next to create the executable. _firstprogram.exe_ is generated inside the build folder. Run firstprogram.exe and see if it prints _Hello World_.

```
D:\07_github\cmakestudy\cmakeproject\firstprogram\build>make
[ 50%] Linking C executable firstprogram.exe
[100%] Built target firstprogram

D:\07_github\cmakestudy\cmakeproject\firstprogram\build>firstprogram.exe
Hello World
```