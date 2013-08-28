set (CDL_NAME OPRoSCDL)
cmake_minimum_required(VERSION 2.6)
PROJECT(${CDL_NAME})

FILE(GLOB_RECURSE CDLSRCS src/*.cpp)

SET(CMAKE_INSTALL_PREFIX "d:/out/install")

INCLUDE_DIRECTORIES(
        ${PROJECT_SOURCE_DIR}/include
        ${PROJECT_SOURCE_DIR}/src
        ${PROJECT_SOURCE_DIR}/src/system/os        		
)

ADD_LIBRARY(${CDL_NAME} STATIC ${CDLSRCS})

ADD_DEFINITIONS(-DMAKE_COMPONENT_DLL)