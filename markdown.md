> # Markdown의 Basic Syntax 소개

___

## **목차**
1. [개요](##개요)
2. [제목](##제목)
3. [단락](##단락)
4. [강조](##강조)
5. [Blockquotes](##Blockquotes)
6. [목록](##목록)
7. [코드](##코드)
8. [수평규칙](##수평규칙)
9. [링크](##링크)
10. [이미지](##이미지)
11. [EscapingCharacters](##EscapingCharacters)
12. [Html](##Html)


___

## **개요**
거의 모든 **Markdown** 응용 프로그램은 **Jogn Gruber**의 원래 디자인 문서에 설명된 기보 구문을 지원합니다.

<br>

___

## **제목**
제목을 만들기 위해선 단어나 문장 앞에 '#'를 추가해야 합니다. <br>
'#'의 갯수에 따라 제목의 크기가 달라지고 '#'은 최대 6개까지 사용이 가능합니다.

    ex)
    # The largest heading
    ## The second largest heading
    ###### The smallest heading

![Headingexamgple](https://docs.github.com/assets/images/help/writing/headings-rendered.png)

### ※ 대체구문
* '#'없이 제목의 다음 줄에 '=='나 '--'를 사용하면 제목으로 만들어 집니다.

<br>
___

## **단락**
단락을 만들려면 빈 줄을 사용하면 됩니다.  
문장을 나눌려면 두 개 이상의 공백을 만들어 Enter 키를 누르거나 `<br>`표현을 사용하면 됩니다.

|Example 1|Example 2|
|:--|:--|
|Thhis is Markdown.(space bar)(space bar) <br> It is good.|This is Markdown. \<br> It is good.

<br>

___

## **강조**
'*' , '_'를 이용하여 텍스트를 굵게 하거나 기울임꼴로 변환시킬 수 있습니다.

* 굵음 : 굵은 텍스트는 단어나 문장 전후에 '*'나 '_'을 2개씩 추가하면 됩니다.

  |Example|출력 값|
      |:------:|:------:|
  |I just love `**bold text**`|I just love **bold text**|
  |I just love `___boid text__`|I just love __bold text__|
<br>

* 기울림 :  기울어진 텍스트는 단어나 문장 전후에 '*'나 '_'을 1개씩 추가하면 됩니다.

  |Example|출력 값|
      |:------:|:------:|
  |Italicized text is the \*cat's meow*|Italicized text is the *cat"s meow*|
  |Italicized text is the \_cat's meow_|Italicized text is the _cat's meow_|
<br>

* 굵고 기울림 : 굵고 기울어진 텍스트는 단어나 문장 전후에 '*'나 '_'을 3개씩 추가하면 됩니다.

  |Example|출력 값|
      |:------:|:-------:|
  |This text is `***really important***` |This text is ***really important***|
  |This text is ` ___really important___`  |This text is ___really important___|
  |This text is `**_really important_**`|This text is **_really important_**|
<br>

> ※ '*' 나 '_'와 단어나 문장 사이에는 공백이 있어서는 안됩니다.
___

## **Blockquotes**
문장을 따로 블럭처리해주는 방법은 단어나 문장 앞에서 '>'을 사용하면 됩니다. Blockquotes는 여러 번 사용이 가능하며, 중첩으로 사용이 가능합니다. 물론, 다른 요소와도 함께 사용이 가능합니다.  
**ex)**
* 입력값
``` 
    1. > Markdown is good.  

    2. > Markdown is great.  
       > Markdown is good.  

    3. > Markdown is good.
       >> Markdown is great.  

    4. > ### Basic syntax
       > - Markdown is good.
       > - Markdown is great.
       >*Everything* is good.
```
* 출력값
1. > Markdown is good.

2. > Markdown is great.  
   > Markdown is good.

3. > Markdown is good.
   >> Markdown is great.

4. > ### **Basic syntax**
   > - Markdown is good.
   > - Markdown is great.
       >*Everything* is good.

<br>

___

## **목록**
항목들을 정렬된 목록들로 구성하거나 순서없이 정렬된 목록들로 구성할 수 있습니다.

* **정렬된 목록** : 숫자와 함께 마침표를 추가하여 텍스트를 입력하면 됩니다.  
  숫자의 순서는 상관없으나 처음은 1로 시작해야 합니다.

  |Example|출력 값|
  |:--:|:--:|
  |1. First item<br>2. Second item<br>3. Third item|  1. First item<br>2. Second item<br>3. Third item|

<br>

* **비정렬된 목록** : 항목 앞에 '-', '*', '+'를 추가하면 됩니다.  
  **ex)**
* 입력값
``` 
    - First item
    + Second item
    * Third item
        * Indented item
    - Fourth item
      ![Tux](https://d33wubrfki0l68.cloudfront.net/e7ed9fe4bafe46e275c807d63591f85f9ab246ba/e2d28/assets/images/tux.png)
```
* 출력값
    - First item
    + Second item
    * Third item
        * Indented item
    - Fourth item  
      ![Tux](https://d33wubrfki0l68.cloudfront.net/e7ed9fe4bafe46e275c807d63591f85f9ab246ba/e2d28/assets/images/tux.png)

<br>

> ※ 입력 값 예시는 3 가지 문자가 사용이 된다는 것을 보여줄려고 표현한 것 입니다.  
목록을 생성할 땐 같은 문자로만 사용하는 것이 좋습니다.

<br>

___

## **코드**
단어나 구를 코드로 나타내려면 백틱( ` )을 사용하면 됩니다.
|Example|출력 값|
|:--:|:--:
|At the command prompt, type \`nano\`.| At the command promp, type `nano`.|

<br>

___

## **수평규칙**
수평 규칙을 만들려면 선에 3개 이상의 ' * ', ' - '(또는 밑줄)을 사용하면 됩니다.
 ```
    ***
    ---
    ________
```
3 가지 모두의 렌더링된 출력은 동일하게 보입니다.

<br>

___

## **링크**
링크를 만들려면 제목은 []로 표현한 이후 URL을 이어지게 괄호안에 넣으면 됩니다. URL의 제목을 추가할 수 있어 추가하려면 괄호안에 ""를 사용하여 쓰시면 됩니다. 링크 역시 강조하기가 가능합니다.  
**ex)**
* 입력값
``` 
    1. My favorite search engine is [Duck Duck Go](https://duckduckgo.com).
    
    2. <https://www.markdownguide.org>
       <fake@example.com>
    
    3. I love supporting the **[EFF](https://eff.org)**.
    This is the *[Markdown Guide](https://www.markdownguide.org)*.
    See the section on [`code`](#code).
```
* 출력값
    1. My favorite search engine is [Duck Duck Go](https://duckduckgo.com).

    2. <https://www.markdownguide.org>  
       <fake@example.com>

    3. I love supporting the **[EFF](https://eff.org)**.  
       This is the *[Markdown Guide](https://www.markdownguide.org)*.  
       See the section on [`code`](#code).

<br>

## 참조 스타일 링크
* 첫 번째 부분 서식 지정 :  
  괄호의 첫 번째 집합은 연결된 것처럼 보이는 텍스트를 둘러싸고 있습니다. 두 번째 괄호 세트에는 문서의 다른 곳에 저장하는 링크를 가리키는 데 사용되는 레이블이 표시됩니다. 첫 번째와 두 번째 괄호 집합 사이에 공백을 포함할 수 있습니다. 두 번째 괄호 세트의 레이블은 대/소문자, 숫자, 공백 또는 문장 부호를 포함할 수 있습니다.

  ex)  
  [hobbit-hole][1]

* 두 번째 부분 서식 지정 : 총 3가지의 특징으로 구성됩니다. 먼저, 대괄호로 라벨이 곧바로 이어지며, 그 다음에 하나 이상의 공간이 뒤따릅니다. 두 번째는 링크의 URL은 선택적으로 각도 대괄호에 동봉할 수 있습니다. 마지막으로 링크의 제목은 선택적이며 이중 따옴표, 단일 따옴표 등을 사용합니다.

  ex)   
  [1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle  
  [1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"  
  [1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> (Hobbit lifestyles)

<br>

___

## **이미지**
이미지를 추가하려면 느낌표 뒤에 []와 ( ) 를 붙이면 됩니다. []안에는 이미지에 대한 간략한 설명을 첨부하고 ( )에는 이미지의 경로 또는 URL을 추가합니다. 괄호 안에 URL 이후에 선택적으로 제목을 추가할 수 있습니다.  
**ex)**
* 입력값
``` 
   ![software](https://img1.daumcdn.net/thumb/R800x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F2360C944579099CA1C)
```
* 출력값  
  ![software](https://img1.daumcdn.net/thumb/R800x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F2360C944579099CA1C)

<br>

___

## **EscapingCharacters**
Markdown 문서에서 텍스트를 포맷하는 데 사용하는 문자, 문자를 표시하려면 문자 앞에 백슬래시를 추가해야 합니다. 백슬래시를 통해 담의 문자들을 피할 수 있습니다.

|문자|이름|
|:--:|:--:|
|\ |백슬래시|
|` |백틱|
|* |별표|
|_ |밑줄|
|{} |중괄호|
|[] |대괄호|
|<> |각도 브래킷|
|() |괄호|
|# |파운드 기호|
|+ |플러스 기호|
|- |마이너스 기호(하이픈)|
|. |온점|
|! |느낌표|
|\||파이프 |

<br>

___

## **Html**
많은 Markdown 응용 프로그램을 사용하면 Markdown 형식의 텍스트에서 HTML 태그를 사용할 수 있습니다. 이 기능은 Markdown 구문에 특정 HTML 태그를 선호하는 경우에 유용합니다.  
HTML을 사용하면 텍스트 색상을 지정하거나 이미지 너비를 변경하는 것과 같이 요소의 특성을 변경해야 하는 경우에도 유용합니다.
```
ex)
This **word** is bold. This <em>word</em> is italic.
```

보안상의 이유로 모든 Markdown 응용 프로그램이 Markdown 문서에서 HTML을 지원하는 것은 아닙니다. 빈 선을 사용하여 주변 콘텐츠에서 블록 수준 HTML 요소를 분리합니다. 서식을 방해할 수 있는 탭이나 공백으로 태그를 들여지지 않도록 시도합니다.블록 수준 HTML 태그 내에서는 Markdown 구문을 사용할 수 없습니다.

___
