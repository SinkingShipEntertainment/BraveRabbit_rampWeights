cmake_minimum_required(VERSION 3.1)
project(rampWeights)

set(CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake)

add_subdirectory(source)

install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/modules/rampWeights/icons DESTINATION ./rampWeights)
install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/modules/rampWeights/scripts DESTINATION ./rampWeights)
install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/modules/rampWeights/presets DESTINATION ./rampWeights)
install(FILES ${CMAKE_CURRENT_SOURCE_DIR}/rampWeights.mod DESTINATION .)
