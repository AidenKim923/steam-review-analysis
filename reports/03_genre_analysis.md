# Step 3: 장르 기반 긍정률 분석

## 분석 개요
게임의 `genres`는 유저가 어떤 유형의 게임을 경험하는지를 나타내는 핵심 지표다.  

이 분석에서는 Steam 데이터의 `genres` 컬럼을 기반으로 장르별 유저의 평균 긍정 반응 비율(positive ratio)을 계산했다.  

## 분석 방법
1. `genres` 컬럼을 `;` 기준으로 분해해 다중 장르를 리스트로 변환
2. 각 장르별로 one-hot encoding 처리
3. `positive_ratio = positive_ratings / (positive_ratings + negative_ratings)` 계산
4. 각 장르에 포함된 게임들의 평균 긍정률을 구함
5. 상위 10개 장르를 시각화
   


## 그래프 및 도표
![](../visuals/top10_genre_positive_review.png)

| Genre | Mean positive ratio |
|-------|---------------------|
| Audio Production | 0.9126 |
| Web Publishing | 0.8638 |
| Design & Illustration | 0.8377 |
| Animation & Modeling | 0.8230 |
| Sexual Content | 0.8150 |
| Utilities | 0.7802 |
| Nudity | 0.7768 |
| Software Training | 0.7716 |
| Education | 0.7716 |
| Video Production | 0.7439 |
| RPG | 0.7427 |
| Indie | 0.7421 |
| Adventure | 0.7400 |
| Game Development | 0.7376 |
| Action | 0.7332 |
| Strategy | 0.7325 |
| Casual | 0.7253 |
| Simulation | 0.7239 |
| Racing | 0.7200 |
| Sports | 0.7116 |
| Free to Play | 0.7095 |
| Early Access | 0.7065 |
| Violent | 0.6809 |
| Gore | 0.6726 |
| Massively Multiplayer | 0.6496 |
| Photo Editing | 0.6251 |

## 결론
- **창작 기반 장르**(Audio, Illustration, Modeling 등)는 강한 유저 만족도를 보인다
- **성인/특수 콘텐츠**도 타깃 유저층에게 높은 만족도를 제공하는 경향
- 대중적인 게임 장르(예: Action, RPG 등)는 상대적으로 긍정률이 낮거나 평균 수준