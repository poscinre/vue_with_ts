# props

### 간단히 이해하는 props 사용법
#### 1. 부모가 전달

&ensp;- 먼저 자식 컴포넌트를 템플릿안에 만들고 바인딩을 해준다.<br>
&emsp; 그리고 변수에 전달할 값을 넣어준다. <br><br>

```javascript
<ChildComponent :propName="propValue" />

const propValue = ref("전달할 값")
```
  
<br><br>
#### 2. 자식은 전달받기
&ensp;- 타입 지정해서 defineProps로 받으면 된다.<br>

```javascript

import { defineProps } from 'vue';
const props = defineProps({
  propName: String // 전달 받을 props의 타입 지정
});

```
<br>
&ensp;- 나는 이렇게 자주 쓴다.<br>
&emsp; typescript와 vue를 함께 사용할땐 타입을 확실히 지정해주는 것이 좋다.<br>
&emsp; interface는 type을 선언하는 역할을 한다.<br><br>
    
```javascript
interface Props {
  propName: string;
}
const props = defineProps<Props>();
const propName = toRef(props, "propName");
```

<br><br>

#### 3. 자식이 전달<br>
&ensp;- 첫번째 방법은 이벤트로 전달하는 것.<br>
&emsp; 이벤트를 발생시키면서 emits을 사용한다.
   
```javascript
const emits = defineEmits(["eventName"]);
const handleClick = () => {
  emits("eventName", "전달할 데이터");
};
```
<br>
&ensp;- 두번째 방법은 노출시키기<br><br>
    
```javascript
const eventName = () => {
  "전달할 데이터나 함수를 쓴다."
};
defineExpose({
  eventName,
});
```
   
