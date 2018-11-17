<style>
div.polaroid {
  	width: 400px;
  	box-shadow: 0 10px 30px 0 rgba(0, 0, 0, 0.2), 0 16px 30px 0 rgba(0, 0, 0, 0.19);
  	text-align: center;
	margin-bottom: 0.5cm;
}
</style>

### 4.1 예제 4 (소프트웨어 시리얼 기능을 갖는 블루투스 쉴드를 이용한 LED의 ON/OFF 제어)

#### 4.1.1 아두이노 보드 연결 구성

<div class="polaroid">
    <img src="images/example4_pin.png" >
</div>


<div class="polaroid">
    <img src="images/example4_pin2.png" >
</div>


#### 4.1.2 Sketch 프로그램
```c
#include <SoftwareSerial.h>int rxPin=2;int txPin=3;SoftwareSerial BTSerial(rxPin,txPin); // 소프트웨어 시리얼 설정int ledPin = 8;       // 아두이노 보드의 디지털입출력 핀 8번에 LED연결void setup( ) {    BTSerial.begin(9600);      // BT 모듈의 통신 속도 9600bps 설정   pinMode(ledPin, OUTPUT); // 디지털입출력 핀 8번을 출력으로 설정}void loop() {  char r_data;  if (BTSerial.available( )> 0) { // BT 모듈을 통한 시리얼 통신 입력 발생 검사    r_data = BTSerial.read( );    // 시리얼 통신 문자 입력 값 저장, (시리얼 통신으로 수신되는 데이터의 타입이 문자형 임을 가정)    if( r_data == '1') {        // 스마트 폰의 앱 “BT_ONOFFSW.apk”의 "Switch ON"이 터치될 때, 문자 '1'이 전송됨         digitalWrite(ledPin, HIGH);  // LED 켜기    }    if( r_data == '2') {        // 스마트 폰의 앱 “BT_ONOFFSW.apk”의 "Switch OFF"이 터치될 때, 문자 '2'가 전송됨         digitalWrite(ledPin, LOW);   // LED 끄기    }  }}
```
