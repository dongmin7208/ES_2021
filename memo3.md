tag.classList.
타입스크립트 알면 바로써야함.
코딩도 타입스크립트로 하는것이 좋음.
타입스크립트= 첫시간이 없을수도있다 이런것들을 다 알려줌.
new Date(); 배열을 중복없이 만들어줌. 현재시간을 해줌.
new Date(2021, 2, 31); 과거로 해줌
12월은 11,
배열처럼 0부터 시작함.
월만 0부터 시작

```
const diff = new Date(2021, 2, 3) - new Date(2021, 1, 21);
console.log(diff / 1000 / 60 / 60 / 24);

```

더 미래의 날짜에서 과거의 날짜를 빼야 합니다. 두 날짜의 차이를 구해 1000 밀리초, 60초, 60분,
24시간으로 나눠주면 며칠 차이가 나는지 나옵니다.

```
['철수','영희','현영','한솔'].reduce((a,c,i) => { a[i] = c; return a}, {})
// {0: 철수',1: '영희',2: '현영',3: '한솔'}

```

[1,2,3,4].reduce((a,c) => (a+c));
// a: 1, c:2
// a: 3, c: 3,
// a: 6, c: 4,
// 10
첫번째값 안넣으면 초기값이 첫번째값이다

p , c
현재, 이전꺼

JSON 쓰면 깊은 복사 가능하나
성능도 느리고 Math, Date같은 객체를 복사 할 수 없다는 단점이 있음
실무= lodash 같은 라이브러리(다른사람만들어둔 코드) 사용.

```
const a = 'b';
const c = ['d',true,1];
const e = {g: 'h'};
const i = [{j:'k'}, {l: 'm'}];
const n = {o: {p: 'q'}};

const a1= a;
const c1= [...c]
const e1= {...e}
const i1= JSON.parse(JSON.stringify(i))
const n1= JSON.parse(JSON.stringify(n))

```

this는 화살표 함수 안에서는 작동 안됨
그냥 펑션일때..
화살표 함수 안에서 this는 윈도우가 되어버림
