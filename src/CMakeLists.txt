set (INCLUDE_ROOT
${PROJECT_SOURCE_DIR}/src/include)
set (SRC_ROOT ${PROJECT_SOURCE_DIR}/src)

set (TARGET PhysicsUtils)

set (SRC
    ${SRC_ROOT}/entrypoint.cpp
)

add_library(${TARGET} SHARED ${SRC})

target_include_directories(${TARGET}
    PUBLIC ${INCLUDE_ROOT}
    PRIVATE ${SRC_ROOT}
)

set_target_properties(${TARGET} PROPERTIES
    LIBRARY_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}
)