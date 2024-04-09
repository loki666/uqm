add_library(regex STATIC regex.c)

target_include_directories(regex PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)
