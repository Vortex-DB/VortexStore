cmake_minimum_required(VERSION "3.15.0")

project(VortexStore)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include(FetchContent)
FetchContent_Declare(
  googletest
    URL https://github.com/google/googletest/archive/52eb8108c5bdec04579160ae17225d66034bd723.zip
)

set(gtest_force_shared_crt ON CACHE BOOL "" FORCE)
FetchContent_MakeAvailable(googletest)

enable_testing()

add_executable(hello_test
  hello_test.cc
)
target_link_libraries(
  hello_test
  GTest::gtest_main
)

include(GoogleTest)
gtest_discover_tests(hello_test)


add_executable(hello
  hello.c
) 