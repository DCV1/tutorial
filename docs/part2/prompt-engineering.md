# 프롬프트 엔지니어링

## Prompt Engineering

![Untitled](media_prompt-enginering/Untitled.png)

### General Tips

1. Negative Prompts
    - **worst quality, normal quality, low quality, low res, blurry, text, watermark, logo, banner, extra digits, cropped, jpeg artifacts, signature, username, error, sketch ,duplicate, ugly, monochrome, horror, geometry, mutation, disgusting**  : 전반적인 이미지 품질이 올라감
    - **bad anatomy, bad hands, three hands, three legs, bad arms, missing legs, missing arms, poorly drawn face, bad face, fused face, cloned face, worst face, three crus, extra crus, fused crus, worst feet, three feet, fused feet, fused thigh, three thigh, fused thigh, extra thigh, worst thigh, missing fingers, extra fingers, ugly fingers, long fingers, horn, realistic photo, extra eyes, huge eyes, 2girl, amputation, disconnected limbs** : 애니메이션 캐릭터를 더 잘 그림
    - **bad anatomy, bad hands, three hands, three legs, bad arms, missing legs, missing arms, poorly drawn face, bad face, fused face, cloned face, worst face, three crus, extra crus, fused crus, worst feet, three feet, fused feet, fused thigh, three thigh, fused thigh, extra thigh, worst thigh, missing fingers, extra fingers, ugly fingers, long fingers, horn, extra eyes, huge eyes, 2girl, amputation, disconnected limbs, cartoon, cg, 3d, unreal, animate** : 사실적인 캐릭터 묘사에 좋음
    - **nsfw, nude, censored** : 성인 및 유해 컨텐츠 생성 제한
    - **bad anatomy** : 부자연스러운 신체표현이 개선됨
        
        ![One white man is dancing, detailed, realistic](media_prompt-enginering/original.gif)
        
        One white man is dancing, detailed, realistic
        
        ![One white man is dancing, detailed, realistic, —neg bad arms, bad anatomy, bad fingers](media_prompt-enginering/add_negative_prompts.gif)
        
        One white man is dancing, detailed, realistic, —neg bad arms, bad anatomy, bad fingers
        
    - **bad face, people** : positive에 사람을 넣을 경우 사람 뒷모습이 주로 나옴
    - **bad arms** : positive에 사람을 넣을 경우 상반신이 주로 나옴
    - **white space, frame** : 그림 테두리에 빈공간이 생기는 현상이 완화됨
2. Key Prompts
    - **neon, sf, mecha funk, star**
3. View/Composition 관련 Prompt
    - **Centered Compositio**n : 중앙 배치
    - **Birds-eye View** : 공중에서 내려다 보는 시야
    - **Up View** : 아래에서 올려다 보는 시야
    - **Rule of Thirds** : 조화롭고 균형있는 배치
    - **Symmetrical** : 좌우 대칭
4. Layout 관련 Prompt
    - in the style of **grid composition**: 이미지가 격자 모양으로 배치되지만 이미지 배경에 격자무늬가 생김
        
        ![Untitled](media_prompt-enginering/Untitled%201.png)
        
    - in the style of **tile composition**: 이미지 배경의 격자무늬는 사라지지만 이미지 배치가 격자가 아닌 자유로운 배치로 배치됨
        
        ![Untitled](media_prompt-enginering/Untitled%202.png)
        
    - in the style of **grid layout**: 이미지가 격자 모양으로 배치되고, 격자무늬도 완화됨
        
        ![Untitled](media_prompt-enginering/Untitled%203.png)
        
5. 주로 예술작품을 prompt에 작성하게 되면 액자 프레임이 생성되는 경향이 있음
    - 특히 zoom out 하게 되면 테두리에 줄이 생기는 현상이 좀 더 빈번하게 생기는 듯함
6. 특정 화가를 넣으면 해당 화가의 화풍으로 그림
    - ex) Starry Night by Wassily Kandinsky
7. Prompt가 너무 길어지면 오히려 반영을 잘 못함
8. CLIP scale 값을 내리면 prompt를 매우 잘 반영함

### Deforum 관련 Tips

1. 영상 색감이 첫 이미지 색감을 따라가는 경향이 있음
    
    ![output1.gif](media_prompt-enginering/output1.gif)
    
    ![output2.gif](media_prompt-enginering/output2.gif)
    

1. Camera movement를 한 방향으로 움직일 때 사람이나 물체를 많이 넣으면 어색함
2. Positive prompt - Prompt - Negative Prompt 순으로 반영이 잘되고, 그 안에서도 앞에 있을 수록 반영이 더 잘됨
    - 객체, 스타일 순으로 넣는 것이 좋음
3. 사람과 비행기 등 구체적인 묘사가 필요한 객체는 어색한 경우가 많으므로 최대한 배제하는 것이 좋음
