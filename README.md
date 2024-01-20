## 배달앱 리뷰 답변 분석 및 생성 서비스

- 배달앱 입점 사장님들을 위한 고객 리뷰 분석 및 자동 답변 서비스 기획 (멀티캠퍼스 Bootcamp Final 프로젝트 최종 우승)
- 팀 프로젝트 repository https://github.com/swoo-nam/BootCamp_project_final
- [발표자료 pdf](https://github.com/piabona/AI-reply-generator-prj/blob/100b9250aeac9d73793436dea4433ee0d8002310/report/%E1%84%8E%E1%85%AC%E1%84%8C%E1%85%A9%E1%86%BC%20%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%8C%E1%85%A6%E1%86%A8%E1%84%90%E1%85%B3%20%E1%84%91%E1%85%A9%E1%84%90%E1%85%B3%E1%84%91%E1%85%A9%E1%86%AF%E1%84%85%E1%85%B5%E1%84%8B%E1%85%A9_1%E1%84%8C%E1%85%A9.pdf) 

## Summary
- 총 2가지 서비스로 분리하여 제공 기획
- 1. 리뷰 분석 서비스 
  - Multi label Classification 문제 : Zero shot 모델
- 2. 
- Streamlit 활용 서비스화

------------------------------

## Service 1. 리뷰 분석 서비스

#### Data Crawling
- 요기요 리뷰 크롤링
#### Data Preprocessing 

#### Model(Pretrained model)
- Random Forest 
#### Ensemble 
- 10Fold, SEED ensemble

#### Visualization 

------------------------------

## Service 2. 답변 생성 서비스 

#### Data Preprocessing 
- 문법적 요소

#### Model(Pretrained model)
- KoGPT Bert기반 다수 모델, LSTM 등
  
#### Ensemble 
- 10Fold, SEED ensemble

#### Visualization 

------------------------------


## Environment
-
- OS: Ubuntu 18.04.4 LTS (GNU/Linux 4.15.0-162-generic x86_64)
- Environment: Anaconda 4.10.3
