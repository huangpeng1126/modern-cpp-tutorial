cmake_minimum_required(VERSION 3.5.0)

include(CTest)
enable_testing()

add_executable(9.1.noexcept 9.1.noexcept.cpp)
add_executable(9.2.literals 9.2.literals.cpp)
add_executable(9.3.alignment 9.3.alignment.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
