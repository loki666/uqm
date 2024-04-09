add_library(math STATIC random.c random2.c sqrt.c)

target_include_directories(math PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)
