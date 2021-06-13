# MTV - 06. MTV의 T,V 만들기 (2) - 회원가입

![](https://images.velog.io/images/sh981013s/post/7e4efe72-9803-47db-b6c9-4bc76403f128/image.png)

---

#### 부트스트랩에서 가져온 코드의 id 값을 아래와 같이 변경한다.
#### 서버를 실행하면 다음과 같은 화면이 보인다.

![](https://images.velog.io/images/sh981013s/post/c352a925-1b02-4253-8395-0dabd136670a/image.png)

![](https://images.velog.io/images/sh981013s/post/f8760ba8-739b-4d70-8ee6-161c3a7bdb22/image.png)

#### 파라미터의 전송 방식에는 get 과 post 가 있는데, post 방식을 사용할 것이다.
#### 또한 꼭 폼안에다가 {% csrf_token %} 을 써준다. 이는, form 은 데이터를 서버에 전달을 해주는데, 안좋게 사용하는 사람들은 cross-domain 을 사용해 자신의 웹에서 따로 전달을 해주는 경우가 존재하는데, 토큰 키를 숨겨 놓음으로써 이를 방지한다.

![](https://images.velog.io/images/sh981013s/post/13b21140-2bca-4593-b35d-c62315077a5c/image.png)

#### 또한 name 을 하나의 'key'로 관리해야 하기 떄문에 name 속성값들 또한 추가해준다.

![](https://images.velog.io/images/sh981013s/post/2d6d055e-2717-465f-a4b3-00cea5d62b60/image.png)

#### 이제는 뷰 함수를 설정해주어야 하는데, 여기서 기존에 만들었던 register 함수가 해야할 일이 두가지로 늘어난다.

#### 하나는 주소를 입력해서 접근하는 상황이고, 두번째는 해당 페이지에서 '등록' 버튼을 눌러서 접근하는 상황이다.

![](https://images.velog.io/images/sh981013s/post/123b1cf0-4698-4c39-8db0-c74d00f31e18/image.png)

#### 그렇기에 우선 주소값을 쓰는 'GET' 방식과 
#### 등록을 누르는 폼의 'POST' 방식을 분리시킨다.
#### 하지만 등록을 누르면 회원가입이 되는 상황을 만들어야한다.

![](https://images.velog.io/images/sh981013s/post/31d55738-6159-4691-a6f1-955cf9499746/image.png)