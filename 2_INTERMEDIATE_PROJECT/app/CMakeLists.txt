add_executable(Executable main.cpp)                     # We add our executable file to the Project to be processed by cmake.

target_link_libraries(Executable PUBLIC Library)        # Here we are saying to link the library added in line add_executable.
