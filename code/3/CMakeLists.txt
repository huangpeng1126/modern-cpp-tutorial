cmake_minimum_required(VERSION 3.5.0)

include(CTest)
enable_testing()

add_executable(3.1.lambda.basic 3.1.lambda.basic.cpp)
add_executable(3.2.function.wrap 3.2.function.wrap.cpp)
add_executable(3.3.rvalue 3.3.rvalue.cpp)
add_executable(3.4.historical 3.4.historical.cpp)
add_executable(3.5.move.semantics 3.5.move.semantics.cpp)
add_executable(3.6.move.semantics 3.6.move.semantics.cpp)
add_executable(3.7.perfect.forward 3.7.perfect.forward.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
