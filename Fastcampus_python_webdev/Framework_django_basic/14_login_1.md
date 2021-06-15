# 로그인 - 02. 로그인 만들기 - 1

![](https://images.velog.io/images/sh981013s/post/bdd6c443-3d8d-4ba1-bd0f-0ef21ad9ccbe/image.png)

---

#### 로그인 화면의 T 먼저 만들고 V를 만들 예정이다.
#### 사실 일전에 만들어 놓은 회원가입 화면에서 이메일과 비밀번호 화면만 없으면 로그인 화면이다.

![](https://images.velog.io/images/sh981013s/post/5979920c-c024-4a42-8fbf-5cffe1d4c15e/image.png)

#### login.html 을 만들고 register.html 을 수정하여 작업했다.

![](https://images.velog.io/images/sh981013s/post/4ff8b5e6-cee6-4d64-b02d-7da12c52f4a0/image.png)

#### 우선 view 로 연결만 해주고
#### url을 login/ 으로 맵핑해주었다.

![](https://images.velog.io/images/sh981013s/post/a850040b-3283-4464-a58b-4815f890a411/image.png)

![](https://images.velog.io/images/sh981013s/post/9ee6d5cd-93c7-4c10-ab53-847410d38736/image.png)

![](https://images.velog.io/images/sh981013s/post/6ab501b0-f9dc-4494-8e44-e8fc158ed2c3/image.png)

#### register 함수와 비슷하게 작성을 하는데, 21번은 모델의 object 를 불러온다. 여기서 비밀먼호 확인을 할때에는 import 한 check_passoword 기능을 쓴다.

![](https://images.velog.io/images/sh981013s/post/21ecbc29-58f0-45d3-9721-9533b1d2abdc/image.png)

![](https://images.velog.io/images/sh981013s/post/8777690b-b3ea-49d5-ad16-0642977a7a84/image.png)

#### 이와같이 작성하고 비밀번호가 틀리면 error 가 작동하게, 맞으면 세션을 이용해야 하는데 이는 뒤에서 다루겠다..

![](https://images.velog.io/images/sh981013s/post/250fffcb-3acc-46cd-9cf0-377a3048af42/image.png)