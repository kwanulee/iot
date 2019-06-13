<style>
div.polaroid {
  	width: 400px;
  	box-shadow: 0 10px 30px 0 rgba(0, 0, 0, 0.2), 0 16px 30px 0 rgba(0, 0, 0, 0.19);
  	text-align: center;
	margin-bottom: 0.5cm;
}
</style>

# 사물인터넷과 빅데이터 및 인공지능 융합기술

## 학습 목표
- 사물인터넷과 빅데이터 및 인공지능 융합기술의 개념 상호 관계를 이해한다.


## 학습내용
- 빅데이터 소개
- 빅데이터와 사물인터넷
- 인공지능 소개
- 인공지능과 사물인터넷

---
## 1. 빅데이터 소개
- **빅데이터란**?
    - **기존 기술로 데이터를 수집·저장·관리·분석하는 것이 어려울 정도로 방대한 규모의
  데이터**를 의미
    - 1분 동안 구글에서는 200만 건의 검색, 유튜브에서는 48시간의 비디오가 Upload,
  트위터에서는 10만 건의 트윗이 생성

- **빅데이터 정의**
  - 빅데이터가 방대한 데이터라는 기준은 동일하지만, 업체별 빅데이터 정의에 미세한 차이 존재
  		- 세계적 컨설팅 기관인 Mckinsey는 빅데이터를 기존 데이터베이스 관리 도구의 데이터 수집·저장·관리·분석역량을 넘어서는 규모로 정의
  		- Gartner는 데이터를 21세기의 원유로 정의
  		- 또다른 기업은 빅데이터를 Terabyte(2^40 byte)이상의 데이터 및 대용량 데이터 처리 아키텍처로 정의
  - 최근 데이터를 통하여 원하는 가치(Value) 창출 여부로 빅데이터를 정의
  
- **빅데이터의 속성**
  - **Volume**: 데이터 크기
  - **Velocity**: 데이터 생성 속도
  - **Variety**: 데이터 다양성
  		- 다양한 종류의 데이터와 시간 경과에 따라 데이터가 바뀐다는 사실
  - **Varacity**: 정확성
	    - 빅데이터 시대에는 방대한 양의 **데이터를 분석하여 일정한 패턴 추출 가능**
	    - 데이터가 많아지면 **엉터리 데이터 생성 가능성 증대로 인해 데이터의 일정 패턴에
	    대한 신뢰성 확보 불가 문제** 발생
	    - 이에 따라 빅데이터 분석 시 기업이나 기관이 수집한 데이터의 정확성, 분석 가치 등 파악 필요성에 따라 새로운 속성인 Veracity 제시

- **빅데이터 플랫폼 기술**
	- 분산 환경에서 빅 데이터를 저장하고 처리할 수 있는 자바 기반의 오픈 소스 프레임 워크인 **하둡(Hadoop)**
	- 통계, 데이터 분석(Data Mining)과 그래프용 언어로 된 분석용 패키지 **R**
	- 비구조적 또는 반구조적 데이터를 처리하는데 적합한 **NoSQL 데이터베이스**


- 관련자료
	- http://www.itworld.co.kr/news/106362?page=0,0

## 2. 빅데이터와 사물인터넷
- 수많은 기기에서 나오는 데이터의 양은 점차 증가하므로 그 데이터에서 의미 있는 정보를 얻고 중요한 데이터만 효율적으로 처리하고 저장해야 한다.
- 머지않아 공장의 기계뿐만 아니라 자동차, 가전제품, 대형마트의 상품 등 거의 모든 사물에 센서가 부착될 것이며 그 센서에서 생성되는 **데이터를 통해 비즈니스 가치를 발굴**하려고 할 것이다.

<iframe width="560" height="315" src="https://www.youtube.com/embed/c_MLr3DqbuA?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<!--
	- 데이터를 중심으로 새로운 가치가 창출
	- 웹 시대의 비즈니스 모델 - 사용자의 검색 결과를 바탕으로 광고
	- IoT 시대의 비즈니스 모델 - 사물들이 만들어내는 Data를 통해서 사용자의 니즈를 예측
	- 사용자 가치를 극대화시킬 수 있는 사업전략 구축
		- 고객 데이터 수집: Iot 시대에는 고객이 입력하는 데이터가 아닌 자동으로 수집되는 데이터
	- IoT 시대를 리드하기 위한 핵심 질문
		- 어떤 데이터를 수집해야 하는가?
		- 어떤 방법으로 축적해야 하는가?
		- 축적된 정보에서 어떤 Context를 얻을 수 있는가?
		- Context를 통해 어떤 사용자 Value를 제공할 것인가? 
-->


### 3.1 UPS 사례

- ORION(On-Road Integrated Optimization and Navigation) 이니셔티브
	- 텔레매틱스 센서 데이터 및 고급 알고리즘을 사용하여 **배달 드라이버를 위한 최적의 경로를 실시간으로 최적화**
  	- 하루추적화물차수: 1,630만(880만고객), 일일배송추적요청: 3,950만건
  	- 46,000대 이상의 화물운송 차량에 부착된 센서데이터 수집
  	- 운행속도, 방향, 제동, 동력전달 성능 등을 데이터 분석을 통해 성과 모니터링 및 운행 노선 개선
- 결과
  	- 배송 기사 1명이 매일 1마일 운행 노선 단축 시, 3천만 달러 절약 효과
- 참고자료: https://www.zdnet.com/article/big-data-case-study-how-ups-is-using-analytics-to-improve-performance/

### 3.2 DBS Bank 사례
- 싱가폴 개발 은행으로 싱가폴 내 가장 많은 ATM기기 운영, 매월 1,100 개 ATM에서 2,500만 건의 거래 발생 
- ATM 내 잔고 소진에 대비하기 위해 **예금 인출 활동 및 현금 충전 시점을 예측**, **최소한으로 현금의 물리적 이동 계획**
- 결과
	- 1,100 개 ATM의 최적화된 운영
	- 30,000시간의 고객 대기 시간 감소
	- 현금 충전을 위한 이동 20% 감소
	- 은행으로 돌아가는 잔금 40% 감소

---
## 3. 인공지능 소개
- 인공지능 (Artificial Intelligence, AI) 이란?
  - 기계(컴퓨터)가 인간 수준의 인지, 이해, 추론, 학습 등의 사고 능력을 모방할 수 있도록 고안된 것
- 인공지능이란 무엇인가? 

	<iframe width="560" height="315" src="https://www.youtube.com/embed/7YSWn4p96Xw?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

	
<!--	
	- https://www.youtube.com/watch?v=sYt8EQzi20Y 
	- https://www.youtube.com/watch?v=2ePf9rue1Ao -->

- 인공지능과 머신러닝

	<iframe width="560" height="315" src="https://www.youtube.com/embed/0bcATLm-ylk?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
	
- [머신러닝, 딥러닝 초간단 설명](https://www.youtube.com/watch?v=aF03asAmQbY)
		

## 4. 인공지능과 사물인터넷의 만남
<!-- - 지능형 사물인터넷 (IoT)
	- https://www.youtube.com/watch?v=n8LvVvJnzdg
-->	
- 버틀러: AI+ 스마트 홈 IoT 서비스 플랫폼

	<iframe width="560" height="315" src="https://www.youtube.com/embed/DXyvIlXmIRA?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
	- https://www.youtube.com/watch?v=DXyvIlXmIRA
- 삼성의 IoT와 AI기술이 만드는 스마트한 일상

	<iframe width="560" height="315" src="https://www.youtube.com/embed/KltujKz8pOg?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
	- https://www.youtube.com/watch?v=KltujKz8pOg

- 사물인터넷 시대의 로봇

	<iframe width="560" height="315" src="https://www.youtube.com/embed/ZbxV9_wMusQ?rel=0&amp;start=157&end=1228" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<!--
- [How will Artificial Intelligence and Internet of Things change the world](https://www.youtube.com/watch?v=Cx5aNwnZYDc)
-->
---
<!--
## 1. IoT-Cloud-Bigdata-Mobile (ICBM) 기술이란?

- [IoT, Big Data and AI – the New ‘Superpowers’ In the Digital Universe]
(https://www.business2community.com/big-data/iot-big-data-ai-new-superpowers-digital-universe-01926411)

- [동영상][Building an Intelligent World with Big Data, IoT, and AI](https://www.youtube.com/watch?v=-DGlG_HrKIo)

- [Applications of AI in IoT | Applications of Big Data in IoT | IoT Future | IoT Career](https://www.youtube.com/watch?v=83gPmqR8ks0)
-->