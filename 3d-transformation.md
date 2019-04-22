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





### 2.3 좌표축 변환 

월드 좌표계 -> 카메라 좌표계로의 변환 [[참고]](https://darkpgmr.tistory.com/84)