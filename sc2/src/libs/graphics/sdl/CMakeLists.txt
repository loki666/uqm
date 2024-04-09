add_library(graphics_sdl STATIC opengl.c palette.c primitives.c pure.c sdl2_pure.c
sdl_common.c sdl1_common.c sdl2_common.c
scalers.c 2xscalers.c
2xscalers_mmx.c 2xscalers_sse.c 2xscalers_3dnow.c
nearest2x.c bilinear2x.c biadv2x.c triscan2x.c hq2x.c
canvas.c png2sdl.c sdluio.c rotozoom.c)

target_include_directories(graphics_sdl PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)

target_link_libraries(graphics_sdl PRIVATE SDL2::SDL2)
