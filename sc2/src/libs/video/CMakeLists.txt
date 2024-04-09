add_library(video STATIC vfileins.c vresins.c video.c videodec.c vidplayer.c dukvid.c
legacyplayer.c)

target_include_directories(video PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)
