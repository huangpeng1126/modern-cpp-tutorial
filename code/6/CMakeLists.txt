cmake_minimum_required(VERSION 3.5.0)

include(CTest)
enable_testing()

add_executable(6.1.regex 6.1.regex.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
