cmake_minimum_required(VERSION 3.2.0 FATAL_ERROR)
project(locomotion)

# Make sure ffmpeg & libcamera are available
find_package(PkgConfig REQUIRED)
pkg_check_modules(LIBAV REQUIRED libavformat libavcodec)
pkg_check_modules(LIBCAMERA REQUIRED libcamera)

add_subdirectory(src)
