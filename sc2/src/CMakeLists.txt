add_subdirectory(regex)
add_subdirectory(libs)
add_subdirectory(uqm)

if(NOT HAVE_GETOPT_LONG)
    add_subdirectory(getopt)
endif()

add_executable(urquan
    config.h
    endian_uqm.h
    options.c options.h
    port.c port.h
    types.h
    uqm.c
    uqmversion.h)

target_link_libraries(urquan regex)
target_link_libraries(urquan libs)
target_link_libraries(urquan uqm)

if(NOT HAVE_GETOPT_LONG)
    target_link_libraries(urquan getopt)
endif()

include_directories(
    ${urquan_SOURCE_DIR}/src
    ${SDL2_INCLUDE_DIR}
    ${SDL2_MIXER_INCLUDE_DIR}
)
