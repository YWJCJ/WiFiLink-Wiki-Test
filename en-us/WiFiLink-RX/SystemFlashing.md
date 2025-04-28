# System Flashing

> [!Warning|style:flat|label：警告]
>
> Flashing the system will erase all files on the WiFiLink-RX's internal storage (eMMC) and TF card. Please back up important data in advance.
>

Video URL:

## A. Obtaining the System Image file

### OpenIPC

1. Open the link below, select the target version, and locate the image file with the .img.xz extension.

   https://github.com/OpenIPC/sbc-groundstations/releases

   ![OpenIPC 系统镜像 1](image/OpenIPC系统镜像1.png)

2. Extract the downloaded compressed file to obtain a system image file.

   ![OpenIPC 系统镜像 2](image/OpenIPC系统镜像2.png)

### Ruby FPV

1. .Go to the Ruby FPV official website's Download page(https://rubyfpv.com/downloads.php), scroll down to find the latest system image files. Select the image file for RunCam VRx, and click to download.

   !> Note: The system version of the WiFiLink-RX must match the version on the air unit; otherwise, connection issues may occur.

   ![RubyFPV系统镜像1](image/RubyFPV系统镜像1.png)

2. Extract the downloaded compressed file to obtain a system image file.

   ![RubyFPV系统镜像2](image/RubyFPV系统镜像2.png)

## B. Flashing Software

1. Click the link below to download the compressed Driver&Tool compressed file.

   GoogleDrive: https://drive.google.com/drive/folders/1moljMrfbCeSgvW7LQA1RAOpFrKZshpGI?usp=sharing

   ![烧录软件1](image/烧录软件1.png)

2. Extract the downloaded compressed file, to obtain flashing software and driver.

   ![烧录软件2](image/烧录软件2.png)

## C. Installing Driver

1. Open DriverAssistant_v5.0 folder, find and double click DriverInstall.exe to execute it. Click Install to continue.

   ![驱动安装1](image/驱动安装1.png)

2. It takes a few seconds to finish.

   ![驱动安装2](image/驱动安装2.png)

## D. Flashing System Image File

1. Open the RKDevTool_Release_v2.96 folder and locate the RKDevTool.exe file. Double-click to execute it.

   ![镜像烧录1](image/镜像烧录1.png)

2. Since the WiFiLink-RX is not yet connected to the computer, the RKDevTool flashing tool will display "No Devices Found" in the lower-left corner.

   ![镜像烧录2](image/镜像烧录2.png)

3. Make sure the WiFiLink-RX is properly connected to the antenna, and that the TF card is removed (to prevent data loss).

4. Use a SIM eject tool or a small screwdriver to press and hold the flash button, then connect DC power. Wait for 2 seconds, then release the button.

5. Connect the WiFiLink-RX to the computer via Type-C data cable.

   ![镜像烧录5](image/镜像烧录5.png)

6. If the previous steps were completed correctly, the WiFiLink-RX will enter flashing mode. The flashing tool will display "Found One MASKROM Device" on the interface.

   ![镜像烧录6](image/镜像烧录6.png)

7. When RX enters a flashing mode (MASKROM available), the paths for Loader and Image need to be changed. Click the area shown in the image below to select the "Loader" file.

   ![镜像烧录7](image/镜像烧录7.png)

8. Locate Drive&Tool folder and select rk356x_spl_loader_ddr1056_v1.10.111.bin to open.

   ![镜像烧录8](image/镜像烧录8.png)

9. Click the area for Image as well.

   ![镜像烧录9](image/镜像烧录9.png)

10. Select the system image file to be flashed, then click "Open." (In this example, version 10.7 is used.)

   ![镜像烧录10RubyFPV](image/镜像烧录10RubyFPV.png)

11. After selecting the paths for both Loader and Image, please must tick Write by Address.

   ![镜像烧录11RubyFPV](image/镜像烧录11RubyFPV.png)

12. Click to execute, and the tool will start flashing the firmware for WiFiLink RX.

   ![镜像烧录12RubyFPV](image/镜像烧录12RubyFPV.png)

13. It takes about two minutes to finish flashing.

   ![镜像烧录13RubyFPV](image/镜像烧录13RubyFPV.png)
