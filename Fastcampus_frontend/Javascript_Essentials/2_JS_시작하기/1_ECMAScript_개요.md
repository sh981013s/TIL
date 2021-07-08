![](https://images.velog.io/images/sh981013s/post/ed9a853f-43d5-4b74-94c0-2b3909ab4b4f/image.png)

ECMA스크립트란, Ecma International이 ECMA-262 기술 규격에 따라 정의하고 있는 표준화된 스크립트 프로그래밍 언어를 말한다. 자바스크립트를 표준화하기 위해 만들어졌다.

ECMA 스크립트는 5버전부터 전성기가 시작되었는데 버전의 특징이라고 보면
단순하게 5버전 이하는 internet explorer 를 위한 버전이라고 보면 되고 
그 이후 버전은 최신 웹 브라우저를 위한 버전이라고 보면 편하다.

ECMA 스크립트와 자바스크립트를 비교하자면

ECMAScript는 스크립팅 언어를 어떻게 만들어야 하는지를 설명하는 일종의 설명서라고 생각하면 되고,

JavaScript는 ECMAScript를 사양을 바탕으로 만들어진 언어인 것이다.

---

이제 자바스크립트를 이용하여 기본적인 코딩을 할 수 있는 세팅을 해보자.

js_test 라는 폴더를 생성 후 터미널에서

```
$npm init -y
```
를 실행해주면 

![](https://images.velog.io/images/sh981013s/post/db260fcf-c2d3-477e-a253-0164acb5529f/image.png)

바로 package.json 이 생성된다. 그 후,

```
$npm install parcel-bundler -D
```
를 통하여 모듈을 설치해준다. 개발용으로만 쓸 것이기 때문에 -D 를 붙여넣는다.

설치가 완료되었으면, package.json 으로 이동하여
parcel-bundler 를 이용하여 프로젝트를 개발용으로 실행할 수 있고
나중에 완성해서 결과물을 낼 수 있는, 즉 build 할 수 있는
스크립트를 추가해준다. 

```javascript
"scripts":{
  "dev":"parcel index.html",
  "build":"parcel build index.html"
}
```

![](https://images.velog.io/images/sh981013s/post/f9507249-2950-4e53-8f29-fa17d5494727/image.png)

이후에 다음과 같이 기본적인 html 틀 안에 script src 를 활용하여 연결해주고

![](https://images.velog.io/images/sh981013s/post/b1df71a8-2243-484a-b290-6f60b401e224/image.png)

main.js 또한 작성해준다.

이제 개발서버를 열어 확인해줄 것인데,
아까 작성한 스크립트를 활용하여 터미널 창에

```
$npm run dev
```
를 실행하여 주소로 들어가 확인해보면

![](https://images.velog.io/images/sh981013s/post/55d1bcc8-30e2-4cc6-83bf-b80ca32fcafd/image.png)

정상적으로 내부 개발서버의 화면이 보인다.