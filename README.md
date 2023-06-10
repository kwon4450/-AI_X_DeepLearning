# AI_X_DEEPLEARNING

### Title: LapTop ㅖrediction 

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
+ 단순 선형 회귀 분석
y = wx + b 와 같은 수식은 단순 선형 회귀의 수식입니다. 독립 변수x와 곱해지는 값 w를 가중치라고 하고 더해지는 값 b를 편향이라고 합니다. 각각 직선의 기울기와 절편을 의미합니다. 하지만 이러한 단순 선형 회귀 분석으로는 여러 값들을 반영하여 학습을 할 수 없습니다.
+ 다중 선형 회귀 분석
다중 선형 회귀 분석은 단순 선형 회귀 분석과 여러개의 가중치와 독립 변수를 가지고 있습니다. 그렇기 때문에 여러 값들을 반영할 수 있습니다.

이와 같은 이유로 다중 선형 회귀 분석을 이용하여 노트북 가격 예측 모델을 만들기로 하였습니다.

우선 회귀 분석에 이용되는 값들은 전부 실수여야하기 때문에 데이터 셋을 수치형과 범주형으로 구부하였습니다. 이를 위해 실제로는 수치형이지만 단위 문자열이 포함되어 저장되어 있는 값들인 ram_gb, ssd, hdd, processor_gnrtn 등을 단위 문자열을 제거하여 수치형으로 형변환을 시켜주었습니다. 또한 수치형이지만 값을 몰라 'Missing'이라는 문자열로 저장되어 있는 column들 또한 해당 데이터를 데이터의 평균치로 치환하여 수치형으로 변경해주었습니다.

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

### 권범수: Data Preprocessing, Blog Processing
### 정민호: Data Preprocessing, Code Implementation
          
