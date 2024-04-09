add_library(network STATIC
    netport.c network_bsd.c
    connect/connect.c connect/listen.c connect/resolve.c
    netmanager/ndesc.c netmanager/netmanager_bsd.c
    socket/socket.c socket/socket_bsd.c)

target_include_directories(network PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)
