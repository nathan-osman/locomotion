set(SRC
    main.cpp
)

add_executable(locomotion ${SRC})

set_target_properties(locomotion PROPERTIES
    CXX_STANDARD          14
    CXX_STANDARD_REQUIRED ON
)

target_link_libraries(locomotion ${CAMERA_LIBRARIES})
target_include_directories(locomotion PUBLIC ${CAMERA_INCLUDE_DIRS})
target_compile_options(locomotion PUBLIC ${CAMERA_CFLAGS_OTHER})
