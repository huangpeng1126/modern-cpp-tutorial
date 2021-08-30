cmake_minimum_required(VERSION 3.5.0)

include(CTest)
enable_testing()

add_subdirectory(1)
add_subdirectory(2)
add_subdirectory(3)
add_subdirectory(4)
add_subdirectory(5)
add_subdirectory(6)
add_subdirectory(7)
add_subdirectory(9)
add_subdirectory(10)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
