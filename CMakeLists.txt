cmake_minimum_required(VERSION 2.8.8)

set(DSN_ROOT "$ENV{DSN_ROOT}")
if((DSN_ROOT STREQUAL "") OR (NOT EXISTS "${DSN_ROOT}/"))
    message(FATAL_ERROR "Please set the environment variable DSN_ROOT to the correct rdsn installation path.")
endif()

include("${DSN_ROOT}/bin/dsn.cmake")
dsn_common_setup()
add_subdirectory(src)
