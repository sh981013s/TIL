![](https://images.velog.io/images/sh981013s/post/f442d231-f720-4598-8d68-7cc728e100e1/image.png)

---

### NPM 을 이용하여 프로젝트 만들기

![](https://images.velog.io/images/sh981013s/post/b2d47c00-ae57-4a94-b297-58093effe638/image.png)

npm test 라는 폴더 생성 후 VSC 로 열어준다.

![](https://images.velog.io/images/sh981013s/post/50a1d2ea-0fa1-4c99-bc43-8551dceed7cf/image.png)

node.js 를 설치하였으면 npm 도 같이 설치가 되었을 것이다.
```
$npm init -y
```
를 터미널에 입력해주면 바로 프로젝트 내부에 package.json 이라는 파일이 생긴다.

![](https://images.velog.io/images/sh981013s/post/d9fcc126-bc92-424c-b13c-43930e478ccf/image.png)

package.json 파일을 열어보면 여러 option들이 보인다.
- name : 프로젝트 이름
- main : 
'main' 은 하나의 프로젝트를 npm 생태계에 업로드 할때 필요하다. 개인 웹사이트를 만들때는 없애줘도 된다.
- scripts : 
'scripts'는 현재 프로젝트 내부에서 사용할 수 있는 여러가지 script 명령들을 내부에 명시를 해놓으면 프로젝트를 진행하면서 사용할 수 있다.

![](https://images.velog.io/images/sh981013s/post/36d2fb70-1271-49d3-8c32-db1298840c59/image.png)


```
$npm install parcel-bundler -D
```
위와같이 터미널에 입력하여 parcel-bundler 라는 package 를 설치한다.<br/>
일정시간 후에 확인을 해보면 프로젝트 내부에 node_modules 라는 폴더와 
package-lock.json 이라는 파일이 생성되었다.

![](https://images.velog.io/images/sh981013s/post/c682aaa7-c6ec-4b5a-9811-dafa04e18029/image.png)

node_modules 라는 폴더에 들어가면 설치한 parcel-bundler 라는 패키지(모듈) 이 설치된 모습을 확인할 수 있는데, 이상하게 parcel-bundler 이외에 다른 패키지들 또한 설치가 되었다. <br/>

![](https://images.velog.io/images/sh981013s/post/218d449b-9ca9-49fa-ae01-b5e36ed60011/image.png)


이는 parcel-bundler 라는 모듈이 만들어지고 활용될때 필요한 다른 묘듈들이기 때문이다. 
parcel-bundler 폴더 내부에 package.json 에 dependencies 를 보면 확인할 수 있다.

![](https://images.velog.io/images/sh981013s/post/921bc868-4d6a-47ed-b449-2b137c8da016/image.png)

다시 최상위 폴더의 package.json 에 들어가면 devDependencies 에 
일전에 설치했던 parcel-bundler 가 포함된 것을 확인할 수 있다.

![](https://images.velog.io/images/sh981013s/post/cb1318ce-996c-4ca8-afe9-78182c7f457b/image.png)


```
$npm install lodash 
``` 
를 터미널에 입력하여 다른 패키지를 설치하면 dependencies 에 lodash 가 추가된 모습을 볼 수 있다.

package.json 에 설치된 모듈들이 기록이 되면 node_modules 라는 폴더를 삭제해도

```
$npm install 
```
명령어를 통해 한번에 명시된 모듈들을 설치할 수 있다.<br/><br/><br/>

---

```
$npm install parcel-bundler -D
$npm install lodash
```

하지만 일전에 두개의 모듈을 설치했을때 parcel-bundler 에 대해서만 -D 를 사용하였고 package.json 에서도 다른 방식으로 두개의 모듈이 각각 기록되었다.

![](https://images.velog.io/images/sh981013s/post/e23a1756-e2a6-4cc6-a63e-b25c5a1b866f/image.png)

이는 npm install 을 이용하여 다른 사용자가 만들어 놓은 패키지 를 install 할때 패키지 A 가 사용하는 또 다른 패키지를 같이 install 하며 이들은 package_lock 으로 관리를 하였다.

![](https://images.velog.io/images/sh981013s/post/ba55acb9-95c3-4533-b7a2-0915fc704eba/image.png)

어떤 모듈을 설치할 때 -D 를 붙여넣는다면
개발용 의존성 패키지 설치를 하는것이고,<br/>

그렇지 않다면,
일반 의존성 설치를 하는것이다.

이 차이는
개발용 의존성 패키지는 내가 직접 '개발'할때만 필요하고 웹이 동작할때는 필요가 없다는 뜻이고,
일반 의존성 설치는 웹브라우저에서 동작할 수 있는 개념이다.

![](https://images.velog.io/images/sh981013s/post/28420420-0fc0-4259-8d92-cb129805cd09/image.png)

앞에서 설치한 두개의 모듈의 설치 방법에 따른 차이점이 된다.



