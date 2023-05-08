# 6주차 CSS 2

[스터디 과제 정리](https://www.notion.so/c8d9a43b1d3f4a31b91d02871fff6054)

# Box model과 FLEX Box

# 1. Box model

박스 모양으로 그 안에 요소들이 들어간다. 박스의 테두리를 border라고 한다. 

![Untitled](6%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20CSS%202%201569a18adc314d72ad6a7fe607333980/Untitled.png)

## 1) 블록 레벨 요소

한 줄을 차지하는 박스. 부모 요소의 전체 칸을 차지한다. ex) <div>, <p> … 여기서 부모요소는 <head>

## 2) 인라인 레벨 요소

자신 만을 감싸는 박스이다. ex) span, strong

## border

박스를 감싸고 있는 테두리이다.

## content

박스 안에 들어가는 내용이다.

## padding

컨텐츠와 보더 사이의 간격

## margin

Border로 부터 다른 컨텐츠 사이의 여백. `margin : **위 오른쪽 아래 왼쪽`** 순서로 특정해서 정해줄 수 있다. 
이 순서는 padding도 마찬가지이다. 보통은 위아래 간격 같고 좌우 간격이 같은 경우가 있다.
`margin : 위아래 좌우` 로 두개만 적으면 두번만 적으면 위아래 좌우에 적용이 된다.

<aside>
📌 F12를 눌러서 개발자 도구를 확인할 수 있다. 맨 밑으로 내리면 박스가 나오는데 이를 통해 내 코드의 
문제점과 제대로 적용됐는지를 확인할 수 있다.

</aside>

# 2. Flexbox Layout

아이템이 배열될 방향인 ‘주축’을 정할 수 있다. 주축과 수직한 축을 cross axis라고 부른다. 주축을 main axis라고 한다. 주축은 row와 column 방향으로 정할 수 있다. row는 좌우방향, column은 상하방향

이를 통해 아이템이 특정 축에서 어떻게 적용될지 정할 수 있다. 

justify-content : main axis

align-item : cross axis

플렉스 박스 안에 플렉스 박스를 넣으면서 디테일을 추가할 수 있다.

# 추가로 공부할 것

1. CSS Grid Layout
2. [Can I use](https://caniuse.com/)
    
    css를 그리는 건 브라우저라 버전을 많이 탄다. 따라서 어느 브라우저 몇 번째 버전부터 확인할 수 있는 
    사이트이다. 사용가능한 API도 확인가능하다.

# 스터디 과제 정리

## 1. justify-content

이 속성은 다음의 값들을 인자로 받아 요소들을 가로선 상에서 정렬합니다.

- **`flex-start`**: 요소들을 컨테이너의 왼쪽으로 정렬합니다.
- **`flex-end`**: 요소들을 컨테이너의 오른쪽으로 정렬합니다.
- **`center`**: 요소들을 컨테이너의 가운데로 정렬합니다.
- **`space-between`**: 요소들 사이에 동일한 간격을 둡니다.
- **`space-around`**: 요소들 주위에 동일한 간격을 둡니다.

## align-items

이 CSS 속성은 다음의 값들을 인자로 받아 요소들을 세로선 상에서 정렬합니다.

- **`flex-start`**: 요소들을 컨테이너의 꼭대기로 정렬합니다.
- **`flex-end`**: 요소들을 컨테이너의 바닥으로 정렬합니다.
- **`center`**: 요소들을 컨테이너의 세로선 상의 가운데로 정렬합니다.
- **`baseline`**: 요소들을 컨테이너의 시작 위치에 정렬합니다.
- **`stretch`**: 요소들을 컨테이너에 맞도록 늘립니다.

## flex-direction

아래의 값들을 인자로 받아 컨테이너 안에서 요소들이 정렬해야 할 방향을 정해준다.

- **`row`**: 요소들을 텍스트의 방향과 동일하게 정렬합니다.
- **`row-reverse`**: 요소들을 텍스트의 반대 방향으로 정렬합니다.
- **`column`**: 요소들을 위에서 아래로 정렬합니다.
- **`column-reverse`**: 요소들을 아래에서 위로 정렬합니다.

<aside>
📌 column-reverse 또는 row-reverse를 사용하면 요소들의 start와 end의 순서도 뒤바뀐다.

</aside>

<aside>
📌 Flex의 방향이 column일 경우 **`justify-content`**의 방향이 세로로, **`align-items`**의 뱡향이 가로로 바뀝니다.

</aside>

## flex-wrap

- **`nowrap`**: 모든 요소들을 한 줄에 정렬합니다.
- **`wrap`**: 요소들을 여러 줄에 걸쳐 정렬합니다.
- **`wrap-reverse`**: 요소들을 여러 줄에 걸쳐 반대로 정렬합니다.

## flex-flow

**`flex-direction`**과 **`flex-wrap`**이 자주 같이 사용되기 때문에, **`flex-flow`**가 이를 대신할 수 있습니다. 이 속성은 공백문자를 이용하여 두 속성의 값들을 인자로 받습니다.

예를 들어, 요소들을 가로선 상의 여러줄에 걸쳐 정렬하기 위해 **`flex-flow: row wrap`**을 사용할 수 있습니다.