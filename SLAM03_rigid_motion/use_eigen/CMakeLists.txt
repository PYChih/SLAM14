# 宣告要求的cmake最低版本
cmake_minimum_required( VERSION 2.8)

# 宣告一個cmake專案
project( useEigen )

set(CMAKE_BUILD_TYPE "Release")
set(CMAKE_CXX_FLAGS "-O3")

# 添加Eigen頭文件
include_directories("/usr/include/eigen3")

# 增加一個可執行程式
# 語法: add_executable( 程式名稱 原始程式碼檔案)
add_executable( eigenMatrix eigenMatrix.cpp)