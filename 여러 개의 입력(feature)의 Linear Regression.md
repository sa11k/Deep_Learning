# 여러 개의 입력(feature)의 Linear Regression

## 3개의 input(x1, x2, x3)을 사용하는 Regression
- 일반적인 가설과 cost 함수 <br>
![16](https://user-images.githubusercontent.com/63536606/90267339-5a4eec00-de90-11ea-9fbe-266b66abe8cd.PNG)<br>
![17](https://user-images.githubusercontent.com/63536606/90267415-79e61480-de90-11ea-92f9-a5493ddeca1c.PNG)<br>
: 변수가 많아지면 같은 방식으로 늘려줌. 하지만 이 방식을 사용하면 번거로워지므로 Matrix(행렬)를 사용함.

- Matrix(행렬)의 곱을 이용한 가설<br>
![18](https://user-images.githubusercontent.com/63536606/90267645-d34e4380-de90-11ea-8c82-ce016493c79e.PNG)<br>
: H(X) = XW로 표현할 수 있음. (여기서 X와 W는 모두 행렬)<br>
![19](https://user-images.githubusercontent.com/63536606/90267784-fe389780-de90-11ea-86b7-9fe2fcb21328.PNG)<br>
: 각각의 인스턴스를 계싼할 필요 없이 전체를 긴 행렬에 넣어 W를 곱하면 됨. (W 행렬의 크기는 변수의 개수가 m개이고 라벨의 개수가 n개이면 [m, n])<br>
: Matrix를 사용하면 tensorflow의 shape의 instance의 수를 자동으로 채워줌. 즉, w = variable shape를 몰라도 자동으로 shape를 선정해줌.