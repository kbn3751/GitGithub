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
<<<<<<< HEAD
=======

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

