
add_library(Library STATIC my_lib.cpp)                  # We move all the add Libraries inside the CMakeFile.txt on the src folder.

target_include_directories(Library PUBLIC "./")         # Here we are saying to target the current directory.