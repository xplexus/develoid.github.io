---
layout: post
title: '프로세싱 기초 - 자주 사용하는 함수 정리'
author: '시류아'
categories: Programming-Processing
tags:
- Programming
- Language
- Graphic
- Arduino
---


<script> location.href='https://cafe.naver.com/develoid/776086' ; </script>


















						<div>
 <div>
  <img src="https://dthumb-phinf.pstatic.net/?src=%22http%3A%2F%2Fblogfiles.naver.net%2FMjAxNzAxMjRfNjcg%2FMDAxNDg1MjM5MjcyMDkx.8NnpKR1RW-0S80KQ5RC8lxzmjT-JsDzgAcB75gSqPmYg.lHEv9th1bjFk-cMvrZ_7J-jbTdRmxf_zHDdpQ7I3i4Qg.PNG.searphiel9%2Fprocessing_logo.png%22&amp;type=cafe_wa740">
 </div>
</div>
<div>
 <div>
  <div>
   프로세싱 기초
   <b>자주 사용하는 함수 정리
  </div>
 </div>
</div>
<div>
 <p>프로세싱에서 자주 사용하는 기초 함수들을 한 번 살펴보자, 설명에 앞서서 프로세싱은 좌표계를 이용하고 있으며, 설명 상 약어료 W(width, 너비), H(height, 높이), X(가로좌표), Y(세로좌표)로 요약한다.</p>
</div>
<div>
 <div>
  <div></div>
 </div>
</div>
<div>
 <div>
  <div>
   setup
  </div>
 </div>
</div>
<div>
 <p>처음&nbsp;시작&nbsp;할&nbsp;때&nbsp;한&nbsp;번만&nbsp;실행하는&nbsp;것들을 모아놓는 함수이다.</p>
</div>
<div>
 <div>
  <div>
   setup()&nbsp;{}
  </div>
 </div>
</div>
<div>
 <div>
  <div>
    draw
  </div>
 </div>
</div>
<div>
 <p>반복해서 실행 되는 것들을 모아놓는 루프 함수이다.</p>
</div>
<div>
 <div>
  <div>
   draw()&nbsp;{}
  </div>
 </div>
</div>
<div>
 <div>
  <div>
   size
  </div>
 </div>
</div>
<div>
 <p>화면의 크기를 지정하는 함수이다.</p>
</div>
<div>
 <div>
  <div>
   size(W,&nbsp;H);
   <b>
   <b>//&nbsp;ex&nbsp;//
   <b>size(360,&nbsp;240);
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
   background
  </div>
 </div>
</div>
<div>
 <p>뒷 배경 색상을 지정한다. 0~255까지의 색상 밝기로도 가능하며, RGB / 웹컬러 등으로도 가능하다.</p>
</div>
<div>
 <div>
  <div>
   background(color);
   <b>background(webcolor);
   <b>background(r,&nbsp;g,&nbsp;b);
   <b>
   <b>//&nbsp;ex&nbsp;//
   <b>background(0);
   <b>background(#000000);
   <b>background(255,&nbsp;255,&nbsp;255);
  </div>
 </div>
</div>
<div>
 <div>
  <div>
   strokeWeight
  </div>
 </div>
</div>
<div>
 <p>점과 선의 두께를 설정한다.</p>
</div>
<div>
 <div>
  <div>
   strokeWeight(size);
   <b>
   <b>//&nbsp;ex&nbsp;//
   <b>strokeWeight(10);
  </div>
 </div>
</div>
<div>
 <div>
  <div>
   stroke
  </div>
 </div>
</div>
<div>
 <p>점과 선의 색상 설정, 0~255 까지 색상 밝기 또는 RGB / 웹컬러 등으로 설정 할 수 있다.</p>
</div>
<div>
 <div>
  <div>
   stroke(color);
   <b>stroke(webcolor);
   <b>stroke(r,&nbsp;g,&nbsp;b);
   <b>
   <b>//&nbsp;ex&nbsp;//
   <b>stroke(0);
   <b>stroke(#000000);
   <b>stroke(255,&nbsp;127,&nbsp;0);
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
   point
  </div>
 </div>
</div>
<div>
 <p>해당 좌표에 점을 찍는다.</p>
</div>
<div>
 <div>
  <div>
   point(x,&nbsp;y);
   <b>
   <b>//&nbsp;ex&nbsp;//
   <b>point(10,&nbsp;10);
  </div>
 </div>
</div>
<div>
 <div>
  <div>
   line
  </div>
 </div>
</div>
<div>
 <p>해당 좌표에 선을 긋는다. X1/Y1 은 첫 번째 점, X2/Y2는 두 번째 점의 위치 좌표이다.</p>
</div>
<div>
 <div>
  <div>
   line(x1,&nbsp;y1,&nbsp;x2,&nbsp;y2);
   <b>
   <b>//&nbsp;ex&nbsp;//
   <b>line(10,&nbsp;10,&nbsp;50,&nbsp;50);
  </div>
 </div>
</div>
<div>
 <div>
  <div>
   rect
  </div>
 </div>
</div>
<div>
 <p>해당 좌표를 기준으로 사각형을 그린다. X/Y는 왼쪽 위의 시작 점, W/H 는 크기이다.</p>
</div>
<div>
 <div>
  <div>
   rect(X,&nbsp;Y,&nbsp;W,&nbsp;H);
   <b>
   <b>//&nbsp;ex&nbsp;//
   <b>rect(10,&nbsp;10,&nbsp;50,&nbsp;50);
  </div>
 </div>
</div>
<div>
 <div>
  <div>
   triangle
  </div>
 </div>
</div>
<div>
 <p>해당 좌표들을 잇는 삼각형을 그린다.</p>
</div>
<div>
 <div>
  <div>
   triangle(x1,&nbsp;y1,&nbsp;x2,&nbsp;y2,&nbsp;x3,&nbsp;y3);
   <b>
   <b>//&nbsp;ex&nbsp;//
   <b>triangle(50,50,0,0,100,0);
  </div>
 </div>
</div>
<div>
 <div>
  <div>
   quad
  </div>
 </div>
</div>
<div>
 <p>해당 좌표들을 잇는 사각형을 그린다.</p>
</div>
<div>
 <div>
  <div>
   quad(x1,&nbsp;y1,&nbsp;x2,&nbsp;y2,&nbsp;x3,&nbsp;y3,&nbsp;x4,&nbsp;y4);
   <b>
   <b>//&nbsp;ex&nbsp;//
   <b>quad(0,0,50,0,0,50,50,50);
  </div>
 </div>
</div>
<div>
 <div>
  <div>
   ellipse
  </div>
 </div>
</div>
<div>
 <p>해당 좌표를 기준으로 원을 그린다. X/Y 는 원의 중앙 좌표이며, W/H 는 크기이다.</p>
</div>
<div>
 <div>
  <div>
   ellipse(x,&nbsp;y,&nbsp;w,&nbsp;h);
   <b>
   <b>//&nbsp;ex&nbsp;//
   <b>ellipse(10,&nbsp;10,&nbsp;50,&nbsp;50);
  </div>
 </div>
</div>
<div>
 <div>
  <div>
   Text
  </div>
 </div>
</div>
<div>
 <p>X/Y 좌표에 글자를 작성한다.</p>
</div>
<div>
 <div>
  <div>
   text(TEXT,&nbsp;X,&nbsp;Y);
   <b>
   <b>//&nbsp;ex&nbsp;//
   <b>text(“TEST”,&nbsp;20,&nbsp;20);
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
   PImage
  </div>
 </div>
</div>
<div>
 <p>PNG, JPG 등 이미지 파일을 가져온다.</p>
</div>
<div>
 <div>
  <div>
   PImage&nbsp;img;
   <b>img&nbsp;=&nbsp;loadImage("test.jpg");
   <b>image(img,&nbsp;0,&nbsp;0);
  </div>
 </div>
</div>
<div>
 <div>
  <div>
   PFont
  </div>
 </div>
</div>
<div>
 <p>VLW 폰트 파일을 가져온다.</p>
</div>
<div>
 <div>
  <div>
   PFont&nbsp;font;
   <b>font&nbsp;=&nbsp;loadFont("test.vlw");
   <b>textFont(font);
  </div>
 </div>
</div>
<div>
 <div>
  <div>
   PShape
  </div>
 </div>
</div>
<div>
 <p>SVG 등 벡터 파일을 가져온다.</p>
</div>
<div>
 <div>
  <div>
   PShape&nbsp;svg;
   <b>svg&nbsp;=&nbsp;loadShape("test.svg");
   <b>shape(test&nbsp;0,&nbsp;0);
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
   Mouse Position
  </div>
 </div>
</div>
<div>
 <div>
  <div>
   mouseX&nbsp;//&nbsp;마우스&nbsp;포인터의&nbsp;현재&nbsp;X&nbsp;좌표
   <b>mouseY&nbsp;//&nbsp;마우스&nbsp;포인터의&nbsp;현재&nbsp;Y&nbsp;좌표
   <b>pmouseX&nbsp;//&nbsp;마우스&nbsp;포인터의&nbsp;이전&nbsp;X&nbsp;좌표
   <b>pmouseY&nbsp;//&nbsp;마우스&nbsp;포인터의&nbsp;이전&nbsp;Y&nbsp;좌표
  </div>
 </div>
</div>
<div>
 <div>
  <div>
   mousePressed
  </div>
 </div>
</div>
<div>
 <p>마우스 클릭 감지 함수</p>
</div>
<div>
 <div>
  <div>
   void&nbsp;mousePressed()&nbsp;{
   <b>&nbsp;&nbsp;...
   <b>}
  </div>
 </div>
</div>
<div>
 <div>
  <div>
   Mause Parameter
  </div>
 </div>
</div>
<div>
 <div>
  <div>
   mouseMoved&nbsp;//&nbsp;마우스&nbsp;움직일&nbsp;때
   <b>mouseDragged&nbsp;//&nbsp;마우스&nbsp;드래그&nbsp;할&nbsp;때
   <b>mouseWheel&nbsp;//&nbsp;마우스&nbsp;휠&nbsp;움직일&nbsp;때
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
   keyPressed
  </div>
 </div>
</div>
<div>
 <p>키보드 입력 감지 함수이다.</p>
</div>
<div>
 <div>
  <div>
   void&nbsp;keyPressed()&nbsp;{
   <b>&nbsp;&nbsp;...
   <b>}
  </div>
 </div>
</div>
<div>
 <div>
  <div>
   KeyReleased
  </div>
 </div>
</div>
<div>
 <p>키보드가 띄어지면 실해되는 함수이다.</p>
</div>
<div>
 <div>
  <div>
   void&nbsp;keyReleased()&nbsp;{
   <b>&nbsp;&nbsp;...
   <b>}
  </div>
 </div>
</div>
<div>
 <div>
  <div>
   Keyboard Parameter
  </div>
 </div>
</div>
<div>
 <div>
  <div>
   keyPressed&nbsp;//&nbsp;키보드&nbsp;입력&nbsp;감지
   <b>key&nbsp;==&nbsp;''&nbsp;//&nbsp;키보드&nbsp;입력&nbsp;값&nbsp;저장&nbsp;변수
   <b>keyCode&nbsp;==&nbsp;"KEY"&nbsp;//&nbsp;Ctrl,&nbsp;Shift,&nbsp;Up,&nbsp;Down,&nbsp;Left,&nbsp;Right&nbsp;등&nbsp;특수키&nbsp;입력
   <b>//&nbsp;ex&nbsp;//&nbsp;keyCode&nbsp;==&nbsp;CONTROL
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
   Frame (FPS)
  </div>
 </div>
</div>
<div>
 <div>
  <div>
   frameCount&nbsp;//&nbsp;현재&nbsp;프레임&nbsp;번호
   <b>framerRate&nbsp;//&nbsp;초당&nbsp;프레임&nbsp;개수
  </div>
 </div>
</div>
<div>
 <p></p>
</div>