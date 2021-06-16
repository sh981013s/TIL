# 로그인 - 07. Form 활용하기 - 2

![](https://images.velog.io/images/sh981013s/post/28eddb5f-db30-43c3-843f-71152c67b913/image.png)

---

#### request method 가 POST 라면 POST의 로그인 폼을 사용하고 정상적인 username 과 password 가 입력됬다면 redirect 를 해준다. 하지만, 정상적이지 않을때 에러 메세지를 출력해야한다.

![](https://images.velog.io/images/sh981013s/post/96f64bee-f8b2-4220-b8c1-5c4bce187fe5/image.png)

#### span을 이용하여 에러메세지에 대한 span을 등록해준다.
#### 이름만 입력했을시에 다음과 같이 나온다.

![](https://images.velog.io/images/sh981013s/post/7c2b1379-6a91-460b-bdbe-435c768c50cb/image.png)

![](https://images.velog.io/images/sh981013s/post/62e6311d-9068-4f93-9134-8c1275d2d98f/image.png)

#### 지금은 값이 들어있는가에대한 유효성 검사만 하고있지만 일치하는지에 대한 유효성 검사 또한 필요하다.
#### 폼을 이런식으로 바꿔준다.

![](https://images.velog.io/images/sh981013s/post/71615fad-5d51-4087-80e1-7199fa519b4c/image.png)

#### 에러 메세지 또한 필요에 맞게 커스터마이징 할 수 있다.

![](https://images.velog.io/images/sh981013s/post/677d1ee2-7f17-446a-a783-422eeb826bb3/image.png)

#### 폼 마지막에 else : (맞다면,) id 를 추가하여 밖에서도 식별할수 있게 해준다.

![](https://images.velog.io/images/sh981013s/post/6a1b4fa0-f8fc-4488-9eb8-11654037bc44/image.png)

#### view 도 이에따라 session 작업까지 해준다.

![](https://images.velog.io/images/sh981013s/post/ca14b810-ba20-4ef4-ae19-890da11290b7/image.png)