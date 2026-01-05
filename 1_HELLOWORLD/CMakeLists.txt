# Steps to Create all.
# 0) Create CMake and Source Files.
# 1) mkdir build
# 2) cd build
# 3) cmake ..                                                                   # Generate the Build Files / Config Project.
# 4) cmake --build .
# 5) Option 2: cmake -S .. -B .
# 6) ./Executable 

cmake_minimum_required(VERSION 3.0.0)                                           # Minimum CMake Version Required

project(                                                                        # Our Project Function Have three parameters, Project Name, Code Version and Languages.
    CppProjectTemplate 
    VERSION 1.0.0 
    LANGUAGES C CXX)

add_executable(Executable main.cpp)                                             # We add our executable file to the Project to be processed by cmake.



# Generators:
# They are used to generated the Makefiles based on the tool being used.
# We want to use the Unix Makefile or the Visual Studio Makefile often.
