cmake_minimum_required(VERSION 3.0.0)
project(LearningOpenGL VERSION 0.1.0)
set(CXX_STANDARD 11)
# config glad
include_directories(${CMAKE_SOURCE_DIR}/vendor/glad/include)
add_subdirectory(${CMAKE_SOURCE_DIR}/vendor/glad)

# config glfw
include_directories(${CMAKE_SOURCE_DIR}/vendor/glfw/include)
add_subdirectory(${CMAKE_SOURCE_DIR}/vendor/glfw)



add_executable(openglapp ${CMAKE_SOURCE_DIR}/src/main.cpp)
target_link_libraries(openglapp Glad glfw) 


