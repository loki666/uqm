add_library(resource STATIC direct.c filecntl.c getres.c loadres.c stringbank.c
propfile.c resinit.c)

target_include_directories(resource PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)

target_link_libraries(resource PRIVATE graphics)
target_link_libraries(resource PRIVATE strings)
target_link_libraries(resource PRIVATE sound)
