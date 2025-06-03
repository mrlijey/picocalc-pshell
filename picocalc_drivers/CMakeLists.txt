# Generated Cmake Pico project file

cmake_minimum_required(VERSION 3.13)

set(CMAKE_C_STANDARD 11)

project(picocalc_drivers
        VERSION 0.0.1
        DESCRIPTION "picocalc drivers for lcd, keyboard, terminal"
        )

add_library(picocalc_drivers INTERFACE)

target_sources(picocalc_drivers INTERFACE
        keyboard.c
        lcd.c
        term.c
        draw.c
        )

target_link_libraries(picocalc_drivers INTERFACE  pico_stdlib hardware_spi hardware_i2c)

target_include_directories(picocalc_drivers INTERFACE ${CMAKE_CURRENT_LIST_DIR})
