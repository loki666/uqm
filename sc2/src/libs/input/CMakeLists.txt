add_subdirectory(sdl)

add_library(input STATIC input_common.c)

target_include_directories(input PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)

target_link_libraries(input PRIVATE input_sdl)
