# `platform_a`

A small library mimicking an implementation of the interface defined in [`common`](https://github.com/cmake-paul/common).

If the above does not ring any bells, check out [CMake PAUL's organization page](https://github.com/cmake-paul) first.

## Usage

In a parent project, include this repository via

```cmake
include(FetchContent)

FetchContent_Declare(
    PlatformA
    GIT_REPOSITORY https://github.com/cmake-paul/platform_a.git
    GIT_TAG main
)

FetchContent_MakeAvailable(PlatformA)
```

That's it, no further steps required.
Utility libraries that are used throughout a parent project will automatically pick up the platform.
