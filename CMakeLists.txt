cmake_minimum_required(VERSION 3.3)
project(ActorTest)

set (CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR})

find_package(Libcaf COMPONENTS core io REQUIRED)
include_directories(${LIBCAF_INCLUDE_DIRS})

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(SOURCE_FILES main.cpp)
add_executable(ActorTest ${SOURCE_FILES})

target_link_libraries(ActorTest ${LIBCAF_LIBRARIES})