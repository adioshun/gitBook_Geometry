# Transformations

> [[영상 Geometry #5] 3D 변환](https://darkpgmr.tistory.com/79?category=460965) : 다크프로그래머 블로그 
> [[추천] 3D TRANSFORMATIONS](http://web.iitd.ac.in/~hegde/cad/lecture/L6_3dtrans.pdf): ppt
> [Rotation matrix](https://en.wikipedia.org/wiki/Rotation_matrix): 위키피디



1. 오일러각과 회전행렬(Euler Angles and Rotation Matrix) - http://blog.daum.net/pg365/170
2. 각속도(Angular Velocity)와 오일러각, 회전행렬 간의 관계 - http://blog.daum.net/pg365/171
3. 쿼터니언(Quaternion)과 오일러각, 회전행렬 간의 관계 - http://blog.daum.net/pg365/172
4. 회전 보간: 쿼터니언(Quaternion)을 사용한 Slerp(구면 선형 보간) - http://blog.daum.net/pg365/176

 
## 1. 2D 변환

> 이전 노트 참고 

## 2. [3D 변환 (3D Transformations)](https://darkpgmr.tistory.com/81?category=460965)


- 강체 변환(회전, 평행 이동)만 고려 
- 물체의 크기가 커지거나(scale), 모양이 변하는것은 고려 안함 


### 2.1 변환 행렬 (오일러 앵글 이용하여)


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

### 2.2 변환 행렬 구하기 (예)

목적 :  비행기 동선의 임의의 두 지점 사이의 변환관계를 구하는 것

#### A. 회전 변환 구하기 

u을 u'로 이동시키는 회전변환은 다음과 같이 구할 수 있습니다.
- u = [x, y, z]T
- u' = [x', y', z']T

##### 가. 회전각 θ와 회전축 단위벡터 v 구하기 

![](https://i.imgur.com/UKkRg7I.png)

- 사잇각(θ): 두 벡터 u, u' 사이의 사잇각 =  벡터의 내적을 이용하여 계산 
- 회전축(v) : 두 벡터 u, u'에 의해 결정되는 평면에 수직인 벡터 -> 벡터의 외적을 이용하면 된다. 

> 벡터의 외적 u1 × u2 란 두 벡터 u1, u2에 의해 결정되는 평면에 수직이면서(오른손 방향) 그 크기가 u1, u2를 두 변으로 하는 평행사변형의 면적과 같은 벡터를 말합니다

##### 나. 임이의 단위벡터$$u=(u_x, u_y, u_z)$$를 축으로 한 회전 변환 행렬 구하기 

![](https://t1.daumcdn.net/cfile/tistory/024BBD4551E1D44422)



#### B. Rigid 변환 구하기(회전 + 평행 이동) 

![](https://i.imgur.com/X2pOb4m.png)
절차 
- 1) p1이 원점이 되도록 A를 평행이동 시킨 후, 
- 2) A'의 방향과 일치되도록 회전시켜서, 
- 3) p1'까지 평행이동시킨다 

https://darkpgmr.tistory.com/81?category=460965



> 3D에서 rigid 변환을 결정하기 위해 필요한 매칭쌍의 개수는 3개입니다.




### 2.3 좌표축 변환 

월드 좌표계 -> 카메라 좌표계로의 변환 [[참고]](https://darkpgmr.tistory.com/84)