# Convolutional Neural Networks

## CNN introduction
![53](https://user-images.githubusercontent.com/63536606/90313223-ca6b7980-df45-11ea-846d-99d010171ff6.PNG)<br>
    : 위 그림에서 보는 것과 같이 한 개의 이미지에서 일부를 읽으면서 전체를 읽는 방식을 CNN이라고 할 수 있음.
    - 작은 필터가 차지하는 영역으로부터 읽어온 값을 공식을 통해 하나의 값으로 변환
    - 동일한 필터를 사용하여 계속해서 다른 영역도 조사
    - 같은 크기의 필터를 수평과 수직으로 이동하며 조사
    - **stride** : 필터가 이동하는 크기
    - **출력 크기** = 1 + (입력 크기 - 필터 크기) / stride 크기 (나누어 떨어져야 함)
    - **padding** : convolutional layer를 거치면서 크기가 작아지기 때문에 원본 이미지 크기를 유지하기 위해 사용

## Pooling layer(sampling)
- Max Pooling<br>
    : 여러 개의 값 중에서 가장 큰 값을 꺼내서 모아 놓는 것

## Fully Connected layer(FC layer)
    : softmax xlassifier와 연결하여 데이터를 labeling

## CNN case
1. LeNet-5<br>
    ![54](https://user-images.githubusercontent.com/63536606/90313493-f7209080-df47-11ea-8509-1a271ef4e626.PNG)
2. AlexNet<br>
    ![55](https://user-images.githubusercontent.com/63536606/90313542-5aaabe00-df48-11ea-9df0-407d6b47db26.PNG)<br>
    : ReLU, dropout, ensemble을 적용하여 좋은 성능을 가지고 있음
3. GoogLeNet<br>
    ![56](https://user-images.githubusercontent.com/63536606/90313600-c7be5380-df48-11ea-8d06-6c63ee265d76.PNG)<br>
4. ResNet<br>
    ![57](https://user-images.githubusercontent.com/63536606/90313632-0bb15880-df49-11ea-9546-266d7cb66d5c.PNG)<br>