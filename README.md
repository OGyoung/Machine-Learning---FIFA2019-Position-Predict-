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
>> 포지션 별로 스탯을 비교해서 차이가 거의 없는 경우 
2. 비슷한 영역의 포지션을 하나의 포지션으로 합쳐서 데이터 수 늘리기
3. NULL 값 들어간 데이터 삭제 → .dropna() 사용
4. 훈련set, 시험set 나누기


![image](https://user-images.githubusercontent.com/52282493/105818677-8acbb200-5ffa-11eb-914e-b88e0ba68094.png)
