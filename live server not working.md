# Visual Studio Code Live Server Not Working

![Visual Studio Code Live Server Not Working](https://cdn-media-2.freecodecamp.org/w1280/5f9c9941740569d1a4ca1eab.jpg)

VSCode لديه العديد من الاضافات الرائعه, و  [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)  تعتبر من افضلهم.

فقط ببعض النقرات Live Server سيمكنك من عرض صفحاتك في متصفح حقيقي. والاجمل انه سيدعم التعديل الفوري, اي تعديل في الكود سيظهر في المتصفح في الحال.

فقط اضغط بالزر الايمن علي ملف ال HTML الذي تريد عرضه واختار Open with Live Server 

ولكن ماذا اذا توقف ال Live Server عن العمل . ولا يقوم بفتح المتصفح وعرض الصفحه بالشكل الذي تتوقعه. اذا حدث لك هذا , اليك بعض الخطوات التي يمكن تجريبها.
## إعاده تشغيل VSCode

احيانا يكون من الافضل اعادة تشغيل VSCode من البداية.

اولا قم بحفظ ما كنت تعمل عليه. ثم اغلق VSCode , والذي بدورة سيغلق كل الاضافات المحملة عليه.

وبعدها, افتح VSCode وجرب مرة اخري -  اضغط بالزر الايمن علي ملف ال HTML الذي تريد عرضه واختار Open with Live Server

## اعداد المتصفح من أجل Live Server
من الوارد ان تكون الاضافه الخاصة ب  Live Server تعمل بشكل جيد ولكن لم يتم تحديد متصفح افتراضي لنظام التشغيل.

حتي لو لم تقوم بتحديد المتصفح الافتراضي. سيكون من الصعب علي  Live Server تحديد المتصفح الذي تفضل العمل عليه.

اولا , افتح ال Command Pallete  بالضغط علي F1 , ثم اكتب  `Preferences: Open Settings (JSON)` واختار هذه الخاصية. 

افتح بعدها ملف ال `settings.json`  الخاص ب VSCode  

انتقل الي اخر الملف وقم باضافة فاصلة/فارزة/ comma في نهاية الملف ثم قم بنسخ هذا السطر واضافته 
`"liveServer.settings.CustomBrowser": "chrome"`


![](https://www.freecodecamp.org/news/content/images/2020/09/settings-json.gif)

يمكنك استخدام اي متصفح اخر مثل `"firefox"`,  `"safari"` عن طريق تغير القيمة للاعداد المسمي `"liveServer.settings.CustomBrowser"`

واخيرا, احفظ الملف `settings.json` وجرب نشغيل Live Server مرة اخري.


## تعيين المتصفح الافتراضي لنظام التشغيل الخاص بك

حتى بعد إخبار Live Server بالمتصفح الذي تريد استخدامه ، فمن المحتمل أنه لا يزال لا يفتح صفحتك في ذلك المتصفح بشكل صحيح.

الشيء التالي الذي يجب تجربته هو تعيين المتصفح الافتراضي لنظام التشغيل نفسه.

يمكن أن تختلف الطريقة بناءً على نظام التشغيل الخاص بك ، لذلك من الأفضل البحث عن كيفية القيام بذلك إذا لم تكن متأكدًا.

إليك ما تبدو عليه صفحة الإعدادات في Windows:

![](https://www.freecodecamp.org/news/content/images/2020/09/image-56.png)

Credit:  [Advitya-sharma](https://forum.freecodecamp.org/u/Advitya-sharma)

## افتح صفحه ive Server  بنفسك 
إذا كان Live Server لسبب ما لا يزال لا يفتح الصفحة في متصفحك بشكل تلقائي ، فلا داعي للقلق. يمكنك دائمًا فتح المتصفح الذي تختاره وعرض الصفحة مباشرة.

فقط افتح المتصفح المفضل لديك وانتقل إلى `http://127.0.0.1:5500/ <your_file_name>`.

على سبيل المثال ، إذا كان ملفك يسمى `index.html` ، فما عليك سوى الانتقال إلى` http: //127.0.0.1: 5500 / index.html`.

طالما أن Live Server قيد التشغيل ، ستتمكن من أن ترى صفحتك.

## في النهاية
كانت هذه مجموعه من الاصلاحات الشائعه لحل مشكلة تعطل Live Server.

ابقوا امنين. واتمني لكم Live coding سعيد