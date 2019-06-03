---
layout: post
title: '#11 알림 메세지 띄우기'
author: '미르'
categories: Android-App-Develop(Eclipse1)
tags:
- Android
- App
- Develop
- Eclipse
---


<script> location.href='https://cafe.naver.com/develoid/296849' ; </script>


















						<p>으어ㅠㅠㅠㅠㅠ</p><p>내일 개학이네요 ㅠㅠㅠ</p><p>어쩔수 없지만 빨리 강좌 하나 쓰고 자렵니다~</p><p>이제 밤늦게 폰을 할수 없다니 ㅠㅠㅠ으어ㅠㅠㅠ</p><p>방학이 끝나고 2학기가 시작되므로 이 강좌의 업로드 속도가 아주 늦어질수 있습니다</p><p><b></p><p><b><span>11. 알림 메세지 띄우기</span></b></p><p><span>11-1 알림 메세지란?</span></p><p>안드로이드 폰을 종료할때 나타나는 메세지</p><p>"기기를 종료하시겠습니까?"</p><p>"아니오" &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;"예"</p><p>이 문구를 한번쯤은 보신적이 있으실겁니다</p><p><b></p><p>이렇게 어플에서 알림메세지를 띄워 사용자의 대답을 입력받을수 있는대요</p><p>이번에는 이 코드를 알아보겠습니다</p><p><b></p><p>참고로 #11강좌부터는 xml을 건들이는 일이 적고 80%가 java에서 이루어 집니다</p><p><b></p><p><span>11-2 코드 미리보기</span></p><p>알림을 띄우는 코드를 확인해 보겠습니다</p><div><p>AlertDialog.Builder alert = new AlertDialog.Builder(this);</p><p>alert.setTitle(<span><u>"경고"</u></span>);</p><p>alert.setPositiveButton(<span><u>"확인"</u></span>, new DialogInterface.OnClickListener() {</p><p>&nbsp; &nbsp; @Override</p><p>&nbsp; &nbsp; public void onClick(DialogInterface dialog, int which) {</p><p>&nbsp; &nbsp;&nbsp;<span><u>dialog.dismiss();</u></span></p><p>&nbsp; &nbsp; }</p><p>});</p><p>alert.setMessage(<span><u>"내용"</u></span>);</p><p>alert.show();<b></p></div><p><b></p><p>위부터 setTitle은 알림의 제목을 지정하는 부분이죠?</p><p>setPositiveButton는 오른쪽에 위치하는 버튼을 설정하는 건대, 설정과 동시에 OnClickListener가 자리잡고 있습니다</p><p>즉 이 오른쪽 버튼을 누르면 어떤작업을 할꺼냐를 지정해 주는겁니다</p><p>아무 작업도 안시킬꺼라면 null을 주면 되는대요</p><p>alert.setNegativeButton("취소", null);</p><p>이런식으로 해주시면 됩니다</p><p><b></p><p>onClick메소드안에 있는&nbsp;dialog.dismiss();는 알림을 닫아주는 코드입니다</p><p>setMessage는 짐작하신바와 같이 알림안에 들어갈 내용을 지정해 주는 코드입니다</p><p><b></p><p>위에서는 큰따음표 "로 설정했지만 R.string으로도 가능하다는점 잊지마세요~</p><p><b></p><p>alert에서 설정할수 있는것은 다양합니다</p><p>setIcon</p><p>setNegativeButton</p><p>setNeutralButton</p><p>등등</p><p><b></p><p>컨드롤 + 스페이스로 뭐가 들어갈수 있는지 꼭 봐보세요</p><p><b></p><p><b></p><p>그럼 예제로 버튼을 클릭하면 알림이 뜨는 어플을 만들어 봅시다</p><p><b></p><p>activity_main.xml</p><div><p>&lt;Button</p><p>&nbsp; &nbsp; &nbsp; &nbsp; android:id="@+id/button1"</p><p>&nbsp; &nbsp; &nbsp; &nbsp; android:layout_width="wrap_content"</p><p>&nbsp; &nbsp; &nbsp; &nbsp; android:layout_height="wrap_content"</p><p>&nbsp; &nbsp; &nbsp; &nbsp; android:layout_centerHorizontal="true"</p><p>&nbsp; &nbsp; &nbsp; &nbsp; android:layout_centerVertical="true"</p><p>&nbsp; &nbsp; &nbsp; &nbsp; android:onClick="alert"</p><p>&nbsp; &nbsp; &nbsp; &nbsp; android:text="알림표시" /&gt;<b><span></span></p></div><p>버튼 하나만 지정하고 onClick줍시다</p><p><b></p><p>MainActivity.java</p><div><p>public void alert(View v){</p><p><span>  </span>AlertDialog.Builder alert = new AlertDialog.Builder(this);</p><p><span>  </span>alert.setTitle("알림!!");</p><p><span>  </span>alert.setPositiveButton("확인", new DialogInterface.OnClickListener() {</p><p><span>  </span>&nbsp;&nbsp; &nbsp;@Override</p><p><span>  </span>&nbsp;&nbsp; &nbsp;public void onClick(DialogInterface dialog, int which) {</p><p><span>  </span>&nbsp;&nbsp; &nbsp;<span> </span>Toast.makeText(MainActivity.this, "확인 버튼이 눌렸습니다",Toast.LENGTH_SHORT).show();</p><p><span>  </span>&nbsp;&nbsp; &nbsp;}</p><p><span>  </span>});</p><p><span>  </span>alert.setIcon(R.drawable.ic_launcher);</p><p><span>  </span>alert.setNegativeButton("취소", new DialogInterface.OnClickListener() {</p><p><span>  </span>&nbsp;&nbsp; &nbsp;@Override</p><p><span>  </span>&nbsp;&nbsp; &nbsp;public void onClick(DialogInterface dialog, int which) {</p><p><span>  </span>&nbsp;&nbsp; &nbsp;<span> </span>Toast.makeText(MainActivity.this, "취소 버튼이 눌렸습니다",Toast.LENGTH_SHORT).show();</p><p><span>  </span>&nbsp;&nbsp; &nbsp;}</p><p><span>  </span>});</p><p><span>  </span>alert.setMessage("안녕하십니까? 알림 예제소스 학습중 입니다");</p><p><span>  </span>alert.show();</p><p><span> </span>}</p></div><p>처음에 배운 예제랑 달라진것은&nbsp;NegativeButton이 추가되었고 setIcon을 지정하였다는 점입니다</p><p><b></p><p>여기까지 이해가 안될경우 다시 정독하시길 바랍니다</p><p>이해가 안된 상태에서 더이상 진행하지 마세요</p><p><b></p><p>그럼 실행 스샷을 확인해 보겠습니다</p><p>확인해야할 것은 아이콘지정과, 버튼 클릭시 나오는 토스트 메세지입니다</p><p><b></p><p><b></p><p><span><span><img src="https://dthumb-phinf.pstatic.net/?src=%22http%3A%2F%2Fcfile9.uf.tistory.com%2Fimage%2F211036375210B576175B1A%22&amp;type=cafe_wa740"></span></span></p><p>버튼을 누르면 이렇게 알림이 뜹니다</p><p><span><span><img src="https://dthumb-phinf.pstatic.net/?src=%22http%3A%2F%2Fcfile25.uf.tistory.com%2Fimage%2F261519375210B5763BDCEF%22&amp;type=cafe_wa740"></span></span></p><p>확인버튼을 누르면 위 메세지가,</p><p><span><span><img src="https://dthumb-phinf.pstatic.net/?src=%22http%3A%2F%2Fcfile2.uf.tistory.com%2Fimage%2F247758375210B57610019C%22&amp;type=cafe_wa740"></span></span></p><p>취소 버튼을 누르면 위 메세지가 나오게 됩니다<b></p><p><b></p><p>즉 코드가 정상 작동 한다는 뜻입니다 ㅎㅎ</p><p><b></p><p><b></p><p>알림도 토스트와 자주 사용하니 꼭 익히시길 바랍니다~</p><p><b></p><p><b></p><p><b></p><p></p><div><p><b></p><p>이글은 [http://whdghks913.tistory.com/315] 에서 다시 보실수 있으며 원본 글의 저작권은 미르에게 있습니다</p><p><b></p></div><p></p><p><b></p><p>예제소스는 원본글에서만 다운받을수 있습니다</p>