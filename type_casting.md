
# Type Casting

### 특정 형식으로 변환
#### 1. as string

이 연산자를 사용하면 개체가 문자열로 변환될 수 없는 경우 예외가 발생하지 않고, 대신 null을 반환<br>
- as 연산자를 사용하여 타입을 강제 형변환
- 이것은 컴파일러에게 변수를 특정 타입으로 취급하도록 알려줌
- 따라서 as string을 사용하면 해당 변수를 강제로 문자열 타입으로 변환

```javascript
let someValue: any = 42;
let stringValue = someValue as string;
// stringValue는 문자열로 간주됨
```
