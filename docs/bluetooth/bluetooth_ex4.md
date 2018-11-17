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
#include <SoftwareSerial.h>
```