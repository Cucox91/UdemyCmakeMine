cmake_minimum_required(VERSION 3.11.0)                                           # Minimum CMake Version Required

project(                                                                        # Our Project Function Have three parameters, Project Name, Code Version and Languages.
    CppProjectTemplate 
    VERSION 1.0.0 
    LANGUAGES C CXX)

add_subdirectory(src)
add_subdirectory(app)


# The Idea is to have one CMakeList.txt file per folder and then if they are nested to have add_subdirectory() per each.