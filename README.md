# 모바일 서비스 데이터 분석 방법론 & 용어 정리
#### 1. LTV(Life Time Value), CLV(Customer Lifetime Value) : 고객 생애 가치
##### 정의  
- 개별 고객이 창출하는 비즈니스 가치
- 고객 관계가 수익성이 있는지 판별하는 데 사용 -> 고객 확보, 참여, 유지에 비용을 얼마나 투자할 것이지 결정

##### 계산  
LTV = (평균 구매 금액 * 총 마진 * 구매 빈도 * 고객 수명) - 고객 획득 비용  
- 평균 구매금액(Average Purchase Value, APV): 고객의 거래당 평균 구매 금액
- 평균 총 마진: (총 매출 - 매출 원가) / 총 수익
- 구매 빈도: 기간 동안 고객 1명의 평균 거래 수
- 고객 수명: 고객 관계가 유지되는 기간
- 고객 확보 비용(Customer Acquisition Cost, CAC): 고객 1명을 확보하기 위해 지출한 모든 비용(마케팅, 광고 etc)
- ex) 월간 구독료 10달러, 평균 총 마진 70%, 고객 수명은 5년, 고객 확보 비용은 20달러 <br> => (10 & 0.7 * 12 * 5) - 20 = $400

[참고url](https://mixpanel.com/ko/resources/how-to-calculate-lifetime-value/)

  
  
#### 2. KPI(Key Performance Indicator): 핵심 성과 지표
##### 정의
- 성과를 객관적으로 평가하는 기준 中 결정적인 요소

##### 효과
- 부서 전체가 하나의 목표를 향해 움직일 수 있다
- 우선순위가 명확하게 정할 수 있다
- 조직 내의 개개인의 성취도를 객관적이고 투명하게 평가할 수 있는 기준이 된다

##### 유형
- 투입 KPI: 예산, 인력 및 물자를 규모와 계획에 맞춰 적절하게 집행했는지
- 과정/활동 KPI: 성과 도출을 위해 특정 절차의 효율성, 생산성, 품질, 일관성을 측정
- 산출 KPI: 진행 과정에서 무엇을 생산했는지, 얼마나 많은 일을 했는지
- 결과 KPI: 궁극적으로 이룬 성과나 조직에 미친 영향력을 평가  

[참고url](https://www.tableau.com/ko-kr/learn/articles/types-and-examples-of-kpis)
  
  
  
#### 3. Cohort Analysis : 코호트(동질 집단) 분석
##### 정의
- 공통적인 특성을 지닌 사용자를 그룹으로 묶은 후, 각 그룹에 대한 특정 KPI를 다양한 기간에 걸쳐 측정 및 분석하는 방법
- 기간/속성/관심사 등의 여러 카테고리에서 공통의 특성을 갖는 유저를 찾는 방법
- 데이터를 압축하고 한 눈에 확인하기 위해 만드는 피벗과 비슷한 방법론
- 목적: 비즈니스 인사이트를 얻는 것 (분석 후 action, action 후 분석 등)
##### 예시
- 1,2,3월에 가입한 회원들의 집합 -> 가입 Month를 기준으로한 코호트 집단  
=> 가입일을 기준으로 한 집단들의 Retention(재구매, 재방문) 분석 => 코호트 분석
- 최근에는 "코호트 분석 == 유저 행동 데이터 분석"

[참고 url](https://alex-blog.tistory.com/entry/pythoncohort)
  
  
  
#### 4. Funnel(퍼널) : 고객의 서비스 내에서의 이동 (여정)
##### 정의
- 목적: 고객의 여정 상에서 문제점을 발견하는 것
- 전형적인 퍼널은 AIDA 모델:
    - Awareness: 고객이 서비스를 인지하고 관심을 가졌을 때
    - Interest: 고객이 의미 있는 방법으로 서비스 이용을 시작했을 때
    - Desire: 고객이 서비스의 가치를 실감하고 전환 의욕을 가졌을 때
    - Action: 사용자가 전환되었을 때
  
  
  
#### 5. AARRR : 
##### 정의
- Acquisition(유입): 처음 서비스를 경험하게 되는 루트
    - DAU(Daily Active Users): 하루 동안 해당 서비스를 이용한 순수 이용자 수
    - MAU(Daily Active Users): 한달 동안 해당 서비스를 이용한 순수 이용자 수
    - New User: 신규 가입 회원 수
    
- Activation(활동): 고객에게 좋은 반응을 보이는가 확인하는 단계
    - Bounce Rate(이탈률): 바로 나가는 경우의 비율
    - PV(Page View): 특정 서비스에 방문하여 둘러 본 페이지 수
    - avg.PV: 한 유저가 평균적으로 둘러 본 페이지 수
    - DT(Duration Time): 특정 서비스에 접속하여 머물다가 떠날 때까지의 시간
    - avg.DT: 한 유저가 평균적으로 서비스에 머물다가 간 시간
    
- Retention : 서비스를 '다시' 사용하는가 측정하는 단계
    - Retention Rate: 재구매 or 재방문 (업종의 특성에 따라 다름)

- Referral(추천): 자발적으로 다른 사람에게 '추천'하는지 확인
    - SNS Share Rate, 사용자 언급 댓글 수
    
- Revenue(매출): 이러한 활동들이 '매출'로 이어지는지 확인
    - ATV(Average Transaction Value): 한 건당 사용금액
    - IPT(Item Per Transaction): 한 건당 구매 아이템 수
    
[참조url](https://alex-blog.tistory.com/entry/Funnel-%EB%B6%84%EC%84%9D-%EA%B7%B8%EB%A1%9C%EC%8A%A4-%ED%95%B4%ED%82%B9-AARRR?category=891945)
  
  
  
#### 6. 기타 용어
- Reach(도달률): 최소 1회 이상 광고가 노출된 타겟 유저의 비율
- Lead(리드): 잠재고객
- Fill Rate(필레이트): F/R, 광고 요청 대비 실제 노출한 광고 비율
 
