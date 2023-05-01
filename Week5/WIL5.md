# 1. HTML(Hyper Text Markup Language)

## 1)HTML이란?

Hyper Text Markup Language의 약어로 hyper text 기능을 가진 문서를 만드는 언어이다.
웹페이지를 위한 마크업 언어라고 생각하면 된다.

## 2) 하이퍼 텍스트

밑줄 쳐져 있는 문자열로 누르면 해당 사이트로 연결이 된다. 
책처럼 한장 한장 찾는게 아니라 정보의 접근에 순차적인 접근을 초월하게 해준다

## 3)마크업 언어?

태그 등을 이용해서 문서나 데이터의 구조를 명시하는 언어이다. 태그는 원래 텍스트와는 별도로 원고의 교정부호 및 주석을 표현하기 위한 것이었으나 용도가 점차 확장되어 문서의 구조를 표현하는 역할을 하게 되었다.

전자적 마크업의 일반적인 분류에는 세 가지가 있다:[[1]](https://ko.wikipedia.org/wiki/%EB%A7%88%ED%81%AC%EC%97%85_%EC%96%B8%EC%96%B4#cite_note-1)[[2]](https://ko.wikipedia.org/wiki/%EB%A7%88%ED%81%AC%EC%97%85_%EC%96%B8%EC%96%B4#cite_note-2)

- **표현적 마크업**(Presentational markup): 전통적인 워드 처리 시스템이 사용하는 마크업. [위지위그](https://ko.wikipedia.org/wiki/%EC%9C%84%EC%A7%80%EC%9C%84%EA%B7%B8) 효과를 내는 문서 텍스트에 포함되니 이진 코드. 이러한 마크업은 사람(저자나 편집자도 포함)의 눈에는 보이지 않도록 설계되는 것이 일반적이다.
- **절차적 마크업**(Procedural markup): 마크업은 텍스트에 포함되며 문자를 처리할 프로그램의 명령을 제공한다. [troff](https://ko.wikipedia.org/w/index.php?title=Troff&action=edit&redlink=1), [LaTeX](https://ko.wikipedia.org/wiki/LaTeX), [포스트스크립트](https://ko.wikipedia.org/wiki/%ED%8F%AC%EC%8A%A4%ED%8A%B8%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8)를 예로 들 수 있다.
- **기술적 마크업**(Descriptive markup): 마크업은 문서의 일부에 이름을 다는 데 사용된다. 예로, HTML의 인용의 이름을 다는 <cite> 태그를 들 수 있다.

## 4) Web이 머고

World Wide Web이란, 인터넷에 연결된 사용자들이 서로의 정보를 공유할 수 있는 공간을 의미한다.
줄여서 WWW, W3, Web이라고 부른다. 웹은 인터넷 상에서 텍스트나 그림, 소리, 영상 등과 같은 멀티미디어 정보를 하이퍼텍스트 방식으로 연결하여 제공한다.

<aside>
📌 TMI : Tim Berners-Lee란 아저씨가 World Wide Web Project 를 시작해서 www 를 만들었다.

</aside>

## 5) Webpage는 그럼 뭔데?

웹페이지는 월드와이드웹 상에 있는 개개의 문서이다. 웹에서는 HTML 언어를 사용하여 작성된 하이퍼텍스트 문서를 웹 페이지(web page)라고 부른다.

---

<aside>
📌 자세한 설명은 우측의 링크를 참조하면 된다 → [https://brunch.co.kr/@coveryou/14](https://brunch.co.kr/@coveryou/14)

</aside>

# 2. 구성요소

css 와 html은 자료가 너무 많아서 쓸때마다 그때그때 찾아서 하는게 효율적이다.

## 1) Tag

태그는 `여는 태그 <`+ `태그 이름(+속성)>`,  `닫는 태그`+ `/ 태그 이름 >` 로 구성된다.

### A. 기본태그

| <html> |  | HTML 문서의 시작과 끝을 나타내는 태그 |
| --- | --- | --- |
| <head> |  | HTML 문서에 필요한 여러 정보를 표시하는 메타 컨테이너 |
|  | <title> | 브라우저 상단 타이틀 정의 |
|  | <meta> | 언어설정, 브라우저 호환성설정 및 모바일 화면설정과 SEO
(Search Engine Optimization) 정보를 제공 |
|  | <body> | • HTML의 메인 콘텐츠 영역을 정의하는 태그로 필수 요소임. 모든 콘텐츠는 <body></body> 사이에 위치해야 함. |
|  |  | JavaScript 및 CSS 코드를 직접 작성하거나 외부 파일 import or URL link |

> `<body>`를 구성하는 여러 태그들은 각각 사용 목적에 따라 필요한 태그를 선택해 콘텐츠를 제작 하면 됩니다. 다만 이들 태그들은 다음과 같이 블럭 혹은 인라인 특성을 가지고 있으므로 화면에 여러 태그를 함께 배치할 때 이러한 부분을 고려해야 합니다.
> 

<aside>
📌 **블럭(Block) 태그**

블럭은 태그 구성요소들이 라인 전체를 차지해서 한줄에 여러 요소가 위치하지 못하는 태그를 말합니다.

- `<div>`,`<ol>,<li>`,`<h1>~<h6`>등의 태그가 대표적임
- 예를들어 `<h1>Hello</h1>world` 라고 작성했을때 world 는 다음줄에 표시됨.
</aside>

<aside>
📌 **인라인(Inline) 태그**

인라인은 태그 구성요소들이 나란히 배치될 수 있는 태그를 말합니다.

- `<span>`,`<a>`,`<img>`등의 태그가 대표적임.
- 예를들어 `사진1: <img src="1.jpg">` 과 같이 했을때 텍스트와 사진이 나란히 배치됨.
</aside>

### B. 제목 태그

- 컨텐츠의 제목을 표시할때 쓰는 태그. 문자의 크기 뿐만 아니라 문서 구조를 표현하기 위해 사용.
- 검색엔진이 검색을 할때 용이하다.

`<h>` 태그는 `heading` 이라고 하며 `<h1> ~ <h6>`까지 있는데, 숫자들은 제목의 레벨을 나타내고,
`<h1>`이 가장 높은 레벨로 크기가 가장 크며 `<h6>`이 가장 낮은 레벨로 크기가 가장 작다.

```html
<h1>This is heading 1</h1>
<h2>This is heading 2</h2>
<h3>This is heading 3</h3>
<h4>This is heading 4</h4>
<h5>This is heading 5</h5>
<h6>This is heading 6</h6>
```

### C. 문단 태그

`<p>`태그는 `paragraph`로 문단을 구분하기 위해 사용한다. HTML에서는 연속된 공백이나 줄 바꿈은 하나의 공백으로 처리하기 때문에 문단 구분 시 `<p>`태그를, 줄 바꿈시 `<br>`태그를 이용한다.

```html
<p>This is a paragraph.</p>
```

`<br>`태그는 닫는 태그가 없습니다. xml 규격으로 html을 표현하는 xhtml 시스템에서는 `</br>`과 같이 xml 규격에 따라 사용 할 수 있다. 
문단 구분을 위해 `<br>` 태그를 연속으로 사용하는 것 보다 `<p>`태그를 사용하는 것이 좋다.

```html
<p> To break lines <br> in a text, <br> use the br element. </p> 
```

HTML 소스 에서는 기본적으로 하나의 공백만 인식이 되고 줄바꿈의 경우에도 별도의 태그를 사용하지 않으면 한줄로 보이게 된다. 따라서, 여러 개의 공백을 넣으려면 `&npsp;`를 사용해야 한다.

```html
Hello **&nbsp;** **&nbsp;** **&nbsp;** World   -> Hello     World
```

소스에 작성한 그대로를 화면에 출력하려면 `pre` 태그를 활용하면 된다.

```html
<pre>
Hello
  World           !!!
</pre>
```

### D. 형식태그

형식 지정 태그들은 텍스트에 의미와 함께 효과를 부여한다.

| <i> | 이탤릭으로 텍스트를 기울임 |
| --- | --- |
| <b> | 굵은 글자 |
| <tt> | 타자기 글자 모양 |
| <u> | 밑줄 |
| <strong> | 강조 텍스트 - b 태그와 결과 동일 |
| <sub> | 아래첨자 |
| <sup> | 윗첨자 |
| <em> | 강조된 텍스트 - i 태그와 결과 동일 |
| <del> | 텍스트 취소선 |
| <mark> | 형광펜 형태의 하이라이트 표현 |
- `<b>`는 텍스트가 중요하지 않지만 단순 진하게 표시할 때, `<strong>`은 의미적으로 중요한 텍스트를 표시할 때 사용한다.
- `<i>`는 단순하게 이탤릭체로 표시할 때, `<em>`은 특정 텍스트에 이탤릭체로 강조된 의미를 표현 할 때 사용한다.

### E. 목록태그

목록 태그는 최신 HTML5 문서 작성에 있어 매우 중요한 태그중 하나이다. 카페나 블로그의 포스트 목록, 쇼핑몰의 상품 목록, 뉴스기사 목록 등 많은 웹 콘텐츠가 목록의 형태를 취하고 있기 때문에 이들을 표현하기 위한 목록태그는 레이아웃 지정을 위해 사용하는 `<div>` 와 함께 가장 많이 사용되는 태그중 하나다.

목록을 만들기 위해서는 기본적으로 `<ul>` 또는 `<ol>` 태그를 사용하며, 각각의 목록 아이템들은 `<li>`태그를 사용한다. 단순한 리스트 나열 뿐 아니라 메뉴를 만들 때에도 사용한다.

- `<ol>` Ordered List 로 번호를 메기는 순서가 있는 목록을 만든다.
- `<ul>` Unordered List로 순서없이 모양으로 목록을 만든다.

```html
<ul>
  <li>Listenelement 1</li>
  <li>Listenelement 2</li>
  <li>Listenelement 3</li>
</ul>
```

**결과**

- Listenelement 1
- Listenelement 2
- Listenelement 3

```html
<ol>
  <li>Listenelement 1</li>
  <li>Listenelement 2</li>
  <li>Listenelement 3</li>
</ol>
```

**결과**

1. Listenelement 1
2. Listenelement 2
3. Listenelement 3

### E. 하이퍼 링크

하이퍼링크는 웹의 대표적인 특징으로 `<a>`(Anchor)태그를 사용해 만들수 있다. `href`속성을 사용해 이동할 콘텐츠의 주소를 기술하면 된다. 이동할 콘텐츠는 html 파일이나 이미지 혹은 .hwp, .pdf 등 모든 파일이 될 수 있으며 URL을 이용해 서버의 콘텐츠를 지정하거나 프로그램을 호출하는 것도 가능하다.

다른 서버 컨텐츠로 이동하는 것이라면 href 에 `http://` 로 시작하는 URL이 들어가야 합니다.

```html
<a href="이동할 콘텐츠" title="말풍선 도움말" target="브라우저 윈도우 옵션">링크 텍스트</a>
```

`href` 에 들어가는 이동할 콘텐츠의 위치는 상대경로와 절대경로로 표현할 수 있다. 내 컴퓨터가 아니라 html 을 서비스하고 있는 웹서버 컴퓨터에서 콘텐츠간의 위치 이므로 개념을 잘 이해해야 한다.

**상대경로와 절대경로**

- 절대경로 : 고유한 경로로 root(/)로부터 시작되는 위치로 지정하는 방법.
예)/home/contents/img/1.jpg
- 상대경로 : HTML 문서를 기준으로 경로를 지정하는 방법.  
예) img/1.jpg, ../contents/img/1.jpg
- 내 컴퓨터의 컨텐로 연결하기 위해 `c:\user\Document\Desktop\hello.html`과 같이 로컬 컴퓨터의 
절대 경로를 사용해서는 안됨.

**target 속성 값**

- `_blank` : 새로운 웹 브라우저 창으로 오픈.
- `_self`   : 현재 웹 브라우저 창으로 오픈. (기본값)
- `_parent`: 부모 웹 브라우저 창으로 오픈.
- `_top`     : 웹 브라우저 전체 영역에 오픈.

**책갈피 구현**

- `<a>`태그를 이용해 같은 문서 내에서 특정 위치로 이동하는 책갈피 기능을 구현할 수 있음.
- `<p>`태그의 `name`속성이나 `id`속성을 이용해 문서 내 이동위치를 지정하고 하이퍼링크에 `href=#name(id)` 과 같이 이동할 위치를 지정함.

```html
메뉴 
<a href="#m1">5.HTML이란 무엇인가?</a>
......
<p id="m1"></p>
<h3>5.HTML이란 무엇인가?</h3>
```

**이미지 링크**

텍스트가 아닌 이미지를 링크로 사용할 수도 있습니다. 이 경우 `<a><img></a>` 형식으로 사용하면 된다.

```html
<a href=“http://www.gachon.ac.kr”>
  <img src=“gachonlogo.jpg” alt=“gachon_logo”>
</a>
```

## 2) Attribute

`속성 이름` + `=` + `속성 값(value)`

<aside>
📌 1. 요소 이름 or 이전 attribute 와 한 칸의 공백
2. attribute name 뒤 =
3. attribute value는 인용부호 “”로 감싸기

</aside>

## 3) 내용

그냥 텍스트

## 4) Element(요소)

`여는 태그` + `내용` + `닫는 태그`

## 5) 문단

```html
<p> </p>
<br/> <!--줄바꿈!-->
```

> 열면 닫아야한다. 물론 한줄짜리도 있다.
> 

# 3. HTML document의 구성요소

## 1)< !DOCTYPE html>

맨 위에 Document 타입을 적어준다. 이 document는 HTML로 쓰여졌다는 뜻이다.

## 2)<html>…</html>

root element라고도 불리는 전체 페이지의 모든 content를 감싸는 element

## 3)<head>…</head>

page’s viewer에게 보이고 싶지 않은 모든걸 넣는 container, seo(검색 엔진 최적화)에서 중요한 역할을 한다.
meta-data(데이터를 설명하는 데이터), description, keywords, CSS, character set 등을 넣는다.

head에 적은것은 타이틀 외에는 안나온다. 근데 왜 필요할까? 
컴퓨터나 프로그래머에게 주는 정보가 저장되어있다(**인코딩 정보).**
메타정보가 저장되어잇다.

<aside>
📌 서치 엔진은 head부터 뜯어보기 때문에 head tag에 다양한 정보를 넣어주면 검색이 잘 된다.

</aside>

## 4)<meta charset = “utf-8”>

문자 인코딩 정보를 표현한다.

## 5)<title>…</title>

브라우저 탭에서 보이는 페이지의 제목

## 6)<body>…</body>

우리가 실제로 보는 부분이다. 웹사이트에 렌더링할 정보이다.
page’s viewer에게 보이고 싶은 모든 걸 넣는 container.

# 소소한 팁

- 크롬에서 F12를 누르면 개발자 도구가 뜬다. 이를 통해 페이지가 이쁠때 element(요소)를 보면 
css, html 코드를 훔쳐볼 수 있다.

# 1. CSS(Cascading Style Sheet)이란?

쉽게 말해서 스타일을 정해주는 시트이다.

# 2. Cascading?

## 1) 상속

1. 수 많은 html 태그가 있는데, 자식에게 부모의 스타일을 상속할 수 있다면?
    
    → 편리하다.
    
2. 만약 한 요소에 여러 스타일이 적용된다면?
    
    → 어떤걸 적용해야하는 지의 문제
    

Dom(document object model) : 트리구조

## 2) 우선순위

스타일 시트 

→ 브라우저 기본 스타일

→사용자 스타일

→인라인 스타일

→내부 스타일 시트

→외부 스타일 시트

1. 사용자 스타일(컴퓨터 사용자)
    
    아무리 개발자가 열심히 스타일을 해도 사용자가 스타일을 지정하면 우선시 된다.
    
2. 제작자 스타일(개발자)
3. 브라우저 기본 스타일
- 만약 두가지 스타일이 겹친다면(서열이 같다면) 세부적인 서열 관계가 있다.
    1. !important
    2. 인라인 스타일
    3. id 스타일
    4. 클래스 스타일
    5. 타입 스타일

→ Selector를 통해 지정 가능

### Selector(선택자)란?

div 와 같은 것

```html
h1{color:red;font-size:12px}
```

→h1이 selector이다. color는 property, red 는 property value이다.

color:red는 선언, { }안은 선언 블록.

| 선택자 | 패턴 | 설명 |
| --- | --- | --- |
| id 선택자 | #아이디{속성:값…} | 특정 아이디를 가진 요소에 적용 |
| class 선택자 | .클래스{속성:값…} | 특정 클래스를 가진 모든 요소에 적용 |
| 타입 선택자 | 태그{속성:값…} |  |
| 전체 선택자 | *{속성:값…} |  |