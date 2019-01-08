aux_source_directory(. DIR_LIB_SRCS)
add_library(myFrame ${DIR_LIB_SRCS})

#wxWidgets库文件的引用
find_package(wxWidgets REQUIRED COMPONENTS net core base)
include(${wxWidgets_USE_FILE})
target_link_libraries(myFrame ${wxWidgets_LIBRARIES})
