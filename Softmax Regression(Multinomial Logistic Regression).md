# Softmax Regression(Multinomial Logistic Regression)

## Multinomial Classification
![25](https://user-images.githubusercontent.com/63536606/90270267-e06d3180-de94-11ea-96ef-b87eb47b7518.PNG)
![26](https://user-images.githubusercontent.com/63536606/90270275-e3682200-de94-11ea-8906-df4a6cc656f6.PNG)<br>
: Label의 종류가 세개(A, B, C)인 Regression<br>
: 3개의 각각 다른 Binary Classification으로도 구현할 수 있음.(각각 독립된 Classifier들을 가지고 구현)

## Classifier의 구현
- Binary Classification<br>
![27](https://user-images.githubusercontent.com/63536606/90270576-64bfb480-de95-11ea-97ca-3c899e029d23.PNG)<br>
: 각각 독립된 Classifier들을 가지고 있어야 함. 이러한 방식을 이용하면 복잡하므로 Multinomial Classification을 이용함.

## Multinomial Classification
![28](https://user-images.githubusercontent.com/63536606/90270724-9df82480-de95-11ea-8b7d-8d93c62e74dc.PNG)<br>
: 3번의 독립된 형태의 벡터를 계산하는 것이 아니라 Matrix multiplication을 이용하여 편리하게 계산

## Softmax 함수
![29](https://user-images.githubusercontent.com/63536606/90270874-e1eb2980-de95-11ea-8202-0325d2e70d01.png)<br>
: softmax 함수를 이용하여 각각의 scores가 0에서 1사이의 값을 가지고 합이 1인 확률(probabilities)로 변환

## One-hot encoding
![30](https://user-images.githubusercontent.com/63536606/90270996-152db880-de96-11ea-9422-9f96b4e0e7d4.png)<br>
: 제일 큰 값을 1로 만들고 나머지는 0으로 만든다.

## Cross-entropy Cost function
- 하나의 training set에 대한 Cross-entropy cost function<br>
![31](https://user-images.githubusercontent.com/63536606/90272158-edd7eb00-de97-11ea-8738-6c5ab8790e18.PNG)<br>
![32](https://user-images.githubusercontent.com/63536606/90271712-30e58e80-de97-11ea-8ff0-29f97e7218c1.PNG)
- 여러 개의 training set에 대한 Cross-entropy cost function<br>
![33](https://user-images.githubusercontent.com/63536606/90271817-5ecad300-de97-11ea-8b4b-abe3bac03267.PNG)

## Cost function의 최소화(Gradient descent)
![34](https://user-images.githubusercontent.com/63536606/90271922-8c178100-de97-11ea-867b-459734f5ac88.PNG)