# Linear Regression의 개념

## Regression (data)
![1](https://user-images.githubusercontent.com/63536606/90256191-4e5b2e00-de80-11ea-87ab-626a48729ffe.PNG)

## (Linear) Hypothesis
![2](https://user-images.githubusercontent.com/63536606/90256335-8bbfbb80-de80-11ea-9964-4fea129a5b52.PNG)
- W와 b에 따라 선이 나타남.

![3](https://user-images.githubusercontent.com/63536606/90256439-b4e04c00-de80-11ea-9c57-37e405c582f6.PNG)
- 실제 데이터와의 거리를 계산하여 좋은 가설인지를 판단 (cost function)

## Cost function
- H(x) - y = 가설 값 - 실제 값<br>
- ![7](https://user-images.githubusercontent.com/63536606/90260711-db08ea80-de86-11ea-916e-288ebf9aa43a.PNG)<br> : 차이가 음수 / 양수 상관 없음
- ![8](https://user-images.githubusercontent.com/63536606/90260822-0b508900-de87-11ea-972f-3ddde2659f49.PNG)<br>
- ![9](https://user-images.githubusercontent.com/63536606/90260882-24f1d080-de87-11ea-9c69-d7a70ad96dc3.PNG)<br> : m은 데이터 개수
- ![10](https://user-images.githubusercontent.com/63536606/90261081-6b472f80-de87-11ea-98a7-956591b8f510.PNG)<br> : 이 값을 가장 작게하는 W, b 값을 찾아야 함 -> 이것을 찾는 것이 Linear Regression의 학습