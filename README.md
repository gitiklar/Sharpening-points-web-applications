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
  <h1>call לעומת קריאה באמצעות apply קריאה לפונקציה באמצעות</h1>
    <p>
        func.call(arg1 , arg2, arg3); //arg1 for 'this';
    </p>
    <p>
        func.apply(array); ///The first limb for this
    </p>
</div>

<div dir="rtl">
  <h1>מהם הפיצ'רים של ריאקט?</h1>
    <p>
      1.) JSX - JavaScript XML
      JSX הוא הרחבה של - JavaScript. משתמשים בו ב- React כדי לתאר כיצד ממשק המשתמש צריך להראות. על ידי שימוש ב- JSX, אנו יכולים לכתוב מבני HTML באותו קובץ המכיל קוד JavaScript.
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
  <h1>ES6 לעומת ES5</h1>
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
      אירוע זו איזשהי פעולה שמשתמש או מערכת עשויים להפעיל כמו לחיצה הזזת עכבר.
      ב-JSX אנחנו מעבירים את הפונקציה שתיקרא בעקבות הפעולה.
      השמות של האירועים דומים ל-HTML אך ההבדל ביניהם הוא שהשם שבא אחרי ה-on מתחיל באות גדולה, כמו:
      onClick
    </p>
</div>

<div dir="rtl">
  <h1>מה זה אירוע סינטטי בריאקט</h1>
    <p>
        אירועים סינתטיים הם האובייקטים המשמשים כעטפת בין דפדפנים סביב האירוע המקורי של הדפדפן.
          הם משלבים את ההתנהגות של דפדפנים שונים ל- API אחד. זה נעשה כדי לוודא שהאירועים מציגים מאפיינים עקביים בדפדפנים שונים.
      </p>
</div>