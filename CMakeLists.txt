project(Packages)

add_library(${PROJECT_NAME} INTERFACE)

#Comes from OS
find_package(OpenGL REQUIRED)
target_link_libraries(${PROJECT_NAME} INTERFACE ${OPENGL_LIBRARIES} )

#glfw_Source
add_subdirectory(glfw)
target_link_libraries(${PROJECT_NAME} INTERFACE glfw) 

#glad
add_subdirectory(glad)
target_link_libraries(${PROJECT_NAME} INTERFACE glad)

add_subdirectory(glm)
target_link_libraries(${PROJECT_NAME} INTERFACE glm)

#stb 
add_subdirectory(stb)
target_link_libraries(${PROJECT_NAME} INTERFACE stb)

#spd
add_subdirectory(spdlog)
#target_link_libraries(${PROJECT_NAME} INTERFACE spdlog::spdlog_header_only)
target_link_libraries(${PROJECT_NAME} INTERFACE spdlog::spdlog)

# ===binary === #
# Precompiled Assimp (binary version)
set(ASSIMP_ROOT "${CMAKE_CURRENT_SOURCE_DIR}/binary")
set(ASSIMP_INCLUDE_DIR "${ASSIMP_ROOT}/include")
set(ASSIMP_LIB_DIR "${ASSIMP_ROOT}/lib")

# Add headers and static lib
target_include_directories(${PROJECT_NAME} INTERFACE ${ASSIMP_INCLUDE_DIR})
target_link_libraries(${PROJECT_NAME} INTERFACE
    debug "${ASSIMP_LIB_DIR}/assimp-vc143-mtd.lib"
)

#MikkTSpace
add_subdirectory(MikkTSpace)
target_link_libraries(${PROJECT_NAME} INTERFACE mikktspace)
