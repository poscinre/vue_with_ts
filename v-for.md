# v-for

### v-for 사용법
#### 1. 어떤 경우에 쓸까?
&ensp;(1) select창 안에서 option을 반복해야할때<br>
&ensp;(2) ul/ol 안에서 li를 반복해야할때

```javascript
 <select>
    <option v-for="option in options" :key="option.value" :value="option.value">
      {{ option.id }}
    </option>
  </select>
```
<br>
&ensp; - 옵션 정의
<br>
<br>

```javascript
const options = [
  { label: '옵션 1', value: 'option1' },
  { label: '옵션 2', value: 'option2' },
  { label: '옵션 3', value: 'option3' },
];
```
<br><br>

#### 2. api를 사용해서 데이터를 가져온다면?
&ensp;- options의 초기값을 정의하고, 함수를 통해<br>
&emsp;&emsp; 데이터를 가져온 후 options.value에 할당하면 된다.<br>

```javascript
const options = ref([]);

const 함수명 = async () => {
    const [status, data] = await api컴포넌트.api명();
    if (status == 200) {
    options.value = data;
  }
```
