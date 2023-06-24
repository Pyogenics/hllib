cmake_minimum_required(VERSION 3.12)
project(HLExtract)

add_executable(${PROJECT_NAME})
target_sources(${PROJECT_NAME}
	PRIVATE
	Main.c
)
target_include_directories(${PROJECT_NAME}
	PRIVATE
	.
	../Include
)
target_link_libraries(${PROJECT_NAME}
	HLLib
)

if (BUILD_STATIC)
	target_link_options(${PROJECT_NAME} PRIVATE -static-libgcc -static)
	set_target_properties(${PROJECT_NAME} PROPERTIES LINK_SEARCH_START_STATIC ON)
	set_target_properties(${PROJECT_NAME} PROPERTIES LINK_SEARCH_END_STATIC ON)
endif()
