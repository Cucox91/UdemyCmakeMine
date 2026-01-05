cmake_minimum_required(VERSION 3.0.0)                                           # Minimum CMake Version Required

project(                                                                        # Our Project Function Have three parameters, Project Name, Code Version and Languages.
    CppProjectTemplate 
    VERSION 1.0.0 
    LANGUAGES C CXX)

add_library(Library STATIC my_lib.cpp)

add_executable(Executable main.cpp)                                             # We add our executable file to the Project to be processed by cmake.

target_link_libraries(Executable PUBLIC Library)                                # Here we are saying to link the library added in line 8.

# Generators:
# They are used to generated the Makefiles based on the tool being used.
# We want to use the Unix Makefile or the Visual Studio Makefile often.
