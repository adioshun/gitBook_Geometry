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

