cmake_minimum_required(VERSION 3.12)
project(Compare)

# Set C++ standard to C++20
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# Add executable
add_executable(cmp main.cpp)

# Find and link Threads package
find_package(Threads REQUIRED)
target_link_libraries(cmp PRIVATE Threads::Threads)

# Add compiler flags
target_compile_options(cmp PRIVATE -O3 -Wall -Wextra -pedantic)
