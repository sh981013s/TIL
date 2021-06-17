# 게시판 - 02. 게시판 만들기 - 2

![](https://images.velog.io/images/sh981013s/post/de435e5f-852b-4f5a-9afd-cb291399e0bf/image.png)

---

#### 글쓰기 기능을 알아보겠다.
#### 보드 리스트에서 코드를 따와서 board_write.html 을 먼저 만들었다.

![](https://images.velog.io/images/sh981013s/post/4afc4ce2-0870-4075-a0fc-e450f4e12596/image.png)

#### 보드의 폼도 작성을 해준다.
#### view 와 url 또한 필요하다.

![](https://images.velog.io/images/sh981013s/post/512d8b84-b049-4a78-8714-a789fe852f85/image.png)

#### views : 

![](https://images.velog.io/images/sh981013s/post/bf2f1277-f056-4c68-b2f0-b80fe955ac44/image.png)

#### urls :

![](https://images.velog.io/images/sh981013s/post/da16eb32-3fcb-4f30-a91f-f22b169dd680/image.png)

#### 결과 : 

![](https://images.velog.io/images/sh981013s/post/d4e44844-8030-4d3a-a88c-143a972015be/image.png)

#### 하지만 내용 부분을 textarea 로 수정해준다.

![](https://images.velog.io/images/sh981013s/post/5be5f67d-1a0b-48ee-84ac-5d185a5937bb/image.png)

#### 글을 쓸때 title 과 contents 입력되면 writer 까지 자동으로 pk 를 통해 저장되도록 작성하였다.

![](https://images.velog.io/images/sh981013s/post/497aad23-57e8-44c7-9d42-1f4ae4b90b36/image.png)

#### 본래는 상세보기 페이지로 넘어가야 하겠지만 우선은 없는채로 보드 리스트로 넘어가게끔 진행을 했다.
#### 글을 쓰면 리스트에 추가가 된 모습을 확인할 수 있다.

![](https://images.velog.io/images/sh981013s/post/1cdd9aba-76fc-4501-a44f-3b01b26b1099/image.png)

![](https://images.velog.io/images/sh981013s/post/d3d4a908-b295-4cfa-99a4-1da99bbd10f8/image.png)

#### 글 상세보기 페이지를 위하여 board_detail.html 페이지를 만들었다. readonly 옵션을 통하여 읽기전용으로 지정해주었고 value : 즉, 값은 컨트롤러를 만든 후에 넣어줄 예정이다.

![](https://images.velog.io/images/sh981013s/post/418e5e5b-c947-4617-8b18-de1e6a932ee7/image.png)

#### board/detail/x 값을 통해 pk 를 받은 후 해당 id 값의 글을 출력해야 하기 때문에 디테일 url 을 아래와 같이 수정해준다.

![](https://images.velog.io/images/sh981013s/post/1b424f6f-41d4-466a-bb17-e66a5b7c001f/image.png)

####  detail view 또한 pk를 사용하여 전당하는 식으로 전달을 해준다.

![](https://images.velog.io/images/sh981013s/post/971efb04-6911-4d2b-8978-bac0b283106e/image.png)

#### detail.html 에 받아온 값을 넣어준다.
#### 정상적으로 pk 값을 받은 주소로 아래와 같은 화면을 보여준다.

![](https://images.velog.io/images/sh981013s/post/acf66044-1961-47db-b059-b95e059792e7/image.png)

![](https://images.velog.io/images/sh981013s/post/3961d706-9a10-4f35-aa9c-e5cc580ba4d4/image.png)

