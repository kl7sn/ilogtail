cmake_minimum_required(VERSION 2.9)
project(observer)

file(GLOB_RECURSE LIB_SOURCE_FILES *.cpp *.h)
append_source_files(LIB_SOURCE_FILES)
add_library(${PROJECT_NAME} STATIC ${LIB_SOURCE_FILES})
target_link_libraries(${PROJECT_NAME} common)
target_link_libraries(${PROJECT_NAME} logger)
target_link_libraries(${PROJECT_NAME} config)
target_link_libraries(${PROJECT_NAME} config_manager)
target_link_libraries(${PROJECT_NAME} monitor)
target_link_libraries(${PROJECT_NAME} profiler)
target_link_libraries(${PROJECT_NAME} event)
target_link_libraries(${PROJECT_NAME} log_pb)

add_subdirectory(network)



