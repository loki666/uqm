add_subdirectory(sdl)

add_library(graphics STATIC boxint.c clipline.c cmap.c context.c drawable.c filegfx.c
bbox.c dcqueue.c gfxload.c
font.c frame.c gfx_common.c intersec.c loaddisp.c
pixmap.c resgfx.c tfb_draw.c tfb_prim.c widgets.c)

target_include_directories(graphics PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)

target_link_libraries(graphics PRIVATE graphics_sdl)
target_link_libraries(graphics PRIVATE resource)
target_link_libraries(graphics PRIVATE png)
