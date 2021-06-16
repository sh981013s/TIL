# 로그인 - 06. Form 활용하기 - 1

![](https://images.velog.io/images/sh981013s/post/9c000762-6783-4bf1-bea8-cc71844b34bb/image.png)

---

### 폼(Form) 이란?

#### 폼을 핸들링하는 것은 생각보다 복잡합니다. 사용자를 위해서 수많은 타입의 데이터 항목들이 필요로 하고 화면에 보여줘야 되며 이런 값들은 다시 서버로 보내집니다. 이후에도 값들에 대한 유효성 검증이 필요로 하죠. 검증 이후에는 데이터를 처리하는 로직까지도 필요로 합니다. 

#### 장고에서는 이런 작업들에 대해서 단순화시켜주고 자동화 기능을 제공해줍니다. 또한 개발자가 HTML 작성을 하여 폼 관련 핸들링하는 코드를 작성하는 것보다 장고에서 제공하는 폼 기능이 더욱 보안적 요소가 훌륭합니다.

 

#### 포괄적으로 장고 폼 기능은 다음 3가지로 요약할 수 있습니다.

- 렌더링을 위해서 데이터를 준비하고 재구성을 해줍니다.
- HTML 폼을 만들어줍니다.
- 클라이언트로부터 제출이 된 데이터를 받고 처리해줍니다.

#### HTML의 form 태그는 폼 역할의 단지 한 부분의 불과합니다. 하지만 장고에서의 폼 개념은 위에서 설명드린 기능들을 제공합니다. 이런 기능들을 사용하기 위해서 Form Class를 사용해주시면 되는데요.

#### 모델 클래스의 필드는 모델 클래스의 필드가 데이터베이스 필드에 매칭 되는 것처럼, 폼도 폼 필드의 클래스는 html 요소 즉 태그에 매핑이 됩니다. 폼이 제출되면 유효성 검사까지 수행이 됩니다.

---

#### 현재 로그인 페이지에서 사용하고 있는 2개의 폼을 삭제해준다.

![](https://images.velog.io/images/sh981013s/post/7e61d770-1c90-405e-9edc-0a41e5becf6e/image.png)

#### forms.py 라는 파일을 앱 내부에 생성해주고 아래와 같이 작성해준다.

![](https://images.velog.io/images/sh981013s/post/07d4dafa-9d3c-4ba0-8d2d-f8d37055162a/image.png)

#### 로그인 폼을 가져와 주고 폼을 이용해 전달하는 방식으로 뷰에있는 로그인 함수를 개편해준다.

![](https://images.velog.io/images/sh981013s/post/5eae9fa7-ec25-41db-898b-88477610c1af/image.png)

![](https://images.velog.io/images/sh981013s/post/16b7b080-3c74-4213-a63d-05793cdb1c1b/image.png)

#### 템플릿에서 {{ form }} 이라고 해주면
#### 아래와 같이 출력해준다.

![](https://images.velog.io/images/sh981013s/post/161b75dd-ae10-45b5-bc40-c7f8b9915a5f/image.png)

![](https://images.velog.io/images/sh981013s/post/70df246c-237d-4d21-825c-1a4217705655/image.png)

#### 장고에서 자동적으로 할당한것이기 때문에 필요에 맞게 커스터마이징이 필요하다.
#### 아래와 같이 작성해준다.

![](https://images.velog.io/images/sh981013s/post/2a78368b-46f3-421a-b986-ca2c4b30490e/image.png)

#### 또한 라벨도 따로 작성해준다.

![](https://images.velog.io/images/sh981013s/post/33976c0a-a9e4-42cd-b657-f386eae08de9/image.png)

#### 정상적으로 보이는 모습이다.

![](https://images.velog.io/images/sh981013s/post/a75dd3d2-84a2-425a-8c08-8dfdc1e5de4d/image.png)

#### 또한 비밀번호를 가려서 입력해야하기 때문에 위젯도 따로 설정해준다.

![](https://images.velog.io/images/sh981013s/post/ad79380b-540d-4ffd-bea2-7827df70623b/image.png)


---

참고 : https://junlab.tistory.com/193