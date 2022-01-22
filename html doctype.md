# Basic HTML5 Template: Use This HTML Boilerplate as a Starter for Any Web Dev Project

![Jessica Wilkins](https://www.freecodecamp.org/news/content/images/size/w100/2021/05/jessica-wilkins-gravatar.jpeg)

[Jessica Wilkins](https://www.freecodecamp.org/news/author/jessica-wilkins/)

![Basic HTML5 Template: Use This HTML Boilerplate as a Starter for Any Web Dev Project](https://www.freecodecamp.org/news/content/images/size/w2000/2021/07/jackson-so-_t-l5FFH8VA-unsplash.jpg)


عندما تقوم بإنشاء موقع ويب جديد ، من المهم أن يكون لديك بداية تم تأسيسها بشكل جيد. في هذه المقالة ، سأشرح ما هو النموذج المعياري الافتراضي ل HTML 5  وكيفية إنشاء قالب أساسي لاستخدامه في مشاريعك.
## ما هو النموذج المعياري ل  HTML 5 ؟

طبقا ل  [Wikipedia](https://en.wikipedia.org/wiki/Boilerplate_code#HTML),

> **boilerplate code**  او فقط  **boilerplate**  هي أقسام من الكود البرمجي تتكرر في أماكن متعددة مع اختلاف بسيط أو معدوم.

النموذج المعياري في HTML هو نموذج ستضيفه في بداية مشروعك. يجب عليك إضافة هذا النموذج المعياري إلى جميع صفحات HTML الخاصة بك
## مثال على نماذج HTML 5 المعيارية

دعنا نلقي نظرة على مثال أساسي.
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>HTML 5 Boilerplate</title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
	<script src="index.js"></script>
  </body>
</html>
```

### ما هو DOCTYPE ؟


يجب أن يكون السطر الأول في كود HTML الخاص بك هو إعلان DOCTYPE. يخبر DOCTYPE المتصفح بإصدار HTML الذي تمت كتابة الصفحة به

```html
<!DOCTYPE html>
```

إذا نسيت تضمين هذا السطر من الكود في ملفك ، فقد لا يدعم المستعرض بعض علامات HTML 5 مثل `<header>` و `< footer >` و `<article>`. 
### ما هو عنصر root ؟

العلامة `<html>` هي العنصر الأعلى لملف HTML. ستقوم بوضع علامتي `<html>` و  `<body>` بداخلها

```html
<!DOCTYPE html>
<html lang="en">
  <head></head>
  <body></body>
</html>
```

تحدد السمة `lang` داخل علامة ` <html> ` اللغة التي ستستخدمها الصفحة. من الجيد أيضًا تضمينه لأسباب تتعلق بإمكانية الوصول الخاصة بذوي الاحتاياجات الخاصة ، لأن برامج قراءة الشاشة ستعرف عن طريقها كيفية نطق النص بشكل صحيح.
### ما هو head ؟

تحتوي علامات `<head>` على معلومات تتم معالجتها بواسطة أجهزة الحاسب. داخل علامات `<head>` ستقوم بوضع البيانات الوصفية وهي البيانات التي تصف المستند للجهاز.

```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>HTML 5 Boilerplate</title>
    <link rel="stylesheet" href="style.css">
</head>
```

### ما هو ترميز أحرف UTF-8؟
UTF-8 هو ترميز الأحرف القياسي الذي يجب أن تستخدمه في صفحات الويب الخاصة بك. ستكون هذه عادةً أول علامة `<meta>` تظهر في عنصر `<head>`.

```html
 <meta charset="UTF-8">
```

طبقا ل  [World Wide Web Consortium](https://www.w3.org/International/questions/qa-choosing-encodings),
 
> يمكن أن يدعم ترميز المستند إلى Unicode مثل UTF-8 العديد من اللغات ويمكنه استيعاب الصفحات والنماذج في أي مزيج من هذه اللغات. يلغي استخدامه أيضًا الحاجة إلى استخدام اكواد من جانب الخادم لتحديد ترميز الأحرف بشكل فردي لكل صفحة يتم عرضها أو كل كود وارد من نموذج في الصفحة.

### ما هي  viewport ؟
تقوم هذه العلامة بضبط عرض الصفحة بنفس العرض الخاص بشاشة الجهاز. إذا كان لديك جهاز يبلغ عرضه شاشته 600 بكسل ، فسيكون عرض نافذة المتصفح أيضًا 600 بكسل.

يتحكم initial-scale في مستوى التكبير / التصغير.  وضع قيمة 1 ل initial-scale تمنع التكبير الافتراضي بواسطة المتصفحات.
```html
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

```

### ماذا يعني متوافق مع X-UA-compatible ؟
تحدد علامة `<meta>` وضع المستند لبرنامج Internet Explorer . أعلى وضع مدعوم هو `IE=edge` 


```html
    <meta http-equiv="X-UA-Compatible" content="ie=edge">

```

### ما هي علامه title؟

العلامة `<title>` هي عنوان صفحة الويب. يظهر هذا النص في شريط عنوان المتصفح.
```html
    <title>HTML 5 Boilerplate</title>

```

![](https://www.freecodecamp.org/news/content/images/2021/07/Screen-Shot-2021-07-30-at-4.15.25-AM.png)

### CSS stylesheet
سيربط هذا الرمز `"rel=stylesheet"` التعديلات الخاصة بك في CSS بصفحة HTML. وتحدد العلاقة بين ملف HTML وأوراق الأنماط stylesheet الخارجية

```html
    <link rel="stylesheet" href="style.css">

```

### علامة script 

سيتم وضع علامه script لربط الاكواد الخارجية قبل علامة نص النهاية مباشرةً. هذا هو المكان الذي يمكنك فيه ربط كود JavaScript الخارجي الخاص بك

```html
	<script src="index.js"></script>

```

## الخلاصة
يجب عليك إضافة نموذج HTML 5 المعياري إلى كل صفحة من صفحات HTML الخاصة بك. يحتوي هذا الكود الاولي على معلومات مهمة مثل نوع المستند والبيانات الوصفية وأوراق الأنماط الخارجية stylesheets وعلامات script.