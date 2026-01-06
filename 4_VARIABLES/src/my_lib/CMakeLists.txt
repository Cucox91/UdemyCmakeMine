
add_library(${LIBRARY_NAME} STATIC my_lib.cpp)                  # We move all the add Libraries inside the CMakeFile.txt on the src folder.

target_include_directories(${LIBRARY_NAME} PUBLIC "./")         # Here we are saying to target the current directory.