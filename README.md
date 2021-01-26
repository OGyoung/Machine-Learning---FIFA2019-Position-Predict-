# FIFA2019 데이터를 이용한 선수 포지션 예측
FIFA2019 데이터에서 선수들의 스탯을 보고 포지션을 예측해본다.

## 데이터 받아오기
![kaggle 사이트](https://user-images.githubusercontent.com/52282493/105815259-ffe8b880-5ff5-11eb-9906-d80f1dc06aba.png)
[kaggle]https://www.kaggle.com/karangadiya/fifa19

## 데이터 분석하기
받아온 데이터set이 어떻게 되어있는지 확인

(몇 개의 샘플인지, 어떤 특성을 갖고있는지)

![image](https://user-images.githubusercontent.com/52282493/105817851-881c8d00-5ff9-11eb-8e8d-7469c6f1f7cf.png)
***
![image](https://user-images.githubusercontent.com/52282493/105818075-cade6500-5ff9-11eb-80f3-d5b148ebc9bc.png)

## 데이터 수정하기
1. 특성(스탯) 중에서 분류에 영향을 주지않는 특성 제거

   * 포지션 별로 스탯을 비교해서 차이가 거의 없는 경우를 찾기
   
     공격수, 수비수, 미드필더 세 포지션을 가지고서 비교
     
     각 포지션만 따로 정렬해서 1000개만 사용
     
     ![image](https://user-images.githubusercontent.com/52282493/105831368-f5d0b500-6009-11eb-8428-cea60756c4a4.png)
     ![image](https://user-images.githubusercontent.com/52282493/105831548-303a5200-600a-11eb-9e19-278c66c9e0c0.png)
     ![image](https://user-images.githubusercontent.com/52282493/105831569-37616000-600a-11eb-9a52-811c96643ed9.png)
     ![image](https://user-images.githubusercontent.com/52282493/105831700-6677d180-600a-11eb-9d3c-b6b0b6e4344d.png)
     
     해당 열마다 값을 다 더하고 포지션 별로 차이가 나는지 확인
     
     ![image](https://user-images.githubusercontent.com/52282493/105831832-8effcb80-600a-11eb-845a-ad82e5dd91cc.png)
     ![image](https://user-images.githubusercontent.com/52282493/105831901-a343c880-600a-11eb-875a-cd1799b7c125.png)
     ![image](https://user-images.githubusercontent.com/52282493/105831924-aa6ad680-600a-11eb-8469-3140556d6f32.png)
     
     ![image](https://user-images.githubusercontent.com/52282493/105832120-e69e3700-600a-11eb-9b49-f1e28f7520e3.png)
     
<center>그래프로 표현</center>
     
     <center>↓</center>
     
     ![image](https://user-images.githubusercontent.com/52282493/105853690-4a375d00-6029-11eb-9433-e35656e8e6b3.png)

     
     
     
2. 비슷한 영역의 포지션을 하나의 포지션으로 합쳐서 데이터 수 늘리기

3. NULL 값 들어간 데이터 삭제

   →  .dropna() 사용
4. 훈련set, 시험set 나누기



