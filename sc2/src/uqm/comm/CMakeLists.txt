add_library(uqm_commm STATIC 
    arilou/arilouc.c
    blackur/blackurc.c
    chmmr/chmmrc.c
    comandr/comandr.c
    druuge/druugec.c
    ilwrath/ilwrathc.c
    melnorm/melnorm.c
    mycon/myconc.c
    orz/orzc.c
    pkunk/pkunkc.c
    rebel/rebel.c
    shofixt/shofixt.c
    slyhome/slyhome.c
    slyland/slyland.c
    spahome/spahome.c
    spathi/spathic.c
    starbas/starbas.c
    supox/supoxc.c
    syreen/syreenc.c
    talkpet/talkpet.c
    thradd/thraddc.c
    umgah/umgahc.c
    urquan/urquanc.c
    utwig/utwigc.c
    vux/vuxc.c
    yehat/yehatc.c
    zoqfot/zoqfotc.c
)

target_include_directories(uqm_commm PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)
