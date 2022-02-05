# Berkshire-Shareholder-Letter-Sentiment-Analysis

## Bert fine_tuning with app review dataset

#### By using app review dataset, Fine tuning Bert and applied it to Berkshire Hathaway's letters for share-holder and performed sentiment analysis.

- (BERT: Pre-training of Deep Bidirectional Transformers)

  - [BERT_24 May 2019](https://github.com/syh0397/Berkshire-Shareholder-Letter-Sentiment-Analysis/files/7808837/1810.04805.pdf)

```
As a result, the pre-trained BERT model can be fine-tuned 
with just one additional output layer to create state-of-the-art models 
for a wide range of tasks, such as question answering and language inference, 
without substantial task-specific architecture modifications.
```

![002](https://user-images.githubusercontent.com/75018963/116491992-2577ad80-a8d6-11eb-94ae-449043868574.png)

### 📌 프로젝트 목적

1. 개인적으로 주식을 하면서 워렌버핏의 저서 및 버크셔 헤서웨이의 연례 주주서한을 통해 많은 도움을 받았습니다.
2. 점점 증가하는 주린이 (주식을 처음하는 사람들)들 위해서 주식에 도움이 될만한 버크셔헤서웨이의 주주서한을 요약해주고
3. fine_tunning된 Bert model 을 이용하여 감성분석을 진행해 주린이들에게 도움이 되고자 했습니다.

### 🚩 가설

1. Transformer library 를 이용해서 텍스트를 압축했을때 경제 용어 및 어려운 용어가 들어간 주주서한 글도 잘 압축이 될까?
2. app review dataset과 같은 전혀 다른 분야의 데이터로 전이학습을 시켜도, 경제용어와 같은 전문적인 단어가 들어간 글을 감성분석 할 수 있을까?
3. 실제로 글을 해석함에 있어서 도움이 될 것인가?


### 🚩 Bert 모델 설명 및 프로젝트 설명




![BERT Explained: State of the art language model for NLP | by Rani Horev |  Towards Data Science](https://miro.medium.com/max/876/0*ViwaI3Vvbnd-CJSQ.png)

### 📌 폴더 설명

#### Data 

- (Unlabeled) 2021_Letter_for_stock_owner.xlsx
  - 2021년의 버크셔 헤서웨이 주주서한 데이터(2021 Berkshire-Shareholder-Letter for stock owners)를 116 rows 로 나누어 담았습니다.
- (Labeled) 2021_Letter_for_stock_owner.xlsx
  - 2021년의 버크셔 헤서웨이 주주서한 데이터를 라벨링 한 결과입니다.
  - postive, neutral, negative 3가지의 결과로 분류했습니다.
- reviews.csv
  - App review dataset입니다.

#### Practice 

- Cosine 유사도를 활용한 금융 단어 추천시스템 개발 및 금융 서비스와 관련된 다양한 연습을 진행 했습니다.
  - 데이터는 한국은행 경제 용어를 참고 했습니다.
  - https://www.bok.or.kr/portal/bbs/B0000249/view.do?nttId=235017&menuNo=200765
- AWS_practice
  - AWS s3를 사용해보기 위해 연습했습니다. (무료에서는 Pandas를 사용하기 힘듦)
- Convert_line
  - 버크셔 헤서웨이와 아마존의 주주서한을 필요한 만큼 한줄씩 자동으로 나누는 코드를 작성해보기 위해 연습했습니다. 결과적으로 단어로 쪼개지는 경우가 생겨서, 일단 한줄씩 수동으로 옮겼습니다.

### Preprocessing

- Summarization_2021_Warren Buffett's' annual letter.ipynb

  - transfomer library의 summarization을 활용해서 요약했습니다.
    - 1Sample 확인 결과 557 -> 240문장, 내용 또한 매우 잘 요약되었습니다.
