project(GNN)
cmake_minimum_required(VERSION 2.8)
aux_source_directory(. SRC_LIST)

include_directories(./include/)

add_executable(${PROJECT_NAME} ${SRC_LIST})

find_package( OpenCV REQUIRED )
target_link_libraries( GNN ${OpenCV_LIBS} )

if(CMAKE_COMPILER_IS_GNUCXX)
    add_definitions(-std=c++11)
endif()
