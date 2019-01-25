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
- 예 : 회전(rotation)과 평행이동(translation)만을 허용

|![](https://i.imgur.com/kHTiPA8.png)|![](https://i.imgur.com/BhIj6YR.png)|![](https://i.imgur.com/cO4kh8Z.png)|
|-|-|-|
|평행이동(translation)|회전(rotation)|Rigid = Translation + rotation|

 
#### B. 유사 변환(Similarity Transformations)

- 변환 후에도 유사하게 속성을 유지 한다. (크기는 변경, 각도는 유지)
- 예 : Scaling 

#### C. 선형 변환(Linear Transformation)


??


#### D. Affine Transformations

- (강체변환+유산변환) + 선형 변환
- 변환 후에도 이전의 평행한 선만은 유지 한다.  


#### E. 원근변환(Projective/Homography Transformation) 

- 변환 후에도 최소 선만은 보존된다. 

> cf. 평형사변형은 Affine변환하면 평형 사변형이지만, 원근 변환하면 평행선이 안된다. 

