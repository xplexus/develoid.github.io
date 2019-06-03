---
layout: post
title: '[08] 표현식'
author: 'ㅎ엘로이ㅎ'
categories: Programming-JavaScript
tags:
- Programming
- Language
- JavaScript
-
---


<script> location.href='https://cafe.naver.com/develoid/701829' ; </script>


















						<b><span>Overview</span></b><div><b></div><div><span>자바스크립트의 표현식은 인터프리터를 통해 값으로 평가되거나 값을 반환하는(연산자,함수호출) 자바스크립트의 구문이다. (인터프리터 : 원시언어로 쓰여진 문장 하나씩 읽어서 기계어로 변환하여 실행하는 방식)</span></div><div><b></div><div><b></div><div><b><span>1. 원시 표현식</span></b></div><div><b></div><div><span>상수나 변수 참조, 예약어(키워드) 같은 다른 표현식을 포함하지 않는 간단한 표현식을 말한다.</span></div><div><b></div><div><span><strong>① 상수(리터럴)</strong></span></div><div><span><b></span></div><div><span>10&nbsp;<span>// 숫자상수</span></span></div><div><span>1.2&nbsp;<span>// 숫자 상수</span></span></div><div><span>"zeroDay"&nbsp;<span>// 문자열 상수</span></span></div><div><span>'jjdev'&nbsp;<span>// 문자열 상수</span></span></div><div><b></div><div><span><strong>② 예약어(키워드)</strong></span></div><div><span></span><b></div><div><span>true</span></div><div><span>false</span></div><div><span>null</span></div><div><span>this&nbsp;<span>// 현재 객체를 나타내는 예약어</span></span></div><div><b></div><div><span><strong>③ 변수</strong></span></div><div><span></span><b></div><div><span>x</span></div><div><span>undifined&nbsp;<span>// 아무값도 아님을 나타내는 전역변수</span></span></div><div><b></div><div><b></div><div><b><span>2. 복합표현식</span></b></div><div><b></div><div><span>배열, 객체, 함수등 &nbsp;원시 표현식의 결합된 형태나 연산자를 사용하여 결합되는 표현을 말한다.&nbsp;</span></div><div><span><b></span></div><div><span><strong>① 배열 표현식</strong>&nbsp;: 대괄호안에 쉼표로 구분한다.</span></div><div><span><b></span></div><div><span>[]</span></div><div><span>[1,2,3]</span></div><div><span>["zeroday", "jjdev"]</span></div><div><span>[[1,2,3],[4,5,6]]</span></div><div><span>[1,,,3]&nbsp;<span>// 두개의 값은 초기화 되진 않은 형태로 배열의 길이는(lenght) 4이다</span></span></div><div><span><b></span></div><div><span><strong>② 객체 표현식</strong>&nbsp;: 중괄호 안에 속성(프로퍼티) 이름과 콜론(:)을 사용하고 속성의 구분에는 쉼표를 사용한다.</span></div><div><span><b></span></div><div><span>{}</span></div><div><span>{x:1 , y:2}</span></div><div><span>{h{left:1,right:2}, v{top:1, bottom:2}}</span><span>&nbsp;// 객체의 중첩</span></div><div><b></div><div><span><strong>③ 함수 표현식</strong>&nbsp;: function 키워드와 괄호(쉼표로 구분한 매개변수 목록), 중괄호(자바스크립트 코드)로 표현한다.</span></div><div><span><b></span></div><div><span>function(x,y) {return x+y;}&nbsp;</span><span>// 입력받은 두개의 인자(매객변수 값)의 합을 리턴한다</span></div><div><b></div><div><span><strong>④ 함수 호출 표현식</strong>&nbsp;: 함수를 호출(실행시키는)하는 문법, 함수이름과 괄호(인자 목록)를 연결하여 표현, 함수가 리턴값을 반환하지 않는 경우는 표현값이 undefined가 된다.</span></div><div><span><b></span></div><div><span>f(0)</span></div><div><span>add(1,2)</span></div><div><span><b></span></div><div><span><strong>⑤ 객체의 속성(프로퍼티) 접근 표현식</strong>&nbsp;: 점(.)이나 대괄호([])를 사용하여 속성을 접근한다.</span></div><div><span><b></span></div><div><span><span>// 예제 객체 선언</span></span></div><div><span>&nbsp;var obj = {</span></div><b><span>age : 20,</span></blockquote><b><span>name : jjdev</span><span>,</span></blockquote><b><span>hobby : ["여행","독서"],</span></blockquote><b><span>move : function(){alert("move...")}</span></blockquote><div><span>}</span></div><div><span><span>// 속성 접근 표현식</span></span></div><div><span>obj.age</span><span>&nbsp;// 20</span></div><div><span>obj["age"]&nbsp;</span><span>// 20</span></div><div><span>obj.name&nbsp;</span><span>// jjdev</span></div><div><span>obj.hobby[0]&nbsp;</span><span>// 여행</span></div><div><span>obj.move()</span></div><div><b></div><div><span><strong>⑥ 객체 생성 표현식</strong>&nbsp;: new키워드와 생성자 함수를 사용하여 객체를 생성하고 속성을 초기화 한다.</span></div><div><span><b></span></div><div><span>new Object()</span></div><div><span>new Person("jjdev",20)</span></div><div><b></div><div><span>⑦ 연산자 표현식 : 복합 표현식을 만드는 가장 쉬원 방법은 연산자를 사용하는 것이다. 한개 이상의 피연산자들의 값들을 결합하여 새로운 값을 반환한다. 연산자들에 대한 자세한 설명은 다음장에 다룬다.</span></div><div><span><b></span></div><div><span>1+2</span></div><div><span>x*y&nbsp;</span><span>// *는 곱하기 연산자다<div><p><b></p></div></span></div>