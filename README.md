# Model
### YOLOv8n 선정 이유
- 검증된 안정성: YOLOv8은 다양한 프로젝트에서 성능이 입증되어 있고, 최신 버전보다 안정적입니다. 실시간 골프공 추적 같은 작업에서는 검증된 솔루션이 더 신뢰할 수 있습니다.
- 속도-정확도 균형: YOLOv8n은 경량화된 모델로, 빠른 속도와 적절한 정확도를 제공하여 실시간 처리가 중요한 프로젝트에 적합합니다. 최신 버전은 더 높은 정확도를 제공할 수 있지만, 그만큼 연산 비용이 증가할 수 있습니다.
- 하드웨어 효율성: YOLOv8n은 고성능 GPU뿐만 아니라 CPU나 엣지 디바이스에서도 효율적으로 작동하여 다양한 환경에서 실행 가능하고 비용 효율적입니다.
- 최신 기능 불필요: 최신 버전의 추가 기능들이 이 프로젝트에 큰 이점을 제공하지 않으며, YOLOv8n으로도 충분한 성능을 낼 수 있습니다.

# Train
### 골프공만 학습

##### 1. 데이터
- data1: https://universe.roboflow.com/school-eihku/golfball-crji6/dataset/1
- data2: https://universe.roboflow.com/mrinmoy-bhadra-lojma/golfballdetector/dataset/10

- 총 데이터 개수:
	- train: 4381개(85%)
	- valid: 448개(9%)
	- test: 339개(6%)


- 클래스 이름
	- 0: GolfBall

##### 2. 하이퍼파라미터(hyperparameters) 설정
- epochs: 100
- imgsz: 640 # 이미지 크기
- batch: 16
- patience: 10  # 10 epoch 동안 개선이 없으면 조기 종료
- augment: True  # 데이터 증강 활성화, 여러 증강 기법들이 학습 과정에서 자동으로 적용, 여기에는 회전, 크기 조정, 좌우 반전, 밝기 및 대비 조정 등의 다양한 변환이 포함

##### 3. 결과



### 골프공과 골프채 헤드 학습

##### 1. 데이터
- data1: https://universe.roboflow.com/sofyan-faidoul-gwvjg/golf-ball-golf-club-handle-golf-club-head/dataset/1#
	- TRAIN SET(86%): 11676 Images
	- VALID SET(9%): 1217 Images
	- TEST SET(4%): 607 Images
- data2: https://universe.roboflow.com/clg-plzss/galf/dataset/2#
	- TRAIN SET(92%): 13502 Images
	- VALID SET(5%): 725 Images
	- TEST SET(3%): 430 Images

- 총 데이터 개수:
	- train: 24867개(89%)
	- valid: 1904개(7%)
	- test: 1020개(4%)

- 클래스 이름
	- 0: GolfBall
	- 1: ClubHead
	- 2: ClubHandle

- 클래스별 데이터 개수
	- Golf Ball (0): 24077개
	- Club Head (1): 21725개
	- Club Handle (2): 12193개

##### 2. 하이퍼파라미터(hyperparameters) 설정
- epochs: 200
- imgsz: 640 # 이미지 크기
- batch: 16
- patience: 10  # 10 epoch 동안 개선이 없으면 조기 종료
- augment: True  # 데이터 증강 활성화, 여러 증강 기법들이 학습 과정에서 자동으로 적용, 여기에는 회전, 크기 조정, 좌우 반전, 밝기 및 대비 조정 등의 다양한 변환이 포함

##### 3. 결과
