cmake_minimum_required(VERSION 3.12)
project(HLLib)

add_compile_options(-fpic)

if (BUILD_STATIC)
	add_library(${PROJECT_NAME} STATIC)
else()
	add_library(${PROJECT_NAME} SHARED)
endif()
target_sources(${PROJECT_NAME}
	PRIVATE
	BSPFile.cpp
	Checksum.cpp
	DebugMemory.cpp
	DirectoryFile.cpp
	DirectoryFolder.cpp
	DirectoryItem.cpp
	Error.cpp
	FileMapping.cpp
	FileStream.cpp
	GCFFile.cpp
	GCFStream.cpp
	HLLib.cpp
	Mapping.cpp
	MappingStream.cpp
	MemoryMapping.cpp
	MemoryStream.cpp
	NCFFile.cpp
	NullStream.cpp
	PAKFile.cpp
	Package.cpp
	ProcStream.cpp
	SGAFile.cpp
	Stream.cpp
	StreamMapping.cpp
	Utility.cpp
	VBSPFile.cpp
	VPKFile.cpp
	WADFile.cpp
	Wrapper.cpp
	XZPFile.cpp
	ZIPFile.cpp
)
