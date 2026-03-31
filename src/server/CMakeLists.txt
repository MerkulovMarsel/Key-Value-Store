add_library(server STATIC server.cpp)
target_link_libraries(server PUBLIC dumbmap config )