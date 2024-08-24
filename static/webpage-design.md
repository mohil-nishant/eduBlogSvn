

### **Introduction to Web Page Designing Using HTML**

Creating a webpage with HTML is the foundation of web development. This guide will help you understand basic HTML elements and attributes, enabling you to design simple yet effective web pages.

#### **1. Understanding HTML Documents**

HTML (HyperText Markup Language) is the standard language for creating webpages. An HTML document consists of elements that define the structure and content of the webpage. Every HTML document starts with the `<!DOCTYPE html>` declaration, followed by the `<html>` element, which encompasses all the content.

- **Creating and Saving an HTML Document**:  
  To create an HTML document, you can use any text editor. After writing the HTML code, save the file with a `.html` extension, such as `index.html`.

#### **2. HTML Elements: Container vs. Empty Elements**

- **Container Elements**: These elements contain content between an opening tag and a closing tag. Examples include `<div>`, `<p>`, `<h1>` to `<h6>`, etc.
  ```html
  <p>This is a paragraph.</p>
  ```

- **Empty Elements**: These elements do not have any content between the opening and closing tags. They are self-closing. Examples include `<br>`, `<hr>`, `<img>`.
  ```html
  <br> <!-- Line Break -->
  <hr> <!-- Horizontal Rule -->
  ```

#### **3. Essential HTML Elements for Web Page Design**

- **`<HTML>`**: The root element that wraps all content on the page.
- **`<HEAD>`**: Contains meta-information about the document, like the title and links to stylesheets.
- **`<TITLE>`**: Sets the title of the webpage, displayed in the browser tab.
- **`<BODY>`**: Contains the visible content of the webpage. Attributes include:
  - **`BACKGROUND`**: Sets an image as the background.
  - **`BGCOLOR`**: Defines a background color.
  - **`TEXT`**: Sets the color of the text.
  - **`LINK`**: Specifies the color of hyperlinks.
  - **`ALINK`**: Specifies the color of active hyperlinks.
  - **`VLINK`**: Sets the color of visited hyperlinks.
  - **`LEFTMARGIN`** and **`TOPMARGIN`**: Set the left and top margins.

  ```html
  <body bgcolor="lightblue" text="black" link="blue" alink="red" vlink="purple">
  ```

#### **4. Text Formatting Elements**

- **`<FONT>`**: Changes the font type, size, and color of the text. 
  ```html
  <font color="red" size="4" face="Arial">This is a sample text.</font>
  ```
  
- **`<BASEFONT>`**: Sets a default font size, color, and face for the entire document.
  ```html
  <basefont color="blue" size="3" face="Verdana">
  ```

- **`<CENTER>`**: Centers the enclosed content.
  ```html
  <center>This text is centered.</center>
  ```

- **`<BR>`**: Inserts a line break.

- **`<HR>`**: Creates a horizontal line. Attributes include `SIZE`, `WIDTH`, `ALIGN`, `NOSHADE`, and `COLOR`.
  ```html
  <hr size="3" width="50%" align="left" noshade color="grey">
  ```

- **Comments**: Used to add notes within the HTML code that are not displayed on the webpage.
  ```html
  <!-- This is a comment -->
  ```

#### **5. Heading and Paragraph Elements**

- **Headings (`<H1>` to `<H6>`)**: Define headings on the webpage. `<H1>` is the largest, and `<H6>` is the smallest.
  ```html
  <h1>Main Heading</h1>
  <h3>Subheading</h3>
  ```

- **`<P>`**: Creates paragraphs of text.
  ```html
  <p>This is a paragraph.</p>
  ```

- **Text Formatting Tags**:
  - **`<B>`**: Makes text bold.
  - **`<I>`**: Italicizes text.
  - **`<U>`**: Underlines text.
  ```html
  <b>Bold Text</b> <i>Italic Text</i> <u>Underlined Text</u>
  ```

#### **6. Lists in HTML**

- **Unordered List (`<UL>`)**: Creates a bulleted list. Attributes include `TYPE` to define the bullet style.
  ```html
  <ul type="square">
    <li>Item 1</li>
    <li>Item 2</li>
  </ul>
  ```

- **Ordered List (`<OL>`)**: Creates a numbered list. Attributes include `TYPE` (number, letter, Roman numeral) and `START` (starting number).
  ```html
  <ol type="A" start="3">
    <li>Item 1</li>
    <li>Item 2</li>
  </ol>
  ```

#### **7. Inserting Images**

- **`<IMG>`**: Embeds images into the webpage. Key attributes:
  - **`SRC`**: Specifies the path to the image file.
  - **`WIDTH`** and **`HEIGHT`**: Set the dimensions of the image.
  - **`ALT`**: Provides alternative text if the image cannot be displayed.
  - **`ALIGN`**: Aligns the image to the text.
  ```html
  <img src="image.jpg" width="150" height="150" alt="Sample Image" align="center">
  ```

#### **8. Creating Links**

- **Internal Links**: Navigate within the same document using the `<A>` tag with `NAME` and `HREF` attributes.
  ```html
  <a name="section1"></a>
  <a href="#section1">Go to Section 1</a>
  ```

- **External Links**: Navigate to other webpages.
  ```html
  <a href="https://www.example.com" title="Example Site" alt="External Link">Visit Example</a>
  ```

#### **9. Inserting Tables**

Tables organize data in rows and columns. The main elements are:
- **`<TABLE>`**: Defines the table.
- **`<TR>`**: Table row.
- **`<TD>`**: Table data (cell).
- **`<TH>`**: Table header.
  ```html
  <table>
    <tr>
      <th>Header 1</th>
      <th>Header 2</th>
    </tr>
    <tr>
      <td>Data 1</td>
      <td>Data 2</td>
    </tr>
  </table>
  ```

---

### **Conclusion**

This guide provides an overview of basic HTML elements and attributes. By experimenting with these elements and creating different webpage layouts, you will gain a solid foundation in HTML and be well-prepared for the test. Remember, practice and experimentation are key to mastering HTML!