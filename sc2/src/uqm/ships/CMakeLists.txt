add_library(uqm_ships STATIC
    androsyn/androsyn.c
    arilou/arilou.c
    blackurq/blackurq.c
    chenjesu/chenjesu.c
    chmmr/chmmr.c
    human/human.c
    druuge/druuge.c
    ilwrath/ilwrath.c
    lastbat/lastbat.c
    melnorme/melnorme.c
    mmrnmhrm/mmrnmhrm.c
    mycon/mycon.c
    orz/orz.c
    pkunk/pkunk.c
    probe/probe.c
    shofixti/shofixti.c
    sis_ship/sis_ship.c
    slylandr/slylandr.c
    spathi/spathi.c
    supox/supox.c
    syreen/syreen.c
    thradd/thradd.c
    umgah/umgah.c
    urquan/urquan.c
    utwig/utwig.c
    vux/vux.c
    yehat/yehat.c
    zoqfot/zoqfot.c
)

target_include_directories(uqm_ships PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)
