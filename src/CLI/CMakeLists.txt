ADD_TARGET(
        MODE EXE
        RET_TARGET_NAME lua
        LIB
        My::MyLua_core
        SOURCE
        "lua.rc"
        INC_PRIVATE
        "${PROJECT_SOURCE_DIR}/src/common"
        "${PROJECT_SOURCE_DIR}/include/MyLua"
)

SET_TARGET_PROPERTIES(${lua} PROPERTIES OUTPUT_NAME lua CLEAN_DIRECT_OUTPUT 1)