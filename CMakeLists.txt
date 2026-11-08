cmake_minimum_required(VERSION 3.16)
project(AsteryCredit VERSION 0.1 LANGUAGES CXX)

# setting up c++ standards
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# declare the sources files
add_executable(astery-credit src/main.cpp)

# declare headers
target_include_directories(astery-credit PRIVATE ${PROJECT_SOURCE_DIR}/include)

if(MSVC)
    target_compile_options(astery-credit PRIVATE/W4)
else()
    target_compile_options(astery-credit PRIVATE -Wall -Wextra -Wpedantic)
endif()