마크 다운(Mark-down) 작성법
===========================
> 조금 더 상세한 마크다운 사용법을 공부하려면
> "Markdown Guide (https://www.markdownguide.org/)" (영어)를 참조하면 좋다.

> 마크 다운으로만 표현이 부족하다고 느껴지면 마크 다운 표기법과 HTML 태그를 같이 활용하여서 마크 다운 문서를 작성할 수 있다.

# 1장 마크 다운에 대하여
## 1.1. 마크 다운이란?
마크 다운(Mark-down)은 일반 텍스트 기반의 경량 마크업 언어이다. 2004년 존 그루버에 의해 만들어졌으며, 쉽게 읽고 쓸 수 있으며 HTML로 변환이 가능하다. 특수기호와 문자를 이용한 매우 간단한 구조의 문법을 사용하여 웹에서도 보다 빠르게 컨텐츠를 작성할 수 있고 직관적으로 인식할 수 있다.   
마크업 언어란, 태그 등을 이용하여 문서나 데이터의 구조 등을 명기하는 언어의 한 가지이다.   
텍스트만으로 서식이 있는 문서들을 작성할 때 자주 사용되며, 다른 마크업 언어들에 비해 문법이 쉽고 간단한 것이 특징이다.   
HTML, 리치 텍스트(RTF) 등의 서식 문서들로 쉽게 변환되기 때문에 README 파일이나 온라인 게시물 등에 사용된다.
일반적인 워드프로세서 문서(Microsoft Word 등)의 파일은 복사하여 붙여넣기 했을 경우 기존에 적용된 서식 등이 모두 사라질 수 있으나, 마크 다운을 사용해 작성한 텍스트 파일은 서식을 보존할 수 있기 때문에 용이하게 사용할 수 있다.

## 1.2. 마크 다운의 장·단점
### 1.2.1. 장점
    1. 문법이 간결하고 쉽다.
    2. 별도의 도구(에디터) 없이 작성 가능하다.
    3. 다양한 형태(포맷)로 변환이 가능하다.
    4. 텍스트(text)로 저장되기 때문에 용량이 적어 보관이 용이하다.
    5. 텍스트 파일이기 때문에 버전관리 시스템을 이용하여 변경이력을 관리할 수 있다.
    6. 거의 대부분의 것에 사용할 수 있다. (웹사이트, 문서, 메모, README 기술 파일 등)
    7. 마크 다운을 지원하는 플랫폼이 다양하다. (Github, svn, Notion, Discord, Dropbox Paper 등)
    8. 대부분의 환경에서 작성 및 수정이 가능하다.
    
### 1.2.2. 단점
    1. 표준이 없기 때문에 도구에 따라서 변환방식이나 생성물이 다르다. 
      그러므로 동일한 문법으로 작성하더라도 아예 다른 방식으로 출력(rendered output)되는 경우가 있다. 
    2. 모든 HTML 마크업(mark-up)을 대신하지 못한다.
      * 색상 코드를 적용할 수 없는 등 완벽하게 지원되지 않는다.
    3. 마크 다운으로 파일을 업로드할 때 저장 이후 파일 경로를 입력해야 한다.
    4. 추가적으로 마크 다운 기호를 입력해야 하기 때문에 번거로울 수 있다.

*****
# 2장 마크 다운 문법(Syntax)
## 2.1. 헤더(Headers)
* 큰 제목: 문서 제목
    ```
    This is a H1
    ============
    ```
    This is a H1
    ============
* 작은 제목: 문서 부제목
    ```
    This is a H2
    ------------
    ```
    This is a H2
    ------------
* 글머리: 1 ~ 6까지만 지원
    ```
    # This is a H1
    ## This is a H2
    ### This is a H3
    #### This is a H4
    ##### This is a H5
    ###### This is a H6
    ```
    
    HTML
    ```
    <h1>This is a H1</h1>
    <h2>This is a H2</h2>
    <h3>This is a H3</h3>
    <h4>This is a H4</h4>
    <h5>This is a H5</h5>
    <h6>This is a H6</h6>
    ```
    
    # This is a H1
    ## This is a H2
    ### This is a H3
    #### This is a H4
    ##### This is a H5
    ###### This is a H6
    ####### This is a H7 (지원하지 않음)

## 2.2. 인용문(BlockQuote)
> 남의 말이나 글에서 직접 또는 간접으로 따온 문장.

> _(네이버 국어 사전)_

이메일(e-mail)에서 사용하는 ```>``` 블럭 인용문자를 이용한다.

```
> This is a first blockquote.
> > This is a second blockquote.
> > > This is a third blockquote.
```

> This is a first blockquote.
> > This is a second blockquote.
> > > This is a third blockquote.

이 안에서는 다른 마크 다운 요소를 포함할 수 있다.
> ### This is a H3
> * List
> `textbox`
>
> ```
> code
> ```
빈 줄이 포함되어 있어도 정상적으로 적용된다.

## 2.3. 목록
### ● 순서 있는 목록(Ordered List)
순서 있는 목록(번호)은 숫자와 점을 사용한다.

```
1. 첫 번째
2. 두 번째
3. 세 번째


1. 첫 번째
  2. 두 번째
    3. 세 번째
```

HTML
```
<ol>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item
    <ol>
      <li>Indented item1</li>
      <li>Indented item2</li>
    </ol>
  </li>
  <li>Fourth item</li>
</ol>
```

1. 첫 번째
2. 두 번째
3. 세 번째


1. 첫 번째
  2. 두 번째
    3. 세 번째

**현재까지는 순번에 맞지 않는 번호를 입력해도 반영되지 않고, 내림차 순으로 순서가 정의된다.**
```
1. 첫 번째
3. 세 번째
2. 두 번째
```
1. 첫 번째
3. 세 번째
2. 두 번째

### ● 순서 없는 목록(Unordered List)
(글머리 기호: `*`, `+`, `-` 지원)

들여쓰기를 하면 모양이 바뀐다.

```
* 빨강
  * 녹색
    * 파랑
+ 빨강
  + 녹색
    + 파랑
- 빨강
  - 녹색
    - 파랑
```

HTML
```
<ul>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item
    <ul>
      <li>Indented item1</li>
      <li>Indented item2</li>
    </ul>
  </li>
  <li>Forth item</li>
</ul>
```

* 빨강
  * 녹색
    * 파랑
+ 빨강
  + 녹색
    + 파랑
- 빨강
  - 녹색
    - 파랑

혼합해서 사용하는 것도 가능하다. 단, 표시하는 방식은 viewer마다 차이가 있을 수 있다.
```
* 1단계
  - 2단계
    + 3단계
      + 4단계
      
+ 첫 번째 아이템
  - 1-1 아이템
  - 1-2 아이템
  - 1-3 아이템
+ 두 번째 아이템
  * 2-1 아이템
  * 2-2 아이템
+ 세 번째 아이템
  + 3-1 아이템
    + 3-1-1 아이템
  + 3-2 아이템
```

* 1단계
  - 2단계
    + 3단계
      + 4단계
      
+ 첫 번째 아이템
  - 1-1 아이템
  - 1-2 아이템
  - 1-3 아이템
+ 두 번째 아이템
  * 2-1 아이템
  * 2-2 아이템
+ 세 번째 아이템
  + 3-1 아이템
    + 3-1-1 아이템
  + 3-2 아이템

### ● 리스트 안 리스트
리스트 안 리스트를 사용하려면 tab과 함께 숫자 1부터 나열하여 적용한다.
```
1. 리스트 1번
    1. 리스트 1-1번
2. 리스트 2번
3. 리스트 3번
    1. 리스트 3-1번 <!-- 리스트 안 리스트를 사용하려면 tab과 함께 숫자 1부터 나열한다. -->
    2. 리스트 3-2번
```

1. 리스트 1번
    1. 리스트 1-1번
2. 리스트 2번
3. 리스트 3번
    1. 리스트 3-1번 <!-- 리스트 안 리스트를 사용하려면 tab과 함께 숫자 1부터 나열한다. -->
    2. 리스트 3-2번

## 2.4. 코드
4개의 공백 또는 하나의 탭으로 들여쓰기를 만나면 변환되기 시작하여 들여쓰지 않은 행을 만날때까지 변환이 계속된다.

### 2.4.1. 들여쓰기
```
This is a normal paragraph:
    
    This is a code block.

end code block.
```

실제로 적용해보면,

적용 예:

*****
This is a normal paragraph:
    
    This is a code block.

end code block.
*****

> 한 줄을 띄어 쓰기 하지 않을 경우 인식이 제대로 되지 않는 문제가 발생한다. 
```
This is a normal paragraph:
    This is a code block.
end code block.
```

적용 예:
*****
This is a normal paragraph:
    This is a code block.
end code block.
*****

### 2.4.2. 코드블럭
단락 또는 전체 코드를 사용해야 하는 경우 인라인 코드로는 처리되지 않는다. 이런 경우 코드블럭을 사용한다.

코드 블록을 생성하려면 블록의 모든 행을 최소 4개의 공백 또는 하나의 탭만큼 들여쓴다.

4개의 공백 또는 하나의 탭으로 들여쓰기를 만나면 들여쓰기를 하지 않은 행을 만날 때까지 코드블럭으로 인식된다.

```
This is a normal paragraph

    <html>
      <head>
        <title>This is a codeblock</title>
      </head>

This is a normal paragraph
```

This is a normal paragraph

    <html>
      <head>
        <title>This is a codeblock</title>
      </head>

This is a normal paragraph

* HTML로 작성
```
    <code>
      <html>
        <head>
          <title>This is a codeblock</title>
        </head>
    </code>
```

    <code>
      <html>
        <head>
          <title>This is a codeblock</title>
        </head>
    </code>

코드블럭은 다음과 같이 2가지 방식을 사용할 수 있다:

* `<pre><code>{code}</code><pre>`을/를 이용하는 방법
```
<pre>
<code>
public class BootSpringBootApplication {
  public static void main(String[] args) {
    System.out.println("Hello, world!");
  }
}
</code>
</pre>
```

<pre>
<code>
public class BootSpringBootApplication {
  public static void main(String[] args) {
    System.out.println("Hello, world!");
  }
}
</code>
</pre>

백틱("`") 3개로 블럭의 앞과 뒤를 감싸도 적용된다. 백틱은 키보드의 틸드("~")와 함께 위치한 문자이다.

* 코드블럭 코드("```")을/를 이용하는 방법

<pre>
<code>
```
public class BootSpringBootApplication {
  public static void main(String[] args) {
    System.out.println("Hello, world!");
  }
}
```
</code>
</pre>

```
public class BootSpringBootApplication {
  public static void main(String[] args) {
    System.out.println("Hello, world!");
  }
}
```

**깃헙(Github)** 에서는 코드블럭 코드("```") 시작점에 사용하는 언어를 선언하여 [문법강조(Syntax highlighting)](https://docs.github.com/en/github/writing-on-github/creating-and-highlighting-code-blocks#syntax-highlighting)가 가능하다.

언어별 문법강조 코드는 [highlight.js](https://github.com/highlightjs/highlight.js/blob/main/SUPPORTED_LANGUAGES.md)를 참조한다.
<pre>
<code>
```java
public class BootSpringBootApplication {
  public static void main(String[] args) {
    System.out.println("Hello, world!");
  }
}
``` // java 코드 강조
</code>

<code>
```html
<a href="https://www.google.com/" target="_blank">GOOGLE</a>
``` // html 코드 강조
</code>

<code>
```css
.list > li {
  position: absolute;
  top: 40px;
``` // css 코드 강조
</code>

<code>
```javascript
function func() {
  var a = 'AAA';
  return a;  
``` // javascript 코드 강조
</code>

<code>
```bash
$ vim ./~zshrc
``` // bash 코드 강조
</code> 

<code>
```python
s = "Python syntax highlighting"
print s
``` // python 코드 강
</code> 
</pre>

```java
public class BootSpringBootApplication {
  public static void main(String[] args) {
    System.out.println("Hello, world!");
  }
}
```

```html
<a href="https://www.google.com/" target="_blank">GOOGLE</a>
```

```css
.list > li {
  position: absolute;
  top: 40px;
```

```javascript
function func() {
  var a = 'AAA';
  return a;  
```

```bash
$ vim ./~zshrc
```

```python
s = "Python syntax highlighting"
print s
```

### 2.4.3. 인라인 코드(Inline Code)
* 마크 다운
```
This is `InlineCode`
```

* HTML
```
This is <code>InlineCode</code>
```

## 2.5. 수평선(Horizontal Rules) ```<hr/>```
기본적으로 언더스코어(```_```) 또는 별(```*```) 기호를 3번 또는 그 이상 입력하면 단락 구분을 위한 수평선이 추가된다.
아래 줄은 모두 수평선을 만든다. 마크 다운 문서를 미리보기로 출력할 때 *페이지 나누기* 용도로 많이 사용한다.
```
* * *
***
*****
- - -
-------------------------------------------
```

* 적용 예

* * *
***
*****
- - -
-------------------------------------------

주의
```
This is normal paragraph
___
This is normal paragraph
```
이와 같이 수펑선 기호 전후에 공백 줄(line)이 없는 경우 적용되지 않을 수 있다.

```

This is normal paragraph

___

This is normal paragraph
```
의도한 출력을 만들기 위해 이와 같이 수평선 전후에 공백을 넣는다.

## 2.6. 링크
* 참조 링크
```
[link keyword][id]

[id]: URL "Optional Title here"
// code
Link: [Google][googlelink]
[googlelink]: https://google.com "Go google"
```

Link: [Google][googlelink]
[googlelink]: https://www.google.com "Go google"

* 외부 링크
```
사용 문법: [Title](link)
적용 예: [Google](https://www.google.com, "google link")
```
Link: [Google](https://www.google.com, "google link")

* 내부(해시) 링크

[보여지는 내용](#이동할 헤드(제목))

괄호 안의 링크를 쓸 때는 **띄어쓰기는 -로 연결**, 영어는 모두 **소문자**로 작성한다.
```
[1. Hearders 헤더](#1-header-헤더)

[2. Emphasis 강조](#2-emphasis-강조)

[3. Blockquotes 인용](#3-blockquotes-인용)
```

* 자동 연결(자동 링크)

꺽쇠 괄호가 없어도 자동으로 링크를 사용한다.
```
일반적인 URL 혹은 이메일 주소인 경우 적절한 형식으로 링크를 형성한다.
<link Address>

* 외부 링크: <http://www.example.com/>
* 이메일 링크: <address@example.com>
``` 

* 외부 링크: <http://www.example.com/>
* 이메일 링크: <address@example.com>

## 2.7. 강조(Empahasis)
본문의 특정 문자에 서식(볼드, 이텔릭, 밑줄, 취소선)을 적용해 강조할 수 있다.
```
이텔릭체는 *single asterisks*
또는 _single underscores_ 사용 // 언더라인으로 작성 시 띄어쓰기에 유의해야 한다.
두껍게(bold)는 **double asterisks**
또는 __double underscores__ 사용
***tripple asterisks 이텔릭체와 두껍게***를 같이 사용 가능
또는 ___tripple underscores 볼드+이텔릭체___
취소선은 ~~cancelline(tilde)~~ 사용
<strike>취소선</strike> 또는 <s>strike</s> 또는 <del>del</del>
밑줄은 <u>underline</u> `<u></u>` 사용
<font color='#1E90FF'>dodgerblue 폰트 색입니다.</font>
```

* 이텔릭체는 *single asterisks*
* 또는 _single underscores_ 사용
* 두껍게(bold)는 **double asterisks**
* 또는 __double underscores__ 사용
* ***tripple asterisks 이텔릭체와 두껍게***를 같이 사용 가능
* 또는 ___tripple underscores 볼드+이텔릭체___
* 취소선은 ~~cancelline(tilde)~~ 사용
* <strike>취소선</strike> 또는 <s>strike</s> 또는 <del>del</del>

> ```문장 중간에 사용할 경우에는 **띄어쓰기** 를 사용하는 것이 좋다.```   
> 문장 중간에 사용할 경우에는 띄어쓰기를 사용하는 것이 좋다.

* 인라인(inline) 코드 강조
\` (grave) 문자를 입력해서 본문의 요소를 강조 처리할 수 있다.
```
`<img>` 태그를 사용해서 본문에 이미지를 삽입할 수 있다.
```

`<img>` 태그를 사용해서 본문에 이미지를 삽입할 수 있다.

## 2.8. 이미지
```
![Alt text](/path/to/img.jpg)
![Alt text](/path/to/img.jpg "Optional title")

// 이미지에 링크 걸기
[![대체 텍스트](https://imageurl "모델Y 이미지")](https://linkURL)
```

![석촌호수 러버덕](http://cfile6.uf.tistory.com/image/2426E646543C9B4532C7B0)
![석촌호수 러버덕](http://cfile6.uf.tistory.com/image/2426E646543C9B4532C7B0 "RubberDuck")


사이즈 조절 기능은 없기 때문에 ```<img width="" height=""></img>```을/를 이용한다.

예
```
<img src="/path/to/img.jpg" width="450px" height="300px" title="px(픽셀) 크기 설정" alt="RubberDuck"></img><br/>
<img src="/path/to/img.jpg" width="40%" height="30%" title="%(비율) 크기 설정" alt="RubberDuck"></img>
```

<img src="http://cfile6.uf.tistory.com/image/2426E646543C9B4532C7B0" width="450px" height="300px" title="px(픽셀) 크기 설정" alt="RubberDuck"></img><br/>
<img src="http://cfile6.uf.tistory.com/image/2426E646543C9B4532C7B0" width="40%" height="30%" title="%(비율) 크기 설정" alt="RubberDuck"></img>

## 2.9. 줄바꿈(Line Breaks)
3칸 이상 띄어쓰기('   ')를 하면 줄이 바뀐다.
```
* 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸 이상을 띄어쓰기해야 한다.   
이렇게

* 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸 이상을 띄어쓰기해야 한다.___\\ 띄어쓰기
이렇게

동해물과 백두산이 마르고 닳도록  
하느님이 보우하사 우리나라 만세   <!--띄어쓰기 2번-->
무궁화 삼천리 화려 강산<br>
대한 사람 대한으로 길이 보전하세
```

* 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸 이상을 띄어쓰기해야 한다.    이렇게

* 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸 이상을 띄어쓰기해야 한다.   \
이렇게

동해물과 백두산이 마르고 닳도록  
하느님이 보우하사 우리나라 만세 <!--띄어쓰기 2번-->  
무궁화 삼천리 화려 강산<br>
대한 사람 대한으로 길이 보전하세

> 일반 줄바꿈이 동작하지 않는 환경(설정 및 버전에 따라)의 경우, '2번 띄어쓰기'나 ```<br>```을/를 활용할 수 있다.

## 2.10. 표(Table)
```<table>``` 태그로 변환한다.
헤더 셀을 구분할 때 3개 이상의 ```-```(hyphen/dash) 기호가 필요하다.
헤더 셀을 구분하면서 ```:```(colon) 기호로 셀(열/칸) 안에 내용을 정렬할 수 있다.
가장 좌측과 가장 우측에 있는 ```|```(vertical bar) 기호는 생락이 가능하다.
```
|값|의미|기본값|
|---|:---:|---:|
|'static'|유형(기준) 없음 / 배치 불가능|'static'|
|'relative'|요소 자신을 기준으로 배치| |
|'absolute'| 위치 상 부모(조상) 요소를 기준으로 배치 | |
|'fixed'|브라우저 창을 기준으로 배치| |

값|의미|기본값
---|:---:|---:
'static'|유형 (기준) 없음 / 배치 불가능|'static'
'relative'|요소 **자신**을 기준으로 배치|
'absolute'|위치 상 **_부모_(조상)요소**를 기준으로 배치|
'fixed'|**브라우저 창**을 기준으로 배치|
```

|값|의미|기본값|
|---|:---:|---:|
|'static'|유형(기준) 없음 / 배치 불가능|'static'|
|'relative'|요소 자신을 기준으로 배치| |
|'absolute'| 위치 상 부모(조상) 요소를 기준으로 배치 | |
|'fixed'|브라우저 창을 기준으로 배치| |

값|의미|기본값
---|:---:|---:
'static'|유형 (기준) 없음 / 배치 불가능|'static'
'relative'|요소 **자신**을 기준으로 배치|
'absolute'|위치 상 **_부모_(조상)요소**를 기준으로 배치|
'fixed'|**브라우저 창**을 기준으로 배치|

## 2.11. 원시 HTML(Raw HTML)
마크다운 문법이 아닌 원시 HTML 문법을 사용할 수 있다.
```
<u>마크다운에서 자원하지 않는 기능</u>을 사용할 때 유용하며 대부분 잘 동작합니다.

<img width="150" src="http://www.gstatic.com/webp/gallery/4.jpg" alt="prunus" title="A Wild Cherry (Prunus avium) in flower"

![Prunus](http://www.gstatic.com/webp/gallery/4.jpg)
```

<u>마크다운에서 자원하지 않는 기능</u>을 사용할 때 유용하며 대부분 잘 동작합니다.

<img width="150" src="http://www.gstatic.com/webp/gallery/4.jpg" alt="prunus" title="A Wild Cherry (Prunus avium) in flower">

![Prunus](http://www.gstatic.com/webp/gallery/4.jpg)

## 2.12. Backslash Escapes
특수문자를 표현할 때에는 표시될 문자 앞에 ```\```을/를 넣고 표현할 특수문자를 적는다. 
```
* 특수문자 출력 안 됨
- 특수문자 출력 안 됨

\* 특수문자 출력 됨
\- 특수문자 출력 됨
```

* 특수문자 출력 안 됨
- 특수문자 출력 안 됨

\* 특수문자 출력 됨

\- 특수문자 출력 됨

## 체크 리스트(Check List)
* `- [x]`를 적어서 완료된 리스트를 표시한다.
* `- []`를 적어서 미완료된 리스트를 표시한다.
```
- [x] This is a complete item
- [ ] This is an incomplete item
```
- [x] This is a complete item
- [ ] This is an incomplete item

*****
# 3장 마크 다운 사용기
마크다운 에디터는 메모장 등 어떤 에디터를 사용해도 무방하다. 다만, 미리보기 기능 존재여부에 따라서 사용성에 큰 차이가 나기 때문에 미리보기 기능이 있는 에디터를 사용하는 것이 좋다.

## 3.1. 위지윅(WSYWIG) 에디터
우리가 흔하게 접하는 웹에서 사용되는 에디터(네이버, 다음, 구글 등)가 대부분 위지윅 에디터에 속하며 기본적으로 HTML을 이용하여 스타일을 적용해 문장을 꾸미는 형태를 취하게 된다. 그래서 하루패드와 같은 마크 다운 에디터의 View 영역의 내용을 복사하여 붙여넣기를 하면 대체적으로 View영역에서 보이는 그대로 복사되는 편이다. 다만, 붙여넣기 이후에 문장들을 수정하려고 할 때 문제가 되는데, 이는 스타일이 포함된 태그가 수정과정에서 변형되면서 전체적인 영향을 끼치는 탓이다. 티스토리 블로그에서는 쉽지 않고, 워드프레스의 경우에는 마크다운으로 작성된 포스트를 HTML로 변환해주는 기능을 활용하는 것이 좋다.
결론은 **복사해서 붙여넣기하면 가급적이면 본문은 수정하지 않는 것이 좋다.**

## 3.2. 깃헙(Github), 비트버킷(Bitbucket)과 요비(Yobi) 등 
최근 유행하는 협업개발 플랫폼의 경우에는 마크 다운을 변환하는 컨버터 기능을 기본 탑재하고 있기 때문에 마크 다운 문법으로 작성한 텍스트를 그대로 복사해서 붙여넣거나 업로드하는 것만으로 마크 다운의 적용이 가능하다.

## 3.3. MS워드 적용
View 영역의 항목을 그대로 붙여넣거나 HTML 내보내기 등으로 생성한 파일을 불러오는 형태로 사용 가능하다.
적용한 헤더를 워드가 읽어드리면서 목차에 적용하기 때문에 이를 활용하면 목차까지도 손쉽게 적용이 가능해진다.

*****

# 4. 정리
마크다운은 기본 문법만 알고 있다면 일반 텍스트 편집기에서도 손쉽게 작성이 가능한 마크업 언어이다. 현재 다양한 도구와 플랫폼에서 지원하고 있기 때문에 더욱 손쉽게 스타일 적용된 문서를 작성할 수 있어 점점 널리 사용되고 있다.

*****

(해시 3개 사용)
3장 나누기 및 내용

*****
# 큰 글머리
**진하게** ~~취소선~~

## 작은 글머리

### 좀 더 작은 글머리

* Unordered list(순서 없는 목록)
  * Git Clone
  * Git Pull
  * Git Commit
    * Git Commit ①
    * Git Commit ②
* Git Push 😸

### 소스 코드 블럭
```c
    #include <stdio.h>
    
    int main() {
        printf("Hello world!"); // 문자열 "Hello world!"를 출력
        return 0;
     }
```

## 참고 문서
* [마크다운 markdown에 대해서 알아보자](https://velog.io/@kimhyeongi/about-markdown)
* [마크다운(Markdown) 사용법](https://gist.github.com/ihoneymon/652be052a0727ad59601)
* [MarkDown 사용법 총정리](https://heropy.blog/2017/09/30/markdown/)
* [마크다운 - 표(테이블) 만들기](https://inasie.github.io/it%EC%9D%BC%EB%B0%98/%EB%A7%88%ED%81%AC%EB%8B%A4%EC%9A%B4-%ED%91%9C-%EB%A7%8C%EB%93%A4%EA%B8%B0/)
* [마크다운(Markdown) 사용법2](https://goddaehee.tistory.com/307)
* [마크다운 작성 문법 정리](https://inpa.tistory.com/entry/MarkDown-%F0%9F%93%9A-%EB%A7%88%ED%81%AC%EB%8B%A4%EC%9A%B4-%EB%AC%B8%EB%B2%95-%F0%9F%92%AF-%EC%A0%95%EB%A6%AC)
*  [마크다운 문법의 기본적인 사용방법](https://comeinsidebox.com/markdown/)
