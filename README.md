![image](https://user-images.githubusercontent.com/57089832/121043182-5c9f7f80-c7ef-11eb-92a0-f82a9d727bf7.png)

# Carvana-Image-Masking-Challenge

### 1) VGG19 vs Resnet50 vs MobileNetV2

![image](https://user-images.githubusercontent.com/57089832/121049934-23690e80-c7f3-11eb-9297-0919d189ad36.png)

_____________________________________________________________________________________________________________________
### 2) VGG19

![image](https://user-images.githubusercontent.com/57089832/121045768-ccfad080-c7f0-11eb-9d16-25433c01e407.png)

VGG-19는 VGG-16 모델을 개선 한 것이고, 19 개의 레이어를 가진 컨볼루션 신경망 모델입니다. 컨볼루션을 함께 쌓아서 만들지만 기울기 감소라는 문제로 인해 모델의 깊이가 제한됩니다. 이 문제는 심층 컨볼루션 네트워크를 훈련하기 어렵게 만듭니다.

#### VGG19 accuracy

![image](https://user-images.githubusercontent.com/57089832/121054496-5e6d4100-c7f7-11eb-8d75-664f69076534.png)
![image](https://user-images.githubusercontent.com/57089832/121054570-7218a780-c7f7-11eb-8bf2-437550ead56f.png)

- accuraccy = 0.9967



______________________________________________________________________________________________________________________
### 3) Resnet50

![image](https://user-images.githubusercontent.com/57089832/121047689-44c8fb00-c7f1-11eb-8b52-9e487cac1368.png)

위에 기울기 감소 문제를 해결하기 위해 Resnet 모델이 제안되었습니다. Resnet의 방식은 연결을 건너 뛰고 잔차를 다음 레이어로 전달하여 모델이 계속 학습 할 수 있도록하는 것이며, Resnet 모델을 사용하면 CNN 모델이 더 깊고 깊어 질 수 있습니다.

#### Resnet50 accuracy

![image](https://user-images.githubusercontent.com/57089832/121053933-d424dd00-c7f6-11eb-85c3-0c18ca4eb440.png)
![image](https://user-images.githubusercontent.com/57089832/121054167-0d5d4d00-c7f7-11eb-8acd-c272191ab367.png)

- accuraccy = 0.9952



_______________________________________________________________________________________________________________________
### 4) MobileNetV2

![image](https://user-images.githubusercontent.com/57089832/121052880-c15dd880-c7f5-11eb-943e-10d9777a54aa.png)

MobileNetV2는 대표적인 경량화 네트워크인 MobileNetV1의 높은 버전으로써 모든 convolution을 MobileNet의 depthwise separable convolution으로 대체되였고, 연산량과 파라미터량을 줄이기 위해 전체적으로 convolution의 channel수를 줄이고, block의 내부에서만 channel수를 증가시켰습니다. 그리고 출력함수를 기존의 ReLU대신 ReLU6를 사용하였습니다.

#### MobileNetV2 accuracy

![image](https://user-images.githubusercontent.com/57089832/121055033-e18e9700-c7f7-11eb-819b-1882fecf7f6e.png)
![image](https://user-images.githubusercontent.com/57089832/121055217-084ccd80-c7f8-11eb-9317-957b7d1fcf35.png)

- accuraccy = 0.9926



_______________________________________________________________________________________________________________________
### 5) Resnet50_update

![image](https://user-images.githubusercontent.com/57089832/121233102-3e0fb600-c8cd-11eb-823f-d6bd7cfb4248.png)

특징 출력 기능을 수행하는 계층을 추가하여 Resnet50의 성능을 향상시켰지만 아직까지 VGG19를 넘어서지는 못했습니다.

![image](https://user-images.githubusercontent.com/57089832/121232974-1a4c7000-c8cd-11eb-98d9-32b79950bc8e.png)
![image](https://user-images.githubusercontent.com/57089832/121233285-7911e980-c8cd-11eb-9eb2-ffef95fa5d68.png)

- accuraccy = 0.9962
_______________________________________________________________________________________________________________________
### 5) Result

맨위에 그림 그래프에서는 정확도가 Resnet50 > VGG19 > MobileNetV2 이지만 실제로 구현을 해봤을때는  VGG19 > Resnet50 > MobileNetV2 로 결과가 나왔습니다.
그 이유로 추정해봤을때는  down stack과 up stack을 합쳐주는 부분과 이미지 전처리 부분의 코딩 수정이 필요한것같습니다. 앞으로 보완하면 정상 결과를 추출할 수 있을것같습니다.







