# 게시판 - 04. 게시판 만들기 - 4

![](https://images.velog.io/images/sh981013s/post/721d4c23-990d-4100-b436-d4b065acb80c/image.png)

---

#### 게시판 리스트에서 페이지를 나타내는 '페이징'을 구현할것이다.
#### 우선 여러개의 글을 써보았다.

![](https://images.velog.io/images/sh981013s/post/17092040-f267-43b3-b23d-622fbe03acb6/image.png)

#### 우선 부트스트랩에 있는 예재로 만들어보았다.

![](https://images.velog.io/images/sh981013s/post/c3cb521d-dc6d-4249-8926-dfd5303a589e/image.png)

![](https://images.velog.io/images/sh981013s/post/f2454f85-76da-4b1a-838d-a8b6032f0a0a/image.png)

#### view 로 넘어와서 장고에서는 Paginator 를 제공해준다.

![](https://images.velog.io/images/sh981013s/post/364eb218-5532-4729-976a-62b2186711ec/image.png)

#### 페이지네이터를 사용하여 한 페이지에 2개씩 출력한다는 내용을 전달해주는 방식으로 수정을 하였다.

![](https://images.velog.io/images/sh981013s/post/23954eb0-29f8-4f0b-9df0-f7cfffb7c4cf/image.png)

#### 6, 4 만 출력이 된다.
#### 하지만 페이지 정보도 아직 적용이 안되있고 버튼에 링크또한 걸려있지 않다.

![](https://images.velog.io/images/sh981013s/post/1eb84f13-53f2-4ae4-b820-6cd6430a74c5/image.png)

#### 값을 넣어주었다.

![](https://images.velog.io/images/sh981013s/post/2cf8f8e2-8874-4cb8-bc60-baffeae22828/image.png)

#### 하지만 에러가 나는데, 전의 페이지가 없어서 그렇기에 예외처리를 해준다.

![](https://images.velog.io/images/sh981013s/post/fb809ac2-bd75-4962-82ac-3d952cf40b4a/image.png)

#### 아래와 같이 정상적으로 작동한다.

![](https://images.velog.io/images/sh981013s/post/07cd1c14-2e5a-41ea-912c-6be485ffcaaa/image.png)

#### 하지만 1페이지에서 이전으로가 disabled 가 되지 않았는데 disabled 는 a태그가 아닌 li 태그에 적용되야 하기에 코드를 수정하였다.

![](https://images.velog.io/images/sh981013s/post/4a8eb6a7-ec3f-4085-bbd3-6ecd14b2bcdc/image.png)

#### disabled 가 정상적으로 작동한다.

![](https://images.velog.io/images/sh981013s/post/63616583-eefb-4c91-a9e3-22fede937b8a/image.png)




