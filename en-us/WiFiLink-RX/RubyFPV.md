# User Manual——RubyFPV

## Connecting to Air Unit

Video URL:

1. Install antennas for both WiFiLink2 and WiFiLink-RX, then power both devices. Connect WiFiLink-RX to a display via HDMI cable.

   ![连接天空端1](image/连接天空端1.png)

2. After powering on devices, press down the 5-way button to open the menu, move to select  Search —> Start Search, press to confirm, and it will search the signal of the transmitter.

   ![RubyFPV连接天空端2](image/RubyFPV连接天空端2.png)

3. When finish the search, please choose “Connect for control”, confirm and connect.

   ![RubyFPV连接天空端3](image/RubyFPV连接天空端3.png)

4. The feed from transmitter will be displayed when it connects successfully.

   ![RubyFPV连接天空端4](image/RubyFPV连接天空端4.png)

## System Flashing

> [!Warning|style:flat]
>
> Flashing the system will erase all files on the WiFiLink-RX’s internal storage (eMMC) and TF card. Please back up important data in advance.
>

Video URL:

### A. Obtaining the System Image file

1. .Go to the Ruby FPV official website’s Download page(https://rubyfpv.com/downloads.php), scroll down to find the latest system image files. Select the image file for RunCam VRx, and click to download.

   !> Note: The system version of the WiFiLink-RX must match the version on the air unit; otherwise, connection issues may occur.

   ![RubyFPV系统镜像1](image/RubyFPV系统镜像1.png)

2. Extract the downloaded compressed file to obtain a system image file.

   ![RubyFPV系统镜像2](image/RubyFPV系统镜像2.png)

### B. Flashing Software

1. Click the link below to download the compressed Driver&Tool compressed file.

   GoogleDrive: https://drive.google.com/drive/folders/1moljMrfbCeSgvW7LQA1RAOpFrKZshpGI?usp=sharing

   ![烧录软件1](image/烧录软件1.png)

2. Extract the downloaded compressed file, to obtain flashing software and driver.

   ![烧录软件2](image/烧录软件2.png)

### C. Installing Driver

1. Open DriverAssistant_v5.0 folder, find and double click DriverInstall.exe to execute it. Click Install to continue. 

   ![驱动安装1](image/驱动安装1.png)

2. It takes a few seconds to finish.

   ![驱动安装2](image/驱动安装2.png)

### D. Flashing System Image File

1. Open the RKDevTool_Release_v2.96 folder and locate the RKDevTool.exe file. Double-click to execute it.

   ![镜像烧录1](image/镜像烧录1.png)

2. Since the WiFiLink-RX is not yet connected to the computer, the RKDevTool flashing tool will display “No Devices Found” in the lower-left corner.

   ![镜像烧录2](image/镜像烧录2.png)

3. Make sure the WiFiLink-RX is properly connected to the antenna, and that the TF card is removed (to prevent data loss).

4. Use a SIM eject tool or a small screwdriver to press and hold the flash button, then connect DC power. Wait for 2 seconds, then release the button.

5. Connect the WiFiLink-RX to the computer via Type-C data cable.

   ![镜像烧录5](image/镜像烧录5.png)

6. If the previous steps were completed correctly, the WiFiLink-RX will enter flashing mode. The flashing tool will display “Found One MASKROM Device” on the interface.

   ![镜像烧录6](image/镜像烧录6.png)

7. When RX enters a flashing mode (MASKROM available), the paths for Loader and Image need to be changed. Click the area shown in the image below to select the “Loader” file.

   ![镜像烧录7](image/镜像烧录7.png)

8. Locate Drive&Tool folder and select rk356x_spl_loader_ddr1056_v1.10.111.bin to open.

   ![镜像烧录8](image/镜像烧录8.png)

9. Click the area for Image as well.

   ![镜像烧录9](image/镜像烧录9.png)

10. Select the system image file to be flashed, then click “Open.” (In this example, version 10.7 is used.)

   ![镜像烧录10RubyFPV](image/镜像烧录10RubyFPV.png)

11. After selecting the paths for both Loader and Image, please must tick Write by Address.

   ![镜像烧录11RubyFPV](image/镜像烧录11RubyFPV.png)

12. Click to execute, and the tool will start flashing the firmware for WiFiLink RX.

   ![镜像烧录12RubyFPV](image/镜像烧录12RubyFPV.png)

13. It takes about two minutes to finish flashing.

   ![镜像烧录13RubyFPV](image/镜像烧录13RubyFPV.png)

## Frequently Asked Questions(FAQ)

### A. Adjusting WiFiLink-RX Frequency and Air Unit Power

Video URL:

1. Press down on the 5-Way Button to open the menu,then select Quick Vehicle Setup to enter the quick setup menu.

   ![RubyFPV8.1.1](image/RubyFPV8.1.1.png ':size=70%')

2. Select Radio Link Frequency to adjust the frequency channel.

   ![RubyFPV8.1.2](image/RubyFPV8.1.2.png ':size=70%')

3. Select Radio Link Tx Power to adjust the air unit’s transmission power.

   ![RubyFPV8.1.3](image/RubyFPV8.1.3.png ':size=70%')

4. Select FC Telemetry Type to change the telemetry protocol (default is MAVLink).

   ![RubyFPV8.1.4](image/RubyFPV8.1.4.png ':size=70%')

### B. Adjusting Air Unit Video Output via WiFiLink-RX

Video URL:

1. Press down on the 5-Way Button to open the menu bar, then select Vehicles Settings → Video to enter the video settings.

2. Select Video Profile to adjust the video quality. The default is High Quality. High Performance can be selected to achieve lower latency.

   ![RubyFPV8.2.2](image/RubyFPV8.2.2.png ':size=70%')

3. Select Video Codec to adjust the video format. (The default H.264 is recommended.)

   ![RubyFPV8.2.3](image/RubyFPV8.2.3.png ':size=70%')

4. Select Resolution to adjust the video resolution. (Note: Resolutions exceeding 1080P will significantly affect the frame rate and may cause system lag. It is not recommended to exceed 1080P for general use, unless necessary.)

   ![RubyFPV8.2.4](image/RubyFPV8.2.4.png ':size=70%')

5. Select FPS to adjust the video frame rate. (The maximum frame rate varies depending on the resolution setting.)

   ![RubyFPV8.2.5](image/RubyFPV8.2.5.png ':size=70%')

6. Select Video Bitrate to adjust the video bitrate. (The default 6 Mbps is sufficient for most scenarios.)

   ![RubyFPV8.2.6](image/RubyFPV8.2.6.png ':size=70%')

### C. Setting HDMI Video Output on WiFiLink-RX

Video URL:

1. Press down on the 5-Way Button to open the menu bar, then select Controller Settings → Audio & Video Output to enter the settings.

2. Select HDMI Output Resolution to adjust the output resolution.

   ![RubyFPV8.3.2](image/RubyFPV8.3.2.png ':size=70%')

3. Select HDMI Refresh Rate to adjust the output frame rate.

   ![RubyFPV8.3.3](image/RubyFPV8.3.3.png ':size=70%')

### D. Exporting Internal Storage Video from WiFiLink-RX

Video URL:

1. Power on the WiFiLink-RX with the antenna properly connected. After the device starts up, insert a USB drive into the OTG port on the WiFiLink-RX.

   ![RubyFPV8.4.1](image/RubyFPV8.4.1.png ':size=70%')

2. Press down on the 5-Way Button to open the menu, then select Media & Storage → Move media files to USB memory stick. After pressing Confirm, the video files from the internal storage will be moved one by one to the root directory of the USB drive.

   ![RubyFPV8.4.2-1](image/RubyFPV8.4.2-1.png ':size=50%')

   ![RubyFPV8.4.2-2](image/RubyFPV8.4.2-2.png ':size=70%')

3. Export completed interface.

   ![RubyFPV8.4.3](image/RubyFPV8.4.3.png ':size=70%')
