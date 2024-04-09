add_subdirectory(mixer)
add_subdirectory(decoders)

add_library(sound STATIC audiocore.c fileinst.c resinst.c sound.c sfx.c music.c stream.c trackplayer.c)

target_include_directories(sound PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)

target_link_libraries(sound PRIVATE sound_mixer)
target_link_libraries(sound PRIVATE sound_decoders)
