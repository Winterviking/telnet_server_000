# set cmake version
cmake_minimum_required(VERSION 3.5.1)

# set project name
project(yourmom LANGUAGES C)

#set c standard and flags
set(CMAKE_C_STANDARD 11)
set(CMAKE_C_FLAGS "-Wall -Werror")
set(myApp_SOURCES 
	${PROJECT_SOURCE_DIR}/main.c
	${PROJECT_SOURCE_DIR}/shape.c
)

add_executable(himom ${myApp_SOURCES})

#link files

#target_sources(himom PRIVATE main.c shape.c shape.h)
INSTALL(TARGETS himom
	RUNTIME DESTINATION bin
)
