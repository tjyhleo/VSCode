cmake_minimum_required(VERSION 3.0)
project(projection)
find_package(OpenCV REQUIRED )
find_package(PCL 1.3 REQUIRED COMPONENTS common io)
include_directories(${OpenCV_INCLUDE_DIR} ${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})
add_executable(projection projection.cpp)
target_link_libraries(projection ${OpenCV_LIBS} ${PCL_LIBRARIES})


# cmake_minimum_required(VERSION 2.6 FATAL_ERROR)
# project(MY_GRAND_PROJECT)
# find_package(PCL 1.3 REQUIRED COMPONENTS common io)
# include_directories(${PCL_INCLUDE_DIRS})
# link_directories(${PCL_LIBRARY_DIRS})
# add_definitions(${PCL_DEFINITIONS})
# add_executable(pcd_write_test readPLY.cpp)
# target_link_libraries(pcd_write_test ${PCL_LIBRARIES})


# cmake_minimum_required(VERSION 3.0)
# project(projection)
# # set(CMAKE_CXX_FLAGS "{CMAKE_CXX_FLAGS} -std=c++11 -03")
# find_package(OpenCV REQUIRED)
# include_directories(${OpenCV_INCLUDE_DIR})
# add_executable(projection projection.cpp)
# target_link_libraries(projection ${OpenCV_LIBS})

