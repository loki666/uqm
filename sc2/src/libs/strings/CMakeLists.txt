add_library(strings STATIC getstr.c sfileins.c sresins.c stringhashtable.c strings.c unicode.c)

target_include_directories(strings PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)

target_link_libraries(strings PRIVATE resource)
target_link_libraries(strings PRIVATE m)
