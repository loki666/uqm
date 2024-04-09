add_library(threads STATIC thrcommon.c sdl/sdlthreads.c)

target_include_directories(threads PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)

target_link_libraries(threads PUBLIC SDL2::SDL2)
target_link_libraries(threads PRIVATE callback)
