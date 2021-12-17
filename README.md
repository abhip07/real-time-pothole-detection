
<div align="center">
<h1>Real Time Pothole Detection</h1>

<p>
This is the project of real time object detection model, using pretrained weights of volov5 algorithm, that performs <a href="https://github.com/abhip07/real-time-pothole-detection">real time Pothole Detection</a>.
</p>

<p align="center">
<img src="./yolov5/data/images/img.jpg" width="600" height="400"/>
</p> 
   
 #### Click on YouTube icon below to see the real time video inference or Click <a href="https://youtu.be/b0Lm3yeNxPM">Here</a>.
<br>
   
<div align="center">
   <a href="https://youtube.com/playlist?list=PLM5rSizdAguQ9ehaJd1he7Tap8_EREmvc">
   <img src="https://www.freepnglogos.com/uploads/youtube-play-red-logo-png-transparent-background-6.png" width="6%"/>
   </a>
   <img width="2%" />
   <a href="https://github.com/abhip07">
   <img src="https://github.com/ultralytics/yolov5/releases/download/v1.0/logo-social-github.png" width="5%"/>
   </a>
   <img width="2%" />
   <a href="https://www.linkedin.com/in/abhishek-pawar-8537971b1/">
   <img src="https://github.com/ultralytics/yolov5/releases/download/v1.0/logo-social-linkedin.png" width="4%"/>
   </a>
   
   
    
</div>
   
<br>

<!--
<a align="center" href="https://ultralytics.com/yolov5" target="_blank">
<img width="800" src="https://github.com/ultralytics/yolov5/releases/download/v1.0/banner-api.png"></a>
-->

</div>

## <div align="center">Dataset Used</div>

In this Project I have used custom labelled dataset with some images from google to make the learning process more complex..

## <div align='left'>Training Dataset Sample</div>
<table border="0">
<tr>
    <td>
    <img src="./yolov5/data/images/training data.jpg" width="100%" />
    </td>
    <td>
    <img src="./yolov5/data/images/training data2.jpg", width="100%" />
    </td>
</tr>
</table>

</details>

## <div align="center">Training Results</div>
   <p align="left"><img width="800" src="./yolov5/data/results/results.png" align="center"></p>
</details>


## <div align="center">Yolo vs Efficientdet performance</div>
   <p align="left"><img width="800" src="https://user-images.githubusercontent.com/26833433/136763877-b174052b-c12f-48d2-8bc4-545e3853398e.png"></p>
</details>

  <summary>YOLOv5 Nano models </summary>
  <p align="left"><img width="800" src="https://user-images.githubusercontent.com/26833433/136901921-abcfcd9d-f978-4942-9b97-0e3f202907df.png"></p>
<details open>


### Pretrained Checkpoints for YOLOv5 transfer learning

[assets]: https://github.com/ultralytics/yolov5/releases
[TTA]: https://github.com/ultralytics/yolov5/issues/303

|Model |size<br><sup>(pixels) |mAP<sup>val<br>0.5:0.95 |mAP<sup>val<br>0.5 |Speed<br><sup>CPU b1<br>(ms) |Speed<br><sup>V100 b1<br>(ms) |Speed<br><sup>V100 b32<br>(ms) |params<br><sup>(M) |FLOPs<br><sup>@640 (B)
|---                    |---  |---    |---    |---    |---    |---    |---    |---
|[YOLOv5n][assets]      |640  |28.4   |46.0   |**45** |**6.3**|**0.6**|**1.9**|**4.5**
|[YOLOv5s][assets]      |640  |37.2   |56.0   |98     |6.4    |0.9    |7.2    |16.5
|[YOLOv5m][assets]      |640  |45.2   |63.9   |224    |8.2    |1.7    |21.2   |49.0
|[YOLOv5l][assets]      |640  |48.8   |67.2   |430    |10.1   |2.7    |46.5   |109.1
|[YOLOv5x][assets]      |640  |50.7   |68.9   |766    |12.1   |4.8    |86.7   |205.7
|                       |     |       |       |       |       |       |       |
|[YOLOv5n6][assets]     |1280 |34.0   |50.7   |153    |8.1    |2.1    |3.2    |4.6
|[YOLOv5s6][assets]     |1280 |44.5   |63.0   |385    |8.2    |3.6    |16.8   |12.6
|[YOLOv5m6][assets]     |1280 |51.0   |69.0   |887    |11.1   |6.8    |35.7   |50.0
|[YOLOv5l6][assets]     |1280 |53.6   |71.6   |1784   |15.8   |10.5   |76.8   |111.4
|[YOLOv5x6][assets]<br>+ [TTA][TTA]|1280<br>1536 |54.7<br>**55.4** |**72.4**<br>72.3 |3136<br>- |26.2<br>- |19.4<br>- |140.7<br>- |209.8<br>-

## In this project I have used YOLOv5l for transfer learning.

## <div align="center">Suggest Improvements</div>

If you have suggestions, you can contact me through gmail or Linkedin! This project is in its early stage and I belive it will get improved over the time in future iterations. Thank you!
   
## <div align="center">Thank You :)</div>
<br>
