cmake_minimum_required(VERSION 3.15)

project(bvh_test_gpu)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_SOURCE_DIR}/OUTPUT/${PROJECT_NAME}")

file(GLOB_RECURSE CPP_SRC_FILES ./*.cpp)

add_executable(bvh_test_gpu ${CPP_SRC_FILES})

target_link_libraries(bvh_test_gpu
	PUBLIC horizon
)

target_include_directories(bvh_test_gpu
	PUBLIC horizon
)
