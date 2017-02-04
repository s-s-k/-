1. 安装qt linux 出现错误You are missing the OpenGL include files. Install the mesa-common-dev package，
../../Qt5.1.0/5.1.0/gcc_64/include/QtGui/qopengl.h:110:21: fatal error: GL/gl.h: No such file or directory
执行
> sudo apt-get install mesa-common-dev
2. 出现下面提示：/usr/bin/ld: cannot find -lGL
> 执行下面命令解决：
sudo apt-get install libgl1-mesa-dev libglu1-mesa-dev

3. qt 依赖gcc g++库 

4. qt 学习网站 https://www.devbean.net
5. qt creater 无法输入中文问题
> 安装fcitx for Qt5  动态库   
   sudo apt-get install fcitx-libs-qt5  
   cp /usr/lib/x86_64-linux-gnu/qt5/plugins/platforminputcontexts/libfcitxplatforminputcontextplugin.so ~/Qt5.3.1/Tools/QtCreator/bin/plugins/platforminputcontexts  
   qt版本大于5.5后拷到此目录下 ~/Qt5.7.0/Tools/QtCreator/lib/Qt/plugins/platforminputcontexts  
   解决qtcreater 无法输入中文问题
   cp /usr/lib/x86_64-linux-gnu/qt5/plugins/platforminputcontexts/libfcitxplatforminputcontextplugin.so ~/Qt5.3.1/5.3/gcc_64/plugins/platforminputcontexts  
   解决程序无法输入中文的问题
