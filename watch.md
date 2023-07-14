# watch

### 간단히 이해하는 watch 사용법
#### 1. watch 사용법
&ensp;- 첫번째 인자 : 감시할 데이터<br>
&emsp; 두번째 인자 : 데이터가 변경될 때 호출될 콜백 함수<br><br>

```javascript
import { ref, watch } from "vue";

const myData = ref("");

watch(myData, (newValue, oldValue) => {
  console.log("myData 변경", newValue, oldValue);
});
```
<br>

#### 2. 어떤 경우에 쓸까?
&ensp;(1) input, select의 입력값을 감지하고,<br>
&emsp;&emsp; 사용자가 어떤 값을 입력/선택했는지, 그리고 그 값을 이용해야 할때 사용한다.<br><br>
&ensp;(2) 비동기 이후의 업데이트<br>
&emsp;&emsp; api 호출 이후, 이벤트 동작 이후에 값을 업데이트 할때 쓴다.<br><br>
&ensp;(3) 두 개 이상의 데이터가 연결되어 있고, <br>
&emsp;&emsp; 한 데이터가 변경되어 다른 데이터에 영향을 주어야 하는 경우<br>
<br>

#### 3. watchEffect는?
&ensp;- 데이터에 변화가 있을 때 즉시 동작<br>
&emsp; 변경 이전의 값을 제공하지는 않는다.<br><br>

```javascript
const myData = ref("");

watchEffect(() => {
  console.log("myData 변경", myData.value);
});
  
