cmake_minimum_required(VERSION 3.5)
project(extract-xiso)

string(TOUPPER __${CMAKE_SYSTEM_NAME}__ TARGET_OS)

set(SOURCE_FILES
	extract-xiso.c
)

add_executable(extract-xiso ${SOURCE_FILES})
target_compile_definitions(extract-xiso PRIVATE ${TARGET_OS})
install(TARGETS extract-xiso RUNTIME DESTINATION "${CMAKE_INSTALL_PREFIX}/bin")
