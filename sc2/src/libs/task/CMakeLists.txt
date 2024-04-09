add_library(task STATIC tasklib.c)

target_include_directories(task PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)
