# 권대웅
## [3월 30일]

### Firebase
- 파이어베이스에 프로젝트 생성하기 
    - nwitter 웹 애플리케이션 등록
    - 파이어베이스에서 제공하는 Config 값을 복사하여 firebase.js에 작성한다
        - :exclamation: 버전차이에 따라 오류가 발생할수 있다
        > [firebase 8버전 이하]
        > import firebase from 'firebase/app';
        > import 'firebase/auth';
        > import 'firebase/firestore';
        > [firebase 9버전 이상]
        > import firebase from 'firebase/compat/app';
        > import 'firebase/compat/auth';
        > import 'firebase/compat/firestore';
    - firebase.js에는 키값등의 깃허브에 업로드 하였을때 숨겨야할 키코드 등이 있으므로 .env 파일을 생성하여 숨기도록 한다
        - firebase.js
        ```
        apiKey: process.env.REACT_APP_API_KEY,
        authDomain: process.env.REACT_APP_AUTH_DOMAIN,
        projectId: process.env.REACT_APP_PROJECT_ID,
        storageBucket: process.env.REACT_APP_STORAGE_BUCKET,
        messagingSenderId: process.env.REACT_APP_MESSAGING_SENDER_ID,
        appId: process.env.REACT_APP_APP_ID
        ```
    - .env 파일을 .gitignore에 추가
### Router
- react-router-dom 설치 
> $ npm install react-router-dom
- src 산하에 components 폴더와 routes 폴더를 만들고 components 파일 아래에 App.js, Router.js 파일을 작성한다. routes 파일 아래에는 Auth.js EditProfile.js, Home.js,Profile.js 파일을 작성한다

- Hooks는 함수 컴포넌트에서 상태를 사용한다

## [3월 23일]

### React app 생성 오류 
- 일회용
> $ npx create-react-app@latest app1 (프로젝트명)
- 설치형(마지막 버전으로 재설치)
> $ npm install -g create-react-app@latest
> $ npx create-react-app app1 (프로젝트명)
### 로컬 PC에서 push 
> $ git config --global user.name "Your Name"
> $ git config --global user.email you@example.com
- 확인방법
> $ git config user.name
> $ git config user.email
### Github에 있는 파일 불러오기
> $ git clone "주소" 
- easysIT nwitter 주소 "https://github.com/easysIT/nwitter.git"
### 리엑트 환경 세팅 
- App.js, index.js, package.json에 대한 불필요한 내용 수정
- src내 불필요한 파일 삭제 
    - App.css
    - App.test.js
    - index.css
    - logo.svg
    - reportWebVitals.js

