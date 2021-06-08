## 반응형 디자인과 미디어쿼리 소개

<br>

#### 화면의 크기에 따라 웹페이지의 각 요소들이 최적화된 크기로 바뀌는 페이지가
#### '반응형 디자인', 영어로는 'responsive web' 이라고 부른다.
<br>
<br>

#### 예시를 보기위해, 화면의 크기에 따라 보였다, 보이지 않았다 하는 페이지를 만든다
<br>

#### 우선적으로 확인하기 위해 하나의 평범한 div를 만든다.

![](https://images.velog.io/images/sh981013s/post/9e4c7868-e0bc-4b19-900b-dc2f5f197701/image.png)

<br>

#### 기준점이 되는 숫자에 따라 반응하게 하려면 우선 보는 화면의 '크기' 를 알아야 하는데 그에대해서는 구글크롬의 'inspect' 기능을 사용하면 된다. 
#### inspect 상태에서 화면을 줄이고 늘이면 우측상단에 사이즈가 표기된다.

![](https://images.velog.io/images/sh981013s/post/401e0d6e-2098-4bf3-8c92-4031f9dc1e61/image.png)

#### 구성하고자 하는 상황은 스크린의 크기가 800px 보다 크다면, div 자체를 보이지 않게 하고 싶다.

![](https://images.velog.io/images/sh981013s/post/6061392d-3937-4563-8820-0077a1ac7531/image.png)

#### 이를 미디어 쿼리를 사용해야 하는데, 이렇게 사용할 수 있다.

![](https://images.velog.io/images/sh981013s/post/c040e35f-a55a-4f34-af79-1fd1dc429504/image.png)

#### 사용한다면, 아래의 사진과 같이 width 가 757px 일때는 생성한 div 가 정상적으로 비추어진다. 

![](https://images.velog.io/images/sh981013s/post/3d6738aa-4299-44c9-894d-c482b1f6932d/image.png)

#### 하지만, 800px 이 넘어가면 "display:none;" 을 통하여 보여지지 않는다.

![](https://images.velog.io/images/sh981013s/post/e1fa5602-0ad9-4b07-a205-4cb1eb9c8730/image.png)

#### 반대로, 800px 보다 작을때 "display:none;" 을 하려면 <br>아래와 같이 'max-width : x" 를 사용하면 된다.

![](https://images.velog.io/images/sh981013s/post/a7241e76-03d8-4e46-9819-a42dfffa8c81/image.png)

---

참고 : https://opentutorials.org/course/3086/18323



