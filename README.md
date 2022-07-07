# OCR
- Detection_SR_Recognition_drawtext.ipynb 이미지에 글씨쓰기
- SuperResolution_Recognition_deomo.ipynb Post-Processing, TTS 추가

# Model 설명
## Text Detection
- <a href="https://github.com/ultralytics/yolov5">yolov5</a>
## Super Resolution
- <a href="https://github.com/jingyunliang/swinir">SwinlR</a>
## Text Recognition
- <a href="https://github.com/clovaai/deep-text-recognition-benchmark">deep-text-recognition-benchmark</a> 의 STAR-Net
## Post Processing
- 각종 맞춤법검사기
## Application
- TTS,Translation,Summarization

## OCR 성능을 올리기 위해 시도한 방법
- 기존 OCR은 Text Detection과 Text Recognition을 진행하여 OCR를 진행하는데, 이점에서 OCR의 성능을 올리고자
Text Detection -> Crop Image -> Crop Image에 대해 각각 Super Resolution 진행후 -> Text Recognition 하여 Text Recognition에서 성능을 높이고자고시도함
- Post Processing을 도입하여 Text Recognition에서 나온결과값의 정확도를 최대한 높일려고 시도함
- Pre Processing을 통해 글자를 잘 인식하도록 OpenCV로 Image 조작
- Text Detection 여러가지 모델 사용
- Text Recognition에서 Custom Dataset을 Data Augmentation을 진행하여 데이터수를 늘려서 학습함

## 데이터셋
AI Hub 데이터셋으로 학습을 진행하였음, 그과정에서 Data Augmentation을 진행하여 데이터수를 늘려서 학습함
