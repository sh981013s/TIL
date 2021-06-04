# CSS
## 개념
html의 정보를 스타일이 좋게 표현하도록, **디자인** 을 지원하는 언어

html에서 stlye을 각 html파일에 만들면 유지보수하기 어렵다.

- style을 분리하여 css파일에 stle 태그의 본문을 css파일에 작성
- css파일의 경로를 html에서 head아래에 다음과 같이 적으면 css style이 적용

```
<link rel="stylesheet" type="text/css" href="<http://localhost:81/style.css">
//link하고 tab하여 자동완성
```
- cf. 크롬 플러그인 chrome extension stylebot을 이용하면 스타일을 실험적으로 디자인 가능.
    - 실험적이지만 stylebot을 저장하면 실제 웹페이지도 바뀜(자신의 로컬에서)
----------
#### html에서 스타일링을 통하는 세가지 방법
1. internal style 방식 \<head\> 태그 사이에 `<style>`태그로 주는 방법

2. external css 방식 : \<head\>태그 사이에 외부 경로 삽입

    `<link rel="stylesheet" type="text/css" url="외부css파일경로"\>`

3. inline style 방식 : html 마크업 자체에서 속성값 지정
    `<div style="background:#000; color:#fff;"></div>`
-------
## 문법
클래스 :  `.NAME {속성들}` : 앞에 쩜을 찍고 접근
아이디 : `#NAME {속성들}` :  앞에 #을 찍음
(아이디를 남발하기 보다는 클래스를 통하는 것이 좋음)
(아이디는 유일하기 때문에 접근이 개별적이지만, 클래스는 모든 엘리먼트에 대해 접근하기 때문)

jQeury에서 css를 사용할 때 문법을 비슷하게 적용 가능
`css`---`#header{ border : 4px solid #ff0000; }`
`jQuery`---`$("#header").css("border", "4px solid #ff0000")`

#### 선택자
 엘리먼트를 선택하는 기능.

|CSS|jQeury|설명|
|---|---|:---|
|*|$("*")|모든 엘리먼트 선택|
|#I|$("#I")|아이디가 I인 엘리먼트 선택|
|E|$("E")|태그 이름이 E인 모든 엘리먼트 선택|
|.C|$(".C")|C라는 클래스 선택자를 가진 모든 엘리먼트|
|E F|$("E F")|E의 자식 노드 중 태그 이름이 F인 모든 엘리먼트 선택|
|E.C|$("E.C")|태그 이름이 E인 엘리먼트중 C라는 클래스 선택자를 가진 모든 엘리먼트 선택|
|E .C|$("E .C")|E의 자식노드 중 C라는 클래스 선택자를 가진 모든 엘리먼트 선택|
|E>F|$("E>F")|E의 바로 아래 자식 태그 이름이 F인 모든 엘리먼트 선택|
---



## CSS 속성 분류
    - 뷰: 태그의 보여짐 여부 결정
        * display
        * opacity, visibility
        * z-index
    - 포지셔닝: 태그의 위치 결정
        * position
        * width, height
        * left, right, top, bottom
        * margin, padding
        * float
        * line-height
        * transform - translate
        * text-align
        * box-sizing
    - 데코레이션: 태그의 디테일한 디자인 결정
        * border
        * color, font-size
        * background, background-image, background-color
        * cursor