cmake_minimum_required(VERSION 3.5.0)
set(CMAKE_C_COMPILER gcc-11)
set(CMAKE_CXX_COMPILER g++-11)
project(modern_cpp VERSION 0.1.0)

include(CTest)
enable_testing()

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED true)

add_subdirectory(code)
add_subdirectory(exercises)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
