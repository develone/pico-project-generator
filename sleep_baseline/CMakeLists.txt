# Generated Cmake Pico project file

cmake_minimum_required(VERSION 3.13)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)

# Initialise pico_sdk from installed location
# (note this can come from environment, CMake cache etc)
set(PICO_SDK_PATH "/home/devel/sdk/pico-sdk")

# Pull in Raspberry Pi Pico SDK (must be before project)
include(pico_sdk_import.cmake)

project(sleep_baseline C CXX ASM)

# Initialise the Raspberry Pi Pico SDK
pico_sdk_init()

# Add executable. Default name is the project name, version 0.1

add_executable(sleep_baseline sleep_baseline.c )

pico_set_program_name(sleep_baseline "sleep_baseline")
pico_set_program_version(sleep_baseline "0.1")

pico_enable_stdio_uart(sleep_baseline 1)
pico_enable_stdio_usb(sleep_baseline 0)

# Add the standard library to the build
target_link_libraries(sleep_baseline pico_stdlib)

pico_add_extra_outputs(sleep_baseline)

