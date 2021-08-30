cmake_minimum_required(VERSION 3.5.0)

include(CTest)
enable_testing()

find_package(OpenSSL)
find_package(Boost)
add_executable(main.http main.http.cpp)
add_executable(main.https main.https.cpp)

target_include_directories(main.http PRIVATE ${Boost_INCLUDE_DIRS})
target_include_directories(main.https PRIVATE ${Boost_INCLUDE_DIRS} ${OPENSSL_INCLUDE_DIR})
target_link_libraries(main.https PRIVATE OpenSSL::SSL)
# target_link_libraries(main.https PRIVATE ${OPENSSL_SSL_LIBRARY})

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
