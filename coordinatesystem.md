# 좌표계 (Coordinate System)

> https://darkpgmr.tistory.com/77

![](https://i.imgur.com/7BZIQE3.png)


## 1. 월드 좌표계 (World Coordinate System)

- 3D 좌표계 

## 2. 카메라 좌표계 (Camera Coordinate System)

![](https://i.imgur.com/2KBVl1E.png)

- 3D 좌표계 
- 카메라 위치를 기

## 3. 픽셀(=이미지) 좌표계 (Pixel Image Coordinate System) 


- 2D 좌표계 


## 4. 정규 좌표계 (Normalized Image Coordinate System)

- 2D 좌표계 

- 가상의 좌표계 : 카메라의 내부 파라미터(intrinsic parameter)의 영향을 제거한 이미지 좌표계

- 카메라 초점과의 거리가 1인 가상의 이미지 평면을 정의하는 좌표계

- 표현 : $$u, v $$

- 도입 이유 : 
    - 동일한 장면을 찍더라도 카메라에 따라서 또는 카메라 세팅에 따라서 서로 다른 영상을 얻게 됨, 이를 제거한 좌표계 
    - 기하학적인 해석은 카메라 파라미터가 제거된 정규 이미지 평면에서 하는 것이 보다 용이 하므로 


---

# Homogeneous Coordinates

기하학 분류 
- 유클리디언 기하학 - 데카르트(=직교) 좌표계 사용 
- 사영(=projective) 기하학 - 동차(=**Homogeneous**,projective)좌표계 사용 

차수를 동일하게 유지 (eg. 직선)
- 직교 좌표계 : 직선의 1차 다항식은 x,y는 1차, 상수는 0차 
- 동차 좌표계 : 직선의 1차 다항식은 x,y,상수 모두 1차 

좌표계 변환 
- 동차 좌표계에서 한점 (x,y,w)는 xy 평면 좌표계에서 (x/w, y/x)가 된다. --> 마지막 값으로 나누어 1로 만들어 버리기. 
- xy 평면 좌표계에서 (x,y)는 동차 좌표계에서 (x,y,1)이 된다. --> 단순히 1더하기. 

원근 투영을 위해 사용 
- 3차원의 공간을 2D 이미지 평면에 투영 시킬때 투영선(projetcion ray) 사용
- 투영선에 걸쳐 있는 모든 점들을 하나의 동일한 점으로 투영 
- eg : (1,1,1), (1,1,2), (1,1,3)은 (1,1)

사영 기하학에서는 길이(length), 각도(angle), 평행성(parallelism)이 보존되지 않음 


> 우리가 유클리디언 기하학에서 익히 알고 있는 사실은 평행한 두 선(line)은 결코 만나지 않는다 입니다. 그런데, 사영 기하학에서는 평행한 두 선의 교점을 구할 수 있습니다. 우리가 이미지에서 흔히 보는 vanishing point가 바로 그 교점입니다.


