cmake_minimum_required(VERSION 3.2.0 FATAL_ERROR)
project(locomotion)

# Make sure libcamera is available
find_package(PkgConfig REQUIRED)
pkg_check_modules(CAMERA REQUIRED camera)

add_subdirectory(src)
