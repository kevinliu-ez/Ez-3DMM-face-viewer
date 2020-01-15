# Ez S316 Face Scan (for Engineering Purpose)
[[中文]](README.md) [[EN]](README.en.md)

Ez S316 Face Scan 是一MS Windows的程式，可透過EzRGBD ToF相機來進行人臉掃描。

## Setup
* Hardware
  * Plug the USB DC power supply into a power outlet.
  * Connect a USB 3.0 cable from the EzRGBD device to your MS Windows computer.
  * Connect a USB 2.0 cable from the USB DC power supply to the EzRGBD device.
  * The current configuration of the device is optimized for static scenes, a tripod is recommended for holding the device.
* Software
  * Install the MS Visual C++ Redistributable for Visual Studio 2017. Or you can find the installer [here](https://github.com/kevinliu-ez/Ez-S316-viewer/blob/master/Setup/MSVCRedist_x64_VS2015-2017-2019.exe) in the repository.

## Usage
The viewer has two modes, 'Preview' (PREVIEW) and 'Face Scan' (FACE_SCAN) modes. To start the viewer, please run the application located at 'RC1\Ez3DFaceScan.exe'. The viewer will be in 'Preview' mode after it started.

<p align="center"> 
<img src="https://github.com/kevinliu-ez/Ez-3DMM-face-viewer/blob/master/README/Viewer_StateMachine.png">
</p>

* Preview mode:
![](https://github.com/kevinliu-ez/Ez-3DMM-face-viewer/blob/master/README/GUI_FaceROI.png)
  * To capture the 3D RGB point cloud of the scene, please short press (<0.5 second) key 'p'. The virtual camera may be located behind the axis mark (the opened window shows only GREEN, BLACK and RED blocks), pressing 'r' after the windows opened is recommended.
  * To exit, please short press (<0.5 second) key 'q'.

* Face Scan mode:
![](https://github.com/kevinliu-ez/Ez-3DMM-face-viewer/blob/master/README/GUI_Prcing.png)
  * 於Preview mode中按下'c'後，程式開始進行臉部掃描，並顯示"Processing"。完成後會自行跳回Preview mode，並結束顯示"Processing"。
  * 掃描結果將存於資料夾中的"Ez3DFaceScan.isomap.png"、"Ez3DFaceScan.mtl"、"Ez3DFaceScan.obj"，分別為材質檔、配置檔、與三角網格檔。<br>![](https://github.com/kevinliu-ez/Ez-3DMM-face-viewer/blob/master/README/OutputFiles.png)
  * 可利用MashLab讀取"Ez3DFaceScan.obj"，來顯示臉部掃描結果。<br>![](https://github.com/kevinliu-ez/Ez-3DMM-face-viewer/blob/master/README/ScanResults.png)

