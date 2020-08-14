# Linear Regression cost 함수 최소화

## Simplified hypothesis
![11](https://user-images.githubusercontent.com/63536606/90265294-5372aa00-de8d-11ea-8e9a-49d909f7f0d8.PNG)<br>
![10](https://user-images.githubusercontent.com/63536606/90261081-6b472f80-de87-11ea-98a7-956591b8f510.PNG)<br>
- b = 0을 대입하여 단순화 시킨다. <br>

![12](https://user-images.githubusercontent.com/63536606/90265611-ce3bc500-de8d-11ea-87a6-5b42eedacce7.PNG)<br>
![13](https://user-images.githubusercontent.com/63536606/90265689-e57ab280-de8d-11ea-8d6b-4481236cd9ff.PNG)<br>

![14](https://user-images.githubusercontent.com/63536606/90265869-283c8a80-de8e-11ea-9b9d-c0e83ec1b0cd.png)
- 아래의 값들을 이용하면 위 그래프처럼 표현된다.
    - W = 0 일 때 cost(W) = 4.67 
    - W = 1 일 때 cost(W) = 0
    - W = 2 일 때 cost(W) = 4.67
- 결국 목표는 cost값이 최솟값이 되는 지점을 찾는 것

## Gradient descent algorithm
- 경사를 따라 내려가는 알고리즘
- Minimize cost function : cost(W, b) - 최소의 W, b를 찾는 알고리즘
- 많은 minimize problems에 사용

## Gradient descent algorithm 작동방법
1. 0.0(혹은 다른 값)에서 시작하여 W와 b를 조금씩 변경하여 cost(W,b)를 감소
2. 파라미터를 변경할 때마다 cost(W,b)를 가장 많이 감소시키는 gradient를 선택
3. 최저점으로 수렴할 때까지 반복
(시작할 때 최종 최솟값을 설정할 수 있음)

## Gradient descent algorithm 계산 방식
![15](https://user-images.githubusercontent.com/63536606/90266523-18717600-de8f-11ea-9ca4-44b0ebcb1cfe.PNG)
- 이 식을 기계적으로 적용시키면 cost function을 최소화하는 W를 구할 수 있고, 그것이 바로 Linear regression의 핵심인 학습 과정을 통해 모델을 만드는 과정이다.