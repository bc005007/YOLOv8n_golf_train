# 모델
YOLOv8n

`yolov8n.pt`로 학습을 요청했음에도 불구하고 `yolo11n.pt`가 다운로드된 이유는 Automatic Mixed Precision (AMP) 기능을 확인하기 위한 루틴 검사 때문입니다. Ultralytics 패키지에서는 AMP가 제대로 작동하는지 확인하기 위해 기본적으로 `yolov8n.pt` 또는 다른 사전 학습된 모델 파일을 다운로드하는 과정을 거칩니다. 이 과정은 사용자가 지정한 모델과는 별개로 진행되며, AMP 체크가 통과되면 실제로 학습에 사용하는 모델은 사용자가 지정한 모델이 됩니다.
AMP(Automatic Mixed Precision)란?
AMP는 **반정밀도(FP16)**와 **단정밀도(FP32)**를 혼합하여 사용하는 훈련 기법입니다. 이는 GPU의 성능을 극대화하면서도 모델의 정확도를 유지하기 위한 방법입니다. AMP를 사용하면 다음과 같은 이점이 있습니다:
	1.	메모리 절약: FP16 형식을 사용하면 메모리 사용량이 줄어들어 더 큰 모델을 훈련할 수 있습니다.
	2.	속도 향상: FP16 연산은 FP32보다 훨씬 빠르기 때문에 훈련 속도가 빨라집니다. 특히, 최신 GPU 아키텍처(Tensor Core 지원)를 사용할 경우 최대 3배의 속도 향상을 얻을 수 있습니다.
	3.	정확도 유지: 중요한 연산 단계에서는 여전히 FP32를 사용하여 정확도를 유지합니다.


# 골프공만 학습
data1: https://universe.roboflow.com/school-eihku/golfball-crji6/dataset/1
data2: https://universe.roboflow.com/mrinmoy-bhadra-lojma/golfballdetector/dataset/10


이미지 개수:
train: 4381개
test: 339개
valid: 448개


# 골프공과 골프채 헤드 학습
data1: https://universe.roboflow.com/sofyan-faidoul-gwvjg/golf-ball-golf-club-handle-golf-club-head/dataset/1#
- TRAIN SET(86%): 11676 Images
- VALID SET(9%): 1217 Images
- TEST SET(4%): 607 Images
data2: https://universe.roboflow.com/clg-plzss/galf/dataset/2#
- TRAIN SET(92%): 13502 Images
- VALID SET(5%): 725 Images
- TEST SET(3%): 430 Images


