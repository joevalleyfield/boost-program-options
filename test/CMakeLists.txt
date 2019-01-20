add_executable(apptest
    test_main.cpp
    no_arguments_tests.cpp
    switch_argument_tests.cpp
    value_argument_no_default_tests.cpp
    raises_exception_on_invalid_argument_tests.cpp
    filename_argument_tests.cpp
)

set_property(TARGET apptest PROPERTY
    RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR})

target_link_libraries(apptest
    boost_program_options_example::src
    Boost::unit_test_framework)
