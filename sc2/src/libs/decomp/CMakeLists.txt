add_library(decomp STATIC lzdecode.c lzencode.c update.c)

target_include_directories(decomp PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)
