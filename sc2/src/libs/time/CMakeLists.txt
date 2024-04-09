add_library(time STATIC timecommon.c sdl/sdltime.c)

target_include_directories(time PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)

target_link_libraries(time PUBLIC SDL2::SDL2)
