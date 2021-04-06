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



