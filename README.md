## 배달앱 리뷰 답변 분석 및 생성 서비스 [1st Prize]

- 배달앱 입점 사장님들을 위한 고객 리뷰 분석 및 자동 답변 서비스 기획 
- 기간 : 2023년 8월 ~ 10월 (팀 6인)
- 성과 : 멀티캠퍼스 Bootcamp Final 프로젝트 최종 우승
- 팀 프로젝트 [Repository](https://github.com/swoo-nam/BootCamp_project_final) / [발표자료 pdf](https://github.com/piabona/AI-reply-generator-prj/blob/100b9250aeac9d73793436dea4433ee0d8002310/report/%E1%84%8E%E1%85%AC%E1%84%8C%E1%85%A9%E1%86%BC%20%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%8C%E1%85%A6%E1%86%A8%E1%84%90%E1%85%B3%20%E1%84%91%E1%85%A9%E1%84%90%E1%85%B3%E1%84%91%E1%85%A9%E1%86%AF%E1%84%85%E1%85%B5%E1%84%8B%E1%85%A9_1%E1%84%8C%E1%85%A9.pdf) 

## Summary
- 총 2가지 서비스로 분리하여 제공 기획
- **1. 답변 생성 서비스 (Text Generative AI)** - 고객의 리뷰에 대한 사장님의 자연스러운 답변을 자동 생성
  - **Data Collection** : 배달앱 리뷰 37,140개 크롤링
  - **Preprocessing** : ID, 가게/음식/지점명 masking
  - **Augmentation** : GPT API 활용하여 추출한 부정 데이터로 긍부정 비율 조정
  - **Model** : KoGPT2-base-v2 model fine-tuning 리뷰-답변 학습
  - **Refinement** : 리뷰와의 유사도(cosine, jaccard) 비교 통한 최종 답변 생성 
  - **Presentation** : Streamlit 구현

- **2. 리뷰 분석 서비스 (Text Classification AI)** - 리뷰의 키워드를 분석하여 리뷰가 맛/가격/서비스 중 어떤 카테고리에 속하는지 분류 
  - Data Collection, Preprocessing, Augmentation, Presentation 서비스 1과 동일
  - **Model** : MoritzLauer/mDeBERTa model fine-tuning 멀티라벨 분류 학습 
  - **Refinement** : Fine-tuned 모델 + Zeroshot base 모델 산술평균 앙상블하여 최종 라벨 생성
  - **Extension** : 부가 서비스 기획 (긍부정 지수 추이 / 고객별 온도 지수 등)

## Environment
- AWS / Google colab
- OS: Ubuntu 18.04.4 LTS (GNU/Linux 4.15.0-162-generic x86_64)
- Environment: Anaconda 4.10.3
