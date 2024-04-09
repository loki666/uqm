add_library(heap STATIC heap.c)

target_include_directories(heap PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)
