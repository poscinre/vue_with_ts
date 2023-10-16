# null coalescing operator

### 널 병합 연산자
#### 1. '??' 연산자

변수가 null일 때 기본 값을 할당하고, 그렇지 않으면 변수의 값을 그대로 사용<br>
- 널 병합 연산자 (??)를 사용하여 값이 null 또는 undefined일 경우 대체 값을 지정
- ?? 왼쪽 피연산자가 null 또는 undefined이면 오른쪽 피연산자를 반환하고, 그렇지 않으면 왼쪽 피연산자를 반환
- ?? ""은 문자열이 null 또는 undefined인 경우 빈 문자열로 대체

```javascript
let maybeNullString: string | null = getSomeString();
// 어떤 함수에서 문자열 또는 null을 반환한다고 가정
let result = maybeNullString ?? "";
// result는 문자열 또는 빈 문자열("")
```
