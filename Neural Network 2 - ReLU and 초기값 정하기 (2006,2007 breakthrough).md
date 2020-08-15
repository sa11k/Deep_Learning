# Neural Network 2: ReLU and 초기값 정하기 (2006/2007 breakthrough)

## ReLU : Rectified Linear Unit
![49](https://user-images.githubusercontent.com/63536606/90312210-73fa3d00-df3d-11ea-9cbb-618748d09bc9.PNG)<br>
- 그림에 있는 것처럼 0보다 작을 때에는 0을 사용하고 0보다 큰 값에 대해서는 해당 값을 그대로 사용하는 방법
- 0과 현재 값(X) 중에서 큰 값을 선택. max(0,X)

## Activation Functions
![50](https://user-images.githubusercontent.com/63536606/90312269-fbe04700-df3d-11ea-800b-e77aea20d35e.PNG)<br>
1. tanh : sigmoid 함수를 재활용하기 위한 함수. sigmoid의 범위를 -1에서 1로 넓힘
2. ReLU : max(0, X). 음수에 대해서만 0으로 처리
3. Leaky ReLU : ReLU 함수의 변형으로 음수에 대해 1/10로 값을 줄여서 사용
4. Maxout : 두 개의 W와 b 중에서 큰 값이 나온 것을 사용
5. ELU : ReLU를 0이 아닌 다른 값을 기준으로 사용

## Weight의 초기화
- set all initial weights to 0<br>
    : Deep Learning Algorithm은 동작하지 않음.
- RBM<br>
    : 현재 layer에 들어온 input x 값에 대해 weight를 계산한 값을 다음 layer에 전달(forward). 전달 받은 값을 거꾸로 이전(현재) layer에 대해 weight 값을 계산(backward)<br>
    - forward와 backward 계산을 반복해서 진행하면서 intput x와 전달받아 다시 계산된 값(x hat)의 차가 최소가 되도록 weight을 조절
- Xavier / He<br>
    - Xavier : 입력값(fan-in)과 출력값(fan-out) 사이의 난수를 선택해서 입력값(fan-in)의 제곱근으로 나눔
    - He : 입력값(fan-in)을 반으로 나눈 제곱근 사용. 분모가 작아지기 때문에 Xavier보다 넓은 범위의 난수 생성 

## Oberfitting을 방지하는 방법
1. training data 수 늘리기<br>
    : 데이터가 많으면 training set, validation set, test set으로 나누어 진행할 수 있고 영역별 데이터의 크기도 커기지 때문에 overfitting 확률이 낮아짐.
2. 입력으로 들어오는 변수의 개수 줄이기
    : 서로 비중이 다른 feature가 섞여 weight에 대해 경합을 하면 오히려 좋지 않은 결과가 나올 수 도 있음.
3. Regularization 사용

## Regularization
1. L2 regularization<br>
    ![51](https://user-images.githubusercontent.com/63536606/90312991-a6a73400-df43-11ea-8170-f6c2dfc5ac43.PNG)<br>
2. Dropout<br>
    ![52](https://user-images.githubusercontent.com/63536606/90313006-d2c2b500-df43-11ea-8d33-8bc0e806f7ed.PNG)<br>
    : 일부를 비활성화 시킨 후 학습
3. Ensemble<br>
    : 데이터를 여러 개의 training set으로 나누어서 동시에 학습을 진행하여 모든 training set에 대한 학습이 끝나면 결과를 통합하는 방법