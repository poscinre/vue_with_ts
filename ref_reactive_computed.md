# ref, reactive, computed

### 내가 이해한 바로는..

1. ref<br>
    - 변수를 바인딩하려면 그냥 ref를 쓰기<br>
.value만 붙여서 할당해주면 끝이니까 너무 편하다.<br><br/>

2. reactive <br>
   - reactive는 배열에서 자주 쓰인다.<br>
     나는 생각보다 자주 쓰지 않는 듯..<br><br/>

3. computed <br>
    - 읽기전용이라고 생각하면 된다.<br>
      대신, ref나 reactive와 달리 업데이트가 바로바로 반영되기때문에 쓴다.<br>
      특히 onMounted 후에는 초기값이 보여지는데,<br>
      computed를 쓰면 초기값이 아니라 지금! 현재!의 데이터를 보여준다<br>
   
