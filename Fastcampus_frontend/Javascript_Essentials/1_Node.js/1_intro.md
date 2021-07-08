![](https://images.velog.io/images/sh981013s/post/6d8fb50b-0b59-48e8-8545-329f1ee4e3a8/image.png)

### Node.js 란? 

##### Node.js는 Chrome V8 JavaScript 엔진으로 빌드된 JavaScript 런타임.


##### 여기서 런타임이란, 프로그래밍 언어가 동작하는 환경이다.

---

### Javasript 의 동작환경

![](https://images.velog.io/images/sh981013s/post/d027a8c6-ab61-4e68-8ca6-9115157ff11a/image.png)

##### 자바스크립트가 동작할 수 있는 환경에는 크게 두가지가 있다.
- Node.js 가 설치되어 있는 로컬 컴퓨터
- 웹 브라우저

##### 자바스크립트를 배우면 컴퓨터를 제어할때, 웹 브라우저를 제어할때와 같이 여러방면에 사용할 수 있다.

---

### 프론트엔드 개발시에 Node.js 를 왜 사용하는가?

![](https://images.velog.io/images/sh981013s/post/2def97c2-27bf-425b-9f28-97f57b4c8780/image.png)

##### 기본적으로 웹 브라우저에서는 HTML,CSS,JS 만 동작을 하는데, 위 세가지만 사용을 하면 완성을 할 수는 있지만 비효율 적일 수가 있다.

##### 그리하여 Sass, BABEL 등과 같은 모듈을 사용하여 Node.js 를 통해 JS 로 변환시켜주는것이 기본적인 프론트엔드 개발 환경이다.

---

### Node.js 설치

![](https://images.velog.io/images/sh981013s/post/21186858-c2ba-43f3-bdbd-648d9960037c/image.png)

https://nodejs.org/ko/

위의 해당 링크를 누르게 되면 Node.js를 설치할 수 있는 웹페이지가 나오는데,

좌측의 LST 에 대해 설명하면

LST(Long Term Supported)는 장기적으로 안정되고 신뢰도가 높은 지원이 보장되는 버전으로, 유지/보수와 보안(서버 운영 등)에 초점을 맞춰 대부분 사용자에게 추천되는 버전이다.

우측의 최신버전은, 최신버전에만 포함된 최신의 기술이 존재할 수 있지만, 비교적 불안정적일 수 있다는 단점이 존재한다.

연습을 할때에는 최신버전을 사용할 수 있지만, 보통은 안정성을 위해 LST 버전을 설치한다.

#### 해당 방법과 같이 공식 홈페이지에서 직접 다운로드 받아 설치할 수 있는 방법이 있지만, 여러가지 버전을 사용해야 할 수도 있기 떄문에, NVM 이라는 Node Version Manager 이라는 '시스템에 여러 개의 node js 를 설치하고 사용할 버전을 쉽게 전환할 수 있게 도와주는 shell script 를 사용하는 방법을 권장한다.

![](https://images.velog.io/images/sh981013s/post/00060a7a-f047-4377-88ac-cba4817873b0/image.png)

https://github.com/nvm-sh/nvm

nvm 의 깃헙 주소로 이동해 

![](https://images.velog.io/images/sh981013s/post/8908572d-204f-468a-ac32-2766ed32b7f5/image.png)

해당 설치 스크립트 코드를 터미널에서 실행해준다.

그후에 확인을 하려고

```
$ nvm --version
```

를 입력하면, 

![](https://images.velog.io/images/sh981013s/post/f9dee9f9-7400-453c-8cc9-eda1c3d93655/image.png)

위와같이 nvm 을 찾을수 없다 라는 화면을 볼 수 있는데,
그렇다면 nvm 을 load 하기위해 

```
$ [[ -s $HOME/.nvm/nvm.sh ]] && . $HOME/.nvm/nvm.sh
```
를 입력해준다.

이제 
```
$ nvm --version
```
을 입력해주면

![](https://images.velog.io/images/sh981013s/post/cf45b570-d337-4e87-93c5-bdc5db45417e/image.png)

0.38.0 버전이 설치되어 있다는 사실을 확인할 수 있다.