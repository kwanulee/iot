## 아두이노 프로그래밍 기초

```c
/*
 Blink
 Turns on an LED for one second, then off for one second, repeatedly.
 
 This example code is in the public domain.
*/

// Pin 13 has an LED connected on most Arduino boards.
// give it a name:
int led = 13;    // set the variable “led” to the value 13

// the setup routine runs once when you press reset:
void setup() {
    // initialize the digital pin as an output.
    pinMode(led, OUTPUT);
}

void loop() {
    digitalWrite(led, HIGH);  // turn the LED on
    delay(1000);              // wait for a second
    digitalWrite(led, LOW);   // turn the LED off
    delay(1000);              // wait for a second
}
```

### 프로그램 구조
- 모든 아두이노 프로그램 (Sketch)는 세 부분으로 구성됨
	- 선언 부분 
		- 전처리기문 (#include, #define) 선언
		- 변수 선언 
	- setup 함수 부분
		- 처음 시작할 때 한번만 실행되는 함수로서, 아두이노 하드웨어 설정, 변수 초기화 등을 수행 
	- loop 함수 부분
		- 전원이 들어오는 동안 무한히 반복 수행하는 함수


### 주석
- 프로그램에 대한 설명
- 주석 안에 있는 문장은 컴파일 시 컴퓨터가 무시
- Syntax
	- /* ... */ - 여러 줄 주석 처리  
	- // ... - 한줄 만 주석 처리 


### 주요 함수
#### [pinMode(pin,mode)](https://www.arduino.cc/reference/en/language/functions/digital-io/pinmode/)
- 이 함수는 디지털 입출력 핀 중 하나에 대해서 입력 혹은 출력을 설정
- 파라미터
	- pin: 디지털 입출력 핀 번호 (0~13번)
	- mode: INPUT, OUTPUT, INPUT_PULLUP 중 하나
- 예제 - 13번 핀을 출력으로 사용
	
	```c
	pinMode(13, OUTPUT)
	```
	
#### [digitalWrite(pin, value)](https://www.arduino.cc/reference/en/language/functions/digital-io/digitalwrite/)
- 이 함수는 디지털 입출력 핀 중 하나에 대해서 입력 혹은 출력을 설정
- 파라미터
	- pin: 디지털 핀 번호
	- mode: HIGH 혹은 LOW
- 예제 - 13번 핀을 HIGH 상태로 만들어라
	
	```c
	digitalWrite(13, HIGH)
	```

#### [delay(time)]()
- 지정된 시간 time (ms 단위) 만큼 시간을 지연
- 파라미터
	- time: 1/1000초 단위의 값
- 예제 - 1초 동안 지연

	```c
	delay(1000);
	```
	
	
	  