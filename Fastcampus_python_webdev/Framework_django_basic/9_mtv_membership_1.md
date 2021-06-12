# MTV - 05. MTV의 T,V 만들기 (1) - 회원가입

### 회원가입 템플릿 만들기

#### fcuser 폴더에 'templates' 라는 폴더를 생성한 후 내부에 register.html 을 생성한다.
#### 부트스트랩을 이용할 것이기 때문에 CSS, 자바스크립트 필요한 헤더들을 복사해서 붙여넣는다.

![](https://images.velog.io/images/sh981013s/post/57afde8a-6263-431a-a37c-536bcf28f1fd/image.png)

![](https://images.velog.io/images/sh981013s/post/492604ce-441f-499d-a92e-c5708fd3e073/image.png)

#### 코드작성을 해주면 이러한 모습이 나오는데, 이를 장고 프로젝트 내에서 보여주게 설정을 해주어야 한다.

![](https://images.velog.io/images/sh981013s/post/a91fa3a5-5392-4ae9-b19e-eb9d761aa44e/image.png)

![](https://images.velog.io/images/sh981013s/post/7f5b8123-0b2e-4b1e-94ac-4ec419b9d6a4/image.png)

#### views.py 에서 아래와 같이 작성을 하는데,
#### request 가 들어오면 'register.html' 을 rendering 해준다.

![](https://images.velog.io/images/sh981013s/post/450ccea1-14ef-47e9-bc1b-19a75ec37aa6/image.png)

#### 반환할 html의 경로는 기본적으로 app 내부의 templates 폴더로 디폴트 값이 설정되어 있지만, 추가적으로 내부에 세부적인 폴더를 만든다면 아래와 같이 경로를 추가적으로 써주거나
#### 통합적으로 templates 를 관리하는 폴더가 있다면 settings.py에서 base directory를 변경해주면 된다.

![](https://images.velog.io/images/sh981013s/post/94d2dc82-1d1c-4a59-8cde-8b34d5966e38/image.png)

#### views.py 를 작성했다면, url 을 설정해주어야 하는데
#### 프로젝트 '자체의' urls.py 에서 아래와 같이 작성해주면 된다.
#### 코드의 뜻은 'fcuser/' 아래로 오는 모든 url들은 fcuser 안에있는 url 에서 관리한다는 뜻이다. 
#### 하지만 아직 fcuser 의 url 은 따로 생성하지 않았다.

![](https://images.velog.io/images/sh981013s/post/413b8919-2623-4250-830b-737b06472806/image.png)

#### 우선 fcuser(앱) 폴더 내부에 urls.py 를 생성하고 기본 틀만 작성한다.
#### 지금의 urls.py 는 빈 껍대기이다.

![](https://images.velog.io/images/sh981013s/post/da821a8d-79c9-490b-8207-d18d6e59870d/image.png)

![](https://images.velog.io/images/sh981013s/post/1f6fda60-8925-4594-9fed-f3fb0de38fde/image.png)

#### register/ 라는 경로를 사용할것이고, ( /fcuser/register ) 뒤에는 '함수'를 사용한다.

![](https://images.velog.io/images/sh981013s/post/e24438cd-20fb-43fa-8e95-51a9c72dddc7/image.png)

#### 그렇기 때문에 2번줄과 같이 같은폴더 내부의 ( . ) views 를 import 한뒤에 5번줄과 같이 views.register 를 할당한다.

![](https://images.velog.io/images/sh981013s/post/eb3b6f29-e4dc-4248-a076-bc271efcd2b1/image.png)

#### 서버를 실행하여 /fcuser/register/ 를 주소창에 추가하여 입력하면 목표인 아래와 같은 회원가입 페이지가 보여진다.

![](https://images.velog.io/images/sh981013s/post/5af49156-bac1-4d03-837e-1f596a8119c0/image.png)