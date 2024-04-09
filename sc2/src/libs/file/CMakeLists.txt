add_library(file STATIC dirs.c files.c)

target_include_directories(file PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)
