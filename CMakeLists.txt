include(FetchContent)

FetchContent_Declare(
    common
    GIT_REPOSITORY https://github.com/cmake-paul/common.git
    GIT_TAG main
)

FetchContent_MakeAvailable(common)

add_library(platform_a)

add_subdirectory(include)
add_subdirectory(src)

target_link_libraries(
    platform_a
    PUBLIC
    common
)

register_with_common(IMPLEMENTATION platform_a)
