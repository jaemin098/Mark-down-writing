마크 다운(Mark-down) 작성법
===========================
> test repo

> 마크 다운으로만 표현이 부족하다고 느껴지면 HTML 태그를 활용하여도 좋다.

# 1장 마크 다운에 대하여
## 1.1. 마크 다운이란?
    마크 다운(Mark-down)은 일반 텍스트 기반의 경량 마크업 언어이다. 마크업 언어란, 태그 등을 이용하여 문서나 데이터의 구조 등을 명기하는 언어의 한 가지이다.
    텍스트만으로 서식이 있는 문서들을 작성할 때 자주 사용되며, 다른 마크업 언어들에 비해 문법이 쉽고 간단한 것이 특징이다.
    HTML 등의 서식 문서들로 쉽게 변환되기 때문에 README 파일이나 온라인 게시물 등에 사용된다.

## 1.2. 마크 다운의 장·단점
### 1.2.1. 장점
    1. 문법이 간결하고 쉽다.
    2. 별도의 도구 없이 작성 가능하다.
    3. 다양한 형태로 변환이 가능하다.
    4. 텍스트(text)로 저장되기 때문에 용량이 적어 보관이 용이하다.
    5. 텍스트 파일이기 때문에 버전관리 시스템을 이용하여 변경이력을 관리할 수 있다.
    6. 거의 대부분의 것에 사용할 수 있다. (웹사이트, 문서, 메모, README 기술 파일 등)
    7. 마크 다운을 지원하는 플랫폼이 다양하다. (Github, Notion, Discord, Dropbox Paper 등)
    8. 대부분의 환경에서 작성 및 수정이 가능하다.
    
### 1.2.2. 단점
    1. 표준이 없기 때문에 도구에 따라서 변환방식이나 생성물이 다르다.
    2. 모든 HTML 마크업(mark-up)을 대신하지 못한다.
    3. 마크 다운으로 파일을 업로드할 때 저장 이후 파일 경로를 입력해야 한다.

*****
# 2장 마크 다운 사용법(문법)
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
    # This is a H1
    ## This is a H2
    ### This is a H3
    #### This is a H4
    ##### This is a H5
    ###### This is a H6
    ####### This is a H7 (지원하지 않음)

## 2.2. BlockQuote
이메일(e-mail)에서 사용하는 ```>``` 블럭 인용문자를 이용한다.

```
> This is a first blockquote.
>       > This is a second blockquote.
>       >       > This is a third blockquote.
```

> This is a first blockquote.
>       > This is a second blockquote.
>       >       > This is a third blockquote.

이 안에서는 다른 마크 다운 요소를 포함할 수 있다.
> ### This is a H3
> * List
>       ```
>       code
>       ```

## 2.3. 목록
### ● 순서 있는 목록(번호)
순서 있는 목록은 숫자와 점을 사용한다.
```
1. 첫 번째
2. 두 번째
3. 세 번째
```
1. 첫 번째
2. 두 번째
3. 세 번째

**현재까지는 어떤 번호를 입력해도 순서는 내림차 순으로 정의된다.**
```
1. 첫 번째
3. 세 번째
2. 두 번째
```
1. 첫 번째
3. 세 번째
2. 두 번째

### ● 순서 없는 목록(글머리 기호: `*`, `+`, `-` 지원)
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
* 빨강
  * 녹색
    * 파랑
+ 빨강
  + 녹색
    + 파랑
- 빨강
  - 녹색
    - 파랑

혼합해서 사용하는 것도 가능하다.
```
* 1단계
  - 2단계
    + 3단계
      + 4단계
```

* 1단계
  - 2단계
    + 3단계
      + 4단계

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

## 2.5. 수평선 ```<hr/>```
아래 줄은 모두 수평선을 만든다. 마크 다운 문서를 미리보기로 출력할 때 *페이지 나누기* 용도로 많이 사용한다.

*****
# 3장 마크 다운 사용기
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
