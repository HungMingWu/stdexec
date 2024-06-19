add_executable(stdexec_demo main.cpp)

set_target_properties(stdexec_demo PROPERTIES
    CXX_STANDARD 20
    CXX_STANDARD_REQUIRED ON
    CXX_EXTENSIONS OFF)

target_link_libraries(stdexec_demo PRIVATE stdexec_modules)