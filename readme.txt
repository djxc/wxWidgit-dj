1、编译g++ dj.cpp $(wx-config --libs --cxxflags) -o dj
2、CMakeLists.txt中依赖wxWidgets库，需要加入一下两行：
find_package(wxWidgets REQUIRED COMPONENTS net core base)
include(${wxWidgets_USE_FILE})
然后在修改：target_link_libraries(main ${wxWidgets_LIBRARIES} myFrame)


