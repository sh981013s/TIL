# 4. Django의 MVC(MTV)


앱 내부에 'templates' 라는 폴더를 생성하면, 기본적으로 앱 템플릿 엔진이 앱 내부의 템플릿 폴더를 향해있기 때문에 사용할 수 있다. 
그러나, 앱 외부에 템플릿 폴더를 생성해 통합적으로 운용하는 방식또한 존재한다.



![](https://images.velog.io/images/sh981013s/post/0afc9da7-3520-48c7-a23a-1fe7e5ba8134/image.png)

---

### Model : 
일전에 살짝 언급했듯이 models.py 에 class 를 사용하여 데이터베이스를 생성할 수 있고,

![](https://images.velog.io/images/sh981013s/post/656a1a5d-9120-4bf8-8e6a-2acdab6bffbc/image.png)

### View :
views.py에 httpresponse와 같은 비지니스 로직을 반화하거나 template 을 반환하는등, 다양한 로직을 사용할수 있다.

![](https://images.velog.io/images/sh981013s/post/bf612b01-bd1c-4cc2-bf05-840fd36d3247/image.png)

### Template : 
template 폴더 내부에 html 파일을 생성할 수 있다.

![](https://images.velog.io/images/sh981013s/post/ce934d81-1ada-4bbb-b824-d9aa079b9fff/image.png)