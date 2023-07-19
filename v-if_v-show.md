# v-if, v-show, v-else, v-else-if

### 사용법
#### 1. v-if
&ensp;- 조건이 true일때만 보인다.<br>

```javascript
<div v-if="condition">조건이 참일 때만 보이는 부분</div>

const condition = ref(true);
```
<br><br>

#### 2. v-show
&ensp;- 조건이 true일때만 보인다.<br>

```javascript
<div v-if="condition">조건이 참일 때만 보이는 부분</div>

const condition = ref(true);
```
<br><br>

#### 3. v-else
&ensp;- v-if와 함께 사용되며, 조건이 false일때만 보인다.<br>

```javascript
<div v-if="condition">조건이 참일 때만 보이는 부분</div>
<div v-else>조건이 거짓일 때만 보이는 부분</div>

const condition = ref(true);
condition.value == false; 
```

위와 같이 조건을 false로 할당하면 v-else만 보이게 된다
<br><br>

#### 3. v-else-if
&ensp;- 여러 조건을 사용해야할때, v-else-if를 끼워준다
```javascript
<div v-if="condition === 'A'">A 조건일 때 보이</div>
<div v-else-if="condition === 'B'">B 조건일 때 보임</div>
<div v-else>위의 조건들이 모두 거짓일 때 보임</div>
```
    
