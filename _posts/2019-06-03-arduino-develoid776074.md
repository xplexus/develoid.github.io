---
layout: post
title: '아두이노 응용 - Bluetooth를 이용한 서보 제어'
author: '시류아'
categories: Arduino
tags:
- IoT-Board
- Arduino
- Programming
-
---


<script> location.href='https://cafe.naver.com/develoid/776074' ; </script>


















						<div>
 <div>
  <img src="https://dthumb-phinf.pstatic.net/?src=%22http%3A%2F%2Fblogfiles.naver.net%2FMjAxNzAxMTlfMjIz%2FMDAxNDg0ODI2MTQ5Mjkz.YnyVgbJSPQLJWaUhuPIqtgX-M8_TJNa10XhZVFR1Y2Yg.5OUUGkPE7NvYz5sx08bJdeEfZcg_hDxcJEjI_llcYzwg.JPEG.searphiel9%2Farduino_logo.jpg%22&amp;type=cafe_wa740">
 </div>
</div>
<div>
 <div>
  <div>
   아두이노 응용
   <b>Bluetooth를 이용한 서보 제어
  </div>
 </div>
</div>
<div>
 <p>이번에는 블루투스를 이용해서 서보모터를 가감속 및 좌우 방향 제어를 해보자, 소스코드는 시리얼 통신을 하기 때문에 시리얼 커뮤니케이션을 이용해서 통신하는 Xbee를 이용한 제어와 차이가 없으며, 스마트폰 블루투스로도 충분히 제어 가능하기 때문에 별도의 송신 장비를 만들 필요가 없다. 단 블루투스 제어 앱이 필요로한데, MIT 앱 인벤터를 이용한 제어 앱 만들기를 통해서 Bluetooth 제어 앱을 만들고 제어까지 할 수 있도록 해보자.</p>
</div>
<div>
 <div>
  <div></div>
 </div>
</div>
<div>
 <div>
  <div>
   회로도
  </div>
 </div>
</div>
<div>
 <div>
  <img src="https://dthumb-phinf.pstatic.net/?src=%22http%3A%2F%2Fblogfiles.naver.net%2FMjAxNzAxMTlfMTQ5%2FMDAxNDg0ODI2MjE2MzUx.PnZLoetUIpUzwPCr-Ukf6LogDG57mTrbZ9IdP8ItyrMg.NHFKGFudkoZ0_9GqaLbGSLj2WtCpUEa_iw8Vk9OE1S0g.PNG.searphiel9%2F1.png%22&amp;type=cafe_wa740">
  <span>Bluetooth 회로도</span>
 </div>
</div>
<div>
 <p>Bluetooth 회로는 위를 참고해서 배선해주길 바란다.</p>
</div>
<div>
 <div>
  <div></div>
 </div>
</div>
<div>
 <div>
  <div>
   블루투스로 서보모터 제어하기
  </div>
 </div>
</div>
<div>
 <div>
  <div>
   <b>#include&nbsp;&lt;VarSpeedServo.h&gt;&nbsp;
   <b>&nbsp;
   <b>VarSpeedServo&nbsp;myservo;
   <b>&nbsp;
   <b>int&nbsp;Servo_deg&nbsp;=&nbsp;90;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;//&nbsp;서보&nbsp;위치
   <b>int&nbsp;Servo_speed&nbsp;=&nbsp;127;&nbsp;&nbsp;&nbsp;&nbsp;//&nbsp;서보&nbsp;속도
   <b>&nbsp;
   <b>void&nbsp;setup()&nbsp;{
   <b>&nbsp;&nbsp;Serial.begin(9600);&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;//&nbsp;시리얼&nbsp;통신&nbsp;설정
   <b>&nbsp;&nbsp;myservo.attach(3);&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;//&nbsp;서보&nbsp;PIN&nbsp;설정
   <b>&nbsp;&nbsp;myservo.write(90,255,true);&nbsp;&nbsp;//&nbsp;서보&nbsp;위치&nbsp;초기화
   <b>}
   <b>&nbsp;
   <b>void&nbsp;loop()&nbsp;{
   <b>&nbsp;&nbsp;if&nbsp;(Serial.available()&nbsp;&gt;&nbsp;0)&nbsp;{
   <b>&nbsp;&nbsp;&nbsp;&nbsp;if(Serial.read()&nbsp;==&nbsp;'u')&nbsp;Servo_speed++;
   <b>&nbsp;&nbsp;&nbsp;&nbsp;if(Serial.read()&nbsp;==&nbsp;'d')&nbsp;Servo_speed--;
   <b>&nbsp;&nbsp;&nbsp;&nbsp;if(Serial.read()&nbsp;==&nbsp;'l')&nbsp;Servo_deg--;
   <b>&nbsp;&nbsp;&nbsp;&nbsp;if(Serial.read()&nbsp;==&nbsp;'r')&nbsp;Servo_deg++;
   <b>&nbsp;&nbsp;}
   <b>&nbsp;
   <b>&nbsp;&nbsp;myservo.write(Servo_deg,&nbsp;Servo_speed,&nbsp;true);&nbsp;&nbsp;&nbsp;&nbsp;//&nbsp;서보&nbsp;위치&amp;속도&nbsp;제어
   <b>}
  </div>
 </div>
</div>
<div>
 <div>
  <div></div>
 </div>
</div>
<div>
 <p>다 되었다면 안드로이드 기준으로 Google PlayStore에서 Arduino BT Joystick, Bluetooth Master 등 다양한 블루투스 제어 앱이 있으니 앱을 다운로드 받아 설정 후 테스트를 해보는 것도 좋다.</p>
</div>
<div>
 <div>
  <div></div>
 </div>
</div>
<div>
 <p>소스코드에 정답은 없다. 다양한 생각이 있듯 다양한 방법이 있으며, 그 중 하나일 뿐이다.</p>
</div>