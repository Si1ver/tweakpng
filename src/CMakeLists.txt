find_package(ZLIB REQUIRED)
find_package(PNG REQUIRED)

add_executable(tweak_png WIN32)

target_sources(tweak_png PRIVATE
    charset.cpp
    chunk.cpp
    iccprof.cpp
    pngtodib.cpp
    tweakpng.cpp
    viewer.cpp
    pngtodib.h
    resource.h
    tweakpng.h
    twpng-config.h
    tweakpng.rc
    tweakpng.manifest
    icon_1.ico
    icon_2.ico
    drag2.cur
)

target_link_libraries(tweak_png PRIVATE ZLIB::ZLIB)
target_link_libraries(tweak_png PRIVATE PNG::PNG)
target_link_libraries(tweak_png PRIVATE comctl32.lib)
