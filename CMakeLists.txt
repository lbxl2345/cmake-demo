project(cmake-demo)

add_executable(cmake_demo demo.c demo.h)

add_library(libcmake_demo SHARED libdemo.c)
set_target_properties(libcmake_demo PROPERTIES OUTPUT_NAME "cmake_demo")

target_link_libraries(cmake_demo libcmake_demo)

install(TARGETS cmake_demo DESTINATION bin)
install(TARGETS libcmake_demo DESTINATION lib)
