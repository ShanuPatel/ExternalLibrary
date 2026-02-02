project(mikktspace)

set(LIBRARY_HEADER {CMAKE_CURRENT_SOURCE_DIR})

add_library(mikktspace)
target_sources(mikktspace PRIVATE 
"${CMAKE_CURRENT_SOURCE_DIR}/mikktspace.c"

)

target_include_directories(mikktspace PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}")


#target_link_libraries(mikktspace PUBLIC glfw glad)
