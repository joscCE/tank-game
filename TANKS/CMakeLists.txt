cmake_minimum_required(VERSION 3.0)

project(TANKS)

# Busca la librería raylib
find_package(raylib REQUIRED)

# Añadir las opciones estándar de C++
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Incluir los directorios de raylib
include_directories(${RAYLIB_INCLUDE_DIRS})

# Añadir los archivos fuente
add_executable(${PROJECT_NAME} main.cpp
        Graph.cpp
        Graph.h
)

# Vincular raylib a tu proyecto
target_link_libraries(${PROJECT_NAME} raylib)
