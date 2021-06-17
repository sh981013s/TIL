# 게시판 - 03. 게시판 만들기 - 3 - 예외처리

![](https://images.velog.io/images/sh981013s/post/c5c6c259-e973-491c-8188-c8920c54df84/image.png)

---

#### 로그인을 할때 잘못된 정보를 입력하게 되면 아래와 같은 화면을 보여주기 때문에 예외처리를 해주어야 한다.

![](https://images.velog.io/images/sh981013s/post/f2e92663-8583-4253-865f-4b16e131d030/image.png)

#### DoesNotExist 를 사용하여 try, except 로 예외처리를 해주었다.

![](https://images.velog.io/images/sh981013s/post/86993363-b0ee-417c-8462-75e5b7ae7657/image.png)

#### 게시물도 '주소 pk 에 대응하는 게시글이 없다면' 에 대응하기 위해 404 를 사용한다.

![](https://images.velog.io/images/sh981013s/post/08177fc9-14a2-4621-a51b-3cf823776246/image.png)

![](https://images.velog.io/images/sh981013s/post/40666212-d656-4a04-b2b3-75e11fc69094/image.png)

#### 게시물 쓰기 또한 로그인을 하지 않은 사용자가 글을 쓰게되면 에러가 나기 때문에 접속 자체를 막아야한다.
#### request session 에 유저가 없으면 로그인으로 리다이렉트 되게 해주었다.

![](https://images.velog.io/images/sh981013s/post/3171205a-ff93-4237-a3dc-b485b6e1c788/image.png)

