# 활용 툴 (dall•e3, 미드저니, playground 등)

아트랩 사업을 준비하며 여러 작품 제작을 하는데 있어 생산성 향상에 도움은 제공한 몇 가지 툴을 소개합니다. DCV LAB은 매주 이러한 AI 기반의 이미지 생성 툴을 활용한 작품들을 만들어 실험하고 피드백을 주고 받으며 기술적 측면 뿐아니라 실제로 작품을 만들며 아이디어 중심적인 실험을 추구합니다. 

## [DALL•E 3](https://openai.com/dall-e-3)

세부적인 상세 설명을 따르도록 성능이 향상된 text-to-image 모델입니다. 예술가들이 복잡한 아이디어를 시각화할 때 원하는 느낌의 이미지에 대한 설명을 제공하면, 더 정확하고 섬세한 이미지 결과를 얻을 수 있게 해줍니다. 모델은 이미지 캡션을 통해 훈련되어, 주어진 프롬프트에 대해 더 일관되고 미적으로 만족스러운 이미지를 생성하며 의도하고 싶은 바가 정확할 경우 최적의 이미지를 생성할 수 있습니다. 자세한 사항은 [DALL•E 3](https://cdn.openai.com/papers/dall-e-3.pdf) 페이퍼에서 확인하실 수 있습니다.

<a href="https://cdn.openai.com/papers/dall-e-3.pdf"><img src="image/dall-e-3.png" alt="dall-e-3" width=80% align="center"></a>

## Midjourney

대규모 이미지와 해당 텍스트 설명 데이터셋을 학습하여 텍스트 기반 프롬프트를 시각적 개념과 연결하는 고급 언어 모델을 기반으로 합니다. 학습 데이터에는 인터넷에서 스크랩한 텍스트와 이미지가 포함되며, 인기 있는 학습 데이터셋으로는 Microsoft의 Common Objects in Context (COCO) 데이터셋이 있습니다. 이 데이터셋에는 약 330,000개의 이미지와 2.5백만 개의 캡션이 포함되어 있으며, 약 80개의 객체 카테고리, 개념 및 장면을 커버합니다. Visual Genome 및 Flickr30k 데이터셋과 같은 다른 인기 있는 학습 데이터셋도 있습니다.

Midjourney는 다양한 알고리즘 버전을 출시하면서 계속해서 알고리즘을 개선해 왔습니다. 2023년 12월에는 버전 6이 출시되어 텍스트 렌더링 개선과 프롬프트에 대한 더 리터럴한 해석을 지원하게 되었습니다. 

<a href="https://www.midjourney-v6.com/advanced-midjourney-v6-guide/"><img src="image/midhourney-v6.png" alt="midhourney-v6" width=80% align="center"></a>

특히, 버전 6에서는 ‘**Consistent Styles**’라는 새로운 테스트 알고리즘을 출시하였습니다. Dev 팀에서는 “Style References”라고 부르며, 작업하려는 일관된 스타일을 ‘describe’하는 하나 이상의 이미지에 대한 URL을 제공하는 이미지 프롬프트와 유사하게 작동합니다. 버전 6에 관한 더 자세한 이야기는 [Midjourney v6 Blog](https://www.midjourney-v6.com/blog/)에서 확인하실 수 있습니다.

<a href="https://www.midjourney-v6.com/a-deeper-dive-into-midjourneys-style-reference-strength/"><img src="image/midjourney-sref.png" alt="midjourney-sref" width=80% align="center"></a>

이러한 기술적 진보에도 불구하고, Midjourney의 학습 방법과 사용된 데이터에 대한 윤리적 논란이 있습니다. 예술가들 사이에서는 자신의 작품이 동의 없이 AI 학습에 사용된다는 우려가 제기되었습니다.

예술가들에게 빠른 프로토타이핑, 광고 산업에서의 창의적 콘텐츠 생성, 건축 분야에서의 무드 보드 생성 등 다양한 용도로 활용될 수 있습니다.

## [Playground](https://playgroundai.com/)

AI research와 product design을 결합한 **free-to-use online AI image creator**이며 누구나 전문가가 아니어도 전문가처럼 그래픽을 만들 수 있도록 지원합니다. 실제 이미지와 합성 이미지를 결합하여 예술 작품과 사실적인 이미지를 만들 수 있는 "**Mixed Image Editing**" 기능을 제공합니다. 사용자는 상상하는 대로 이미지를 편집하고, 이미지를 원래의 가장자리를 넘어 확장하며, 어떤 장면에나 객체를 적합하게 배치하고, 스케치를 현실로 변환할 수 있습니다.

<a href="https://youtu.be/ddoXfmzeT_A?feature=shared"><img src="image/image.png" alt="Playground Mixed Image Editing" width=80% align="center"></a>