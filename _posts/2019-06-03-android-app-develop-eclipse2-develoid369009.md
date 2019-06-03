---
layout: post
title: '"아마도 쉬운 안드로이드 어플만들기" [39] 일시정지(Delay)'
author: '달팽이들'
categories: Android-App-Develop(Eclipse2)
tags:
- Android
- App
- Develop
- Eclipse
---


<script> location.href='https://cafe.naver.com/develoid/369009' ; </script>


















						<p>&nbsp;<img src="https://dthumb-phinf.pstatic.net/?src=%22http%3A%2F%2Fpostfiles3.naver.net%2F20130523_178%2Ftjdtnsu_1369283538974akCh1_JPEG%2Fand.jpg%3Ftype%3Dw2%22&amp;type=cafe_wa740"> </p><div><div><div><div><p><i>퍼갈 때에는 반드시 저작자의 허락과 저작자의 이름(아이디)를 기록하어야 합니다.</i></p><p><i>저작자는 Snails(tjdtnsu)입니다.</i></p><p><span><strong><span>제발 덧글 좀 적어주세요. 강의 적는 시간은 1시간이지만 덧글은 1분도 걸리지 않습니다.</span></strong></span></p><p><u>참고 : 이 강좌는 초보자를 위한 Eclipse를 사용하였습니다.</u></p><p><u>올리는 곳 : 제 네이버 블로그, 디벨로이드 카페</u> </p><div><span><u><strong>업로드 시간 :&nbsp;매달 2,4주 오후 11시</strong></u> <div></div><p>&nbsp;<strong><span>난이도 : ★</span><span>★★</span></strong></p></span></div><p></p><p></p></div></div></div></div><p>&nbsp;</p><p>&nbsp;</p><p>네, 오늘은 딴 걸 하겠습니다.</p><p>액티비티, 스레드 등을 일시정지하게 할 수 있을까요?</p><p>&nbsp;</p><p>네, 얼마만큼 아무 작업도 안 하게 할 수 있습니다.</p><p>&nbsp;</p><p>일반적으로 C언어에서 sleep이라는 걸 배웠죠</p><p>이것도 스레드에서는 sleep을 씁니다.</p><p>&nbsp;</p><p>하지만, 액티비티 코드에서는 sleep이 통하지 않습니다.</p><p>그러면 어떻게 해야 할까요?</p><div><table style="BORDER-BOTTOM-WIDTH: 0px; BORDER-TOP: #cccccc 1px solid; BORDER-LEFT-WIDTH: 0px; BORDER-RIGHT: #cccccc 1px solid" class="__se_tbl" border="0" cellspacing="0" cellpadding="0"><tbody><tr><td style="BORDER-BOTTOM: #cccccc 1px solid; BORDER-LEFT: #cccccc 1px solid; BORDER-RIGHT-WIDTH: 0px; BACKGROUND-COLOR: #ffffff; BORDER-TOP-WIDTH: 0px" width="741"><p><span>...</span></p><p><span>final Handler handler = new Handler();<b>handler.postDelayed(new Runnable() {<b>&nbsp;@Override<b>&nbsp;public void run() {<b>&nbsp; m.setText("Ang!");&nbsp; //여기에 실행될 코드를</span></p><p><span>&nbsp; }<b>}, 1000); //1000은 1초</span></p><p><span>...</span></p></td></tr></tbody></table></div><p>&nbsp;</p><p>이렇게 된다 합니다.</p><p>정말 이건 할 게 없습니다.</p><p>포스팅 할 것도 없으므로</p><p>예제만 한번 주고, 끝내겠습니다.</p><p>(제 미완성 앱중 하나 자동 액티비티 이동 코드, MainActivity.java)</p><table style="BORDER-BOTTOM: 0px; BORDER-LEFT: 0px; BORDER-TOP: #cccccc 1px solid; BORDER-RIGHT: #cccccc 1px solid" class="__se_tbl" border="0" cellspacing="0" cellpadding="0"><tbody><tr><td style="BORDER-BOTTOM: #cccccc 1px solid; BORDER-LEFT: #cccccc 1px solid; BACKGROUND-COLOR: #ffffff; BORDER-TOP: 0px; BORDER-RIGHT: 0px" width="741"><p>&nbsp;package com.naver.j;</p><p><b>import android.app.Activity;<b>import android.content.Intent;<b>import android.os.Bundle;<b>import android.os.Handler;<b>import android.view.Menu;</p><p>public class MainActivity extends Activity {</p><p>&nbsp;@Override<b>&nbsp;protected void onCreate(Bundle savedInstanceState) {<b>&nbsp;&nbsp;super.onCreate(savedInstanceState);<b>&nbsp;&nbsp;setContentView(R.layout.activity_main);<b>&nbsp;&nbsp;Handler mHandler = new Handler();<b>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; mHandler.postDelayed(new Runnable() {<b>&nbsp;&nbsp;public void run()<b>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; {<b>&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;Intent main_intro = new Intent(MainActivity.this,SelectActivity.class);<b>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; startActivity(main_intro);<b>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; finish();&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <b>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }<b>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }, 3000);<b>&nbsp;}</p><p>&nbsp;@Override<b>&nbsp;public boolean onCreateOptionsMenu(Menu menu) {<b>&nbsp;&nbsp;// Inflate the menu; this adds items to the action bar if it is present.<b>&nbsp;&nbsp;getMenuInflater().inflate(R.menu.main, menu);<b>&nbsp;&nbsp;return true;<b>&nbsp;}</p><p>}&nbsp;</p></td></tr></tbody></table><p>&nbsp;</p><p>&nbsp;</p><p>&nbsp;</p><div><iframe frameborder="0" scrolling="no" name="mplayer" title="플레이어" width="720" height="405" src="https://serviceapi.nmv.naver.com/view/ugcPlayer.nhn?vid=E9E22E96ACAF39AD7906258F3043A7F03459&amp;inKey=V12140ad1ec08bf1fe8c8338657ee98c82b52d1b36008d6f591745466a8f7e2af9530338657ee98c82b52&amp;wmode=opaque&amp;hasLink=1&amp;autoPlay=false&amp;beginTime=0" allowfullscreen="allowfullscreen"></iframe></div><p>&nbsp;</p><p>영상입니다.</p><p>&nbsp;</p><p>&nbsp;</p><p>다음 시간부터는 대단원 중단원 형식이 아니라</p><p>번호로 붙여 나가도록 하겠습니다.</p><p>&nbsp;</p><p>&nbsp;</p>