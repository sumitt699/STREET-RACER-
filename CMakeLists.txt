cmake_minimum_required(VERSION 3.20)
project(STREET_RACER LANGUAGES C)

set(CMAKE_C_STANDARD 11)
set(CMAKE_C_STANDARD_REQUIRED ON)

# The original C source is kept in a ZIP to preserve it exactly.
file(ARCHIVE_EXTRACT
  INPUT "${CMAKE_CURRENT_SOURCE_DIR}/source.zip"
  DESTINATION "${CMAKE_CURRENT_SOURCE_DIR}/source"
)

find_package(raylib CONFIG REQUIRED)

add_executable(STREET_RACER source/main.c)
target_link_libraries(STREET_RACER PRIVATE raylib)

if(APPLE)
  target_link_libraries(STREET_RACER PRIVATE m)
endif()
