cmake_minimum_required(VERSION 2.8.8)

set(DSN_ROOT "E:/rDSN")
if(NOT EXISTS "${DSN_ROOT}/")
    message(FATAL_ERROR "Please make sure that ${DSN_ROOT} exists.")
endif()

include("${DSN_ROOT}/bin/dsn.cmake")

set(DSN_BUILD_RUNTIME 0)

add_subdirectory(src)