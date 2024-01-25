# LoRA
LoRA는 기존 pre-trained weight는 고정하고, 몇 개의 dense layer만 rank decomposition matrices를 최적화하는 방식으로 학습시키는 모델입니다.

![lora](https://github.com/DCV1/tutorial/assets/79503414/600a8e74-edd8-4213-9775-92b562d2542b)

Stable diffusion 모델을 fine-tuning하여, 적은 수의 데이터셋을 이용하여 concept customization 할 수 있는 모델입니다.

따라서, 사용자 개인의 경험을 반영하여 **concept을 유지**한 채 이미지를 생성할 수 있습니다. 

예를 들어 우리집 강아지(Doppler)의 이미지를 이용하여 그림을 그려봅시다. Stable diffusion 모델은 우리집 강아지의 이미지를 반영하지 못해 기존에 학습된 이미지 중 강아지 이미지를 사용하여 일반적인 강아지를 사용하여 그림을 그리게 됩니다. 이렇게 방대한 양의 이미지로 학습된 stable diffusion은 사용자 개인의 경험을 반영하기 어렵습니다.

![example1](https://github.com/DCV1/tutorial/assets/79503414/aefe40ed-e0d9-445f-817a-090aef89b59c)

반면에 LoRA 모델은 우리집 강아지(Doppler)의 이미지를 받아 학습시킬 수 있어, 우리집 강아지의 이미지를 이용해 concept customization된 그림을 그릴 수 있습니다.

![example2](https://github.com/DCV1/tutorial/assets/79503414/1d0e7099-e8c8-4461-89d3-ec12fb3dc705)

그래서 저희 팀은 **사용자가 원하는 custom 작품**을 생성할 수 있도록 하기 위해 LoRA 모델을 사용하였습니다. 
