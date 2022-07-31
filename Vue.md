# Vue.js 
Vue 공식 사이트 한글 번역(문법 등 참고) :
<a style="font-size:20px;">https://kr.vuejs.org/v2/guide/#Vue-js%EA%B0%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80%EC%9A%94</a>
---
## 사용 이유 : Web-app만들 때 페이지가 자연스럽게 넘어가는 상황을 만들기 위해

---
### 구동 방법 (터미널 작성)
- 시작 : `npm run serve`
- 종료 : `ctrl + c -> clear`
- 부모 폴더 이동 : `cd ..`
- 폴더 만들기 : `vue create 폴더명`
---

### App.vue(=메인 페이지)에서 코드 짜면 됨!

#### 한 페이지 안에 링크 주석 간단하게 하는 법?
`<router-link to="/">Home</router-link> 
<router-link to="/about">About</router-link>
싱글페이지 애플리케이션 머 어쩌고 ~
4시간 Vue 입문 <50m ~>`

`webpackPrefetch:true`

### vue 파일 하나 추가하면 router 폴더 파일에도 반드시 머 추가해야 함

### 문자열로 binding : {{ - }}
### html로 binding : v-html = " ~ "
### input value == v-model = " 값 " 사용

### react는 양방향 바인딩 사용 못 함

### checkbox는 데이터 선언 = [] 배열로 선언
### radio는 = '' 문자열로 선언

### v-for로 테이블 or  select 만들면 정말 쉬움  --> DataBindingListView.vue 참고
<-- 4시간 강의 -->

------

# <-- vue로 직방 만들기 영상 -->

// node_modules : 프로젝트에 쓰는 라이브러리들
// src : 소스코드 다 담는 곳
// public : html파일, 기타파일 보관
// package.json : 라이브러리 버전, 프로젝트 설정 기록

---

### {{ 데이터바인딩 }}하는 이유 
- html에 하드코딩해놓으면 나중에 변경 어려움
- vue의 실시간 자동 렌더링 쓸 수 있음
- 값이 자주 바뀔 것 같은 애들한테 사용(변수)
- html속성을 `:속성="데이터이름"` <== 이런식으로도 사용 가능

---
### vue의 HTML 반복문
`태그 v-for="작명 in 몇회(or array/변수)" :key="작명"`
- 자료 안의 데이터 갯수만큼 반복됨
- 작명한 변수는 데이터 안의 자료가 됨
- 변수 작명 2개까지 가능 `(a,i) <-- 예시`
  --> 왼쪽 변수(a) : array 내의 데이터
  --> 오른쪽 변수(i) : 1씩 증가하는 정수
- `:key=""`의 용도 : 반복문 돌린 요소를 컴퓨터가 구분하기 위해 사용. 반드시 써야 함
---
### 이벤트 핸들러 (@태그 or v-on:태그)
- 버튼 눌렀을 때 java 실행하려면 `@click=""`
``` vue에서 함수 만들고 싶으면 `method: {}`안에 만들면 됨 ```
- 함수 안에서 데이터 쓸 땐 `this.데이터명`

---
### 이미지 넣기
- `img src="경로/이름.jpg or .png"`
- -src에 있는거 가져올 때 경로는 `./`부터 시작
---
### 모달창 만들기
##### 동적인 UI 만드는 법
1) UI의 현재 상태를 데이터로 저장해둠
   `--> 그 UI가 지금 어떻게 보여야 할 지`
   (data 안에)
2) 데이터에 따라 UI가 어떻게 보일지 작성
`v-if="조건식" -> 조건식이 참일때만 html 보여줌`
---
### import / export 문법 쓰는 법
강의 3:26~: <https://www.youtube.com/watch?v=38PWm8TgaV0&t=22s>