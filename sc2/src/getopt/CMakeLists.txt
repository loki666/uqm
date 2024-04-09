add_library(getopt STATIC getopt.c getopt1.c)

target_include_directories(getopt PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)
