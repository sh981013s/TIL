# 로그인 - 03. 로그인 만들기 - 2

![](https://images.velog.io/images/sh981013s/post/da447a87-6aae-4422-b5cf-0c63edf50fb7/image.png)

---

#### 로그인 만들기를 진행할때 redirect 라는 함수를 사용할것인데, redirect 는 django.shortcuts 안에 있다.

![](https://images.velog.io/images/sh981013s/post/674de75d-d009-48e1-abbf-794e9d45d7f6/image.png)

#### redirect 는 return redirect 로 쓰게 되는데, 예시로 이런식으로 사용한다면 비밀번호가 일치한다면 네이버로 이동하게 된다.

![](https://images.velog.io/images/sh981013s/post/c7371a77-7c49-4e19-ae6e-4e4a5e43ba4a/image.png)

#### 일반적으로는 이렇게 쓴느데, '/' 라고 하면 home 으로 가게된다.

![](https://images.velog.io/images/sh981013s/post/9ff98ec6-989e-4ca6-b685-a7a0730c1767/image.png)

#### request 안에 session 이라는 함수가 존재하는데, 딕셔너리 함수를 사용하듯이 'user' 라는 키에다가 fcuser.id 를 넣게되면 방금 로그인한 user 의 id 값을 할당한 것이다.

![](https://images.velog.io/images/sh981013s/post/3311be0a-6567-4301-8841-dc85a9b7cd55/image.png)

#### fcuser 가 아닌 전체의 url 18줄과 같이 import를 해주고  에 home 이라는 주소를 맵핑 시켜준다
#### 물론 지금 서버를 가동시키면 home 이라는 함수를 만들지 않았기에 에러가 난다.

![](https://images.velog.io/images/sh981013s/post/c3904860-8336-4e14-a340-bd467e4db084/image.png)

#### 정삭적으로 작동하는지 확인을 하려고 우선 HttpResponse를 이용해 출력을 해본다.
#### 정상적으로 맵핑이 된 모습을 확인할 수 있다.

![](https://images.velog.io/images/sh981013s/post/e74b6a2a-918c-4b9a-a3d9-95a0b64547ea/image.png)

![](https://images.velog.io/images/sh981013s/post/5d0e626f-4236-433f-a244-9123b7281bd7/image.png)

#### 로그인이 정상적으로 됬는지 확인해 보기 위해서 홈화면을 바꾸어보겠다.
#### 아래와 같이 session을 이용하여 로그인이 됬다면 username을 출력하도록 바꾸어보았다.
#### 로그인을 했더니 아래와 같은 화면이 보인다.

![](https://images.velog.io/images/sh981013s/post/c9671ddc-5106-4bfb-8b4c-4d08f590405b/image.png)

![](https://images.velog.io/images/sh981013s/post/d521486a-a73a-4bab-bc4c-179565890394/image.png)

#### 로그아웃 함수는 반대로, session 이 있으면 삭제 해주면 된다.

![](https://images.velog.io/images/sh981013s/post/fa84f0bb-6218-4876-ad37-2cb64df0814f/image.png)

![](https://images.velog.io/images/sh981013s/post/9158559a-2bcb-40f0-92ce-6f50f72b92c3/image.png)