### Q&A
*출처: https://github.com/sudheerj/vuejs-interview-questions-korean/blob/master/README.md#slots%EC%9D%B4%EB%9E%80*

  - Q. vuejs 의 특징  
  ```
    - 가상 DOM(Virtual DOM): VueJS에서는 ReactJS, Ember 프레임워크와 유사하게 가상 DOM을 사용합니다. 가상 DOM은 원본 HTML DOM을 표현하는 메모리 상의 가벼운 DOM 트리로, 원본 DOM에 영향을 미치지 않고 업데이트를 할 수 있습니다.  
    - 컴포넌트(Components): VueJS 어플리케이션에서 재사용할 수 있는 엘리먼트들을 만들 수 있습니다.  
    - 템플릿(Templates): VueJS는 Vue 인스턴스 데이터와 DOM에 접근할 수 있는 HTML 기반의 템플릿을 제공합니다.  
    - 라우팅(Routing): 페이지의 전환은 vue-router를 이용합니다.  
    - 저용량(Light weight): VueJS는 다른 프레임워크와 비교해 저용량입니다.  
  ```

  - A. 

---

  - Q. (쉬움) vuejs 라이프사이클은?  
  ```
    - creation, mounting, updating, destruction 크게 4가지로 구분되어져있음.  

    - creation -> beforeCreate, created  
    - mounting -> beforeMount, mounted  
    - updating -> beforeUpdate, updated  
    - destruction -> beforeDestroy, destroyed  
  ```

  - A. 

---

  - Q. (쉬움) v-if 와 v-show의 차이점  
  - A. v-if는 조건이 일치해야지만 화면에 렌더링 하지만, v-show는 모든 엘리먼트를 DOM에 렌더링 후 CSS를 이용하여 display: none 속성만 줌   

---

  - Q. (쉬움) 상위 컴포넌트의 정보를 하위 컴포넌트로 데이터를 전달할때 사용되어지는 속성은?  
  - A. props(프롭스)  

---

  - Q. (쉬움) 범위 CSS(Scoped CSS)란?  
  - A. 해당 CSS는 해당 컴포넌트에서만 영향을 미치는 것

---

  - Q. (쉬움 or 중간) filter란?  
  - A. 텍스트를 형식화 하기위해 사용되어짐. 예) 시간단위, 금액 소수점 표기 등  

---

  - Q. (쉬움 or 중간) $nextTick 이란?
  - A. DOM 조작시 created, mounted Hook 에서 UI렌더 및 데이터까지 갱신 후 사용되는 callback함수

---

  - Q. (중간?) 하위 컴포넌트에서 상위 컴포넌트로의 이벤트 전달 방법은?  
  - A. event emitting || eventbus || store 

---

  - Q. (중간) VueRouter에서 중첩된 라우팅, children이란?  
  - A. 하위 url path 설정  
    ```
      path:'/user/:id'
      component: User,
      children: [
        {
          path: 'mypage', // url-> /user/:id/mypage
          component: MyPage
        }
      ]
    ```

---

  - Q. (중간) 이벤트버스란? & 사용법  
  - A. Vue 인스턴스 객체를 통해 $emit(주는쪽), $on(받는쪽)을 사용하여 설정

---

  - Q. (중간) 믹스인(mixins)이란?  
  - A. 각 컴포넌트에 재사용 가능한 기능을 배포하는 유연한 방법 중 하나  

---

  - Q. (중간) slot이란?
  - A. Vue에서 ```<slot>```을 이용해 상위 컴포넌트에서 하위 컴포넌트 내부에 사용자 정의의 컨텐츠를 집어 넣을 수 있음
    ```
      Vue.component('alert', {
        template: `
          <div class="alert-box">
            <strong>Error!</strong>
            <slot></slot>
          </div>
        `
      })
    ```
    ```<alert>``` 태그 안에 넣은 값은 컴포넌트 내부의 ```<slot>```의 컨텐츠로 들어간다
    ```
      <alert>
        There is an issue with in application.
      </alert>
    ```


---

  - Q. (중간 or 어려움) 동적으로 컴포넌트를 로드하는 방법은?  
  - A. v-bind:is 로  

---