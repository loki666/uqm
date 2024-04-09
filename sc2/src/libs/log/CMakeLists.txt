add_library(log STATIC uqmlog.c msgbox_stub.c)

target_include_directories(log PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)
