# Goodbye 2013 
project(FishPlayer)

SET(FISHPLAYER_VERSION "0.2.4")

find_package(KDE4 REQUIRED)
include(KDE4Defaults)
include(MacroLibrary)

include_directories(${KDE4_INCLUDES})

include_directories(
    ${CMAKE_CURRENT_BINARY_DIR}
    ${CMAKE_CURRENT_BINARY_DIR}/src
    ${CMAKE_CURRENT_SOURCE_DIR}/src
    )

configure_file(config.h.cmake ${CMAKE_CURRENT_BINARY_DIR}/config.h)

add_subdirectory( src )
add_subdirectory( doc )

