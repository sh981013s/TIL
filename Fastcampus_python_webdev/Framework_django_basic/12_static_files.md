# Static - 01. static 파일 관리하기

![](https://images.velog.io/images/sh981013s/post/cad2a64f-2113-4b59-9975-7ced0f21904d/image.png)

---

#### 스태틱 파일을 관리하기 전에 CDN 이라는 개념을 알아야 한다.
#### CSS, JS 파일이 어떤 서버에 원본이 들어가 있고 아래와 같이 분산이 되있다. 원본을 가져오기에는 느리기 때문에 주로 글로벌 서비스를 런칭할때 사용한다.
#### 자신에게 가장 빠른 서버를 사용하는것이 CDN 의 메인 개념이다.

![](https://images.velog.io/images/sh981013s/post/880ce679-5520-4066-9a91-8ee284a3cb62/image.png)

#### 이런식으로 주소를 통해 가져온 파일들은 원본이 있는 서버에서 가져오는 것이 아닌, 가장 근접한, 빠른 서버에서 파일을 가져오게된다.

![](https://images.velog.io/images/sh981013s/post/b280ee85-07c4-4342-963d-ef8924336867/image.png)

#### 하지만 CDN 방식이 아닌 따로 CSS 를 관리하는 방식을 사용하겠다.
#### 우선, 프로젝트 폴더 내부에 static 이라는 폴더를 만들어준다.
#### settings.py 에서 BASE_DIR 은 이미 프로젝트로 설정이 되어있기에, 그 내부에 있는 static 폴더로 설정을 해준다.

![](https://images.velog.io/images/sh981013s/post/dba8506e-1c52-47c4-aced-546b73cb6f0a/image.png)

#### 부트스트랩을 이용한 테마를 적용하려 하는데, 아래와 같이 구글에 검색하면 bootswatch 가 나온다.
#### 그 후 다운로드 받은 css 파일을 static 폴더 내부에 넣어준다.

![](https://images.velog.io/images/sh981013s/post/5ce3b92f-f8f1-40a5-8440-0c053f3011c3/image.png)

![](https://images.velog.io/images/sh981013s/post/7fd4c34c-6d09-470e-8672-3bf7964aebcc/image.png)

#### 기존에 사용하던 CDN 방식의 코드를 cmd + / 로 주석처리 해준뒤에 따로 static 폴더에 있는 css 파일을 연결해준다.
#### 바로 테마가 적용된 하면을 확인할 수 있다.

![](https://images.velog.io/images/sh981013s/post/467a8f22-22dc-4faa-979f-d23ee28e33ab/image.png)

![](https://images.velog.io/images/sh981013s/post/cd1b15aa-0c60-42f4-ae30-8cb7dabdc3eb/image.png)

