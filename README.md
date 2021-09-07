# Anomaly Detection
 
데이터 분석에서 이상 탐지는 대부분의 데이터와 크게 달라 의심을 불러 일으키는 희귀 항목, 이벤트 또는 관찰을 식별하는 것입니다.
이 저장소는 이상 탐지에 대한 주요 알고리즘 기법, 논문에 대한 스터디와 관련 코드를 적용해보는 공간입니다.

<br>

## Anomaly Detection 분류
Anomaly Detection은 학습에 사용하는 label 유무에 따라 크게 3가지로 분류할 수 있습니다. 

### 1. Supervised Anomaly Detection
- 학습시, Labeling된 정상/비정상 데이터를 모두 사용한 경우
- Class-Imbalance(불균형) 문제
- 모델 성능 평가가 가능하다는 점에서 직관적일 수 있지만, 척도 선정에 주의

### 2. Semi-supervised Anomaly Detection
- 정상 sample만 이용해서 모델을 학습시키는 방법
- 정상 sample들을 둘러싸는 boundary를 설정하고, 이 boundary 밖에 있는 sample들을 모두 비정상으로 간주
- One-Class SVM, Deep SVDD 논문이 잘 알려져있음

### 3. Unsupervised Anomaly Detection
- 대부분의 데이터가 정상 sample이라는 가정하에 차원을 축소하고 복원을 하는 과정으로 비정상을 검출하는 방법이 대표적
- 정상/비정상 데이터의 구분에 대한 임계치 설정이 필요할 수 있음

<br>

|분류|모델|코드|
|---|---|---|
|Supervised Anomaly Detection||
|Semi-supervised Anomaly Detection|One-Class SVM|
|Unsupervised Anomaly Detection|Autoencoder|[Autoencoder](https://github.com/jaeeun49/Anomaly-Detection/blob/main/code/Autoencoder.ipynb)

<br>

## Anomaly Detection 논문
|데이터|논문|정리|코드리뷰|
|---|---|---|---|
|sensor data|[LSTM-based Encoder-Decoder for Multi-sensor Anomaly Detection](https://arxiv.org/abs/1607.00148)|[pdf](https://github.com/jaeeun49/Anomaly-Detection/blob/main/review/LSTM-based%20Encoder-Decoder%20for%20Multi-sensor%20Anomaly%20Detection.pdf)|[.ipynb](https://github.com/jaeeun49/Anomaly-Detection/blob/main/code_practices/LSTM-based%20Encoder-Decoder%20for%20Multi-sensor%20Anomaly%20Detection.ipynb)|
