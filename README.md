# Physical.GG
[DataContest] Korea BigData-Culture Platform &amp; Korea Sports Promotion Foundation(KSPF)
## 프로젝트 개요

![캡처.PNG](attachment:f56073e8-5aff-4df5-bcbf-3a94811bcfc8:캡처.png)

<aside>
🛠 **한국빅데이터문화플랫폼 & 국민체육진흥공단 주최 데이터 활용 아이디어 공모전**

각 국민체육센터의 **체력측정데이터** 활용
데이터 기반 문제 정의 / 해결 방안 도출 / 데이터 탐색 / 전처리 / 모델설계(분류 & 군집화)\n
**개인 출전** - 홀로 전 과정 진행

</aside>

---

## 세부 진행 내용

- **문제 정의 / 니즈 도출**
    1. 통계청 국가지표체계 「2024 신체활동실천율」, 문화체육관광부 「2023 국민생활체육」
        
        👉 청년층 신체활동 저하 확인
        
    2. 스스로의 건강을 손쉽게 모니터링하는 채널 확보
        
        👉 신체활동 관심 및 접근성 증대 예상
        
    
- **아이디어 : 티어 시스템**
    1. [OP.GG](http://OP.GG) 등 청년층에게 익숙한 ‘티어’(등급) 개념 활용
        
        👉 체력 측정 항목을 바탕으로 ‘피지컬 티어’ feature 도출하기로 결정
        

- **데이터 분석 / 모델링**
    1. 데이터 수집 및 전처리
        
        👉 국민체육진흥공단 ‘체력측정 및 운동처방 종합 데이터’
        
        👉 월별 데이터이지만 record(사람)이 중복되지 않음 - 비시계열 데이터처럼 사용
        
        👉 시각화 기반 EDA + 도메인 탐색으로 이상치 식별
        
    2. 모델링
        
        👉 ‘피지컬 티어’ 예측 모델 : Stacking 모델
        
        - Sub Model
            
            Logistic Regression, Decision Tree, KNN, XGBoost, Light GBM
            
        - Final Model
            
            Random Forest
            
        
        👉 ‘피지컬 타입’ 분류 모델 : KMeans 클러스터링
        
        - K 결정 기준(k=7)
            
            ![image.png](attachment:a825060c-4aa4-467c-b839-945e59ba4204:image.png)
            
        - 군집 양상
            
            ![image.png](attachment:4fc61b99-1904-4213-a29f-8cefc0d876f7:image.png)
            
    
    | **Work** | **Tech Stack** |
    | --- | --- |
    | ✔️ 데이터 병합, 결측치 및 이상치 제거, 추가 열 생성 | pandas |
    | ✔️ 시각화 EDA | seaborn |
    | ✔️ target 예측 모델 생성, GridSearch, 성능평가 | sklearn |
    | ✔️ Physical Type 측정 모델 : 클러스터링 | K-Means |
    

---

## PPT

https://drive.google.com/file/d/1GORUFzM7BGt8DJzeCJixb4PDPxdcvPUL/view?usp=sharing
