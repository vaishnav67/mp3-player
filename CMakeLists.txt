# CMakeList.txt : CMake project for src, include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.8)

project (src)

add_executable (src "src/main.cpp" "src/main.h")

target_include_directories(src PRIVATE "${CMAKE_CURRENT_SOURCE_DIR}/inc")
target_link_directories(src PRIVATE "${CMAKE_CURRENT_SOURCE_DIR}/lib")
target_link_libraries(src PRIVATE avcodec avdevice avfilter avformat avutil postproc swresample swscale)
# TODO: Add tests and install targets if needed.
