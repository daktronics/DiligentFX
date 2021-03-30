cmake_minimum_required (VERSION 3.6)

set(SOURCE
    "${CMAKE_CURRENT_SOURCE_DIR}/src/GLTF_PBR_Renderer.cpp"
)

set(INCLUDE
    "${CMAKE_CURRENT_SOURCE_DIR}/interface/GLTF_PBR_Renderer.hpp"
)

target_sources(DiligentFX PRIVATE ${SOURCE} ${INCLUDE})

get_target_relative_dir(Diligent-DiligentFX TARGET_RELATIVE_PATH)

target_include_directories(DiligentFX
PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/interface>
    $<INSTALL_INTERFACE:include/${TARGET_RELATIVE_PATH}/GLTF_PBR_Renderer/interface>
)
