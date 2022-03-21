cmake_minimum_required(VERSION 3.16)

if (NOT BUILD_NUMBER)
    set(BUILD_NUMBER "")
else()
    set(BUILD_NUMBER ".${BUILD_NUMBER}")
endif()

project(image_registration VERSION 0.0${BUILD_NUMBER})

set(CMAKE_CXX_STANDARD 17)

add_subdirectory(lib)
add_subdirectory(test)
add_subdirectory(thirdparty/googletest googletest)

enable_testing()
