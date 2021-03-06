<img src="https://swhackathon.com//image/main.png"></img>
## <a href="https://swhackathon.com/Team/Info/41">프로젝트 <strong>Polaris</strong>:북극성</a>

![preview](./image/preview.png)

## 데모영상
[![AppDemo](https://img.youtube.com/vi/f-8SmoucINY/maxresdefault.jpg)](https://youtu.be/f-8SmoucINY)

## 프로젝트 컨셉
<p align="center">
  우리에게 가장 친숙한 별, <strong>북극성</strong><br>
<br>
작은곰자리의 알파별<br>
북두칠성이 가리키고있는 별,<br>
  <strong>북극성</strong>은 아주 오랜 옛날부터 항해자와 여행자에게 <br>
방향을 알려주는 길잡이 역할을 해왔습니다.<br>
  <strong>북극성</strong>을 찾는다면 전세계 그 어디든 자신의 위치를 알수 있다고 하죠.<br>
<br>
  이런 <strong>북극성</strong>이 처음으로 우리에게 길잡이 역할을 하게 된 것은<br>
그 옛날, 몽골의 유목민들에게서부터 시작됩니다.<br>
방향을 잃기 쉬울만큼 드넓은 몽골의 초원에서<br>
  유목민들은 밤하늘의 길잡이인 <strong>북극성</strong>을 바라보며 이동했습니다.<br>
<br>
혹독한 환경 속에서 끊임없이 이동하고 이동하며<br>
한 곳에 정착한 삶을 살 수밖에 없었던 유목민들에게는<br>
  <strong>북극성</strong>은 방향을 알려주는 나침반 뿐만아니라<br>
곁에서 항상 지켜주는 친구이자 보호자 역할을 해주었죠.<br>
<br>
그들은 저마다 자신만의 나침반을 가슴에 담고 있습니다.<br>
</p>



## 프로젝트 개발 동기
<dl>
  <dd>
  코로나로 인해 비대면 사회가 되었습니다.<br>
  코로나가 언제 종식 될지는 모르지만, <br>
  현재 뉴딜정책을 펼치는 것으로 보아 <br>
  코로나가 끝이나도 많은 산업이 비대면화 될 것으로 예상됩니다.<br>
  비대면화된 사회로 인해 사람들은 혼자있는 시간이 늘어났습니다.<br>
  혼자있는 시간을 이용하여<br>
  사람들이 자신에 대해서 한번쯤 생각해 보는 것이 좋겠다고 생각했습니다.<br>
  </dd>
</dl>

## 프로젝트 개발환경
* 개발 툴<br>
  <a href="https://developer.android.com/studio"><img src=https://img.shields.io/badge/AndroidStudio-4.1.2-blue></img></a>
* 안드로이드 버전<br>
   <a href="https://github.com/chaejina/polystar"><img src=https://img.shields.io/badge/Android-8.1-green></img></a> 
* 에뮬레이터 테스트 기종<br>
   <a href="https://github.com/chaejina/polystar"><img src=https://img.shields.io/badge/Pixel%202%20API%2027-Run-sucess></img></a>

## 프로젝트 Activity 흐름도
  * 로그인 안되어있을 시<br>
    + IntroActivity ->  JoinActivity -> Guide Acitivity (3개) -> MainActivity & 내부순환<br><br>
  
  * 로그인이 되어있을 시<br>
    + IntroActivity ->  MainActivity & 내부순환<br><br>
  
  * Guide Activity (3개)<br>
    + StarQuestionActivity2 -> StarQuestionActivity3 -> StarQuestionActivity4<br><br>
  
  * MainActivity & 내부순환: 홈버튼을 누르면 아래의 순서대로 화면이 전환됩니다.<br>
    + MainActivity -> MainActivity2 -> MainActivity3 -> MainActivity4 -> MainActivity5 ->  MainActivity -><br>
            ↓<br>
    + APP 하단 네비게이션바: 홈, 별의기억, 별자리, 즐겨찾기<br><br>


     + 공통사항<br>
          - 별의기억, 별자리, 즐겨찾기에서 뒤로가기 선택 시 MainActivity로, 프로필 선택 시 StraActivity로 이동합니다.<br><br>
        
     + 홈: MainActivity  <br>
          - 내부순환 중에도 MainActivity로 돌아옵니다.<br>
          - 뒤로가기 선택 시 MainAtivity로 이동합니다.<br><br>
           
     + 별의기억: CalanderActivity </img><br>
          - 선택한 날짜에 답한 답변을 볼 수 있습니다.<br>
          - 뒤로가기 선택 시 MainAtivity로 이동합니다.<br>
          - 프로필 선택 시 StarActivity로 이동합니다.<br><br>
                
     + 별자리: StraActivity </img><br>
          - 획득한 별자리를 볼 수 있습니다.<br>
          - 프로필에서 사진을 변경할 수 있습니다.<br>
          - 기존 5개는 활성화상태로 고정, 그 중 3개는 세부페이지 StarInfoActivity, StarInfoActivity2, StarInfoActivity3로 이동됩니다.<br>
          - StarInfoActivity, StarInfoActivity2, StarInfoActivity3 에서 뒤로가기 선택시  StarActivity로 이동합니다.<br><br>
                                       
     + 즐겨찾기: BookmarkActivity <br>
          - 전체 질문 중 1개를 선택하여 답변을 볼 수 있습니다.<br>
          - 질문 선택 시 답변 페이지: OutputAcitvity로 이동합니다.<br>
          - Output Activity에서 뒤로가기는 BookmarkActivity로 이동합니다.<br>
          - 답변 연동 미구현<br><br>
                
     + 상단 달 또는 별자리 아이콘: InputActivity로 이동합니다.<br>
          - 선택 시 질문이 나오고 답변을 입력합니다.<br>
          - 완료를 선택 시 답변이 저장됩니다.<br>
          - 질문 새로고침 선택 시 질문이 변경됩니다.<br><br>
                
# 팀 구성원
  |역할|분야|학교|이름|
  |---|---|---|---|
  |팀장|SW개발|<a href = "http://sw.anu.ac.kr/"><img src="https://swhackathon.com/image/university_24.png"></a>|김채연|
  |팀원|SW개발|<a href = "http://sw.cu.ac.kr/"><img src="https://swhackathon.com/image/university_10.png"></a>|이단경|
  |팀원|SW개발|<a href = "http://tusw.tu.ac.kr"><img src="https://swhackathon.com/image/university_12.png"></a>|김현호|
  |팀원|SW개발|<a href = "http://computer.hanyang.ac.kr/"><img src="https://swhackathon.com/image/university_39.png"></a>|강태연|
  |팀원|디자인|<a href = "https://aisw.dongseo.ac.kr/main/main.html"><img src="https://swhackathon.com/image/university_13.png"></a>|권민재|
