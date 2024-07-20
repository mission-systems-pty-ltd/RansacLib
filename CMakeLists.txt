cmake_minimum_required (VERSION 3.0)

project(RansacLib VERSION 1.0.0)

if (EXISTS "${CMAKE_SOURCE_DIR}/cmake")
  set (CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${CMAKE_SOURCE_DIR}/cmake)
endif ()

find_package(pybind11 REQUIRED)
find_package(Eigen3 REQUIRED)
find_package(PoseLib REQUIRED)

include_directories(${EIGEN3_INCLUDE_DIR}
                    ${POSELIB_INCLUDE_DIR}
)
add_subdirectory (examples)
install(DIRECTORY RansacLib DESTINATION include)