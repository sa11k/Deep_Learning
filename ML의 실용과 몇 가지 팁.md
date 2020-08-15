# ML의 실용과 몇 가지 팁

## Learning rate
1. Large learning rate : overshooting<br>
![35](https://user-images.githubusercontent.com/63536606/90309710-d1828f80-df25-11ea-874a-925d1e22acb1.PNG)<br>
: learning rate가 너무 클 경우에는 경사면을 타고 튕겨져 올라가다가 결국에는 밥그릇을 탈출하는 overshooting 현상이 발생함. 

2. Small learning rate <br>
![36](https://user-images.githubusercontent.com/63536606/90309745-28886480-df26-11ea-8795-118a816c7961.PNG)<br>
: learning rate가 너무 작은 경우에는 한참을 내려갔음에도 불구하고 최저점까지 도달하지 못하는 현상이 발생함.

- learning rate를 너무 크지도, 작지도 않게 조절하는 것이 중요
- 다양한 learning rate를 사용하여 여러 번에 걸쳐 실행하는 것이 최선

## Data(X) preprocessing for gradient descent
- gradient descent algorithm을 적용하기 전에 preprocessing 작업으로 데이터의 범위를 제한할 수 있음.

## Feature Scaling
1. Normalization(Re-Scaling)<br>
    : 전체 구간을 0 ~ 100으로 설정하여 데이터를 관찰하는 방법으로 특정 데이터의 위치를 확인할 수 있도록 함
2. Standardization<br>
    : 평균까지의 거리로 2개 이상의 대상이 단위가 다를 때 대상 데이터를 같은 기준으로 볼 수 있도록 함

## Overfitting
- 모델이 training dataset에 잘 맞추기 위해 과도하게 복잡하여 실제로 사용할 때 맞지 않는 상황이 발생
- 해결책
    1. training data 수 늘리기
    2. 입력으로 들어오는 변수의 개수 줄이기
    3. Regularization 사용

## Regularization
- W(weight)가 너무 큰 값들을 갖지 않도록 하는 것
- 모델의 복잡도를 낮추기 위한 방법
![37](https://user-images.githubusercontent.com/63536606/90310025-a2215200-df28-11ea-9069-e887d0cfc71b.PNG)<br>
- cost 함수가 틀렸을 때 높은 비용이 발생할 수 있도록 penalty를 부과하는 것처럼 W에 대한 값이 클 경우 penalty 부여

## Training, Validation and test sets
![38](https://user-images.githubusercontent.com/63536606/90310087-2c69b600-df29-11ea-95db-49220028ba18.PNG)<br>
: 위 그림처럼 학습을 시키기 위한 training set, 학습 결과를 확인하기 위한 test set이 필요<br>
: 여러 번에 걸쳐 학습(train)하고, 검증(test)하는 작업을 반복