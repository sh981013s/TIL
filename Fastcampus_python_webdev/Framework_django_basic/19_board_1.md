# 게시판 - 01. 게시판 만들기 - 1

![](https://images.velog.io/images/sh981013s/post/158d41b0-e5bf-4ee9-9d1f-12612e912e36/image.png)

---

#### board 라는 게시판 앱을 만든뒤에 templates 안에 일전에 만든 base.html 을 복사해준다.


![](https://images.velog.io/images/sh981013s/post/c8cc0712-1168-4e63-b446-b124705d3818/image.png)

#### board_list.html 생성 후 기본적인 틀을 잡아준다.

![](https://images.velog.io/images/sh981013s/post/355c98b2-0235-4a46-b954-3bdb8901973a/image.png)

#### 프로젝트 url 에 보드를 연결해준다.

![](https://images.velog.io/images/sh981013s/post/a8a741ff-4dc2-421c-befe-adabc29759c5/image.png)

#### 보드 앱 내부에 url.py 를 만들고 수정해준다.

![](https://images.velog.io/images/sh981013s/post/b31d81a9-b4b9-49d8-99ec-afa64ce6d0f8/image.png)

#### 뷰에서 보드 리스트 함수를 만들어준다.

![](https://images.velog.io/images/sh981013s/post/da8ba329-e8bc-4a56-b134-7b20246e2390/image.png)

#### 이런식으로 화면이 정상적으로 나온다.

![](https://images.velog.io/images/sh981013s/post/a43a21aa-8b1f-4fae-94ce-da26a56f46e0/image.png)

#### 부트스트랩을 활용하여 색깔을 변경해준다.

![](https://images.velog.io/images/sh981013s/post/ecb12feb-c1d7-43b7-9866-50358470a25d/image.png)

![](https://images.velog.io/images/sh981013s/post/83f35b59-8996-461c-bd28-20ec7d3ce62e/image.png)

#### board 의 모델을 작성해준다.
#### writer 는 ForeignKey를 사용했다.

![](https://images.velog.io/images/sh981013s/post/56d94c53-7b03-4cd8-91ce-f24b2b90e284/image.png)

#### view 에서 모든 객체를 가져와주고 역순으로 재정렬까지 해준 뒤에 렌더로 념거주는 코드를 작성한다.

![](https://images.velog.io/images/sh981013s/post/e524c4b3-599b-40dd-a16a-f59f1efd9dc2/image.png)

#### 보드의 어드민또한 작성해준다.

![](https://images.velog.io/images/sh981013s/post/e815e703-ae0f-40fe-a37e-bf2bee50d5f6/image.png)

#### for 문을 이용하여 테이블을 채워준다.

![](https://images.velog.io/images/sh981013s/post/6c88e476-eca0-4699-8cca-ed9424de041d/image.png)

#### admin에서 게시물을 작성하고 보드 리스트를 확인하면 다음과 같은 화면을 볼 수 있다.

![](https://images.velog.io/images/sh981013s/post/7f25eb79-eab6-4c7c-afc1-b8184bf1589e/image.png)






