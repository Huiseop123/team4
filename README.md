# AI_CP1_Project
## **Repository 설명**

- comment_scraping.ipynb → 유튜브 댓글을 수집하는 코드
- data_preprocessing.ipynb → 유튜브 댓글을 전처리하는 코드
- word_cloud.ipynb → 댓글 키워드를 워드크라우드로 표현하는 코드
- all_in_one.ipynb → 위 세가지 코드를 하나로 합친 코드
- [AIB] CP1_4팀(업로드용)
    - 프로젝트를 발표할 때 사용한 PPT 파일을 수정하여 GitHub에서 바로 볼 수 있게 PDF로 수정
    - 아래 내용보다 더 자세하게 설명이 되어 있음.

## **프로젝트에서 풀고자 하는 문제**

- Youtube 동영상에 달린 댓글의 감정, 주요 키워드 등을 재생 목록, 동영상 별로 분석하여 크리에이터가 Youtube 채널을 성장시키는 의사결정에 도움을 주는 분석 결과 제공

## **프로젝트 진행 과정**

- 사전 기획
- 역할 분담
- 데이터 수집 및 전처리 코드 작성
- DL 모델링
- 서비스 구축 및 시연

## **데이터셋 설명**

- 감성 라벨링 데이터
    - AiHub
    - 문장: 38,594
    - 감성(라벨): 7개(행복, 놀람, 분노, 공포, 혐오, 슬픔, 중립)
- 분석에 사용하는 데이터
    - Youtube 댓글
    - 재생목록, 동영상 별로 상이함

## **문제 상황 해결 과정(분석 기법, 모델 등)**

- 분석에 사용할 동영상 댓글 수집
    - 링크를 입력하면 재생목록, 동영상 제목, 조회수, 댓글 내용, 댓글을 단 Youtube ID 등을 수집
- 댓글 전처리 진행
    - 이모티콘 제거
    - 형태소 분석기(Mecab)를 활용한 토큰화 진행
- 다양한 모델 사용
    - RNN 모델 ⇒ 연속형 데이터 처리를 위한 모델, 장기 의존성 문제 존재
    - LSTM 모델 ⇒ RNN의 단점을 해소하기 위한 모델
    - Bi-LSTM 모델 ⇒ 시간 순서대로 입력되는 RNN, LSTM 모델의 한계를 극복하기위한 모델
- FLASK Web api 개발
    - Youtube 동영상 댓글 저장 및 감정 통계 가져오기
    - 저장된 동영상 리스트별 댓글의 감정 통계 가져오기
    - 저장된 동영상 댓글 중 많이 사용된 단어 가져오기
- 데이터베이스 저장
    - Mongodb Atlas: 클라우드로 로컬에 설치할 필요 없이 바로 서버로 활용

## **결과 정리**

- 분석 결과 구현 사진
    - 재생목록 별 감정분포
        - 05학번이즈히어
            
            ![1](https://user-images.githubusercontent.com/88868181/196591716-be560641-7a26-4626-b634-806a750eb76d.png)
            
        - 지금 우리 통화할래?
            
            ![2](https://user-images.githubusercontent.com/88868181/196591736-77350484-eedb-4b35-a744-83a5ade6529b.png)
            
    - 동영상 별 감정분포
        - [05학번이즈히어] 신도시 아재들
            ![3](https://user-images.githubusercontent.com/88868181/196591803-975b970d-16e9-449c-a663-0fd950f17be3.png)

            
            
        - [05학번이즈히어] 신도시 아재는 무엇을 타는가
            ![4](https://user-images.githubusercontent.com/88868181/196591813-a69a91d9-c7b5-4766-85a7-19454612e2c1.png)

            
            
    - 동영상 댓글 중 많이 언급된 단어
        - [05학번이즈히어] 신도시 아재들
            ![5](https://user-images.githubusercontent.com/88868181/196591830-3b16d6e9-e525-4215-9423-e3246112992e.png)

            
            
        - [지금 우리 통화할래?] 술 먹은 다음날 끼부리는 남녀의 전화통화
            ![6](https://user-images.githubusercontent.com/88868181/196591838-67d00fb5-8820-4add-8437-ecdc4d5c42db.png)

            
            

## **한계점 및 해결 방안**

- 대체적으로 댓글 감성의 분포가 크게 차이가 나지 않는다.
    - 학습에 사용한 데이터와 Youtube 댓글의 문체, 단어 등에서 괴리감이 있기 때문이라 추정
    - 직접 크롤링하여 라벨링을 했으면 더욱 좋았을 것이라 생각
- 초기 계획은 사용자가 영상의 url만 입력하면 자동으로 서버에서 댓글 수집, 감성 분석을 하려고 했음.
    - 시간이 부족했고 능숙하지 못했기 때문이라 생각
    - 다양한 프로젝트를 진행하고 고도화 한다면 충분히 해결 가능한 문제라 생각
- Youtube 댓글을 수집할 때 크롤링 방식이라 시간이 많이 걸렸다.
    - Youtube api를 사용하면 해결할 수 있을 것이라 생각.


# team4
CP1 Project source code

https://github.com/123KANGMO/team4

https://github.com/Huiseop123/team4

https://github.com/eastman-ki/team4

https://github.com/djatmdgus/team4
