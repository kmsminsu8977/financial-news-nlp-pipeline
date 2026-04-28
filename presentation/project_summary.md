# 발표 초안

## 1. 문제 정의

뉴스 텍스트를 매매나 리스크 분석에 쓰려면 어떤 전처리 산출물이 먼저 필요한가?

## 2. 데이터와 가정

- 합성 샘플 데이터: `data/sample/news_articles.csv`
- 재현 가능한 baseline 실행을 우선 구성

## 3. 방법

금융 뉴스 텍스트를 정제하고 간단한 감성 점수와 토큰 통계를 산출한다.

## 4. 현재 산출물

- 실행 스크립트: `python -m src.run_baseline`
- 결과 표: `outputs/tables/baseline_results.csv`

## 5. 후속 작업

- 실제 데이터 연결
- 민감도 분석
- 차트/보고서 산출
- 프로젝트별 상세 검증
