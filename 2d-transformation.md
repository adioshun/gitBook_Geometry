# Transformations

> [darkpgmr](https://darkpgmr.tistory.com/79?category=460965), [shksjy](http://blog.daum.net/shksjy/228)

## 1. 2D 변환 (2D Transformations)


변환 : 점 x를 점 x'에 매핑하는 함수

### 1.1 변환의 예 
- Translation 
- Rotation 
- Scaling

![](https://i.imgur.com/VIk8stX.png)


### 1.2 변환의 종류 

![](https://i.imgur.com/awcWP5u.png)

분류의 기준은 변환된 후 그 물체의 특성이 어느 정도까지 보존되는가에 따른 것이다.
- 강체 변환(Ridid-Body transformation)
- 유사 변환(Similarity Transformations)
- 선형 변환(Linear Transformation)
- Affine Transformations
- 원근변환(Projective Transformation)

#### A. 강체 변환(Ridid-Body/Euclidean transformation)

- 강체 = 단단한 물체 
- 변환 후에도 속성(크기, 각도)을 유지한다.
- 자유도 3 : 변환을 추정하기 위해서는 최소 2개 이상의 매칭쌍을 필요
- 예 : 회전(rotation)과 평행이동(translation)만을 허용

|![](https://i.imgur.com/kHTiPA8.png)|![](https://i.imgur.com/BhIj6YR.png)|![](https://i.imgur.com/cO4kh8Z.png)|
|-|-|-|
|평행이동(translation)|회전(rotation)|Rigid = Translation + rotation|

 
#### B. 유사 변환(Similarity Transformations)

- 강체 변환 + Scale 변화
- 변환 후에도 유사하게 속성을 유지 한다. (크기는 변경, 각도는 유지)
- 자유도 4 : similarity 변환을 유일하게 결정하기 위해서는 2개의 매칭쌍이 필요

|![](https://i.imgur.com/tyNrZHS.png)|![](https://i.imgur.com/XQVz4m8.png)|
|-|-|
|Similarity Transformations |Similarity Transformations (homogeneous 좌표 표현)|

#### C. 선형 변환(Linear Transformation)


??


#### D. Affine Transformations

- (강체변환+유사 변환) + 선형 변환
- 회전, 평행이동, 스케일 + shearing, 반전(reflection)까지를 포함
- 변환 후에도 이전의 평행한 선만은 유지 한다.  
- 자유도 6 : 3쌍의 매칭쌍이 있으면 affine 변환을 유일하게 결정할 수 있

|![](https://i.imgur.com/GTkN5X7.png)|![](https://i.imgur.com/jlw9HRm.png)|
|-|-|
|Affine Transformations |Affine Transformations (homogeneous 좌표 표현)|

> cf. 평형사변형은 Affine변환하면 평형 사변형이지만, 원근 변환하면 평행선이 안된다. 



#### E. 원근변환(Projective/Homography Transformation) 

- 변환 후에도 최소 선만은 보존된다. 
- 자유도 8 : 최소 4개의 매칭쌍을 필요 

> 9가 아니라 8인 이유는 (x,y,1), (wx',wy',w)이 homogeneous 좌표이므로 homography의 scale을 결정할 수 없기 때문



|_homogeneous 좌표계에서 정의_|![](https://i.imgur.com/Jq2zgPO.png)|
|-|-|
|Projective Transformations |Projective Transformations (homogeneous 좌표 표현)|




