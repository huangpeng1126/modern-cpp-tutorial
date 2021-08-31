cmake_minimum_required(VERSION 3.20.0)

include(CTest)
enable_testing()

set(ENV{OPENSSL_ROOT_DIR} "/usr/local/Cellar/openssl@1.1/1.1.1l/")
find_package(OpenSSL REQUIRED)
find_package(Boost REQUIRED)
add_executable(main.http main.http.cpp)
add_executable(main.https main.https.cpp)

target_include_directories(main.http PRIVATE ${Boost_INCLUDE_DIRS})
target_include_directories(main.https PRIVATE ${Boost_INCLUDE_DIRS} ${OPENSSL_INCLUDE_DIR})
target_link_libraries(main.https PRIVATE OpenSSL::SSL)
# target_link_libraries(main.https PRIVATE ${OPENSSL_SSL_LIBRARY})

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
