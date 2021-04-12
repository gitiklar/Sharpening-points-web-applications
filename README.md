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
<u><b>היתרונות:</b></u><br>
- לקצר את החוטים הארוכים של הסטייט שמועבר בין אבא לבן עמוק בעץ הפקדים<br>
- קל מאד לראות בכל רגע נתון את המצב של היישום מכל ההיבטים כיון שכל המידע שמור באוביקט אחד דבר שמקל מאד על הדיבוג<br>
- קל לכתוב בדיקות נקיות כאשר כל הלוגיקה מצויה במקום אחד<br>

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
  <h1>ה-flux שלנו הוא redux</h1>
    <p>
    רידאקס זוהי גרסה ספציפית או מימוש ספציפי של ארכיטקטורת פלאקס.<br>
    <h2>הרעיונות המרכזיים של redux</h2>
    1.) ברידאקס יש רק Store אחד. כל המידע שנשמר ב Store הוא Immutable.<br>
    2.) כל פעם שה Store משתנה מכל סיבה שהיא, כל הקומפוננטות במסך ירונדרו מחדש.<br>
    3.) זה לא כל כך נורא כי כל המידע הוא Immutable. לכן באופן אוטומטי נוכל לדלג על Render של קומפוננטות אם המידע שהן תלויות בו לא משתנה.<br>
    4.) בגלל שיש רק Store אחד, ה Store הוא גם ה Dispatcher. הוא מקבל את כל ה Actions ומעדכן את עצמו בהתאם.<br>
  </p>  
</div>