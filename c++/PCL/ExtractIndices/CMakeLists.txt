cmake_minimum_required(VERSION 2.6 FATAL_ERROR)

project(ExtractIndices)
find_package(PCL 1.0 REQUIRED COMPONENTS io)

include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable(ExtractIndices ExtractIndices.cpp)
#target_link_libraries(ReadFile pcl_io)
target_link_libraries (ExtractIndices ${PCL_COMMON_LIBRARIES} ${PCL_IO_LIBRARIES} 
pcl_filters)
