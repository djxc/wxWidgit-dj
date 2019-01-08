cmake_minimum_required(VERSION 3.2)
PROJECT(wxWidgets)
aux_source_directory(. DIR_SRC)
add_subdirectory(src)
add_executable(main ${DIR_SRC})

#引入wxWidgets的库
find_package(wxWidgets REQUIRED COMPONENTS net core base)
include(${wxWidgets_USE_FILE})

target_link_libraries(main ${wxWidgets_LIBRARIES} myFrame)
