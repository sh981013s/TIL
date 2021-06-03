#### html 기본 태그 정리

1. 제목 

   &lt;h1>글자&lt;/h1&gt; : h1 ~ h6까지 있음. 

   + 예시

     <h1>h1</h1>

     <h2>h2</h2>

     <h6>h6</h6>

2. 링크 

   &lt;a href = "URL"&gt; 깃허브주소로이동&lt;/a&gt;

   + 예시

     <a href="www.github">깃허브주소로이동</a> 

3. 강조

   &lt;em&gt;글자&lt;em&gt;

   + 예시

     <em>em태그</em>

   &lt;strong&gt;글자&lt;/strong&gt;

   + 예시

     <strong>strong태그</strong>

4. 가로 선

   &lt;hr&gt;

   + 예시

     <hr>

5. 단락 설정

   &lt;p&gt;문자열&lt;/p&gt;

6. 굵은 글꼴

   &lt;b&gt;문자열&lt;/p&gt;

   + 예시

   ​	<b>b태그</b>

7. 밑줄

   &lt;u&gt;문자열&lt;/u&gt;

   + 예시

     <u>u태그</u>

8. 개행

   &lt;br&gt;

9. 이미지

   &lt;img src="그림 파일명"&gt;

10. 목록

    + &lt;ul&gt; : 번호 부여 x

      &lt;li&gt; 1 &lt;/li&gt;

      &lt;li&gt; 2 /li&gt;

      &lt;/ul&gt;

      예시

      <ul>

      <li>1</li>

      <li>2</li>

      </ul>

    + &lt;ol&gt; : 번호 부여 o

      &lt;li&gt; 1 </li&gt;

      &lt;li&gt; 2 </li&gt;

      &lt;/ol&gt;

      예시

      <ol>

      <li>1</li>

      <li>2</li>

      </ol>

11. 특수 기호 (' '사이 공백 제거해야함)

    + '& amp;' : &amp;
    + '& lt;' : &lt;
    + '& gt;' : &gt;
    + '& quo;' : "
    + '& nbsp;' : 공백

12. 표 작성하기

    + 테이블 시작과 끝 태그 : &lt;table&gt; &lt;/table&gt;

    + 행 태그 tr(table row) : &lt;tr&gt; &lt;/tr&gt;

    + 셀 태그 td(table data) : &lt;td&gt;내용&lt;/td&gt;

    + 예시

      <table&gt;

       &lt;tr&gt; &lt;td&gt;1행1셀&lt;/td&gt; &lt;td&gt;1행2셀&lt;/td&gt;&lt;/tr&gt;

       &lt;tr&gt; &lt;td&gt;2행1셀&lt;/td&gt; &lt;td&gt;2행2셀&lt;/td&gt;&lt;/tr&gt;

       &lt;/table&gt;

      <table>

      <tr><td>1행1셀</td><td>1행1셀</td></tr>

      <tr><td>2행1셀</td><td>2행2셀</td></tr>

      </table>

    + 기타 기능

      + 표 테두리 굵기 

        예시 

        &lt;table border="1"&gt;

      + 표 크기

        예시

        &lt;table width="150"&gt;

      + 표의 셀 간격

        예시

        &lt;table cellspacing="10"&gt;

      + 표의 여백

        예시

        &lt;table cellpadding="10"&gt;

      + 표의 셀 병합

        예시

        &lt;td colspan="2"&gt; : 2개의 셀을 가로로 병합

        &lt;td rowspan="2"&gt; : 2개의 셀을 세로로 병합

      + 표 위의 제목

        예시

        &lt;table&gt; 

        &lt;caption&gt; 표 제목 &lt;caption&gt;

        &lt;table&gt;