cmake_minimum_required(VERSION 3.14)

project(Homework2Task1 LANGUAGES CXX)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Qt6 REQUIRED COMPONENTS Core)
find_package(Qt6 REQUIRED COMPONENTS Network)
find_package(Qt6 REQUIRED COMPONENTS Sql)

add_executable(Homework2Task1
  main.cpp
)
target_link_libraries(Homework2Task1 Qt6::Core)
target_link_libraries(Homework2Task1 Qt6::Network)
target_link_libraries(Homework2Task1 Qt6::Sql)

install(TARGETS Homework2Task1
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR})
