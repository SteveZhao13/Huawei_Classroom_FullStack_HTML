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

Code directory: [CSS_Chapter1.html](https://github.com/SteveZhao13/Huawei_Classroom_WebFrontEnd/blob/master/CSS_Chapter1.html) and [CSS_Chapter1.css](https://github.com/SteveZhao13/Huawei_Classroom_WebFrontEnd/blob/master/CSS_Chapter1.css)

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
> **Notes:**
> 1. Use ";" to separate different properties
> 2. Use "," to group multiple tags and set them to the same style

> Characteristics:
> 1. Only the latest(code in the bottom) property value is showed if multiple same properties are defined
> 2. Some properties(mostly related to text) of parent tags can be inherited by child tags

#### Chapter 2
This chapter is a description to CSS Selectors

Code directory: [CSS_Chapter2.html](https://github.com/SteveZhao13/Huawei_Classroom_WebFrontEnd/blob/master/CSS_Chapter2.html) and [CSS_Chapter2.css](https://github.com/SteveZhao13/Huawei_Classroom_WebFrontEnd/blob/master/CSS_Chapter2.css)

###### Types of CSS Selectors

1. Universal selector (*): used to define styles for all HTML elements on one page
2. Element selector (**h1**, **div**, **p**, etc): used to define style for a specific HTML element
3. Id selector (#*id*): used to define style for a element with unique *id* value

> **Note:** *id* attribute is unique in one HTML page; "id_value" should contain NO spaces and start with a character

4. Class selector (.*class* or **tag**.*class*): used to define styles for a class of elements

> **Note:** 
> *class* attribute can be used to cluster several elements into a group or a class. We can also specify certain elements to be affected by a class by using following syntax
> ```css
> tag.class {property: value}
> ```

5. Attribute selector (**tag**[*attribute*], **tag**[*attribute*="value"] or **tag**[*attribute*~="value"], etc): used to define styles for tag(s) with certain attributes

6. Pseudo-classes selector (**tag**:pseudo-class): often comes together with **a** tag to define styles of a link

> **Notes:**
> pseudo-classes should contain certain orders to take effect
> ```css
> a.link {property: value}
> a.visited {property: value}
> a.hover {property: value}
> a.active {property: value}
> ```

7. Contextual selector: used when selectors need to match elements that appear in a context
    * Descendant selector (**ancestor_tag** **descendant_tag**): all descendant tags will have the same style
    * Child selector (**father_tag** > **child_tag**): only child tags will have the style (grandson tag won't take effect)
    * Adjacent sibling selector (**sibling_tag_1** + **sibling_tag_2**)
    
###### Weights of CSS Selectors

> The HTML page will show the style of the Largest Weights
>
> * Universal Selector (*): 0
> * Element Selector (**tag**): 1 
> * Class Selector (.class), Pseudo-classes Selector (**tag**:pseudo-class) and Attribute Selector (**tag**[*attribute*]): 10
> * Id Selector (#*id*): 100
> * Inline CSS style Selectors: 1000
> * Selectors with *!important* value: Unlimited
>
> **Note:** Different selectors can be combined to get a larger weight

#### Chapter 3
This chapter is to learn common used CSS Attributes

Code directory: [CSS_Chapter3.html](https://github.com/SteveZhao13/Huawei_Classroom_WebFrontEnd/blob/master/CSS_Chapter3.html) and [CSS_Chapter3.css](https://github.com/SteveZhao13/Huawei_Classroom_WebFrontEnd/blob/master/CSS_Chapter3.css)

###### Font
1. *font-family*: which kind of fonts will be used (e.g. "serif", "monospace")
2. *font-size*: how big the font is (e.g. "30px", "50%")
3. *font-style*: how the font will be italic (e.g. "italic", "normal")
4. *font-weight*: how bold the font is (e.g. "bold", "200")

> **Note:** we can combine different font attribute into one *font* attribute, for example below (order matters). This also applies to *list-style* and *background* attributes.
> ``` css 
> p {font: italic bolder 30px serif;}
> ```

###### Text
1. *color*: used to change text color (e.g. "red", "#ff0000", "rgb(155,0,0)")
2. *line-height*: used to change how high a line is (e.g. "50px")
3. *text-align*: used to set align type of text (e.g. "center", "right")
4. *directory*: used to set text directory (e.g. "rtl", "ltr")
5. *text-indent*: used to set indent at the beginning of text (e.g. "50px", "2em")
6. *text-decoration*: used to add a decoration line above/below/through the text (e.g. "line-through", "underline")
7. *letter-spacing*: used to set spacing between characters (e.g. "10px", "-3px")
8. *text-shadow*: (e.g. "5px 5px 2px yellow")

> **Note:** *text-shadow* syntax is as below
> ``` css 
> p {text-shadow: x-offset y-offset blur radius color;}
> ``` 

###### Size
1. *height*/*width*: set height or width of a part of the window (e.g. "20px")
2. *min-height*/*min-width*: set the minimum height or width of a part of the window (e.g. "10px")
3. *max-height*/*max-width*: set the maximum height or width of a part of the window (e.g. "50px")

> **Note:** if *height*/*width* > *max-height*/*max-width* or *height*/*width* < *min-height*/*min-width*, it will use the boundary values of *max-height*/*max-width* or *min-height*/*min-width*

###### List
1. *list-style-type*: set icon shape of the list (e.g. "circle", "square", "decimal")
2. *list-style-image*: set a image as the list icon (e.g. "url(icon.png)")
3. *list-style-position*: set the position of the list icon (e.g. "inside", "outside")

> **Note:** *list-style-type* and *list-style-image* attributes cannot be showed at the same time. However, in a real HTML project, these two attributes are often written at the same time. Because some web browsers don't support *list-style-image* attribute, we will use *list-style-type* as a backup plan

###### Background
1. *background-color*: set a background color (e.g. "red", "#ff0000", "rgb(255,0,0)")
2. *background-image*: set a image as background (e.g. "url(bg.png)")
3. *background-repeat*: control how the image repeats if the background window is larger than the image (e.g. "no-repeat", "repeat-x", "repeat-y")
4. *background-position*: set the position of the background image (e.g. "left center", "50% 50%", "100px 50px")

> **Note:** for *background-position* attribute, zero point is the left-top of the background, syntax is as below
> ``` css
> div {background-position: "x-offset y-offset";}
> ```
> "x-offset" can be set to: left, center, right/10px/20%; "y-offset" can be set to: top, center, bottom/20px/50%

5. *background-attachment*: set if the background image will be fixed or scrolled with the page (e.g. "fixed", "scroll")