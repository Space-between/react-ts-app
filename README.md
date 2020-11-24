밑에있는 글은 이 프로젝트를 설치하는 과정이다
이 프로젝트는 밑에있는 글에 나와있는 방법으로 만들어졌다.
따라서 이 프로젝트를 다운받으면 밑에 과정을 거치지 않고
npm run dev로 바로 react+ts를 사용할 수 있다

cra안쓰고 React+Typescript설치하는 과정
(참고 : https://ko.parceljs.org/getting_started.html)

npm i
npm init
npm i -D parcel-bundler typescript
npm i react react-dom
npm i -D @types/react @types/react-dom
npx tsconfig.json

위에 있는 명령어 설치하기

public폴더 생성해서 index.html만들고 밑에 코드 붙여넣기

<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>React app</title>
</head>
<body>
  <div id="root"></div>
  <noscript></noscript>
  <script src="../src/index.tsx"></script>
</body>
</html>

src폴더 생성해서 index.tsx만들고 밑에 코드 붙여넣기

import React from "react";
import ReactDOM from "react-dom";
import App from "./App";

ReactDOM.render(<App />, document.getElementById("root"));

src폴더안에 App.tsx만들고 rfc입력해서 컴포넌트형식으로 코드하나 만들기

npm init 명령어로 만들어진 package.json파일이 있는데 package.json안에 "scripts"에 해당하는 객체안에
"dev": "parcel -p 3000 ./public/index.html --open", 이거 넣어주기

npm run dev로 실행하기

tsconfig.json안에 "compilerOptions"에 해당하는 객체안에 "esModuleInterop": true 이거 넣어주기

참고한 곳(https://github.com/rhkdgns95/react-app)
