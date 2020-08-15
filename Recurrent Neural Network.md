# Recurrent Neural Network

## Sequence data
- RNN은 Sequence data를 처리하는 모델
- 음성인식, 자연어처리 등이 포함<br>
![58](https://user-images.githubusercontent.com/63536606/90313751-fd177100-df49-11ea-8954-dcb1ae2dd877.PNG)

## Recurrent Neural Network
![59](https://user-images.githubusercontent.com/63536606/90313785-26380180-df4a-11ea-94b1-e05c3611b581.PNG)<br>
- y = Wx + b<br>
![60](https://user-images.githubusercontent.com/63536606/90313829-7ca54000-df4a-11ea-94a9-9927d5db2887.PNG)<br>
: 이전 단계에서의 상태 값과 입력 벡터(x)로 계산하면 새로운 상태의 값

## (Vanilla) Recurrent Neural Network
![61](https://user-images.githubusercontent.com/63536606/90313879-e3c2f480-df4a-11ea-84a2-cdce3c4aa0c5.PNG)<br>
: 가장 단순한 형태의 RNN 모델<br>
- t : sequence data에 대한 특정 시점
- W의 이전 상태와 입력을 가지고 fw에 해당하는 tanh 함수를 호출
- ht : 현재 상태
- yt : 예측값

## Character-level language model ex
![62](https://user-images.githubusercontent.com/63536606/90314020-a6129b80-df4b-11ea-91f7-686b6c73a142.PNG)<br>
- hello가 들어왔다면 hell에 대한 예측은 ello가 됨
- 위의 사진에서는 첫번째 예측은 틀렸음. 네번째가 가장 크기 때문에 one-hot encoding을 거치면 o를 예측하고 있음.

## Recurrent Networks의 여러가지 형태
![63](https://user-images.githubusercontent.com/63536606/90314108-25a06a80-df4c-11ea-87c3-7fc9576fc94e.PNG)<br>
- one to one : Vanilla Neural Networks
- one to many : Image Captioning (한 장의 그림에 대해 여러 개의 단어 형태로 표현될 수 있음)
- many to one : Sentiment Classification (여러 개의 입력에 대해 하나의 결과)
- many to many : Machine Translation (기계 번역)
- many to many : video classification on frame level (다대다 모델의 또 다른 형태로 동영상 같은 경우 여러 개의 이미지 프레임에 대해 여러 개의 설명이나 번역 형태로 결과를 반환)

## Several advanced models
- Long Short Term Memory(LSTM)
- GRU