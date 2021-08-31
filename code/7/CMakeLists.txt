cmake_minimum_required(VERSION 3.5.0)

include(CTest)
enable_testing()

add_executable(7.1.thread.basic 7.1.thread.basic.cpp)
add_executable(7.2.critical.section.a 7.2.critical.section.a.cpp)
add_executable(7.3.critical.section.b 7.3.critical.section.b.cpp)
add_executable(7.4.futures 7.4.futures.cpp)
add_executable(7.5.producer.consumer 7.5.producer.consumer.cpp)
add_executable(7.6.atomic 7.6.atomic.cpp)
add_executable(7.6.bad.example 7.6.bad.example.cpp)
add_executable(7.7.is.lock.free 7.7.is.lock.free.cpp)
add_executable(7.8.memory.order 7.8.memory.order.cpp)

if (CMAKE_CXX_COMPILER_ID STREQUAL GNU)
target_link_libraries(7.7.is.lock.free atomic)
target_link_directories(7.7.is.lock.free PRIVATE "/usr/local/lib") # libboost-*
endif()

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
