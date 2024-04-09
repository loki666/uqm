add_library(sound_mixer STATIC mixer.c
nosound/audiodrv_nosound.c sdl/audiodrv_sdl.c)

target_include_directories(sound_mixer PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)

target_link_libraries(sound_mixer PUBLIC SDL2::SDL2)
