◎ 建立Ubuntu in VirtualBox
http://blog.xuite.net/yh96301/blog/220731233-VirtualBox+4.3%E5%AE%89%E8%A3%9DUbuntu+14.04(%E4%B8%80)

※ 相關文章參考：
---------------------------
如何複製文字/檔案到 Virtualbox 內
https://tnlin.wordpress.com/2015/07/04/
---------------------------

◎ 更新系統

安裝完畢後，更新整個作業系統內軟體版本

1. 確認更新軟體列表
>> sudo apt-get update

2. 下載並更新軟體 
>> sudo apt-get upgrade

◎ 安裝Eclipse，編譯C語言

1. 安裝Eclipse-CDT使用終端機，輸入以下字串
>> sudo apt-get install eclipse eclipse-cdt g++
※ 注意，在安裝過程中CDT可能無法正常運作，需完全刪除CDT後重新安裝；或另外建立Workspace重設資訊。

2. 啟動專案，並設定正確的專案include路徑
file -> properties -> C/C++ Build -> Settings -> Include -> Add ( 路徑/usr/include )


※ 相關文章參考：
---------------------------
C/Cpp IDE
http://wiki.ubuntu.org.cn/index.php?title=C_Cpp_IDE&variant=zh-tw
---------------------------

◎ 安裝OpenCV
http://docs.opencv.org/2.4/doc/tutorials/introduction/linux_install/linux_install.html#linux-installation
https://www.youtube.com/watch?v=Cci256oj8dg

1. 必要安裝，透過apt-get

[compiler] 
>> sudo apt-get install build-essential
[required] 
>> sudo apt-get install cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev
[optional] 
>> sudo apt-get install python-dev python-numpy libtbb2 libtbb-dev libjpeg-dev libpng-dev libtiff-dev libjasper-dev libdc1394-22-dev

2. 建立檔案夾儲存下載資料

>> mkdir opencv
>> cd opencv

3. 下載OpenCV

>> wget -O [download file name] [download URL]
※ https://github.com/Itseez/opencv/archive/2.4.13.zip

4. 解壓縮OpenCV

>> unzip [download file name]

5. 重編譯函式庫

>> cd [download file name]
>> mkdir release
>> cd release

6. 設計編譯命令cmake

A. 表準句型 
>> cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local ..

B. 包括C語言範例
>> cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local -D WITH_TBB=ON -D WITH_V4L=ON -D WITH_OPENGL=ON -D INSTALL_C_EXAMPLES=ON -D BUILE_EXAMPLES=ON ..

※ 參數 -D WITH_QT 需有QT版本，此部分有待確認使用狀態
※ TBB, Threading Building Blocks
https://www.threadingbuildingblocks.org/

7. 編譯
正確執行cmake後，會產生可編譯的make file

>> make

8. 安裝

編譯完成後，將編譯內容安裝置系統
>> sudo make install
設定opencv.config file
>> sudo sh -c 'echo "/usr/local/lib" > /etc/ld.so.conf.d/opencv.conf'
>> sudo ldconfig

安裝完畢後重開主機，使系統正式啟動。

※ 相關文章參考：
---------------------------
Installing OpenCV 2.2 in Ubuntu 11.04
http://www.samontab.com/web/2011/06/installing-opencv-2-2-in-ubuntu-11-04/
---------------------------

9 執行範例程式
重開後啟動終端機，進入下載檔案中的sample

>> cd /opencv/opencv-2.4.13/samples/cpp/

10. 編譯範例程式 (僅供參考)

>> g++ houghlines.cpp -o application 'pkg-config --cflags --libs opencv'
>> g++ 'pkg-config --cflags opencv' houghlines.cpp 'pkg-config --libs opencv' -o application 

※ 相關文章參考：
---------------------------
How to compile OpenCV sample code ?
http://www.learnopencv.com/how-to-compile-opencv-sample-code/

pkg-config --cflags opencv: No such file or directory
http://stackoverflow.com/questions/20625096/
---------------------------




