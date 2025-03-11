IF (LUA_BUILD_AS_DLL)
    SET(mode SHARED)
    SET(def "LUA_BUILD_AS_DLL")
ELSE ()
    SET(mode STATIC)
    SET(def "")
ENDIF ()

ADD_TARGET(
        MODE ${mode}
        RET_TARGET_NAME liblua
        INC
        "${PROJECT_SOURCE_DIR}/include"
        DEFINE_PRIVATE
        ${def}
        LIB_PRIVATE
        My::MyLua_common
)

SET_TARGET_PROPERTIES(${liblua} PROPERTIES OUTPUT_NAME lua CLEAN_DIRECT_OUTPUT 1)