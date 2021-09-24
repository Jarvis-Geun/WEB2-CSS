# 2021.09.24(FRI) 생활코딩 WEB2-CSS 강의

## WEB2 CSS - 1. 수업 소개
### Reference
> https://opentutorials.org/module/3129

<br>

## WEB2 CSS - 2. CSS가 등장하기 이전의 상황

HTML은 웹의 정보를 전달하기에 너무나 좋은 언어이다. 그럼에도 디자인 측면에서는 단점이 존재하여 사람들이 불만을 갖기 시작하였다. 이러한 문제를 해결하기 위해 나온 언어가 CSS이다.<br>

```HTML
<h1><a href="index.html"><font color="red">HTML</font></a></h1>
```
위의 코드는 font 태그를 사용했을 때의 예제 코드이다. 코드를 보면 알 수 있듯이, 중요한 중보와 불필요한 정보(디자인 관련, font 태그)가 뒤섞여있는 것을 확인할 수 있다. 이러한 이유 때문에 정보로써의 가치를 잃어버리게 된다. 따라서 새로운 방법을 이용하여 웹디자인을 개선시킬 필요가 있다.

### Reference
> https://opentutorials.org/module/3129/18311

<br>

## WEB2 CSS - 3. CSS의 등장

```HTML
(font 태그를 사용하여 글씨의 색깔을 바꾼 경우)

       <h1><a href="index.html"><font color="red">WEB</font></a></h1>
        <ol>
            <li><a href="1.html"><font color="red">HTML</font></a></li>
            <li><a href="2.html"><font color="red">CSS</font></a></li>
            <li><a href="3.html"><font color="red">JavaScript</font></a></li>
        </ol>
```
위의 코드처럼, HTML로도 글씨의 색깔을 바꿀 수 있으나 너무 많은 중복된 작업을 필요로 한다. 웹페이지의 규모가 커질수록 이러한 중복된 작업은 큰 낭비일 수 밖에 없다. 이러한 중복된 작업을 줄여줄 수 있는 방법이 CSS를 이용하는 것이다. 아래의 코드를 확인한다.
<br>

```HTML
(style 태그를 사용하여 글씨의 색깔을 바꾼 경우)

    <head>
        <meta charset="utf-8">
        <title>WEB1-Welcome</title>
        <style>
            a {
                color:red;
            }
        </style>
    </head>
```
위의 코드처럼, head 태그 안에 style 태그를 추가하였다. a 태그의 색깔을 "전부" 빨간색으로 바꾸겠다는 코드이다. 중복된 작업없이 한번에 글씨의 색을 바꿀 수 있어 더 효과적인 것을 확인할 수 있다.<br>

여기서 style 태그는 CSS이다. head 태그 안에 따로 적는 이유는, HTML 코드 자체에서 style 태그 안에 있는 코드들은 CSS로 인식하게 된다.

<br>

### Reference
> https://opentutorials.org/module/3129/18312

<br>

## WEB2 CSS - 4. CSS의 기본 문법

### 간단 요약
- 선택자(selector) + 선언(declaration)
- style 태그, style 속성
- a 태그의 밑줄 없애기(선택자 사용) $\rightarrow$ text-decoration: none  
  특정 a 태그에 대해 밑줄 생기기(속성 사용) $\rightarrow$  text-decoration:underline
<br>


```HTML
(선택자, selector) + 선언(declaration)
style 태그에서 특정 태그에 대해 범위를 선택할 수 있는데 이를 "선택자"라고 한다. 아래의 코드는, a 태그에 대한 선택자를 표현하고 있다. 또한, 선택자 안의 코드를 "declaration"이라고 한다. color는 "property", black은 "value"를 의미한다.

<style>
  a {
      color:black;
  }
</style>
```
<br>


```HTML
아래의 코드는 전체 a 태그에 대해 글자의 색깔은 검정색으로 하며, 밑줄을 없앤다는 의미이다.

<style>
    a {
        color:black;
        text-decoration: none;
    }
</style>
```
text-decoration: none; $\rightarrow$ 밑줄 없애기
<br>


```HTML
style 속성을 사용하여 해당 a 태그에만 밑줄을 긋는다.

    <h1><a href="index.html">WEB</a></h1>
    <ol>
        <li><a href="1.html">HTML</a></li>
        <li><a href="2.html" style="text-decoration: underline;">CSS</a></li>
        <li><a href="3.html">JavaScript</a></li>
    </ol>
```
<br>


### Reference
> https://opentutorials.org/module/3129/18318

<br>

## WEB2 CSS 5 - 혁명적 변화

### 간단 요약
- 선택자(selector)
- 선언(declaration)
- 특성(property)
- 값(value)
<br>


```HTML
(선택자, selector) + 선언(declaration)

style 태그에서 특정 태그에 대해 범위를 선택할 수 있는데 이를 "선택자"라고 한다. 아래의 코드는, a 태그에 대한 선택자를 표현하고 있다.

또한, 선택자 안의 코드를 "declaration"이라고 한다. color는 "property", black은 "value"를 의미한다.

<style>
  a {
      color:black;
  }
</style>
```

### Reference
> https://opentutorials.org/module/3129/18318