# 아두이노 소개

**아두이노**는 마이크로프로세서나 컴퓨터 하드웨어에 대한 전문적인 지식 없이 쉽게 구현할 수 있는 **오픈소스 전자장치 플랫폼**으로서, [아두이노 하드웨어](#1.1)와 [아두이노 소프트웨어](#1.2)로 구성되어 있다.

- 초보에서부터 전문적인 수준의 기능도 구현할 수 있도록 다양한 확장성 제공
- 회로도 및 관련 소프트웨어가 공개된 대표적인 오픈소스 시스템
- 아두이노 보드를 사용한 많은 활용 예제 코드들이 공개되어 있음

아두이노 공식 홈페이지: http://www.arduino.cc/
- 아두이노 소프트웨어 다운로드
- 아두이노 하드웨어 정보


---
<a name="1.1"> </a>
## 1. 아두이노 하드웨어
아두이노 하드웨어는 보드와 기능 확장을 위해 보드에 적층되는 다양한 쉴드로 구성되어 있음.

### 1.1 보드
+ 컴퓨터와 같은 확장 가능한 전자기기의 부품의 일종으로, CPU나 램과 같은 시스템이 작동되기 위한 주요 부품 장착과 주변 장치를 연결할 수 있는 인터페이스를 제공하는 인쇄회로기판(PCB)을 의미 [https://ko.wikipedia.org/wiki/메인보드]
	- **아두이노 우노 보드** ([Arduino Uno REV3](https://store.arduino.cc/usa/arduino-uno-rev3))
		- Atmel사의 8비트 ATmega328 **[마이크로컨트롤러](https://ko.wikipedia.org/wiki/마이크로컨트롤러)**
		- **디지털 입/출력핀**(0~13번) : 14개
			- PWM 출력: 3, 5, 6, 9, 10, 11번핀(“~”가붙어있는핀)
			- 시리얼통신: RX 출력(0번), TX 입력(1번)
		- **아날로그 입력핀**(0~5번) : 6개
		
		<img src=images/arduino_uno_r3.jpg width=400>
		
		<img src=images/uno_pin.jpg width=400>

	- 그외 다양한 [아두이노 보드 종류](https://ko.wikipedia.org/wiki/%EC%95%84%EB%91%90%EC%9D%B4%EB%85%B8_%EB%B3%B4%EB%93%9C#%EC%83%81%EC%97%85%EC%9A%A9_%EC%95%84%EB%91%90%EC%9D%B4%EB%85%B8_%EB%B3%B4%EB%93%9C)

### 1.2 쉴드
+ 추가 기능 확장을 위하여 보드에 플러그 인되는 요소

	<img src=images/shield.jpg width=600>
	<img src=images/shield2.jpg width=600>

---
<a name="1.2"></a>
## 2. 아두이노 소프트웨어

### 2.1 [**Sketch**](https://www.arduino.cc/en/Tutorial/Sketch) 프로그램
- 아두이노 보드에 업로드되고 실행되는 프로그램 코드 단위
- C/C++ 문법을 따름
- 많은 활용 예제 코드들이 공개되어 있음
	- *Sketch* 예제 (1초마다 디지털 13번 핀에 연결된 LED를 켜고 끄는 것을 반복)

	```C
	// the setup function runs once when you press reset or power the board
	void setup() {
	 	// initialize digital pin 13 as an output.
		 pinMode(13, OUTPUT);
	}

	// the loop function runs over and over again forever
	void loop() {
		 digitalWrite(13, HIGH);   // turn the LED on (HIGH is the voltage level)
		 delay(1000);                       // wait for a second
		 digitalWrite(13, LOW);    // turn the LED off by making the voltage LOW
		 delay(1000);                       // wait for a second
	}
	```


<a name="1.3"> </a>
### 2.2 아두이노 IDE
- *Sketch* 프로그램을 작성하고 컴파일하여 보드에 업로드할 수 있는 기능을 제공하는 통합 개발 환경으로써, 데스크탑 버전과 웹 버전으로 제공된다.

- **Ardunio Desktop IDE**
	- Windows, Mac OSX, Linux 환경에서 	*Sketch* 프로그램을 작성하고 업로드할 수 있는 개발 환경

		<img src=images/install_ide.png width=500>

- **Arduino WEB Editor**
	- 웹 브라우저 환경에서 *Sketch* 프로그램을 작성하고 보드에 업로드할 뿐만아니라, 작성된 *Sketch* 프로그램을 공유하고 협업할 수 있는 개발 환경   

	<img src=images/arduino_web_editor.png width=600>
