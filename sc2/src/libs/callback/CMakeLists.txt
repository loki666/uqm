add_library(callback STATIC alarm.c async.c callback.c)

target_include_directories(callback PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)

target_link_libraries(callback PRIVATE SDL2::SDL2)
target_link_libraries(callback PRIVATE heap)
