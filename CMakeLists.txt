cmake_minimum_required(VERSION 3.19)
project(Skillbox_HW_30_2)

set(CMAKE_CXX_STANDARD 17)
set(CPR_BUILD_TESTS_SSL OFF)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR})
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR})

add_executable(Skillbox_HW_30_2 main.cpp)

include(FetchContent)
FetchContent_Declare(cpr GIT_REPOSITORY https://github.com/libcpr/cpr.git GIT_TAG f4622efcb59d84071ae11404ae61bd821c1c344b) # the commit hash for 1.6.2
FetchContent_MakeAvailable(cpr)

target_link_libraries(Skillbox_HW_30_2 PRIVATE cpr::cpr)