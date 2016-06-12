◎ NAVIDA Jetson TK1
http://docs.nvidia.com/jetpack-tk1/1_2/index.html#developertools/mobile/jetpack/jetpack_main.htm

※ 相關文章參考：
---------------------------
【開箱文】NVIDIA Jetson TK1
http://www.coolpc.com.tw/phpBB2/viewtopic.php?f=70&t=147025

Jetson TK1
http://elinux.org/Jetson_TK1

Embedded Download Center
https://developer.nvidia.com/embedded/downloads#?tx=$product,jetson_tk1

Jetson/Installing OpenCV
http://elinux.org/Jetson/Installing_OpenCV

Jetson TK1 Development Kit User Guide
http://developer.download.nvidia.com/embedded/jetson/TK1/docs/2_GetStart/Jeston_TK1_User_Guide.pdf

Video：
NVidia Jetson TK1 Unboxing and booting
https://www.youtube.com/watch?v=8iJ-h96syKE

NVIDIA Jetson TK1 Samsung SSD Unboxing and Install
https://www.youtube.com/watch?v=poCV36nbAZM
---------------------------

◎ 零組件

從文件說明確認，原始的TK1盒內缺乏以下東西：

1. 鍵盤、滑鼠，礙於設備僅一個USB port，需使用USB hub去銜接設備。
2. HDMI輸出，若要輸出至無法使用HDMI設備，應準備對應的轉換器。
3. Ethernet 網路線。

◎ 嵌入式系統簡介

本段內容是與有實務經驗網友討論之成果。
TK1的啟動運作如下：
0. 依據啟動用的按鈕決定使用的Booting模式
1. Normal 模式：
- 若系統尚未安裝，自Flash rom中取得系統，將系統安裝置Ram的作業系統區域。
- 若喜統已安裝，自作業系統區域啟動系統。
2. Recovry 模式
- 啟動BootLoader，提供使用者載入作業系統映像檔並存入Flash rom。
- 在此區域，使用者可以下達Erase、Update等，對作業系統處理的程序。

由於Booting系統規範，原則上可區分為BootLoader區域、OS區域；前者是儲存管理、安裝作業系統事宜的軟體，後者為實際安裝完畢並可啟動的作業系統。
實際使用時用後者區域，其儲存資料亦在此處；若重新安裝將會清空OS區域，無法對BootLoader區域處理。

◎ Install Jetpack in Jetson TK1 

1. Install Ubuntu in x86 NB / PC。
	- Windows OS, use VirtualBox install Ubuntu and execute Jetpack

2. Execute Jetpack, and Jetpack will install data in Ubuntu OS.

3. Use USB to link Jetson TK1.

※ VM安裝注意：
在連結MicroUSB後，要先去VM內設定啟用USB連結，並確保VM安裝完畢USB連結軟體，並於VM內設定掛入USB後，可在Ubuntu內看到USB啟用。

4. Flash Jetson TK1 OS and setting IP address.
	- Jetpack will using internet to install CUDA and OpenCV library.

※ 相關文章參考：
---------------------------
Getting Started with Jetson TK1 and the ZED
https://www.stereolabs.com/blog/index.php/2015/09/24/getting-started-with-jetson-tk1-and-zed/

Video：
JetPack TK1 1.1 Install and Flash on NVIDIA Jetson TK1
https://www.youtube.com/watch?v=TB-bIayjBbc

Jetpack 2.0 Install on NVIDIA Jetson TK1
https://www.youtube.com/watch?v=J-ma4aZyqfY

Jetson focused Linux tips and tricks
https://devtalk.nvidia.com/default/topic/785551/embedded-systems/my-jetson-focused-linux-tips-and-tricks/
---------------------------

◎ Jetson TK1 IDE

原則上，安裝Jetpack的過程，便會在Ubuntu內安裝好Nsight Eclipse。
如果沒有，則安裝CUDA即會安裝Nsight Eclipse。

※ 但要注意，Jetpack安裝過程並不包含提供OpenCV等函數庫，因此若要編譯此類軟體，需另外安裝。