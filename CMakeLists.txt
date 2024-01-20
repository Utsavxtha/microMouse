cmake_minimum_required(VERSION 3.12)

include(pico_sdk_import.cmake)

project(cytron)

pico_sdk_init()

add_executable(cytron
    cytron.c
)

# Add pico_stdlib library which aggregates commonly used features
target_link_libraries(cytron pico_stdlib hardware_uart )

# create map/bin/hex/uf2 file in addition to ELF.
pico_add_extra_outputs(cytron)