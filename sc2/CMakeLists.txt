cmake_minimum_required(VERSION 3.20.3)

project(urquan VERSION 0.8.0
            LANGUAGES C)

option(NETPLAY "Set to ON to enable netplay" ON)

include(CheckSymbolExists)
include(CheckTypeSize)

check_symbol_exists(readdir_r   "dirent.h"  HAVE_READDIR_R)
check_symbol_exists(setenv      "stdlib.h"  HAVE_SETENV)
check_symbol_exists(strupr      "string.h"  HAVE_STRUPR)
check_symbol_exists(strcasecmp  "strings.h" HAVE_STRCASECMP_UQM)
check_symbol_exists(stricmp     "string.h"  HAVE_STRICMP)
check_symbol_exists(getopt_long "getopt.h"  HAVE_GETOPT_LONG)
check_symbol_exists(iswgraph    "wctype.h"  HAVE_ISWGRAPH)
check_type_size(wchar_t WCHAR_T)
check_type_size(_Bool   _BOOL)

set(CONTENTDIR "/userdata/roms/uqm")
set(USERDIR "/userdata/saves/uqm")

configure_file(${PROJECT_SOURCE_DIR}/src/config_cmake.h.in
               ${PROJECT_BINARY_DIR}/src/config_cmake.h @ONLY)

add_definitions(-DCMAKE -DGFXMODULE_SDL -DUSE_INTERNAL_MIKMOD -DTHREADLIB_SDL -DHAVE_JOYSTICK -DHAVE_ZIP=1)
if(NETPLAY)
    add_definitions(-DNETPLAY=NETPLAY_FULL)
endif()

list(APPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_LIST_DIR}/cmake")

find_package(SDL2 2.0.0 REQUIRED)
find_package(PNG REQUIRED)
find_package(ZLIB REQUIRED)
find_package(Vorbis REQUIRED)

if(!VORBIS_FOUND)
    add_definitions(-DOVCODEC_NONE)
endif()

add_subdirectory(src)
