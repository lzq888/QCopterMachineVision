﻿[QCopterMV](https://github.com/QCopter/QCopterMachineVision)
========
* Author  : [Hom](https://github.com/Hom-Wang)
* Version : v1.2
* Update  : 2014/02/02

Description
========
QCopteMV 是一個機系視覺開發板，用來實現影像處理的裝置，目前 QCopterMV 搭配 MT9V022 灰階的攝像頭模組，用以實現光流、特徵辨識等演算法，板子上引出 FSMC，可以外接 3.5-inch TFT 螢幕模組，實現照相機功能。

License
========
* 硬體(Hardware)採用 [CC BY-SA 3.0 TW](http://creativecommons.org/licenses/by-sa/3.0/tw/deed.zh_TW) 方式授權 
  
　　<a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/tw/"><img alt="創用 CC 授權條款" style="border-width:0" src="http://i.creativecommons.org/l/by-sa/3.0/tw/80x15.png" /></a>  
　　<span xmlns:dct="http://purl.org/dc/terms/" property="dct:title"> QCopterMachineVision </span>由<a xmlns:cc="http://creativecommons.org/ns#" href="https://plus.google.com/u/0/112822505513154783828/posts" property="cc:attributionName" rel="cc:attributionURL"> Hom </a>製作，以<a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/tw/deed.zh_TW"> 創用CC 姓名標示-相同方式分享 3.0 台灣 授權條款 </a>釋出。  

* 軟體(Software)採用 [MIT License](http://opensource.org/licenses/MIT) 方式授權  

Hardware
========
* 控制器　 : [STM32F407V](http://www.st.com/web/catalog/mmc/FM141/SC1169/SS1577/LN11/PF252140) 100Pin 168MHz DSP FPU
* 感測器　 : [MT9V022](http://www.aptina.com/support/documentation.jsp?t=0&q=31&x=24&y=11#) ( mono )，使用 DCMI 操作
* 儲存紀錄 : micro SD，使用 SDIO 操作
* 外接介面 : 1*USB ( Micro )、1*SPI ( FFC16 )、1*FSMC、7*PWM
* PCB 尺寸 : 68 * 33mm
* 設計軟體 [Altium Designer 13](http://www.altium.com/en/products/altium-designer) ( PcbLib use AD [PcbLib v?](https://github.com/OpenPCB/AltiumDesigner_PcbLibrary) )

QCopterMV v2.0 預計修改 ( 尚未決定改版時間 )： 
>1. 微控制器改為 LQFP144 的 STM32F42xZ 或 STM32F43xZ，增加運算速度及功能。  
>2. 加入 [SDRAM](http://www.issi.com/WW/pdf/42-45S16400J.pdf)，透過 FMC 操作，用以增加影像處理時所需的 RAM 空間。  
>3. 加入 SPI 操作的 6DOF IMU，並預計新增影像自動水平的功能。  
>4. 加入 [Microphone](http://www.analog.com/en/audiovideo-products/mems-microphones/admp522/products/product.html) 來做聲音紀錄，並預計加入聲控的功能，同時也可以用來做飛行器間的溝通。  
>5. 更改 CamSPI 名稱為 FFCSPI，並修改腳位，使其可以連接 [QFC v2.2](https://github.com/QCopter/QCopterFlightControl)、[QRC](https://github.com/QCopter/QCopterRemoteControl)、[TFT_2.2](https://github.com/OpenPCB/TFT_2.2-inch) 等裝置。  
>6. 設計 Camera 模組，使用 [MT9V034](https://www.aptina.com/products/image_sensors/mt9v034c12stc/) 8bit DCMI，預計會有灰階和彩色兩種版本，方便做不同的演算法實現。  
>7. 設計類似 [Boscam HD19 雲台](http://www.dronesvision.net/en/fpv/1333-boscam-hd19-explorerhd-fpv-camera-pan-tilt-mount-for-fixwing-aircrafts.html)的裝置，用來攜帶 QCopterMV。 ( 該結構預計透過 3D Printer 製做 )  

<img src="https://lh5.googleusercontent.com/-swW9VgqOZBU/UlA1hQbLx9I/AAAAAAAAD7s/co_2QQ1q5HY/s1200/QCopterMV_System.png" />

Related Documents
========
* [Update Records - Hackpad](https://hom.hackpad.com/QCopterMV-sQqGKy2RUlY)
* [Datasheet & BOM - Google Drive](https://drive.google.com/folderview?id=0BzL2wwAot6oPQWdKS3VMWmZ1Sjg&usp=drive_web)

Program
========
* QcopterMV Camera

Test
========
* QCopterMV LED
* QCopterMV USART
* QCopterMV PWM
* QCopterMV CamSPI-Slave
* QCopterMV SDIO
* QCopterMV SCCB
* QCopterMV FSMC
* QCopterMV OV7725 ( Use 480*272 SSD1963 )

View
========
<img src="https://lh3.googleusercontent.com/-Cy3CKYy0Y_w/Ud7K7XM_dFI/AAAAAAAAClc/evAgj8h4Sug/s1200/DSC_1179.jpg" />
<img src="https://lh5.googleusercontent.com/-LGxC8SM5YcU/Ud7K7xpP_8I/AAAAAAAAClc/WOheIGD4gww/s1200/DSC_1184.jpg" />
<img src="https://lh5.googleusercontent.com/-beekj574_I8/Ud7K5oIszrI/AAAAAAAAClc/P-EEJkbjrXs/s1200/DSC_1165.jpg" />
<img src="https://lh5.googleusercontent.com/-PonR56Y_DV8/Ud7K699bGII/AAAAAAAAClc/dmLREQBeU3w/s1200/DSC_1169.jpg" />
<img src="https://lh6.googleusercontent.com/-e9bpHqgJpKw/Ud7K7bGqDVI/AAAAAAAAClc/cZY7Y83zMEw/s1200/DSC_1173.jpg" />
<img src="https://lh3.googleusercontent.com/-JoVNYnuH20k/Ud7K9y_R4BI/AAAAAAAAClc/OCoD4AMalt0/s1200/DSC_1238.jpg" />
<img src="https://lh3.googleusercontent.com/-kZqt3l8fEWY/Ud7K-eDvCOI/AAAAAAAAClc/JQULeyFK128/s1200/DSC_1250.jpg" />
<br />
更多圖片 [Google+ albums](https://plus.google.com/u/0/photos/112822505513154783828/albums/5930570551599057185)

Config
========
<img src="https://lh6.googleusercontent.com/-Tylx81-lq6Q/UfliB3uha1I/AAAAAAAAC38/316n2OBTpWg/s1200/MV_T_Config.png" />
<img src="https://lh3.googleusercontent.com/-UubxWMWHGIs/UfliB1x-dnI/AAAAAAAAC34/w0i0qdxApcQ/s1200/MV_B_Config.png" />
<img src="https://lh5.googleusercontent.com/-bw6FBNQ-psk/UlA1dMj0nQI/AAAAAAAAD6I/kdzETuHT9oY/s1200/QCopterMV_Config_PIN.png" />
<img src="https://lh6.googleusercontent.com/-7jmhGBZESQw/UlA1cULocII/AAAAAAAAD5w/ciB-7ToHH4A/s1600/QCopterMV_Config_AF.png" />
<img src="https://lh5.googleusercontent.com/-dGunvCDcZcs/UlA1cYbLupI/AAAAAAAAD50/4b87URacEH8/s1200/QCopterMV_Config_DMA.png" />

Schematic
========
<img src="https://lh6.googleusercontent.com/-hHO6OBH94Qk/UlA1fh63edI/AAAAAAAAD7I/mpEoB8fNeSU/s1600/QCopterMV_Sch_MAIN.png" />
<br>＊STM32F407V<br>
<img src="https://lh6.googleusercontent.com/-ES2ZKJsFjik/UlA1fmFfGiI/AAAAAAAAD7E/oia47ndPYBY/s1600/QCopterMV_Sch_MCU.png" />
<br>＊SW<br>
<img src="https://lh5.googleusercontent.com/-xemt7G0G824/UlA1gkA-9qI/AAAAAAAAD7g/OVlnynBMdbU/s800/QCopterMV_Sch_SW.png" />
<br>＊POWER<br>
<img src="https://lh3.googleusercontent.com/-IecpsSUfAzY/UlA1fjoMAeI/AAAAAAAAD7A/Kbb5jWT3ajo/s800/QCopterMV_Sch_POWER.png" />
<br>＊LED<br>
<img src="https://lh6.googleusercontent.com/-muDI4sIRFEQ/UlA1evKbU8I/AAAAAAAAD6k/v_8gGxbnGE8/s800/QCopterMV_Sch_LED.png" />
<br>＊KEY<br>
<img src="https://lh3.googleusercontent.com/-H7x8Mf2dIPM/UlA1eKeuz3I/AAAAAAAAD6o/IL0sE17btcc/s800/QCopterMV_Sch_KEY.png" />
<br>＊PWM<br>
<img src="https://lh5.googleusercontent.com/-8dzm3Nm710U/UlA1gNpAxYI/AAAAAAAAD7M/M9GE7fhL20A/s800/QCopterMV_Sch_PWM.png" />
<br>＊CamSPI<br>
<img src="https://lh5.googleusercontent.com/-371qCai2vVk/UlA1eG1gytI/AAAAAAAAD6Q/nam-eBJvorY/s800/QCopterMV_Sch_CAMSPI.png" />
<br>＊FSMC<br>
<img src="https://lh6.googleusercontent.com/-NCY8MV4wX60/UlA1eIg9fDI/AAAAAAAAD6s/548hJj96NYc/s800/QCopterMV_Sch_FSMC.png" />
<br>＊DCMI<br>
<img src="https://lh6.googleusercontent.com/-_y7yZ-a3wKY/UlA1dQtk9rI/AAAAAAAAD6E/V_zeSbFtkLg/s800/QCopterMV_Sch_CAMERA.png" />
<br>＊SD<br>
<img src="https://lh3.googleusercontent.com/-a9Fd9XCbPd8/UlA1gTOdX7I/AAAAAAAAD7k/DCISW0c75HI/s800/QCopterMV_Sch_SDCARD.png" />
<br>＊USB<br>
<img src="https://lh6.googleusercontent.com/-5qwNq3d9KLU/UlA1grvfI5I/AAAAAAAAD7c/V6Uqb0F4KLk/s800/QCopterMV_Sch_USB.png" />
