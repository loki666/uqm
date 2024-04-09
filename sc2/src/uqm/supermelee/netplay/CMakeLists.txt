add_library(uqm_supermelee_netplay STATIC 
    checkbuf.c checksum.c crc.c netconnection.c netinput.c netmelee.c netmisc.c
    netoptions.c netrcv.c netsend.c netstate.c notify.c notifyall.c
    packet.c packethandlers.c packetsenders.c packetq.c
    proto/npconfirm.c proto/ready.c proto/reset.c
)

target_include_directories(uqm_supermelee_netplay PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)

target_link_libraries(uqm_supermelee_netplay PRIVATE network)
target_link_libraries(uqm_supermelee_netplay PRIVATE uqm)
