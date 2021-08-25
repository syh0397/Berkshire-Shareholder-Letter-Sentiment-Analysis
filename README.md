# Berkshire-Shareholder-Letter-Sentiment-Analysis


## Bert fine_tunning with app review dataset
![002](https://user-images.githubusercontent.com/75018963/116491992-2577ad80-a8d6-11eb-94ae-449043868574.png)


### 📌 프로젝트 목적

1. 개인적으로 주식을 하면서 워렌버핏의 저서 및 버크셔 헤서웨이의 연례 주주서한을 통해 많은 도움을 받았습니다.
2. 점점 증가하는 주린이 (주식을 처음하는 사람들)들 위해서 주식에 도움이 될만한 버크셔헤서웨이의 주주서한을 요약해주고
3. fine_tunning된 Bert model 을 이용하여 감성분석을 진행해 주린이들에게 도움이 되고자 했습니다. 

### 🚩 가설

1. Transformer library 를 이용해서 텍스트를 압축했을때 경제 용어 및 어려운 용어가 들어간 주주서한 글도 잘 압축이 될까?
2. app review dataset과 같은 전혀 다른 분야의 데이터로 전이학습을 시켜도, 경제용어와 같은 전문적인 단어가 들어간 글을 감성분석 할 수 있을까?
3. 실제로 글을 해석함에 있어서 도움이 될 것인가? 

### 📌 사용한 데이터

1. app review dataset
2. 2021 Berkshire-Shareholder-Letter for stock owners
