cmake_minimum_required(VERSION 3.16)

project(testing VERSION 1.0.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)


find_package(Qt6 REQUIRED COMPONENTS Widgets)
qt_standard_project_setup()

qt_add_executable(testing
    mainwidget.cpp
    main.cpp
)

target_link_libraries(testing PRIVATE Qt6::Widgets)

set_target_properties(testing PROPERTIES
    WIN32_EXECUTABLE ON
    MACOSX_BUNDLE ON
    )
