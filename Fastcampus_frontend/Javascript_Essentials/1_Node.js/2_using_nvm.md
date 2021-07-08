![](https://images.velog.io/images/sh981013s/post/b701064b-c1e6-476c-9419-c6c46f2ad012/image.png)

---

### NVM 을 사용하여 Node.js 설치하기 <br/><br/>

해당 작업은 터미널에서 이루어진다.  

1. ``` $nvm ls ```  


node.js 가 설치되어 있는지 확인 

![](https://images.velog.io/images/sh981013s/post/15ecea1c-9b34-4590-9e46-e73a683ac7c9/image.png)

2. ``` $nvm install 14.17.3 ```

설치하려는 node.js 의 LST 버전 설치

![](https://images.velog.io/images/sh981013s/post/4389754d-6fd9-4d00-acac-74b00e3a26f2/image.png)

3. ``` $nvm install 16.4.2 ```

node.js 의 Current 버전 설치

4. ``` $nvm ls ```

설치된 node.js 버전들 확인

![](https://images.velog.io/images/sh981013s/post/a89a0193-9e75-4471-9fa9-7209546d2c45/image.png)

5. ``` $nvm use 14.17.3 ```

현재 current version 인 16.4.2 버전이 선택되어 있는데 14.17.3 버전으로 변경

![](https://images.velog.io/images/sh981013s/post/b57a833e-8bad-4d9f-b832-dcd58ed10f51/image.png)

정리하자면 혼자 개발을 할 시에는 버전 하나를 사용하기에 nvm 을 사용하면서까지 버전관리를 할 필요는 없지만, 팀원들과 프로젝트를 할 시에는 버전을 통일해야 하기에 nvm 을 사용한다.

---

