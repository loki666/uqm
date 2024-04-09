add_library(uio STATIC charhashtable.c defaultfs.c fileblock.c fstypes.c gphys.c io.c
ioaux.c match.c mount.c mounttree.c paths.c physical.c uiostream.c
uioutils.c utils.c stdio/stdio.c zip/zip.c)

target_include_directories(uio PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)

target_link_libraries(uio PRIVATE ${ZLIB_LIBRARIES})
