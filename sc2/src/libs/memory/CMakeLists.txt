add_library(memory STATIC w_memlib.c)

target_include_directories(memory PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)
