إذا حاولت تثبيت أحدث إصدار من node باستخدام apt-package manager ، فسوف ينتهي بك الأمر بـ ** v10.19.0 **. هذا هو أحدث إصدار في متجر تطبيقات ubuntu ، ولكنه ليس أحدث إصدار تم إصداره من NodeJS.

وهذا لأنه عند إصدار إصدارات جديدة من البرنامج ، قد يستغرق فريق Ubuntu شهورًا للاختبار والتحميل في متجر Ubuntu الرسمي. نتيجة لذلك ، للحصول على أحدث إصدارات أي برنامج ، قد نضطر إلى استخدام حزم خاصة ينشرها المطورون.

في هذه المقالة التعليمية ، ما نريد فعله هو الحصول على ** v12.18.1 ** (LTS - مع دعم طويل المدى) أو ** v14.4 ** من Node. للحصول على أحدث الإصدارات ، يمكننا استخدام إما  nodesource  أو  nvm  (node version manager ). سأوضح لك كيفية استخدامهم.

سيتم تشغيل جميع الأوامر هنا باستخدام Ubuntu CLI / Terminal.

## استخدام NVM - طريقتي المفضلة
أنا أحب nvm لأنه يسمح لي باستخدام إصدارات مختلفة من node لمشاريع مختلفة.
في بعض الأحيان ، قد تتعاون في مشروع مع شخص يستخدم إصدارًا مختلفًا من node وتحتاج إلى تبديل إصدارات node إلى ما يتطلبه المشروع. لهذا ، فإن nvm هو أفضل أداة.

## تثبيت NVM

`curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash`

للتحقق من تثبيت nvm ، اكتب `nvm --version`. إذا حصلت على رقم إصدار مثل `0.35.3` ، فأعلم أن nvm قد تم تثبيته بنجاح.
**أعد تشغيل terminal لتصبح التغييرات سارية المفعول.**

## تثبيت NodeJS

بعد ذلك ، لنقم بتثبيت الإصدار 14.4 من Nodejs.

ما عليك سوى كتابة "install nvm 14.4.0".

يمكنك استخدام أمر مشابه لتثبيت أي إصدار تريده من node ، على سبيل المثال `nvm install 12.18.1`.

يقوم هذا الأمر تلقائيًا بتثبيت  nodejs  بالإضافة إلى أحدث إصدار من npm  الذي هو في `v6.14.5`.

إذا احتجت في أي وقت إلى تبديل إصدارات node ، فيمكنك ببساطة كتابة `nvm use <version-number>` ، على سبيل المثال `nvm use v12.18.1`.

لسرد إصدارات node المختلفة التي قمت بتثبيتها مع nvm ، قم بتشغيل `nvm ls`.
## تثبيت Nodesource

قم بتشغيل الأمر أدناه لإخبار Ubuntu بأننا نريد تثبيت حزمة Nodejs
 من nodesource.

`curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -`

**ملحوظة**  الإصدار 14.4.0 هو أحدث إصدار من Node ولكنه لا يحتوي حاليًا على LTS - دعم طويل الأجل له. لتثبيت أحدث إصدار من Node مع LTS ، قم بتغيير "14" في الأمر أعلاه إلى "12".

قد يُطلب منك إدخال كلمة المرور للمستخدم root. أدخلها واضغط enter.
## تثبيت NodeJS
بمجرد الانتهاء من إعداد Nodesource ، يمكننا الآن تثبيت Nodejs v14.4.

`sudo apt-get install -y nodejs`.

بمجرد الانتهاء ، يمكننا التحقق من تثبيت أحدث إصدار من Node.
ما عليك سوى كتابة `nodejs -v` في terminal الخاصة بك ويجب أن يظهر ` v14.4.0`.

يجب أن يكون لديك npm مثبتًا بشكل تلقائي في هذه المرحلة. للتحقق من إصدار npm لديك ، قم بتشغيل  `npm version`. إذا لم تحصل على شيء يتضمن أحدث إصدار منnpm فيمكنك تحديث npm يدويًا عن طريق تشغيل الأمر التالي:

`npm install -g npm@latest`.

إذا واجهت أي مشكلات مع عدم قدرة npm على التحديث لأنه غير مثبت ، فيمكنك تثبيت npm أولاً باستخدام `sudo apt-get install -y npm` ، ثم قم بتشغيل الأمر أعلاه لتحديثه.

لتشغيل حزم npm معينة ، نحتاج أيضًا إلى تشغيل الأمر أدناه`sudo apt install build-essential`.

وهذا كل شيء!
لديك أحدث إصدارات NodeJS و NPM على جهاز Ubuntu الخاص بك.
اذهب لبناء منتجات رائعة :)
