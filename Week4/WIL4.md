# 4주차 HTML
노션 본문 링크 : https://dramatic-elbow-87e.notion.site/4-HTML-4bf7889766264aa786142b3c08fd4f3f
노션 실습 링크2 : https://dramatic-elbow-87e.notion.site/4-bc504332ed2d4a509c4dcdcd62c0b925

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
- **기술적 마크업**(Descriptive markup): 마크업은 문서의 일부에 이름을 다는 데 사용된다. 예로, HTML의 인용의 이름을 다는 \<cite\> 태그를 들 수 있다.

## 4) Web이 머고

World Wide Web이란, 인터넷에 연결된 사용자들이 서로의 정보를 공유할 수 있는 공간을 의미한다.
줄여서 WWW, W3, Web이라고 부른다. 웹은 인터넷 상에서 텍스트나 그림, 소리, 영상 등과 같은 멀티미디어 정보를 하이퍼텍스트 방식으로 연결하여 제공한다.

\<aside\>
📌 TMI : Tim Berners-Lee란 아저씨가 World Wide Web Project 를 시작해서 www 를 만들었다.

\</aside\>

## 5) Webpage는 그럼 뭔데?

웹페이지는 월드와이드웹 상에 있는 개개의 문서이다. 웹에서는 HTML 언어를 사용하여 작성된 하이퍼텍스트 문서를 웹 페이지(web page)라고 부른다.

---

\<aside\>
📌 자세한 설명은 우측의 링크를 참조하면 된다 → [https://brunch.co.kr/@coveryou/14](https://brunch.co.kr/@coveryou/14)

\</aside\>

# 2. 구성요소

css 와 html은 자료가 너무 많아서 쓸때마다 그때그때 찾아서 하는게 효율적이다.

## 1) Tag

태그는 `여는 태그 \<`+ `태그 이름(+속성)\>`,  `닫는 태그`+ `/ 태그 이름 \>` 로 구성된다.

### A. 기본태그

| \<html\> |  | HTML 문서의 시작과 끝을 나타내는 태그 |
| --- | --- | --- |
| \<head\> |  | HTML 문서에 필요한 여러 정보를 표시하는 메타 컨테이너 |
|  | \<title\> | 브라우저 상단 타이틀 정의 |
|  | \<meta\> | 언어설정, 브라우저 호환성설정 및 모바일 화면설정과 SEO
(Search Engine Optimization) 정보를 제공 |
|  | \<body\> | • HTML의 메인 콘텐츠 영역을 정의하는 태그로 필수 요소임. 모든 콘텐츠는 \<body\>\</body\> 사이에 위치해야 함. |
|  |  | JavaScript 및 CSS 코드를 직접 작성하거나 외부 파일 import or URL link |

\> `\<body\>`를 구성하는 여러 태그들은 각각 사용 목적에 따라 필요한 태그를 선택해 콘텐츠를 제작 하면 됩니다. 다만 이들 태그들은 다음과 같이 블럭 혹은 인라인 특성을 가지고 있으므로 화면에 여러 태그를 함께 배치할 때 이러한 부분을 고려해야 합니다.
\> 

\<aside\>
📌 **블럭(Block) 태그**

블럭은 태그 구성요소들이 라인 전체를 차지해서 한줄에 여러 요소가 위치하지 못하는 태그를 말합니다.

- `\<div\>`,`\<ol\>,\<li\>`,`\<h1\>~\<h6`\>등의 태그가 대표적임
- 예를들어 `\<h1\>Hello\</h1\>world` 라고 작성했을때 world 는 다음줄에 표시됨.
\</aside\>

\<aside\>
📌 **인라인(Inline) 태그**

인라인은 태그 구성요소들이 나란히 배치될 수 있는 태그를 말합니다.

- `\<span\>`,`\<a\>`,`\<img\>`등의 태그가 대표적임.
- 예를들어 `사진1: \<img src="1.jpg"\>` 과 같이 했을때 텍스트와 사진이 나란히 배치됨.
\</aside\>

### B. 제목 태그

- 컨텐츠의 제목을 표시할때 쓰는 태그. 문자의 크기 뿐만 아니라 문서 구조를 표현하기 위해 사용.
- 검색엔진이 검색을 할때 용이하다.

`\<h\>` 태그는 `heading` 이라고 하며 `\<h1\> ~ \<h6\>`까지 있는데, 숫자들은 제목의 레벨을 나타내고,
`\<h1\>`이 가장 높은 레벨로 크기가 가장 크며 `\<h6\>`이 가장 낮은 레벨로 크기가 가장 작다.

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

`<br>`태그는 닫는 태그가 없습니다. xml 규격으로 html을 표현하는 xhtml 시스템에서는 `<br>`과 같이 xml 규격에 따라 사용 할 수 있다. 
문단 구분을 위해 `<br>` 태그를 연속으로 사용하는 것 보다 `<p>`태그를 사용하는 것이 좋다.

```html
<p> To break lines <br> in a text, <br> use the br element. </p> 
```

HTML 소스 에서는 기본적으로 하나의 공백만 인식이 되고 줄바꿈의 경우에도 별도의 태그를 사용하지 않으면 한줄로 보이게 된다. 따라서, 여러 개의 공백을 넣으려면 `&npsp;`를 사용해야 한다.

```html
Hello **&nbsp;** **&nbsp;** **&nbsp;** World   -\> Hello     World
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

| \<i\> | 이탤릭으로 텍스트를 기울임 |
| --- | --- |
| \<b\> | 굵은 글자 |
| \<tt\> | 타자기 글자 모양 |
| \<u\> | 밑줄 |
| \<strong\> | 강조 텍스트 - b 태그와 결과 동일 |
| \<sub\> | 아래첨자 |
| \<sup\> | 윗첨자 |
| \<em\> | 강조된 텍스트 - i 태그와 결과 동일 |
| \<del\> | 텍스트 취소선 |
| \<mark\> | 형광펜 형태의 하이라이트 표현 |
- `\<b\>`는 텍스트가 중요하지 않지만 단순 진하게 표시할 때, `\<strong\>`은 의미적으로 중요한 텍스트를 표시할 때 사용한다.
- `\<i\>`는 단순하게 이탤릭체로 표시할 때, `\<em\>`은 특정 텍스트에 이탤릭체로 강조된 의미를 표현 할 때 사용한다.

### E. 목록태그

목록 태그는 최신 HTML5 문서 작성에 있어 매우 중요한 태그중 하나이다. 카페나 블로그의 포스트 목록, 쇼핑몰의 상품 목록, 뉴스기사 목록 등 많은 웹 콘텐츠가 목록의 형태를 취하고 있기 때문에 이들을 표현하기 위한 목록태그는 레이아웃 지정을 위해 사용하는 `\<div\>` 와 함께 가장 많이 사용되는 태그중 하나다.

목록을 만들기 위해서는 기본적으로 `\<ul\>` 또는 `\<ol\>` 태그를 사용하며, 각각의 목록 아이템들은 `\<li\>`태그를 사용한다. 단순한 리스트 나열 뿐 아니라 메뉴를 만들 때에도 사용한다.

- `\<ol\>` Ordered List 로 번호를 메기는 순서가 있는 목록을 만든다.
- `\<ul\>` Unordered List로 순서없이 모양으로 목록을 만든다.

```html
<ul>
  <li>Listenelement 1\<li>
  <li>Listenelement 2\<li>
  <li>Listenelement 3\<li>
\<ul>
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
<a href="#m1"\>5.HTML이란 무엇인가?</a>
......
<p id="m1"></p>
<h3>5.HTML이란 무엇인가?</h3>
```

**이미지 링크**

텍스트가 아닌 이미지를 링크로 사용할 수도 있습니다. 이 경우 `\<a\>\<img\>\</a\>` 형식으로 사용하면 된다.

```html
\<a href=“http://www.gachon.ac.kr”\>
  \<img src=“gachonlogo.jpg” alt=“gachon_logo”\>
\</a\>
```

## 2) Attribute

`속성 이름` + `=` + `속성 값(value)`

\<aside\>
📌 1. 요소 이름 or 이전 attribute 와 한 칸의 공백
2. attribute name 뒤 =
3. attribute value는 인용부호 “”로 감싸기

\</aside\>

## 3) 내용

그냥 텍스트

## 4) Element(요소)

`여는 태그` + `내용` + `닫는 태그`

## 5) 문단

```html
\<p\> \</p\>
\<br/\> \<!--줄바꿈!--\>
```

\> 열면 닫아야한다. 물론 한줄짜리도 있다.
\> 

# 3. HTML document의 구성요소

## 1)\< !DOCTYPE html\>

맨 위에 Document 타입을 적어준다. 이 document는 HTML로 쓰여졌다는 뜻이다.

## 2)\<html\>…\</html\>

root element라고도 불리는 전체 페이지의 모든 content를 감싸는 element

## 3)\<head\>…\</head\>

page’s viewer에게 보이고 싶지 않은 모든걸 넣는 container, seo(검색 엔진 최적화)에서 중요한 역할을 한다.
meta-data(데이터를 설명하는 데이터), description, keywords, CSS, character set 등을 넣는다.

head에 적은것은 타이틀 외에는 안나온다. 근데 왜 필요할까? 
컴퓨터나 프로그래머에게 주는 정보가 저장되어있다(**인코딩 정보).**
메타정보가 저장되어잇다.

\<aside\>
📌 서치 엔진은 head부터 뜯어보기 때문에 head tag에 다양한 정보를 넣어주면 검색이 잘 된다.

\</aside\>

## 4)\<meta charset = “utf-8”\>

문자 인코딩 정보를 표현한다.

## 5)\<title\>…\</title\>

브라우저 탭에서 보이는 페이지의 제목

## 6)\<body\>…\</body\>

우리가 실제로 보는 부분이다. 웹사이트에 렌더링할 정보이다.
page’s viewer에게 보이고 싶은 모든 걸 넣는 container.

# 소소한 팁

- 크롬에서 F12를 누르면 개발자 도구가 뜬다. 이를 통해 페이지가 이쁠때 element(요소)를 보면 
css, html 코드를 훔쳐볼 수 있다.
- 개발자 도구 창에서 아래의 이미지를 클릭하면 편하게 요소들을 시각적으로 확인할 수 있다.

![스크린샷 2023-04-04 오후 6.51.58.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e11bd7ef-403d-467a-8d8f-315cb3eac50c/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2023-04-04_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_6.51.58.png)

# REFERENCE

1. [Web이란?](http://www.tcpschool.com/webbasic/www)
2. [마크업 언어란?](https://ko.wikipedia.org/wiki/%EB%A7%88%ED%81%AC%EC%97%85_%EC%96%B8%EC%96%B4)
3. [태그 관련](https://dinfree.com/lecture/frontend/121_html_2.html)


# 4주차 실습

# 1. HTML 기본 설정

## 1. 기본 양식 세팅하기

![스크린샷 2023-04-06 오후 2.02.06.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4c1ee49b-7f7a-4534-ae60-adc4358222ca/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2023-04-06_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_2.02.06.png)

\> vscode에 들어가서 !를 입력하고 ENTER를 입력하면 기본 양식이 자동으로 생성된다.
\> 

![스크린샷 2023-04-06 오후 2.03.17.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f86594a0-950b-44ad-9bea-10a71f8dd8d8/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2023-04-06_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_2.03.17.png)

# 2. 빙고 만들기

## 1) 주제 작성하기

뭐가 빙고하기에 좋을까 고민하다 훈련소에서 할거 없어서 했던 롤 챔피언 빙고를 하기로 마음 먹었다.

```html
\<h1\>방병훈 롤 챔피언 빙고\</h1\>
```

제목 태그를 활용해서 제목을 표시하고 자동으로 강조도 했다.

## 2) 목록 항목 작성하기

```html
\<p\>
    롤 챔피언을 주제로 만든 빙고입니다.\<br\>
    \<ul\>
        \<li\>가장 선호하는 챔피언을 하이라이트 해봅시다.\</li\>
        \<li\>가장 싫어하는 챔피언을 볼드체와 밑줄로 강조해봅시다.\</li\>
    \</ul\>
```

일단 텍스트를 출력하기 위해 `\<p\>`태그로 문단을 열었다. 그 아래에 주제를 적고 목록 항목을 적기 위해서
목록 태그를 활용했다. `\<li\>`태그로 점 표시를 구현했다.

## 3) 테이블 만들기

`\<table\>` 태그는 HTML 문서에서 표를 만드는 태그입니다.행과 열을 표현하기 위해 `\<tr\>`, `\<td\>`등의 태그와 함께 작성하게 됩니다.

예전에는 웹 페이지의 레이아웃을 구성할 때, `\<table\>` 태그를 이용하여 많이 구성하였는데 적당한 사용 방법이 아니므로레이아웃 구성시에는 [\<div\> 태그](https://ofcourse.kr/html-course/div-%ED%83%9C%EA%B7%B8)와 *CSS*를 이용 해 주세요.

- `\<tr\>` 태그는 표의 행을 나타냅니다.
- `\<td\>` 태그는 표의 열을 나타내며, `\<tr\>` 태그 하위에 위치합니다.

```html
\<table\>
    \<tr\>
        \<td\>\<mark\>리신\</mark\>\</td\>
        \<td\>자르반\</td\>
        \<td\>\<b\>\<u\>티모\</u\>\</b\>\</td\>
    \</tr\>
    \<tr\>
        \<td\>야스오\</td\>
        \<td\>앨리스\</td\>
        \<td\>조이\</td\>
    \</tr\>
    \<tr\>
        \<td\>잭스\</td\>
        \<td\>말파이트\</td\>
        \<td\>블리츠크랭크\</td\>
    \</tr\>        
\</table\>
```

## 4)테이블에 디테일 추가하기

### 1. 표의 테두리 설정하기

```html
\<style\>
    table {
        border: 1px solid #444444
    }
\</style\>
```

`\<head\>`하위에 존재하는 `\<style\>` 에서 table{ } 안에 border attribute를 통해서 테두리를 설정할 수 있다.

border 뒤에는 테두리 두께, 테두리 스타일, 테두리 색깔이 온다.(각각 1px, solid, #444444)

### 2. 테두리 두개의 실선으로 만들기

```html
\<style\>
    table {
        border: 1px solid #444444
    }
    th, td {
        border: 1px solid #444444;
    }
\</style\>
```

th, td { } 안에 border attribute를 추가해서 테두리를 다시 설정할 수 있다. 기존에는 그냥 표 외곽에만 선이 
있었다면, th, td 속성을 추가해서 테이블 열과 행 사이에 선을 만들 수 있다. **사실 \<th\>는 필요 없다.**

\<aside\>
📌 \<tr\> : ‘table row’의 약자로 테이블의 행을 의미한다.
\<th\> : ‘table header’의 약자로 테이블의 타이틀을 의미한다.
\<td\> : ‘table data’의 약자로 테이블에 들어가는 데이터, 셀을 의미한다.
즉, 하나의 테이블 안에 \<tr\> 태그로 행을 표현하고, 그 안에 \<td\> 태그를 이용하여 데이터를 표현한다.

\</aside\>

### 3. 표와 셀의 크기 수정

표와 셀의 크기는 설정되어있지 않다. 따라서 크기를 직접 설정하려면 width 속성과 height 속성을 수정해야한다.

```html
\<style\>
    table {
        border: 1px solid #444444
    }
    th, td {
        border: 1px solid #444444;
    }
\</style\>
```

1. width 속성을 변경해서 가로 크기를 수정할 수 있다. 위의 코드처럼 %를 활용하거나 px을 직접 정할수있다.
가로로 꽉찬 표를 만들고 싶다면 `width : 100%`를 하면 된다.
2. height 속성을 변경해서 세로 크기를 수정할 수 있다. 수정 방법은 width와 마찬가지이다.

## 5) input 값을 받는 칸 구현하기

### 1. input 값을 받는 네모칸 구현

```html
\<form\>
    \<br\>이번 차례에 체크할 동물 : \<input type = 'text' 
    value = '챔피언 이름을 입력하세요..' 
    name = 'name'/\>
\</form\>
```

### 2. label 태그 적용

```html
\<form\>
   \<br\>\<label for = "inputChamp"\>이번 차례에 체크할 동물 :\</label\>
   \<input type = 'text'
   id = 'inputChamp'
   value = '챔피언 이름을 입력하세요..' 
   name = 'name'/\>
\</form\>
```

# Tag들의 자세한 속성

## 1. \<table\>

### border-style 속성

border-style 속성을 이용하면 테두리(border)를 다양한 모양으로 설정할 수 있습니다.

- dotted : 테두리를 점선으로 설정함.
- dashed : 테두리를 약간 긴 점선으로 설정함.
- solid : 테두리를 실선으로 설정함.
- double : 테두리를 이중 실선으로 설정함.
- groove : 테두리를 3차원인 입체적인 선으로 설정하며, border-color 속성값에 영향을 받음.
- ridge : 테두리를 3차원인 능선효과가 있는 선으로 설정하며, border-color 속성값에 영향을 받음.
- inset : 테두리를 3차원인 내지로 끼운 선으로 설정하며, border-color 속성값에 영향을 받음.
- outset : 테두리를 3차원인 외지로 끼운 선으로 설정하며, border-color 속성값에 영향을 받음.
- none : 테두리를 없앰.
- hidden : 테두리가 존재하기는 하지만 표현되지는 않음.
- 코드
    
    ```html
    \<style\>
    
        .dotted {border-style: dotted;}
    
        .dashed {border-style: dashed;}
    
        .solid {border-style: solid;}
    
        .double {border-style: double;}
    
        .groove {border-style: groove;}
    
        .ridge {border-style: ridge;}
    
        .inset {border-style: inset;}
    
        .outset {border-style: outset;}
    
        .none {border-style: none;}
    
        .hidden {border-style: hidden;}
    
        .mix {border-style: solid dashed dotted double;}
    
    \</style\>
    ```
    

### border-width 속성

border-width 속성은 테두리(border)의 두께를 설정한다.

px, em, cm 등과 같은 CSS 크기 단위를 이용하여 두께를 직접 설정할 수 있다.

또한, 미리 설정해 놓은 예약어인 thin, medium, thick을 사용하여 설정할 수도 있다.

- 코드
    
    ```html
    \<style\>
    
        .dottedA { border-style: dotted; border-width: 2px; }
    
        .dottedB { border-style: dotted; border-width: 5px; }
    
        .dashedA { border-style: dashed; border-width: thin; }
    
        .dashedB { border-style: dashed; border-width: thick; }
    
        .doubleA { border-style: double; border-width: 5px; }
    
        .doubleB { border-style: double; border-width: thick; }
    
        .mix { border-style: solid; border-width: 1px 2px 10px thick; }
    
    \</style\>
    ```
    

### border-color 속성

border-color 속성은 테두리(border)의 색상을 설정한다.

기본적인 color 속성값들뿐만 아니라 투명한 선을 나타내는 transparent 속성값을 사용할 수도 있다.

border-color 속성값이 설정되지 않으면 해당 요소의 color 속성값을 그대로 물려받는다.

- 코드
    
    \<style\>
    
    .red { border-color: red; }
    
    .green { border-color: rgb(**0,255,0**); }
    
    .blue { border-color: **#0000FF**; }
    
    .mix { border-color: red green blue maroon; }
    
    .color { color: teal; }
    
    \</style\>
    

## 2. input

input 태그는 사용자로부터 정보를 입력받기위해 사용한다. type attribute를 통해서 다양한 입력 양식을 
정할 수 있다. 

대표적인 속성으로는 

1. type : 입력 태그의 유형
2. value : 입력 태그의 초기값으로 사용자가 변경 가능하다.
3. name : 서버로 전달되는 이름.(사용자 임의 지정)

### 1. type

| hidden | 사용자에게 안보임 | text | 텍스트 입력 | search | 검색 상자 |
| --- | --- | --- | --- | --- | --- |
| tel | 전화번호 입력 | url | Url 주소 입력 | email | 이메일 입력 |
| password | 비밀번호 입력 | datetime | 국제 표준시 삽입 | date | 사용자 지역 연/월/일 삽입 |
| month | 사용자 지역 연/월 삽입 | week | 사용자 지역 연/주 삽입 | time | 사용자 지역 시/분/초 삽입 |
| number | 숫자 조절 화살표 | range | 숫자 조절 슬라이드 막대 | color | 색상표 삽입 |
| checkbox | 체크박스 삽입 | radio | 라디오 버튼 삽입 | file | 파일 첨부 버튼 |
| submit | 서버 전송 버튼 | reset | 리셋 버튼 삽입 | button | 버튼 삽입 |

### 2. value

value 속성은 \<input\> 요소의 type 속성값에 따라 다른 용도로 사용된다.

- “button”, “reset”, “submit” : 버튼 내의 텍스트를 정의함.
- “hidden”, “password”, “text” : 입력 필드의 초깃값을 정의함.
- “checkbox”, “image”, “radio” : 해당 입력 필드를 선택 시 서버로 제출되는 값을 정의함.
- 또한, \<input\> 요소의 type 속성값이 “file”인 경우에는 value 속성을 사용할 수 없다.

### 3. name

\<input\> 태그의 name 속성은 \<input\> 요소의 이름을 명시한다.

name 속성은 폼(form)이 제출된 후 서버에서 폼 데이터(form data)를 참조하기 위해 사용되거나, 자바스크립트에서 요소를 참조하기 위해 사용된다.

\<aside\>
📌 자세한 속성을 알고싶다면 하단의 링크를 참조하기 바란다 
→ [http://www.tcpschool.com/html-tags/input](http://www.tcpschool.com/html-tags/input)

\</aside\>

## 3. label

이러한 \\<label\> 요소는 브라우저에 의해 일반적인 텍스트로 랜더링되지만, 사용자가 마우스로 해당 텍스트를 클릭할 경우 \\<label\> 요소와 연결된 요소를 곧바로 선택할 수 있어 사용자의 편의성을 높일 수 있다.

- label은 폼의 양식에 이름 붙이는 태그이다.
- 주요 속성은 for이다. label의 for의 값과 양식의 id의 값이 같으면 연결된다.
- label을 클릭하면, 연결된 양식에 입력할 수 있도록 하거나, 체크를 하거나, 체크를 해제한다.

# REFERENCE

1. [\\<table\> 태그](https://ofcourse.kr/html-course/table-%ED%83%9C%EA%B7%B8)
2. [border attribute](https://ofcourse.kr/css-course/border-%EC%86%8D%EC%84%B1)
3. [표 크기 수정하기](https://www.codingfactory.net/10501)
4. [표 테두리 설정하기](https://www.codingfactory.net/10510)
5. [테이블 자세한 속성](http://www.tcpschool.com/css/css_boxmodel_borders)
6. [input 태그의 속성](https://yangbari.tistory.com/28)
[type attribute](https://alvine.tistory.com/161)
[value attribute](http://www.tcpschool.com/html-tag-attrs/input-value)
[name attribute](http://www.tcpschool.com/html-tag-attrs/input-name)
7. [\\<label\> 태그](http://www.tcpschool.com/html-tags/label)
[\<label\> 태그2](https://abcdqbbq.tistory.com/63)