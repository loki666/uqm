set(SOUND_DECODERS_SRC decoder.c aiffaud.c wav.c dukaud.c modaud.c)
if(VORBIS_FOUND)
    list(APPEND SOUND_DECODERS_SRC oggaud.c)
endif()

add_library(sound_decoders STATIC ${SOUND_DECODERS_SRC})

target_include_directories(sound_decoders PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)

target_link_libraries(sound_decoders PRIVATE mikmod)

if(VORBIS_FOUND)
    target_link_libraries(sound_decoders PRIVATE ${VORBIS_LIBRARIES})
endif()
