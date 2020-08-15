# Neural Network 1: XOR 문제와 학습방법, Backpropagation (1986 breakthrough)

## XOR using NN
![41](https://user-images.githubusercontent.com/63536606/90310778-c92f5200-df2f-11ea-959e-1436fae35d68.PNG)<br>
- 3개의 logistic regression의 과정에서 마지막에는 sigmoid 과정이 있음
- sigmoid 과정으로 hypothesis의 결과는 항상 0과 1 사이의 값으로 조정됨
- 앞 두개의 결과를 마지막 logistic regression의 입력으로 사용한다.

## Forward propagation
![42](https://user-images.githubusercontent.com/63536606/90310901-d993fc80-df30-11ea-956e-ef1c2f7172b3.PNG)<br>
: 이전의 그림을 하나로 연결하면 다음과 같다. 

# NN
![43](https://user-images.githubusercontent.com/63536606/90310964-5030fa00-df31-11ea-8287-699d2668dc96.PNG)<br>
: logistic regression을 multinomial classification으로 변환할 때 행렬을 사용하여 처리했음. 오른쪽은 왼쪽 그림의 첫번째 logistic regression들을 하나로 결합할 수 있음을 보여줌.
- 오른쪽 그림에서 k의 계산은 다음과 같음<br>
    ![44](https://user-images.githubusercontent.com/63536606/90311069-75723800-df32-11ea-8736-4915b48bdaf4.PNG)<br>
- Y(y hat)의 계산은 다음과 같음<br>
    ![45](https://user-images.githubusercontent.com/63536606/90311075-802ccd00-df32-11ea-8d52-9c1fcbbcd8a8.PNG)<br>

## Backpropagation
![40](https://user-images.githubusercontent.com/63536606/90310463-71431c00-df2c-11ea-8268-8ccd6f9c1750.PNG)<br>
- 앞에서부터 뒤로 진행하면서 W와 b를 바꾸어 나갈 때 : forward propagation
- 뒤에서부터 앞으로 거꾸로 진행하면서 바꾸어 나갈 때 : backward propagation
- NN에 포함된 여러 layer 중에서 결과에 가장 큰 영향을 주는 것은 뒤쪽 layer이므로 많은 layer 중에서 뒤쪽에 있는 일부만 수정하는 것이 훨쓴 더 좋은 예측을 할 수 있게 함<br>
![46](https://user-images.githubusercontent.com/63536606/90311470-2201e900-df36-11ea-989f-9b1afef1b9d8.PNG)<br>
![47](https://user-images.githubusercontent.com/63536606/90311510-7016ec80-df36-11ea-8719-e2d7c0a32e93.PNG)<br>
- chain rule을 이용하여 길게 늘어져있는 계산을 간단한 미분을 통해 동작하는 것
- 단점<br>
    ![48](https://user-images.githubusercontent.com/63536606/90311601-8cffef80-df37-11ea-897b-fb3d4d74846b.PNG)<br>
    - Vanishing gradient : sigmoid는 전달된 값을 0과 1 사이로 심하게 변형되어 값이 현저하게 작아지는 현상이 발생
    - layer을 지날 때마다 최초 값보다 현저하게 작아지기 때문에 값을 전달해도 의미를 가질 수 없음