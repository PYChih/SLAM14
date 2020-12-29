# 宣告要求的cmake最低版本
cmake_minimum_required( VERSION 2.8)

# 宣告一個cmake專案
project( HelloSLAM )

# 增加一個可執行程式
# 語法: add_executable( 程式名稱 原始程式碼檔案)
add_executable( helloSLAM helloSLAM.cpp)
# 增加一個函數庫
# 語法: add_library( 函數庫名稱 原始程式碼檔案)
add_library( hello libHelloSLAM.cpp)

# 增加一個共用函數庫
# 語法: add_library( 函數庫名稱 SHARED 原始碼檔案)

add_executable( useHello useHello.cpp)
target_link_libraries( useHello hello)