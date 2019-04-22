# Transformations

> [[영상 Geometry #5] 3D 변환](https://darkpgmr.tistory.com/79?category=460965) : 다크프로그래머 블로그 
> [[추천] 3D TRANSFORMATIONS](http://web.iitd.ac.in/~hegde/cad/lecture/L6_3dtrans.pdf): ppt
> [Rotation matrix](https://en.wikipedia.org/wiki/Rotation_matrix): 위키피디




## 1. 2D 변환

> 이전 노트 참고 

## 2. [3D 변환 (3D Transformations)](https://darkpgmr.tistory.com/81?category=460965)


- 강체 변환(회전, 평행 이동)만 고려 
- 물체의 크기가 커지거나(scale), 모양이 변하는것은 고려 안함 


### 2.1 변환 행렬


#### A. 회전 


3차원 공간의 점 (X, Y, Z)를 X축, Y축, Z축을 중심으로 θ 라디안(radian) 회전시키는 행렬을 각각 Rx(θ), Ry(θ), Rz(θ)라 하면 이들은 다음과 같다.

|![](https://i.imgur.com/lQ6Bb4L.png)|![](https://i.imgur.com/jsnfVGd.png)|
|-|-|
|![](https://i.imgur.com/t5Fxl4L.png)|위 3개의 기본 회전변환 조합하면  임의의 3D 회전을 표현할 수 있다.|
|![](https://t1.daumcdn.net/cfile/tistory/024BBD4551E1D44422)|임이의 단위벡터$$u=(u_x, u_y, u_z)$$를 축으로 한 회전 변환 행렬|

#### B. 평행 이동 

평행 이동 $$ t=[tx,ty,tz]^T $$ 




#### C. 회전(R) + 평행 이동(t) = 변환행렬  

|![](https://i.imgur.com/XnxT2oA.png)|![](https://i.imgur.com/gywfsCX.png)|
|-|-|
|변환행렬 |변환행렬 (homogeneous 좌표 표현)|


>  어떤 행렬 R이 회전변환이 되기 위한 **필요충분 조건**은 RT = R-1, det(R) = 1 이라 한다.

### 2.2 변환 행렬 구하기 

#### A. 회전 변환 구하기 

> 자세한 내용은 홈페이지 [참고](https://darkpgmr.tistory.com/81?category=460965)


#### B. 회전 + 평행 이동 변환 구하기 

![](https://i.imgur.com/X2pOb4m.png)

3D에서 rigid 변환을 결정하기 위해 필요한 매칭쌍의 개수는 3개입니다.


> 자세한 내용은 내공 쌓고 다시 [참고](https://darkpgmr.tistory.com/81?category=460965)



### 2.3 좌표축 변환 

월드 좌표계 -> 카메라 좌표계로의 변환 [[참고]](https://darkpgmr.tistory.com/84)