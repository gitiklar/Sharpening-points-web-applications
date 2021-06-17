# 1 - 5

נראה את זה בדוגמא מדפדפן כרום אצלי על המחשב ומגלישה לאתר גוגל. הפעם אלחץ על כפתור העכבר הימני על המסך, אבחר Inspect Element וייפתח לי בדפדפן חלון חדש עם כלי פיתוח ואיתור שגיאות. אנחנו נדבר עוד הרבה על הכלי הזה במהלך הקורס, אבל בינתיים בואו ניכנס כבר לטאב שנקרא Network.

בטאב Network הדפדפן מציג רשימת הודעות - אלה ההודעות שהדפדפן שלי שלח לשרת והתשובות שקיבל. נלחץ על ההודעה הראשונה ונוכל לראות שההודעה כוללת כל מיני פרמטרים שמספרים עליי, והתשובה נראית כמו טקסט בשפת תכנות שממש קשה לקרוא או להבין מה הוא אומר. אנחנו אולי לא יכולים לקרוא את זה אבל לשמחתנו הדפדפן שלנו יכול. הרצת הקוד שהדפדפן קיבל מהשרת גורמת להצגת דף הבית של גוגל שאתם רואים בחלון הראשי

Inspect Element-> Network

https://neocities.org/ - שמירת פרויקטים </br>

HTML
-
```JS
<meta> and <link> without close tag /
<link> for style
<header> the header file
<ul> unorder list
<ol> order list
<a href=""> link to other webSite
```
CSS
-
```JS
background: url("");
background-position-x: 100px;
ul {
     column-count:2;
     max-width:30vw; vw = % from all screen
}
```
JavaScript
-
```JS
function step() {
    pos-=2;
    header.style.backgroundPositionX = `${pos}px`;
    requestAnimationFrame(step);
}

step();
```

# 6 - 11

------------------------------------להצגה של תוכן HTML תגיות ------------------------------- 

```html
<!DOCTYPE html> -- של דף זה HTML מהי גרסת ה--
<html>
    <head>
        <title></title> --
         --.בתוך תגית זו רשומה כותרת העמוד --
         --.הכותרת היא שתופיע בתוצאות החיפוש בגוגל וגם בדפדפן בתוך הטקסט של הטאב--
         <meta charset="utf8">
    </head>
    <body>
        ----------  ה-6 התגיות הראשונות שנרצה להכיר נקראות תגיות הכותרת . הן נראות כך -----------
        <h1>Header 1</h1>
        <h2>Header 2</h2>
        <h3>Header 3</h3>
        <h4>Header 4</h4>
        <h5>Header 5</h5>
        <h6>Header 6</h6>
        -- מייצרת פסקת טקסט כאשר פסקה יכולה להכיל גם בלוק של טקסט וגם את התמונות שלידו p התגית --
        <p>This is the paragraph</p>
        -- img התגית --
        <img src="https://miro.medium.com/max/3052/1*C23nUxZgvrvkKsr9sM5rTw.jpeg" alt="HTML5 tricks" width="400" />
        -- a תגית עוגן --
        <a href="http://www.google.com">Go To Google</a> -- קישור לאתר חיצוני --
        <a href="#footer"> -- עוגן בתוך העמוד  --
        <a name="footer">Footer</a> 
        במידה וקיים בעמוד עוגן כזה
        אפשר להוסיף # לשורת הכתובת וכך לגרום לדפדפן לגלול עד שהעוגן יוצג על המסך
        index.html לדוגמא אם לקובץ קוראים
        תוכלו לכתוב בשורת הכתובת בדפדפן:
        index.html#footer
        
        -- תגיות רשימה--
        <ul> -- unorder list ---- ol - order list --
        <li>Milk</li>
        <li>Cheese
            <ul>
                <i>Blue cheese</li>
                <li>Feta</li>
            </ul>
        </li>
        </ul>
    </body>
</html>
--------------------------------לשליטה על מבנה העמוד HTML תגיות ------------------------------------
ההבדל בין בלוק לאינליין

:block תגיות
h1-6 , p , ul , ol , li , div ,time, form

:inline תגיות
a , b , em , i, label, input


:inline-block תגיות 
img , 

   -- HTML- תגיות סמנטיות ב ---
 
.מגדירה שחלק מסוים בעמוד הוא כותרת header התגית

.מגדירה את החלק העיקרי שבעמוד main התגית

.מגדירה אזור שבתוכו יש תפריט או לינקים לדפים אחרים nav התגית

.מגדירה אוסף של פריטים section התגית

.מגדירה אזור שהוא מאמר או פריט תוכן מסוים article התגית

.מגדירה אזור בעמוד שהוא תיבת צד או משהו פחות חשוב aside התגית

מגדירה את האזור התחתון של העמוד footer התגית

---------------------------------------- HTML- טפסים ב -----------------------------------

<form action="/contactus.php" method="post" > 
-- action= כתובת הדף של השרת שאליו ישלח הטופס --
-- method - מגדיר את אופן הבקשה --
-- סוגי הקלט שנכתבים בדר"כ בתוך התוית הם --
    <label>
        Name:
        <input type="text" name="name"/> 
        -- מאפיין השם קובע מה המידע של השדה 
        כדי שיוכלו לקרא אותו מהשרת או מהגאווה סקריפט --
    </label>
    <label>
        choose color:
        <input type="color" name="color"/> 
    </label>
     <label>
        choose:
        <input type="checkbox" name="checkbox"/> 
    </label>
     <label>
        choose date:
        <input type="date" name="date"/> 
    </label>
    <label>
        choose time:
        <input type="time" name="time"/> 
    </label>
     <label>
        Password:
        <input type="password" name="password"/> 
    </label>
      <label>
        Phone number:
        <input type="tel" name="telephone"/> 
    </label>
    --textarea  - בשונה מהקלט שהוא שורה אחת, תגית זו מייצגת מספר שורות טקטסט --
    <label>
        Message:
        <textarea name="user_message"></ textarea>
    </label>
    -- כך מייצרים רשימת שדות לבחירה על ידי תיבת גלילה נפתחת --
    <label>
        Category
        <select name="category">
            <option value="sales">Sales</option>
            <option value="support">Support</option>
            <option value="other">Other</option>
        </select>
    </label>
    <button type="submit">Send</button>
    <input type="submit" value="Send"/>
</form>
```

# 12 - 28

```JS
 -----------------    SASS/SCSS    ----------------
בו משתמשים CSS-דומה יותר ל SCSS-שניהם שווים רק בסינטקס אחר וכיון ש

CSS - אין אפשרות להריץ אותו ככה הוא חייב להיות מתורגם ל
"http://koala-app.com/" :הכלי שמתרגם הוא
SCSS צריך להוריד ולהתקין ואז להוסיף בפלוס את התיקיה של הפרויקט והוא יודע למצא את הקובץ 
CSS - הוא מתרגם אותו אוטומטית ל

:ואז הוא פותח את הקובץ שאותו מקנפגים Edit Settings <- Project Settings <- אחרי שמעלים את התיקיה - לחצן ימני על התיקיה 
"mappings": [
		 {	
		 	"src": "client/scss",
		 	"dest": "client/css"
		 }
],

שעליו עובדים SCSS -ולשני קובץ CSS - עושים 2 תיקיות לאחד מכניסים קובץ




----------------- HTML בדף CSS שילוב תוכן  -----------------

1.) Link to a CSS file in our project
        <link rel="stylesheet" href="style.css" />

2.) Link to a CSS file on the web
        <link rel="stylesheet" href="https://unpkg.com/sakura.css@1.0.0/css/sakura.css" />

3.) Add style inline head in HTML
        <style>
            h1 { color: darkcyan; }
        </style>

4.) Add style inline in specific tags
        < h1 style="border-bottom: 2px solid blue">We ♥ CSS< /h1>
```
-----------------------  סלקטורים  -------------------------
```CSS
1.) Element Selector 
    body, h1, h2

2.) ID Selector 
    #left-section

3.) Class Selector 
    .blue, .with-border, .btn, .large-btn

4.) Descendant Selector 
    #left-section li 
    footer a

5.) State Selector 
    :hover
    :focus
    footer a:hover

--- Zebra Tables ---

1.) HTML Tables

2.) first-child selector

3.) nth-child selector

4.) even / odd lines

5.) last-child selector

---------------------------- סיכום תרגול סלקטורים --------------------------------------

plate.small - ללא רווח הכוונה שלו עצמו יש את הקלאס

plate * - כל הילדים של הצלחת

plate + apple - תפוח שבא מיד אחרי צלחת

bento ~ pickle - כמו הקודם רק שאם יש רצף מביא את כל הרצף

plate *:only-child - תופס את כל אלו בתוך צלחת שהם ילד יחיד של הצלחת

apple:first-of-type - התפוח הראשון שקיים בעמוד

plate:nth-of-type(2n) - הצלחות הזוגיות

plate apple:only-of-type - תפוח שהוא היחיד בתוך הצלחת

orange:last-of-type,apple:last-of-type -תפוז ותפוח שהם האחרונים כל אחד מסוגו 

bento:empty - ללא ילדים

apple:not(.small) - תפוח לא קטן

[for^="S"] = שמתחיל ב

[for$="to"] - שמסתיים ב

[for*="S"] - שמכיל את האות


------------------------- ספסיפיסיטי ---------------------------------

1.) id
2.) class or attribute
3.) element
4.) the long rule is the first

------------------------- בסיסיים CSS מאפיייני ---------------------------
color: #2D3D48;
background-color: #D1D4D1;

font-weight: 900;
font-size: 100px;
font-family: 'Rubik', sans-serif;

box-shadow: -32px 32px 27px -2px rgba(0,0,0,0.43);

line-height: 3;
border-collapse: collapse;
filter: grayscale(1);
filter: none;
column-count: 3;
list-style: none;
padding-left: 50px;

background-image: url(https://cache.desktopnexus.com/thumbseg/2259/2259026-bigthumbnail.jpg);
background-size: 50px auto;
background-position:0 0;
background-repeat: no-repeat;
   
display: inline-block;
vertical-align: middle/top/buttom;

-----------------------------------  em rem  ----------------------------------------
If .inner div has a size in em, then my size will be relative to .outer font size
If .inner div has a size in rem, then my size will still be relative to html's font size

html { font-size: 15px; }

.em h1 { font-size: 2.35em; }
.em h2 { font-size: 2.00em; }
.em p { font-size: 1em; }

.rem h1 { font-size: 2.35rem; }
.rem h2 { font-size: 2.00rem; }
.rem p { font-size: 1rem; }

/** Rem vs. Em confusing bit */

.em .inner { font-size: 1.5em; }
.em .outer { font-size: 2em; }

.rem .inner { font-size: 1.5rem; }
.rem .outer { font-size: 3rem; }

-----------------------------  מודל הקופסא  -------------------------------

-- Content Size --
% - אחוז מרוחב האלמנט שמעלי
height: 30vh; - אחוז מרוחב כל העמוד
width: 30vw; - אחוז מגובה כל העמוד
max-width: 300px; - בכל מקרה לא יהיה הגודל מעבר ל-300 


-- Padding --
 padding: 10px 5px 5px 10px;
 padding: 10px (top/bottom) 5px (left/right)
 padding: 8px (all 4 sides)

 -- Border --
border: 5px dashed pink;


-- Margin --
margin-top: 50px;
margin: top right bottom left
margin: top/bottom right/left
margin: 5px (all four sides)


width: calc(50% - 20px);
box-sizing: border-box;



טריק נחמד עם שוליים הוא שימוש במילה 
auto
:בשני הצדדים כדי לשים אלמנט מסוים שיש לו רוחב קבוע במרכז המסך

p:first-child {
    height: 30vh;
    width: 50vw;
    max-width: 300px;
    margin-left: auto;
    margin-right: auto;
}

-------------  Media Queries שינוי הגדרות עיצוב לפי גודל המסך באמצעות -------------

@media only screen and (min-width: 600px) {
}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {
}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
}

@media (min-width: 700px) {
    body {
        background: pink;
    }
}

@media (max-width: 700px) {
    body {
        background: pink;
    }
}

@media only screen and (min-width: 600px) {

}

@media (orientation:portrait) {עומד}
@media (orientation:landscape) {שוכב}

---------------------------        flex       -------------------------------
justify-content:
- flex-start: Items align to the left side of the container.
- flex-end: Items align to the right side of the container.
- center: Items align at the center of the container.
- space-between: Items display with equal spacing between them.
- space-around: Items display with equal spacing around them.

align-items:
- flex-start: Items align to the top of the container.
- flex-end: Items align to the bottom of the container.
- center: Items align at the vertical center of the container.
- baseline: Items display at the baseline of the container.
- stretch: Items are stretched to fit the container.

flex-direction:
- row: Items are placed the same as the text direction.
- row-reverse: Items are placed opposite to the text direction.
- column: Items are placed top to bottom.
- column-reverse: Items are placed bottom to top.

order:
- positive or negative integer value (-2, -1, 0, 1, 2).

align-self: 
- the same values as align-items and overriding the align-items value.


Oh no! The frogs are all squeezed onto a single row of lilypads.
flex-wrap:
- nowrap: Every item is fit to a single line.
- wrap: Items wrap around to additional lines.
- wrap-reverse: Items wrap around to additional lines in reverse.


The two properties flex-direction and flex-wrap are used so often together that the shorthand property flex-flow:
- flex-flow: flex-direction  flex-wrap
- flex-flow: row wrap


align-content: 
- flex-start: Lines are packed at the top of the container.
- flex-end: Lines are packed at the bottom of the container.
- center: Lines are packed at the vertical center of the container.
- space-between: Lines display with equal spacing between them.
- space-around: Lines display with equal spacing around them.
- stretch: Lines are stretched to fit the container.

This can be confusing, but ----align-content--- determines the spacing between lines, while   ---align-items---   determines how the items as a whole are aligned within the container. When there is only one line, align-content has no effect.

--------------  grid  ---------------
#garden {
  display: grid;
  grid-template-columns: 20% 20% 20% 20% 20%;
  grid-template-rows: 20% 20% 20% 20% 20%;
}

#water {
    grid-column-start:3
    grid-column-end:4
}

grid-template-columns:
- grid-template-columns: 20% 20% 20% 20% 20%;
- grid-template-columns:repeat(8,1fr);
- grid-template-columns:repeat(5,100px 3em 40%);
- grid-template-columns:1fr 5fr;
- grid-template-columns:50px 1fr 1fr 1fr 50px;
- grid-template-columns:75px 3fr 2fr;

grid-template-rows:
- grid-template-rows: 20% 20% 20% 20% 20%;
- grid-template-rows: repeat(4,12.5px) calc(100% - 50px)

grid-template: 
- grid-template: grid-template-rows/grid-template-columns.
- grid-template:60% 40%/ 200px calc(100% - 200px)

grid-column-start:
- grid-column-start:3

grid-column-end:
- grid-column-end: 4
- grid-column-end: span 2

grid-row-start:
- grid-row-start:3

grid-row-end:
- grid-row-end: 4 
- grid-row-end: span 2

grid-column:
- grid-column:4/6
- grid-column: 4/span 2

grid-row:
- grid-row:4/6
- grid-row: 4/span 2

grid-area:
- grid-area:1/2/4/6 (x,y) (x,y)
- grid-area: grid-row-start/grid-column-start/grid-row-end/grid-column-end.

order:
- positive or negative integer value (-2, -1, 0, 1, 2).

 display: grid;
    grid-template-areas: "h1  h1  h1"
                         "h2  h2  h2" 
                         "nav nav nav"
                         "txt txt txt"
                         "bq  bq  bq";
    grid-area: h1;


-----------------------------------  Overflow  ---------------------------------
clip-path: polygon(50% 0%, 83% 12%, 100% 43%, 94% 78%, 68% 100%, 32% 100%, 6% 78%, 0% 43%, 17% 12%);

&lt - <
&-gt - >

overflow:hidden;
overflow:auto;
overflow:scroll;

-----------------------------------  Position  ---------------------------------
position: relative; - עוגן , כל דבר בתוכו נוכל לשלוט במיקום שלו
position: absolute; - לילדים שלו
top , buttom , right , left - מיקום לילדים

<label>
    <span class="label-text">Name< /span>
    <input placeholder="Name..." type="text" />
</label>

label {
  position: relative;
}

.label-text {
  position: absolute;
}
```

# 29 - 37 

```JS
----------- שלנו HTML בדף JavaScript איך לשלב קוד ---------

1.)<body>
       <script src="demo.js"></script> 
    </body> 
2.) <body> 
        <script> 
            console.log('Running from an inline script tag'); 
        </script> 
    </body> 

3.) <button onclick="alert('Ouch!')"> Click Me </button>

-----------  JavaScript Basic Syntax  ------------------

alert("Hello World!");
1. Comments
    /* */  //

2. Variables
    var, let, const

3. Conditions
    if(2==="2") { ... }
    ==, ===

4. For loops
    for(let i=0; i < 10; i++) { ... }
    
5. While loops
    while( ... ) { ... }

6. Functions
    function foo() { ... }

'hello'.length;       //5 
'hello'.endsWith('o');//true 
'hello'.indexOf('e'); //1 
console.log('JavaScript'.toUpperCase()); 

---------------- JavaScript Debugging  --------------------

1. Debugger Page

2. Breakpoint

3. Conditional Breakpoint

4. Change code on disk

-----------------  Strict Mode  מצב בטוח ------------------ 
 .JavaScript מצב בטוח מבקש מהדפדפן לחפש יותר שגיאות בתוכניות
.מצב זה לא מופעל אוטומטית כדי שקוד ישן יוכל לעבוד

1. Enabling strict mode
    -"use strict";

2. Assignment to global variables

3. Assignemnt to reserved words

4. Octal values

--------------------- JavaScript מערכים ב -----------------

1. Defining Arrays 
const colors = ['red', 'blue', 'white']; 
const arr = [10,20,'three',[10,20,30],null]; 

2. Access arrays items and length 
console.log(arr[0]); 
arr[0] = 99; 
console.log(arr); 

3. Array Methods 
arr.push(40); 
arr.unshift(0); 
arr.pop(); 
arr.shift(); 
arr.splice(1,2); 

4. Arrays and Loops 
for(let clr of colors) { 
    console.log(clr); 
} 

for(let i =0; i < colors.length ; i++) { 
    const clr = colors[i]; 
    console.log(`Colors[${i}] === ${clr}`); 
} 

5. Array and const 
let numbers = [10, 12, 17, 5, 9]; 

function sum(x, y) {
  return x + y;
}

function square(x) {
  return x * x;
}

function printSingleItem(val, index) {
  console.log(`Index = ${index}; Value = ${val}`);
}

const total = numbers.reduce(sum);
console.log('sum of all items = ' + total);

const squares = numbers.map(square);
console.log('squares = ', squares);

const sumSquares = numbers.map(square).reduce(sum);
console.log('sum of squares = ' + sumSquares);

numbers.forEach(printSingleItem);

--------------------- JavaScript אובייקטים ב ----------------- 
// Dictionary / Hash

1. Defining Objects

const email = {
  bob: 'bob@gmail.com',
  jane: 'jane@walla.co.il',
  bill: 'crazypen@yahoo.com'
};

const details = {
  name: 'Peter Parker',
  alias: 'Spider-Man',
  appeared_in: 1962,
  friends: ['Superman', 'Batman']
};

2. Accessing Object Items and added new item in object
// print out bob's email
console.log(email['bob']);

// same as:
console.log(email.bob);

// change an email address
email.jane = 'jane@yahoo.com';

// add a new email
email.barbara = 'barbara@gmail.com';

let name = 'bob';
email[name] = `${name}@gmail.com`;

3. Delete Keys
delete email.jane;

4. Objects and Loops
for (let key of Object.keys(email)) {
    const val = email[key];
    console.log(`${key} has email: ${val}`);
}
```

# 38 - 45

# JavaScript and the DOM
```JS
1. What is the DOM
  Document Object Model

2. Reading data from DOM
  - document.querySelector
  - element.querySelector
  - document.querySelectorAll
  
3. Writing to the DOM
  - element.textContent = '...'
  - element.innerHTML = '...'
  
4. Style


document.body

document.getElementById

document.querySelector

document.querySelectorAll

element.querySelector

element.querySelectorAll

document.body.clientWidth

divElement.classList

li.classList.add('max');

document.body.style.backgroundColor = 'lightyellow';

.tagName (DIV, BODY, A) מחזיר את שם התג של האלמנט הנוכחי 
.id - מחזיר את המזהה הייחודי של האלמנט 
.value - textarea או input מחזיר את הטקסט שכרגע כתוב כתוכן תיבת טקסט מסוג 
.textContent - מחזיר את הטקסט שכרגע כתוב כתוכן אלמנט מסוים 
.innerHTML - מחזיר את כל תוכן תת העץ הפנימי של אלמנט בתור מחרוזת 

-----------------DOM Tree Navigation------------------

All nodes include the text between the elements (left side list)

1. Navigating a tree
  - childNodes / children
  - firstChild / firstElementChild
  - lastChild / lastElementChild
  - parentNode / parentElement
  - nextSibling / nextElementSibling
  - previousSibling / previousElementSibling

2. Creating new elements
  - document.createElement
  - document.createDocumentFragment
  - element.appendChild
  
  -------------------- JavaScript Events -----------------------------

1. What's an Event
    - mouse move
    - scroll
    - click
    - write text in an input field
    - submit a form

2. Handling Click Events
    - When user does X -> Please do Y
    
3. Events and Anonymous Functions

4. Input events and event info object

----------------------- Event Delegation ---------------------------------

1. Problem with specific event handlers

2. Example: A button that adds an input field

3. Solution: Event Delegation

inp.value = event.target.value;

------------------------ Timers and Intervals -----------------------------

1. Who needs timers

2. Using Timers
  - setTimeout, clearTimeout

3. IIFE - Immediately Invoked Function Expressions

4. Using intervals
  - setInterval, clearInterval

timerId = setTimeout(tick,1000);
clearTimeout(timerId);

timerId = setInterval(tick,1000);
clearInterval(timerId);

(function() {
const startIntervalDemo = document.querySelector('#start-interval-demo');
const cancelIntervalDemo = document.querySelector('#cancel-interval-demo');
const result2 = document.querySelector('#result2');

cancelIntervalDemo.addEventListener('click', cancel);
startIntervalDemo.addEventListener('click', start);

const text = ['wait for it...','Hi!' , 'bye!', ''];
let index = 0;
let timerId;

function start() {
    cancel();
    timerId = setInterval(tick,1000);
}

function tick() {
    result2.textContent = text[index];
    index = (index+1) % text.length;
}


function cancel() {
    clearInterval(timerId);
    result2.textContent = '';
    index = 0;
}

}());


-------------- JavaScript and CSS Animations ---------------

1. Image Slider
    transition: all 0.2s;


2. Animate.css
  < link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.7.2/animate.min.css" />   
    box.classList.add('animated','bounce');

3. Velocity.JS
<script src="https://cdnjs.cloudflare.com/ajax/libs/velocity/2.0.5/velocity.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/velocity/2.0.5/velocity.ui.min.js"></script>
    Velocity(box,'jello', {duration:1500});
    Velocity(box, {left:x, top:y}, {duration:1500});

```

# 46 - 55

```JS
-------------------------------------------   Functions  ----------------------------------------------- 
// Function Declaration
function twice(x) {
    return x * 2;
}

// Function Expression
const thrice = function(x) { return x * 3; };

// Arrow Function Expression
const fourTimes = (x) => x * 4;

// Save a function in a variable
const anotherNameForTwice = twice;

console.log(twice(10));
console.log(thrice(10));
console.log(fourTimes(10));
console.log(anotherNameForTwice(10));

// Take function as argument
function applyTwice(f, arg) {
    return f(f(arg));
}

// What do we get here?
console.log(applyTwice(twice, 10));


------------------------------------ Function in array -----------------------------------------
// Define an array
const nthice = [];
for (let i=0; i < 10; i++) {
    // Fill the array with "functions"
    nthice[i] = (x) => x * i;
}

// prints 6 - not a big surprise
console.log(nthice[2](3));


------------------------------------ Function in object -----------------------------------------
const p1 = {
    name: 'John',
    hello: function() {
        console.log('Hi!');
    },
}
p1.hello();

---- Same as:
const p1 = {
    name: 'John',
    hello() {
        console.log('Hi!');
    },
}

p1.hello();

---- Add `this`:

const p1 = {
    name: 'John',
    hello() {
        console.log(`Hi! ${this.name}`);
    },
}

p1.hello();

----------------------   Use a function as an Object ------------------

function square(x) {
    return x * x;
}

// prints 1 - function expects 1 argument
console.log(square.length);

// prints "square" - as this is the name of the function
console.log(square.name)

square.author = 'Ynon';
console.log(square.author);


------------------------  פיתוח קוד מונחה עצמים  -----------------------

---------- Object of game --------
const game = {
    secret: 0,
    numberOfTries: 10,

    startNewGame() {
        this.secret= Math.floor(Math.random() * 10);
        this.numberOfTries = 0;
    },

    play(guess) {
        if (this.numberOfTries >= 10) {
            // Sorry, game over
            return;
        }
        this.numberOfTries += 1;
        if (guess > this.secret) {
            return 1;
        } else if (guess < this.secret) {
            return -1;
        } else {
            return 0;
        }
    }
}

---------- Object of game inside a function and return game object--------

function Game () {
      const game = {
      secret: 0,
      numberOfTries: 10,

      startNewGame() {
          this.secret= Math.floor(Math.random() * 10);
          this.numberOfTries = 0;
      },

      play(guess) {
          if (this.numberOfTries >= 10) {
              // Sorry, game over
              return;
          }
          this.numberOfTries += 1;
          if (guess > this.secret) {
              return 1;
          } else if (guess < this.secret) {
              return -1;
          } else {
              return 0;
          }
      }
    }
  return game;
}

const game1 = Game();
const game2 = Game();
const game3 = Game();


----------------------------------- Class with prototype ----------------------------

function Person(name) {
    const person = {
        name: name,
        hello() {
            console.log(`Hi! ${this.name}`);
        },
    }
    return person;
}

const p1 = Person('one');
const p2 = Person('two');

p1.hello();
p2.hello();

>> p1.hello === p2.hello
false!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

To use a prototype you need:
1. Call the constructor function with a "new" -> new Game()
2. Inside the function, use "this" to refer to your new object
3. Create a .prototype field on the function
Game.prototype = {}
 
1.) Prototype
2.) New
3.) This

function Person(name) {
    this.name = name;
}

Person.prototype.hello = function() {
    console.log(`Hi! ${this.name}`);
}

const p1 = new Person('one');
const p2 = new Person('two');

>> p1.hello === p2.hello
true!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

>> p2.hello === Person.prototype.hello
true!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!


----------------------------------- Class with `class` ----------------------------
class Person {
    constructor(name) {
        this.name = name;
    }

    hello() {
        console.log(`Hi! ${this.name}`);
    }
}

const p1 = new Person('one');
const p2 = new Person('two');

>> typeof Person
"function"

>> Person.prototype.hello === p1.hello
true


--------------------------------------------  This ------------------------------------------
class Counter {
    constructor() {
        this.val = 0;
    }

    inc() {
        this.val++;
        console.log(this.val);
    }
}

const c = new Counter();
const btn = document.querySelector('button');
btn.addEventListener('click', c.inc);

// prints 1
c.inc();

// prints 2
c.inc();

But in button click -> NaN Why?

בקוד שלנו זה לא אנחנו שהפעלנו את הפונקציה אלא הדפדפן.
:אנחנו רק העברנו את הפונקציה לכפתור וביקשנו מהדפדפן לקרוא לה כשלוחצים על הכפתור 
btn.addEventListener('click', c.inc);

הדפדפן קיבל את הפונקציה אבל בלי האוביקט אליו היא היתה מחוברת
את האוביקט this ולכן כשהפונקציה מופעלת באופן אוטומטי בעקבות לחיצה על הכפתור היא לא מקבלת דרך המשתנה 

--------------------------- פתרון 1 --------------------------
class Counter {
    constructor() {
        this.val = 0;
    }

    inc() {
        this.val++;
        log.innerHTML = this.val;
    }
}

const c = new Counter();

const btn = document.querySelector('button');
btn.addEventListener('click', function() {
    c.inc();
});

--------------------------- bind -  פתרון 2 --------------------------
class Counter {
    constructor() {
        this.val = 0;
        this.inc = this.inc.bind(this);
    }

    inc() {
        this.val++;
        log.innerHTML = this.val;
    }
}
const c = new Counter();
const btn = document.querySelector('button');
btn.addEventListener('click', c.inc);

הקוד עובד אבל שימו לב להתפתחות מעניינת בעלילה
אם קודם כל האוביקטים חלקו את כל הפונקציות
עכשיו אנחנו יוצרים פונקציה חדשה בבנאי ולכן הפונקציה
:inc עצמה לא תהיה משותפת לכל האוביקטים של המחלקה

>> const x = new Counter();
>> const y = new Counter();
>> x.inc === y.inc;
false

--------------------------- פתרון 3 פונקצית חץ --------------------------

class Counter {
    constructor() {
        this.val = 0;
    }

    inc = () => {
        this.val++;
        log.innerHTML = this.val;
    }
}

const c = new Counter();
const btn = document.querySelector('button');
btn.addEventListener('click', c.inc);


--------------------------------------- Components ---------------------------------------------
קומפוננטה בעולם פיתוח ווב תהיה מחלקה שמטפלת באזור מסוים במסך, 
.ויכולה להיות בקשר עם קומפוננטות אחרות או עם מידע אחר של היישום.
הקומפוננטה אחראית על האזור שלה במסך
.של אזור זה ועדכונו HTML כולל הרבה פעמים בניה של ה

עליו היא צריכה לפעול  HTML קומפוננטה נכתבת בתור מחלקה שתקבל בבנאי אלמנט
 DOM הקומפוננטה תיצור את האלמנטים ב
 .תחבר אליהם קוד טיפול באירועים וכמובן תכתוב פלט לאותם אלמנטים
```

Example:
-```HTML
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF8" />
    </head>
    <body>
        <div id="c1"></div>
        <div id="c2"></div>
        <script src="counter.js"></script>
    </body>
</html>
```

```JS
class Counter {
    constructor(el) {
        this.val = 0;
        this.render(el);

        this.inc = this.inc.bind(this);
        this.incButton.addEventListener('click', this.inc);
    }

    render(el) {
        el.innerHTML = `
            <p>
                <button class="inc">Click Me</button>
                Clicks: <span class="log">${this.val}</span>
            </p>
        `;
        this.el = el;
        this.incButton = el.querySelector('.inc');
        this.log = el.querySelector('.log');
    }

    inc() {
        this.val++;
        this.log.textContent = this.val;
    }
}

const c1 = new Counter(document.querySelector('#c1'));
const c2 = new Counter(document.querySelector('#c2'));

const el = document.createElement('div');
document.body.appendChild(el);
const c3 = new Counter(el);


------------------------------------------- מנהל אירועים --------------------------------------------
this.unsubscribe = bus.subscribe('boom', this.handleBoomEvent.bind(this));

// then later in the code, to stop listening we'll just call unsubscribe
this.unsubscribe();

const even = [10, 12, 13, 15, 17, 20].filter(x => x % 2 === 0);
const notTen = [10, 12, 13, 15, 17, 20].filter(x => x !== 10);

class EventBus {
  constructor() {
    this.listeners = {};
  }

  subscribe(eventName, handler) {
    if (!this.listeners[eventName]) {
      this.listeners[eventName] = [];
    }

    this.listeners[eventName].push(handler);
    return () => {
      this.listeners[eventName] = this.listeners[eventName].filter(fn => fn !== handler);
    }
  }
}

 emit(eventName, ...args) {
    const listeners = this.listeners[eventName] || [];
    for (let fn of listeners) {
      fn(...args);
    }
  }

  bus.emit('boom', 10, 20);
  
const t = bus.subscribe('boom', function(x) { console.log('Boom!', x)});
const u = bus.subscribe('boom', function(x) { console.log('Boom!', x * x )});
bus.emit('boom', 10)
// Prints: Boom! 10 
// And then prints: Boom! 100

u()
bus.emit('boom', 10)
// Prints: Boom! 10


----------------------------  חיבור מנהל האירועים לקומפוננטות -------------------------

class EventBus {
  constructor() {
    this.listeners = {};
  }

  subscribe(eventName, handler) {
    if (!this.listeners[eventName]) {
      this.listeners[eventName] = [];
    }

    this.listeners[eventName].push(handler);
    return () => {
      this.listeners[eventName] = this.listeners[eventName].filter(fn => fn !== handler);
    }
  }

  emit(eventName, ...args) {
    const listeners = this.listeners[eventName] || [];
    for (let fn of listeners) {
      fn(...args);
    }
  }
}

class Display {
  constructor(el, bus) {
    this.setupUi(el);
    this.eventBus = bus;
    this.eventBus.subscribe('value', this.update.bind(this));
  }

  setupUi(el) {
    el.innerHTML = `
            <p>And the maximum value is: <span class="maxvalue"></span></p>
        `;
    this.panel = el.querySelector('.maxvalue');
  }

  update(val) {
    if (val > Number(this.panel.textContent)) {
      this.panel.textContent = val;
    }
  }
}

class Counter {
  constructor(el, bus) {
    this.val = 0;
    this.setupUi(el);
    this.eventBus = bus;
  }

  setupUi(el) {
    el.innerHTML = `
            <p>
              <button>Click To Inc</button>
              <span class="log"></span>
            </p>
        `;
    this.log = el.querySelector('.log');
    this.button = el.querySelector('button');
    this.button.addEventListener('click', this.inc.bind(this));
    this.updateUi();
  }

  inc = () => {
    this.val++;
    this.eventBus.emit('value', this.val);
    this.updateUi();
  }

  updateUi() {
    this.log.innerHTML = this.val;
  }
}

const bus = new EventBus();

const panelElement = document.createElement('div');
const panel = new Display(panelElement, bus);
document.body.appendChild(panelElement);

for (let i=0; i < 5; i++) {
  const el = document.createElement('div');
  const counter = new Counter(el, bus);
  document.body.appendChild(el);
}

```

# 56 - 63

------------------ Local Storage -----------------
```JS
localStorage.setItem('language', 'JavaScript');
localStorage.getItem('language')
localStorage.removeItem('language')
localStorage.hello = 'world';

const data = { one: 10, two: 'hello world', three: [10, 20, 30] };
JSON.stringify(data);
JSON.parse(dataAsText)
```

----------------- Audio / Video ------------------
```JS
<audio autoplay="true" controls="true" >
    < source src="mp3/birds.mp3" type="audio/mpeg" />
</audio>

const audioElement = new Audio('mp3/birds.mp3');
audioElement.play();
audioElement.pause();
audioElement.currentTime = 0;

---------------------- SVG -------------------------
 <svg width="400" height="400" viewBox="0 0 400 400">
    <circle cx="150" cy="150" r="50" />
</svg>

const svgns = "http://www.w3.org/2000/svg";
const circle = document.createElementNS(svgns, 'circle');
circle.setAttributeNS(null, 'cx', i * 30);
circle.setAttributeNS(null, 'cy', i * 30);
circle.setAttributeNS(null, 'r', 10);

const svgns = "http://www.w3.org/2000/svg";

const svg = document.querySelector('svg');

for (let i=0; i < 10; i++) {
    const circle = document.createElementNS(svgns, 'circle');
    circle.setAttributeNS(null, 'cx', i * 30);
    circle.setAttributeNS(null, 'cy', i * 30);
    circle.setAttributeNS(null, 'r', 10);
    svg.appendChild(circle);
}

//CSS:
circle { transition: all 0.5s; }
```


# 64 - 71

server.js :דוגמא פשוטה לקוד צד שרת הנמצא בתוך קובץ שנקרא
```JS
const express = require('express'); 
const bodyParser = require('body-parser')
const app = express();

app.use(bodyParser.json())

const users = [];

app.post('/users', function(req, res) {
    users.push(req.body);
    console.log(req.body);
    res.sendStatus(201);
});

app.get('/users', function(req, res) {
    res.send({ users: users });
});

app.listen(8080);


Node.JS - על מנת להפעיל את קוד צד השרת יש להתקין על המכונה את ה 
curl על מנת להפעיל את הקוד משורת הפקודה יש לוודא שמותקן גם  

(npm install :כותבים את הפקודה package.JSON - בתיקיה של השרת שבה יש את ה
node_modules שמביאה את הרשימה שיש שם מהאינטרנט ומכניסה אותה לתוך תיקיה שנקראת)

*** npm init -y
*** npm install --save express body-parser lodash socket.io

node server.js לאחר מכן באותה תיקיה מפעילים את קוד צד השרת באמצעות הפקודה 
GET/POST :וכעת השרת מופעל ואפשר לפנות אליו באמצעות אחד מהפעלים 

GET:
curl localost:8080/users     (due to this row in server: app.listen(8080))

POST:
curl -H "Content-Type: application/json" -d '{ "name" : "jim" }' localhost:8080/users



# Client / Server Ajax:
1.) const xhr = new XMLHttpRequest(); גישת האירועים
2.) await fetch(url,optionsObj); הבטחות

-----------------------------------------------------------------   גישת האירועים   -----------------------------------------------------------------------
1. XMLHttpRequest and events
  Verb (GET / POST) + Path (/users) + Request Body ({ name: 'jim', email: 'jim@gmail.com' })
  Request Headers (Content-Type: application/json)

2. CORS and File:// url restrictions
  - Running our code in a localhost:// server
  - npm install --global http-server
  - In the "client" folder run: 
    http-server -p 9090 -c-1

3. Demo Time - Server API

4. Demo Time - Client Code
  - Login
  - Get new messages
  - Send a message

 ------- example -------

 login(username) {
        const xhr = new XMLHttpRequest();
        xhr.open('POST', `${serverUrl}/login`);
        xhr.setRequestHeader('Content-Type', 'application/json');
        xhr.send(JSON.stringify({ username: username }));

        xhr.addEventListener('load', this.loginComplete.bind(this));
        xhr.addEventListener('error', this.error.bind(this));
  }

  loginComplete(evt) {
        const xhr = evt.target;
        if (xhr.status !== 200) { return this.error(evt) };

        const data = JSON.parse(xhr.responseText);
        this.token = data.token;
        console.log(`Got server token: ${this.token}`);
  }

-----------------------------------------------------------------   גישת ההבטחות עם פונקציות אסינכרוניות  -----------------------------------------------
# Async Communication with Fetch API

 ------- example -------

async login(username) {
        try {
            const response = await fetch(`${serverUrl}/login`,{
                method: 'POST',
                headers: {
                    'Content-Type':'application/json',
                },
                body: JSON.stringify({username}),
                mode: 'cors',
            });
            const data = await response.json();
            this.token = data.token;
            console.log(`Got token: ${this.token}`);
        } catch(err) {
            alert("Oops that didn't work "+err);
        }
    }
```

# JS ES6/7/8

```JS
----------------------------------------------------------------------
                              babel
ES6 לקוד ES5 קיים כלי אוטומטי שיודע לתרגם כל קוד 

https://babeljs.io/repl

----------------------------------------------------------------------
                        Webpack install
1.) all JS files save inside src folder near index.html 

2.)
npm init -y
npm i webpack --save-dev
npm i webpack-cli --save-dev
npm i babel-core babel-loader babel-preset-env --save-dev
npm install --save-dev @babel/core

create new file 'webpack.config.js' near index.html with->:
module.exports = {
  module: {
    rules: [
      {
        test: /\.js$/,
        exclude: /node_modules/,
        use: {
          loader: "babel-loader"
        }
      }
    ]
  }
};

npx webpack --mode development / production


----------------------------------------------------------------------
                        const , let and freeze

var מוכר בכל הפונקציה - לא משנה באיזה בלוק הוגדר
for (var i=0; i < 10; i++) {
    // do stuff
}
console.log(i);

const , let - מוכרים רק באותו הבלוק בהם הוגדרו

const - קבוע
:הדוגמא הבאה אינה חוקית
const name = 'ynon';
name = 10;

let - ניתן לשינוי
:ההדפסה השניה אינה חוקית
for (let i=0; i < 10; i++) {
  console.log(i);
}
console.log(i);

ERROR->:
let x = 10;
{
  console.log(x); //לא נתפס ReferenceError: אין אפשרות לגשת ל- 'x' לפני האתחול
  let x = 5;
  console.log(x);
}
console.log(x);



console.log print:  10, 5 , 10 ->:
let x = 10;
console.log(x);
{
  let x = 5;
  console.log(x);
}
console.log(x);

const a = Object.freeze([10, 20]);
a.push(30);// ERROR - because freeze

----------------------------------------------------------------------
                     arrow functions
const f = (x) => x * x;
// is the same as:
const ff = function(x) { return x * x; };

setTimeout(() => {
    console.log(this.name);
}, 500);
// is the same as:
setTimeout(function() {
    console.log(this.name);
}.bind(this), 500);

----------------------------------------------------------------------
                          class and extends

class AutoBind {
    constructor() {
        this.autoBindMethods();
      }
    
      getMethods() {
        const childClassPrototype = this.constructor.prototype;
        return Object.getOwnPropertyNames(childClassPrototype).filter(item => item !== 'constructor');
      }
    
      autoBindMethods() {
        this.getMethods().forEach(methodName => {
          this[methodName] = this[methodName].bind(this);
        });
      }
}

class Counter extends AutoBind {
    constructor(btn) {
      super();
      this.btn = btn;
      this.btn.textContent = '0';
      btn.addEventListener('click', this.inc);
    }
    
    inc() {
      this.btn.textContent++;
    }
  }
  
  const c = new Counter(document.querySelector('button'));

  --------------------------------------------------------------------
          GET , SET and functions create and return classes
  1.) Getters and Setters:

      class Timer {
        constructor() {
            this.seconds = 0;
        }

        set minutes(val) {
            this.seconds = val * 60;
        }

        set hours(val) {
            this.seconds = val * 3600;
        }

        get minutes() {
            return this.seconds / 60;
        }

        get hours() {
            return this.seconds / 3600;
        }
    }


  2.) Dinamic fields.

      class Timer {
          constructor() {
              this.seconds = 0;
          }
      }

      [['hours', 3600], ['minutes', 60]].forEach(function(prop) {
          const [propName, propFactor] = prop;
          Object.defineProperty(Timer.prototype, propName, {
              get() {
                  return this.seconds / propFactor;
              },
              set(val) {
                  this.seconds = val * propFactor;
              }
          }) 
      });



 3.)  functions creates classes 

      function makeTimerClass(factors) {
        const Timer = class {
            constructor() {
                this.seconds = 0;
            }
        };

        Timer.prototype.newFunction = function() {

        }

        factors.forEach(function(prop) {
            const [propName, propFactor] = prop;
            Object.defineProperty(Timer.prototype, propName, {
                get() {
                    return this.seconds / propFactor;
                },
                set(val) {
                    this.seconds = val * propFactor;
                }
            })    
        });   
        return Timer;
    }


    const Timer = makeTimerClass([['hours', 3600], ['minutes', 60]]);
    const SmallTimer = makeTimerClass([['ms', 1/1000]]);

    const t = new Timer();
    const st = new SmallTimer();

----------------------------------------------------------------------
1.) Default values instead of arguments.

    function printTimes(text , times = 5) {
        for(let i = 0 ; i< times ; i++) {
            console.log(text);
        }
    }
    printTimes('hello');
    printTimes('hello' , 3);


2.) ...  מכניס למערך איברים בודדים בתוך הפונקציה או מפרק מערך לאיברים בודדים בקריאה לפונקציה
function longetThan(minLength , ...words) {
    return words.filter(w=>w.length>minLength);
}

longetThan(4 , 'aaaaa', 'ggg' , 'fffff' , 'jjjj');
longetThan(4 , ...['aaaaa', 'ggg' , 'fffff' , 'jjjj']);

----------------------------------------------------------------------
                          for of and generators
const arr = [10 ,20 , 30, 40 , 60 , 50];
1.) for index:
    let results = 0;
    for(let i=0; i< arr.length ; i++) {
        results+=arr[i];
    }
    console.log(results);

2.) forEach with callback
    let results2 = 0;
    arr.forEach((val , index)=>{
        results2+=val;
    });
    console.log(results2);

3.) for of:
    a.) let results3 = 0;
        for(let num of arr) {
            results3+=num;
        }
        console.log(results3);

    b.) const divs = document.querySelectorAll('div')
        for(div of divs) {
            div.textContent = 'Ouch!';
        }

    c.) Generators: someNumbers returns a suspended calculation (someNumbers{<suspended>})
        function *someNumbers() {
            yield 10;
            yield 20;
            yield 30;
            for(let i =0; i<2; i++) {
                yield 5;
            }
            yield 70;
        }

        for(let num of someNumbers()) {
            console.log(num);
        }

        g = someNumbers();
        g.next()
        //{value: 10, done: false}
        g.next()
        //{value: 20, done: false}
        g.next()
        //{value: 30, done: false}
        g.next()
        //{value: 5, done: false}
        g.next()
        //{value: 5, done: false}
        g.next()
        //{value: 70, done: false}
        g.next()
        //{value: undefined, done: true}
        g.next()
        //{value: undefined, done: true}

----------------------------------------------------------------------
                            Symbols
1.) :מקבלת מחרוזת ויוצרת ממנה סימבול חדש, כמה דוגמאות Symbol הפונקציה 
    const x = Symbol('foo');
    const y = Symbol('foo');
    const z = Symbol('bar');
    x === y; //false : Each call to Symbol returns a new symbol object
    x.toString() === y.toString() //true: symbol.toString returns a string representation of the symbol results = "Symbol(foo)"
    x.toString() === z.toString() //false: z.toString() is "Symbol(bar)"

2.) :מקבלת מחרוזת ושולפת את הסימבול המתאים לה מהטבלא (אם לא קיים יוצרת חדש ומוסיפה לטבלא). כמה דוגמאות Symbol.for הפונקציה 
    const x = Symbol.for('foo')
    const y = Symbol.for('foo')
    const z = Symbol.for('bar')
    x === y // true: both refer to the same symbol
    x === z // false

:דוגמאות ל-2 סימבולים הקיימים כבר מובנים בשפה
1.) דוגמא ל-2 הסימבולים
    class MyStuff {
        [Symbol.toPrimitive] (hint) {
            if(hint === 'number') {
                return 4;
            } else if(hint === 'string'){
                return 'stuff programmers have';
            } else {
                return 7;
            }
        }
        *[Symbol.iterator]() {
            yield 'coffee';
            yield 'laptop';
            yield 'keyboard';
            yield 'cool hat';
        }
    }

    a.) Symbol.iterator
        const stuff = new MyStuff();
        for(let item of stuff) {
            console.log(item);
        }
    b.) Symbol.toPrimitive
        stuff - 1          // results: 3
        stuff+'hello'      // results: "7hello"
        Math.min(5, stuff) // results: 4

2.) עוד דוגמא לסימבול השני
    class Car {
        constructor(speed) {
          this.speed = speed;
        }

        [Symbol.toPrimitive](hint) {
          if (hint === 'string') {
                return "I am a car driving at " + this.speed + " km/h";
          } else if (hint === 'number') {
                return this.speed;
          } else {
              // JavaScript is not sure if it should use a string or a number
              // so it passes the value "default"
              return this.speed;
          }
        }
    }
    const c1 = new Car(20);
    const c2 = new Car(50);
    alert(c1);                        // alerts: "I am a car driving at 20 km/h";
    console.log(c1 + c2);             // prints: 70 to the console
    const fastest = Math.max(c1, c2); // fastest is now 50
    console.log(fastest);

----------------------------------------------------------------------
                     שיפור בכתיב האובייקטים 

const foo = 10;
const obj = {
  foo,

  [Math.max(2, 5)]: 'hello',

  hello() {
    console.log('hello');
  }
};

----------------------------------------------------------------------
                       שילוב קוד בתוך מחרוזת
const name = 'giti';
const text = `<h1>${name}</h1>`;
document.body.innerHTML = text;

const stuff = ['coffee' , 'leptop' , 'cool hat'];
const list = `
    < ul>
        ${stuff.map(el=>`<li>${el}</li>`).join('')}
    < ul>
`;
document.body.innerHTML+= list;

----------------------------------------------------------------------
                פירוק והרכבה של מערכים ואובייקטים
1.) מערכים
    const arr = [10 ,20 , 30 , 40 , 50];
    const [first , second , ...rest] = arr;


2.) אובייקטים
    const data = {
        name: 'giti' , 
        likes: {
            programing:'JavaScript',
            drinks: 'coffee',
        }
    };

    a.) const {name , likes:{programing ,drinks}} = data;
    
    b.) function printData({name , likes: {programing, drinks}}) {
            //name , programming , drinks
            console.log(`${name} ${programing} ${drinks}`);
        }
        printData(data);
----------------------------------------------------------------------
                            מודולים
 <script src="src/index.js" type="module"></script> 
1.) To load class/function that defined with export default need to do: import myName from '/.file.js'; 
2.) To load class/function that defined with export only need to do: 
    a.) import {exactlyName as myName , exactlyName as myName} from '/.file.js'; 
    b.) import * as myName from '/.file.js'; myName.* includes all functions; 
3.) To load class/function inside a function need to do: import('./file.js').then(module=>{ module.default/module.exactlyName }); 
4.) import {} from "https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"; 


1.) :יצוא מחלקה בודדת מקובץ
    export default class Car {
    }

2.) :יבוא מחלקה בודדת מקובץ חיצוני
    import Car from './car.js';


3.) :יצוא מספר פונקציות מקובץ
    export function foo() { }
    export function bar() { }

4.) :יבוא מספר פונקציות מקובץ חיצוני
    import { foo as 'myName', bar as 'myName'} from './utils.js';

5.) :טעינת ספריית צד-שלישי ללא יבוא סמלים
    import {} from 'https://cdnjs.cloudflare.com/ajax/libs/jquery/3.3.1/jquery.min.js';

6.) :טעינה דינמית
    //for default
    import('./car.js').then(function(module) {
        const Car = module.default;
        const c = new Car(10);
        c.drive();
    });
    
    //for export not default
    import('./utils.js').then(module=>{
         const {lastLetter , firstLetter} = module;
         console.log(firstLetter('giti'));
         console.log(lastLetter('giti'));
    });

----------------------------------------------------------------------
                            Promises
1.)
    const btnStart = document.querySelector('#btn-start');
    const results = document.querySelector('#result');
    btnStart.addEventListener('click',start);

    function awaitForUserInput() {
        const myPrompt = document.querySelector('#prompt');
        const input = document.querySelector('input');
        const btnGo = document.querySelector('#btn-go');
        results.style.display = 'none';
        myPrompt.style.display = 'block';
        input.value = '';

        return new Promise((resolve , reject)=>{
            btnGo.addEventListener('click',()=>{
                resolve(input.value);
                myPrompt.style.display = 'none';
            });
        });
    }

    function start() {
        awaitForUserInput().then((input)=>{
            results.style.display = 'block';
            results.innerHTML = `Hello ${input}`;
        });
    }

2.)
    function allImagesLoaded() {
        const p = document.querySelector('.loading');
        p.classList.remove('loading');
    }

    const promises = [];
    const images = document.querySelectorAll('img');
    for(let img of images) {
        const p = new Promise((resolve , reject)=>{
            img.addEventListener('load'  , resolve);
            img.addEventListener('error' , reject);
        });
        promises.push(p);
    }

    Promise.all(promises).then(allImagesLoaded).catch(function(e) {
        console.log('error loading image: ' + e.target.src);
    });

----------------------------------------------------------------------
                          async / await

const lat_field = document.querySelector('#lat-field');
const long_field = document.querySelector('#long-field');

async function getLocationAndPrint() {    
    try {
        const data = await $.get('http://api.open-notify.org/iss-now.json');
        const { iss_position: { latitude, longitude  }} = data;
        lat_field.value = latitude;
        long_field.value = longitude;
        setTimeout(getLocationAndPrint, 1000);
    } catch(err) {
        console.log('network error');
    }
}

getLocationAndPrint();

----------------------------------------------------------------------
                         Async Generator
1.) await Promise.all
2.) async iterator: for await(let data of promises) {}
3.) async generator: async function *generator() {yield...}

examples for all:

1.) 
    import {} from 'https://cdnjs.cloudflare.com/ajax/libs/jquery/3.3.1/jquery.min.js';

    async function getData(id) {
        const data = await $.get(`https://swapi.co/api/people/${id}/`);
        const futureFilms = data.films.map(film => $.get(film));
        const films = await Promise.all(futureFilms);
        for (let film of films) {
            console.log(film.title);
        }
    }

    getData(1);


2.)
    import {} from 'https://cdnjs.cloudflare.com/ajax/libs/jquery/3.3.1/jquery.min.js';

    async function getData(id) {
        const data = await $.get(`https://swapi.co/api/people/${id}/`);
        const futureFilms = data.films.map(film => $.get(film));
        for await (let film of futureFilms) {
            console.log(film.title);
        }
    }

    getData(1);

3.)
    import {} from 'https://cdnjs.cloudflare.com/ajax/libs/jquery/3.3.1/jquery.min.js';
    function asleep(ms) {
        return new Promise((resolve, reject) => {
            setTimeout(resolve, ms);
        });
    }

    async function *issLocations() {
        while (true) {
            yield $.get('http://api.open-notify.org/iss-now.json');
            await asleep(60000);
        }    
    }

    async function main() {
        const lat_field = document.querySelector('#lat-field');
        const long_field = document.querySelector('#long-field');

        for await (let data of issLocations()) {
            const { iss_position: { latitude, longitude  }} = data;
            lat_field.value = latitude;
            long_field.value = longitude;
        }
    }
    main();

-------------------------------- Maps and Sets --------------------------------------
                           
 Array.from את שניהם ניתן להפוך למערך באמצעות הפונקציה

---- Map / WeakMap ---- מפתחות וערכים בדומה לאובייקט רגיל

m = new Map(); / new WeakMap();
m.set(2, 'number two');
m.set('2', 'string two');

// m.size is now 2
m.size;

:הגבלות באובייקט המוחלש
1.) המפתחות חייבים להיות אובייקטים
2.) לדעת את הגודל או בכלל לקבל רשימה של המפתחות ,for אין אפשרות לסרוק את כל המפתחות בלולאת



---- Set / WeakSet ---- רק מפתחות

const mySet = new Set();

mySet.add(1); // Set [ 1 ]
mySet.add(5); // Set [ 1, 5 ]
mySet.add(5); // Set [ 1, 5 ]
mySet.add('some text'); // Set [ 1, 5, 'some text' ]
const o = {a: 1, b: 2};
mySet.add(o);

mySet.add({a: 1, b: 2}); // o is referencing a different object so this is okay

mySet.has(1); // true
mySet.has(3); // false, 3 has not been added to the set
mySet.has(5);              // true
mySet.has(Math.sqrt(25));  // true
mySet.has('Some Text'.toLowerCase()); // true
mySet.has(o); // true

mySet.size; // 5

mySet.delete(5); // removes 5 from the set
mySet.has(5);    // false, 5 has been removed
```

# Git and  Github


# Download specific folder from a git
# https://downgit.github.io/#/home


```JS
----------------- GIT and GitHub-------------------------

Install git window
Install gitbash

1.) git init inside my project directory
    git status to show current status
2.) git add . for all files at the first time
    git add 'file name path1' 'file name path2' for other times
    git reset 'file name path1' 'file name path2' 
3.) git commit -m 'my comment'
              
                                  GitHub
4.) Create "New reoisitory" in gitHub and then (These lines you can also be seen in GitHub): 
        a.) git remote add origin "https://github.com/gitiklar/yourRepositoryName.git"
        b.) git branch -M main
        c.) git push -u origin main



git log to see all commits
git diff to show the differences beetween versions
ls -a .git to see .git files

git cat-file commit 'dscae...'
git cat-file blob 'dscae...'
git ls-tree 'abcfeg...'

git checkout <version>
git checkout <branch>

git branch 'name' - create new branch 
git checkout -b 'bigChanges'    ===    git branch 'bigChanges'   &&&    git checkout  'bigChanges'
git branch - show all brench and what is my now
git merge master

------------------------------------- heroku -------------------------------------

1.) Click "New" -> "Create new app" -> "Create app"
2.) In Deploy tab click "GitHub" search your repository name and click "Connect"
3.) click "Enable Automatic Deploys"

Now, after you will do the next push to your repository it will be updated automatic here in heroku.
You can see in Activity tab.
In Activity tab you can click "Open app" to see the app in browther and this is the url.


link to learn How to deploy your app to the web using Express.js and Heroku
"https://www.freecodecamp.org/news/how-to-deploy-your-site-using-express-and-heroku/"
```

<div dir="rtl">
  <h1> מה קורה מהרגע שמזינים כתובת אתר ועד שהאתר מוצג למשתמש </h1>
  <p>
      1.)
        מזינים כתובת אתר בדפדפן אינטרנט.
  </p>
  <p>
      2.)
        הדפדפן מחפש את כתובת ה- IP עבור שם הדומיין באמצעות DNS
        - שהוא כעיין ספר טלפונים ועוזר לנו לספק את כתובת ה- IP המשויכת לשם הדומיין.
        
  </p>
  <p>
      3.)
        הדפדפן שולח בקשת HTTP לשרת שאחראי על הצגת המידע.
  </p>
  <p>
      4.)
        השרת מחזיר תגובה ושולח איתה את דף ה-html המתאים.
  </p>
  <p>
      5.)
        הדפדפן מריץ את הדף
        ושולח בקשות לאובייקטים נוספים המוטבעים ב- HTML (תמונות, css, JavaScript)
        ומקבל בחזרה את המידע מהשרת ומציג אותו.
  </p>
  <p>
      6.)
       לאחר טעינת הדף הדפדפן שולח בקשות אסינכורניות לפי הצורך.
  </p>
</div>




<div dir="rtl">
  <h1> הבדלים בין: LocalStorage , SessionStorage ו- Cookie </h1>
  <h2> LocalStorage </h2>
  <p>
    שומר נתונים ללא תאריך תפוגה עד שמוחקים בצורה ידנית מהדפדפן או דרך קוד JS.    </br>    
    ניתן לקריאה רק על ידי דפדפן - צד לקוח.    </br>
    10MB    </br>
  </p>
   <h2> SessionStorage </h2>
  <p>
  שומר נתונים עד לסגירת הדף    </br>
  ניתן לקריאה רק על ידי דפדפן - צד לקוח.    </br>
  5MB    </br>
  </p>
   <h2> Cookie </h2>
  <p>
מאחסן נתונים שיש לשלוח בחזרה לשרת עם בקשות עוקבות. תפוגתו משתנה בהתאם לסוג ואת משך התפוגה ניתן להגדיר מצד השרת או מצד הלקוח (בדרך כלל מצד השרת).    </br>
עוגיות מיועדות בעיקר לקריאה בצד השרת (ניתן לקרוא גם בצד הלקוח), localStorage ו- sessionStorage ניתן לקרוא רק בצד הלקוח.    </br>
ניתן לאבטח עוגיות על ידי הגדרת הדגל httpOnly כנכון עבור אותה קובץ cookie. זה מונע גישה מצד הלקוח לאותו קובץ cookie    </br>
4KB
  </p>
</div>



<div dir="rtl">
  <h1> מה זה < meta charset="UTF-8"> </h1>
  <p>
  מטא תג זה מציין בעצם עם איזו ערכת תווים אתר כתוב.
UTF-8 (Universal Transformation Format 8-bit) הוא קידוד תווים המסוגל לקודד את כל התווים האפשריים הנקראים נקודות קוד ב- Unicode. הקידוד באורך משתנה ומשתמש ביחידות קוד של 8 סיביות.
  </p>
</div>







<div dir="rtl">
  <h1> מדוע מגדירים קבצי CSS ב-head וקבצי JavaScript ב- body?</h1>
  <p>
  
 כי כאשר יש לך הצהרת CSS לפני תחילת < body>,
 הסגנונות שלך למעשה נטענו כבר.
 אז מהר מאוד משתמשים רואים שמשהו מופיע על המסך שלהם 
(למשל צבעי רקע).
 אם לא,
 משתמשים רואים מסך ריק למשך זמן מה לפני שה- CSS 
מגיע למשתמש.

כמו כן, 
אם אתה משאיר את הסגנונות איפשהו ב- < body>, 
הדפדפן צריך לעבד מחדש את הדף (חדש וישן בעת הטעינה) 
כאשר הסגנונות שהוגדרו כבר עובדו.
  </p>
</div>






<div dir="rtl">
  <h1> שליחת מידע לשרת באמצעות מהטופס ללא בקשת AJAX</h1>
  <pre dir="ltr">
        < form action="/action_page.php" method="post" target="_blank">
          < label for="fname">First name:< /label>
          < input type="text" id="fname" name="fname">
          < label for="lname">Last name:< /label>
          < input type="text" id="lname" name="lname">
          < input type="submit" value="Submit">
        < /form>
  </pre>
  <p>
    השמות שישלחו מתאימים למה שנכתב ב-name=
    בבקשה מסוג GET יופיע המידע בשורת הכתובת ובבקשה מסוג POST הוא לא יופיע אלא רק ישלח.
    לדוגמא:
    </p>
    <p dir = "ltr">
      "https://www.w3schools.com/action_page.php?fname=רחל&lname=כהן"
    </p>
</div>

<div dir="rtl">
  <h1>כמה דרכים למיקום אלמנט במרכז</h1>
    <p>
      1.) For container element do:  display: flex , align items:center , justify-content:center
    </p>
    <p>
      2.) For inner element do: margin-top: calc(50% - halfHeight) , margin-left: calc(50% - halfWidth)
    </p>
    <p>
      3.) # For container element do position: relative  # For inner element do: position: absolute , top: ...px , left: ...px
    </p>
    <p>
      4.) For inner element do: margin: auto
    </p>
    <p>
      5.) For inner element do: display: inline-block , text-align:center
    </p>
</div>


<div dir="rtl">
  <h1>מצב בטוח</h1>
    <p>
    <p>
    -----------------  Strict Mode  מצב בטוח ------------------ 
    </p>
    <p>
 מצב בטוח מבקש מהדפדפן לחפש יותר שגיאות בתוכניות JavaScript.
 </p>
  <p>
מצב זה לא מופעל אוטומטית כדי שקוד ישן יוכל לעבוד.
</p>

1. Enabling strict mode
    -"use strict";

2. Assignment to global variables

3. Assignemnt to reserved words

4. Octal values
    </p>
</div>

<div dir="rtl">
  <h1>קריאה לפונקציה באמצעות Call לעומת Apply</h1>
    <p>
        func.call(arg1 , arg2, arg3); //arg1 for this
    </p>
    <p>
        func.apply(array); ///The first limb for this
    </p>
</div>

<div dir="rtl">
  <h1>מהם הפיצ'רים של ריאקט?</h1>
    <p>
      1.) JSX - JavaScript XML
      הוא הרחבה של - JavaScript. משתמשים בו ב- React כדי לתאר כיצד ממשק המשתמש צריך להראות. על ידי שימוש ב- JSX, אנו יכולים לכתוב מבני HTML באותו קובץ המכיל קוד JavaScript.
      הדפדפנם לא יודעים לקרא את ה-JSX כיון שזה לא מבנה חוקי של JS ולכן משתמשים בתרגום של Babel שמתרגם אותו לשפת JS רגילה.
      את Babel מפעילים גם באמצעות webpack.
    </p>
    <p>
      2.) Components - 
        קומפוננטות הם אבני הבנין של כל יישום ריאקט , כל אפליקציה מורכבת מהרבה קומפוננטות , 
        הקומפוננטות האלה למעשה מפצלות את ממשק המשתמש לחלקים עצמאיים , שניתן לעשות בהם שימוש חוזר.
    </p>
       <p>
      3.) Virtual DOM - 
        DOM וירטואלי הוא אובייקט JavaScript קל משקל אשר מכיל עותק של ה- DOM האמיתי. זהו עץ המפרט את האלמנטים, תכונותיהם ותוכנם כאובייקטים ותכונותיהם. 

כיצד זה עובד:
בכל פעם שנתונים בסיסיים משתנים, ממשק המשתמש כולו מועבר מחדש בייצוג DOM וירטואלי.ואז מחושב ההפרש בין ייצוג ה- DOM הקודם לזה החדש.
לאחר ביצוע החישובים, ריאקט יעדכן ב- DOM האמיתי רק את הדברים שהשתנו בפועל.
וזה בעצם מה שמביא את ריאקט לביצועים מהירים מאד, כי את הגישה ל-DOM האמיתי שהיא כבידה יותר - ריאקט הוא זה שמבצע, ובצורה היעילה ביותר.
    </p>
    <p>
    4.) 
    זרימת נתונים חד כיווני:
    state -> render -> Ui -> event -> state -> render -> Ui <br>
    כל השינויים בתצוגה באים רק דרך השינוי של הסטייט, אין אפשרות לשנות את ה-HTML בגישה ישירה<br>
    לעומת זרימה פשוטה שהיא דו כוונית:<br>
    Ui -> model(=data=state or props) .על ידי אירוע התצוגה מעדכת את המודל <br>
    model -> Ui .המודל יכול לעדכן את התצוגה בגישה ישירה<br>
    </p>
</div>

<div dir="rtl">
  <h1>ריאקט לעומת אנגולר</h1>
    <pre dir="ltr">
            React                           Angular<br>
            Virtual DOM                     Real DOM<br>
            Fast                            Slow<br>
            Compile time debugging          Runtime debugging<br>
            Facebook                        Google<br>
            One-way data binding            Two-way data binding<br>
    </pre>  
</div>

<div dir="rtl">
  <h1>ES6 לעומת ES5 בריאקט</h1>
    <pre dir="ltr">
            ES5                           ES6<br>
            React.createClass             class<br>
            exports                       export<br>
            require                       import<br>
    </pre>  
</div>


<div dir="rtl">
  <h1>מה צריך בשביל לבנות פרויקט ריאקט</h1>
    <p>
      להתקין NodeJS בשביל חבילת ה-npm שבאמצעותו מתקינים את ריאקט
    </p>
    <p>
      להתקין create-react-app<br>
      מומלץ לעבוד עם webpack ואז צריך להתקין את החבילות שלו
    </p>
    <p>
      להתקין איזשהו text editor כמו VS Code
    </p>
</div>

<div dir="rtl">
  <h1>מה זה אירוע בריאקט</h1>
    <p>
      אירוע זו איזשהי פעולה שמשתמש או מערכת עשויים להפעיל כמו: לחיצה, הזזת עכבר.
      ב-JSX אנחנו מעבירים את הפונקציה שתיקרא בעקבות הפעולה.
      השמות של האירועים דומים ל-HTML אך ההבדל ביניהם הוא שהשם שבא אחרי ה-on מתחיל באות גדולה, כמו:
      onClick
    </p>
</div>

<div dir="rtl">
  <h1>מה זה אירוע סינטטי בריאקט</h1>
    <p>
        אירועים סינתטיים הם האובייקטים המשמשים כמעטפת בין דפדפנים סביב האירוע המקורי של הדפדפן.
          הם משלבים את ההתנהגות של דפדפנים שונים ל- API אחד. זה נעשה כדי לוודא שהאירועים מציגים מאפיינים עקביים בדפדפנים שונים.
      </p>
</div>

<div dir="rtl">
  <h1>מהו המאפיין key?</h1>
    <p>
       <h2>המאפיין key מסמן לריאקט את הקשר בין האלמנט ברנדר הקודם לאותו אלמנט ברנדר הבא.</h2><br>
       כאשר אנו נותנים key,  ריאקט יכול להסתכל על תוצאה של רנדר ישן ורנדר חדש ולהתאים אלמנטים, ובצורה כזו הוא לא יצטרך ליצור מחדש אלמנטים שכבר נמצאים שם. <br>
       ריאקט יעשה מאמץ להשתמש ממש באותו אלמנט אם בתוכן שלו אין שום שינוי ואם יש שינוי אז יתן פקודות לשנות רק את מה שהכרחי. <br>
       ז"א: לאחר כל רנדר, כאשר יש לריאקט ביד את הוירטואל דום החדש הוא ישווה אותו לוירטואל דום הישן.<br>
       אם הוא רואה איזשהו מפתח שקיים בשני הוירטואל דום , והמאפיינים שלו לא השתנו, אז הוא יקח את האלמנט בשלימותו ולא ייצור אותו מחדש.
       בצורה כזו אנחנו מבטיחים ביצועים טובים יותר.<br>
       וגם אם יש הבדל בתוכן של האלמנטים - ריאקט יתן פקודות לשנות רק את מה שהכרחי.<br>
       <h2>לדוגמא:</h2>
       נניח שבמסך מופיעות 5 קוביות שמיוצרות כרשימה מתוך מערך ואין להם מפתחות, נקרא להם:<br>
       [A , B , C , D , E]<br>
       לחיצה על קוביה מוחקת מהמערך את אותה קוביה , נניח שלחצו על C<br>
       ז"א שברנדר הבא יהיה לריאקט ביד  את הדום אלמנט הישן והדום אלמנט החדש שנראה כך:<br>
       [A , B , D , E]<br>
       כאשר אין מפתחות , ברירת המחדל של ריאקט הוא האינדקס, כלומר המיקום שלו ברשימה.<br>
       ואז ריאקט מחשב את זה כך:<br>
       הקוביה הראשונה A לא השתנתה.<br>
       הקוביה השניה B גם כן לא השתנתה.<br>
       הקוביה השלישית, אותו מקום שבו היה האלמנט C כעת יש שם אלמנט אחר שנקרא D ולכן תקבל את המאפיינים של D.<br>
       הקוביה הרביעית, אותו מקום שבו היה האלמנט D כעת יש שם אלמנט אחר שנקרא E ולכן תקבל את המאפיינים של E.<br>
       וכך יוצא שכל תיבה שבאה אחרי התיבה שנמחקה תקבל את המאפיינים של התיבה שבאה אחריה וזה בעצם בזבזני <br>    
      כיוון שאם היינו נותנים מפתחות לאלמנטים ריאקט היה יודע להתאים את האלמנטים לפי המפתחות וכך רק היה מדלג על התיבה C ומשאיר את כל השאר אותו דבר.<br>
      ענין המפתחות חשוב מאד גם בשביל memo:<br>
      בדוגמא הנ"ל, עבור 2 האלמנטים הראשונים ה-memo יתפוס ויגרום לאלמנט לא להתרנדר מחדש כיון שהתוכן לא השתנה.<br>
      אבל עבור 2 האלמנטים שנשארו - אלו שבאו אחרי המחיקה, מבחינת ריאקט המאפיינים שלהם השתנו כיון שהוא משווה את האלמנטים לפי האינדקס שלהם ולכן:<br>
      new D != old C <br>
      new E != old D <br>
      </p>

</div>

<div dir="rtl">
  <h1>מה זה useRef</h1>
    <p>
    בעבודה הרגילה עם ריאקט יש ניתוק בין הקוד לבין מה שרואים על המסך , הקוד הוא דיקלרטיבי וריאקט דואג להכל מאחורי הקלעים. 
    ולכן בשיטה הזו אין לנו את הגישה הישירה לדום.<br>
    יש מצבים מסויימים, נדירים שבהם הגישה לדום היא הכרחית, כמו: פוקוס על אלמנט או API חיצוני כלשהו שדורש אלמנט.<br>
    עבור המקרים האלה ריאקט נותן לנו את ה-useRef שהוא בעצם הquerySelector של ריאקט, זו הדרך להגיע ממש לאלמנט.<br>
    <b>איך זה עובד:</b><br>
     מגדירים איזשהו משתנה שמתקבל מ - useRef 
    ואז לאותו אלמנט שאנו רוצים עבורו את ההפניה, אנחנו נותנים מאפיין מיוחד שנקרא ref והוא יהיה שווה לאותו משתנה שקיבל את הערך שלו מה-useRef.<br>
    המאפיין הזה אומר לריאקט: כשאתה לוקח את האלמנט הזה ומחבר אותו לדום אלמנט אמיתי - כי הרי כאן מדובר בוירטואל דום אלמנט -
    אז שמור את ההפניה לדום אלמנט האמיתי ותן לי לגשת אליו באמצעות המשתנה שהגדרתי נקודה current וזה האלמנט .<br>
    (event.target גם גן מביא לי את האלמנט רק שלא תמיד אנחנו רוצים לקבל את אותו אלמנט שיצר את האירוע)
    </p>
</div>

<div dir="rtl">
  <h1>מה זה useEffect</h1>
    <p>
      הדינמיקה של ריאקט עובדת כך:<br>
      יש לנו משהו בסטייט שמתעדכן ואחרי שמתעדכן יש UI חדש שיוצר איזשהו אירוע שמעדכן שוב פעם את הסטייט ואז שוב יתבצע רנדר ל-UI חדש , וזה נראה כך:<br>
      State -> Render -> UI -> State -> Render -> UI<br>
      מה קורה כשרוצים לצאת לעולם שבחוץ , לולאת הסטייט UI הרי לא נותנת לנו יותר מידי קשר לעולם החיצון: <br>
      ומה יש בעולם החיצון:<br>
      1.) כותרת - Title<br>
      2.) APIs חיצוניים<br>
      3.) פעולות אסינכרוניות<br>
      4.) פעולה שמתבצעת רק בעת עלית הפקד<br>
      useEffect הוא הדרך שלנו לקשר בין משתנה סטייט לבין משהו שקורה מחוץ למעגל הזה,<br>
       התבנית: <br>
      <pre dir="ltr">
          useEffect(()=>{
              //run code here if dependencies change
              return function abort() {
              };
          },[dependecies]);
      </pre>
      וזה עובד כך: כאשר יש איזשהו שינוי בסטייט , ז"א שאחד מהתלויות שנמצאות ברשימה משתנה, ריאקט מפעיל את הקוד שנמצא בתוך ה-useEffect<br>
      ואם הסטייט משתנה פעם נוספת או שהקומפוננטה עוזבת את המסך, לפני שריאקט מריץ שוב את הקוד שלמעלה , הוא יריץ את פונקציית הביטול.
    </p>
</div>


<div dir="rtl">
  <h1>מה זה Custom Hook?</h1>
    <p>
      Custom Hook - הוא הדרך לשתף קוד שהוא לא JSX אלא כל הקוד שנמצא מעל ה-JSX בריאקט Hooks.<br>
      Custom Hook - היא פונקציה שמתחילה במילה use ויכולה לקרא לכל הHooks הרגילים של ריאקט:<br>
      useState , useEffect , useRef ...<br>
      בדרך כלל היא מחזירה ערך אחד או יותר שהיא מחשבת.<br>
      לדוגמא: <br>
      <pre dir="ltr">
      export function useTimer(ms = 1000) {
        const [tick , setTick] = useState(0);
        function updateTick() {
          setTick(v => v + 1);
        }
        useEffect(()=>{
          const timerId = setInterval(updateTick , ms);
          return ()=>clearInterval(timerId);
        },[]);
        return tick;
      }
      function NewsTicker({items}) {
        const index = useTimer(2000);
        return (
          < p>{items[index % items.length]}< /p>
        );
      }
      </pre>
      <h2>מהי החשיבות בכך שפונקצית Custom Hook מתחילה במילה use?</h2>
      התשובה היא שפונקציות Hooks חייבות להיקרא בדיוק לפי הסדר ובאותה כמות בכל פעם שמפעילים את פונקצית הפקד.<br>
      ולכן אסור להשתמש בפונקציות Hook בתוך תנאי או לולאה , כיון שזה מבלבל את ריאקט ואת מנגנון שמירת הסטייטים שלו.<br>
      ולכן מאד חשוב כשכותבים פונקציית פקד, לדעת האם הוא מפעיל use  או לא מפעיל כדי לדעת האם אסור לרשום אותו בלולאה או בתנאי.<br> 
      <b>ז"א שריאקט לא מחייב שהשם יתחיל ב-Hook אבל אנחנו עושים זאת כדי שנדע שמדובר ב-Hook.</b>
    </p>
</div>

<div dir="rtl">
  <h1>מה זה Higher Order Component - HOC?</h1>
    <p>
      אם Custom Hook היא הדרך שלנו לשתף קוד בריאקט Hook בלבד, אז HOC היא הדרך לשיתוף קוד שעובד גם בכתיב הקלאסים וגם בכתיב הקפונקציות:<br>
      קוד של HOC מגיע תמיד באותו מבנה דומה: <br>
      1.) מגדירים פונקציה שמקבלת קוד של פקד בתור פרמטר<br>
      2.) הפונקציה מחזירה קוד של פקד חדש אותה היא יוצרת<br>
      3.) ברנדר של הפקד החדש הפונקציה מחזירה את הפקד שהועבר כפרמטר ומעבירה אליו את כל ה-props שקיבלה כמו שהם<br>
      4.) הפונקציה מעבירה props חדש שאותו היא יצרה וזה בעצם הקוד שמשותף.<br>
      לדוגמא:<br>
    </p>
</div>

```JS
  function withClock(Component) {
        return function WithClock(props) {
          const { ms } = props;
          const [tick , setTick] = useState(0);

          function updateTick() {
            setTick(tick => tick + 1);
          }

          useEffect(()=>{
            const timerId = setInterval(updateTick , ms);
            return ()=>clearInterval(timerId);
          });

          return(<Component {...props} tick={tick}/>);
        }
    }

  const NewsTicker = withClock(function NewsTicker({items , tick}) {
        return (
          <p>{items[tick % items.length]}</p>
        );
  });
  NewsTicker.defaultProps = { ms: 1000,};

  const App = () => {
    const items = [
      "I lit up from Reno",
      "I was trailed by twenty hounds",
      "Didn't get to sleep that night",
      "Till the morning came around",
    ];

    return (
      <div>
          <NewsTicker items={items} ms = {2000}/>
      </div>
    );
  };
```
<div dir="rtl">
  <h1>מה זה React.children?</h1>
    <p>
      React.children הוא הדרך לשתף קוד ולהוציא החוצה לוגיקה עוטפת של קוד JSX<br>
      דוגמאות: <br>
    </p>
</div>
<div dir="rtl">
    <p>
     דוגמא פשוטה ללא הוספת לוגיקה:<br>
    </p>
</div>

```JS
import React from 'react';

function PagesContainer(props) {
  return (
    <div>
      <h1>Hello World</h1>
      {props.children}
      <h1>Hi all</h1>
    </div>
  );
}

export function Page1(props) {
  return (
    <PagesContainer>
      <p>Page 1</p>
      <p>Page 111</p>
    </PagesContainer>
  );
}

export function Page2(props) {
  return (
    <PagesContainer>
      <p>Page 2</p>
      <p>Page 222</p>
    </PagesContainer>
  );
}
```
<div dir="rtl">
    <p>
     דוגמא שכוללת הוספת לוגיקה לאלמנט המיכל:<br>
    </p>
</div>

```JS
export function FormsContainer(props) {
    const [dataObjOfAllPages , setDataObjOfAllPages] = useState({});
    const [currentIndex , setCurrentIndex] = useState(0);
    const countOfPages = React.Children.count(props.children);
  
    function updateDataObjOfAllPages(dataObj) {
      setDataObjOfAllPages({...dataObjOfAllPages, ...dataObj});
    }
    
    function getCurrentPage() {
      //In order to add props to child , we need do this:
      const child = React.Children.toArray(props.children)[currentIndex];
      return React.cloneElement(child , { dataObjOfAllPages : {...child.props.dataObjOfAllPages , ...dataObjOfAllPages} , updateDataObjOfAllPages});
    }
   
    return (
      <>
        {getCurrentPage()}
        <div className="btnsContainer">
            <button disabled={currentIndex === 0} onClick={()=>setCurrentIndex(v=>v-1)}>Previous</button>
            <button disabled={currentIndex === countOfPages-1} onClick={()=>setCurrentIndex(v=>v+1)}>Next</button>
        </div>
      </>
    );
  }
```
<div dir="rtl">
  <h1>מה זה memo?</h1>
    <p>
         מטרת ה-memo: צימצום הרנדרים המיותרים שביישום:<br>
         ללא שימוש ב-memo , בכל פעם שסטייט משתנה מתבצע רנדר מחדש של כל עץ הפקדים שנמצא מתחת לקומפוננטה הזו שהשתנתה<br>
         React.memo זה בעצם HOC שריאקט יצרה לנו שאותה אנחנו מפעילים ואליה אנחנו שולחים את הקומפוננטה שלנו שאותה אנחנו לא רוצים לרנדר תמיד.<br>
         ה-HOC הזה מסתכל על ה-props שנשלח ובודק האם משהו השתנה בו מהרנדר הקודם, אם לא, אז הוא יודע לא לרנדר מחדש את הפקד.<br>
         ל-memo ניתן להעביר פרמטר שני שלא חובה להעביר אותו, הפרמטר השני זוהי פונקציה נוספת שאומרת לו מתי ה-props שווים , היא צריכה להחזיר ערך true או false <br>
          דוגמאות ל-2 המקרים:<br>
    </p>  
</div>

- 1.)
```JS
export default React.memo(function ColorPalette(props) {
  console.log('Color Palette');
  const { start } = props;
  const [deletedBoxes, setDeletedBoxes] = useState(new Set());

  function removeBox(e) {
    const id = e.target.dataset.id;
    deletedBoxes.add(Number(id));
    setDeletedBoxes(new Set(deletedBoxes));
  }

  const colors = [];
  for (let i=-360; i < 360; i++) {
    if (deletedBoxes.has(i)) continue;

    colors.push(
      <ColorBox
        key={i}
        start={start}
        spin={i}
        onClick={removeBox}
        id={i}
      />
    );
  }
  return colors;
});
```
- 2.)
```JS
export default React.memo(function Fiver(props) {
  console.log('Fiver');
  const { ticks } = props;

  return (
    <p>{Math.floor(ticks / 5)}</p>
  );
},(prevProps , nextProps)=>{
  return Math.floor(prevProps.ticks / 5) === Math.floor(nextProps.ticks / 5);
});
```
<div dir="rtl">
  <h1>מה זה useCallback?</h1>
    <p>
        הפונקציה useCallbak של ריאקט נועדה להגיד לריאקט שהפונקציה שלי לא משתנה בין render-ים ואפשר להשתמש באותו אוביקט פונקציה. זה קצת דומה ל Ref אבל נועד ספציפית לפונקציות.<br>
        <b>לדוגמא:</b> <br>
    </p>  
</div>

```JS
export default React.memo(function ColorPalette({start}) {
  console.log('Color Palette');
  const [render , setRender] = useState(0);
  const deletedBoxesRef = useRef(new Set());
  const deletedBoxes = deletedBoxesRef.current;

  const removeBox = useCallback(function removeBox(e) {
    const id = e.target.dataset.id;
    deletedBoxes.add(Number(id));
    setRender(v=>!v);
  },[deletedBoxes]);

  const colors = [];
  for (let i=-360; i < 360; i++) {
    if (deletedBoxes.has(i)) continue;

    colors.push(
      <ColorBox
        start={start}
        spin={i}
        onClick={removeBox}
        id={i}
      />
    );
  }
  return colors;
});
```
<div dir="rtl">
    <p>
הפרמטר הראשון ל useCallback הוא הפונקציה, והפרמטר השני הוא מערך של משתנים שהפונקציה תלויה בהם. עכשיו כל פעם שאחד הדברים במערך ישתנה ריאקט יבנה מחדש את הפונקציה, אבל כל עוד משתנים אלה שומרים על ערכם גם הפונקציה תישאר זהה.    
    </p>  
</div>

<div dir="rtl">
  <h1>ארכיטקטורת flux</h1>
    <p>
אנחנו יודעים לשמור מידע בתור משתנה State של פקד, וגם להעביר מידע מפקד לילדים שלו, אבל העסק הזה הופך קשה יותר ויותר ככל שהמרחק בין הפקד העליון ביותר שצריך את המידע לפקד התחתון ביותר שצריך אותו גדל.<br>    
לכן יהיה לנו הרבה פעמים מאוד נוח לשמור את המידע והלוגיקה של היישום מחוץ לפקדים, ולהשתמש בפקדים רק בתור שכבת UI שמקבלת את המידע מבחוץ ומציגה אותו. רעיון זה הביא לארכיטקטורה שנקראת Flux.<br>
<b>היתרונות:</b><br>
- לקצר את החוטים הארוכים של הסטייט שמועבר בין אבא לבן עמוק בעץ הפקדים.<br>
- קל מאד לראות בכל רגע נתון את המצב של היישום מכל ההיבטים כיון שכל המידע שמור באוביקט אחד דבר שמקל מאד על הדיבוג.<br>
- קל לכתוב בדיקות נקיות כאשר כל הלוגיקה מצויה במקום אחד.<br>

  <h2>הרעיונות המרכזיים של ארכיטקטורת Flux</h2>

1.) הרכיב המרכזי נקרא Store. זהו מחסן מידע חיצוני לפקדים שתפקידו לשמור את המידע הגלובאלי של היישום. בפלאקס הקלאסי יהיה Store לכל היבט ביישום. כל קומפוננטה יכולה לקרוא מידע מכל Store, ובאופן אוטומטי כשמשהו ב Store משתנה כל הקומפוננטות שקשורות אליו ירונדרו מחדש.<br>

2.) כדי להודיע ל Store שמשהו קרה קומפוננטה שולחת Action. ה Action הוא בסך הכל אוביקט ותפקידו של ה Store להחליט איך לטפל ב Action הזה.<br>

3.) בגלל שקומפוננטה לא יודעת איזה Store יצטרך לטפל באיזה Action, יש לנו רכיב נוסף שנקרא Dispatcher. ה Dispatcher תופס את ה Action ומעביר אותו ל Store שמחכה לו.<br>

גישה כזו מייצרת סוג נחמד של דינמיקה ביישום:<br>

1.) המידע הראשוני נכנס ל Stores וגורם להצגת ממשק משתמש ראשוני על המסך.<br>

2.) משתמש מבצע פעולה ואז הקומפוננטה הרלוונטית זורקת Action ל Dispatcher.<br>

3.) ה Dispatcher מפנה את ה Action לכל ה Stores הרלוונטיות, וכל Store שאכפת לו מה Action מתעדכן.<br>

4.) בעקבות העדכון במידע ב Stores גם הקומפוננטות שמקשיבות ל Stores אלה מרונדרות מחדש.<br>

  </p>  
</div>

<div dir="rtl">
  <h1>מימוש flux על ידי redux</h1>
    <p>
    רידאקס זוהי גרסה ספציפית או מימוש ספציפי של ארכיטקטורת פלאקס.<br>
    <h2>הרעיונות המרכזיים של redux</h2>
    1.) ברידאקס יש רק Store אחד. כל המידע שנשמר ב Store הוא Immutable.<br>
    2.) כל פעם שה Store משתנה מכל סיבה שהיא, כל הקומפוננטות במסך ירונדרו מחדש.<br>
    3.) זה לא כל כך נורא כי כל המידע הוא Immutable. לכן באופן אוטומטי נוכל לדלג על Render של קומפוננטות אם המידע שהן תלויות בו לא משתנה.<br>
    4.) בגלל שיש רק Store אחד, ה Store הוא גם ה Dispatcher. הוא מקבל את כל ה Actions ומעדכן את עצמו בהתאם.<br>
  </p>
  <h2>ה-flow: </h2>
  <h2>Component => Action => Dispatcher => middleware=>middleware... => Store => Reducers => State</h2>
</div>

<div dir="rtl">
  <h1>Mutable לעומת immutable ב-JS</h1>
    <p>
      Immutable - משתנה שלא ניתן לשנות את ערכו מאז שהוגדר מבלי לשנות את הכתובת שלו, ז"א שהדרך היחידה לעדכן אותו היא ליצור אובייקט חדש עם כתובת חדשה בזכרון. לדוגמא: String , Number
    </p>  
    <p>
      Mutable - משתנה שניתן לשנות את ערכו מבלי לשנות את הכתובת שלו בזכרון, לדוגמא: Array , Object
    </p>
</div>




# סיכום חדש
```JS

/////////////////////////////////////////////////////////////////////
////////////        var , const , let and freeze        /////////////
/////////////////////////////////////////////////////////////////////
```
```html
 var   = מוכר בכל הפונקציה
 const = מוכר רק בבלוק שבו הוגדר ולא ניתן לשנות את ההפניה שלו לאחר ההצהרה
 let   = מוכר רק בבלוק שבו הוגדר וניתן לשנות את ההפניה שלו לאחר ההצהרה 

כך הקוד קריא יותר כיון שברור שיש למשתנה רק ערך אחד אפשרי const-ומעדיפים מלכתחילה להשתמש ב var-היום לא מקובל להשתמש ב
let - רק כשממש חייבים משתמשים ב

 Object.freeze(arr/obj)
 לא ניתן גם לשינוי פנימי
```

/////////////////////////////////////////////////////////////////////
//////////////////            == vs ===            //////////////////
/////////////////////////////////////////////////////////////////////

```html
 == ממיר טיפוסים ולכן פחות מחמיר , לדוגמא אם נשווה את המספר 2 למחרוזת 2 מבחינתו הם שווים והתוצאה תהיה אמת 
 === לא ממיר טיפוסים ולכן יותר מחמיר, ואם נשווה את המחרוזת 2 למספר 2 התוצאה תהיה שקר
```

/////////////////////////////////////////////////////////////////////
////            Strict Mode - "use strict"  מצב בטוח            ////
/////////////////////////////////////////////////////////////////////

.JavaScript מצב בטוח מבקש מהדפדפן לחפש יותר שגיאות בתוכניות
.מצב זה לא מופעל אוטומטית כדי שקוד ישן יוכל לעבוד
Enabling strict mode -"use strict";
1. מתריע על משתנים גלובלים שלא הוגדרו כנדרש
2. מתריע על הקצאה למילים שמורות
3. Octal values


/////////////////////////////////////////////////////////////////////
///////            Array - פונקציות הכנסה והוצאה            ///////
/////////////////////////////////////////////////////////////////////


arr.push(40); - הכנסת איבר לסוף המערך
arr.unshift(0); - הכנסת איבר לתחילת המערך
arr.pop(); - הוצאת איבר מסוף המערך
arr.shift(); - הוצאת איבר מתחילת המערך


/////////////////////////////////////////////////////////////////////
////////////            Array - מעבר בלולאה            /////////////
/////////////////////////////////////////////////////////////////////


for(let item of array) {
   console.log(item); 
}


/////////////////////////////////////////////////////////////////////
//////            Array - פונקציות שימושיות במערך            //////
/////////////////////////////////////////////////////////////////////


array.forEach((item , index , arr) => console.log(item))
מעבר על המערך ועשיית פעולה כלשהי עבור כל איבר במערך הפונקציה לא מחזירה ערך

array.map((item , index , arr) => item*2)
callback - מעבר על המערך , הפונקציה מחזירה מערך חדש באותו גודל של המערך המקורי , המערך יכיל את הערכים שחזרו מפונקצית ה

array.filter((item , index , arr) => item > 3)
true את הערך callback - מעבר על המערך, הפונקציה מחזירה מערך חדש בגודל הקטן או שווה למערך המקורי, המערך יכיל את כל האיברים שעבורם החזירה פונקצית ה

array.reduce((accumulator, currentValue, index, arr) => accumulator + currentValue);
מתבצעת על כל אלמנט במערך למעט האלמנט הראשון אם לא סופק פרמטר שני לפונקציה, הערך שחוזר הוא ערך יחיד שהוא הערך המצטבר callback - פונקציה ה

array.find((item , index , arr) => item > 20)
undefined ואם אין אלמנט כזה הפונקציה מחזירה true callback - הפונקציה מחזירה את האיבר הראשון שעבורו מחזירה פונקצית ה

array.findIndex((item , index , arr) => item > 20)
-1 ואם אין אלמנט כזה הפונקציה מחזירה את הערך true callback - הפונקציה מחזירה את האינדקס של האיבר הראשון שעבורו מחזירה פונקצית ה

array.indexOf(5)
הפונקציה מקבלת איזשהו ערך ומחזירה את האינדקס של המופע הראשון שלה

array.sort((a , b) => a - b)
ואם הערך אפס אז הם שווים a קודם ל - b אם הערך שחוזר הוא מספר חיובי אז  b - קודם ל a הפונקציה מקבלת פונקציית השוואה ואם הערך שחוזר מהפונקציה הוא מספר שלילי אז  

array.every((item , index ,arr) => item > 30)
false אם כל האלמנטים במערך עונים על התנאי שמספקת הפונקציה הפנימית, אחרת יוחזר true הפוקציה מחזירה ערך בוליאני 

array.includes(5)
הפונקציה בודקת אם המערך מכיל את המספר 5 אם כן מחזירה אמת אחרת שקר

array.slice(startIndex , endIndex)
מחזיר מערך חדש מהאינדקס הראשון ועד השני לא כולל השני , הפונקציה אינה משפיעה על המערך המקורי

array.splice(startIndex , count , [elements to add from start index])
מחזיר מערך חדש מהאינדקס הראשון על פי הכמות המסופקת במשתנה השני , הפונקציה משפיעה על המערך המקורי

array.reversed();
האלמנט הראשון הופך להיות אחרון ולהיפך

array.join()
הפונקציה יוצרת ומחזירה מחרוזת חדשה על ידי שרשור של כל האלמנטים במערך, האלמנטים יופרדו בפסיקים או בדבר אחר שצויין בסוגריים

array.fill(value , [start] , [end])
מילוי המערך בערך שנקבע מאינדקס נתון עד אינדקס נתון

const array1 = ['a', 'b', 'c'];
const array2 = ['d', 'e', 'f'];
const array3 = array1.concat(array2);
expected output: Array ["a", "b", "c", "d", "e", "f"]
חיבור 2 מערכים למערך אחד, ניתן גם לחבר ערכים בודדים למערך הראשון


Array.from(arrayLike, function mapFn(element, index, array) { ... }, thisArg)
const range = (start, stop, step) => Array.from({ length: (stop - start) / step + 1}, (_, i) => start + (i * step));
ניתן להפוך סט או כל איטרבל למערך רק האיבר הראשון הוא חובה


///////////////////////////////////////////////////////////////////
//            Object - פונקציות שימושיות אובייקט            /////
///////////////////////////////////////////////////////////////////

:שתי דרכים להוספת איבר לאובייקט
1.) obj['key'] = value;
2.) obj.key = value;

:מחיקת איבר מאובייקט:
1.) delete obj['key'];
2.) delete obj.key;


call הוא האובייקט שנמצא משמאל לנקודה, ניתן לשנות אותו באמצעות הפונקציה  this - גישה לפונקציה מאובייקט, ה
const p1 = {
    name: 'John',
    hello() {
        console.log(`Hi! ${this.name}`);
    },
}

const p2 = {
    name: 'aaa',
    hello() {
        console.log(`Hi! ${this.name}`);
    },
}

p1.hello.call(p2) // print Hi! aaa


///////////////////////////////////////////////////////////////////
//            String - פונקציות שימושיות במחרוזת            /////
///////////////////////////////////////////////////////////////////

String.indexOf(value , fromIndex);
חיפוש מחרוזת בתוך מחרוזת מהאינדקס המבוקש

///////////////////////////////////////////////////////////////////
//////////////////            This            /////////////////////
///////////////////////////////////////////////////////////////////

1.) window - מחוץ לפונקציה הערך תמיד יהיה שווה ל 
2.) window - בתוך הפונקציה - ברב המקרים ערכו של המשתנה הזה תלוי בדרך אותה מפעילים את הפונקציה ואם מפעילים כרגיל בדרך הפשוטה אז הוא עדיין שווה ל 
3.) const newFn = fn.bind(this); 
    מגדיר פונקציה חדשה כשהערך של המשתנה דיס שלה ישאר תמיד ללא קשר כיצד יקראו לפונקציה
4.) arrow functions - שומר על הדיס בהקשר המתאים ללא קשר כיצד הפונקציה נקראת
5.) fn.apply(thisArg , argsArray) and fn.call(thisArg , arg1 , arg2...);
    פונקציות אלו מאפשרות לקרא לפונקציה ולתת לה את הערך של הדיס , המשתנה הראשון שנשלח לפונקציה נכנס לתוך הדיס של הפונקציה
6.) אם מפעילים את הפונקציה מתוך אובייקט הדיס הוא האובייקט שנמצא משמאל לנקודה

///////////////////////////////////////////////////////////////////
///////////////////            Map()          /////////////////////
///////////////////////////////////////////////////////////////////

Map היתרונות של 
1.) שומר על סדר ההכנסה
2.) ניתן לדעת גודל בקלות
3.) ניתן לרוץ בקלות על המפתחות והערכים
     for (let [word, count] of counters) {
         console.log(`The word ${word} appears ${count} times`);
     }
4.) ניתן להשתמש בכל סוג של משתנה בתור מפתח ולא רק מחרוזות כמו באובייקט רגיל ולכן ניתן להכניס גם את המחרוזת 2 וגם את המספר 2


בגלל הבעיה שהמפה יכולה לשמור גם אובייקטים ולגרום לזליגת זכרון במקרה שהאלמנט ימחק מהדום
לשם כך יש את האובייקט המוחלש שמנם יכול לשמור אך ורק אובייקטים אך הוא אינו שומר את המפתחות בחיים ומוחק אוטומטית את האובייקט מהמפה ברגע שימחק מהדום 
הגבלה נוספת מעבר לכך שהמפתחות חייבים להיות אובייקטים היא שאין אפשרות לסרוק בלולאה או לדעת את הגודל של המפה או לקבל רשימה של המפתחות

///////////////////////////////////////////////////////////////////
///////////////////            Set()          /////////////////////
///////////////////////////////////////////////////////////////////

הסט דומה למפה רק שמחזיק מפתחות בלבד
וגם לו יש את האובייקט המוחלש שמאחסן אובייקטים בלי לשמור עליהם בחיים 
באובייקט המוחלש שלו ניתן רק לדעת האם אובייקט מסויים שייך לקבוצה וזהו.

את שניהם ניתן להפוך למערך וכך יווצר מהמפה מערך של מערכים ומהסט מערך רגיל
דוגמא לשימוש אם רוצים לקחת ממערך את הערכים הייחודיים שלו בלי כפילויות

///////////////////////////////////////////////////////////////////
/////////////////            Callback       ///////////////////////
///////////////////////////////////////////////////////////////////

פונקציה שמועברת כפרמטר לפונקציה אחרת , היא מאפשרת לתוכנית להמשיך לעבוד כרגיל ומונעת חסימה
הפונקציה הזו תיקרא רק בעקבות טריגר מסויים
האסינכורניות מסתמכת על ההתקשרות החוזרת


///////////////////////////////////////////////////////////////////
/////////////////            Method          //////////////////////
///////////////////////////////////////////////////////////////////

https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch


POST / PUT
fetch('https://example.com/profile', {
  method: 'POST', // or 'PUT'
  headers: {
    'Content-Type': 'application/json',
  },
  body: JSON.stringify(data),
})

// GET -
const response = await fetch(fileURL);

// DELETE - without data

/////////////////////////////////////////////////////////////////////
//////////////////            Promises          /////////////////////
/////////////////////////////////////////////////////////////////////

async function *issLocations() {
    while(true) {
        yield $.get('http://api.open-notify.org/iss-now.json');
        await asleep(1000);
    }
}

async function showLocationsInFields() {
    const lat_field = document.querySelector('#lat-field');
    const long_field = document.querySelector('#long-field');
    for await (let data of issLocations()) {
        const {iss_position: {longitude , latitude} } = data;
        lat_field.value = latitude;
        long_field.value = longitude;
    }
}

showLocationsInFields();

//////////////////            Promises  2       /////////////////////


const promises = [];
const images = document.querySelectorAll('img');
for(let img of images) {
    const p = new Promise((resolve , reject)=>{
        img.addEventListener('load'  , resolve);
        img.addEventListener('error' , reject);
    });
    promises.push(p);
}

Promise.all(promises).then(allImagesLoaded).catch(function(e) {
    console.log('error loading image: ' + e.target.src);
});

```
```JS

/////////////////////////////////////////////////////////////////////
////////////////            איטיות באתר          ///////////////////
/////////////////////////////////////////////////////////////////////

1.) תלוי במקום ששם מאוחסן האתר שלי.
    הרבה פעמים מחפשים דוקא שירות איחסון זול , והזולים נמצאים ע"פ רב בארה"ב, כך שאם רב הגולשים באתר הם מישראל, 
    עדיף שיהיה מאוחסן בישראל או לכל הפחות שירות אירופי שקרוב,  על מנת להבטיח מהירות סבירה.
2.) סקריפטים חיצוניים עלולים לגרום לאיטיות, סרטון מוטמע מיוטיוב עלול להיות איטי,
    בעצם כל עם שמזינים קוד חיצוני באתר - גורמים לכך ההדפדפן של הלקוח צריך לבקש את המידע מאותו אתר חיצוני, בנוסף לכל המידע שהוא צריך מהאתר שלכם.
   - ככל שקוראים הרבה למשאבים חיצוניים כך אורך הרבה זמן הטעינה. ולכן צריך בקריאות שרת לחשוב כל הזמן על יעילות.
3.) אתר שלא מתוחזק עלול לגרום לאיטיות , כמו למשל סקריפט שקורא למשהו שכבר לא קיים. או גישה לפונט שנמצא היום בתיקיה אחרת.
     אם למשל היה פעם צורך לטעון סקריפט למשהו מסויים ולאחר זמן מנה שינו אותו ולא משתמשים יותר בסקריפט ההוא אז עצם הטעינה כבדה וצריך לזכור למחוק אותה גם מהתלויות.
4.) תמונות כבדות מידי, אם עלתה בטעות תמונה בגודל מגה בייט במקום קילובייט, בכלל עדיף להשתמש כמה שאפשר היום בתמונה שיוצרים בקוד ויש הרבה כאלה מוכנים ברשת רק להעתיק את הקוד ולהדביק - SVG
5.) אם מבקשים פונט שונה עבור כלא למנט או שיש אפקטים מיותרים אנימתיות מיותרות, 

6.) תמיד כדאי לבדוק יעילות גם בסיבוכיות זמן ריצה, תלוי כמה זה כבד.
7.) כי כאשר יש לך הצהרת 
    CSS 
    לפני תחילת 
    <body>
     הסגנונות שלך למעשה נטענו כבר.
     אז מהר מאוד משתמשים רואים שמשהו מופיע על המסך שלהם (למשל צבעי רקע). 
     אם לא, משתמשים רואים מסך ריק למשך זמן מה לפני שה- 
     CSS מגיע למשתמש.
     JS-כיון שקודם הדפדפן מריץ את ה

```
```JS

/////////////////////////////////////////////////////////////////////
////////////////            באג שהיה לי          ///////////////////
/////////////////////////////////////////////////////////////////////

dispatch -  היה פעם שבניתי את הרידאקס הכל היה נראה תקין ומשום מה אחרי 
reducers - הקומפוננטה לא התעדכנה , שמתי דיבאגרים וראיתי שבכלל לא מגיע ל
הזה  action - ולכן הוא בלע את ה next - ואז שמתי דיבאגר במידדלאוור וראיית שלשם כן מגיע, עד שקלטתי שלא שמתי לו 

בעקבות זה הלך לי בקלות לפתור באג דומה בצד שרת שהיה לי פעם
!יש לו מידדלוורס וצריך לזכור תמיד להפעיל נקסט במקרה שאני רוצה שימשיך לטפל בבקשה node.js דבר כזה עלול לקרות גם בכתיבת שרת 


/////////////////////////////////////////////////////////////////////
////////////////            Single thread         ///////////////////
/////////////////////////////////////////////////////////////////////

יש את המחסנית של הקריאות , היא עוברת שורה שורה בקוד ומבצעת אותו,
כאשר נתקלת בפעולה אסינכרונית היא שולחת את הפעולה ל
- WEB Apis
- שם מצטברות כל הפעולות האסינכרויות.
כאשר יש שם פעולה שמסתיימת, ה 
WEB apis -  
מעביר אותה לתור של ה
-callbacks.
שם התור שולח אחד אחד לפי הסדר שוב חזרה למחסנית של הקריאות שתבצע את הפעולה שבאה לאחר סיום ההמתנה.

```