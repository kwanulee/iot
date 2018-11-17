<style>
div.polaroid {
  	width: 500px;
  	box-shadow: 0 10px 30px 0 rgba(0, 0, 0, 0.2), 0 16px 30px 0 rgba(0, 0, 0, 0.19);
  	text-align: center;
	margin-bottom: 0.5cm;
}
</style>

<a name="ex2"></a>
### 2.2 예제 2 (스마트폰을 이용한 4개의 LED ON/OFF 제어)
- 아두이노 보드에 4개의 LED 연결
- 스마트 폰과 블루투스 모듈을 통하여 4개의 LED  ON/OFF
- 6개의 기능 버튼이 있는 스마트 폰 App(**BT_SW6.apk**) 설치
	- [**BT_SW6.apk** 다운로드 링크](https://github.com/kwanulee/iot/releases/download/v1/BT_SW6.apk)

	<div class="polaroid">
    	<img src="images/example2.png" >
	</div>

#### 2.2.1 아두이노 보드 연결 구성
- 이전 보드 연결 구성에서 다음 연결 추가
	- 디지털 입출력 핀 9, 10, 11 번과 LED 1,2,3 연결 추가

	<div class="polaroid">
    	<img src="images/example2_connection.png" >
	</div>

#### 2.2.2 Sketch 프로그램
```c
int ledPin[4] = {8,9,10,11};
int k, num;
char phoneData;

void setup( ) {
   Serial.begin(9600);
   for (k=0; k<4; k++) {
      pinMode(ledPin[k], OUTPUT);
   }
}

/*
  SerialEvent occurs whenever a new data comes in the hardware serial RX. This
  routine is run between each time loop() runs, so using delay inside loop can
  delay response. Multiple bytes of data may be available.
*/
void serialEvent() {
  phoneData = Serial.read( );
}

void loop() {
    if (phoneData == '1') {
         digitalWrite(ledPin[0], HIGH);
    } else if (phoneData == '2') {
         digitalWrite(ledPin[1], HIGH);
    } else if (phoneData == '3') {
         digitalWrite(ledPin[2], HIGH);
    } else if (phoneData == '4') {
         digitalWrite(ledPin[3], HIGH);
    } else if (phoneData == '6') {
      for (k=0; k<4; k++) {
        digitalWrite(ledPin[k], LOW);
      }
    }
}
```

- [**serialEvent**](https://www.arduino.cc/en/Reference/SerialEvent)() 함수
	- 이 함수는 loop()함수가 실행될 때마다, 시리얼 데이터가 있으면 호출됨
	- 이 함수는 [Esplora](https://store.arduino.cc/arduino-esplora), [Leonardo](https://store.arduino.cc/arduino-leonardo-without-headers), [Micro](https://store.arduino.cc/arduino-micro-without-headers) 아두이노 보드에서는 호환되지 않음

#### 2.2.3 스마트 폰에 App 설치
1. 휴대폰에서 아래 링크를 클릭하여 앱(**BT_SW6.apk**) 다운로드
	[**BT_SW6.apk** 다운로드 링크](https://github.com/kwanulee/iot/releases/download/v1/BT_SW6.apk)
2. 다운로드된 후, 파일 열기를 클릭하여 설치
	- "보안상의 이유로 이 소스에서 가져온 알 수 없는 앱을 휴대전화에 설치할 수 없습니다." 메시지가 나오면, 설정을 클릭한후 "이 출처 허용"을 활성화
	- 앞 페이지로 이동한 후에, 설치를 클릭하여 설치

#### 2.2.4 실행
1. 스마트폰에서 앱 실행
2. 블루투스 찾기 버튼 클릭하여 연결할 블루투스 모듈 선택
	- 연결이 되면, 화면 상단에 연결 ON이 표시됨
2. SW1, SW2, SW3, SW4, SW_OFF 버튼을 눌러 8,9,10,11번 핀에 연결된 LED의 ON/OFF 확인
