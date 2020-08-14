# Logistic(Regression) Classification

## Binary Classification
- 소요된 시간을 기준으로 두 개 중 하나의 결과값을 가짐.(ex> P/F, 0/1)

## 공부한 시간을 기준으로 Pass(1) or Fail(0)을 예측
- Linear Regression을 통해 실제 데이터와 가장 근접한 선형적 모델을 만들고, 그 중간 지점을 찾아 그 지점보다 작으면 Fail(0), 크면 Pass(1)로 예측<br>
![20](https://user-images.githubusercontent.com/63536606/90268794-83707c00-de92-11ea-9b14-e07a2e422a36.PNG)<br>
: 이렇게 하면 training set의 값이 커지면 중간 지점이 달라지고, 그렇게 되면 이전에는 Pass(1)였던 시간도 Fail(0)로 예측될 수 있음.

## Logistic Classification의 가설(Hypothesis) 정의
- Logistic Hypothesis<br>
: H(X) = WX를 z라고 하면 z 값에 상관없이 0에서 1 사이의 값이 나올 수 있도록 해주는 함수<br>
![21](https://user-images.githubusercontent.com/63536606/90269054-f8dc4c80-de92-11ea-957e-e1a556f26b7b.PNG)

## Logistic REgression의 cost 함수
: Linear Regression과 동일한 cost 함수를 사용하게 되면 cost 함수의 모양이 매끄럽지 못하므로 매끄럽게 바꿔주어야 함.<br>
![22](https://user-images.githubusercontent.com/63536606/90269346-730cd100-de93-11ea-81b3-2eff2ab23d13.PNG)<br>
![23](https://user-images.githubusercontent.com/63536606/90269357-7607c180-de93-11ea-8d2a-7f94836212e8.PNG)

## cost 함수의 최소화(Gradient descent algorithm)
![24](https://user-images.githubusercontent.com/63536606/90269515-b7986c80-de93-11ea-9f0a-8ab663bf52d7.PNG)