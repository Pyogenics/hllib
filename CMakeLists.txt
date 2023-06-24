cmake_minimum_required(VERSION 3.12)
project(hllib)

option(BUILD_STATIC "Build HLExtract and HLLib into static objects" ON)

add_compile_options(-O2 -g -funroll-loops -fvisibility=hidden)

add_subdirectory(HLLib)
add_subdirectory(HLExtract)
