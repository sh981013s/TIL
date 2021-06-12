# MTV 의  M 만들기 (회원)

#### 현재는 'board' 와 'fcuser' 라는 2개의 앱을 만든 상황이다. 
#### 우선적으로 fcuser(회원) 먼저 진행하겠다.

![](https://images.velog.io/images/sh981013s/post/33816de9-e3f3-4482-863c-f5b2f6031b49/image.png)

#### model.py 에서 class 에 field 를 작성한다.
#### 여기서 verbose_name 은 추후에 admin 페이지에서 이름을 지정한 값으로 나오게 하는 기능이다.

![](https://images.velog.io/images/sh981013s/post/fc1300c0-9794-4773-ba5d-6d98a165f58b/image.png)


#### 장고 framework 는 이런식으로 모델에 클래스를 만들고 나면 따로 sql을 만들거나 추가로 수행해야 할 일들이 없다. 자동적으로 저장되고 실행된다.

#### 데이터베이스에 '테이블명'을 설정할 수 있다.
#### 아래처럼 class Meta: 를 작성해주면 된다.

![](https://images.velog.io/images/sh981013s/post/eaf2b13f-992e-406d-8125-673adfd99e17/image.png)


#### 이제는 이 모델을 관리할수 있는 관리자 페이지를 만들고
#### 템플릿과 뷰를 만들어주면 된다.









