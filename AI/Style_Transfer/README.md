# Style Transfer 논문 실습 및 결론 도출
 - DaeJeong Kim([v4chelsea](https://github.com/v4chelsea))
 - 2021/08/30 ~ 2021/08/31
<br></br>

## Style Transfer 논문
 - 제목 : Image Style Transfer Using Convolutional Neural Networks
 - 링크 : [https://rn-unison.github.io/articulos/style_transfer.pdf](https://rn-unison.github.io/articulos/style_transfer.pdf)
<br></br>

## Style Transfer 테스트 결과

1. My Face + The Starry Night
![result_plt-1 (1)](https://user-images.githubusercontent.com/56423426/131475668-8476dcef-50a0-458d-ae94-89ecd8f45cdb.png)
<br></br>
2. Scenery Photo + The Starry Night
![result2_plt-1 (1)](https://user-images.githubusercontent.com/56423426/131475677-057c7daa-3a35-4025-83c9-5ec7f799add8.png)
<br></br>
3. Cat + The Starry Night
![result3_plt-1 (1)](https://user-images.githubusercontent.com/56423426/131475683-505a44e2-38e9-4655-9324-a7bce289a0fb.png)
<br></br>

### 결론
 - 위 테스트 결과를 미뤄봤을 때, 30 ~ 50 Epoch의 이미지가 가장 자연스러운 형태로 Style Transfer가 진행된것으로 보인다.
 - 본 리뷰에서는 Max Epoch를 100로 제한하였으나, 100 Epoch를 넘어가는 형태로 테스트를 진행하였을 때, Content의 이미지가 Style 이미지에 점차 잠식되어 Content의 형태가 완전히 사라진다.
 - 위 내용은 Epoch가 덜 진행된 상태에서는 Content가 많이 진행된 상태에서는 Style이 더 강세를 보이는 형태로 ```Epoch를 기준으로 Content와 Style이 Trade Off 관계``` 라는 추측이 가능하다. 
 - 100 Epoch동안 학습을 진행하면서 약 130 ~ 150초의 소요시간이 걸렸다.
 - 학습된 모델이 이미지를 출력하는 시간은 0.015 ~ 0.02초로 반복문을 통해 테스트를 진행한 결과 최초 이미지 출력이 가장 오래걸렸고, 반복을 진행하면서 점차 0.017초로 수렴되었다.
 - 이미지 출력에 걸린 Max Time : 0.02022, Min Time : 0.01589 
<br></br>

## 참고 내용
플랫폼|이름 / 제목|링크
---|---|---
Youtube|동빈나 / CNN을 활용한 스타일 전송(Style Transfer) 꼼꼼한 딥러닝 논문 리뷰와 코드 실습|https://www.youtube.com/watch?v=va3e2c4uKJk&t=441s|
Blog|뭉그적뭉그적 / [논문 리뷰] Image Style Transfer Using Convolutional Neural Networks, Instance Normalization|https://jayeon8282.tistory.com/12|
Blog|Lunit Tech Blog / Style Transfer|https://blog.lunit.io/2017/04/27/style-transfer/|
Tensorflow|Tensorflow Official / tf.keras를 사용한 Neural Style Transfer|https://www.tensorflow.org/tutorials/generative/style_transfer?hl=ko|
