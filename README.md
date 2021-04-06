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
    -----------------  Strict Mode  מצב בטוח ------------------ 
 .JavaScript מצב בטוח מבקש מהדפדפן לחפש יותר שגיאות בתוכניות
.מצב זה לא מופעל אוטומטית כדי שקוד ישן יוכל לעבוד

1. Enabling strict mode
    -"use strict";

2. Assignment to global variables

3. Assignemnt to reserved words

4. Octal values
    </p>
</div>
