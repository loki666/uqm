add_subdirectory(comm)
add_subdirectory(planets)
add_subdirectory(ships)
add_subdirectory(supermelee)

add_library(uqm STATIC 
    battle.c
    battlecontrols.c
    border.c
    build.c
    cleanup.c
    clock.c
    cnctdlg.c
    collide.c
    comm.c 
    commanim.c
    commglue.c
    confirm.c
    cons_res.c
    credits.c
    cyborg.c
    demo.c
    displist.c
    dummy.c
    encount.c
    flash.c
    fmv.c
    galaxy.c
    gameev.c
    gameinp.c
    gameopt.c
    gendef.c
    getchar.c
    globdata.c
    gravity.c
    grpinfo.c
    hyper.c
    init.c
    intel.c
    intro.c
    ipdisp.c
    load_legacy.c
    load.c
    loadship.c
    master.c
    menu.c
    misc.c
    oscill.c
    outfit.c
    pickship.c
    plandata.c
    process.c
    restart.c
    save.c
    settings.c
    setup.c
    setupmenu.c
    ship.c
    shipstat.c
    shipyard.c
    sis.c
    sounds.c
    starbase.c
    starcon.c
    starmap.c
    state.c
    status.c
    tactrans.c
    trans.c
    uqmdebug.c
    util.c
    velocity.c
    weapon.c
)

target_include_directories(uqm PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)

target_link_libraries(uqm uqm_commm)
target_link_libraries(uqm uqm_planets)
target_link_libraries(uqm uqm_ships)
target_link_libraries(uqm uqm_supermelee)
