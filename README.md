# react_text

## 로컬 개발 환경 구성

### CMD/Terminal

- CMD/Terminal 명령어

- node.js 설치
- yarn 설치 : npm
- node.js / npm / yarn 버전 확인

### VS Code

- vs code 설치
- vs code terminal에서 nodejs / npm / yarn 버전 확인

### git 환경 구성

> git 설치
> git config setting
>  - git config --list
>  - git config --global user.name ""
>  - git config --global user.email ""
> git permission 확인
>  - personal access token : https://hyeo-noo.tistory.com/184
> - mac : keychain 인증 확인

> - vs code에서 github clone
> - commit / push test
> - github 확인

### react project install / 시작

- create-react-app react-prj

> vs code 재실행 => commit / push
> 
> github 확인

- yarn start
- App.js 수정/반영 테스트

### localhost URL

- 로컬 서버에서 실행을 할떄 사용할 수 있는 키워드 URL
- localhost => IP 주소 : 127.0.0.1
- port - URL:port번호
  - 하나의 물리 서버에서 여러개의 서버 SW를 실행할 수 있음

> github commit / push 테스트

```
npx error / permission
sudo chown -R 900:900 "/Users/moonbro/.npm"
sudo chown -R $USER:$GROUP ~/.npm
```

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

## react 공식문서
https://ko.reactjs.org/

## react 파일 구조와 component 실습

> 파일/폴더 설명
>  - node_module : nodejs module folder
>  - public : 실제 화면에 보이는 html 파일 또는 리소스들이 저장되는 폴더
>   - index.html : 메인 페이지
>  
>  - src : html 파일에 렌더링되도록 하는 콤포넌트 파일이 저장된 폴더
>   - index.js : index.html에 렌더링되는 파일
>   - App.js : index.js에 렌더링되는 기본 콤포넌트
>   
> 파일 실행 흐름
```
> component 파일 생성
> App.js : 부분부분 콤포넌트가 App.js에 최종적으로 모임
> index.js : 파일 내부의 <App /> 부분에 렌더링
> index.html : <div id="root"></div>에 최종 반영됨
```

- Hello Wold Component => App.js 에 포함 시키는 연습

## react focus

- virtual DOM
  - 일반 DOM 개발 : DOM Tree <-> 노드마다 매번 렌더링
  - document.querySelector()
  - DOM 복사본
  - 메모리상에서 필요한 동작
  - 동작 완료 후 이전 내용과 비교해서 바뀐 부분만 실제 DOM을 변경하는 렌더링 실행
  - Ex) 두 가지 상황 비교(https://velog.io/@sbinha/React%EC%97%90%EC%84%9C-Virtual-DOM#virtual-dom-%ED%8A%B9%EC%A7%95)
  
- SPA(Single Page Application)
  - Ajax
    - 일반 개발과 AJAX 비교 : W3school
  - Routing
    - 그림 비교

- Component : 작은 단위로 나누어준 코드 블럭(단위, 조각)

> - component 작성 방식
> - App.js에 Component 추가 : Hello.js

## JSX(Javascript Syntax Extension / Javscript XML)

- 정의 : 공식문서

- HTML 마크업 언어를 별다른 기호 사용없이 그대로 Javascript 구문처럼 사용할 수 있는 것

- Babel.js 라이브러리가 JSX를 사용가능하게 해줌

- JSX는 return 키워드 ()안에 하나의 Element영역으로 그룹화 되어 있어야 함

> - Hello2.js - 간단한 태그 구성 추가

- self-close 태그 사용 : Empty Element

> - Hello3.js - component 태그 구성 추가

- 하나의 영역으로 그룹화 할 때 특정 Element로 그룹화 해서 반영하지 않을 때 - Fragment 사용

  - fragment ( https://ko.reactjs.org/docs/fragments.html )

> - fragment1.js : React.fragment
>
> - fragment2.js : <></>

- JSX에서 자바스크립트 변수 값 사용하기
  - {변수이름}

> - variable.js : const name = 'Hello React'

- JSX에서 class, id 지정하기
  - class : className 속성 사용
  - id : id 속성 사용

> - identifier.js : class, id 표시

- 주석 : {/* 주석내용 */}

## props

- 포함하는 component에서 포함되는 컴포넌트에 값을 전달할 때 사용하는 것

> - props1.js
> 
> - props2.js : 값을 여러개 전달할 때

- 비구조화 할당 / 구조 분해 할당 => 객체, 배열
  - 객체 안에 있는 값을 추출해서 변수 혹은 상수로 바로 선언(https://learnjs.vlpt.us/useful/06-destructuring.html)

> - props3.js : 구조 분해 할당 - 배열 타입 적용
> - props4.js : 구조 분해 할당 - 객체 타입 적용
> - props5.js : 구조 분해 할당 적용된 Component

- props.children

> - props6_wrap.js / props6.js : Wrapper

## 조건부 렌더링
- 조건에 따른 다른 렌더링
- condition1.js
- condition2.js
- condition3.js

## Todo Markup & Styling Coding
https://dev.to/hariramjp777/todo-app-using-html-css-and-js-local-storage-design-html-and-css-1m0j

- public
  - todo.html
  - todo.css
  - add_button.svg

### Todo Component Structure

> component로 분해

- header : TodoHeader
- main : TodoMain
  - todo-list : TodoList
    - todo-item(동적생성) : TodoItem
  - status : TodoStatus
- footer : TodoFooter

### React에서 css를 작성/사용하는 방식

- App.css에 전체 css를 구성하고 전역으로 사용하는 방식
- module css 방식 : css를 하나로 구성하지 않고 component별로 구성
  - component와 css 파일이 분리되어 있음.
  - 작성 방법
    - 폰트 설정, reset css 등은 App.css에 전역으로 사용
    - 하나의 요소를 선택해서 css를 적용한 경우 module css로 활용함
- styled-component : 스타일링된 컴포넌트 => component별로 css를 구성
  - 인라인 방식처럼 사용 => component 파일에 css, component contents 같이 작성
  - Internal 방식으로 렌더링됨

## React JSX에 기능 추가

- event와 함수를 연결

```
on이벤트 = {함수이름}

Ex) onClick={myFunction}
```

### React Hook
(공식문서 : 참고)

- Input Value
  - JSX에 반영되는 값이 업데이트되어 다시 렌더링(리렌더링)되어야 할 때 Hook을 사용함

- Hook 소개
  - Hook은 상태 값과 여러 React의 기능을 사용할수 있음
  - 상태 변경후 리렌더링

- Hook API
  
  - useState : 초기값으로 지정한 값을 사용해서 상태를 표현하는 값과 그 값을 설정(지정)하는 함수를 반환함
  ```
  const [state, setState] = useState(initState);
  
  state : 값이 저장되는 변수
  setState : 값을 지정하는 함수
  initState : 초기값
  ```
  
  - useRef : DOM 찾기, focus 이동
    - useRef로 할당된 객체와 해당 객체가 할당된 Element와 연결되어 Rendering된 DOM에 직접 Access할 수 있도록 하는 함수
  
  - map 함수
    - 특정 데이터를 다른 형태나 성질의 데이터로 변형하여 매핑해주는 함수
  
  - 배열 렌더링(App => 배열 component)
  
  - 배열 추가/제거
  
  - 현재 배열 개수 구하기 => 남은 할일 구하기


### Hook을 사용해서 배열에 데이터를 추가/삭제

- 기본 배열 데이터
  - 최종으로 수정되는 데이터이기 때문에 기본 배열 데이터도 useState()로 싱태 관리가 필요함.

- 새로 입력되는 객체
  - 새로 값이 입력될 때 useState()로 상태 관리가 필요함.
  - 구조 분해 할당을 통해 단순한 형태의 변수를 사용

- 실행 사이클의 상태 관리
  - 기본데이터 개수 이후로 데이터가 추가될 수 있도록 useRef()로 상태 관리가 필요함

- 컴포넌트 밖의 함수와 값을 사용하기 위해 컴포넌트 속으로 전달해서 사용하기도 함

## React Router

> Main Router
> 
> Sub Router

### Plugin

- Prettier
- Eslint
