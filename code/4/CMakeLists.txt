cmake_minimum_required(VERSION 3.5.0)

include(CTest)
enable_testing()

add_executable(4.1.linear.container 4.1.linear.container.cpp)
add_executable(4.2.unordered.map 4.2.unordered.map.cpp)
add_executable(4.3.tuples 4.3.tuples.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
