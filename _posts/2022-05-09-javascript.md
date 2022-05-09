---
layout: post
title:  " 반복문 "
---

## 08. 반복문

반복문은 특정 작업을 반복적으로 할 때 사용할 수 있는 구문입니다.

### for

for 문은 가장 기본적인 반복문입니다. 특정 값에 변화를 주어가면서 우리가 정한 조건이 만족된다면 계속 반복합니다.

```javascript
for (let i = 0; i < 10; i++) {
  console.log(i);
}
```



for 문을 사용 할 때 보통 `i++` 를 해서 1씩 증감하는 형태로 사용합니다. 그런데, 1씩 빼는 형태도 가능합니다.

```javascript
for (let i = 10; i > 0; i--) {
  console.log(i);
}
```

![](/Users/yoonsujin/Downloads/1.png)

```javascript
const result = sumOf([1, 2, 3, 4, 5]);
console.log(result);
```



#### 배열과 for

```javascript
const names = ['멍멍이', '야옹이', '멍뭉이'];

for (let i = 0; i < names.length; i++) {
  console.log(names[i]);
}
```

![img](https://i.imgur.com/XcBZTli.png)



### while

while문은 특정 조건이 참이라면 계속해서 반복하는 반복문입니다. for 문은 특정 숫자를 가지고 숫자의 값을 비교하고, 증감해주면서 반복을 한다면, while문은 조건을 확인만 하면서 반복을 합니다. 때문에, 조건문 내부에서 변화를 직접 주어야 합니다.

```javascript
let i = 0;
while (i < 10) {
  console.log(i);
  i++;
}
```

while 문을 사용 할 때에는 조건문이 언젠간 false 가 되도록 신경쓰셔야 합니다. 만약에 언젠간 false 로 전환이 되지 않는다면 반복문이 끝나지 않고 영원히 반복됩니다.



### for...of

`for...of`문은 배열에 관한 반복문을 돌리기 위해서 만들어진 반복문입니다.

```javascript
let numbers = [10, 20, 30, 40, 50];
for (let number of numbers) {
  console.log(number);
}
```

![img](https://i.imgur.com/IVuAtm1.png)



### 객체를 위한 반복문 for...in

객체를 위한 반복문을 알아보기 전에, 객체의 정보를 배열 형태로 받아올 수 있는 함수 몇가지를 알아보겠습니다.

```javascript
const doggy = {
  name: '멍멍이',
  sound: '멍멍',
  age: 2
};

console.log(Object.entries(doggy));
console.log(Object.keys(doggy));
console.log(Object.values(doggy));
```

![img](https://i.imgur.com/CUhSfvA.png)

각 함수의 역할은 다음과 같습니다.

- `Object.entries`: `[[키, 값], [키, 값]]` 형태의 배열로 변환
- `Object.keys`: `[키, 키, 키]` 형태의 배열로 변환
- `Object.values`: `[값, 값, 값]` 형태의 배열로 변환

객체가 지니고 있는 값에 대하여 반복을 하고 싶다면 위 함수들을 사용하셔도 되고, `for...in` 구문을 사용하셔도 됩니다.

```javascript
const doggy = {
  name: '멍멍이',
  sound: '멍멍',
  age: 2
};

for (let key in doggy) {
  console.log(`${key}: ${doggy[key]}`);
}
```

![img](https://i.imgur.com/rJPZwu3.png)

### break 와 continue

반복문 안에서는 `break` 와 `continue` 를 통하여 반복문에서 벗어나거나, 그 다음 루프를 돌게끔 할 수 있습니다.

```javascript
for (let i = 0; i < 10; i++) {
  if (i === 2) continue; // 다음 루프를 실행
  console.log(i);
  if (i === 5) break; // 반복문을 끝내기
}
```

i 가 2 일땐 `continue` 를 하여 원래 console.log 를 해야 하지만 그 코드를 수행하지 않고 바로 3으로 넘어갑니다.

i 가 5 일땐 `break` 를하여 반복문을 종료시킵니다.

![img](https://i.imgur.com/UmWM0tA.png)

### 연습

```javascript
function sumOf(numbers) {
  let sum = 0;
  for (let i = 0; i < numbers.length; i++) {
    sum += numbers[i];
  }
  return sum;
}

const result = sumOf([1, 2, 3, 4, 5]);
console.log(result);
```

결과는 15 입니다.



[출처]

https://learnjs.vlpt.us/basics/08-loop.html

