if(NETPLAY)
    add_subdirectory(netplay)
endif()

add_library(uqm_supermelee STATIC 
    buildpick.c
    loadmele.c
    melee.c
    meleesetup.c
    pickmele.c
)

target_include_directories(uqm_supermelee PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)

if(NETPLAY)
    target_link_libraries(uqm_supermelee PRIVATE uqm_supermelee_netplay)
endif()
