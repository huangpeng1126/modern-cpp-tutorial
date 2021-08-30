cmake_minimum_required(VERSION 3.5.0)

include(CTest)
enable_testing()

add_executable(1.1.c.and 1.1.c.and.cpp foo.c)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
