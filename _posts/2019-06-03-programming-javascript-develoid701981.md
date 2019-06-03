---
layout: post
title: '[13] 연산자 - 5.논리 연산자'
author: 'ㅎ엘로이ㅎ'
categories: Programming-JavaScript
tags:
- Programming
- Language
- JavaScript
-
---


<script> location.href='https://cafe.naver.com/develoid/701981' ; </script>


















						<p><strong><span>1. 논리곱 &amp;&amp; (AND 논리연산자)</span></strong></p><p><b></p><table width="671" height="40" bgcolor="#b7bbb5" border="0" cellspacing="1" cellpadding="1" style="color: rgb(32, 32, 32); font-family: &quot;994265_10&quot;; font-size: 13.3333px; line-height: 18.6667px;"><tbody><tr bgcolor="#ffffff"><td width="223" style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>좌변</span></p></td><td width="223" style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>우변&nbsp;</span></p></td><td width="223" style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>결과&nbsp;</span></p></td></tr><tr bgcolor="#ffffff"><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>true</span></p></td><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>true</span></p></td><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>true</span></p></td></tr><tr bgcolor="#ffffff"><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>true</span></p></td><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>false</span></p></td><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>false&nbsp;</span></p></td></tr><tr bgcolor="#ffffff"><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>false</span></p></td><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>true</span></p></td><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>false</span></p></td></tr><tr bgcolor="#ffffff"><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>false</span></p></td><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>false</span></p></td><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>false</span></p></td></tr></tbody></table><p><b></p><p><span>&amp;&amp; 연산자는 좌변의 값이 false값이면,우변의 값을 비교하지 않고 false값을 반환한다.</span></p><p><span>이와 같은 &amp;&amp;연산자의 특성을 이용하여 코드에서 if문을 대신하여 사용되기도 한다. 아래의&nbsp;두&nbsp;예제는 동일하게 실행된다.</span></p><p><b></p><p><span>ex)</span></p><p><span>var x = 10;</span></p><p><span>var y = 20;</span></p><p><span>if(x==y) {</span></p><p><span>&nbsp;&nbsp;&nbsp; myFun();</span><span>&nbsp;// x==y가 true일때만 함수가 실행된다</span></p><p><span>}</span></p><p><b></p><p><span>var x = 10;</span></p><p><span>var y = 20;</span></p><p><span>(x==y) &amp;&amp; myFun();&nbsp;</span><span>// x==y가 true일때만 함수가 실행된다</span></p><p><b></p><p><b></p><p><strong><span>2. 논리합 || (OR 논리연산자)</span></strong></p><p><b></p><table width="671" height="40" bgcolor="#b7bbb5" border="0" cellspacing="1" cellpadding="1" style="color: rgb(32, 32, 32); font-family: &quot;994265_10&quot;; font-size: 13.3333px; line-height: 18.6667px;"><tbody><tr bgcolor="#ffffff"><td width="223" style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>좌변</span></p></td><td width="223" style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>우변&nbsp;</span></p></td><td width="223" style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>결과&nbsp;</span></p></td></tr><tr bgcolor="#ffffff"><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>true</span></p></td><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>true</span></p></td><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>true</span></p></td></tr><tr bgcolor="#ffffff"><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>true</span></p></td><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>false</span></p></td><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>true</span></p></td></tr><tr bgcolor="#ffffff"><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>false</span></p></td><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>true</span></p></td><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>true</span></p></td></tr><tr bgcolor="#ffffff"><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>false</span></p></td><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>false</span></p></td><td style="font-family: 돋움, dotum, Helvetica, sans-serif; font-size: 10pt;"><p><span>false</span></p></td></tr></tbody></table><p><b></p><p><span>피연산자 값중 하나라도 true이면 true를 반환한다. 둘다 false이면 false를 반환한다.</span></p><p><span>|| 연산자는 좌변의 값이 true이면 우변의 값을 비교하지 않고 true값을 반환한다.</span></p><p><b></p><p><b></p><p><strong><span>3. ! (NOT 연산자)</span></strong></p><p><b></p><p><span>!는 단항 연산자로 피연산자 앞에 놓여 피연산자 불리언 값을 반전시킨다.</span></p><p><b></p><p><span>ex)</span></p><p><span>!true;&nbsp;</span><span>// false</span></p><p><span>!false;&nbsp;</span><span>// true</span></p><div><p><b></p></div><p></p>