project(boost_program_options_example)
cmake_minimum_required(VERSION 3.12)

find_package(Boost COMPONENTS
  filesystem
  program_options
  regex
  unit_test_framework
)

add_subdirectory(src)
add_subdirectory(test)
