cmake_minimum_required(VERSION 3.1)

project(RectangleBinPack)


include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include)

file(GLOB SOURCES src/*.cpp)

# rely on BUILD_SHARED_LIBS for STATIC/SHARED lib
add_library(${PROJECT_NAME} ${SOURCES})

install(TARGETS ${PROJECT_NAME} DESTINATION lib/${PROJECT_NAME})

file(GLOB HEADERS include/*.h)
install(FILES ${HEADERS} DESTINATION include/${PROJECT_NAME})