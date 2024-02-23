#  데이터가 가르쳐주는 파워업 플랜

<br/>

## 프로젝트 소개

데이터 분석 역량을 키우기 위해 [부트캠프](https://github.com/siilver94/Stock-data-collection-analysis-and-visualization)와 [공모전](https://github.com/siilver94/Stock-investment-automation) 의 데이터 과제와 [공공 데이터 포털](https://github.com/siilver94/csv-data-analysis)에서 여러 분석 과제를 진행해 보았습니다.
또한, [데이콘](https://github.com/siilver94/Customer-Gender-Prediction)과 [캐글](https://github.com/siilver94/Analysis-for-Opening-a-Bakery/tree/main)에서 다양한 데이터를 활용하여 데이터 분석 및 기계학습을 진행 해 보았습니다.

이런 경험을 통해 많은 것을 배웠지만 비슷한 프로세스를 따르는 사람이 많다는 것을 깨달았고 나만의 개성 있는 프로젝트의 필요함을 느꼈습니다.

<br/>

**[관심사를 통한 A to Z 데이터 분석]**

이리하여 저와 가장 가까운 생활권의 지표를 분석하고자 해당 프로젝트를 기획하게 되었습니다.

저는 평소 헬스를 매우 좋아했고 운동 종목 중 스쿼트에 진심이었습니다. 저는 더 무거운 중량을 들기 위해 많은 정보를 찾아보고 다양한 시도를 해 보았습니다. 하지만 찾은 수많은 정보들이 일치 하지 않는 경우도 많았고, 실제로 운동을 할 때 예상보다 수월하게 무게를 들었고, 때로는 컨디션이 좋았지만 원하는 결과를 얻지 못한 적도 있었습니다.

위와 같은 경험의 원인을 찾고 저의 스쿼트 중량을 증대시키기 위해 요소들을 직접 선정/수집 및 분석하여 스쿼트 *1RM 증량의 핵심 인사이트를 도출하였습니다.
*1RM : 1회 들 수 있는 최대 중량



<br/>

## 쌓을 데이터 목록

- **날짜** - DateTime
- **몸무게** - Weight(kg)
- **1RM중량** - Squat, Sumo_Deadlift, OHP, Pendlay_Row
- **휴식기간(얼마만에 그 부위를 하는지)** - Rest_Period(day)
- **운동 시간** - Workout_time(오전/오후/저녘 : 0/1/2)
- **운동 시 최대심박수, 평균 심박수**
- **일일 섭취 칼로리**

  
<br/>


### 수집 기간

**- 벌크업 :** 2022-06 ~ 2022-12

**- 다이어트 :** 2022-12 ~ 2023-05

**- 추가 :** 2023-08 ~ 2023-11
  
<br/>

## 분석 전 가설

1. 체중을 증량하면 1RM도 증량될까?
 
2. 어떤 요소들이 1RM에 영향을 미칠까?
  
3. 최적의 휴식 기간은 얼마일까?
   
4. 운동 시간이 1RM에 영향이 있을까?
   

<br/>

## 분석 결과

#### 1. 체중의 중요성 검증

초기 가설대로 체중과 1RM의 강한 연관성 확인하였습니다. 특히 바이올린 플롯으로 밀집도를 시각화해 본 결과 1.9kg~2.0kg의 구간에 1RM이 밀집되어 있음을 확인할 수 있었습니다.
이로써 **1RM 증량을 위해 체중 관리의 중요성을 검증하였습니다.**

#### 2. 체중보다 중요한 요소 발견

히트맵 분석 결과, 스쿼트 1RM 중량은 다른 5대운동들과 강한 양의 상관관계를 보였고 특히 **데드리프트[Sumo_daelift(kg)]** 는 오히려 체중보다도 더 강한 상관관계를 보여 연관성이 더 강하게 나타났습니다.
초기 가설에는 체중이 가장 밀접하다고 생각하였고 이 새로운 사실을 통해 **데드리프트의 1RM 증량에 집중할수록 스쿼트와 데드리프트의 1RM 둘 다 서로 좋은 시너지 효과를 볼 수 있다**는 새로운 인사이트 발견했습니다.

상관계수 : 체중 = 0.88  / 데드리프트 = 0.93

#### 3. 휴식 기간의 새로운 지표

상관분석을 통해 휴식 기간은 1RM 중량과 관련성이 매우 낮음을 확인했지만, 개인적인 경험을 토대로 추가 분석을 진행했습니다. 그 결과 4일 휴식은 많은 데이터가 평균치보다 더 높은 중량을 보여줌으로써 이는, 널리 알려진 근육 회복의 **최적 시간(48hr)** 지표보다 두 배가 넘는 차이를 보여줬습니다.
이것은 휴식 기간이 다소 길어지면, 일종의 **"차지 기간"** 으로 볼 수 있어서, 근육 회복과 성능 향상에 긍정적인 영향을 미칠 수 있다는 흥미로운 관찰이었습니다. 결론적으로 **근육 회복의 최적시간(48hr)의 두 배 이상을 쉬어야 1RM 증량에 효과적임을 검증. 휴식 기간을 효율적으로 조절함으로써 최상의 운동 결과를 얻을 수 있는 전략을 개발하는 데 도움을 줍니다.**

#### 4. 시즌별 운동시간의 차이

다이어트 시즌 동안, 저녘에 운동하는 것이 벌크업 시즌과는 달리 스쿼트 1RM 중량과 매우 큰 상관관계를 가지고 있다는 흥미로운 결과가 도출되었습니다.
아침보다 저녘에 운동을 하는 것이 1RM 중량 증가에 미치는 영향이 뚜렷하게 드러났고 이러한 결과로 보아, **다이어트 시즌 동안 특히 저녘에 운동을 함으로써 스쿼트 1RM을 향상하는 데에 높은 효과가 있음을 검증하였습니다.**


<br/>

## 리뷰

이 프로젝트를 계획하는 과정에서 문제를 명확하게 정의하고 필요한 데이터를 선별하는 데에 어려움을 겪었습니다. 하지만, 운동능력 지표를 정량적 수치로써 스쿼트 1RM을 선택하여 문제 해결에 중요한 첫걸음을 내딛었습니다.

프로젝트 초기 단계에서는 목표를 달성하기 위한 변수를 설정하는 과정에서 다양한 정보를 찾아본 후, 이를 선별하여 활용했습니다. 상관분석을 통해 불필요한 변수를 걸러내는 등의 시도를 거쳐, 문제 해결을 위한 데이터 준비를 완료했습니다.

프로젝트는 단기적인 목표로 시작했지만, 분석의 욕심으로 인해 V1부터 V3까지 총 17개월이라는 긴 기간 동안 진행되었습니다. 각 버전에서는 체중을 증량하는 V1, 그리고 체중을 감량했을 때의 데이터 변화를 추적하기 위한 V2, 그리고 체중 외의 새로운 지표를 얻기 위한 V3까지 진행하며 데이터의 다양한 측면을 고려하여 결과를 분석했습니다.

흥미로운 부분 중 하나는 휴식기간과의 관련성을 분석할 때였습니다. 초기 상관분석에서는 통계적으로 유의미한 결과를 얻지 못했지만, 개인적 경험과 추가적인 시각화를 통해 숨겨진 흥미로운 인사이트를 발견할 수 있었습니다. 이 것은 널리 알려진 최적의 근육회복 시간(48hr)의 두배 이상을 쉬어야 1RM 증량에 효과적인 것을 검증해 보았습니다.

이 프로젝트를 통해 데이터의 힘을 최대한 활용하여 실제 문제를 해결하고 개인적인 목표를 달성하는 방법에 대한 자신감을 키웠습니다. 이러한 경험과 깨달음을 토대로, 미래에는 보다 나은 데이터 분석가로 성장해 나아가겠습니다.
