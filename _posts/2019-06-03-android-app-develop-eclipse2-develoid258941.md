---
layout: post
title: '"아마도 쉬운 안드로이드 어플만들기" 3-1 글자가 화면에 나타나기까지의 과정'
author: 'Snails'
categories: Android-App-Develop(Eclipse2)
tags:
- Android
- App
- Develop
- Eclipse
---


<script> location.href='https://cafe.naver.com/develoid/258941' ; </script>


















						<p><img src="https://dthumb-phinf.pstatic.net/?src=%22http%3A%2F%2Fpostfiles3.naver.net%2F20130523_178%2Ftjdtnsu_1369283538974akCh1_JPEG%2Fand.jpg%3Ftype%3Dw2%22&amp;type=cafe_wa740"></p><p><i>퍼갈 때에는 반드시 저작자의 허락과 저작자의 이름(아이디)를 기록하어야 합니다.</i></p><p><i>저작자는 Snails(tjdtnsu)입니다.</i></p><p><u>참고 : 이 강좌는 초보자를 위한 Eclipse를 사용하였습니다.</u></p><p><u><strong>참고 : 이 강좌는 매주 일요일마다 업데이트합니다.</strong></u> (공휴일, 개인사정 등등 제외)</p><p><span><strong>개인강좌게시판을 득템하기 위하여</strong></span><span>&nbsp;</span></p><p>&nbsp;<u>﻿</u></p><p><b><span>학습목표 :&nbsp;프로젝트 글자출력의 과정을 이해할 수 있다.</span></b></p><p><b><span><span>난이도 : ★★</span></span></b>★</p><div>&nbsp;</div><div>네 이제는 대단원 3입니다.</div><div>대단원 2는 실습 위주면 3은 이론 위주입니다.</div><div>이번 대단원에서는 xml,java 파일을 분석해보는 시간을 갖도록 하겠습니다.</div><div>오늘은 간단하게 string.xml의 쓰임새를 배워보자 합니다.</div><div>&nbsp;</div><div>&nbsp;</div><div><img src="https://dthumb-phinf.pstatic.net/?src=%22http%3A%2F%2Fblogfiles.naver.net%2F20130609_151%2Ftjdtnsu_1370775832731ivCwO_PNG%2F%25C1%25A6%25B8%25F1_%25BE%25F8%25C0%25BD.png%22&amp;type=cafe_wa740"></div><div>프로젝트를 생성한 후 레이아웃을 열어보면</div><div>Hello world!라 적혀 있습니다.</div><div>&nbsp;</div><div>오늘은 이 글자가 출력되는 과정을 살펴 보겠습니다.</div><div>&nbsp;</div><div>&nbsp;</div><div>일단 이 그래프를 보면서 살펴보겠습니다.</div><div><div><img src="https://dthumb-phinf.pstatic.net/?src=%22http%3A%2F%2Fblogfiles.naver.net%2F20130609_85%2Ftjdtnsu_1370776857708IYYfV_PNG%2FScan06092013_201646.png%22&amp;type=cafe_wa740"></div></div><div>(실습중심 안드로이드 프로그래밍 책 중 한 그림을 발췌함을 알려드립니다.)</div><div>&nbsp;</div><div>뭐 이렇게 과정을 걸쳐 온다는 것을 알 수 있습니다.</div><div>그리면 이것도 응용을 할 수 있겠군요.</div><div>&nbsp;</div><div>res-values-string.xml-string.xml파일로 갑니다.</div><div><img src="https://dthumb-phinf.pstatic.net/?src=%22http%3A%2F%2Fblogfiles.naver.net%2F20130609_39%2Ftjdtnsu_1370777245922JgN7o_PNG%2FScan06092013_201646.png%22&amp;type=cafe_wa740"></div><div>&nbsp;</div><div>위에 무슨 말인지 알겠죠?<b>app_name은 'aaaaaeb'고</div><div>그 밑에 <span>&lt;string name="hello_world"&gt;Hello world!&lt;/string&gt;</span> 이 우리가 찾는 줄입니다.</div><div>이것의 'Hello world!'를 'Bye world!'로 고쳐줍니다.</div><div>&nbsp;</div><div>&nbsp;</div><div>그리고 activity_main.xml로 와서 확인합니다.</div><div><img src="https://dthumb-phinf.pstatic.net/?src=%22http%3A%2F%2Fblogfiles.naver.net%2F20130609_44%2Ftjdtnsu_13707774564616QWhM_PNG%2FScan06092013_201646.png%22&amp;type=cafe_wa740"></div><div>자 잘 수정이 되었군요.</div><div>여기서 설명 들어갑니다.</div><div>&nbsp;</div><div>string.xml은 프로젝트 내 사용될 문자열을 미리 등록해두는 것입니다.</div><div>이러면 동일한 문자열을 사용할 경우 매우 편리해집니다.</div><div>뭐 100글자적을 거 10글자만 적으면 된다 라고 생각하시면 됩니다.</div><div>&nbsp;</div><div>&nbsp;</div><div>참고 : R.java 파일은 프로그래머는 거의 손대지 않습니다. 그냥 보는 건데요, 프로젝트에서 R.java를 습관적으로 확인을 하는 것이 좋다고 합니다.(왜?)<b></div><div>&nbsp;</div><div>응용숙제 : @string을 하나 더 생성해서 Bye world 밑줄에 'It was fack!'를 출력해 보시오.</div><div>&nbsp;</div><div>&nbsp;</div><div>다음 강좌에는 매니페스트를 살펴보겠습니다.</div><p></p><p>&nbsp;</p><p></p>