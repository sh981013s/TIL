![](https://images.velog.io/images/sh981013s/post/74616e4d-43a9-4ad8-b115-465ffcd2688a/image.png)

---

테스트 저장소를 깃허브에 푸쉬하려한다.
이때 npm 을 통해 호스트를 관리할때는 몇가지 주의사항이 있다.

![](https://images.velog.io/images/sh981013s/post/38a1d323-4be9-4f29-af88-be256b4e8c51/image.png)

우선 설치한 모듈은 package.json 의 devDependencies 와 dependencies 에 기록되고, 
실제 모듈들은 node_modules/ 라는 폴더에 존재한다.

또한 해당 모듈들이 사용하는 다른 모듈들은 package-lock.json 에 기록되고 관리된다.

![](https://images.velog.io/images/sh981013s/post/d598657f-6fc4-487c-9fbb-c7d6802496bd/image.png)

또한 .cache/ , dist/ , node_modules/ 는 parcel build 명령어를 통해 생성되었다.
이런식으로 후작업을 통해 생성된 폴더들은 따로 버전관리를 해줄 필요가 없다.
<br/>
이 말인 즉슨, 해당 폴더들은 깃허브 저장소에 따로 푸쉬를 하지 않아도 된다는 뜻이다.

예를 들어서 node_modules/ 라는 폴더를 삭제하더라도

```
$npm i
```
라는 명령어 한줄로 package.json 을 이용하여 정확한 버전의 모듈들을 한번에 설치할 수 있다.

또한, 마찬가지로 dist/ 와 .cache/ 폴더를 삭제하더라도 

```
$npm run build
```
라는 사전에 정의한 명령어로 다시 생성할 수 있다.

---

그렇기에 .gitignore 라는 파일을 최상단 디렉토리에 생성 후

```python
.cache/
dist/
node_modules/
```
이라고 버전관리가 필요하지 않은 파일 혹은 폴더를 추가하면 해당 파일/폴더를 제외한 채 버전관리를 할 수 있다.

![](https://images.velog.io/images/sh981013s/post/b461aea3-8ae2-427d-83dd-fb4ea265583d/image.png)

그렇기에 git status 로 체크를 하면 해당 폴더들이 제외된 모습을 확인할 수 있다.

