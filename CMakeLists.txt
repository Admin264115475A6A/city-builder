cmake_minimum_required(VERSION 3.31)
project(CityBuilder)

set(CMAKE_CXX_STANDARD 17)

# Set paths for dependencies
set(GLFW_DIR "C:/game_engine/libs/glfw")
set(PYBIND11_DIR "C:/game_engine/libs/pybind11")
set(ENTT_DIR "C:/game_engine/libs/entt/single_include")
set(GLAD_DIR "C:/game_engine/libs/glad")  # ✅ Define GLAD_DIR

# Add required subdirectories
add_subdirectory(${GLFW_DIR} ${CMAKE_BINARY_DIR}/glfw)
add_subdirectory(${PYBIND11_DIR} ${CMAKE_BINARY_DIR}/pybind11)

# Include directories
include_directories(${ENTT_DIR})
include_directories(${GLAD_DIR}/include)  # ✅ Include GLAD headers

# Add GLAD as a static library
add_library(glad STATIC ${GLAD_DIR}/src/glad.c)

# Add source files
file(GLOB SOURCES src/*.cpp)

# Define executable
add_executable(CityBuilder WIN32 ${SOURCES})

# Set as a Windows GUI application
set_target_properties(CityBuilder PROPERTIES WIN32_EXECUTABLE YES)

# Link libraries
#target_link_libraries(CityBuilder PRIVATE glfw pybind11::module opengl32 glad)
target_link_libraries(CityBuilder PRIVATE glfw pybind11::module opengl32 glad glu32)