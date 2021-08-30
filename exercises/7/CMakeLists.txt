cmake_minimum_required(VERSION 3.5.0)

include(CTest)
enable_testing()

add_executable(7.1.main 7.1/main.cpp)
add_executable(7.2.mutex 7.2.mutex.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
