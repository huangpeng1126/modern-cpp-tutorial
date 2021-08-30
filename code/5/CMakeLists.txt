cmake_minimum_required(VERSION 3.5.0)

include(CTest)
enable_testing()

add_executable(5.1.shared.ptr.a 5.1.shared.ptr.a.cpp)
add_executable(5.2.unique.ptr 5.2.unique.ptr.cpp)
add_executable(5.3.weak.ptr 5.3.weak.ptr.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
