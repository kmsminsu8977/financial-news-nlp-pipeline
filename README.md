# Financial News NLP Pipeline

금융 뉴스 NLP 파이프라인 프로젝트의 기본 연구 구조와 재현 가능한 baseline 산출물을 담은 저장소입니다.

**핵심 연구 질문**

> 뉴스 텍스트를 매매나 리스크 분석에 쓰려면 어떤 전처리 산출물이 먼저 필요한가?

## 저장소 구조

```text
financial-news-nlp-pipeline/
├── src/                         # baseline 계산 로직과 실행 엔트리포인트
├── data/sample/                 # 합성 샘플 입력 데이터
├── docs/                        # 방법론과 해석 기준
├── notebooks/                   # 실행 흐름을 보여주는 최소 노트북
├── outputs/tables/              # 재현 가능한 결과 CSV
├── presentation/                # 발표/보고서 초안
└── references/                  # 재작성 개념 노트와 참고문헌 메모
```

## 빠른 시작

```bash
python -m src.run_baseline
```

실행 결과는 `outputs/tables/baseline_results.csv`에 저장됩니다.

## 구현 범위

- headline과 summary를 소문자 토큰으로 정리하고 불용기호를 제거한다.
- 작은 금융 감성 lexicon으로 긍정/부정 단어 수와 label을 계산한다.
- 기사 문장은 감성 분류 흐름이 드러나도록 작성했다.

## 주요 파일

- `src/news_nlp_baseline.py`: 금융 뉴스 텍스트를 정제하고 간단한 감성 점수와 토큰 통계를 산출한다.
- `data/sample/news_articles.csv`: baseline 실행용 합성 입력값
- `docs/methodology.md`: 계산 절차, 입력/출력 정의, 해석상 주의점
- `outputs/tables/baseline_results.csv`: 현재 baseline 산출물

## 다음 확장 방향

- 실제 공개 데이터 또는 별도 수집 데이터 연결
- notebook 기반 탐색 분석 추가
- 차트와 표를 포함한 최종 보고서 작성
- 모델 검증, 민감도 분석, 비용/리스크 가정 보강
