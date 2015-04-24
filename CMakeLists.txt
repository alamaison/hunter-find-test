cmake_minimum_required(VERSION 3.0)

include(${CMAKE_CURRENT_LIST_DIR}/HunterGate.cmake)

HunterGate(
    URL "https://github.com/ruslo/hunter/archive/v0.9.2.tar.gz"
    SHA1 "94f56cb0242146c4db10ed6f92996b3e2b9270ef"
)

project(hunter-find-test)

hunter_add_package(ZLIB)
find_package(ZLIB REQUIRED)

hunter_add_package(PNG)
find_package(PNG REQUIRED)

hunter_add_package(TIFF)
find_package(TIFF REQUIRED)

hunter_add_package(Expat)
find_package(EXPAT REQUIRED)

add_executable(foo foo.cpp)