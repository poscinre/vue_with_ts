# vue 바인딩 기초

### vue의 특징

1. **양방향 바인딩**이 가능하다는 것!<br>
    - 양방향 바인딩이란?<br>
부모 컴포넌트에서 데이터 prop을 통해 자식 컴포넌트로 데이터를 전달하고,<br>
그 데이터를 전달받은 자식 컴포넌트는 이벤트 전달($emit)을 통해 다시 부모로 보내주는 구조<br><br/>

2. v-bind를 사용한 바인딩
   - v-bind는 template 속에서 : 로 축약해서 사용할 수 있다.<br>
   - 아래와 같이 쓰면 template 부분과 script 부분이 바인딩된다.<br>
만약, isActive에 다시 사용하고 싶다면, isActive.value 이렇게 쓰면된다.<br><br/>

```javascript

    <div :class="{ active: isActive }"></div>

    const isActive = ref(true);


```
<br>

3. 콧수염 괄호 <br>
    - 아래와 같이 쓰면 {{ message }} 부분에 Hello Vue.js!가 나타난다.
   
```javascript
<div id="app">
    {{ message }}
</div>

 const message = ref('Hello Vue.js!');
```
<br>

4. v-model<br>
     - 아래 3개의 태그는 v-model을 사용해서 바인딩 할 수 있다.<br>

 ```javascript
 <input v-model="변수명"> 
 <select v-model="변수명">
 <textarea v-model="변수명"> 
 ```
