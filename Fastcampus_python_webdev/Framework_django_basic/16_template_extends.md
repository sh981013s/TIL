# 로그인 - 05. MTV의 T 확장하기 - 상속

![](https://images.velog.io/images/sh981013s/post/97f1fd8c-cd10-4b5a-98aa-51f12b130cd0/image.png)

---

#### 보면, login.html 과 register.html 의 바디를 제외한 코드가 거의 유사하기 때문에 '상속' 이라는 개념이 필요하다.

#### 그렇기 때문에 기준이 되는 하나의 템플릿을 만들고 상속을 하는 시스템을 구축해야한다.

![](https://images.velog.io/images/sh981013s/post/61ad7bef-a0cd-4c45-acb9-e9d7c972023f/image.png)

#### base.html 을 만들어서 기준이 되는 템플릿을 만들어준다.

```
{% block contents %}
{% endblock %} 
```

#### 이 코드를 사용하면 상속반은 템플릿은 내부의 내용만 수정해주면 된다.

![](https://images.velog.io/images/sh981013s/post/da21c28e-2786-456d-bc32-c55ff6f7b72b/image.png)

#### 로그인 페이지를 이처럼 상속을 해준다는 
#### {% extends "base.html %}  과
#### {% block contents %}
#### {% end block %} 을 사용해주면 된다.

![](https://images.velog.io/images/sh981013s/post/ec0c67e9-f777-41f2-b923-7e35c06a7c3b/image.png)

