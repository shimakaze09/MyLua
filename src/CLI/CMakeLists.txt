ADD_TARGET(
        MODE EXE
        OUTPUT_NAME lua
        LIB
        My::MyLua_core
        SOURCE
        "lua.rc"
        INC_PRIVATE
        "${PROJECT_SOURCE_DIR}/src/common"
        "${PROJECT_SOURCE_DIR}/include/MyLua"
)