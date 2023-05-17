# Plant Health LSTM Classifier

This repository contains an LSTM model for classifying the health of plants based on their time series data. The dataset consists of approximately 5,000 files each for healthy and diseased plants. Each file contains time series data with 9 features.

## Model Architecture
The LSTM model consists of the following layers:

An LSTM layer with 50 units and 'return_sequences=True' to enable the following LSTM layer to receive sequences as input.
A Dropout layer with a rate of 0.2 to reduce overfitting by randomly setting input units to 0 during training.
Another LSTM layer with 50 units.
A Dropout layer with a rate of 0.2 to further reduce overfitting.
An output Dense layer with a single neuron and a sigmoid activation function for binary classification.

## 프로젝트 배경 및 목표:
디지털 변화의 흐름 속에서 농업 분야는 최적화된 작물 생산을 통해 탄소 중립을 실현하는 방향으로 나아가고 있습니다. 그러나, 환경적 제약, 기후 변화, 병충해 발생 등의 예측하기 어려운 변수들로 인해 실제 농업에 이러한 모델들을 적용하는 것은 여전히 어려운 상황입니다. 이런 문제를 해결하기 위해, 본 프로젝트의 주요 목표는 파인애플에 대한 질병 예측 모델을 개발하여 조기 질병 감지를 통한 살균제 사용 감소를 이루는 것입니다. 이를 통해 농업의 환경 부담 감소와 생산성 향상을 도모하고자 하였습니다.

## 구현 방법:
농장의 센서 데이터를 이용하여 LSTM 과 CNN 의 모델을 각각 학습시켰습니다. 저는 Python 의 Keras 라이브러리를 사용하여 LSTM 기반 이진 분류 모델을 개발했습니다. 데이터 전처리 단계에서는 누락된 값 처리, 레이블링, 클래스 균형 조정, 시퀀스 생성등을 수행하였습니다. 파인애플의 질병 여부를 예측하기 위해, 주어진 데이터를 훈련 및 테스트 세트로 분리하고, 모델을 훈련시킨 후, 모델의 성능을 평가했습니다. 또한, 다양한 모델 아키텍처를 실험하고 하이퍼파라미터 튜닝을 통해 최적의 모델을 찾았습니다.

## 난이도가 높았던 작업:
프로젝트를 진행하면서 저는 실험적인 문제에 직면했습니다. 목표는 수집된 파인애플 데이터를 활용하여 질병을 예측하는 것이었으나, 제가 처음 개발한 모델은 100%의 정확도를 보였습니다. 이는 분명히 모델이 잘못된 것을 의미했고, 이를 통해 유의미한 결과를 도출해낼 수 없었습니다. 하지만, 저는 다양한 해결책을 모색하며 모델을 개선해나갔습니다. 최종적으로 클래스 분포를 조정하고, 데이터 전처리 방법을 변경하며, 모델의 학습 순서를 수정함으로써, 성공적인 결과를 얻을 수 있었습니다.

## 결과 및 배운 점:
프로젝트를 통해 개발한 제 LSTM 모델은 파인애플의 질병을 92%의 정확도로 예측할 수 있었습니다. 이 프로젝트를 통해 기계 학습의 실제 적용 사례를 경험하고, 딥러닝 모델의 개발 및 튜닝에 대한 실질적인 이해를 얻을 수 있었습니다. 또한, 실제 문제 해결을 위해 여러 단계를 거쳐야 하는 딥러닝 프로젝트의 흐름을 이해하는 데 큰 도움이 되었습니다. 이러한 문제해결 능력은 인턴십 동안 업무에 임할 때 큰 도움이 될 것입니다.
