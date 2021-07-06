# MTV - 04. Admin 활용

#### admin.py 는 말그래도 관리자에 쓸 여러 정보들을 기입한다.
#### 우선적으로 .models 에서 Fcuser 라는 일전에 작성한 모델을 import 한다.

![](https://images.velog.io/images/sh981013s/post/ab2c92d8-fd52-4101-8dc3-c336df15678c/image.png)

#### 클래스를 생성하고 pass 는 아무 동작을 하지 않는다는 뜻이다.
#### 그 후, register를 해준고 다시 실행을 해준다.

![](https://images.velog.io/images/sh981013s/post/cb38e0ee-52d4-4324-93ae-a9169773671a/image.png)

#### Fcusers 라는 모델을 확인할 수 있고 내부에 접속하여 추가, 수정, 삭제또한 가능하다.

![](https://images.velog.io/images/sh981013s/post/8f657365-bf83-4296-9dcf-1d7627074021/image.png)


#### 추가를 하고 확인을 해보면 불편한 사항이 있는데,
#### 제목때문에 아래처럼 한눈에 파악하기 어렵다.

![](https://images.velog.io/images/sh981013s/post/c3016461-87d5-4c49-bda3-82023a399bf8/image.png)

#### 총 두가지 방법이 있는데,
#### 모델에 

	def__str__(self):
	  return self.username

#### 를 사용 해준다.


![](https://images.velog.io/images/sh981013s/post/c7fa79bb-3d02-40dd-80c7-fdd66d6a7971/image.png)

#### 이제 제목으로 username을 반환해준다.

![](https://images.velog.io/images/sh981013s/post/d56e9ade-605c-4cfe-9e82-87541c1d0199/image.png)

#### 하지만 해당 페이지에서 이름 뿐만 아니라 다른 정보도 표시하고 싶다면 
#### admin.py 에서 pass가 아닌, list_display를 통해서 표시하고 싶은 내용을 튜플을 통하여 명시할 수 있다. 

![](https://images.velog.io/images/sh981013s/post/6e9c52e7-d03c-4e30-be2e-71a374a19bb0/image.png)

#### 이제 좀 더 확인이 편하게 바뀐 모습을 확인할 수 있다.
#### 모델의 class의 객체(object)가 list up이 되는것이 아닌,
#### 모델의 class의 field들이 listup 된다.

![](https://images.velog.io/images/sh981013s/post/80955fad-3c58-48b4-b574-0ad56181b936/image.png)

#### 이제 아래의 Fcuser 를 한글로 '패스트캠퍼스 사용자' 로 바꾸고 싶다.

![](https://images.velog.io/images/sh981013s/post/b5bba788-6464-4ed8-9aa4-e244e420e85e/image.png)

#### 이 부분은 models.py 에서 'class Meta:' 에서 반영 해준다.

![](https://images.velog.io/images/sh981013s/post/fb6069b2-c730-45d8-ac2a-1a48d659513d/image.png)

#### 여기서 궁금한점은 작성한 model 의 이름을 Fcuser 로 지정했는데, admin 페이지에서는 Fcusers 라고 보여진다.
#### 이는 장고는 기본적으로 모델을 보여줄때 '복수형' 을 사용하기 때문이다.

![](https://images.velog.io/images/sh981013s/post/2ffa3a88-dd89-4061-9da1-3a3a9796c1a7/image.png)

#### 그렇기 때문에 복수형의 이름까지 따로 지정을 해준다.

![](https://images.velog.io/images/sh981013s/post/76864830-2b39-4712-97fd-5a8416fb63ae/image.png)

#### 이제 '패스트캠퍼스 사용자' 라고 보여진다..

![](https://images.velog.io/images/sh981013s/post/704c4a64-0cd8-4a0e-aef2-d7d63527f43d/image.png)

