---
layout: post
title: "TIL 5일차"
subtitle: "페어프로그래밍과 TIL 양식"
type: "TIL"
createDate: "2020-06-19"
til: true
text: true
author: "hankyeolk"
post-header: false
header-img: ""
order: 5
---

#### TIL 정리 양식을 아래의 순서로 하려고 한다.

1. 오늘 배운 것 중에 가장 중요한 개념 또는 활동을 정리 : Today's Key 🔑
2. 배운 것 중에서 추가적인 공부가 필요한 것 : 추가로 공부하자 💪🏼
3. 문제를 풀었거나, 페어와 함께 알고리즘 구조를 짰다면 : 머리 뽀개기 🔥

이 3가지 항목을 꾸준히 유지하면서 작성할 예정이다. 그렇다면 오늘부터!

<br>

### Today's Key 🔑

- 지난번에 배웠던 `배열의 함수형 메소드`를 활용한 알고리즘 문제를 페어와 함께 해결했다.
- 코플릿의 알고리즘 문제를 스스로 풀어보았다. 아래에서 어려움을 겪은 문제를 풀이하고자 한다.

<br>

### 추가로 공부하자 💪🏼

- 정규 표현식에 대해서 솔직하게 공부할 시간이 필요하다.
- 재귀함수를 이용한 규칙적이고 반복적인 알고리즘 문제 해결하기

<br>

### 머리 뽀개기 🔥

배열과 문자열의 대표적인 메소드 `**.length**`를 사용하지 않고 문자열의 길이 구하기

```js
function getStringLength(string) {
  // 1. 우선적으로 빈 문자열이라면 숫자 0을 리턴한다.
  if (string === "") {
    return 0;
  } else {
    // 2. 리듀스 메소드를 활용하기 위해 문자열을 배열 형태로 바꾸었다.
    let arr = string.split("");
    return arr.reduce(function (a, b, c) {
      // 리듀서 함수에서 세번째 인자로 '인덱스'를 호출한다는 점을 이용했다.
      return c + 1;
    });
  }
}
```

- 굳이 리듀스를 사용할 필요가 있었는지 싶지만, 배운 것을 바로 생각해서 해결할 수 있다는 용기를 얻었다.
