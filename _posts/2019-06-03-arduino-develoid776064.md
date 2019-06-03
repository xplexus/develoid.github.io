---
layout: post
title: '아두이노 기본 - Serial 함수'
author: '시류아'
categories: Arduino
tags:
- IoT-Board
- Arduino
- Programming
-
---


<script> location.href='https://cafe.naver.com/develoid/776064' ; </script>


















						<div>
 <div>
  <img src="https://dthumb-phinf.pstatic.net/?src=%22http%3A%2F%2Fblogfiles.naver.net%2FMjAxNzAxMThfNjIg%2FMDAxNDg0NzA1NjM1OTcw.Ymu3eB7NhpZyofFcJS2P4w_Fc6TSYJYMd0L3KdlL9s0g._OBm7D7ygwJVmmrthsPgTuBZnkzHtCpdbpxsihEn1y4g.JPEG.searphiel9%2Farduino_logo.jpg%22&amp;type=cafe_wa740">
 </div>
</div>
<div>
 <div>
  <div>
   아두이노 기본
   <b>Serial 함수
  </div>
 </div>
</div>
<div>
 <p>아두이노와 아두이노, 아두이노와 PC의 통신에서 가장 많이 사용되는 방법은 RS232 시리얼 통신이다. 주로 사용되는 것은 별로 없으나 생각보다 많은 함수가 있다. 그 중 자주 사용되는 것들을 중심으로 정리해보겠다.</p>
</div>
<div>
 <div>
  <div></div>
 </div>
</div>
<div>
 <div>
  <div>
   begin
  </div>
 </div>
</div>
<div>
 <p>통신을 시작하고 통신속도를 지정할 때 사용한다. 통신속도는 4800~250000 까지 있으며, 보통 평균적으로 9600~115200 사이로 사용된다. ( 참고로 L 사 같은 경우 4800 을 권장속도로 사용하고 있다. )</p>
</div>
<div>
 <div>
  <div>
   Serial.begin(speed)
   <b>&nbsp;
   <b>//&nbsp;speed&nbsp;:&nbsp;통신&nbsp;속도
   <b>//&nbsp;4800&nbsp;/&nbsp;9600&nbsp;/&nbsp;14400&nbsp;/&nbsp;19200&nbsp;/&nbsp;22800&nbsp;/&nbsp;38400&nbsp;/&nbsp;57600&nbsp;/&nbsp;115200
  </div>
 </div>
</div>
<div>
 <p>Serial.begin 예제</p>
</div>
<div>
 <div>
  <div>
   void&nbsp;setup()&nbsp;{
   <b>&nbsp;&nbsp;Serial.begin(9600);&nbsp;//&nbsp;9600의&nbsp;속도로&nbsp;통신을&nbsp;시작한다
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
 <div>
  <div>
   available
  </div>
 </div>
</div>
<div>
 <p>통신 중 통신 값이 들어온 여부 파악시 사용한다. 이를 사용해서 통신 도중 잘 못 들어온 값에 의해서 동작하거나, 다른 신호가 들어와서 동작하는 경우를 예방 할 수 있다.</p>
</div>
<div>
 <div>
  <div>
   Serial.available()
  </div>
 </div>
</div>
<div>
 <p>Serial.available 예제</p>
</div>
<div>
 <div>
  <div>
   int&nbsp;readByte&nbsp;=&nbsp;0;
   <b>&nbsp;
   <b>void&nbsp;setup()&nbsp;{
   <b>&nbsp;&nbsp;Serial.begin(9600);&nbsp;//&nbsp;9600의&nbsp;속도토&nbsp;통신을&nbsp;시작한다
   <b>}
   <b>&nbsp;
   <b>void&nbsp;loop()&nbsp;{
   <b>&nbsp;&nbsp;if(Serial.available()&nbsp;&gt;&nbsp;0)&nbsp;{
   <b>&nbsp;&nbsp;&nbsp;&nbsp;readByte&nbsp;=&nbsp;Serial.read();&nbsp;//&nbsp;통신을&nbsp;통해&nbsp;들어온&nbsp;값을&nbsp;readByte에&nbsp;저장해라
   <b>&nbsp;&nbsp;&nbsp;&nbsp;Serial.print(“I&nbsp;Read&nbsp;:&nbsp;”);
   <b>&nbsp;&nbsp;&nbsp;&nbsp;Serial.println(readByte,&nbsp;DEC);&nbsp;//&nbsp;readByte로&nbsp;들어온&nbsp;값&nbsp;출력
   <b>&nbsp;&nbsp;}
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
 <div>
  <div>
    flush
  </div>
 </div>
</div>
<div>
 <p>시리얼 통신 후 시리얼 통신 할 때 들어오거나 남아있는 값을 제거할 때 사용한다.</p>
</div>
<div>
 <div>
  <div>
   Serial.flush()
  </div>
 </div>
</div>
<div>
 <p> Serial.flush 예제</p>
</div>
<div>
 <div>
  <div>
   void&nbsp;setup()&nbsp;{
   <b>&nbsp;&nbsp;Serial.begin(9600);&nbsp;//&nbsp;9600의&nbsp;속도토&nbsp;통신을&nbsp;시작한다
   <b>&nbsp;&nbsp;Serial.flush();&nbsp;//&nbsp;통신에&nbsp;남아있는&nbsp;쓰레기&nbsp;값&nbsp;제거
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
 <div>
  <div>
   print / println
  </div>
 </div>
</div>
<div>
 <p>print 와 println 은 시리얼 통신으로 값을 송출할 때 사용한다. 또 이를 활용해 현재 진행상황 등을 확인 할 수 있다.</p>
</div>
<div>
 <div>
  <div>
   Serial.print(val)
   <b>&nbsp;
   <b>val&nbsp;:&nbsp;보낼&nbsp;값,&nbsp;이때&nbsp;문자열을&nbsp;송출하려면&nbsp;“”을&nbsp;사용해서&nbsp;해야된다
  </div>
 </div>
</div>
<div>
 <p>Serial.print / Serial.println 예제</p>
</div>
<div>
 <div>
  <div>
   int&nbsp;x&nbsp;=&nbsp;0;
   <b>&nbsp;
   <b>void&nbsp;setup()&nbsp;{
   <b>&nbsp;&nbsp;Serial.begin(9600);
   <b>}
   <b>&nbsp;
   <b>void&nbsp;loop()&nbsp;{
   <b>&nbsp;&nbsp;Serial.print(“NO&nbsp;FORMAT&nbsp;\t”);
   <b>&nbsp;&nbsp;Serial.print(“DEC&nbsp;\t”);
   <b>&nbsp;&nbsp;Serial.print(“BIN&nbsp;\t”);
   <b>&nbsp;&nbsp;Serial.print(“OCT&nbsp;\t”);
   <b>&nbsp;&nbsp;Serial.print(“HEX&nbsp;\t”);
   <b>&nbsp;
   <b>&nbsp;&nbsp;for(x=0;&nbsp;x&lt;64;&nbsp;x++)&nbsp;{
   <b>&nbsp;&nbsp;&nbsp;&nbsp;Serial.print(x);
   <b>&nbsp;&nbsp;&nbsp;&nbsp;Serial.print(“\t”);
   <b>&nbsp;&nbsp;&nbsp;&nbsp;Serial.print(x,&nbsp;DEC);
   <b>&nbsp;&nbsp;&nbsp;&nbsp;Serial.print(“\t”);
   <b>&nbsp;&nbsp;&nbsp;&nbsp;Serial.print(x,&nbsp;BIN);
   <b>&nbsp;&nbsp;&nbsp;&nbsp;Serial.print(“\t”);
   <b>&nbsp;&nbsp;&nbsp;&nbsp;Serial.print(x,&nbsp;OCT);
   <b>&nbsp;&nbsp;&nbsp;&nbsp;Serial.print(“\t”);
   <b>&nbsp;&nbsp;&nbsp;&nbsp;Serial.print(x,&nbsp;HEX);
   <b>&nbsp;&nbsp;&nbsp;&nbsp;Serial.print(“\t”);
   <b>&nbsp;&nbsp;&nbsp;&nbsp;delay(200);
   <b>&nbsp;&nbsp;}
   <b>&nbsp;&nbsp;Serial.println(“”);
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
 <div>
  <div>
   read
  </div>
 </div>
</div>
<div>
 <p>시얼 통신에서 값을 수신 받을 때 사용한다.</p>
</div>
<div>
 <div>
  <div>
   Serial.read()
  </div>
 </div>
</div>
<div>
 <div>
  <div></div>
 </div>
</div>
<div>
 <div>
  <div>
   write
  </div>
 </div>
</div>
<div>
 <p>시리얼 통신으로 값을 보낼 때 사용한다. print 함수와 동일한 기능을 하지만 다르다.</p>
</div>
<div>
 <div>
  <div>
   Serial.write(val)
  </div>
 </div>
</div>
<div>
 <p>Serial.read &amp; Serial.write 예제</p>
</div>
<div>
 <div>
  <div>
   void&nbsp;setup()&nbsp;{
   <b>&nbsp;&nbsp;Serial.begin(9600);&nbsp;//&nbsp;9600의&nbsp;속도토&nbsp;통신을&nbsp;시작한다.
   <b>}
   <b>&nbsp;
   <b>void&nbsp;loop()&nbsp;{
   <b>&nbsp;&nbsp;if(Serial.available()&nbsp;&gt;&nbsp;0)&nbsp;{
   <b>&nbsp;&nbsp;&nbsp;&nbsp;int&nbsp;readByte&nbsp;=&nbsp;Serial.read();&nbsp;//&nbsp;통신을&nbsp;통해&nbsp;들어온&nbsp;값을&nbsp;readByte에&nbsp;저장해라
   <b>&nbsp;&nbsp;&nbsp;&nbsp;readByte&nbsp;*=&nbsp;2;&nbsp;//&nbsp;readByte에&nbsp;2를&nbsp;곱하여라
   <b>&nbsp;&nbsp;&nbsp;&nbsp;Serial.write(readByte);&nbsp;//&nbsp;write를&nbsp;통해서&nbsp;출력해라
   <b>&nbsp;&nbsp;&nbsp;&nbsp;delay(100);
   <b>&nbsp;&nbsp;}
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
 <div>
  <div>
   write 와 print 의 차이점
  </div>
 </div>
</div>
<div>
 <p>write 와 print의 차이점은 한 문자를 출력하느냐, 한 문단을 출력하느냐의 차이이다. 간단하게 write 와 print 를 통해서 각각 한 문단을 송출해보면 손 쉽게 알 수 있다.</p>
</div>
<div>
 <div>
  <div>
   void&nbsp;loop()&nbsp;{
   <b>&nbsp;&nbsp;Serial.write(“Hello”);
   <b>&nbsp;&nbsp;Serial.print(“Hello”);
   <b>}
  </div>
 </div>
</div>
<div>
 <p>우리가 만약 Hello 를 출력한다고 하자, write로 출력을 했을 경우 Hello 는 한 글자씩 끊어져서 H, e, l, l, o 로 출력되었을 것이다. 그에 비해서 print는 Hello 를 끊지 않고 한 문장으로 출력하고 있을 것이다. 이 둘 중 어떤 것이 틀렸다는 것은 없다. 상황에 따라서 write를 써야 될 수도 있으며, 반대로 print를 사용해야 될 수도 있다.</p>
</div>