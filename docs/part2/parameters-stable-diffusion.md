# Stable Diffusion - 주요 Paramemters

<br>

## Checkpoint
<details>
<summary><b>Web UI Screenshot</b></summary>
    
![Untitled](media-deforum-parameters/Untitled.png)
</details>


### 설명

- 특정 스타일의 이미지를 생성하기 위한 ****pre-trained Stable Diffusion weights
- 적용 방법 : `stable-diffusion-webui/models/Stable-diffusion` 폴더에 원하는 모델의 `.safetensors` 파일을 저장

### 예시
<!--
![ckpt_v15_20240113071553.gif](media-sd-parameters/ckpt_v15_20240113071553.gif)

v1-5-pruned-emaonly.safetensors (default)

![ckpt_sdxl_20240113070148.gif](media-sd-parameters/ckpt_sdxl_20240113070148.gif)

stable-diffusion-xl-refiner-1.0

![ckpt_dreamshaper_20240113071026.gif](media-sd-parameters/ckpt_dreamshaper_20240113071026.gif)

dreamshaper_8.safetensors
-->

| v1-5-pruned-emaonly.safetensors <br> (default) | stable-diffusion-xl-refiner-1.0 | dreamshaper_8.safetensors |
| :----: | :----: | :----: |
| <img src="media-sd-parameters/ckpt_v15_20240113071553.gif" width="100%"> | <img src="media-sd-parameters/ckpt_sdxl_20240113070148.gif" width="100%"> | <img src="media-sd-parameters/ckpt_dreamshaper_20240113071026.gif" width="100%"> |
- **Prompt** : a man standing on the beach looking at the sea

### 팁

- webui 기본 checkpoint인 `v1-5-pruned-emaonly.safetensors` 로 영상을 생성할 경우 영상 퀄리티가 좋지 않음
- 전시회 작품은 SDXL, Dreamshaper을 주로 사용함

<br>

## Sampler
<details>
<summary><b>Web UI Screenshot</b></summary>
    
![Untitled](media-deforum-parameters/Untitled%201.png)
</details>

### 설명

- Diffusion 과정의 각 단계에서 새로운 샘플 이미지를 생성할 때 노이즈를 제거하는 방법

- [Complete guide to samplers in Stable Diffusion](https://www.felixsanz.dev/articles/complete-guide-to-samplers-in-stable-diffusion)

- [ArtStation - Stable Diffusion - Samplers](https://www.artstation.com/blogs/kaddoura/pBPo/stable-diffusion-samplers)

### 예시


<!--
![Euler_a_japanese.gif](media-sd-parameters/Euler_a_japanese.gif)

Euler a : 3min 41s

![LMS_japanese_20231028071030.gif](media-sd-parameters/LMS_japanese_20231028071030.gif)

LMS : 3min 44s

![DPM__2M_Karras_japanese.gif](media-sd-parameters/DPM__2M_Karras_japanese.gif)

DPM++ 2M Karras: 3min 6s
-->

| Euler a | LMS | DPM++ 2M Karras |
| :----: | :----: | :----: |
| <img src="media-sd-parameters/Euler_a_japanese.gif" width="100%"> | <img src="media-sd-parameters/LMS_japanese_20231028071030.gif" width="100%"> | <img src="media-sd-parameters/DPM__2M_Karras_japanese.gif" width="100%"> |
- **Prompt** : the old japanese street side on an avenue with trees, in the style of concept art, lively tavern scenes, muted palette, bloomcore, cherry blossoms, anime-inspired, religious building

### 팁

- Prompt 별로 잘 그려내는 sampler가 다름
- 모든 Prompt에서 노이즈처럼 그려내는 sampler들도 있음
    - LMS, DPM++ 2M SDE, DPM++ 2M SDE Heun, PLMS
- Euler, Euler a가 눈에 보기에 가장 자연스럽고, Kaiber 영상과 가장 유사함
- 전시회 작품은 Euler a를 사용함

<br>

## Steps
<details>
<summary><b>Web UI Screenshot</b></summary>
    
![Untitled](media-deforum-parameters/Untitled%202.png)
</details>


### 설명

- Diffusion 과정의 한 단계에서 주어진 프롬프트 도달까지 반복하는 샘플링 횟수
- 값이 크면 생성이 오래 걸리는 대신 그만큼 생성되는 이미지의 퀄리티가 올라감
- 값이 작으면 생성이 빠른 대신 이미지의 퀄리티가 떨어짐
- 값이 어느 정도 이상보다 더 커지면 더 이상 이미지의 퀄리티가 증가하지 않음

### 예시

<!--
![bulb_step_10.gif](media-sd-parameters/bulb_step_10.gif)

step = 10

![bulb_step_20.gif](media-sd-parameters/bulb_step_20.gif)

step = 20

![bulb_step_30.gif](media-sd-parameters/bulb_step_30.gif)

step = 30
-->
| step = 10 | step = 20 | step = 30 |
| :----: | :----: | :----: |
| <img src="media-sd-parameters/bulb_step_10.gif" width="100%"> | <img src="media-sd-parameters/bulb_step_20.gif" width="100%"> | <img src="media-sd-parameters/bulb_step_30.gif" width="100%"> |
- **Prompt** : a light bulb is put on a table near a gray wall, in the style of light cyan and gold, use of screen tones, youthful energy, iso 200, organic material, clean-lined, award-winning

### 팁

- Sampler의 종류에 따라 필요한 steps 수가 달라짐
- 평균적으로 25이상이면 이미지 퀄리티가 크게 달라지지 않음
- 전시회 작품은 주로 25을 사용함

<br>

## Seed
<details>
<summary><b>Web UI Screenshot</b></summary>
    
![Untitled](media-deforum-parameters/Untitled%203.png)
</details>


### 설명

- 생성 과정에 걸쳐 이미지를 일관되게 유지할 수 있는 기능(숫자)
- 다른 사용자가 영상을 생성하더라도 seed를 비롯한 타 조건이 동일하면 동일한 결과물 생성이 가능함
- Behavior 예시 :
    1. **Iter** = incremental change (ex 77, 78, 79 ,80, 81, 82, 83…)
    2. **Fixed** = no change in seed (ex 33, 33, 33, 33, 33, 33…)
    3. **Random** = randomized seed (ex 472, 12, 927812, 8001, 724…)

### 팁

- Seed behavior 중에서 fixed를 사용할 경우 시드가 동일해지면서 노이즈 제거가 발생하지 않아 시간이 지나면서 이미지가 노이지로 뒤덮이게 되거나 이미지가 flat하게 보이는 등의 문제가 발생하므로 피하는 것이 좋음
