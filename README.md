#  데이터로 보는 나의 운동능력(My training ability as driven by data)

<br/>

## 프로젝트 소개

직무 전환을 위해 다양한 데이터를 다루며 포트폴리오를 만들어 보는 과정에서, [부트캠프](https://github.com/siilver94/Stock-data-collection-analysis-and-visualization)와 [공모전](https://github.com/siilver94/Stock-investment-automation) 의 데이터 과제와 [공공 데이터 포털](https://github.com/siilver94/csv-data-analysis)의 데이터를 가지고 여러 분석 과제를 진행해 보았습니다.
또한, [데이콘](https://github.com/siilver94/Customer-Gender-Prediction)과 [캐글](https://github.com/siilver94/Analysis-for-Opening-a-Bakery/tree/main)에서 다양한 데이터를 활용하여 데이터 분석, 모델링, 그리고 머신러닝을 진행했습니다.

이런 경험을 통해 많은 것을 배우고 데이터 분석가로 성장하는 듯하였지만, 주변을 보니 비슷한 프로세스를 따르는 사람이 많다는 것을 깨달았습니다. 그리하여 말 그대로 나만의 프로젝트가 필요함을 느꼈습니다.

이에 따라, 문제를 스스로 정의하여 이에 필요한 데이터를 선정하고 직접 수집하며, 분석 결과를 도출하고 시각화하여 나만의 인사이트를 얻는 것이 가장 값지다 생각했습니다.
이에 맞춰, 저의 취미생활인 운동(헬스)을 접목해 나의 운동 수행 능력을 개선하기 위해 주기적으로 헬스장에서의 웨이트 트레이닝 데이터를 수집하고 분석하며, 나만의 인사이트를 찾는 장기 프로젝트를 시작하기로 했습니다.

<br/>

## 쌓을 데이터 목록

- **날짜** - DateTime
- **몸무게** - Weight(kg)
- **1RM중량** - Squat, Sumo_Deadlift, OHP, Pendlay_Row
- **휴식기간(얼마만에 그 부위를 하는지)** - Rest_Period(day)
- **운동 시간** - Workout_time(오전/오후/저녘 : 0/1/2)
- **운동 시 최대심박수, 평균 심박수**
- **일일 섭취 칼로리**

### 수집 기간

- 벌크업 : 2022-06 ~ 2022-12

- 다이어트 : 2022-12 ~ 2023-05

- 추가 : 2023-08 ~ 2023-11
  
<br/>

## 분석 전 세부 목표

**- 시간별 운동 선호도 분석:** 오전/오후/저녁 중 어떤 시간대에 가장 많이 운동하는지, 그리고 계절이나 월별로 운동하는 시간대가 달라지는지 조사합니다. 예를 들어, 여름과 겨울철에 다른 운동 시간대의 분포가 있는지 확인할 수 있습니다.

**- 운동과 휴식 기간의 관계:** 운동과 휴식 기간의 상관관계를 분석하여, 얼마나 휴식 기간을 가지고 운동을 하고 있는지 확인할 수 있습니다. 더 많은 휴식 기간이 높은 1RM과 연관이 있는지, 또는 그렇지 않은지 알아볼 수 있습니다.

**- 1RM 중량의 분포와 추이:** 1RM 중량의 분포를 히스토그램이나 상자 그림 등을 이용해 시각화하여 살펴봅니다. 또한 시간에 따른 1RM 중량의 변화를 추적하는 추세선을 그려봄으로써 운동 성과의 발전을 확인할 수 있습니다.

**- 날짜와 몸무게의 관계:** 날짜별로 몸무게의 변화를 추적하고, 이를 시계열 그래프로 시각화하여 패턴이나 트렌드를 파악할 수 있습니다.

**- 체중과 운동 시간대의 관계:** 체중과 운동 시간대의 상관관계를 조사하여, 특정 시간대에 운동하는 사람들이 체중 관리를 어떻게 하는지 파악할 수 있습니다.

**- 날짜와 운동 빈도의 관계:** 날짜별 운동 빈도를 파악하고, 특정 날짜에 운동을 더 많이 하는 경향이 있는지 살펴봅니다.

**- 1RM 중량과 운동 시간대의 관계:** 오전/오후/저녁 중 어떤 시간대에 더 높은 1RM 중량을 기록하는지 분석하여, 시간대가 운동 성과에 미치는 영향을 알아볼 수 있습니다.

<br/>

## 분석 결과

#### 1. 몸무게의 중요성

초기 가설대로 1RM 중량은 체중과 밀접한 관계가 있다는 것을 상관계수와 시각화를 통해 검증. 체중 대비 스쿼트 1RM 중량을 바이올린 플롯으로 추가 분석 결과, 체중 대비 1.9kg ~ 2.0kg 구간에서 스쿼트 1RM이 밀집됨을 확인
이를 통해 이 개인의 운동 능력을 최적화하고 개선하기 위해서는 체중 관리에 대한 중요성을 강조하는 운동 계획이 필요하다는 것을 검증.

#### 2. 데드리프트와 스쿼트의 1RM 연관성

히트맵 분석 결과, 스쿼트 1RM 중량은 다른 5대운동들과 강한 양의 상관관계를 보였고 특히 **데드리프트[Sumo_daelift(kg)]** 는 오히려 체중보다도 더 강한 상관관계를 보여 연관성이 더 강하게 나타남. 
초기 가설에는 중량이 가장 밀접하다고 생각하였고 이 새로운 사실을 통해 데드리프트 1RM 증량에 집중할수록 스쿼트와 데드리프트의 1RM 둘 다 서로 좋은 시너지 효과를 볼 수 있다는 새로운 인사이트 발견.

상관계수 : 체중 = 0.88  / 데드리프트 = 0.93

#### 3. 휴식 기간의 새로운 지표

상관분석을 통해 휴식 기간은 1RM 중량과 관련성이 매우 낮음을 확인했지만, 개인적인 경험을 토대로 추가 분석을 진행. 그 결과 4일 휴식은 많은 데이터가 평균치보다 더 높은 중량을 보여줌으로써 이는, 널리 알려진 근육 회복의 **최적 시간(48hr)** 지표보다 두배가 넘는 차이를 보여줬음.
이것은 휴식 기간이 다소 길어지면, 일종의 **"차지 기간"** 으로 볼 수 있어서, 근육 회복과 성능 향상에 긍정적인 영향을 미칠 수 있다는 흥미로운 관찰. 휴식 기간을 효율적으로 조절함으로써 최상의 운동 결과를 얻을 수 있는 전략을 개발하는 데 도움.

#### 4. 벌크업/다이어트 시즌별 1RM 중량 차이

다이어트 시즌 동안, 저녘에 운동하는 것이 벌크업 시즌과는 달리 스쿼트 1RM 중량과 매우 큰 상관관계를 가지고 있다는 흥미로운 결과가 도출.
아침보다 저녘에 운동을 하는 것이 1RM 중량 증가에 미치는 영향이 뚜렷하게 드러났고 **상관계수 또한 벌크업 시즌에 비해 크게 증가(0.079 -> 0.74)** 한 것은 주목할 만한 결과.
이에 더불어 **p-value가 0.0004**로 유의하게 낮게 나왔는데, 이는 결과의 통계적 유의성을 더 강조. 이러한 결과로 보아, 다이어트 시즌 동안 특히 저녘에 운동을 함으로써 스쿼트 1RM을 향상하는 데에 높은 효과가 있음을 시사.


<br/>

  ## 리뷰

17개월이라는 장기간에 걸친 프로젝트를 통해 저는 몸무게와 1RM 중량 사이의 상관관계를 깊이 있게 분석하고자 했습니다. 처음부터 이 두 변수 간의 연관성을 확인하고 싶었습니다.

사실 프로젝트를 시작할 때는 벌크 시즌의 체중 변화로부터 보이는 데이터를 분석하고자 했지만, 다음에 다이어트를 할 때의 분석 결과도 궁금하여서 추가로 다이어트를 진행해 보았고 이 시즌에 데이터를 수집하느라 프로젝트가 연장되었습니다. 데이터 수집을 하는 김에 몸무게와 1RM 중량 외에 상관관계가 있을 수도 있겠다 생각한 다양한 요소를 추가하였습니다. 그리고 그만큼 더 많은 인사이트와 결론을 도출할 수 있었습니다. 이러한 결과를 바탕으로 향후 운동 계획을 최적화하기 위한 실질적인 통찰을 얻고자 했습니다. 


이 프로젝트를 통해 저는 데이터 분석의 핵심적인 요소들을 직접 분석하고 배울 소중한 기회를 가졌습니다. 제가 진행한 여러 가지 분석 중 가장 주목할 만한 부분은 운동과 휴식 기간, 그리고 1RM 중량 사이의 상관관계를 분석한 부분입니다. 이를 통해 제가 어떻게 데이터를 활용하여 운동 성과를 향상하는 데 도움을 줄 수 있는 인사이트를 도출할 수 있는지를 명확히 확인할 수 있었습니다.

또한, 저의 경험을 통해 데이터의 질과 중요성을 다시 한번 느낄 수 있었습니다. 데이터의 일관성과 신뢰성은 분석의 결과를 신뢰할 수 있는지에 결정적인 영향을 미칩니다. 따라서 데이터 수집부터 분석, 시각화까지의 과정에서 데이터의 품질을 유지하는 것이 얼마나 중요한지를 몸소 체감할 수 있었습니다.

또한, 시각화를 통해 데이터의 패턴과 트렌드를 더 명확하게 파악할 수 있었으며, 이를 통해 인사이트를 도출하는 것이 얼마나 중요한지를 깨달을 수 있었습니다.

마지막으로, 이 프로젝트를 통해 데이터 분석의 지속적인 공부와 학습의 필요성을 다시 한번 느낄 수 있었습니다. 데이터 분석의 분야는 빠르게 변화하고 발전하고 있으며, 새로운 도구와 기술이 끊임없이 출시되고 있습니다. 따라서, 저는 항상 새로운 도전에 대한 열린 마음을 가지고 지속적인 학습과 자기 계발을 통해 더 나은 데이터 분석가로 성장해 나가겠다는 것을 다시 한번 다짐해 보았습니다.

이 프로젝트를 통해 저는 데이터의 힘을 최대한 활용하여 실제 문제를 해결하고 개인적인 목표를 달성하는 데에 어떻게 기여할 수 있는지에 대한 자신감을 키울 수 있었습니다. 이러한 경험과 깨달음을 바탕으로 더 나은 데이터 분석가로 성장해 나가겠습니다.
