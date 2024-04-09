add_library(uqm_planets STATIC 
    calc.c
    cargo.c
    devices.c
    gentopo.c
    lander.c
    orbits.c
    oval.c
    pl_stuff.c
    planets.c
    plangen.c
    pstarmap.c
    report.c
    roster.c
    scan.c
    solarsys.c
    surface.c
    generate/genand.c
    generate/genburv.c
    generate/genchmmr.c
    generate/gencol.c
    generate/gendefault.c
    generate/gendru.c
    generate/genilw.c
    generate/genmel.c
    generate/genmyc.c
    generate/genorz.c
    generate/genpet.c
    generate/genpku.c
    generate/genrain.c
    generate/gensam.c
    generate/genshof.c
    generate/gensly.c
    generate/gensol.c
    generate/genspa.c
    generate/gensup.c
    generate/gensyr.c
    generate/genthrad.c
    generate/gentrap.c
    generate/genutw.c
    generate/genvault.c
    generate/genvux.c
    generate/genwreck.c
    generate/genyeh.c
    generate/genzfpscout.c
    generate/genzoq.c
)

target_include_directories(uqm_planets PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)

target_link_libraries(uqm_planets PRIVATE math)
target_link_libraries(uqm_planets PRIVATE uqm)
target_link_libraries(uqm_planets PRIVATE graphics)

