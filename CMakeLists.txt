cmake_minimum_required(VERSION 3.23)
project(project-name)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_CLANG_TIDY clang-tidy)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
add_compile_options(-Wall -Wextra -Wpedantic -Werror)


set(Boost_USE_STATIC_LIBS   ON)
find_package(Boost 1.87.0 NO_MODULE REQUIRED COMPONENTS program_options json filesystem)
include_directories(${Boost_INCLUDE_DIRS})

find_package(GTest REQUIRED)
enable_testing()

find_package(benchmark REQUIRED)

include_directories(include)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

add_subdirectory(src)

