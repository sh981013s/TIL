# MTV - 02. 데이터베이스 관리

#### admin 을 만들기 전에, 만든 이 클래스가 어떻게 테이블로 만들어지는지 터미널 명령어를 통해 살펴보겠다.  

#### makemigrations 을 하게되면, 저희가 만든 모델이 만들어지고 migrations 폴더 내부에 initial 이 생성된다.

![](https://images.velog.io/images/sh981013s/post/ea617aa3-f7a9-4ecf-91f5-5ac90870420b/image.png)

![](https://images.velog.io/images/sh981013s/post/72e3bed9-b9f6-43cc-92f3-5724d1479ce9/image.png)

#### migrat를 하면 생성된 데이터베이스가 앱들이 사용하는 여러가지 테이블들과 아까 생성된 initial 도 생성된다.

![](https://images.velog.io/images/sh981013s/post/9d5fff0a-4418-4041-81cd-f22d5890c701/image.png)

#### migrate 를 하니 db.sqlite3 또한 생성되었다.

![](https://images.velog.io/images/sh981013s/post/8bec7973-6ade-47f5-9c57-44e7ca5fbc4d/image.png)