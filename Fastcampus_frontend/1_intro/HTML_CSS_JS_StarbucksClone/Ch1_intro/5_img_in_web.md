# 웹에서 사용하는 이미지



### 비트맵과 벡터

#### 웹에서 쓰이는 이미지는 크게 '비트맵' 과 '벡터' 로 나누어진다.
#### 비트맵은 각각의 '픽셀'이 모여서 만들어진 이미지고,
#### 벡터는 '레이어' 를 '비트맵'으로 만드는 개념이다.
#### 벡터는 점과 면과 선과 면으로 이루어져있는 이미지이다.

![](https://images.velog.io/images/sh981013s/post/e88bd709-76ec-4f07-a17d-cdfe0d10b439/image.png)

### 비트맵

- 정교하고 다양한 색상을 자연스럽게 표현한다.
- 확대/축소 시 계단 현상, 품질 저하가 일어난다.
- 대부분의 '사진' 이미지들이 비트맵으로 이루어져 있다.

### 벡터

- 확대/축소에서 자유롭고 용량 변화가 없다.
- 정교한 이미지(인물,풍경 사진 같은)를 표현하기 어렵다.

![](https://images.velog.io/images/sh981013s/post/0d3cec3a-7b37-4a4c-a560-aa794ad2205f/image.png)

---

### 비트맵의 확장자를 가진 포맷 : 

### JPG(JPEG) 

#### 비트맵의 확장자를 가진 포맷중 가장 많이 쓰이는 
#### JPG(Joint Photographic Coding Experts Group)는 Full-color와 Gray-scale의 압축을 위해 만들어졌으며, 압축률이 훌륭해 사진이나 예술 분야에서 많이 사용한다.

- '손실 압축' 방식을 사용한다.
- 표현 색상도(24비트, 약 1600만 가지의 색상)가 뛰어나다.
- 이미지의 품질과 용량을 쉽게 조절 가능하다.
- 가장 널리 쓰이는 이미지 포맷이다.

#### JPG 는 저장이 될때 초기 이미지의 데이터가 '손실'되어 저장되기 때문에 용량면에서 이점을 가지지만, 반복적인 손실을 피하기 위해서는 반복적인 저장을 피해야한다.

![](https://images.velog.io/images/sh981013s/post/ecab8b92-a089-454b-92bd-62dbe20559d6/image.png)

### PNG :

#### 비트맵의 확장자를 가진 포맷중 하나인
#### PNG(Portable Network Graphics)는 Gif의 대체 포맷으로 개발되었다.

- '비손실 압축' 방식을 사용한다.
- 8비트(256 색상 / 24비트(약 1600만 색상) 으로 컬러 이미지 처리를 한다.
- Alpha Channel 을 지원한다. (투명도)
 - W3C 권장 포맷이다.
 
 ![](https://images.velog.io/images/sh981013s/post/c75e552c-3ba9-4110-bd6d-63f45a13ea8f/image.png)
 
 #### 아래 비교와 같이 PNG 는 Alpha Channel 을 지원하기에 원하는 이미지의 부분만 사용할 수 있지만, JPG 는 배경까지 사용해야한다.

 
 ![](https://images.velog.io/images/sh981013s/post/4aa474c3-108f-4e1a-a7df-1ed49a54478b/image.png)
 
 ⬆️ JPG
 
 ![](https://images.velog.io/images/sh981013s/post/230ffd5c-a6d0-44af-9ad6-73b4122caa5d/image.png)
 
  ⬆️ PNG
  
 ### GIF
 
 #### GIF(Graphics Interchange Format)는 이미지 파일 내에 이미지 및 문자열 같은 정보들을 저장한다.
 
 - '비손실 압축' 방식을 사용한다.
 - 여러장의 이미지를 한 개의 파일에 담을 수 있다.
 - 8피트 색상만을 지원한다.(다양한 색상 표현에는 적합하지 않다.)
 
 ![](https://images.velog.io/images/sh981013s/post/1b865465-a248-4ac0-8b38-000f98bce1c5/image.png)
 
 ![](https://media.giphy.com/media/jUwpNzg9IcyrK/giphy.gif)
 
 
 ### WEBP
 
 #### JPG, PNG, GIF를 모두 대체할 수 있는 구글이 개발한 이미지 포맷이다.
 
 #### 최근에 개발된 기술이기때문에 '하위호환성' 을 찾아보며 지원하지 않는 웹브라우저 및 버전을 확인해야만 한다.
 #### ex) Internet Explorer 는 지원을 하지 않는다.
 
 - 완벽한 손실/비손실 압축을 지원한다.
 - GIF 같은 애니메이션을 지원한다.
 - Alpha Channel을 지원한다.(손실/비손실 모두)

![](https://images.velog.io/images/sh981013s/post/62dfdbab-b5a3-470e-910a-a74e3aa32f18/image.png)

---

### 백터의 확장자를 가진 포맷 :

### SVG
#### SVG(Scalable Vector Graphics)는 마크업 언어(HTML/XML) 기반의 벡터 그래픽을 표현하는 포맷이다.

- 해상도의 영향에서 자유롭다.
- CSS와 JS로 제어가 가능하다.
- 파일 및 코드를 삽입 가능하다.

![](https://images.velog.io/images/sh981013s/post/123eb023-cd8e-48a2-91c1-c1bc4debd7ff/image.png)

