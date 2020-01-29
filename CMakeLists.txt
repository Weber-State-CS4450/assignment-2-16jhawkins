cmake_minimum_required(VERSION 3.16)

project(main)

add_executable(main main.cpp)


install(TARGETS main)

enable_testing()
add_custom_target(check COMMAND ${CMAKE_CTEST_COMMAND}
     --force-new-ctest-process
     --verbose
      --output-on-failure
)
add_test(NAME main COMMAND main)
