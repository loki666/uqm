add_library(input_sdl STATIC input.c keynames.c vcontrol.c)

target_include_directories(input_sdl PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)

target_link_libraries(input_sdl SDL2::SDL2)
