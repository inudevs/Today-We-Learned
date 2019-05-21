# 003. Vue.js
프론트엔드 과제가 생각보다 심각해서 준비했습니다. Vue.js로 간단한 프로젝트를 만드는 강의입니다.

모든 내용은 Windows 10 기준으로 진행하겠습니다.

## 1. Node.js, NPM 설치

### 설치
윈도우에서는 아마 NPM(npm package manager)까지 같이 깔릴 거예요.

- [nodejs.org](https://nodejs.org/en/)에 가서 최신 버전의 Node.js를 설치해주세요.
  - LTS로 깔아도 되고 걍 최신으로 깔아도 돼요.
- 인스톨러가 나오면 아는 거 빼고 걍 다 `Next`랑 `Install` 같은 긍정적인 느낌의 단어만 눌러주시면 됩니다.
- 제대로 쭉쭉 누르셨다면 NPM도 깔리고, PATH에도 설치 위치가 추가될 겁니다.

### Node.js: 설치 확인
1. CMD를 열어주세요. 윈도우 키를 누르고 `cmd` 치면 나와요.
2. `node -v`하면 아마 `v11.9.0` 같은 형식의 버전이 표시될 거예요. 그러면 `node`가 제대로 설치된 거예요.

### NPM: 설치 확인
마찬가지로 `npm -v`를 실행하면 `6.9.0` 같은 NPM 버전이 나올 거예요. 그럼 제대로 된 거임.

### 여담
NPM 말고 Yarn이라는 패키지 매니저도 있으니까 참고하세요.

## 2. Vue CLI 설치

### NPM으로 설치

```bash
npm install -g @vue/cli
```

Vue CLI 3을 설치해주세요. 3.X 버전이 이미 2018년에 나왔는데도 대부분의 강의가 2.X 버전을 다루고 있어요. 제발 3으로 해주세요.
 
저거 골뱅이 안 붙이면 2로 깔리니까 주의하세요.

## 설치 확인
설치가 완료되고 `vue -V`를 실행해서 버전을 확인할 수 있어요.

## 3. Vue 프로젝트 만들기
먼저 CMD를 열고 `cd` 명령어를 이용해서 프로젝트 폴더를 위치시킬 곳으로 이동해주세요. 이건 검색하면 진짜 바로 나옵니다.

```bash
vue create example
```

`example`이라는 새로운 앱을 생성하겠습니다.

```bash
Vue CLI v3.4.0
┌───────────────────────────┐
│  Update available: 3.7.0  │
└───────────────────────────┘
? Please pick a preset: (Use arrow keys)
❯ default (babel, eslint) 
  Manually select features 
```

아마 설정(프리셋)을 고르라고 하는 이런 인터페이스가 나타날 건데요. 일단은 그냥 `default`로 가보겠습니다.

```bash
(...)
⚓  Running completion hooks...

📄  Generating README.md...

🎉  Successfully created project example.
👉  Get started with the following commands:

 $ cd example
 $ npm run serve
```

프로젝트 생성이 완료되면 위와 같은 내용이 나오네요.

현재 폴더에서 `cd example`로 생성된 `example` 폴더로 들어가 주세요.

```bash
 DONE  Compiled successfully in 3349ms                                                                                 오후 4:35:52

 
  App running at:
  - Local:   http://localhost:8080/ 
  - Network: http://172.18.0.240:8080/

  Note that the development build is not optimized.
  To create a production build, run npm run build.
```

`npm run serve`를 실행하면 위처럼 로컬 서버가 돌아갈 거예요. [http://localhost:8080/](http://localhost:8080/)로 가주세요.

<img alt="hello-vue" src="./images/hello-vue.png" width="80%">

> 와! 드디어!

이런 창이 뜨면 일단 성공입니다. 이제 Vue 프로젝트의 구조랑 문법을 다뤄볼게요.
