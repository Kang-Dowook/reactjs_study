# Redux
<hr/>

## 컨테이너 컴포넌트 만들기
> 컴포넌트에서 리덕스 스토어에 접근하여 원하는 상태를 받아 오고, 액션도 디스패치해줄 차례.
> 리덕스 스토어와 연동된 컴포넌트를 컨테이너 컴포넌트라고 한다.
> 컴포넌트를 리덕스와 연동하려면 connect 함수를 사용해야 한다. 다음과 같이 사용한다.
> `connect(mapStateToProps, mapDispatchToProps) (연동할 컴포넌트)`
- mapStateToProps: 리덕스 스토어 안의 상태를 컴포넌트의 props로 넘겨주기 위해 설정하는 함수.
- mapDispatchToProps: 액션 생성 함수를 컴포넌트의 props로 넘겨주기 위해 사용하는 함수.

> connect 함수를 호출하고 나면 또 다른 함수를 반환한다. <dr/>
반환된 함수에 컴ㅁ포넌트를 파라미터로 넣어 주면 리덕스와 연동된 컴포넌트가 만들어진다.
> 위 코드를 다음과 같이 풀어 쓸 수 있다.
```
const makeContainer = connect(mapStateToProps, mapDispatchToProps)
makeContainer(타깃 컴포넌트)
```
<hr/>

> mapStateToProps와 mapDispatchProps에서 반환하는 객체 내부의 값들은 커모넌트의 props로 전달.
> mapStateToProps는 state를 파라미터로 받아오며, 이 값은 현재 스토어가 지니고 있는 상태.
> mapDispatchToProps의 경우 store의 내장 함수 dispatch를 파라미터로 받아온다.
