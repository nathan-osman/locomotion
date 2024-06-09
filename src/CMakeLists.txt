set(SRC
    camera.cpp
    camera.hpp
    main.cpp
)

add_executable(locomotion ${SRC})

set_target_properties(locomotion PROPERTIES
    CXX_STANDARD          17
    CXX_STANDARD_REQUIRED ON
)

target_link_libraries(locomotion
    ${LIBAV_LIBRARIES}
    ${LIBCAMERA_LIBRARIES}
)

target_include_directories(locomotion PUBLIC
    ${LIBAV_INCLUDE_DIRS}
    ${LIBCAMERA_INCLUDE_DIRS}
)

target_compile_options(locomotion PUBLIC
    ${LIBAV_CFLAGS_OTHER}
    ${LIBCAMERA_CFLAGS_OTHER}
)
