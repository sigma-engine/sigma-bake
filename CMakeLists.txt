cmake_minimum_required(VERSION 3.5)
project(sigma-bake)

add_executable(sigma-bake
    src/bake_material.cpp
    src/bake_mesh.cpp
    src/bake_shader.cpp
    src/bake_texture.cpp
    src/main.cpp
    src/glm_json.cpp
    src/glm_json.hpp
)

target_include_directories(sigma-bake
PRIVATE
    src
)

target_link_libraries(sigma-bake
PRIVATE
    sigma-core
    stb::stb_image
    nlohmann_json::nlohmann_json
    assimp::assimp
)
