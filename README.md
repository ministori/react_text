# react_text

## react focus

- virtual DOM
- SPA : routing

## react 로컬 환경 구성

- node.js 섪치
- yarn 설치 : npm
- node.js / npm / yarn 버전 확인
- vs code 설치
- vs code에서 github clone
- create-react-app react-prj
- vs code 재실행 => commit / push
- github 확인
- yarn start
- App.js 수정/반영 테스트
- github commit / push 테스트

## VS Code Github Message

```
- A : Added (This is a new file that has been added to the repository)
- M : Modified (An existing file has been changed)
- D : Deleted (a file has been deleted)
- U : Untracked (The file is new or has been changed but has not been added to the repository yet)
- C : Conflict (There is a conflict in the file)
- R : Renamed (The file has been renamed)
- S : Submodule (In repository exists another subrepository)
```

## react 파일 구조와 component 실습

> 파일/폴더 설명
>  - node_module : node module folder
>  - public : 실제 화면에 보이는 html 파일 또는 리소스들이 저장되는 폴더
>   - index.html : 메인 페이지
>  
>  - src : html 파일에 렌더링되도록 하는 콤포넌트 파일이 저장된 폴더
>   - index.js : index.html에 렌더링되는 파일
>   - App.js : index.js에 렌더링되는 기본 콤포넌트
>   
> 파일 실행 흐름
> - App.js 부분부분 콤포넌트가 App.js에 최종적으로 모임
> - index.js 파일 내부의 <App /> 부분에 렌더링
> - index.html <code>&lt;div id="root"&gt;&lt;/div&gt;</code>에 최

Hello Wold Component => App.js 에 포함 시키는 연습


## JSX

- 정의 : 공식문서
- Babel.js
- 문법 - self-close
- 하나의 구역으로 구분
  - fragment ( https://ko.reactjs.org/docs/fragments.html )
- JSX 변수
- className, id
- 주석 : {/**/}

## props

- 컴포넌트에 값을 전달할 때 사용하는 것
- 예제 소스
- 객체 비구조화 할당 => 객체 구조 분해
- 예제 소스
- 배열 비구조화 할당
- 예제 소스
- props.children


## 조건부 렌더링
- 조건에 따른 다른 렌더링
- 예제 소스









