cmake_minimum_required(VERSION 3.5.0)

include(CTest)
enable_testing()

add_subdirectory(2)
add_subdirectory(6)
add_subdirectory(7)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
