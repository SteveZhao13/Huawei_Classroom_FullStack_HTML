# Huawei_Classroom_WebFrontEnd
This repository is code base for learning web front end knowledge in the Huawei Classroom

Some format notes:

* All **tags** will be **Bold**
* All tag *attributes* will be *Italic*
* All attribute "values" will be "quoted"

## Content - HTML
This part is the basic knowledge of HTML, specific the usage of HTML tags
#### Chapter 2


#### Chapter 5
This chapter is to learn the **form** tag

Code directory: [HTML_Chapter5.html](https://github.com/SteveZhao13/Huawei_Classroom_WebFrontEnd/blob/master/HTML_Chapter5.html)

* **form** tag has a *action* attribute and a *method* attribute. *action* is to show where the data of the from goes; *action* is the way to deliver data
* all the following tags should be included in the **form** tag
    * **input** tag can be used in various places, use *type* attribute to differ different usage: "text" - input text ; "radio" - single selection; "checkbox" - multiple selection; "button" - normal button; "submit" - submit data to database; "reset" - clear form content; "file" - upload files
    * **input** tag should have the same *name* attribute value for the same amount of selections, e.g. if there are 5 choices of *radio* type of **input** tags, all the **input** tags should have the same *name*; However, the *value* attribute should be different for each tag, because it's used to differ choices for the back-end database
    * **select** tag is used to make scroll-down menu, it should be used along with **option** tags. *selected* attribute is used to change the default option
    * **textarea** tag is used to create a multi-line text input area. Using *cols* and *rows* attributes can control the size of the area

## Content - CSS
This part is the basic knowledge of CSS

#### Chapter 1
This chapter is a brief introduction to CSS

Code directory: [CSS_Chapter1.html]()

###### There are THREE ways to insert a CSS style sheet into a HTML web page
> Inline CSS: An inline style is used to apply a unique style for `a single element`
> * How to use: add the *style* attribute to the relevant element
>
> Internal CSS: An internal style is used to apply a unique style for `a single HTML page`
> * How to use: define the style inside the **style** tag, inside the **head** section
>
> External CSS: An external style sheet is used to change the look of `an entire website`
>    * How to use: add a reference to the external style sheet file inside the **link** tag, inside the **head** section

###### CSS Syntax
```css
Selector-1, Selector-2 { Property-1: Value-1; Property-2: Value-2; }
```
> Notes:
>
> 1. Use ";" to separate different properties
>
> 2. Use "," to group multiple tags and set them to the same style

> Characteristics:
>
> 1. Only the latest(code in the bottom) property value is showed if multiple same properties are defined
>
> 2. Some properties(mostly related to text) of parent tags can be inherited by child tags