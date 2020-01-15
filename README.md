# Ez S316 Face Scan (for Engineering Purpose)
[[中文]](README.md) [EN]

Ez S316 Face Scan 是一MS Windows的程式，可透過EzRGBD ToF相機來進行人臉掃描。

## 下載
  請按此處下載<a href="https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/kevinliu-ez/Ez-3DMM-face-viewer/tree/master/RC1" target="_blank">[HERE]</a>。

## 安裝與設置
* Hardware
  * 插入USB DC電源變壓器至插座。
  * 連接USB 3.0訊號線至EzRGBD ToF相機與MS Windows電腦。
  * 連接USB 2.0訊號線USB DC變壓器與EzRGBD ToF相機。
  * 將相機與光源置於腳架上。
* Software
  * 安裝MS Visual C++ Redistributable for Visual Studio 2017。或可由以下位置安裝[HERE](https://github.com/kevinliu-ez/Ez-3DMM-face-viewer/blob/master/Setup/MSVCRedist_x64_VS2015-2017-2019.exe)。

## Usage
此程式有兩狀態，'Preview' (PREVIEW)與'Face Scan' (FACE_SCAN)狀態。要開起程式時，請執行以下檔案'RC1\Ez3DFaceScan.exe'。程式開起時將於'Preview'狀態中。

<p align="center"> 
<img src="https://github.com/kevinliu-ez/Ez-3DMM-face-viewer/blob/master/README/Viewer_StateMachine.png">
</p>

* Preview mode:
![](https://github.com/kevinliu-ez/Ez-3DMM-face-viewer/blob/master/README/GUI_FaceROI.png)
  * 開起環型LED光源，並調整好光源亮度，與相機角度。
  * 要進行臉部掃描時，請將臉置於綠框中，並按下按鍵'c'。建議的掃描距離(相機至臉部)為20cm。
  * 要離開程式時，請按下按鍵'q'。

* Face Scan mode:
![](https://github.com/kevinliu-ez/Ez-3DMM-face-viewer/blob/master/README/GUI_Prcing.png)
  * 於Preview mode中按下'c'後，程式開始進行臉部掃描，並顯示"Processing"。完成後會自行跳回Preview mode，並結束顯示"Processing"。
  * 掃描結果將存於資料夾中的"Ez3DFaceScan.isomap.png"、"Ez3DFaceScan.mtl"、"Ez3DFaceScan.obj"，分別為材質檔、配置檔、與三角網格檔。<br>![](https://github.com/kevinliu-ez/Ez-3DMM-face-viewer/blob/master/README/OutputFiles.png)
  * 可利用MashLab讀取"Ez3DFaceScan.obj"，來顯示臉部掃描結果。<br>![](https://github.com/kevinliu-ez/Ez-3DMM-face-viewer/blob/master/README/ScanResults.png)

## 進行中項目
* 由臉部掃描的3D surface建立3D列印時所需的厚度體積。
* 臉部輪廓的手動調整，如胖、瘦等。
