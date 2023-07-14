# router

### 간단히 이해하는 router 사용법
#### 1. query 전달

```javascript
import { useRouter } from "vue-router";
router.push({
  name: "이동할 컴포넌트",
  query: {
    전달할 데이터 이름: 데이터,
  },
});
```

&ensp;- query 전달 받기
```javascript
import { useRoute } from 'vue-router';
const route = useRoute();
const query = route.query;
```

<br>

#### 2. params 전달

```javascript
import { useRouter } from "vue-router";
router.push({
  name: "이동할 컴포넌트",
  params: { 전달할 데이터 이름: 데이터 },
});
```

&ensp;- params 전달 받기

```javascript
import { useRoute } from 'vue-router';
const route = useRoute();
const params = route.params;
```

<br>

#### 번외. interface로 전달 받기
&ensp;- typescript를 쓰는 경우 타입 지정을 위해 interface를 사용해준다.

```javascript
import { useRoute } from 'vue-router';
interface UserParams {
  id: string;
  name: string;
}
const route = useRoute();
const params = route.params as UserParams;
```
