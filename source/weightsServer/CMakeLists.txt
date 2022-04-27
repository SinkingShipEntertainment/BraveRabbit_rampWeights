
file(GLOB_RECURSE CPP_HEADERS "${CMAKE_CURRENT_SOURCE_DIR}/*.h")
file(GLOB_RECURSE CPP_SOURCES "${CMAKE_CURRENT_SOURCE_DIR}/*.cpp")

set(PLUGIN_NAME weightsServer)

add_library(${PLUGIN_NAME} SHARED ${CPP_HEADERS} ${CPP_SOURCES})

# Link to Maya
target_link_libraries(${PLUGIN_NAME} PRIVATE Maya::Maya)

# Includes Maya and current directory
target_include_directories(${PLUGIN_NAME} PRIVATE Maya::Maya)
target_include_directories(${PLUGIN_NAME} PRIVATE "${CMAKE_CURRENT_SOURCE_DIR}")

maya_set_plugin_properties(${PLUGIN_NAME})

install(TARGETS ${PLUGIN_NAME} LIBRARY DESTINATION rampWeights/plug-ins)
