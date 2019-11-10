#要求CMake的最低版本为3.5  
cmake_minimum_required(VERSION 3.5)
#项目名字
project(test)
#c++标准
set(CMAKE_CXX_STANDARD 11)
#头文件路径
include_directories("../3rdparty/glfw/include/")
include_directories("../3rdparty/glfw/deps/")
#依赖库路径，要根据自己的路径做下修改
link_directories("/usr/local/lib")
#指定源代码
set(SOURCE_FILES create_window.cpp glad_gl.c)
#生成目标文件
add_executable(create_win ${SOURCE_FILES})
#链接库文件
target_link_libraries(create_win GL glfw3 X11 pthread Xrandr dl)
