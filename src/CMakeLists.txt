
add_library(src INTERFACE)
target_include_directories(src INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})
target_link_libraries(src INTERFACE
    Boost::program_options)
target_compile_features(src INTERFACE cxx_std_11)

add_executable(app
    main.cpp)
target_link_libraries(app PRIVATE src)
set_property(TARGET app PROPERTY
    RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR})

add_library(boost_program_options_example::src ALIAS src)
