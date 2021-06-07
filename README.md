![image](https://user-images.githubusercontent.com/57089832/121043182-5c9f7f80-c7ef-11eb-92a0-f82a9d727bf7.png)

# Carvana-Image-Masking-Challenge

### 1) VGG19 vs Resnet50 vs MobileNetV2

![image](https://user-images.githubusercontent.com/57089832/121049934-23690e80-c7f3-11eb-9297-0919d189ad36.png)

_____________________________________________________________________________________________________________________
### 2) VGG19

![image](https://user-images.githubusercontent.com/57089832/121045768-ccfad080-c7f0-11eb-9d16-25433c01e407.png)

VGG-19는 우리가 조사한 첫 번째 모델이며 검토 한 모델 중 가장 오래된 모델입니다. VGG-19는 VGG-16 모델을 개선 한 것입니다. 19 개의 레이어를 가진 컨볼 루션 신경망 모델입니다. 컨볼 루션을 함께 쌓아서 만들지 만 기울기 감소라는 문제로 인해 모델의 깊이가 제한됩니다. 이 문제는 심층 컨볼 루션 네트워크를 훈련하기 어렵게 만듭니다.

#### VGG19 accuracy

![image](https://user-images.githubusercontent.com/57089832/121054496-5e6d4100-c7f7-11eb-8d75-664f69076534.png)
![image](https://user-images.githubusercontent.com/57089832/121054570-7218a780-c7f7-11eb-8bf2-437550ead56f.png)

- accuraccy = 0.9952

______________________________________________________________________________________________________________________
### 3) Resnet50

![image](https://user-images.githubusercontent.com/57089832/121047689-44c8fb00-c7f1-11eb-8b52-9e487cac1368.png)

기울기 감소 문제를 해결하기 위해 Resnet 모델이 제안되었습니다. 아이디어는 연결을 건너 뛰고 잔차를 다음 레이어로 전달하여 모델이 계속 학습 할 수 있도록하는 것입니다. Resnet 모델을 사용하면 CNN 모델이 더 깊고 깊어 질 수 있습니다.

#### Resnet50 accuracy

![image](https://user-images.githubusercontent.com/57089832/121053933-d424dd00-c7f6-11eb-85c3-0c18ca4eb440.png)
![image](https://user-images.githubusercontent.com/57089832/121054167-0d5d4d00-c7f7-11eb-8acd-c272191ab367.png)

- accuraccy = 0.9967



_______________________________________________________________________________________________________________________
### 4) MobileNetV2

![image](https://user-images.githubusercontent.com/57089832/121052880-c15dd880-c7f5-11eb-943e-10d9777a54aa.png)

모든 convolution을 MobileNet의 depthwise separable convolution으로 대체하였고, 연산량과 파라미터량을 줄이기 위해 전체적으로 convolution의 channel수를 줄이고, block의 내부에서만 channel수를 증가시켰습니다. 기존의 ReLU대신 ReLU6를 사용하였습니다.

#### MobileNetV2 accuracy

![image](https://user-images.githubusercontent.com/57089832/121055033-e18e9700-c7f7-11eb-819b-1882fecf7f6e.png)
![image](https://user-images.githubusercontent.com/57089832/121055217-084ccd80-c7f8-11eb-9317-957b7d1fcf35.png)

- accuraccy = 0.9926









