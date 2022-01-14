# How to undo changes in Git

![Zell Liew](https://www.freecodecamp.org/news/content/images/size/w100/2021/05/zell-liew-gravatar.jpeg)

[Zell Liew](https://www.freecodecamp.org/news/author/zellwk/)

![How to undo changes in Git](https://cdn-media-1.freecodecamp.org/images/0*6JjR02sGP4FgM6zj.png)

قد تعلم بالفعل أن Git يشبه نظام نقطة الحفظ. ما تتعلمه بشكل عام باستخدام Git في البداية هو تعلم كيفية حفظ التغييرات وحفظها في remote repository. لكن كيف يمكنك التراجع عن التغيير والعودة إلى الحالة السابقة؟

هذا ما سنقوم بتغطيته في هذه المقالة.

لقد غطيت محتويات هذه المقالة في مقطع فيديو إذا كنت تحب التعلم بالمشاهدة بدلاً من القراءة.

### تخزين علي الحاسب او  تخزين علي الموقع

يعتبر التراجع عن شيء موجود بالفعل على موقع الانترنت عن بُعد أكثر تعقيدًا. هذا هو السبب في أنك تريد الاحتفاظ بالأشياء في جهازك حتى يتم تأكيدها نوعًا ما.

### أربعة سيناريوهات معروفه

سنغطي السيناريوهات الأربعة الشائعة التالية
1. تجاهل التغييرات المحلية
2. تعديل ال commit السابق
3. التراجع عن commit سابق
4. التراجع عن commit الذي تم دفعه إلى موقع الانترنت

ملاحظة: في لقطات الشاشة أدناه ، استخدمت  GIT clients الخاصة ب [Fork for Mac OS](https://git-fork.com/) . يمكنك أن تفعل الشيء نفسه مع GIT clients الآخرين المشابهين.

#### السيناريو 1: تجاهل التغييرات المحلية

السيناريو الأول هو عندما تكون قد أنشأت بعض التغييرات. لم تقوم بعمل commit لهم بعد. وتريد حذف هذه التغييرات.

لنفترض أننا نريد إنشاء ميزة جديدة. سنقوم بإضافة بعض HTML و CSS إلى المشروع:

```html
<!--In index.html-->
<div class="feature"></div>
```

```css
/* In CSS file */
.feature {
  font-size: 2em; 
  /* Other styles */
}
```

لتجاهل هذه التغييرات:
1. انتقل إلى منطقة التدريج Stage
2. حدد الملفات التي تريد تجاهل التغييرات فيها
3. انقر بزر الماوس الأيمن على الملفات
4. حدد تجاهل التغييرات discard changes

![](https://cdn-media-1.freecodecamp.org/images/0*6JjR02sGP4FgM6zj.png)

#### السيناريو 2: تعديل commit السابق

عندما تقوم بإنشاء commit وفقدت بعض التغييرات وتريد إضافة هذه التغييرات في رسالة commit السابقة.

1. انتقل إلى منطقة التدريج stage
2. تنظيم الملفات  Stage the files to commit
3. انقر فوق خانة الاختيار "تعديل" edit
4. قم بتحرير رسالة commit الخاصة بك
5. commit

![](https://cdn-media-1.freecodecamp.org/images/0*1wkCc2i9X8JWsBz4.png)

#### السيناريو 3: التراجع إلى commit سابق

لديك بالفعل بعض الالتزامات في المستودع المحلي الخاص بك. قررت أنك لا تريد هذه الالتزامات بعد الآن وتريد "تحميل" ملفاتك من حالة سابقة.
1. اذهب الي  the Git History
2.  انقر بزر الماوس الأيمن على commit الذي تريد التراجع عنه
3.  اختار  reset  `branch`  to here

![](https://cdn-media-1.freecodecamp.org/images/0*IwWQ9XZNRmCaVvb8.png)

>ملاحظة: يمكنك فقط إعادة التعيين إلى commit لم يتم رفعه إلى الموقع.

#### السيناريو 4: التراجع revert عن commit الذي تم رفعه إلى الموقع

إذا كان لديك commit تم دفعه إلى branch الموجود علي الموقع ، وأنت بحاجة إلى التراجع عنه.
> تعني reveret التراجع عن التغييرات بإنشاء commit جديد. إذا أضفت سطرًا ، فسيؤدي revert commit  هذا إلى إزالة السطر. إذا قمت بإزالة سطر ، فإن revert commit هذا سيضيف السطر مرة أخرى.

للعودة revert، يمكنك:
1. انتقل إلى تاريخ Git
2. انقر بزر الماوس الأيمن على commit الذي تريد التراجع عنه
3. حدد revert commit
4. تأكد من تحديد "commit the changes".
5. انقر فوق revert

![](https://cdn-media-1.freecodecamp.org/images/0*29rgArX4rXn3aH6x.png)

![](https://cdn-media-1.freecodecamp.org/images/0*fUD5rUESrzaMnbXu.png)

### سيناريوهات أخرى

يحتوي GitHub على مقال مفيد يوضح لك كيفية التراجع عن كل شيء تقريبًا باستخدام Git. سيكون مفيدًا إذا واجهت سيناريوهات أخرى. اقرأها [هنا](https://blog.github.com/2015-06-08-how-to-undo-almost-anything-with-git/).

شكرا للقراءة. هل هذه المقالة تساعدك بأي شكل من الأشكال؟ إذا حدث ذلك ، [ واتمني مشاركتها](http://twitter.com/share?text=Undoing%20changes%20in%20Git%20by%20@zellwk%20?%20&url=https://zellwk.com/blog/git-undo/&hashtags=) قد تساعد شخص ما. شكرا لك!

تم نشر هذه المقالة في الأصل على [my blo](https://zellwk.com/blog/git-undo)g.
اشترك في [النشرة الإخبارية](https://zellwk.com/) إذا كنت تريد المزيد من المقالات لمساعدتك في أن تصبح مطورًا أفضل للواجهة الأمامية.