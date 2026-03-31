add_subdirectory(map/dumbmap)
add_subdirectory(server)

add_executable(app main.cpp)
target_link_libraries(app PRIVATE config server)