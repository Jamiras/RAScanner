# Required: sudo apt install cmake libgl1-mesa-dev

cmake_minimum_required(VERSION 3.16)
project(RAScanner LANGUAGES CXX)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

set(CMAKE_PREFIX_PATH "~/Qt/6.11.0/gcc_64")
find_package(Qt6 REQUIRED COMPONENTS Widgets Core Gui)

add_executable(RAScanner
    src/main.cpp
    src/MainWindow.cpp
    src/MainWindow.h
    src/MainWindow.ui
)

target_link_libraries(RAScanner PRIVATE Qt6::Widgets Qt6::Core Qt6::Gui)
