# 2023-2-PSAT-team-deeplearning
[notion page](https://www.notion.so/d8e330e9fa9f4461b48caeb27d2f5f8f?v=498c78de406e491296467a215f8275a2)

2023년 2학기 통계분석학회 P-SAT 딥러닝팀 주제분석  



## 💻 프로젝트 소개

<예측 기상&발전량을 활용한태양광 발전량 예측>☀️

POSTECH과 H energy가 함께 주최하는 태양광 발전량 예측 대회 - 대학 및 대학원생 대상 제5회 OIBC CHALLENGE

활용 데이터: 예측된 발전량, 예측대상 발전소 실제 발전량, 운량/기온/습도 등을 포함한 13개의 기상데이터, 예측된 발전량에 대한 인센티브(모델평가 점수)
데이터 출처: 주최 측

개발 기간(duration): 23.10.22 ~ 23.11.17


## 🔥 팀 구성 및 역할
- 이정환(팀장): 태양전지 도메인 조사, 파생변수(시간변환/계절변환), LGBM, LSTM, MLP+LGBM 앙상블,RNN+LGBM 앙상블,SCINet
- 김동환: 태양전지 도메인 조사, 시계열 클러스터링, 회귀+LGBM 앙상블,구조적시계열모형
- 권가민: 앙상블, XGB, 상관분석, x변수 클러스터링(오차율/계절), 오차율/발전량 패턴파악(시간별/계절별), 
- 박채원: 앙상블,LGBM, 상관분석, 선형회귀계절, x변수 군집화(오차율/계절), 변수선택(계절)
- 박준영: 앙상블, 상관분석, 선형회귀시간/계절, 유사도예측, x변수 군집화(오차율/계절)

## 🔍 분석 흐름
1. 도메인 조사
2. EDA (모델별 발전량 예측/시간대별 예측량의 분산,평균/계절 별 오차율/상관관계)
3. 변수 선택/모델링 - 성능향상을 위해 다양한 방법 활용
4. 예측 결과 시각화 및 분석/점수 계산


## 📈 공모전 개요
![image](https://github.com/donghwan0318/Solar-Power-Generation-Forecasting-Using-Weather-and-Generation-Data/assets/136334371/3bd9ed50-fe2f-4906-a29d-94f5f97cd2d7)


## 🚨 특수한 발전량 패턴 존재
![image](https://github.com/donghwan0318/Solar-Power-Generation-Forecasting-Using-Weather-and-Generation-Data/assets/136334371/52dfcb34-d0aa-4dc4-9ec5-5242f0898e4f)

일반적으로 정오에 발전량이 최대치를 보이는 커브 형태를 띠지만, 특정한 날에는 그렇지 않을 때가 있음 

💡 해결을 위한 노력들
- 단순 그러한 특수한 패턴을 띄는 날들을 클러스터링,변수선택법 등을 통해 분리하고자 하였음(시계열 클러스터링, 오차율기반 클러스터링, 계절별, 시간별, 변수선택법), 이후 클러스터별 개별 모델링 진행
- 특수한 패턴을 띄는 날들이 과거에 하루는 존재할 것이다 판단하고, 백터 유사도를 이용하여 파생변수를 생성

## 클러스터링
![image](https://github.com/donghwan0318/Solar-Power-Generation-Forecasting-Using-Weather-and-Generation-Data/assets/136334371/7b6276b6-9ab5-4870-8887-1f52989ce87e)
![image](https://github.com/donghwan0318/Solar-Power-Generation-Forecasting-Using-Weather-and-Generation-Data/assets/136334371/22b6b698-1d23-44a5-81aa-cf1717972486)



## 📃 모델링
![image](https://github.com/donghwan0318/Solar-Power-Generation-Forecasting-Using-Weather-and-Generation-Data/assets/136334371/876ba0d6-23e0-405e-a68b-a52a7b07cd3a)
![image](https://github.com/donghwan0318/Solar-Power-Generation-Forecasting-Using-Weather-and-Generation-Data/assets/136334371/9a53886e-e74a-4617-8d93-78962fd65639)
![image](https://github.com/donghwan0318/Solar-Power-Generation-Forecasting-Using-Weather-and-Generation-Data/assets/136334371/3480801a-ef37-4977-8661-0fa8c4b0eb5c)





