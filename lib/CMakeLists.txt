cmake_minimum_required(VERSION 3.8)
find_package( PythonLibs 2.7 REQUIRED )
find_package( PythonInterp 2.7 REQUIRED )
include_directories(${PYTHON_INCLUDE_DIRS})
add_library(online_get_lib online_get.cpp invoice.py ${PYTHON_INCLUDE_DIRS})
set_target_properties(online_get_lib
        PROPERTIES PREFIX ""
        SUFFIX ".so"
                                   )
