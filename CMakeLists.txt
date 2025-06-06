cmake_minimum_required(VERSION 3.20)

project(CppCraft 
    VERSION 1.0.0
    DESCRIPTION "C++ Minecraft Engine - Converted from MineKhan JavaScript"
    LANGUAGES CXX
)

# C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Build type
if(NOT CMAKE_BUILD_TYPE)
    set(CMAKE_BUILD_TYPE Release CACHE STRING "Build type" FORCE)
endif()

# Dependencies via vcpkg
find_package(glfw3 CONFIG REQUIRED)
find_package(glm CONFIG REQUIRED)
find_package(glad CONFIG REQUIRED)
find_package(OpenAL CONFIG REQUIRED)
find_package(Stb CONFIG REQUIRED)

# Source files (minimal for now)
set(SOURCES
    src/main.cpp
)

# Executable
add_executable(${PROJECT_NAME} ${SOURCES})

# Include directories
target_include_directories(${PROJECT_NAME} PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/include
)

# Link libraries
target_link_libraries(${PROJECT_NAME} PRIVATE
    glfw
    glm::glm
    glad::glad
    OpenAL::OpenAL
)

# Platform-specific
if(WIN32)
    target_link_libraries(${PROJECT_NAME} PRIVATE opengl32)
endif()

message(STATUS "CppCraft configured successfully") 