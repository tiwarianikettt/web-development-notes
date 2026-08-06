# HTML - Complete Notes

- **What is HTML?**
    
    HTML (Hyper Text Markup Language) is the standard markup language used to structure the content of web pages. It defines elements such as headings, paragraphs, images, links, tables, and forms.
    
    Remember:
    
    - HTML → Structure
    - CSS → Appearance
    - JavaScript → Behavior
    
    ### Useful shortcuts in VS Code
    
    | Shortcut | Expands To |
    | --- | --- |
    | `!` | HTML boilerplate |
    | `div` | `<div></div>` |
    | `ul>li*5` | List with 5 items |
    | `nav>ul>li*4>a` | Navigation menu |
    | `img` | Image tag |
- **CH- 01: Creating our first website**
    
    ### **Starting a website:**
    
    Starting by entering the file name in VS code application like: index.html.
    
    ### **Basic HTML page structure:**
    
    ```html
    <!DOCTYPE html> <!-- It specifies this is an HTML5 document / file. -->
    <html lang="en"> <!-- Root of an HTML page. Here lang is a key word. -->
    <head> <!-- It contains the meta data of the page. Meta data- Structured information of page's size, format, etc. -->
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>ANIKET TIWARI</title> <!-- Title of website. -->
        <link rel="stylesheet" href="style.css">
    </head> <!-- Head closing tag. -->
    <body> <!-- Contains the main body of the page. -->
    		<h1>This is my first website.</h1> <!-- Tabs to enter headings. -->
    		<p>MY PARAGRAPH</p> <!-- Tabs to enter paragraphs. -->
        <script src="script.js"></script>
    </body> <!-- Body closing tag. -->
    </html>
    ```

    <aside>
    
    💡NOTE :

    1. Tags are like container for content or other HTML tags. 
    
    📄 HTML File → 🌐 Browser → 🖥️ Rendered Page
    
    1. Most of the HTML tags have opening and closing tags between them the data or content exists.
    2. File extension can either be .htm or .html
    3. Comments in HTML: They are the content which are not to pass on, they can be written as- <! — HTML Comment — >
    4. Case sensitivity: HTML is not a case sensitive language ```<H1>``` and ```<h1>``` are same.
    </aside>
    
- **CH- 02: Tags in HTML**
    
    ### Semantic tags make HTML easier to read, improve accessibility, and help search engines understand the page structure.
    
    ### **HTML Elements:**
    
    The fundamental building block of HTML where everything from starting to ending tag comes.
    
    ```html
    <body> <!-- opening tag -->
    content
    </body> <!-- closing tag -->
    ```
    
    ### **HTML Attributes:**
    
    They are special keywords used to add more information about an element or to modify its behaviour.
    
    Also, we can either use single or double quotes in attributes.
    
    ```html
    <a href="https://google.com"> click me </a>
    <!-- href is an attribute -->
    ```
    
    ### **Heading tag:**
    
    It is used to mark the heading of our page, from sizes h1 to h6.
    
    this tag is written as:
    
    ```html
    <h1>HEADING 1</h1>
    <h2>HEADING 2</h2>
    <!-- from h1 to h2 size decreases -->
    ```
    
    ### **Paragraph tag:**
    
    They are used to add paragraphs inside a page.
    
    ```html
    <p>HERE I CAN WRITE PARAGRAPHS between these opening and closing tags.</p>
    ```
    
    ### **Anchor tag:**
    
    This tag is used to add links to an existing content inside and HTML page.
    
    ```html
    <a href="https://google.com"> click me </a>
    ```
    
    <aside>

    💡NOTE :
    
    By using this anchor tag when we click on the given link the new page will get open on the same tab. But, if we want to open the new page in different tab then we have to use target attribute.
    
    ```html
    <a href="https://google.com" img src="image link" alt="Google" target="_blank"> </a>
    <!-- This helps in adding clickable image link in    web page -->
    ```
    
    </aside>
    
    ### **Img tag (Image):**
    
    It is used to add image in an HTML page.
    
    ```html
    <img width=230 height=300 src="image.jpg" alt="school image">
    <!-- 
    image.jpg is url of the respective image.
    alt is an attribute.
    width and height are ways to edit pixels of image and they are optional.
    the code will still work if we do not enter the height and width. 
    -->
    ```
    
    <aside>

    💡NOTE :
    
    While working with image tab after src we have an alt attribute.
    1. The work of alt attribute is, if by any chance we didn’t add any image or we have entered wrong URL then the alt attribute will help us to tell the user of the page to define what image it is related to.
    2. Hence as written in above code alt=”school image”. if we write any wrong URL of image it will just show a text at the page saying “school image” so that the client or user can understand what the image is about.
    
    Also, we can scale the image as per our choices with the help of image tag.
    1. As written in the above code we can fix height and width as per our choice and this is optional. we can only enter height or only width it will adjust automatically and if do not enter any of them then also the image will display in larger area.
     
    
    </aside>
    
    ### **Bold, Italic & Underline tags:**
    
    They are used to highlight the text with their respective properties.
    
    ```html
    <b> these are bold tags </b>
    <i> these are italic tags </i>
    <u> these are underline tags </u>
    ```
    
    ### **Br tags (Break):**
    
    This tag is used to insert single line breaks in the document or page without starting new paragraph.
    
    ```html
    <p>
    This is the first line. I want to add empty space after this line.<br>
    My name is Aniket Tiwari<br>
    this is the last line.
    </p>
    <!-- This tag is always used at the end of the line after which we want to add space line -->
    ```
    
    ### **Big & Small tags:**
    
    We can make the text a bit bigger or smaller using big & small tags respectively.
    
    ```html
    <big> This is BIG tag.</big>
    <small> This is small tag.</small>
    ```
    
    ### **Hr tag (Horizontal):**
    
    This tag is used to add horizontal line after a line of text.
    
    ```html
    <p>
    My name is Aniket Tiwari <hr>
    I am 19 years old.
    </p>
    <!-- This tag is used at the end of the line after wich we want to add horizontal line. -->
    ```
    
    ### **Subscript & Superscript tags:**
    
    We can add superscripts and subscripts using these tags.
    
    ```html
    <sub> this is subscript tag. </sub> <!-- It helps us to write smaller text below normal text. -->
    <sup> this is superscript tag. </sup> <!-- It helps to write smaller text over normal text. -->
    ```
    
    ### **Pre tag:**
    
    Used to display text as it is (without ignoring spaces & next line)
    
    ```html
    <pre> This
    is a 
    sample
    text.
    </pre>
    <!-- Here we have written a single line in different different spaces or lines if we do not use the pre tag it will ignore the spaces we have given between words and give us the output as: This is a sample text. But if we will use the pre tag it will give us the output as it is. -->
    ```
    
    ### **Header & Footer:**
    
    To add header and footer we use the following tabs:
    
    ```html
    <header>_______</header>
    <footer>_______</footer>
    ```
    
    ### Main Tag:
    
    Represents the primary content of the page.
    
    ```html
    <main>Main_content</main>
    ```
    
    ### Section Tag:
    
    This helps dividing our web page into different sections.
    
    ```html
    <main>
      <section>sectional_division_inside_main_tag</section>
    </main>
    ```
    
    ### Article Tag:
    
    It helps in adding stories, text and all in our web page.
    
    ```html
    <header>
         <h1>My Portfolio</h1>
    </header>
    
    <main>
        <pre>
    			Name: Aniket TIWARI
          Age: 19
          DOB: 31/05/2007
        </pre>
          <br />
    <section>Hobbies: Sports, Working out | Singing</section>
    <section>Qualifications: Passed 12<sup>th</sup></section>
    <article>Hi I am making this testing website for my experience.</article>
    </main>
    <footer><h5>you can contact me at: tiwarianiket@gmail.com</h5></footer>
      </body>
    ```
    
    ### Aside Tag:
    
    Contains related information.
    
    ```html
    <aside>Recent Posts Advertisements Related Links</aside>
    ```
    
    ### Div tag:
    
    Div is container used for other HTML elements.
    It is a block element (Takes complete width).
    The content written under the div tag is consider as a whole single element.
    
    ```html
     <div>
          <p>Hi I am ANIKET</p>
          <p>I am 19 years old.</p>
     </div>
     <!-- Here these two paragraphs written between div tag will be considered as a whole single unit. -->
    ```
    
    ### Span tag:
    
    Span is also a container for other HTML elements.
    It is an inline elements (Takes width as per size or requirement).
    
    ```html
    <span>
    	<p>Hi I am ANIKET</p>
    	<p>I am 19 years old.</p>
    </span>
    ```
    
    <aside>

    💡NOTE :
    
    Here are some tags which don’t have ending tags with them.
    
    ```html
    <br>, <hr>, <img>, <input>, <meta>, <link>
    ```
    
    </aside>
    
    ### Some other attributes:
    
    These can be used with almost every element.
    
    | Attribute | Purpose |
    | --- | --- |
    | id | Unique identifier |
    | class | Group elements |
    | style | Inline CSS |
    | title | Tooltip |
    | hidden | Hide element |
    | draggable | Make element draggable |

    
- ## **CH-03: Tables, Lists in HTML**
    
    ### **Tables in HTML**:
    
    Helps in creating a basic table structure in a web page.
    Table tag- <table>_______</table>
    
    ```html
    <table> <!-- Opening tab for tables -->
        <tr> <!-- "tr"- represents table rows where we can enter the elements of table -->
            <th>Name</th> <!-- "th"- represents the table        heading -->
            <th>Age</th> <!-- Opening and closing tabs of th -->
            <th>Work</th>
        </tr> <!-- Closing tab of table rows (tr) -->
        <tr> <!-- Opening tab of table rows (tr) -->
            <td>Aniket Tiwari</td> <!-- td- represents table     data that will be visible under the respective headings      order wise -->
            <td>19</td> <!-- Opening and closing tabs of td -->
            <td>Programming</td>
        </tr>
    </table> <!-- Closing tab for tables -->
    ```
    
    <aside>

    💡NOTE :
    
    - Every time when we had to write a row we have to use table row (tr) tabs.
    - This method only gives a basic skeleton of a table to add borders and design we have to use CSS with HTML.
    </aside>
    
    ### <b>Thead Tbody tags: </b>
    
    These tags are used to wrap up the whole table heading and table body together.
    
    If we use <thead>______</thead> tag it will wrap up the heading part togeather and between these tags only heading part of the tables come.
    
    If we use <tbody>_______</tbody> tag it will wrap up the rest data of the table other than the heading part.
    
    ### **Colspan & Rowspan functions in table:**
    
    They are used to merge columns or rows.
    
    ```html
    <table>
        <tr>
            <th>Name</th>
            <th>Age</th>
            <th>Work</th>
        </tr>
        <tr>
            <td>Aniket Tiwari</td>
            <td colspan="2"> 19</td> <!-- Here colspan function is used with value "2" (Written in quotes) this means that this particular data will take space of two columns -->
            <!-- Here we have removed the third data to make space for 2 columns -->
        </tr>
    </table>
    
    <!-- In this same way rowspan function also works -->
    ```
    
    ### **Adding caption to the tables in HTML:**
    
    By this process we can give title to our tables.
    This function is known as Caption and the tags are: <caption>_______</caption>
    
    ```html
    <table>
        <caption>Person's Details</caption> <!-- Here we have used caption function with opening and closing tabs between which we have given the title of our table -->
        <tr>
            <th>Name</th>
            <th>Age</th>
            <th>Work</th>
        </tr>
        <tr>
            <td>Aniket Tiwari</td>
            <td>19</td>
            <td>Programming</td>
        </tr>
    </table>
    ```
    
    ## **Lists in HTML:**
    
    ### <b>Types of HTML Lists:</b>
    
    - **Unordered lists**- Displays items using bullets.
    
    ```html
    <ul> <!-- Opening tab for unordered lists -->
        <li>Aniket Tiwari</li> <!-- li- represents list contents -->
        <li>19 years old</li>
        <li>Learning web development</li>
    </ul> <!-- Closing tab for unordered lists -->
    ```
    
    <aside>
    💡NOTE :
    
    Here in unordered lists we can change the bullets into squares or circles by using type attribute.
    
    ```html
    <ul type="square"> <!-- It will convert bullets into square shape -->
        <li>Aniket Tiwari</li>
        <li>19 years old</li>
        <li>Learning web development</li>
    </ul>
    ```
    
    </aside>
    
    - **Ordered lists**- Displays items in numbered forms.
    
    ```html
    <ol> <!-- Opening tab for ordered lists -->
       <li>Aniket Tiwari</li>
       <li>19 years old</li>
       <li>Learning web development</li>
    </ol> <!-- Closing tab for ordered lists -->
    ```
    
    <aside>
    💡NOTE :
    
    Here in ordered lists we can change the numbers into roman numerals or alphabets by using type attribute.
    
    - type=”I”- For capital roman numerals.
    - type=”i”- For small roman numerals,
    - type=”1”- For default numbers.
    - type=”A”- For capital letters.
    - type=”a”- For small letters.
    
    ```html
    <ol type="I">
       <li>Aniket Tiwari</li>
       <li>19 years old</li>
       <li>Learning web development</li>
    </ol> <!-- Closing tab for ordered lists -->
    ```
    
    </aside>
    
    - **Definition lists**- It displays the contents and items as title and their definitions.
    
    ```html
    <dl> <!-- Opening tab for definition list -->
       <dt>Aniket Tiwari</dt> <!-- dt- represents definition title -->
       <dd>19 years old boy who lives in delhi</dd> <!-- dd- represents definition of definition -->
    </dl> <!-- Closing tab for definition list -->
    ```
    
- ## **CH-04: Forms in HTML**
    
    ### HTML forms are used to collect inputs from the user.
    
    #### Form tag is used for the same purpose.
    
    ```
    <form>
    
    — Elements of form —
    
    </form>
    ```

    There are different form elements for different kinds of user inputs.
    
    ### Input elements:
    
    It can be of different types like- text, checkbox, submit and buttons, etc. and we also have a file type.
    
    ```html
    <h1>Details</h1>
       <form action="">
        <label for="fname">First Name:</label> <input type="text" id="fname" name="fname">
    ```
    
    <aside>
    💡NOTE :
    
    Here in the above code we have used input tag with type attribute which is by default text type. 
    This input type can be of many types other than text like- buttons, date, color, etc.
    
    With type attribute we have choose radio type which gives us choice to choose a single option.
    
    Value is also an attribute where we have written our options that will be given to choose in our form. 
    
    Label tag is used so as to make it in line element other than block element.
    
    </aside>
    
    <aside>
    💡NOTE :
    
    Different types of Input types:
    
    | Type | Purpose |
    | --- | --- |
    | text | Text input |
    | email | Email address |
    | password | Password |
    | date | Date picker |
    | file | Upload file |
    | color | Color picker |
    | number | Numbers |
    | range | Slider |
    | checkbox | Multiple choices |
    | radio | Single choice |
    </aside>
    
    ### <b>Text area element:</b>
    
    It defines a multi line text input columns and rows attributes can be used to size the text area
    
    ```html
    <textarea name="Feedback" id="" placeholder="Please write your feedback here"></textarea>
    ```
    
    ### <b>Select element:</b>
    
    Defines a drop down list.
    
    ```html
    <h5>Select your City:</h5>
        <select name="city" id="">
          <option value="Select">Select</option>
          <option value="Delhi">Delhi</option>
          <option value="Mumbai">Mumbai</option>
          <option value="Uttarpradesh">Uttarpradesh</option>
        </select>
    ```
    
- ## **CH-05: HTML Entities**
    
    HTML entities are special codes used to display reserved characters or symbols that cannot be typed directly in HTML.
    
    ### <b>Common Entities:</b>
    
    | Entity | Output | Use |
    | --- | --- | --- |
    | `&lt;` | `<` | Less than |
    | `&gt;` | `>` | Greater than |
    | `&amp;` | `&` | Ampersand |
    | `&copy;` | © | Copyright |
    | `&nbsp;` | Space | Non-breaking space |
    
    ```html
    <p>5 &lt; 10</p>
    <p>&copy; 2026 Aniket Tiwari</p>
    ```
    
- ## **CH-06: Multimedia & Embedded Content**
    
    ### <b>Audio:</b>
    
    It is used to embed audio files in the web page.
    
    ```html
    <audio controls>
        <source src="song.mp3" type="audio/mpeg">
    </audio>
    ```
    
    <aside>
    💡NOTE :
    
    The attributes used in this are:
    
    - controls: This helps in embedding audio controls like pause, start, etc.
    - autoplay: By using this the audio will start play by it self once the web page refreshes.
    - loop: This allows the video to play continuously without stopping.
    - muted: By using this attribute the video will be muted un till we unmutes.
    </aside>
    
    ### <b>Video:</b>
    
    It is used to embed videos in the web page.
    
    ```html
    <video width="500" controls>
        <source src="video.mp4" type="video/mp4">
    </video>
    ```
    
    <aside>
    💡NOTE :
    
    The attributes used in this are:
    
    - controls: This helps in embedding video controls like pause, start, etc.
    - autoplay: By using this the video will start play by it self once the web page refreshes.
    - muted: By using this attribute the video will be muted until we unmutes.
    - loop: This allows the video to play continuously without stopping.
    - poster
    </aside>
    
    ### <b>iframe:</b>
    
    An iframe can embed YouTube videos, Google Maps, documents, or another webpage inside the current webpage.
    
    ```html
    <iframe src="https://www.youtube.com/embed/VIDEO_ID" width="500" height="300">
    </iframe>
    ```
    
- ## **Practice Sessions**
    
    ### <b>HTML Best Practices</b>
    
    - Use semantic HTML.
    - Always write meaningful `alt` text.
    - Use lowercase tag names.
    - Indent code properly.
    - Keep HTML for structure only.
    - Use external CSS and JavaScript files.
    - Avoid excessive `<br>` tags for spacing.
    - Validate your HTML.
    - Use descriptive file and folder names.