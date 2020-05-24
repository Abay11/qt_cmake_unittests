project(mytest LANGUAGES CXX)

enable_testing(true)

set(CMAKE_AUTOMOC ON)

add_executable(mytest test.cpp)
add_test(NAME mytest COMMAND mytest)

target_link_libraries(mytest PRIVATE Qt5::Test)
