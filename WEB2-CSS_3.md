## 2021.09.26(SUN) 생활코딩 WEB2-CSS 강의

### WEB2 CSS - 8. 박스 모델

- block level element : 화면 전체를 쓰는 태그. Ex) h1 태그
- inline element : 자신의 컨텐츠의 크기만큼 가지는 태그. Ex) a 태그
- block level element <-> inline element (강제로 변환가능)

```HTML
(h1 태그와 a 태그의 범위를 확인하기 위해 박스 생성)

<style>
    /*
    block level element
    */
    h1  {
        border-width: 5px;
        border-color: red;
        border-style: solid;
    }

    /*
    inline element
    */
    a  {
        border-width: 5px;
        border-color: red;
        border-style: solid;
    }
</style>
```
- block level element 크기 > inline element 크기
<br>


```HTML
<style>
    /*
    block level element
    */
    h1  {
        border-width: 5px;
        border-color: red;
        border-style: solid;
        display: inline;
    }

    /*
    inline element
    */
    a  {
        border-width: 5px;
        border-color: red;
        border-style: solid;
        display: block;
    }
</style>
```
- block level element를 display 속성을 사용하여 강제로 inline element로 변환 가능(그 반대도 가능)
<br>


```HTML
<style>
    h1, a {
        border-width: 5px;
        border-color: red;
        border-style: solid;
    }
</style>
```
- 중복된 작업(h1 태그, a 태그의 style 태그)에 대해 위의 코드처럼 줄일 수 있음
<br>


```HTML
<style>
    h1, a {
        border: 5px red solid;
    }
</style>
```
- border의 중복된 작업을 더 축약해서 사용할 수 있음
<br>


```HTML
(컨텐츠와 테두리의 간격을 padding 속성을 사용하여 지정할 수 있음)

<style>
    h1 {
        border: 5px red solid;
        padding: 20px;
    }
</style>
```
<br>

```HTML
(margin 속성을 사용하면 h1 컨텐츠끼리의 테두리 간격을 조정할 수 있음)
(width 속성을 사용하면 block의 크기 조정 가능)

<style>
    h1 {
        border: 5px red solid;
        padding: 20px;
        margin: 0px;
        width: 100px;
    }
</style>
```
<br>


![CSS-box model](WEB2-CSS_3_boxmodel.png)
- `CSS box model`