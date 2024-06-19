add_library(stdexec_modules)

set_target_properties(stdexec_modules PROPERTIES
    CXX_STANDARD 20
    CXX_STANDARD_REQUIRED ON
    CXX_EXTENSIONS OFF)

target_compile_options(stdexec_modules PUBLIC
    $<$<COMPILE_LANG_AND_ID:CXX,MSVC>:/Zc:__cplusplus /Zc:preprocessor>
)

target_sources(stdexec_modules
  PUBLIC
    FILE_SET cxx_modules TYPE CXX_MODULES FILES
    stdexec.cppm
)

target_include_directories(stdexec_modules PUBLIC ../include)