# MTV - 07. MTV의 T,V 만들기 (3) - 회원가입

![](https://images.velog.io/images/sh981013s/post/e3e779b7-e20b-4f5a-b7f8-8d4ff605813a/image.png)

---
#### 전에 정의한 form 의 name 값을 통해 데이터를 가져와준다. 

![](https://images.velog.io/images/sh981013s/post/f70b16af-b41f-4a3f-a8b9-3e61ca5e8fda/image.png)

#### fcuser 를 생성해줄때 class 가 필요하기에 import 를 통해 가져와 준다.
#### 가져와 준뒤에 아래처럼 객체를 생성해준다.

![](https://images.velog.io/images/sh981013s/post/d301c1e5-ad4a-4118-a2be-092ea5b388f4/image.png)

#### 그 후에 저장을 해준다.

![](https://images.velog.io/images/sh981013s/post/f48293aa-c028-4266-ac59-9316ac77f210/image.png)

#### 아직 특정 로직을 만든것이 아니고, 데이터를 입력후 가져와 모델에 저장이 되는지 확인을 해보겠다.
#### 서버에서 회원가입 정보를 입력하니 실제로 모델에 저장이 되었다.

![](https://images.velog.io/images/sh981013s/post/08495130-c46f-40fe-9de1-c8ed94fa7251/image.png)

#### 이제 로직을 작성해볼텐데, 비밀번호와 비밀번호 확인이 다르면 '비밀번호가 다릅니다!' 라는 화면을 HttpResponse 를 사용하여 구현할 것이다.
#### 이를 위해서 

```
from django.http import HttpResponse
```

#### 를 사용해주고 16줄과 같이 코드를 작성해준다.

#### 비밀번호를 다르게 입력하면 다음과 같은 화면을 출력하는것을 확인할 수 있다.

![](https://images.velog.io/images/sh981013s/post/3250fd59-8552-456e-a0a1-6dc4e376d8df/image.png)

![](https://images.velog.io/images/sh981013s/post/fa478a9e-0a56-4af4-b8fc-ec051fe10975/image.png)

#### 하지만 원래 입력하던 폼에 이 내용이 나오면 좋겠는데, 별도의 화면으로 이동하여 불편하다.
#### 아래와 같이 변경을 하였는데,
#### res_data = {} 라는 변수를 선언하고, password 가 다르면 변수에 '비밀번호가 다릅니다' 라는 문자열을 추가하고, 다르지 않을시에 저장한다.
#### 또한 render 를 할 시에 res_data 값을 전달한다. 라고 변경을 하였다.

![](https://images.velog.io/images/sh981013s/post/8bca4726-b347-49b2-b20e-cf4da353e99c/image.png)

#### row를 추가하여 {{ error }} 라는 값을 html 에 만들어주었다. 그러면 자동으로 res_data 의 ['error'] 가 자동으로 맵핑된다.

![](https://images.velog.io/images/sh981013s/post/4d1bc52e-7eb2-415b-a3b4-3d6cee7d8d96/image.png)

#### 이제 아무것도 나오지 않다가 비밀번호 확인이 다르면 해당 문자열이 추가된다.

![](https://images.velog.io/images/sh981013s/post/4808fafd-cf9a-42a6-94c0-9f7d62e04f0a/image.png)

#### 왜 처음에는 나오지 않았냐면, 
#### 처음 들어간 페이지는 GET 방식이지만, 버튼을 누른순간 POST 방식을 사용하기에 비밀번호가 다르기 때문에 해당 로직이 작동했다.

![](https://images.velog.io/images/sh981013s/post/45e02a97-0167-447c-a5be-40371000d30e/image.png)

#### 또 다른 문제로는 이런식으로 저장을 하게되면 아래와 같이 비밀번호 또한 평문으로 저장이 된다. 암호화를 시켜주어야 한다.
#### 하지만 장고에서는 자동으로 암호화 해주는 기능또한 제공한다.

![](https://images.velog.io/images/sh981013s/post/75dc686c-c8ad-47fd-a3d5-e72cff5c7436/image.png)

#### 3번줄과 같이 import 를 해준다.

![](https://images.velog.io/images/sh981013s/post/0a07a6f7-6da2-4e70-a309-ed43bf62cc27/image.png)

#### password 를 저장할때 make_password(password) 를 사용하면 자동으로 함수를 사용하여 암호화해 저장해준다.

![](https://images.velog.io/images/sh981013s/post/f3a41abe-d42a-426f-8730-2c92269a5837/image.png)

#### 관리자 페이지에서 확인을 해주면 보이는 바와 같이 암호화 되어 저장된 모습이다.

![](https://images.velog.io/images/sh981013s/post/21e9b409-2780-443a-b44f-097bc6b43f2e/image.png)

#### 마지막 문제는 사용자가 아무런 정보를 기입하지 않은체 submit 을 하게되면 빈 문자열을 가진 정보가 생성이 된다.
#### 입력받지 않은값을 예외처리를 해주어야 한다.
<br>

#### 13 ,14 ,15 줄과 같이 get 을 사용해서 받아오고 None 을 추가해 아무값도 들어있지 않은 디폴트 값을 설정해준다.
#### 그 후에 if not 을 통해 아까 비밀번호가 다른 상황과 같이 로직을 수정해준다.

![](https://images.velog.io/images/sh981013s/post/53ff73f9-64ad-48ec-948a-c430e8713501/image.png)

#### 하나라도 정보가 입력되지 않으면 다음과 같은 화면을 보여준다.

![](https://images.velog.io/images/sh981013s/post/a0fc6093-9037-44e6-91f1-3cfa56ac1389/image.png)