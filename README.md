# AI_X_DEEPLEARNING

### Title: LapTop Price Prediction 

### Members: 
          권범수, 컴퓨터학부
          정민호, 컴퓨터학부


## Index
####           I. Proposal
####           II. Datasets
####           III. Methodology
####           IV. Evaluation & Analysis
####           V. Related Works
####           VI. Conclusion: Discussion

## I. Proposal
+ Motivation
  현대 사회에서 노트북이 중요한 역할을 맡고 있으며, 많은 사람들이 노트북을 구매하고자 하는데에 있어서 예상 가격에 대한 정보는 중요한 역할을 합니다. 노트북은 일상 생활과 업무에 필수적인 도구로 사용되고 있으며, 개인용이나 업무용으로 사용되는 등 다양한 용도로 사용됩니다. 그러나 노트북 가격은 여러 요인에 의해 변동될 수 있기 때문에, 사람들은 구매 전에 가격에 대한 예측 정보를 얻기 위해 많은 노력을 기울입니다. 그래서 저희는 노트북 데이터를 이용하여 노트북 가격을 예측하는 모델을 주제로 선정하게 되었습니다.
+ What do you want to see at the end?
  Linear regression를 통해 데이터를 학습시켜 노트북 가격을 예측하는 모델을 만들어 소비자들에게 구매 결정에 도움이 되고싶습니다.

## II. Datasets
+ https://www.kaggle.com/datasets/kuchhbhi/latest-laptop-price-list
+ 노트북과 관련된 데이터셋입니다. 이 데이터셋을 이용하여 노트북의 가격을 예측하는 모델을 학습시킬 예정입니다.
+ 학습 데이터는 kaggle의 Datasets을 사용할 예정이며 두 개의 csv 파일이 주어지지만 Column의 종류가 달라 더 많은 정보를 제공하는 Cleaned_Laptop_data.csv를 사용할 예정입니다. 각 csv 파일은 23개의 Column으로 구성되어있습니다. 각각의 Column에 대한 정보는 다음과 같습니다.

          brand             : 노트북의 브랜드
          model             : 모델명
          processor_brand   : 프로세서의 브랜드
          processor_name    : 프로세서의 세부 모델명
          processor_gnrtn   : 프로세서의 세대
          ram_gb            : 램 용량(GB)
          ram_type          : 램 타입
          ssd               : SSD 용량(GB)
          hdd               : HDD 용량(GB)
          os                : 운영체제
          os_bit            : 운영체제 비트수
          graphic_card_gb   : 그래픽카드 용량(GB)
          weight            : Casual or thinNlight
          display_size      : 화면 크기(inch)
          warranty          : 보증기간(년)
          Touchscreen       : 터치스크린 유무
          msoffice          : MS Office 소프트웨어 유무
          latest_price      : 최신 가격($)
          old_price         : 정가($)
          discount          : 할인율(%)
          star_rating       : 평점(5점 만점)
          ratings           : 평점 수
          reviews           : 리뷰 수
          
         
## III. Methodology
본 문제는 가격을 예측하는 회귀 문제입니다.
+ 단순 선형 회귀 분석 :
y = wx + b 와 같은 수식은 단순 선형 회귀의 수식입니다. 독립 변수x와 곱해지는 값 w를 가중치라고 하고 더해지는 값 b를 편향이라고 합니다. 각각 직선의 기울기와 절편을 의미합니다. 하지만 이러한 단순 선형 회귀 분석으로는 여러 값들을 반영하여 학습을 할 수 없습니다.
+ 다중 선형 회귀 분석 :
다중 선형 회귀 분석은 단순 선형 회귀 분석과 여러개의 가중치와 독립 변수를 가지고 있습니다. 그렇기 때문에 여러 값들을 반영할 수 있습니다. 

이와 같은 이유로 다중 선형 회귀 분석을 이용하여 노트북 가격 예측 모델을 만들기로 하였습니다. 본 문제에서 종속변수로 설정할 수 있는 변수는 old_price와 latest_price가 있는데, 노트북의 가격은 수시로 변동되므로 초기 출시가를 기준으로 삼기 위해 old_price를 종속 변수로 설정하고 latest_price는 삭제하였습니다. 독립변수는 나머지 21개의 변수가 됩니다.

우선 독립변수와 종속변수를 구분해준 뒤 종속 변수의 값이 0인 열을 삭제했습니다. 그리고 회귀 분석에 이용되는 값들은 전부 실수여야하기 때문에 독립변수를 수치형과 범주형으로 구분하였습니다. 이를 위해 실제로는 수치형이지만 단위 문자열이 포함되어 저장되어 있는 값들인 ram_gb, ssd, hdd, processor_gnrtn 등을 단위 문자열을 제거하여 수치형으로 형변환을 시켜주었습니다. 또한 수치형이지만 값을 몰라 'Missing'이라는 문자열로 저장되어 있는 column들 또한 해당 데이터를 데이터의 평균치로 치환하여 수치형으로 변경해주었습니다. 그리고 범주형 변수는 one-hot encoding 시켜주었습니다.

## IV. Evaluation & Analysis
  source 참조.
## V. Related Works
+ Tools, libraries, blogs, or any documentation that you have used to do this project.
  https://wikidocs.net/21670
  https://datascienceschool.net/03%20machine%20learning/04.02%20%EC%84%A0%ED%98%95%ED%9A%8C%EA%B7%80%EB%B6%84%EC%84%9D%EC%9D%98%20%EA%B8%B0%EC%B4%88.html
  https://pandas.pydata.org/docs/
  https://scikit-learn.org/stable/user_guide.html
  
  
+ DataSet : https://www.kaggle.com/datasets/kuchhbhi/latest-laptop-price-list
## VI. Conclusion: Discussion
+ Train 데이터와 Test 데이터의 비율은 8대2로 설정했습니다. 80%의 데이터로 다중 선형 회귀 모델을 학습시킨 뒤 20%의 데이터로 성능 지표를 확인했습니다. 
+ 평가 지표는 MAE로 선정하였습니다. MAE는 회귀 모델의 예측 정확도를 평가하는 지표로 예측값과 실제값의 차이에 절댓값을 씌운 뒤 평균을 구하는 과정으로 구성되어 있으며 이상치에 민감하지 않다는 특징이 있습니다. 
+ Test 데이터의 예측값 중 소수가 다른 값과 약 100,000배 가량 차이나는 것을 확인할 수 있었는데 이는 해당 데이터의 결측치 문제로 인해 이상치가 생긴 것으로 판단하여 제거하였습니다.
+ MAE는 약 98로, 종속변수의 대부분이 30,000과 60,000 사이에 분포해있다는 것을 고려하면 매우 준수한 수치임을 알 수 있습니다. 본 문제의 데이터가 정형 데이터이고 변수의 수가 많지 않기 때문에 단순한 모델을 사용했고, 과적합이 일어나지 않은 것으로 판단됩니다. 해당 모델을 참고하여 소비자들이 노트북을 구매할 때 선명한 소비를 할 수 있으면 좋겠습니다. 

## Youtube Link : https://www.youtube.com/watch?v=kTGUYVGqUkQ

### 권범수: Data Preprocessing, Blog Processing, Youtube Recording
### 정민호: Data Preprocessing, Code Implementation
          
