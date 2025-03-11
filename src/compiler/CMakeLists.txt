ADD_TARGET(
        MODE EXE
        RET_TARGET_NAME luac
        SOURCE
        "luac.rc"
        LIB
        My::MyLua_common
        INC
        "${PROJECT_SOURCE_DIR}/include"
)

SET_TARGET_PROPERTIES(${luac} PROPERTIES OUTPUT_NAME luac CLEAN_DIRECT_OUTPUT 1)