# Markup Code Style Guide

## 개요
- 개발에 필요한 애매한 요소를 타파하자.
- 유지보수에 일관성을 유지하자.
- 개발자의 불필요한 삽질은 최소화하자.
- 대신 섹시한 코드를 만들자.


## 용어 정리
- 언더바
- 하이픈
- 카멜케이스
- 파스칼케이스
- Tag
- Attribute

## 네이밍 규칙
1. 공통 규칙
    - 짧고 간단한 이름을 사용하자. 하지만 자신만 아는 줄임은 피하자.
    - 모든 네이밍은 **`형태(prefix) + 의미(subfix) + 상태(suffix)`** 순서로 조합한다.
    - 이름에는 **영문, 숫자, 언더스코어(_), 하이픈(-)**를 사용한다. (하이픈은 CSS에서만)
    - 이름의 시작은 영문소문자나 언더스코어만 가능하다.

1. HTML/CSS
    - ID 이름는 카멜케이스*를 사용하자. (예: id="listOrder")
    - Class 이름은 하이픈(-)을 사용하자 (예: class="btn-alert")


1. 파일이름
    - 디렉토리
        - html : html 템플릿을 저장한다.
        - js : javascript 파일을 저장한다
        - css
        - img
    - HTML
        - 역시 공통 규칙을 따름, 특히 **`형태 + 의미 + 상태`**
        > 예 : notice_view.html, order_list.html, menu_main_left.html
    - CSS
        - 역시 공통 규칙을 따름, 하지만 3개이상의 단어조합은 지양하자
        - 되도록 한 단어로 그룹핑하자
        > 예 : common.css, order.css
    - 이미지
        - 역시 공통 규칙을 따름, 특히 **`형태 + 의미 + 상태`** 
        > 예 : btn_search_on.png (O), btn_search_bar.png (X)
        
        

1. Prefix 모음 (Subfix도 같이 사용)
    
    <table>
        <tr>
            <td><b>구분</b></td> <td><b>Prefix</b></td> <td><b>설명</b></td>
        </tr>
        <tr>
            <td>btn</td> <td>버튼</td> <td></td>
        </tr>
        <tr>
            <td>tab</td> <td>탭</td> <td></td>
        </tr>
        <tr>
            <td>ico</td> <td>아이콘</td> <td></td>
        </tr>
        <tr>
            <td>img</td> <td>이미지</td> <td></td>
        </tr>
        <tr>
            <td>sp</td> <td>스프라이트</td> <td>이미지 스프라이트</td>
        </tr>
        <tr>
            <td>bg</td> <td>배경</td> <td></td>
        </tr>
        <tr>
            <td>bu</td> <td>불릿</td> <td></td>
        </tr>
        <tr>
            <td>line</td> <td>선</td> <td></td>
        </tr>
        <tr>
            <td>nav</td> <td>네비게이션</td> <td></td>
        </tr>
        <tr>
            <td>tbl</td> <td>테이블</td> <td></td>
        </tr>
        <tr>
            <td>inp</td> <td>input</td> <td>input text,checkbox,radio</td>
        </tr>
        <tr>
            <td>list</td> <td>리스트</td> <td></td>
        </tr>
        <tr>
            <td>menu</td> <td>메뉴</td> <td></td>
        </tr>
        <tr>
            <td>txt</td> <td>텍스트</td> <td></td>
        </tr>
        <tr>
            <td>link</td> <td>링크</td> <td></td>
        </tr>
        <tr>
            <td>pop</td> <td>팝업</td> <td></td>
        </tr>
        <tr>
            <td>copy</td> <td>카피라이트</td> <td></td>
        </tr>
    </table>

    
1. Suffix 모음

    <table>
        <tr>
            <td><b>구분</b></td> <td><b>Suffix</b></td> <td><b>설명</b></td>
        </tr>
        <tr>
            <td>on / off / over / hit / focus</td> <td>상태 변화</td> <td></td>
        </tr>
        <tr>
            <td>top / mid / bot / left / right</td> <td>위치 변화</td> <td></td>
        </tr>
        <tr>
            <td>fst / lst</td> <td>순서 변화</td> <td>first/last</td>
        </tr>
        <tr>
            <td>prev / next</td> <td>이전 / 다음</td> <td>first/last</td>
        </tr>
        <tr>
            <td>open / close</td> <td>열고 / 닫고</td> <td></td>
        </tr>
        <tr>
            <td>new / old / v2 / v3...</td> <td>버전</td> <td></td>
        </tr>
    </table>
        

## 코딩 컨벤션
1. HTML
    1. Tag*는 소문자로 작성한다
    1. Attribute*도 소문자로 작성하며, Value은 " "(쌍따옴표)로 감싼다
    1. Attribute만 쓸 수 있는 것이라도 Attribute / Value 쌍으로 표현하자
        - 예: `selected="selected"` selected는 value 없이 쓸 수 있지만..
    1. Tag는 열고 닫자. 닫는 Tag가 없이 쓸 수 있더라도 닫자.
        - 예: `<div>...</div>` 안에 값이 없어도 닫자
        - 예: `<br />` (이때는 공백하나 넣어줌) 
    1. HTML5를 기본으로 사용하자.
        - `<!DOCTYPE html>` 을 사용하자
        - frame 은 사용하지 않는다.(html5에서 없어짐)
        - iframe 대신 object를 쓰자.
    1. 주석은 `<!-- 내용 -->` 을 사용하며, 코드 변경시 주석안에 일시를 남기자.(YYYY-MM-dd)
        - 내용가 주석 태그 사이에는 공간을 넣어주자
        - 나중에 구현해야할 부분은 TODO 로 주석을 씌워서 기록해두자 
        - 또한 수정한 섹션을 구분할때는 시작과 끝 주석으로 감싸자.
    1. 들여쓰기는 모두 탭을 사용함. 1 tab = 4 spaces (IDE 세팅을 바꾸자)
    1. 이외 모든 컨벤션은 IDE 환경설정에 따른다. (동일한것을 배포해서 쓰자
    1. 인코딩은 항상 `utf-8` 이다 
        - `<meta http-equiv="Content-Type" content="text/html; charset=utf-8">`

1. CSS 
    1. 모든 Attributes는 소문자로와 하이픈(-)으로만 작성한다
    1. 모든 Values는 따옴표를 사용하지 않는다.
        - 단, 스페이스가 포함된 값을 표현할때는 홑따옴표(' ')로 감싼다. 
        - 또한 `@charset "utf-8"` 는 쌍따옴표로 감싼다
        - 속성의 마지막에는 세미콜론(;)을 넣지 않는다. (.body{font-size:14; color:#0})    
    1. 주석은 `/* 내용 */` 을 사용하며, 코드 변경시 주석안에 일시를 남기자.(YYYY-MM-dd)
        - 내용가 주석 태그 사이에는 공간을 넣어주자
        - 나중에 구현해야할 부분은 TODO 로 주석을 씌워서 기록해두자 
        - 또한 수정한 섹션을 구분할때는 시작과 끝 주석으로 감싸자.
    1. 들여쓰기는 없으며, 정리는 IDE에게 맞긴다.
    1. 속성/값 쌍이 3개 이하이고, 80자를 넘지 않으면(한줄에 표현가능하면) 한줄로 표현한다. 
    1. @import 대신 link 태그를 사용하자. 
    

## 레이아웃
1. 모든 레이아웃의 디자인은 부트스트랩과 폰트어썸을 기본으로 사용한다.
1. 폰트
    - 기본 폰트 사이즈 : 14px
1. div 대신 시멘틱 태그를 잘 쓰자
    - `<header>, <footer>, <nav>, <article>, <section>` 같은 것들
1. 축약형 속성을 잘 쓰자. CSS사이즈가 줄어든다!
    - <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties" target="_blank">제대로 알고 쓰자: Shorthand properties</a>
    1. color도 축약형을 쓸수있다면 사용하자.(`#fff`)
    1. font 속성은 축약형을 쓰지말고 font-style > font-variant > font-weight > font-size > line-height > font-family 순으로 선언하자
1. HTML에서 style은 최대한 CSS 파일로 분리하자
1. 하나의 페이지에서는 전체적으로 3개의 id를 가진 section으로 구분하자
    - \#header (재사용 하자)
    1. \#container
    1. \#footer (재사용 하자)
1. z-index는 1~9999 까지 사용가능
    - 일반적으로 페이지 내부에서는 1~999까지만 사용하자
    1. 팝업 레이어의 경우 1000을 사용하자
    1. iframe 위에 표현할 경우는 9999를 사용하자.
1. margin, padding은 위아래로 한방에 스타일링 가능한 놈에다가 할당한다.
    - 역시 축약형 추천
1. 스타일 그룹핑
    1. 공통 스타일시트(common.css)를 만들어 놓자. 공통 스타일로 그룹핑해야할 것들은 아래와 같다.
        - 폰트 : 전체적으로 동일한 폰트를 사용하며, 사이즈와 스타일만 다르게 하자.
        1. a(link) : 뭔가 클릭해서 페이지 이동할것.
            - 내부 페이지와 외부 페이지 이동을 구분하자.
            - `target="_blank"`로 나올 것은 dash-underline을 주자 
        1. input(text, button, checkbox 등) : 전체적으로 사용할 기본 디자인을 정하자.
        1. `body,div,dl,dt,dd,ul,ol,li,h1,h2,h3,h4,h5,h6,pre,code,form,fieldset,legend,textarea,p,blockquote,th,td,input,select,textarea,button {margin:0;padding:0}
fieldset,img {border:0 none}`
        1. `dl,ul,ol,menu,li {list-style:none}`
        1. `blockquote, q {quotes: none}`
        1. `blockquote:before, blockquote:after,q:before, q:after {content:'';content:none}`
        1. `input,select,textarea,button {vertical-align:middle}`
        1. `button {border:0 none;background-color:transparent;cursor:pointer}`
        1. `body {background:#fff}` 
    1. Specific Grouping
        - 기본적으로 서비스(앱) 단위로 그룹핑하자.
        - 예: signinup.css, order.css
        - 하지만 다른 서비스(앱)이더라도 겹쳐서 하나로 통합할 수 있는 부분이 있을 것임.
            - 요럴땐 해당 기능들을 모아서 기능단위로 그룹핑하자.
            - 예: input.css, nav.css
        - 정리
            - 다양한곳(2군데 이상)에서 쓰이면 기능단위로 묶고
            - 그 이외의 경우 페이지가 나뉘어 있더라도 서비스(앱) 단위로 묶는다. 


# Reference
- 네이버 컨벤션 : http://nuli.navercorp.com/data/convention/NHN_Coding_Conventions_for_Markup_Languages.pdf
- 다음 컨벤션 : http://darum.daum.net/convention/html
- 네이밍 규칙 : http://hhh8947.tistory.com/323
- codjs 컨벤션 : http://codejs.co.kr/portfolio/views/convention/convention.html#rule-html
- CSS 최적화 기법 : http://techbug.tistory.com/206
- 가비아 컨벤션 : http://gabia-frontend-dev.com/wordpress/?p=603
- HTML&CSS 공부하기 : https://www.gitbook.com/book/singihae/front-end-developer-guide-book/details






 
     