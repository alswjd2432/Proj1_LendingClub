# LendingClub 데이터를 이용한 부도확률 예측 및 이익 최대화
## 목표 : 이익 최대화 및 손실 최소화를 위한 대출 승인 여부 결정
### 데이터 : LendingClub(P2P 대출 업체)에서 제공하는 대출 승인자의 정보 데이터

### 부도 확률 예측 모델
모델 1. Lasso로 최적 변수 추출 후 LogisticRegression 이용해 부도 확률 예측 (model_Lasso_logistic.ipynb) /n
모델 2. Elastic으로 최적 변수 추출 후 LogisticRegression 이용해 부도 확률 예측 (model_Elastic_logistic.ipynb) /n
모델 3. LogisticRegression (model_Logistic.ipynb) /n
모델 4. DecisionTreeClassifier (model_Decision_Tree.ipynb) /n
모델 5. RandomForestClassifier (model_RandomForest.ipynb) /n

### 결론 1. Cost 함수를 0.83*FN + 0.17*FP 설정했을 때, 이익과 손실이 최적화된다.
복잡한 이익 함수와 손실 함수를 쓰지 않아도, 최적의 Cost 함수를 통해 적절한 optimal threshold를 구성할 수 있다.
(이익 함수와 손실 함수에 사용되는 사전변수의 영향 없이 Cost 함수 구성 가능)

### 결론 2. LogisticRegression(모델3)을 적용, optimal threshold를 0.177로 설정했을 때 이익이 최대화 되었다.
초기 전체 데이터에서 계산한 이익의 1.368배로 이익을 증가시킴

### 결론 3. LogisticRegression(모델3)을 적용, optimal threshold를 0.15로 설정했을 때 손실이 최소화 되었다.
초기 전체 데이터에서 계산한 손실의 0.9261배로 손실을 감소시킴


### 추가 사항
모델을 새로운 데이터에 적용하기 (OutOfSample_Logistic.ipynb)
결론에 등장한 모델을 적용했을때, 이익과 손실이 모두 기존보다 최적화되는 것을 확인 가능

### 자세한 사항은 아래 PPT로
[Lending Club.pdf](https://github.com/alswjd2432/desktop-tutorial/files/11948506/Lending.Club.pdf)
