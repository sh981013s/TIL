# 2. 웹 프레임워크로써 Django


### 모델 계층

- 데이터베이스와 연동하는 계층
- 클래스만 만들어주면 자동으로 SQL형태로 생성해준다.
- 직접 따로 Raw SQL 을 생성 해줄 수 있다.

![](https://images.velog.io/images/sh981013s/post/62c15e9a-b654-4819-b21c-5c5777addc3a/image.png)
### 뷰 계층


비지닉스 로직에 대한 부수적인 url을 생성, 연결, 관리 해준다.

![](https://images.velog.io/images/sh981013s/post/a4c14457-0a00-4df8-8b3f-aaef1952b219/image.png)

함수 하나로 이 모든 작업이 가능하다.

![](https://images.velog.io/images/sh981013s/post/802e68d0-b4f8-46bc-914e-74c19ce4e875/image.png)

### 템플릿 계층

사용자에게 표시할 정보를 표현하기 위해 디자이너에게 친숙한 문법을 제공한다.

![](https://images.velog.io/images/sh981013s/post/127b76a2-bbe3-4a34-8c1c-9f5fdb7a1c54/image.png)

---

#### 정리하자면

모델 계층에서 데이터를 생성하고,
뷰 계층에서 해당 데이터를 이용하여 동작하고,
템플릿 계층에서 결과를 인해 보여준다.

---


**시작하기에 앞서 기본 터미널 사용 총 정리.**

 

1. 폴더 생성 

2. $ python3 -m vev myvenv (가상환경 구축)

3. $ source myvenv/bin/acivate (가상환경 실행)

4. $ pip install django (가상환경에 django 설치)

5. $ django-admin startproject firstproject (프로젝트 생성) 

6. $ python manage.py startapp firstapp (앱 생성)

7. $ python manage.py runserver