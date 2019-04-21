# Personal Notes (Training Guide)

## HTML Elements
---
### HTML5 origin
- HTML5 derives from HTML 4.01, not from XHTML

### Semantic Markup
- HTML5 stresses separating structure, presentation and behavior.  
- HTML tags provides a meaningful structure, but does not provide presentation.

### Casing
- Casing isn't important in HTML.  
- W3C recommends lowercase tag names as a standard (was the case for 4.01 and XHTML).

### Elements
- a: Hyperlink
- abbr: Abbreviation
- address: Contact information
- area: Image map region
- article: Independent section
- aside: Auxiliary section
- audio: Audio stream
- b: Bold text
- base: Document base URI
- bb: Browser button
- bdo: Bi-directional text override
- blockquote: Long quotation
- body: Main content
- br: Line break
- button: Push button control
- canvas: Bitmap canvas
- caption: Table caption
- cite: Citation
- code: Code fragment
- col: Table column
- colgroup: Table column group
- command: Command that a user can invoke
- datagrid: Interactive tree, list, or tabular data
- datalist: Predefined control values
- dd: Definition description
- del: Deletion
- details: Additional information
- dfn: Defining instance of a term
- dialog: Conversation
- div: Generic division
- dl: Description list
- dt: Description term
- em: Stress emphasis
- embed: Embedded application
- fieldset: Form control group
- figure: A figure with a caption
- footer: Section footer
- form: Form
- h1: Heading level 1
- h2: Heading level 2
- h3: Heading level 3
- h4: Heading level 4
- h5: Heading level 5
- h6: Heading level 6
- head: Document head
- header: Section header
- hr: Separator
- html: Document root
- i: Italic text
- iframe: Inline frame
- img: Image
- input: Form control
- ins: Insertion
- kbd: User input
- label: Form control label
- legend: Explanatory title or caption
- li: List item
- link: Link to resources
- map: Client-side image map
- mark: Marked or highlighted text
- menu: Command menu
- meta: Metadata
- meter: Scalar measurement
- nav: Navigation
- noscript: Alternative content for no script support
- object: Generic embedded resource
- ol: Ordered list
- optgroup: Option group
- option: Selection choice
- output: Output control
- p: Paragraph
- param: Plug-in parameter
- pre: Preformatted text
- progress: Progress of a task
- q: Inline quotation
- rp: Ruby parenthesis
- rt: Ruby text
- ruby: Ruby annotation
- samp: Sample output
- script: Linked or embedded script
- section: Document section
- select: Selection control
- small: Small print
- source: Media resource
- span: Generic inline container
- strong: Strong importance
- style: Embedded style sheet
- sub: Subscript
- sup: Superscript
- table: Table
- tbody: Table body
- td: Table cell
- textarea: Multiline text control
- tfoot: Table footer
- th: Table header cell
- thead: Table head
- time: Date and/or time
- title: Document title
- tr: Table row
- ul: Unordered list
- var: Variable
- video: Video or movie
- wbr: Optionally break up a large word at this element

### Attributes
- Attributes must be surrounded by '' or ""
- Boolean attributes can be used in 3 different ways
  - attribute
  - attribute=''
  - attribute='attribute'
- Global attributes can be applied to all element
  - accesskey: shortcut key, but may cause problem with recent browser...
  - class: Specifies one or many css class
  - contenteditable: Specifies that the content within the tag can be edited
  - contextmenu:  no browser supports this attribute. 
  - dir: left-to-right or right-to-left text direction
  - draggable: Specifies whether an element is draggable.
  - dropzone: Specifies the behavior of the dragged data when it’s
dropped.
  - hidden: Specifies that an element is not relevant
  - id: Specifies an element unique id
  - lang: Specifies the language of the element's content
  - spellcheck: Indicates whether element is to have spelling and grammar checked...
  - style: Specifies inline css style
  - tabindex: Sets the tabbing order of the element
  - title: Provides extra information aoutthe element.
- Data attributes (expando)
  - Browser are designed in a way that the ignore any element or attribute they don't know.
  - By convention custom element attributes should start with data- prefix.

### Container elements vs Void elements
- Elements that can't contain any elements are self closing or void element (ex: `<br />`)
  - area, base, br, col, command, hr, img, input, link, keygen, meta, param, source and wbr
- Elements that can contain other elements requires a closing tag and are known as container element (ex: `<div></div>`)
- Lookout there is some exceptions
  - script can't contain any elements but requires a closing tag.

### Comments
- Comments must start with `<!--`  an no spaces is allowed
- Comments ends with a `-->`; but spaces is allowed between the `--` and `>` sign.
  - This means it is impossible to use any -- within comments...

### Conditional comments
- IE supports conditional comments
  - `<!--[if lte IE 7]> <html class="no-js ie6" lang="en"> <![endif]-->`

### HTML document structure
- Document should always start with &lt;!DOCTYPE html>
- head contains the meta data for the page
- body encapsulates the content

### Nonbreaking space
- `&nbsp;` designate a non breaking space.
  - Browser will remove any contiguous white spaces used nonbreaking space if contiguous spaces are important.
  - Use in case where you want to make sure that browser doen't wrap at a given space position 
    - To prevent browser to wrap betweent he number and its related unit (ex: 10 km)


---

## Embedding content (iframe)

### iframe
The iframe element creates a nested browser context into which another HTML
document can be loaded. Loading an HTML document creates a browsing context for that document. The document that contains an iframe is contained within the parent browser context, where the document that is loaded into the iframe element is within the nested browser context

### Context navigation
- window.top: A WindowProxy object representing the top-level browsing context
- window.parent: A WindowProxy object representing the parent browsing context
- window.frameElement: An element that represents the browsing context container but returns null if there isn’t one

### Attributes
- name: The name of the iframe for references (browsing context name)
- src: the address of the document to be loaded

### Sandboxing
Allow definition of security layer to apply to document loaded within the iframe.
- Allow-forms: Enables form
- allow-same-origin: Allows the content to be treated as being from the same origin instead of forcing it into a unique origin
- allow-scripts: Enables scripts except pop-ups
- allow-top-navigation: Allows the content to navigate its top-level browsing context
- ex: `<iframe sandbox="allow-same-origin allow-forms allow-scripts"
src="http://otherContent.com/content.html"></iframe>`

---

## Hyperlink

### States
- Unvisited link: Underlined and blue
- Visited link: Underlined and purple
-  Active link: Underlined and red

### References
- Can either references external link through relative or absolute url (src="url.html")
- Can also reference a section of the document (src="#section")

### Target
- _blank: Open in a new browser window
- _parent: Open in the parent frame or window
- _self: Open in the current window or frame (default)
- _top: Open in the topmost frame, thus replacing the contents of the window
- iframe name: Open in the iframe element

### Email
- The mailto URL accepts the following parameters: subject, cc, bcc, and body.
- The parameters can be entered in any order by adding a question mark (?) after the email address and separating the parameters with the ampersand (&).

---

## Images

### Formats
- JPEG
  - best for photograph because of its high compression
  - compression is lossy (lose detail everytime you save)
- GIF
  - Great for small images
  - supports animation
  - supports transparency
  - lossless compression
- PNG
  - Multi purpose
  - supports variable transparency
  - lossless compression
  - larger in size that jpeg.
- SVG
  - Great for drawing
  - Scalable

### Image maps
Creates clickable image map
- The map element has a name attribute that must be set. On an img element, set the usemap attribute to the map element’s name to create a relationship between the image and the map.
- Coordinates
  - rect: x1, y1, x2, and y2 specify the coordinates of the left, top, right, and bottom.
  - circle: x, y, and radius specify the coordinates of the center and the radius.
  - poly: x1, y1, x2, y2,.., xn, and yn specify the coordinates of the edges. The first and last coordinate pairs should be the same to close the polygon, but if they aren’t the same, the browser will add a closing pair.

```html
<img src ="worldmap.gif" 
     width="145" 
     height="126"
     alt="World Map" 
     usemap ="#countries" />
<map name="countries">
  <area shape="rect" 
        coords="10,15,30,25"
        href="USA.html" alt="USA" />
  <area shape="circle" 
        coords="95,40,20"
        href="China.html" 
        alt="China" />
  <area shape="poly" 
        coords="97,76,115,76,113,83,105,90,97,76"
        href="Australia.html" 
        alt="Australia" />
  <area shape="default" 
        href="InvalidChoice.html" 
        alt="Invalid" />
</map>
```

---

## Plugin content
### Embed
Easier to use than object tag but servesthe same purpose...
- height: Specifies the height in pixels of the embedded content
- src: Specifies the URL of the external file to embed
- type: Specifies the MIME type of the embedded content
- width: Specifies the width in pixels of the embedded content

### Object
The `<object>` tag embeds an object within an HTML document. You can embed multimedia such as audio, video, Java applets, ActiveX, PDF, and Flash in your webpages.
- data: Supplies the URL of the resource to be used by the object
- form: Indicates one or more form ids to which the object belongs
- height: Specifies the height in pixels of the object
- name: Defines the name of the object
- type: Defines the MIME type of data specified in the data attribute
- usemap: Indicates the name of a client-side image map to be used with the object
- width: Specifies the width in pixels of the object
- Se cna use param elements to pass data to the object...