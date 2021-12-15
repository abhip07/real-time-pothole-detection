
<div align="center">
<h1>Real Time Pothole Detection</h1>

<p>
This is the project of real time object detection model, using pretrained weights of volov5 algorithm, that performs <a href="https://github.com/abhip07/real-time-pothole-detection">real time Pothole Detection</a>.
</p>

<p align="center">
<img src="./yolov5/data/images/img.jpg" width="700" />
</p>   
<br>
<div>
   <a href="https://colab.research.google.com/github/ultralytics/yolov5/blob/master/tutorial.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a>
   
</div>
<br>
<div align="center">
   <a href="https://www.linkedin.com/company/ultralytics">
   <img src="https://www.freepnglogos.com/uploads/youtube-play-red-logo-png-transparent-background-6.png" width="6%"/>
   </a>
   <img width="2%" />
   <a href="https://github.com/ultralytics">
   <img src="https://github.com/ultralytics/yolov5/releases/download/v1.0/logo-social-github.png" width="5%"/>
   </a>
   <img width="2%" />
   <a href="https://www.linkedin.com/company/ultralytics">
   <img src="https://github.com/ultralytics/yolov5/releases/download/v1.0/logo-social-linkedin.png" width="5%"/>
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

## <div align="center">Quick Start Examples</div>

<details open>
<summary>Install</summary>

[**Python>=3.6.0**](https://www.python.org/) is required with all
[requirements.txt](https://github.com/ultralytics/yolov5/blob/master/requirements.txt) installed including
[**PyTorch>=1.7**](https://pytorch.org/get-started/locally/):
<!-- $ sudo apt update && apt install -y libgl1-mesa-glx libsm6 libxext6 libxrender-dev -->

```bash
$ git clone https://github.com/ultralytics/yolov5
$ cd yolov5
$ pip install -r requirements.txt
```

</details>

<details open>
<summary>Inference</summary>

Inference with YOLOv5 and [PyTorch Hub](https://github.com/ultralytics/yolov5/issues/36). Models automatically download
from the [latest YOLOv5 release](https://github.com/ultralytics/yolov5/releases).

```python
import torch

# Model
model = torch.hub.load('ultralytics/yolov5', 'yolov5s')  # or yolov5m, yolov5l, yolov5x, custom

# Images
img = 'https://ultralytics.com/images/zidane.jpg'  # or file, Path, PIL, OpenCV, numpy, list

# Inference
results = model(img)

# Results
results.print()  # or .show(), .save(), .crop(), .pandas(), etc.
```

</details>



<details open>
<summary>Inference with detect.py</summary>

`detect.py` runs inference on a variety of sources, downloading models automatically from
the [latest YOLOv5 release](https://github.com/ultralytics/yolov5/releases) and saving results to `runs/detect`.

```bash
$ python detect.py --source 0  # webcam
                            img.jpg  # image
                            vid.mp4  # video
                            path/  # directory
                            path/*.jpg  # glob
                            'https://youtu.be/Zgi9g1ksQHc'  # YouTube
                            'rtsp://example.com/media.mp4'  # RTSP, RTMP, HTTP stream
```

</details>

<details open>
<summary>Training</summary>

Run commands below to reproduce results
on [COCO](https://github.com/ultralytics/yolov5/blob/master/data/scripts/get_coco.sh) dataset (dataset auto-downloads on
first use). Training times for YOLOv5s/m/l/x are 2/4/6/8 days on a single V100 (multi-GPU times faster). Use the
largest `--batch-size` your GPU allows (batch sizes shown for 16 GB devices).

```bash
$ python train.py --data coco.yaml --cfg yolov5s.yaml --weights '' --batch-size 64
                                         yolov5m                                40
                                         yolov5l                                24
                                         yolov5x                                16
```

<img width="800" src="https://user-images.githubusercontent.com/26833433/90222759-949d8800-ddc1-11ea-9fa1-1c97eed2b963.png">

## <div align="center">Why I used YOLO for Transfer Learning</div>

<p align="left"><img width="800" src="https://user-images.githubusercontent.com/26833433/136901921-abcfcd9d-f978-4942-9b97-0e3f202907df.png"></p>
<details open>
  <summary>YOLOv5-P5 640 Figure (click to expand)</summary>

<p align="left"><img width="800" src="https://user-images.githubusercontent.com/26833433/136763877-b174052b-c12f-48d2-8bc4-545e3853398e.png"></p>
</details>

### Pretrained Checkpoints

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


## <div align="center">Suggest Improvements</div>

If you have suggestions, you can contact me through gmail or Linkedin! This project is in its early stage and I belive it will get improved over the time in future iterations. Thank you!
   
## <div align="center">Conclusion</div>

For YOLOv5 bugs and feature requests please visit [GitHub Issues](https://github.com/ultralytics/yolov5/issues). For business inquiries or
professional support requests please visit [https://ultralytics.com/contact](https://ultralytics.com/contact).

<br>

<div align="center">
    <a href="https://github.com/ultralytics">
        <img src="https://github.com/ultralytics/yolov5/releases/download/v1.0/logo-social-github.png" width="3%"/>
    </a>
    <img width="3%" />
    <a href="https://www.linkedin.com/company/ultralytics">
        <img src="https://github.com/ultralytics/yolov5/releases/download/v1.0/logo-social-linkedin.png" width="3%"/>
    </a>
</div>
