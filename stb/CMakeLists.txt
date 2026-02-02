project(stb LANGUAGES CXX)
add_library(${PROJECT_NAME}
	"${CMAKE_CURRENT_SOURCE_DIR}/include/stb_image.h"
	"${CMAKE_CURRENT_SOURCE_DIR}/include/stb_image_write.h"
	"${CMAKE_CURRENT_SOURCE_DIR}/src/stb_image.cpp"
)

target_include_directories(${PROJECT_NAME}
	PUBLIC
		include/
	PRIVATE
		src/
)