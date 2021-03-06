cmake_minimum_required(VERSION 3.5)
project(cemblua)

set(CMAKE_C_STANDARD 99)
set(CMAKE_CXX_STANDARD 11)

# needs -g to debug.
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -g -Wall -Wno-deprecated-declarations")

include_directories(
    source
    lua-5.3.5/src
    )

# Source files.
add_executable(cemblua
    source/main.c
    source/common.c
    source/exec.c
    source/board.c
    source/luainterop.c
    source/ctolua.c
    source/luatoc
    lua-5.3.5/src/lapi.c
    lua-5.3.5/src/lauxlib.c
    lua-5.3.5/src/lbaselib.c
    lua-5.3.5/src/lbitlib.c
    lua-5.3.5/src/lcode.c
    lua-5.3.5/src/lcorolib.c
    lua-5.3.5/src/lctype.c
    lua-5.3.5/src/ldblib.c
    lua-5.3.5/src/ldebug.c
    lua-5.3.5/src/ldo.c
    lua-5.3.5/src/ldump.c
    lua-5.3.5/src/lfunc.c
    lua-5.3.5/src/lgc.c
    lua-5.3.5/src/linit.c
    lua-5.3.5/src/liolib.c
    lua-5.3.5/src/llex.c
    lua-5.3.5/src/lmathlib.c
    lua-5.3.5/src/lmem.c
    lua-5.3.5/src/loadlib.c
    lua-5.3.5/src/lobject.c
    lua-5.3.5/src/lopcodes.c
    lua-5.3.5/src/loslib.c
    lua-5.3.5/src/lparser.c
    lua-5.3.5/src/lstate.c
    lua-5.3.5/src/lstring.c
    lua-5.3.5/src/lstrlib.c
    lua-5.3.5/src/ltable.c
    lua-5.3.5/src/ltablib.c
    lua-5.3.5/src/ltm.c
    # lua-5.3.5/src/lua.c
    # lua-5.3.5/src/luac.c
    lua-5.3.5/src/lundump.c
    lua-5.3.5/src/lutf8lib.c
    lua-5.3.5/src/lvm.c
    lua-5.3.5/src/lzio.c
    )
