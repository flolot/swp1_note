# Lecture 2 (2015/9/10)
---
## Part 1: HTML CSS Basics
###Chapter 1: Basics of HTML
- The basic structure of HTML
<!DOCTYPE html> HTML5 최신 웹 표준을 사용하겠다는 선언(항상 맨 위에 작성해야 함)
<html>...</html> HTML의 시작과 끝
<head>...</head> 웹 페이지의 제목과 정보를 구성하는 태그들이 위치하는 문서의 서문 영역
<body>...</body> 실제로 화면에 보여지게 될 문서의 본문 영역
- <title> element - 웹 브라우저 탭에 보이는 웹 페이지의 제목을 정의하는 태그
- <meta> element- 한글 깨지는 현상 방지, 메타 데이터 = 문서의 정보, <meta>는 닫기 태그가 없으며 <title>과 마찬가지로 <head>...</head> 사이에 작성해야 함
- <h1> element - <h1>, <h2>, <h3>, <h4>, <h5>, <h6>는 본문의 표제 역할
- <p> element -  문단을 나눌 때 사용함함 
※ HTML 문서에서는 두 칸 이상의 공백이나 줄바꿈이 하나의 공백으로 출력
- <br> element -  줄바꿈을 함
- <hr> element - 수평선,  닫는 태그가 없음
- <pre> element - 예외로 공백과 줄바꿈을 그대로 보여주는 태그
- <div> element - 레이아웃을 만드는 데 가장 많이 쓰이는 태그, 부모의 너비나 브라우저의 너비 만큼 꽉 채워진다는 특징이 있으며, 여러 태그들을 감싸 하나의 그룹 영역을 만드는 것이 주 역할
 
### Chapter 2: Basics of CSS
- How to apply class - HTML 태그로 만들어진 요소와 구조에 디자인을 적용하는 역할
인라인 방식 - 태그에 style 속성을 추가하여 그 안에 직접 CSS 코드를 작성하는 방식
```html
<태그 class="클래스이름"></태그>
```
태그는 단 하나의 id(이름)를 갖고, 동시에 여러 class(종류)를 가질 수 있음
```html
//사람(class)인 샘(id)은 학생(class) 또는 선생님(class)이 될 수 있다.
<div class="human student" id="sam"></div>
<div class="human teacher" id="sam"></div>
```
내부 스타일 시트
<head>...</head> 안에 <style>을 작성하는 스타일
외부 스타일 시트
HTML 문서 외의 CSS 파일을 따로 분리하는 스타일
- CSS 작성 규칙
모든 CSS 속성은 {} 안에 포함되어야 한다.
class를 선택할 때는 이름 앞에 .을 붙인다.
id를 선택할 때는 이름 앞에 #을 붙인다.
CSS 속성들은 ;으로 구분된다.
- <link> element - HTML 파일에서 외부 파일을 불러올 때 사용
rel="stylesheet" CSS 파일을 불러올 때 추가하는 속성
media="all" 모든 디바이스에서 불러올 때 추가하는 속성
href="css/style.css" 불러올 파일(css 폴더 속의 style.css)의 경로

## Part 2: How to use semantic elements
시맨틱 태그란 HTML5에서 새롭게 추가된, 문서의 구조를 만드는 요소
### Chapter 1: header and footer
- <header> element - 주로 사이트의 상단에 위치하여 로고, 메뉴, 머리말 등의 용도로 사용
- <footer> element - 주로 사이트의 하단에 위치하여 저작권 정보, 꼬리말 등의 용도로 사용
![image](https://s3-ap-northeast-1.amazonaws.com/toycode/images/content/html_css_basic_ko/semantic_layout.jpg)
![image](https://s3-ap-northeast-1.amazonaws.com/toycode/images/content/html_css_basic_ko/padding_10px.jpg)


### Chapter 2: nav and section
- Semantic element - <nav> element - 네비게이션, 사이트 메뉴 역할
- Semantic element - <section> element - 영역을 나누는 태그
- <nav> and  <section> elements - apply css
float 속성- float는 정렬에 관련된 CSS 속성으로 대표적인 속성값으로 left, right가 있음
overflow: hidden은 어떤 요소 속의 내용이 너무 많아서 그 요소의 영역에 내용을 다 담아내지 못해서 영역 바깥으로 넘쳐날 경우 넘치는 부분을 보이지 않도록 합니다.
overflow: scroll은 일단 넘치는 부분을 보이지 않게 하되 요소에 스크롤 바를 만들어서 스크롤링을 통하여 볼 수 있도록 함
overflow: hidden 요소 너비 = 부모 너비 - float 요소 너비
float 요소 뒤에 overflow: hidden 요소가 붙게 될 것이고 한 층에 좌우로 배치될 것입니다.

- <body> element - remove white space 
```html
body {
  margin: 0;
}
```

## Part 3: Practice HTML elements
### Chapter 1: accents and link elements
인라인 요소
- <b> and <strong> elements  = font-weight: bold;
<b>와 <strong>은 텍스트를 굵게 만들어주는 인라인 요소
- <i> and <em> elements = font-style: italic;
- Inset a line between <section> elements - border-bottom: 1px solid black;
- <span> element using style or class- 아무 효과도 없는 인라인 요소 태그
- <a> element- insert a link
<a>의 target 속성을 지정하지 않은 채로 링크를 클릭하면 현재 페이지가 이동할 페이지로 전환
하지만 target 속성에 _blank라는 값을 넣으면 이동할 페이지가 새 탭에서 띄워짐

### Chapter 2: list and table
![image](https://s3-ap-northeast-1.amazonaws.com/toycode/images/content/html_css_basic_ko/ui_li.jpg)
- <ol> element -  Ordered List의 줄임말로 순서가 있는 리스트
- <li> element
- <li> and <a> elements - make a side menu
a 태그 href 속성에 페이지 주소 대신 #li-tag같은 id를 넣어주면 현재 페이지 내에서 해당 id를 가지고 있는 영역으로 화면이 이동
- <nav> and <a> elements - remove underline - text-decoration: none;
- <nav> and <span> elements - apply css
- <nav> - widen space between texts - line-height: 30px;
- <table> element
th - 제목 셀
tr - 행
td - 내용 셀(열)
table border 속성 - 테이블의 선 두께

### Chapter 3: form
폼 태그에 로그인 정보 입력 -> 제출 -> 확인 -> 로그인 성공
- <form> element - basics - 사용자와 상호작용하기 위한 태그
- <input type="text"> 와 같은 형태는 한 줄 정도를 입력할 수 있는 텍스트 입력창
- <textarea> 여러 줄의 텍스트를 입력받고 싶을 때
rows="10" cols="50"을 입력하게 되면 세로로 10줄 가로로 50자 정도의 크기
- <input type="radio" name ="[name]" value ="[value]" >
- <select name="[name]">
    <option value="[value]">
- <input type="submit" value ="[value]">

## Part 4: Properties of CSS
### Chapter 1: work on an album cover
- 배경 이미지를 지정
background: url("이미지 주소") no repeat; 
- 이미지의 비율을 잃지 않고 자연스럽게 보여줌
background-size: cover; 
- 여백 활용하기
여백: 10px; // 모든 방향에 10px의 여백
여백: 10px 20px; // 위쪽 아래쪽에 10px, 오른쪽 왼쪽에 20px의 여백
여백: 10px 20px 30px 40px; // 위쪽 10px, 오른쪽 20px, 아래쪽 30px, 왼쪽 40px의 여백(시계 방향)
- 요소 반투명하게 만들기
opacity: 0.5;

### Chapter 2: add hover class
hover 클래스를 부모로 가지고 있는 title 클래스에 마우스가 닿았을 때,
중괄호({}) 안에 작성된 css 속성이 해당 title 클래스에 지정
```html
.hover .title:hover {
  ...
}
```
border-radius는 모서리를 둥글게 만드는 css 속성
속성값으로 픽셀(px) 단위, 퍼센트(%) 단위 등을 사용할 수 있는데,
50% 이상의 퍼센트 단위로 지정하면 원형

### Chapter 3: optimize for mobiles
- 반응형 웹
접속한 디바이스(PC, 태블릿, 모바일 등)의 화면 크기에 따라 가장 최적화된 레이아웃을 보여주는 웹 디자인 기술
- media query
미디어 쿼리의 가장 기본적인 문법
```html
@media (조건) {
  css 코드
}
```
max-width: 너비 해당 너비가 최대값일 때(0 ~ 너비)
min-width: 너비 해당 너비가 최소값일 때(너비 ~)
- apply css for a specific width
.contents가 nav에게 영향 받지 않고 가로 화면을 꽉 채울 수 있도록 너비를 100%로 지정
```html@media (max-width: 768px) {
  .content {
    width: 100%;
  }
}
```

### Useful terminal commands
Initialize git
```sh 
> git init
```
list all the files in a directory
```sh 
> ls -al
```
Show the working tree status of git
```sh 
> git status 
```
Add the file to git
```sh 
> git add [filename]
```
Commit the change to git with a message <-m (message)>
```sh 
> git commit -m  [message]
```
Show all the logs
```sh 
> git log
```
Show changes that were made (press q to end)
```sh 
> git diff 
```
Pus the modified file to my repo
```sh 
> git push
```
