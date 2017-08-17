- reset css : http://sapjil.net/resetcss-normalizecss/
- Lorem Ipsum : http://www.lipsum.com/
- font awesome : http://fontawesome.io/icons/
- Semantic 마크업이란 ?
- Semantic ui : https://semantic-ui.com/

- css box model
    - http://www.unilearning.net/wp-content/uploads/2017/01/CSS-Box-Model.png
    - width, hegith는 border, padding, margin을 뺀 값이라는것이 포인트임.
    - [CSS에서 마이너스마진 사용하기](http://naiyumie.tistory.com/entry/CSS-%EC%97%90%EC%84%9C-%EB%A7%88%EC%9D%B4%EB%84%88%EC%8A%A4-%EB%A7%88%EC%A7%84-%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0) 
    - float 의 반대 방향으로 마이너스 마진을 줘서 컨텐츠를 끌어올 수 있습니다
- [inline level elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements)
```
<a>, <b>, <big>, <i>, <small>, <tt>, <abbr>, <acronym>, <cite>
<code>, <dfn>, <em>, <kbd>, <strong>, <samp>, <time>. <var>, <bdo>, <br>
, <img>, <map>, <object>, <q>, <script>, <span>, <sub>, <sup>, <button>, <input>
, <label>, <select>, <textarea>

```
    - width, height 속성 설정 불가.
    - top, bottom margin 속성 설정 불가. left, right 는 가능, reset.css 없으면 기본적으로 left, right 마진이 있음.
    - padding 은 left right, bottom 설정가능, top은 안되네??
    - position 동작.
- [block level elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements)
```
<address>, <article> HTML5, <aside> HTML5, <blockquote>, <canvas> HTML5
<dd>, <div>, <dl>, <dt>, <fieldset>, <figcaption> HTML5, <figure> HTML5
<footer> HTML5, <form>, <h1>, <h2>, <h3>, <h4>, <h5>, <h6>, <header> HTML5
<hgroup> HTML5, <hr>, <li>, <main>, <nav>, <noscript>, <ol>, <output> HTML5
<p>, <pre>, <section> HTML5, <table> , <tfoot>, <ul>, <video> HTML5
```
    - width, height 설정가능
    - text-align: center
    - margin, padding 가능
    - 기본적으로 좌우, 상하단 마진이 겹쳐지면 높은값으로 collapse 됨.
    - position 동작.
- inline-block 
	- inline 요소처럼 line break 없고 block 요소에 설정할수 있는 것들 설정 가능.
- position 은 총 4가지
	- static, fixed, absolute, relative 가 있음.
	- absolute 는 부모 (parent) 가 relative가 아니면 body 기준으로 정렬됨.
	- position 위치를 지정하기위해 top, right, bottom, left를 지정하는데 top, left 는 좌,상단이 0부터이고 bottom, right는 우하단이 0 부터임.
- center align 
    - 가로정렬은 text-align 으로 하면 참 쉬운데 세로 정렬은 여러 꼼수가 있음.
        - text-align:center content를 가로정렬을 한다. 가로정렬방법은 이외 margin:0 auto 방법이 있고 이게 먹히려면 width, height가 설정되어 있어야함.
    - [세로정렬은 어떻게 ?](https://www.zerocho.com/category/CSS/post/5881edef636a7f0b8e8507d8)
    - vertical-align의 특징은 다른 태그를 기준으로 vertical-align이 된다는 것입니다. 즉 옆의 다른 태그가 있어야 그 태그에 맞춰서 세로 정렬이 된다.
    - (M1)width가 0이고 높이가 100%인 보이지 않는 헬퍼 태그 : child 태그들에 margin: 0, padding: 0을 줬음에도 서로간에 간격이 발생한. display: inline-block의 문제점
    - (M2)display: table과 display: table-cell : table-cell들의 width와 height를 조절하기 어려워집니다.
    - (M3)tranform이라는 css 속성을 사용하는 방법 (top: 50%;transform: translateY(-50%);) :  여기에서도 display: inline-block의 간격 문제가 발생
    - (M4)float도 정렬 
- 레이아웃 잡는 방법
    - table TAG
    - float:left or right : float를 선언하면 기존의 block level 의 width 100%는 사라지고 content에 맞는 width로 변경된다.
    - display:table
	- display:grid
    - display:flex    
-  [다양한 CSS Layouts 학습](http://www.free-css.com/free-css-layouts/page1)
    - http://www.free-css.com/free-css-layouts/page1/css-layout-1
    - UI component 학습.
    - state : :focus, :active. :active.focus, :active:focus, .disabled. :hover
- Wunderlist
```
class="main-interface"
  id="modal"
  id="lists" (left aside)
    lists-inner
      id=search-tollbar
      id=user-toolbar
      class=lists-scroll
      sidebarAction
  id="tasks"
    list-toolbar
    tasks-list
    tasks
    addTask
contentinfo
  top
  body
  bottom
```