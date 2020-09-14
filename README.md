# Clion个人使用笔记
# 1 安装
  1. 下载<a href="https://www.jetbrains.com/clion/download" target="_blank">官方安装程序</a>
  2. 笔者使用的是windows版本的，一路默认安装，其他版本可以搜索安装方法。
# 2 环境配置
  ## 2.1 字体
  1） 字体<a href="https://github.com/Ubuntuser2012/Clion_UserNotes/blob/master/font/YaHei.Consolas.1.12.ttf">YaHei&Consolas</a>
  
  ![系统字体设置](https://github.com/Ubuntuser2012/Clion_UserNotes/tree/master/png/font-setting1.png "系统字体设置")
  
  2） 编辑器字体颜色配置
  
  
  ## 2.2 打开方式
  1） *.ui文件打开方式添加
     
  a) 添加额外工具
  ![设置添加工具](https://github.com/Ubuntuser2012/Clion_UserNotes/tree/master/png/tool-qtdesigner-setting1.png "添加工具")
  ![添加Designer](https://github.com/Ubuntuser2012/Clion_UserNotes/tree/master/png/tool-qtdesigner-setting2.png "添加QtDesigner")
  ![使用QtDesigner](https://github.com/Ubuntuser2012/Clion_UserNotes/tree/master/png/rightclick-use-qtdesigner.png "使用QtDesigner")
  
  ## 2.3 插件
  ## 2.4 其他配置
  1） 文件修改之后显示*号
  
  2） 配置Clion启动时不加载项目
  
# 3 编译
  ## 3.1 编译环境配置
  ### 3.1.1 MSVC编译环境
  Clion针对MSVC只支持cl.exe编译器，不支持msbuild.exe。参考官网说明： <a href="https://www.jetbrains.com/help/clion/quick-tutorial-on-configuring-clion-on-windows.html#msvc-compiler" target="_blank">CLion supports the Microsoft Visual C++ compiler that ships with Visual Studio 2013, 2015, 2017, and 2019。</a>
  #### 3.1.1.1 Jom加速编译
  1）  下载Jom或者使用Qt内置的Jom。
  
  2）  配置系统环境环境变量，将jom.exe路径加入到系统Path变量。
  
  3）  配置编译参数如下图所示：
  
     a） CMake options: -G "NMake Makefiles JOM" -DCMAKE_MAKE_PROGRAM="jom安装路径/jom.exe"
     b） Build options: -j8 （数字根据计算机核数配置）
     
     注意：Path环境变量在Clion中不能配置，否则会报错。
     

# 4 调试
  ## 4.1 调试环境配置
  ### 4.1.1 MSVC调试环境配置
  Clion对MSVC调试只支持lldb调试<a href="https://www.jetbrains.com/help/clion/quick-tutorial-on-configuring-clion-on-windows.html#msvc-debugger" target="_blank">LLDB-based MSVC debugger。</a>
  Clion可以配置NatVis调试视图，支持加载NatVis脚本。针对Qt可以使用qt5.natvis脚本以便支持Qt内置变量的调试（QString、QList、QHash等）
  
备注：图后续补上，第一次写不太好见谅~~  
  