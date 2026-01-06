add_executable(${EXECUTABLE_NAME} main.cpp)                             # We add our executable file to the Project to be processed by cmake.

target_link_libraries(${EXECUTABLE_NAME} PUBLIC ${LIBRARY_NAME})        # Here we are saying to link the library added in line add_executable.
