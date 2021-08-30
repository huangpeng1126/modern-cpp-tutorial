cmake_minimum_required(VERSION 3.5.0)

include(CTest)
enable_testing()

add_executable(10.1.without.concepts 10.1.without.concepts.cpp)
# add_executable(10.2.concepts 10.2.concepts.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
