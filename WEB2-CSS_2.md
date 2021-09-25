# 2021.09.25(SAT) 생활코딩 WEB2-CSS 강의

## WEB2 CSS - 6. CSS 속성(property)을 스스로 알아내기

### 간단 요약
- property(속성)을 스스로 알아내는 방법 : 굳이 모든 속성을 외울 필요없이 검색을 통해 필요할 때만 알아내면 됨.
- 글자 크기 조절 ==> font-size: 45px;
- 가운데정렬 ==> text-align: center;

```HTML
<style>
    h1  {
        font-size: 45px;
        text-align: center;
    }
</style>
```
<br>

### Reference
> https://opentutorials.org/course/3086/18328

<br>

## WEB2 CSS - 7. CSS 선택자(selector)의 기본

### 간단 요약
- class 속성 사용하여 글자 색 변환(중복 제거 가능)
- 선택자의 우선순위

<br>

```
아래의 코드처럼 글자색을 바꿀 경우, 중복된 작업이 많게 된다. 이를 해결하기 위해 class 속성을 사용한다.
```
```HTML
        <ol>
            <li><a href="1.html" style="color: gray;">HTML</a></li>
            <li><a href="2.html" style="color: gray;">CSS</a></li>
            <li><a href="3.html">JavaScript</a></li>
        </ol>
```
<br>

```
아래의 경우처럼 그냥 saw만 입력할 경우, saw 라는 이름의 태그를 바꾸는 것이다. 따라서 새로운 방법으로 바꾸어주어야 한다.
```
```HTML
    <style>
        saw {
            color: gray;
        }
    </style>
```
```
아래의 코드처럼 .saw로 선언하면, saw라는 이름의 "클래스"를 바꾼다는 의미로, a 태그의 글자를 변경해줄 수 있다.
```
```HTML
    <style>
        .saw {  
            color: gray;
        }
    </style>
```
<br>

```HTML
class 속성에 여러 개의 값을 정의할 수도 있다(saw active).

        <style>
            .saw {
                color: gray;
            }

            .active {
                color: red;
            }
        </style>
...

(중략)

...
        <ol>
            <li><a href="1.html" class="saw">HTML</a></li>
            <li><a href="2.html" class="saw active">CSS</a></li>
            <li><a href="3.html">JavaScript</a></li>
        </ol>
```
<br>

선택자에는 우선 순위가 있다.  
- `태그 선택자 < class 선택자 < id 선택자`  
- 더 `포괄적인` 선택자의 우선순위 < 더 `구체적인` 선택자의 우선순위

```HTML
id 속성에는 하나의 값만 정의하도록 한다.

        <style>
            .saw {
                color: gray;
            }

            #active {
                color: red;
            }
        </style>
...

(중략)

...
        <ol>
            <li><a href="1.html" class="saw">HTML</a></li>
            <li><a href="2.html" class="saw" id="active">CSS</a></li>
            <li><a href="3.html">JavaScript</a></li>
        </ol>
```
<br>

### CSS selector
> https://www.w3schools.com/cssref/css_selectors.asp


### Reference
> https://opentutorials.org/course/3086/18329