# 프론트 엔드 개발

## 클라이언트-서버 시스템(모델)

> 클라이언트-서버 시스템은 복잡한 네트워크 연결중 양 끝단에 연결된 사용자와 공급자의 관계를 의미함.
> 
> 클라이언트 : 사용자가 사용하는 디바이스 또는 디바이스에서 실행되는 어플리케이션
> 
> Ex) 웹브라우저
> 
> 서버 : 데이터, 네트워크 서비스가 공급되는 디바이스 또는 디바이스에서 실행되는 서버 소프트웨어
> 
> Ex) 아파치 서버

## HTML 기본개념

> HTML - Hyper Text Markup Language
> 
> 웹페이지에 구성 요소를 표시하는 언어
> 
> 구성요소 : 콘텐츠, 구조

## HTML 기본구조

`(backtick)

```
<!DOCTYPE html>
<html>
  <head></head>
  <body></body>
</html>
```

- DOCTYPE : html 문서타입
- html : html 영역 표시
- head : 해당 웹페이지의 부연설명, 부가정보가 포함
- body : 웹페이지의 콘텐츠를 표시하는 영역

## HTML 요소 기본 개념

### 요소 문법

```
<starttag>contents</endtag>
```

### 포함관계

> 요소의 영역안에 다른 요소를 포함하는 관계
> 
> 직계 포함하는 요소 : 부모(parent)요소 
> 
> 직계 포함되는 요소 : 자식(child)요소
> 
> 직계가 아닌 포함하는 요소 : 조상(ancestor)요소
> 
> 직계가 아닌 포함되는 요소 : 자손(descendant)요소

### Empty element(빈 요소)

> 시작태그만 있고 종료 태그가 없는 요소


### HTML 속성(Attribute)

> html element에 대해 추가정보(이동경로, 파일명...)를 제공
> 
> 시작태그에 입력
> 
> 형식 : 속성이름 = "속성값"
> 


### HTML로 표현할 수 있는 콘텐츠(웹페이지에서 표현할 수 있는 콘텐츠)

> 텍스트 콘텐츠
> 
> 멀티미디어 콘텐츠
>  - 이미지
>  - 비디오
>  - 오디오

### 제목 요소(Heading Element)
> h1 ~ h6(h : heading)

### 단락 요소(Paragraph Element)
> p : Paragraph

> hr : Horizontal Rules
> - 단락을 구분하는 수평선을 표시
> 빈요소

> br : Line Break
> - 같은 단락안에서 강제 줄바꿈
> 빈요소

### 하이퍼링크 요소(Hyper Link Element)
> a : anchor

```
<a href="url">링크텍스트</a>
```

> href : Hyper Text Reference - 이동하고자 하는 목적지 위치/경로를 표시하는 속성
> - url(Uniform Resource locator) : 이동하고자 하는 목적지의 위치/경로 값

### 목록 요소(List Element)
> 순서있는 / 순서없는 목록
> 
> ol(Ordered List), ul(Inordered List), li(List Item)

> 설명목록
> 
> 주제와 설명이 한 세트로 구성되는 목록
> 
> dl(Description List), dt(Description Term), dd(Description Data)

### Tavle Element(https://www.tablesgenerator.com/html_tables)
> table, thead, tbody, tfoot, tr, th, td, caption 

```
<table>
  <caption></caption>
  <thead>
    <tr>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td></td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td></td>
    </tr>
  </tfoot>
</table>
```

> table : table의 영역을 설정
> 
> thead, tbody, tfoot : table 데이터의 그룹을 표시
> 
> tr(table row) : 행
> 
> th(table head) : 제목 칸(셀)
> 
> td(table data) : 데이터 칸(셀)
> 
> caption : 테이블의 제목, 설명
> 

### Image element
> img(image)
> 
> attribute : src(source), alt(alternative)

```
<img src="image.jpg" alt="image">
```

> img 태그를 사용할 때 src, alt 속성은 반드시 사용해야 함

### Video Element

> attrubute
> - controls : 비디오 컨트롤 버튼 표시
> - loop : 비디오 반복 재생
> - muted : 음소거
> - autoplay : 자동재생(항상 muted와 같이 사용)

### 절대경로/상대경로

> 절대경로 : 콘텐츠 파일을 불러오고자 하는 HTML 페이지가 어떤 위치에 있던 동일하게 찾아올 수 있도록 자세하게 표시하는 경로
> 
> 상대경로 : 콘텐츠 파일을 불러오고자 하는 HTML 페이지의 위치를 기준으로 콘텐츠 파일의 위치를 표시하는 경로

```
<img src="https://www.w3schools.com/images/picture.jpg">

<img src="images/picture.jpg">

<img src="../images/picture.jpg">

root 상대경로
<img src="/images/picture.jpg">
```

### Block/Inline Element
> 화면에 표시되는 형태를 기준으로 구분하는 방식

> Block Element
> 
> - 화면에 줄바꿈되어 표시되는 요소
> 
> - 항상 사용 가능한 전체 너비를 차지함
> 
> Inline Element
> 
> - 화면에 줄바꿈되지 않고 나란히 표시되는 요소
> 
> - 인라인요소에 포함된 콘텐츠의 너비만큼만 차지함
> 
> div(division) / span
> 
> - 단순 영역구분 요소(Container Element)

### 폼 요소

> input, button

```
<input type="text">

<input type="password">

<input type="button" value="이름">
<input type="submit" value="이름">
<input type="reset" value="이름">

<button type="button">이름</button>
<button type="submit">이름</button>
<button type="reset">이름</button>
```

### 인터넷 주소체계

> IP address : 192.168.0.1
> 
> Domain address : https://www.naver.com
> - 기본주소(IP) => 의미있는 영어단어로 변환 : 도메인 주소
> 
> www.naver.com/images/picture.jpg => URL

## CSS 

> CSS(Cascading Style Sheet)
> 
> - cascading : 나중에 선언한 것이 최종 반영되는 CSS 특징
> - CSS는 여러 대상에 대해서 공통으로 스타일을 적용시킬 수 있음

> CSS syntax
> - selector(선택자)와 declaration block(선언블록)dmfh rntjdehla
> - 선언블록은 중괄호 안에 여러 선언을 포함
> - 각 선언에는 prorerty와 value로 구성됨

```
h1 {color:red;font-size:10px;}
```

### class, id
> HTML element에 대해서 이름을 지정해줄 때 사용하는 attribute
> 
> class
> 
> - 여러개의 HTML element에 같은 클래스 이름을 사용할 수 있음
> 
> - 한 개의 HTML element에 여러개의 클래스 이름을 사용할 수 있음
> 
> id
> 
> - id 이름은 HTML 문서내에서 고유해야함(한 개만 존재)
> 
> - 한 개의 HTML element에 한 개의 id 이름만 사용할 수 있음

```
<div class="box box1 box2"></div>
<div class="box box1 box2"></div>
<div class="box box1 box2"></div>

<div id="title1"></div>
<div id="title2"></div>
<div id="title3"></div>
```

### naming 표기방식
- naming을 할 때 한 단어로 naming을 하기에는 한계가 있기 때문에 여러 단어로 naming을 하게 될 때, 단어와 단어 사이를 구분해야 하는데 일반 문서 작성처럼 띄어쓰기로 구분할 수 없기 때문에 단어와 단어 사이를 기호나 규칙에 의해서 띄어쓰지 않고 구분할 수 있도록 함 => 표기방식

> 표기방식 종류
> - snake case : gnb_list_item (underbar/underscore) => file/folder
> - kebab case : gnb-list-item (hyphen/dash) => id/class
> - camel case : gnbListItem => javascript 변수/함수 이름
> - Pascal case : GnbListItem => javascript에서의 class 이름 지정

### 컬러 모드/코드 정리

> 컬러모드
> - RGB : Red, Green, Blue - 가산혼합
> - CMYK : Cyan, Magenta, Yellow, Black(Key plate) - 감산혼합

> 색 표현 범위
> - 1bit : 최소단위
> - 8bit => 1byte : 정보표현 최소단위
> - RGB 색상 표현 : 각 1byte씩 총 3byte(24bit)로 표현(트루컬러)
> - RGB 색상 표현 값
>   - 16진수 : #0FAB78
>   - 10진수 : (255, 100, 121) ※숫자범위 : 0~255

### Text CSS

> color
> 
> - value : #000000, rgb(0,0,0)(black), #ffffff, rgb(255, 255, 255)(whithe)
> 
> text-align : left, center, right, justify
> 
> text-decoration : underline, line-through, overline, none
> 
> text-indent : 50px(들여쓰기), -50px(내어쓰기)
> 
> letter-spacing : 3px, -3px
> 
> line-height : 24px, 1.6(배수표현. 이게 더 좋다)
> 
> word-spacing
> 
> white-space : nowrap(줄바꿈 비활성화)

### Font CSS

> font-family : 'Times New Roman', Times, serif; // ''를 사용하는 의미는 공백으로 인해 컴퓨터가 하나의 단어로 인식을 못하기 때문에 ''로 묶어주는 것이다.
> 
> - font fallback : 랜더링시 폰트를 찾지 못했을 때 다른 폰트를 사용하도록 하는 대비책
> - web safe : 웹 페이지가 표시될 때 표시하고자 했던 폰트가 제대로 보일 수 있도록 선택
> - web font : 사용자 클라이언트에서 폰트를 찾는 것이 아니라 서버에서 폰트를 찾도록 하는 방식
> - google font : 웹 폰트를 사용할 수 있도록 해주는 구글 폰트 서비스
> - 눈누 : 한글 웹폰트 서비스
> 
> font - weight : normal(regular:400), bold(700)
> 
> font-size : 20px
> 
> font-style : italic

### Box Model

> HTML Element에는 기본적으로 영역이 존재하는데, 이 영역에 몇 가지 CSS 요소를 적용할 수 있음.
> - content 영역 : width/height
> - padding : 안쪽 영역
> - border : 테두리
> - margin : 바깥 여백

### width/height

> width : 가로길이/너비
> - 기본 속성 : Block 요소는 부모요소에 맞춰지고, Inline 요소는 자식요소에 맞춰짐
> 
> height : 세로길이/높이
> - 기본 속성 : Block, Inline 모두 자식요소에 맞춰짐
> 
> 단위
> - px : 지정된 수치값으로 고정
> - % : 지정된 수치값이 부모요소를 기준으로 일정 비율 크기로 
> - Block 요소의 경우 px, % 단위가 적용됨(width 사용시)
> - Inline 요소의 경우 px, % 단위 모두 적용되지 않음(width 사용시)

### padding

> padding-top
> 
> padding-rigth
> 
> padding-botton
> 
> padding-left
> 
> padding 축약표현

```
padding:20px; : 모든방향

padding:20px 30px; : top/bottom right/left

padding:20px 30px 40px; : top right/left bottom

padding:20px 30px 40px 30px; : top right bottom left (top부터 시계방향으로 돌면 알기 쉬움)
```

### margin

> padding과 사용방법이 같음

> margin 겹침
> - 위아래 연이어 배치된 박스의 위/아래 margin이 겹쳐서 큰 수치의 margin만 표현되는 것

### border

> border
> 
> width, style, color
> 
> top, right, bottom, left

```
border:1px solid #fff; Ex) #aa5500 => #a50 (RGB에서 같은색이 똑같을 때 줄여줄 수 있다.)

border-width:1px;
border-style:solid;
border-color:#fff;

border-top:1px solid #fff;
border-rigth:1px solid #fff;
border-bottom:1px solid #fff;
border-left:1px solid #fff;
```

### 박스 모델 크기 계산

> width/height, padding, border, margin 모두 별개의 요소

> Ex) 박스의 전체너비 : 300px, padding:20px; 4방향, border:1px; 4방향, margin:30px; 4방향
```
div{
  padding:20px;
  border:1px solid #fff;
  margin:30px;
  width:258px; (padding 왼쪽,오른쪽 더하고/border 왼쪽,오른쪽 더한값을 전체너비에서 빼준 값이 width가 됨)
               (padding rigth+left=20+20=40 / border right+left=1+1=2 / 총 42를 빼주면 width 값이 나온다는 의미)
}
```

> box-sizing:border-box;(기본값 : content-box)

```
div{
  padding:20px;
  border:1px solid #fff;
  margin:30px;
  width:300px;
  box-sizing:border-box; (박스사이즈를 위에처럼 계산하고 빼면 전체너비를 한번에 보기 어려우니까 아예 border size로 적어서 다 알아)
}
```

### Block, Inline에 박스모델 적용

> Block : 박스모델의 모든 요소가 적용 가능
> Inline : 박스모델의 width/height, 상하 margin 이 제대로 적용되지 않음













