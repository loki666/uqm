add_library(mikmod STATIC drv_nos.c load_it.c load_mod.c load_s3m.c load_stm.c load_xm.c
mdreg.c mdriver.c mloader.c
mlreg.c mlutil.c mmalloc.c mmerror.c mmio.c mplayer.c munitrk.c
mwav.c npertab.c sloader.c virtch.c virtch2.c virtch_common.c)

target_include_directories(mikmod PUBLIC
    ${urquan_SOURCE_DIR}/src
    ${PROJECT_BINARY_DIR}/src
)
