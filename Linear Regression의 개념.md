# Linear Regression의 개념

## Regression (data)
|  <center>X</center> |  <center>Y</center> | 
|:--------|:--------:|
| <center>1<center> | <center>1</center> |
| <center>2<center> | <center>2</center> |
| <center>3<center> | <center>3</center> |

![1](https://user-images.githubusercontent.com/63536606/90256191-4e5b2e00-de80-11ea-87ab-626a48729ffe.PNG)

## (Linear) Hypothesis
![2](https://user-images.githubusercontent.com/63536606/90256335-8bbfbb80-de80-11ea-9964-4fea129a5b52.PNG)
- W와 b에 따라 선이 나타남.

![3](https://user-images.githubusercontent.com/63536606/90256439-b4e04c00-de80-11ea-9c57-37e405c582f6.PNG)
- 실제 데이터와의 거리를 계산하여 좋은 가설인지를 판단 (cost function)

## Cost function
- H(x) - y = 가설 값 - 실제 값
- $$ \(H(x)-y)^2 $$ : 차이가 음수 / 양수 상관 없음
- $$ \{(H(x_1)-y_1)^2 + (H(x_2)-y_2)^2 + (H(x_3)-y_3)^2} / 3 $$
- cost = 1/m*