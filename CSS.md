# CSS- Complete Notes

- # **CH-01 What is CSS & Connecting HTML to CSS?**
    
    CSS (Cascading Style Sheets) is a stylesheet language used to control the appearance and layout of web pages written in HTML.
    
    HTML creates the structure of the page.
    
    &, CSS adds styling to that structure.
    
    ```
    💡
    
    Remember,
    
    HTML → Structure
    
    CSS → Styling
    
    JavaScript → Functionality
    
    ```
    
    ### Connecting HTML to CSS:
    
    There are some methods by which we can connect HTML to CSS together and they are as follows:
    
    - Inline CSS: Here we use style attribute every time when we want to add style in our web page.
    
    ```html
    <body>
     <h1 style = "color: yellow; background-color: red;">This is my heading</h1>
    </body>
    ```
    
    - Internal CSS: Here we use `<style>` tag and we can bulk style everything at once in our web page.
    
    ```html
     <style>
        h1{color:red;
        background-color:yellow}  <!-- Here we have changed color and background color for all the h1 present in our code. -->
      </style>
    </head>
    <body>
     <h1>This is my heading</h1>
    </body>
    ```
    
    - External CSS: By this method we create a CSS file where we write all the styles we want to add in our web site.
    But, at the same time we would have to connect both HTML and CSS file to each other.
    
    ```html
    <!-- way to link HTML and CSS files.
    Here, we use <link> element/tag to add CSS file in HTML above the head tab-->
    <head>
        <link rel="stylesheet" href="style.css">
    </head>
    ```
    
    ```css
    h1{
        color: red;
        background-color:yellow
    }
    ```
    
    ```
        💡Note:
        
        - Adding comments in CSS file:
        
        ```css
        /* Comments here */
        ```
    
    ```
    
- # **CH-02 CSS Selectors**
    
    #### CSS selectors allow us to choose specific elements and apply styles to them
    
    ```
    💡Note:
    
    Here we can select a specific terms like we want to style all heading1 as same then we will use selectors with h1 and some more items if we want and then style it all combined.
    
    By this way we would not have to style same thing one by one.
    
    ```
    
    ### Element Selector:
    
    Here we can style a selected element as we want by using style attribute in HTML file.
    
    ```html
      <style>
            div {
                color: blue;
                background-color: lightgray;
            }
    
            /* Here we have selected div element and applied styles to it and
             by this method all the div present in the document will be selected and styles will be applied to them. */
        </style>
    </head>
    
    <body>
        <div>
            this is a div.
        </div>
    </body>
    ```
    
    ```
    💡Note:
    
    But if we want to style some specific div as same but we don’t want to style all the div present in the document then we will firstly assign class to the div that we want to style and then we will use style selector.
    
    ```
    
    ### Class Selector:
    
    If we give a specific class to a div or span and add class in style function too then the style will only be applied in the respective class.
    
    ```html
    <style>
            .my_div1 {
                color: blue;
                background-color: lightgray;
            }
    
            .my_div2 {
                color: red;
                background-color: lightblue;
            }
    
            /* Here we have used class selector to style the selected div at once by this method all the div with same class will be styled at once.
    same as here we can see when we have selected the class my_div it styled both the div having class my_div and
    when we selected the class my_div2 it only styled the third div having class my_div2 */

        </style>
    </head>
    
    <body>
        <div id="div1" class="my_div">
            this is a div.
        </div>
        <div id="div2" class="my_div">
            this is another div.
        </div>
        <div id="div3" class="my_div2">
            this is a third div.
        </div>
    </body>
    ```
    
    ```
    💡Note:
    
    We use “ . ” to represent class.
    
    ```
    
    ### ID Selector:
    
    Here the style will be apply to the respective ID.
    
    ```html
     <style>
            #div1{
                color: red;
                background-color: yellow;
            }
            #div2{
                color: blue;
                background-color: green;
            }
            #div3{
                color: red;
                background-color: lightblue;
            }
        </style>

        <!-- Here we have used id selector to style the divs. The id selector is used to select a single element with a specific id attribute.
        In this case, we have three divs with different ids (div1, div2, and div3), and we have applied different styles to each of them using their respective ids. -->

    </head>
    
    <body>
        <div id="div1" class="my_div">
            this is a div.
        </div>
        <div id="div2" class="my_div">
            this is another div.
        </div>
        <div id="div3" class="my_div2">
            this is a third div.
        </div>
    </body>
    
    ```
    
    ```
    💡Note:
    
    Here “ # ” represents id.
    
    ```
    
    ### Child Selector:
    
    The child selector `>` selects only elements that are direct children of another element.
    
    ```html
    <style>
            div> p {
                color: red;
                background-color: yellow;
            }
        </style>
        <!-- Here we have used child selector to select only the paragraphs which are children of the divs.
       the paragraphs which are not children of the divs will not be selected.
       and style will only be applied to the paragraphs which are children of divs. -->
    
    <body>
        <div id="div1" class="my_div">
            this is a div.
            <p>
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Vitae consectetur enim officiis recusandae
                cupiditate optio.
            </p>
        </div>
        <div id="div2" class="my_div">
            this is another div.
        </div>
        <div id="div3" class="my_div2">
            this is a third div.
            <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugit aliquam ea sapiente esse cumque nostrum
                eveniet eius voluptas vitae dolore?
            </p>
        </div>
    </body>
    ```
    
    ```
    💡Note:
    
    These options are not only for div and span we can also use it for other tags like article, main, section, etc. the only thing which we will have to change will be:
    
    We would have to replace “div” with the particular tag that we want to style in the internal CSS code.
    
    ```
    
    ```
    💡Note:
    
    The child selector will only work if the paragraph will be the direct child of the div. If we have a div and we use an article tag under div then write the paragraph inside the article tag then the style will not get applied to the paragraph because in this case the paragraph is not the direct child of div. But to still apply tag to paragraph we can either replace div with article in internal CSS or we can use descendant selector. 
    
    ```
    
    ### Descendant Selector:
    
    The descendant selector selects all matching elements inside another element, whether they are direct or indirect children.
    
    ```html
    <style>
            div p {
                color: red;
                background-color: yellow;
            }
        </style>
        <!-- Here we have used descendant selector to select the paragraphs which are not direct children of the divs.
       the paragraphs which are children of the divs will also be selected.
       and style will get applied to the paragraphs which are children of divs in any way be it direct or indirect.
       Here we can see in the first div that paragraph is not the direct child of the div,
       still the style will get apply to it as we have used descendant selector. -->
    
    <body>
        <div id="div1" class="my_div">
            this is a div.
            <article>
            <p>
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Vitae consectetur enim officiis recusandae
                cupiditate optio.
            </p>
            </article>
        </div>
        <div id="div2" class="my_div">
            this is another div.
        </div>
        <div id="div3" class="my_div2">
            this is a third div.
            <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugit aliquam ea sapiente esse cumque nostrum
                eveniet eius voluptas vitae dolore?
            </p>
        </div>
    </body>
    ```
    
    ### Universal Selector:
    
    The universal selector `*` selects all elements on the page.
    
    ```html
     <style>
            *{
                padding: 5px;
                margin: 10px;
            }
        </style>
    </head>
    <body>
        <div id="div1" class="my_div">
            this is a div.
            <article>
            <p>
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Vitae consectetur enim officiis recusandae
                cupiditate optio.
            </p>
            </article>
        </div>
        <div id="div2" class="my_div">
            this is another div.
        </div>
        <div id="div3" class="my_div2">
            this is a third div.
            <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugit aliquam ea sapiente esse cumque nostrum
                eveniet eius voluptas vitae dolore?
            </p>
        </div>
    </body>
    ```
    
    ```
    💡Note:
    
    Here “ * “ represents universal selector and by this method we have applied style to everything we had.
    
    ```
    
    ### Selectors and their symbols:
    
    | Selector | Symbol | Example |
    | --- | --- | --- |
    | Element | none | `h1` |
    | Class | `.` | `.box` |
    | ID | `#` | `#header` |
    | Universal | `*` | `*` |
    | Child | `>` | `div > p` |
    | Descendant | space | `div p` |
- # **CH-03 Specificity & Cascade**
    
    ### Cascade Algorithm:
    
    If we apply multiple styles to a single class, id, div, etc. The CSS algorithm decides which style will be applied to the given class, id, div, etc.
    
    It judges according to 4 different stages:
    
    1. Position & order of appearance: Suppose we have used a single type of selector example- class selector 4 times for a single element. Then according to the element it will treat all styles applied by using class selector as a same category and the last style given to the element will be applied to the element. 
    2. Specificity: It divides all the ways we can apply styles into a different category and every type as a specific order priority the order is:
    Inline CSS > ID Selector > Class selector > Element selector > Universal selector.  
    3. Origin
    4. Importance: The cascade determines which CSS declaration wins when multiple declarations apply to the same element.
    
    ### Here is the value to remember while calculating the specificity:
    
    These numbers are useful for understanding specificity, but specificity is better thought of as a four-part comparison rather than normal arithmetic.
    
    | Selector | Value |
    | --- | --- |
    | Inline | 1000 |
    | ID | 100 |
    | Class | 10 |
    | Element | 1 |
    | Universal | 0 |
- # **CH-04 CSS Units**
    
    CSS units are used to specify the size of properties such as:
    
    - `width`
    - `height`
    - `margin`
    - `padding`
    - `font-size`
    - `gap`
    - `position`
    
    CSS units are broadly divided into:
    
    1. **Absolute units**
    2. **Relative units**
    
    ### Absolute Units:
    
    Absolute units have a fixed size and don't depend on another element.
    
    #### px-Pixels:
    
    It gives specific sizes in pixels.
    
    `px` is useful when you need precise control over a particular dimension.
    
    ```css
    .box {
    width: 300px;
    height: 200px;
    }
    ```
    
    ```
    💡Note:
    
    Drawback: Relying heavily on fixed pixels can make a layout less flexible across different screen sizes.
    
    ```
    
    ### Relative Units:
    
    Relative units depend on something else, such as:
    
    - Parent element
    - Root element
    - Viewport
    
    #### %-Percentage:
    
    Percentage is generally relative to the corresponding dimension of the containing block.
    
    This means suppose a container of width 100px and it has an element if I give command to that element for 30% width, then it will take space of 30px out of 100px of container width.
    
    ```css
    .container {
        width: 500px;
    }
    
    .box {
        width: 50%;
    }
    
    /* Here the box will take 250px width */
    ```
    
    #### em:
    
    `em` is relative to the font size of the element's context. For `font-size`, it is commonly based on the parent's font size.
    
    It means the font size of the child element will be depending on parent element.
    
    suppose if my parent element has font size of 20px and for child I give font size as 2em, then the font size of child element will be 2 times the parent element.
    
    ```css
    .parent {
        font-size: 20px;
    }
    
    .child {
        font-size: 2em;
    }
    
    /* Here the child will have font size of 40px. */
    ```
    
    #### rem- Root em:
    
    It is relative to the font size of the root `<html>` element.
    
    Suppose we have an HTML element  <HTML> The size relation here is not parent child relation.
    
    the relation here is in between the element and the html element.
    
    ```css
    html {
        font-size: 15px;
    }
    
    h1 {
        font-size: 2rem;
    }
    
    /* Here the h1 will have font size 30px */
    ```
    
    #### Why `rem` is useful
    
    Unlike `em`, `rem` consistently refers to the root font size, making it easier to maintain consistent sizing across a website.
    
    #### vw-Viewport Width:
    
    The width of whole screen is viewport width.
    
    If I give command of 50vw then that particular element will take the 50% width of the whole screen.
    
    ```css
    .text {
        width: 50vw;
    }
    
    /* Here the text element will have 50% screen width. */
    ```
    
    #### vh-Viewport Height:
    
    The height of whole screen is viewport height.
    
    If I give command of 50vh then that particular element will take the 50% height of the whole screen.
    
    ```css
    .text {
        height: 50vh;
    }
    
    /* Here the text element will have 50% screen height. */
    ```
    
    #### vmin:
    
    Suppose my screen’s width is 1000px and height is 500px.
    
    what happens with vmin is it represents the smaller dimension of the viewport whether it is the height or width.
    
    If I give command of 1vmin width it means that the element will take width which will be equal to 1% of the smaller dimension which is height in this case.
    
    As height is 500px the element will take height of 5px, which is 1% of 500px.
    
    ```css
    .text {
        width: 50vmin;
    }
    ```
    
    ```
    💡Note:
    
    vmax is the exact opposite of this it will go with the bigger dimension.
    
    ```
    
- # **CH-05 CSS Box Model**
    
    ### What is the Box Model?
    
    Every HTML element is treated as a **rectangular box** in CSS.
    
    The CSS Box Model defines how much space an element occupies and how spacing is managed.
    
    ### Structure of Box Model:
    
    ┌───────────────────────────────┐
    │            Margin                                                                    │
    │  ┌─────────────────────────┐          │
    │  │         Border                                                      │          │
    │  │  ┌───────────────────┐          │          │
    │  │  │      Padding                                    │          │          │
    │  │  │  ┌─────────────┐          │          │          │
    │  │  │  │   Content                     │          │          │          │
    │  │  │  └─────────────┘          │          │          │
    │  │  └───────────────────┘          │          │
    │  └─────────────────────────┘          │
    └───────────────────────────────┘
    
    #### Content:
    
    Content is the actual text, image, button, or any element present inside the box.
    
    ```html
    <p>This is content</p>
    ```
    
    #### Padding:
    
    Padding is the space **between the content and the border**.
    
    ```css
    div{
        padding:20px;
    }
    ```
    
    ```
    💡Note:
    
    - Padding increases the space inside the element.
    - The background color extends into the padding area.
    ```
    
    #### Border:
    
    Border surrounds the content and padding.
    
    ```css
    div{
        border:2px solid black;
    }
    ```
    
    #### Margin:
    
    Margin is the space **outside the border**.
    
    ```css
    div{
        margin:20px;
    }
    ```
    
    ```
    💡Note:
    
    - Margin creates distance between two elements.
    - Background color does **not** extend into the margin.
    ```
    
    #### Height & Width:
    
    `width` and `height` control the dimensions of an element. How they are interpreted depends on `box-sizing`.
    
    ```css
    div{
        width:300px;
        height:200px;
    }
    ```
    
    #### Box Sizing Property:
    
    The `box-sizing` property determines how the total width and height of an element are calculated.
    
    #### Content Box (Default):
    
    ```css
    box-sizing:content-box;
    ```
    
    The width includes **only the content**.
    
    Padding and border are added separately.
    
    #### Border Box:
    
    ```css
    box-sizing:border-box;
    ```
    
    The width includes:
    
    - Content
    - Padding
    - Border
- # **CH-06 Fonts, Text & Color properties**
    
    ### Fonts:
    
    To edit the appearance of text we can choose different fonts using font-family property.
    
    ```html
    <style>
            h1{
                font-family:'Times New Roman', Times, serif
            }
            p{
                font-family: Arial, Helvetica, sans-serif
            }
        </style>
        <!-- Here, we have used two different fonts for heading and paragraph.
        by using selectors we have applied it one by one.
        Font-family is an attribute that is used to set the font of the text.
        and the font as we can see has two three names separated by commas.
        this is because if the first font is not available then it will use the second one and so on. -->
    </head>
    <body>
        <div>
            <h1>Fonts</h1>
            <p>Hi my name is Aniket Tiwari. I am 19 years old.</p>
        </div>
    </body>
    ```
    
    ```
    💡Note:
    
    - To change the style of font like italic, oblique, etc. we will use font-style attribute in the same way as font-family.
    - Same as if we want to make the text bold or bolder we use font-weight attribute.
    - To underline our text we use text-decoration attribute.
    - To change font size we use font-size attribute.
    - Line height- The spacing between two lines is refer to as line height and to increase or decrease this spacing we use line-height attribute.
    - To change the text spacing we use letter-spacing attribute.
    - To give indent we use text-indent attribute.
    - To have our text at center we use text-align: center attribute.
    ```
    
    ### Colors:
    
    We can use different ways to change colors:
    
    - Color keyword- By writing name of color.
    
    ```css
    color: red;
    ```
    
    - Hex color code- By using hex code of color.
    
    ```css
    color: #ff0000;
    ```
    
    - RGB- Red. Green, Blue we can choose the color code of these three from 0-255 and the color will be applied.
    
    ```css
    color: rgb(255,0,0);
    ```
    
    - RGBA- A stands for alpha and controls transparency/opacity.
    
    ```css
    color: rgba(255,0,0,0.5);
    ```
    
    - HSL- Hue, Saturation, lightness.
    
    ```css
    color: hsl(0,100%,50%);
    ```
    
- # **CH-07 Background Properties**
    
    Background properties are used to control the appearance of an element's background, such as its **color, image, position, size, and repetition**.
    
    They help make web pages visually appealing and improve the overall design.
    
    ### Different types of background properties:
    
    #### Background Color:
    
    Used to change the background color of an element.
    
    ```css
    div{
        background-color: lightblue;
    }
    ```
    
    #### Background Image:
    
    Used to set an image as the background.
    
    ```css
    body{
        background-image: url("background.jpg");
    }
    ```
    
    #### Background Repeat:
    
    Controls whether the background image repeats.
    
    ```css
    body{
        background-repeat: no-repeat;
    }
    ```
    
    #### Background Position:
    
    Determines where the background image is placed.
    
    ```css
    body{
        background-position: center;
    }
    ```
    
    #### Background Size:
    
    Controls the size of the background image.
    
    ```css
    body{
        background-size: cover;
    }
    ```
    
    #### Shorthand Property:
    
    ```css
    body{
        background-color: black;
        background-image: url("bg.jpg");
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;
    }
    
    /* Instead of writing this whole thing */
    
    /* We can write: */
    
    body{
       background: black url("bg.jpg") no-repeat center / cover;
    }
    ```
    
- # **CH-08 Display Properties**
    
    The `display` property determines **how an HTML element is displayed on the webpage**.
    
    Every HTML element has a default display type. By using the `display` property, we can change how an element behaves and how it occupies space.
    
    ### Block Elements:
    
    A block element always starts on a **new line** and occupies the **entire available width** of its parent container by default.
    
    ```css
    div {
    	display: block;
    }
    ```
    
    ### **Inline Elements:**
    
    Inline elements only occupy as much width as required by their content.
    
    ```css
    span{
        display:inline;
    }
    ```
    
    ### **Inline-Block Elements:**
    
    `inline-block` combines the advantages of both inline and block elements.
    
    The element:
    
    - stays on the same line,
    - but also allows custom width and height.
    
    ```css
    .box{
        display:inline-block;
        width:150px;
        height:80px;
     }
    ```
    
    ### **Display None:**
    
    The `display: none` property completely removes an element from the webpage.
    
    The element:
    
    - is not visible,
    - occupies no space,
    - behaves as if it does not exist.
    
    ```css
    .box{
        display:none;
    }
    ```
    
    ### **Display Flex:**
    
    The `display: flex` property converts an element into a **Flex Container**.
    
    All direct child elements become **Flex Items**.
    
    ```css
    .container{
        display:flex;
    }
    ```
    
    Flexbox is mainly used to:
    
    - Align elements
    - Create responsive layouts
    - Distribute space efficiently
    
    ### **Display Grid:**
    
    The `display: grid` property converts an element into a **Grid Container**.
    
    It is mainly used for creating two-dimensional layouts consisting of rows and columns.
    
    ```css
    .container{
        display:grid;
    }
    ```
    
    Grid is commonly used for:
    
    - Website layouts
    - Dashboards
    - Galleries
    - Complex page structures
- # **CH-09 Position Properties**
    
    The `position` property is used to specify **how an element is positioned on a webpage**.
    
    It determines how an element is placed in relation to:
    
    - its normal position,
    - its parent element,
    - the browser window (viewport), or
    - the document.
    
    ### **Static Position:**
    
    `static` is the **default** position value for all HTML elements.
    
    The element follows the normal document flow.
    
    Properties like `top`, `right`, `bottom`, and `left` do **not** work with `position: static`.
    
    ```css
    .box{
        position: static;
    }
    ```
    
    ### **Relative Position:**
    
    The element remains in its normal position, but it can be moved relative to that position.
    
    ```css
    .box{
        position: relative;
        top: 20px;
        left: 30px;
    }
    ```
    
    ### **Absolute Position:**
    
    An absolutely positioned element is removed from the normal document flow.
    
    It is positioned relative to its **nearest positioned ancestor** (an ancestor with a position other than `static`).
    
    If no positioned ancestor exists, it is positioned relative to the webpage.
    
    ```css
    .parent{
        position: relative;
    }
    
    .child{
        position: absolute;
        top: 20px;
        right: 10px;
    }
    ```
    
    ### **Fixed Position:**
    
    A fixed element is positioned relative to the browser window (viewport).
    
    It remains in the same position even when the page is scrolled.
    
    ```css
    .button{
        position: fixed;
        bottom: 20px;
        right: 20px;
    }
    ```
    
    ### **Sticky Position**
    
    A sticky element behaves like a relative element until it reaches a specified scroll position.
    
    After that, it behaves like a fixed element.
    
    ```css
    nav{
        position: sticky;
        top: 0;
    }
    ```
    
    ### **Position Offsets**
    
    The following properties are used to move positioned elements.
    
    #### `top`
    
    Moves the element downward from the top.
    
    ```css
    top:20px;
    ```
    
    #### `right`
    
    Moves the element from the right side.
    
    ```css
    right:15px;
    ```
    
    ---
    
    #### `bottom`
    
    Moves the element upward from the bottom.
    
    ```css
    bottom:25px;
    ```
    
    ---
    
    #### `left`
    
    Moves the element from the left side.
    
    ```css
    left:30px;
    ```
    
    #### `z-index`
    
    ```css
    z-index: 10;
    ```
    
    ### When to use each Position:
    
    | Position | Common Uses |
    | --- | --- |
    | `static` | Default positioning |
    | `relative` | Small adjustments, parent for absolute elements |
    | `absolute` | Badges, icons, overlays, tooltips |
    | `fixed` | Floating buttons, chat widgets, back-to-top buttons |
    | `sticky` | Sticky navigation bars, table headers |
- # **CH-10 Flexbox**
    
    ### Float Property:
    
    The **`float`** property is used to position an element to the **left** or **right** of its container, allowing other content to wrap around it.
    
    It was commonly used for page layouts in older websites but has largely been replaced by **Flexbox** and **CSS Grid** because they provide more flexible and responsive layouts.
    
    ```css
    img{
        float: right;
    }
    ```
    
    ### Flexbox:
    
    Flexbox (Flexible Box Layout) is a CSS layout model used to **arrange, align, and distribute space** among items inside a container.
    
    It makes it easier to create responsive and flexible layouts.
    
    ```css
    container {
      display: flex; /* by this method we initialize the flexbox */
    }
    
    /* After applying display: flex, the selected element becomes a Flex Container, and all its direct children become Flex Items. */
    ```
    
    ### Flex Direction:
    
    The `flex-direction` property defines the direction in which flex items are placed.
    
    ```css
    .container{
        flex-direction: row;
    }
    ```
    
    #### Different values in flex-direction:
    
    | Value | Purpose |
    | --- | --- |
    | `row` | Left to Right (Default) |
    | `row-reverse` | Right to Left |
    | `column` | Top to Bottom |
    | `column-reverse` | Bottom to Top |
    
    ### Flex Properties for the Parent (Container)
    
    #### 1. `flex-wrap`
    
    Controls whether flex items stay on one line or move to the next line.
    
    ```css
    flex-wrap:wrap;
    ```
    
    Values:
    
    - `nowrap`
    - `wrap`
    - `wrap-reverse`
    
    ---
    
    #### 2. `justify-content`
    
    Aligns items along the **main axis**.
    
    ```css
    justify-content:center;
    ```
    
    Common values:
    
    - flex-start
    - center
    - flex-end
    - space-between
    - space-around
    - space-evenly
    
    ---
    
    #### 3. `align-items`
    
    Aligns items along the **cross axis**.
    
    ```css
    align-items:center;
    ```
    
    Common values:
    
    - stretch
    - center
    - flex-start
    - flex-end
    
    ---
    
    #### 4. `align-content`
    
    Aligns multiple rows of flex items when extra space is available.
    
    This property works only when `flex-wrap` is enabled.
    
    ### Flex Properties for the Children (Items)
    
    #### 1. `order`
    
    Changes the display order of an item.
    
    ```css
    .item{
        order:2;
    }
    ```
    
    ---
    
    #### 2. `align-self`
    
    Overrides the alignment of an individual flex item.
    
    ```css
    align-self:center;
    ```
    
    ---
    
    #### 3. `flex-grow`
    
    Specifies how much an item should grow relative to the other items.
    
    ```css
    flex-grow:1;
    ```
    
    ---
    
    #### 4. `flex-shrink`
    
    Specifies how much an item should shrink when space is limited.
    
    ```css
    flex-shrink:1;
    ```
    
    ---
    
    #### 5. `flex-basis`
    
    Defines the initial size of a flex item before extra space is distributed.
    
    ```css
    flex-basis:200px;
    ```
    
- # **CH-11 CSS Grid**
    
    CSS Grid Layout is a **two-dimensional layout system** used to arrange elements in rows and columns.
    
    Unlike Flexbox, which is mainly used for **one-dimensional layouts** (either row or column), CSS Grid allows us to control both rows and columns simultaneously.
    
    It is commonly used to create complete webpage layouts.
    
    ### Grid Container:
    
    The parent element on which `display: grid` is applied.
    
    ```css
    div {
        display: grid;
    }
    ```
    
    ### Grid Item:
    
    The direct children of grid container are called grid items.
    
    ```css
    <div class="container">
        <div class="item">1</div>
        <div class="item">2</div>
        <div class="item">3</div>
    </div>
    ```
    
    ### Grid Columns:
    
    Used to define the number and size of  columns.
    
    ```css
    .container{
        display:grid;
        grid-template-columns: 200px 200px 200px;
    }
    
    /* Here the values we have given in the grid-template-column are the lengths of 3 columns, each of 200px */
    ```
    
    #### Fraction tag:
    
    The `fr` unit represents a fraction of the available space.
    
    ```css
    .container{
        display:grid;
        grid-template-columns:1fr 2fr 1fr;
    }
    ```
    
    ```
    💡Note:
    
    Here the fraction command helps us to divide the columns as per our choices.
    
    as in above given example we have given lengths as 1fr 2fr 1fr this means the first column and third column will have length of 1 fraction and second column will have length of 2 fractions.
    
    ```
    
    ### Grid Rows:
    
    Used to define the height of rows.
    
    ```css
    .container{
        grid-template-rows:100px 150px;
    }
    
    /* Same as in columns the given lengths are the heights of two rows */
    ```
    
    ### Gap:
    
    Used to add spaces between rows and columns.
    
    ```css
    row-gap:20px;
    column-gap:15px;
    ```
    
    #### Repeat function:
    
    It is used as a shorthand to write the length of rows and columns.
    
    Instead of:
    
    ```css
    grid-template-columns:200px 200px 200px;
    ```
    
    We can write:
    
    ```css
    grid-template-columns:repeat(3,200px);
    ```
    
    #### Minmax() Function:
    
    Used to set the minimum and maximum size of a grid.
    
    ```css
    grid-template-columns:repeat(3,minmax(150px,1fr));
    
    /* Each column
    Minimum width → 150px
    Maximum width → 1 fraction */
    ```
    
    ### **Auto-fit**
    
    Automatically fits as many columns as possible.
    
    ```css
    grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
    ```
    
    Useful for responsive layouts.
    
    ### **Auto-fill**
    
    Similar to `auto-fit`, but keeps empty columns if space is available.
    
    ```css
    grid-template-columns:repeat(auto-fill,minmax(200px,1fr));
    ```
    
    ### Placing Grid Items:
    
    #### Grid Column:
    
    Used to specify how many columns an item should occupy.
    
    ```css
    .item{
        grid-column:1/3;
    }
    
    /* Here the item will take space of 2 columns.
    The item starts at grid line 1 and ends at grid line 3.*/
    ```
    
    #### grid-row:
    
    Used to specify how many rows an item should occupy.
    
    ```css
    .item{
        grid-row:1/3;
    }
    
    /* Here the item will take space of 2 rows.
    The item starts at grid line 1 and ends at grid line 3.*/
    ```
    
    #### Grid Area:
    
    A shorthand for:
    
    - grid-row-start
    - grid-column-start
    - grid-row-end
    - grid-column-end
    
    ```css
    .item{
        grid-area:1/1/3/3;
    }
    ```
    
    ### Grid Alignments:
    
    #### Justify Items:
    
    Aligns items horizontally inside their cells.
    
    ```css
    justify-items:center;
    ```
    
    #### align-items:
    
    Aligns items vertically.
    
    ```css
    align-items:center;
    ```
    
    #### justify-content:
    
    Aligns the **entire grid** horizontally.
    
    ```css
    justify-content:center;
    ```
    
    #### align-content:
    
    Aligns the **entire grid** vertically.
    
    ```css
    align-content:center;
    ```
    
    ### **Difference Between Flexbox and Grid**
    
    | Flexbox | Grid |
    | --- | --- |
    | One-dimensional | Two-dimensional |
    | Row OR Column | Rows AND Columns |
    | Best for components | Best for page layouts |
    | Easier for small layouts | Better for complex layouts |
    
    ### **When to Use CSS Grid**
    
    Use Grid when:
    
    - Creating webpage layouts
    - Dashboards
    - Gallery layouts
    - Card layouts
    - Pricing sections
    - Image grids
    - Admin panels
    
    Use Flexbox when:
    
    - Navigation bars
    - Buttons
    - Menus
    - Small components
    - Centering elements
- # **CH-12 Pseudo Classes & Elements**
    
    ### **Pseudo-Classes & Pseudo-Elements:**
    
    Pseudo Classes and Pseudo Elements allow us to style elements based on **their state** or **specific parts** without adding extra HTML.
    
    - **Pseudo Class (`:`)** → Styles an element based on its **state** or **position**.
    - **Pseudo Element (`::`)** → Styles a **specific part** of an element.
    
    ### **Pseudo Classes:**
    
    A pseudo class selects an element when it is in a particular state.
    
    #### Hover:
    
    Applies styles when the mouse pointer is placed over an element.
    
    ```css
    button:hover{
        background-color:green;
        color:white;
    }
    ```
    
    #### Active:
    
    Applies styles while an element is being clicked.
    
    ```css
    button:active{
        transform:scale(0.95);
    }
    ```
    
    #### Visited:
    
    Styles links that have already been visited.
    
    ```css
    a:visited{
        color:purple;
    }
    
    /* Works only with <a> tag */
    ```
    
    #### Link:
    
    Styles link that have not been visited.
    
    ```css
    a:link{
        color:blue;
    }
    ```
    
    #### First Child:
    
    Selects the first child of the parent container.
    
    ```css
    li:first-child{
        color:red;
    }
    ```
    
    ```
    💡Note:
    
    Same as it is for Last Child.
    
    ```
    
    #### nth Child:
    
    Selects a child based on its position.
    
    ```css
    li:nth-child(2){
        color:green;
    }
    
    /* It will apply style to the 2nd child of the list */
    ```
    
    ### Pseudo Elements:
    
    They help in styling a specific part of an element.
    
    #### Before:
    
    Creates content before an element.
    
    ```css
    h1::before{
        content:"🔥 ";
    }
    
    /* It will add the fire emoji before the content of <h1> tag */
    ```
    
    ```
    💡Note:
    
    Similarly, `::after` is used to add content after an element
    
    ```
    
    #### Difference Between Pseudo Class and Pseudo Element:
    
    | Pseudo Class | Pseudo Element |
    | --- | --- |
    | Uses one colon (`:`) | Uses two colons (`::`) |
    | Styles an element's state | Styles a specific part of an element |
    | Example: `:hover` | Example: `::before` |
    | Example: `:focus` | Example: `::after` |
- # **CH-13 CSS Overflow**
    
    The `overflow` property controls what happens when the content inside an element is **larger than the element's defined width or height**.
    
    This commonly happens when:
    
    - Text is too large for a box.
    - An image is larger than its container.
    - Content extends outside a fixed-height element.
    - A child element is bigger than its parent.
    
    ### Overflow Visible (Default):
    
    The content is allowed to extend outside the element.
    
    ```css
    .box {
        width: 200px;
        height: 100px;
        overflow: visible;
    }
    ```
    
    ```
    💡Note:
    
    By this command the content will be completely visible, although it will be going out side the container width or height.
    
    ```
    
    ### Overflow Hidden:
    
    Hides anything that extends outside the element.
    
    ```css
    .box {
        width: 200px;
        height: 100px;
        overflow: hidden;
    }
    ```
    
    ### Overflow Scroll:
    
    It **adds scrollbars to the container** so that the content remains in the box & will still be visible.
    
    ```css
    .box {
        width: 200px;
        height: 100px;
        overflow: scroll;
    }
    ```
    
    ### Overflow Auto:
    
    It adds scrollbars only when they are needed.
    
    ```css
    .box {
        width: 200px;
        height: 100px;
        overflow: auto;
    }
    ```
    
    ### Overflow-X:
    
    We use this property to control the overflow properties in the horizontal direction.
    
    ### Overflow-Y:
    
    We use this property to control the overflow properties in the vertical direction.
    
    ```css
    .box {
        overflow-x: hidden;
        overflow-y: auto;
    }
    ```
    
    ### Shorthand for Overflow:
    
    ```css
    .box {
        overflow: hidden auto;
    }
    
    /* Here the hidden property will be applied horizontally (x).
    and auto property will be applied vertically (y). */
    ```
    
- # **CH-14 Object Properties**
    
    CSS Object Properties control **how replaced elements** (such as images and videos) are displayed inside their container.
    
    The two main object properties are:
    
    - `object-fit`
    - `object-position`
    
    ### Replaced Elements:
    
    Replaced elements are HTML elements whose content comes from an external source.
    
    Examples:
    
    - `<img>`
    - `<video>`
    - `<iframe>`
    
    ### object-fit:
    
    The `object-fit` property specifies how an image or video should fit inside its container.
    
    #### Fill (Default):
    
    The replaced element is resized to fill the content box, which can distort its aspect ratio.
    
    - Aspect ratio is **not maintained**.
    - The image may look distorted.
    
    ```css
    img{
        width: 300px;
        height: 200px;
        object-fit: fill;
    }
    ```
    
    #### Contain:
    
    The entire image fits inside the container.
    
    - Aspect ratio is maintained.
    - Empty space may appear.
    
    ```css
    img{
        object-fit: contain;
    }
    ```
    
    #### Cover:
    
    The image completely covers the container.
    
    - Aspect ratio is maintained.
    - Some parts of the image may be cropped.
    
    ```css
    img{
        object-fit: cover;
    }
    ```
    
    #### Difference between Contain & Cover:
    
    | contain | cover |
    | --- | --- |
    | Entire image visible | Image fills container |
    | Empty space may appear | Image may be cropped |
    | No cropping | Cropping possible |
    | Best for logos | Best for profile pictures and cards |
    
    #### None:
    
    The image keeps its original size.
    
    If it's larger than the container, it overflows.
    
    ```css
    object-fit: none;
    ```
    
    #### Scale-Down:
    
    Chooses whichever is smaller between none and contain and applies that ratio.
    
    ```css
    object-fit: scale-down;
    ```
    
    ### Object Position:
    
    The `object-position` property specifies **which part of the image remains visible** when the image is cropped (usually with `object-fit: cover`).
    
    #### Center (Default):
    
    By this the center part will remain.
    
    ```css
    object-position: center;
    ```
    
    #### Top:
    
    By this the top part will be biased and will remain.
    
    ```css
    object-position: top;
    ```
    
    ```
    💡Note:
    
    This will be same for other values such as:
    
    - Bottom
    - Left
    - Right
    ```
    
    #### Custom Values:
    
    ```css
    object-position: 20% 40%;
    ```
    
- # **CH-15 CSS Transform, Transitions & Animations**
    
    ### CSS Transitions & Animations:
    
    Transitions and Animations are used to add motion and visual effects to elements on a webpage.
    
    - **Transition** → Smoothly changes an element from one state to another.
    - **Animation** → Creates continuous or complex movements using keyframes.
    
    ### CSS Transition:
    
    A transition allows CSS property values to change **smoothly** over a specified duration.
    
    ```css
    selector{
        transition: property duration timing-function delay;
    }
    ```
    
    ```css
    button{
        background-color: blue;
        transition: background-color 0.5s;
    }
    
    button:hover{
        background-color: green;
    }
    
    /* When the button is hovered, the background color changes smoothly. */
    ```
    
    ### Transition Properties
    
    #### Transition-property:
    
    Specifies which CSS property will transition.
    
    ```css
    transition-property: background-color;
    ```
    
    #### Transition Duration:
    
    Specifies how long the transition takes.
    
    ```css
    transition-duration: 1s;
    ```
    
    #### Transition Timing Function:
    
    Controls the speed curve of the transition.
    
    ```
    💡Note:
    
    Controlling speed curves means- It ensures the speed of transition coming in and going out.
    
    ```
    
    ```css
    transition-timing-function: ease-in-out;
    ```
    
    #### Transition Delay:
    
    Specifies how long to wait before the transition starts.
    
    ```css
    transition-delay: 0.3s;
    ```
    
    #### Transition Multiple Properties:
    
    You can animate more than one property.
    
    ```css
    transition: background-color 0.5s, transform 0.5s;
    ```
    
    ### CSS Transform
    
    The `transform` property changes an element's position, size, or rotation without affecting the document flow.
    
    #### translate():
    
    Used for moving the element.
    
    ```css
    transform: translate(50px,20px);
    
    /* Moves the element 50px right and 20px down.*/
    ```
    
    #### scale():
    
    Used in changing the size (Increasing/decreasing).
    
    ```css
    transform: scale(1.2);
    
    /* It will increase the size of the element 1.2 times */
    ```
    
    #### rotate():
    
    It rotates the element.
    
    ```css
    transform: rotate(45deg);
    ```
    
    #### skew():
    
    It stretches the element diagonally.
    
    ```css
    transform: skew(20deg);
    ```
    
    ### CSS Animations:
    
    CSS animations allow CSS properties to change through multiple stages defined by `@keyframes`.
    
    ### @keyframes:
    
    It defines the animation sequence.
    
    ```css
    @keyframes colorChange{
    
    from{
        background:red;
    }
    
    to{
        background:blue;
    }
    
    }
    ```
    
    #### Animation Name:
    
    Specifies which animation to use.
    
    ```css
    animation-name: colorChange;
    ```
    
    #### Animation Duration:
    
    specifies how long the animation runs.
    
    ```css
    animation-duration: 2s;
    ```
    
    #### Animation Timing Function:
    
    It controls the speed of animation.
    
    ```css
    animation-timing-function: ease;
    ```
    
    #### Animation Delay:
    
    It states the delay of animation.
    
    ```css
    animation-delay:1s;
    ```
    
    #### Animation Iteration Count:
    
    Specifies how many times the animation repeats.
    
    ```css
    animation-iteration-count:3;
    ```
    
    #### Animation Direction:
    
    Specifies the direction of animations.
    
    ```css
    animation-direction:alternate;
    ```
    
    #### Animation Fill Mode:
    
    Specifies which styles are applied before the animation starts and/or after it ends.
    
    ```css
    animation-fill-mode:forwards;
    ```
    
    ### Animation Shorthand:
    
    Instead of writing:
    
    ```css
    animation-name: bounce;
    animation-duration:2s;
    animation-timing-function:ease;
    animation-delay:0s;
    animation-iteration-count:infinite;
    animation-direction:alternate;
    ```
    
    Write:
    
    ```css
    animation:
    bounce 2s ease 0s infinite alternate;
    ```
    
    #### Example of writing animation to your Webpage:
    
    ```css
    .box {
        width: 100px;
        height: 100px;
    
        background-color: aquamarine;
    
        animation: move 1.5s linear 0s infinite alternate;
    }
    
    @keyframes move {
    
        from {
            transform: translateX(0px);
        }
    
        to {
            transform: translateX(10px)
        }
        
    }
    ```
    
    #### Difference Between Transitions and Animations:
    
    | Transition | Animation |
    | --- | --- |
    | Triggered by an event (e.g., `:hover`) | Can run automatically |
    | Moves between two states | Can have multiple keyframes |
    | Simpler | More powerful |
    | No `@keyframes` required | Requires `@keyframes` |
    
    #### When to Use:
    
    Use Transition for:
    
    - Hover effects
    - Buttons
    - Cards
    - Navigation menus
    - Color changes
    - Scaling
    
    Use Animation for:
    
    - Loading indicators
    - Typing effects
    - Floating objects
    - Rotating icons
    - Progress bars
    - Moving backgrounds
- # **CH-16 CSS Variables**
    
    CSS Variables (also called **Custom Properties**) allow us to store values in reusable variables. Instead of writing the same value multiple times, we can define it once and use it wherever needed.
    
    This makes the code easier to maintain and update.
    
    ### Syntax:
    
    CSS variables are declared using **`--`** (double hyphen).
    
    ```css
    :root {
    	--primary-color: blue;
    }
    ```
    
    To use a variable, we use the `var()` function.
    
    ```css
    h1 {
    	color: var(--primary-color);
    }
    ```
    
    ### Declaring Variables
    
    Custom properties declared on `:root` are available throughout the document through inheritance.
    
    ```css
    :root{
        --primary-color: #3498db;
        --secondary-color: #2ecc71;
        --text-color: white;
    }
    ```
    
    #### Using these variables:
    
    ```css
    body{
        background-color: var(--primary-color);
        color: var(--text-color);
    }
    
    button{
        background-color: var(--secondary-color);
    }
    ```
    
    ### Fallback Values
    
    If a variable doesn't exist, we can provide a fallback value.
    
    ```css
    color:var(--primary-color,black);
    ```
    
    If `--primary-color` is missing, `black` will be used.
    
    ### Local Variables:
    
    Variables can also be declared inside a specific selector, this way is known as local variable.
    
    ```css
    .card{
        --card-color: lightblue;
        background-color: var(--card-color);
    }
    
    .card h2{
        color: var(--card-color);
    }
    
    /* In this case, `--card-color` is available only inside `.card` and its child elements. */
    ```
    
    ```
    💡Note:
    
    - Variables start with **`--`**.
    - Variables are accessed using **`var()`**.
    - `:root` is generally used to declare global variables.
    - Variables can also be local to a specific selector.
    - Changing one variable updates every place where it is used.
    ```
    
- # **CH-17 CSS Filter Properties**
    
    There are some filters which CSS provides that helps us to enhance our images.
    
    these properties are:
    
    ### Blur Filter:
    
    Helps us to blur our image.
    
    ```css
    img {
      filter: blur(10px);
    }
    ```
    
    ### Brightness Filter:
    
    Helps in changing brightness of image.
    
    ```css
    img {
    	filter: brightness(50%);
    }
    ```
    
    ### Contrast Filter:
    
    Controls the difference between the light and dark areas of an element.
    
    ```css
    img {
    	filter: contrast(30%)
    }
    ```
    
    ### Grayscale Filter:
    
    Reduces the color saturation of the image. `100%` produces a fully grayscale image.
    
    ```css
    img {
    	filter: grayscale(60%)
    }
    ```
    
    ### Invert Filter:
    
    With this we can change our normal image into negative.
    
    ```css
    img {
    	filter: invert(1)
    }
    ```
    
    ### Opacity Filter:
    
    It helps us in managing the transparency of the image.
    
    ```css
    img {
    	filter: opacity(30%)
    }
    
    /* makes the element approximately 30% opaque.*/
    ```
    
    ```
    💡Note:
    
    There are many filters which CSS provides these are some of them which are used in general.
    
    ```
    
- # **CH-18 Media Queries & Responsiveness**
    
    Media Queries are used to make a website **responsive**, meaning the layout can adapt to different screen sizes and devices.
    
    For example, the same website should work properly on:
    
    - 💻 Desktop
    - 💻 Laptop
    - 📱 Mobile
    - 📟 Tablet
    
    Without media queries, a layout designed for a large screen may look broken on a smaller screen.
    
    ### Basic Syntax
    
    The basic syntax is:
    
    ```css
    @media (condition) {/* CSS rules */
    }
    ```
    
    ```css
    @media (max-width: 600px) {
        body {
            background-color: lightblue;
        }
    }
    ```
    
    When the viewport width is **600px or less**, apply these styles.
    
    ### `max-width`
    
    Applies styles when the viewport is **at or below** the specified width.
    
    ```css
    @media (max-width:768px) {
        .container {
            flex-direction:column;
        }
    }
    
    /* It means when the viewport width will be less than 768px then containers will have the flex-direction: column property */
    ```
    
    ### `min-width`
    
    Applies styles when the viewport is **at or above** the specified width.
    
    ```css
    @media (min-width:768px) {
        .container {
            display:flex;
        }
    }
    
    /* It means when the viewport width will be more than 768px then containers will have the display:flex property */
    ```
    
    ### Combining Conditions:
    
    You can combine multiple conditions using `and`.
    
    ```css
    @media (min-width:600px)and (max-width:900px) {body {
            background-color:lightgreen;
        }
    }
    ```
    
    This applies when the viewport is: 600px ≤ width ≤ 900px.
    
    ### Changing Layout:
    
    One of the most common uses of media queries is changing a horizontal layout into a vertical layout.
    
    #### Desktop:
    
    ```css
    .container {
        display:flex;
        gap:20px;
    }
    ```
    
    On smaller screens:
    
    ```css
    @media (max-width: 600px) {
        .container {
            flex-direction: column;
        }
    }
    ```
    
    therefore:
    
    ```
    Desktop:
    
    [ Box 1 ] [ Box 2 ] [ Box 3 ]
    
    Mobile:
    
    [ Box 1 ]
    [ Box 2 ]
    [ Box 3 ]
    ```
    
    ### Changing Font Size:
    
    You can also change typography according to screen size.
    
    ```css
    h1 {
        font-size:50px;
    }@media (max-width:600px) {h1 {
            font-size:32px;
        }
    }
    ```
    
    On a smaller screen, the heading becomes smaller.
    
    ### Changing Width:
    
    For example:
    
    ```css
    .card {
        width:600px;
    }
    ```
    
    On mobile:
    
    ```css
    @media (max-width:600px) {
        .card {
            width:90%;
        }
    }
    ```
    
    Instead of forcing a `600px` wide card onto a small screen, the card uses most of the available screen width.
    
    ### Hiding Elements:
    
    Media queries can also hide elements on certain screen sizes.
    
    ```css
    @media (max-width:600px) {
        .desktop-menu {
            display:none;
        }
    }
    ```
    
    The element will not be displayed when the viewport is 600px or smaller.
    
    ### Common Breakpoints:
    
    There are no mandatory breakpoints in CSS. You choose them according to **when your design needs to change**.
    
    Common examples are:
    
    - 576px
    - 768px
    - 992px
    - 1200px
    
    For example:
    
    ```css
    @media (max-width:768px) {/* Tablet/mobile adjustments */
    }
    ```
    
    ### Mobile-First Approach:
    
    A common modern approach is to design for smaller screens first and then add styles for larger screens.
    
    Example:
    
    ```css
    .container {
        display:flex;
        flex-direction:column;
    }@media (min-width:768px) {
        .container {
            flex-direction:row;
        }
    }
    ```
    
    ### Desktop-First Approach:
    
    You can also start with the desktop design:
    
    ```css
    .container {
        display:flex;
        flex-direction:row;
    }@media (max-width:768px) {
        .container {
            flex-direction:column;
        }
    }
    ```
    
    ### Media Queries with Grid:
    
    Media queries are especially useful with CSS Grid.
    
    For example:
    
    ```css
    .grid {
        display:grid;
        grid-template-columns:repeat(3,1fr);
    }
    ```
    
    On smaller screens:
    
    ```css
    @media (max-width:700px) {
        .grid {
            grid-template-columns:1fr;
        }
    }
    ```
    
    #### Desktop:
    
    ```
    ┌─────┐ ┌─────┐ ┌─────┐
    │  1  │ │  2  │ │  3  │
    └─────┘ └─────┘ └─────┘
    ```
    
    #### Mobile:
    
    ```
    ┌─────────┐
    │    1    │
    └─────────┘
    ┌─────────┐
    │    2    │
    └─────────┘
    ┌─────────┐
    │    3    │
    └─────────┘
    ```
    
    ### Orientation:
    
    Media queries can also check the orientation of the device.
    
    #### Landscape
    
    ```css
    @media (orientation:landscape) {body {
            background-color:lightblue;
        }
    }
    ```
    
    #### Portrait
    
    ```css
    @media (orientation:portrait) {body {
            background-color:lightgreen;
        }
    }
    ```
    
    ### Viewport Meta Tag:
    
    When building responsive websites, you should also include this inside your `<head>`:
    
    ```css
    <metaname="viewport"content="width=device-width, initial-scale=1.0">
    ```
    
    This tells the browser to use the device's actual viewport width.
    
    Without it, responsive layouts can behave incorrectly on mobile devices.
    
    ### Media Queries Don't Automatically Make a Website Responsive:
    
    Adding:
    
    ```css
    @media (max-width:600px) {
        ...
    }
    ```
    
    doesn't magically make everything responsive.
    
    You still need to design your layout properly.
    
    For example, avoid unnecessarily fixed widths like:
    
    ```css
    .box {
        width:1000px;
    }
    ```
    
    on a mobile layout.
    
    Instead, consider:
    
    ```css
    .box {
        width:90%;
        max-width:1000px;
    }
    ```
    
    Then use media queries when the layout actually needs to change.
    
    ### The most important syntax to remember:
    
    ```css
    @media (max-width:768px) {/* styles for smaller screens */
    }
    ```
    
    and:
    
    ```css
    @media (min-width:768px) {/* styles for larger screens */
    }
    ```