add_library(list STATIC list.c)

target_include_directories(list PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)
