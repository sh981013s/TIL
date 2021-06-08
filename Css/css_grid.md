

> 목표 : 가로로 나뉘어진 모습을 구현하기

---

## div
	div는 아무런 의미가 없고 '디자인' 의 용도로만 쓰이는 무색무취한 태그이다. 
    또한, div 는 기본적으로 'block level element' 이기 때문에, 화면 '전체'를 사용한다.

![](https://images.velog.io/images/sh981013s/post/604c6277-d6b2-434b-acc1-454226a5063f/image.png)

## span
	div 와 같은 의미로 무색무취한 태그이지만, 다른점은 'inline element' 이기 때문에,
    필요와 상황에 맞추어서 사용할 수 있다.
    
![](https://images.velog.io/images/sh981013s/post/3fea063f-9af2-4ab8-b7dc-dd2e0b31484b/image.png)

### 두개의 div를 가로로 '나란히' 사용하고 싶을시에는 우선적으로 '부모' 태그를 사용하여 감싸준다.

![](https://images.velog.io/images/sh981013s/post/cd6ce728-a6ec-41c0-a50d-b00b8d43c1c8/image.png)


## css 속성값을 
### display : gird;
### grid-template-columns: x x; 
### 를 주게되면 사용이 가능하다. 
#### 여기서 fr 값을 사용하게되면 화면의 퍼센테이지 값을 자동으로 할당한다.
#### 아래의 예시를 보면, 2fr 1fr; 값을 주었는데, 
#### 화면 전체를 3으로 나누어 2/3 : 1/3 으로 할당한 모습이다.

![](https://images.velog.io/images/sh981013s/post/50fc9bf7-770a-4a20-95ec-5e7bf99bbea9/image.png)

---
### 하단부의 사진과 같이 가로획으로 나누어 만들고 싶을때, 우선div 로 감싸준 뒤, id를 해당한다.

![](https://images.velog.io/images/sh981013s/post/5649ce14-caf9-4a24-b3e0-dfff5d7661f6/image.png)

### display 를 grid 로 표기하고,
### grid-template-columns 에 값을 넣어준다.
### ex) 150px 1fr;

![](https://images.velog.io/images/sh981013s/post/c6871dcc-f55d-4e58-9c80-838cbafce25d/image.png)

---

### 하지만 grid는 최신기술인만큼 지원하지 않는 브라우저들, 버저들 또한 존재한다.

![](https://images.velog.io/images/sh981013s/post/01f58425-3fb1-4442-a357-1af05124fc45/image.png)

---

참고 : https://opentutorials.org/course/3086/18322