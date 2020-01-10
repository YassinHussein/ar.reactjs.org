---
id: release-channels
title: قنوات الاصدار
permalink: docs/release-channels.html
layout: docs
category: installation
---

React يعتمد على مجتمع مفتوح المصدر مزدهر لتقديم تقارير الأخطاء وفتح طلبات التغيير، و [عروض "طلب للحصول على تعليقات"](https://github.com/reactjs/rfcs). لتشجيع التعليقات ، نشارك أحيانًا بنيات خاصة من React تتضمن ميزات غير مُصدرة.

> هذا المستند سيكون أكثر ملاءمة للمطورين الذين يعملون على أدوات العمل أو مكتبات أو أدوات التطوير. للمطورين الذين يستخدمون React بشكل أساسي في إنشاء تطبيقات الواجهة الاماميه للمستخدم لا ينبغي عليهم القلق حول النسخ التجريبية الخاصة بنا.

لكل إصدار من React مسارات مصممة لحالة استخدام مختلفة:

- [**الأحدث**](#latest-channel) للإصدارات المستقرة، SemVer(الإدارة الدلالية لنُسخ) اصدارات React. هذا ما تحصل عليه عند تثبيت React من npm. هذه هي القناة التي تستخدمها بالفعل اليوم. **استخدم هذا لجميع تطبيقات React لواجهة المستخدم الاماميه.**
- [**التالى**](#next-channel) تتبع الفرع الرئيسي لمستودع الكود المصدري React. فكر في كل الإصدرات المرشحة للإفراج عنها في الإصدار البسيط التالي. استخدم هذا لاختبار المتكامل بين مشاريع React ومشاريع الجهات الخارجية.
- [**التجريبية**](#release-channel) تتضمن واجهات برمجة التطبيقات التجريبية والميزات التي لا تتوفر في الإصدارات المستقرة. هذه أيضًا تتبع الفرع الرئيسي ، ولكن مع إشارات ميزة إضافية قيد التشغيل. استخدم هذا لتجربة الميزات القادمة قبل إصدارها.

يتم نشر جميع الإصدارات إلى npm ، ولكن يستخدم فقط الأحدث [الإصدار الدلالية](/docs/faq-versioning.html). تشتمل الإصدارات التجريبية (تلك الموجودة في القنوات التالية والقنوات التجريبية) على إصدارات تم توليدها من مزج محتوياتها ، على سبيل المثال `0.0.0-1022ee0ec` و للتالى `0.0.0-experimental-1022ee0ec` للتجريبية.

**قناة الإصدار الوحيدة المدعومة رسميًا للتطبيقات واجهة المستخدم هي الأحدث**. يتم توفير الإصدارات التالية والتجريبية لأغراض الاختبار فقط ، ونحن لا نقدم أي ضمانات بأن السلوك لن يتغير بين الإصدارات. لا يتبعون بروتوكول semver الذي نستخدمه للإصدارات من الأحدث.

من خلال نشر الإصدارات التجريبية على نفس السجل الذي نستخدمه للإصدارات المستقرة ، يمكننا الاستفادة من العديد من الأدوات التي تدعم سير عمل npm ، مثل [unpkg](https://unpkg.com) و [CodeSandbox](https://codesandbox.io).

### أحدث قناة {#latest-channel}

الأحدث هو القناة المستخدمة لإصدارات React مستقرة. يتوافق مع علامة `الأحدث` على npm. إنها القناة الموصى بها لجميع تطبيقات React التي يتم شحنها إلى مستخدمين حقيقيين.

**إذا لم تكن متأكدًا من القناة التي يجب أن تستخدمها ، فهي الأحدث.** إذا كنت من مطوري React ، فهذا ما تستخدمه بالفعل.

يمكنك توقع أن تكون تحديثات "الأحدث" مستقرة للغاية. تتبع الإصدارات مخطط الإصدار الدلالي. تعرف على المزيد حول التزامنا بالاستقرار والهجرة المتزايدة في [سياسة الإصدار](/docs/faq-versioning.html).

### القناة التالية {#next-channel}

القناة التالية هي قناة تجريبية تتعقب الفرع الرئيسي لمستودع React. نستخدم الإصدارات التجريبية في القناة التالية كمرشحين لإصدار القناة الأخيرة. يمكنك التفكير في التالي باعتباره مجموعة فرعية من الأحدث التي يتم تحديثها بشكل متكرر أكثر.

درجة التغيير بين الإصدار التالي الأحدث والأحدث الأحدث تقريبًا هي نفسها التي ستجدها بين إصدارين بسيطين من الفصل. ومع ذلك ، **القناة التالية لا تتوافق مع الإصدار الدلالي.** يجب أن تتوقع تغييرات فاصلة عرضية بين الإصدارات المتتالية في القناة التالية.

**لا تستخدم التجريبية في التطبيقات واجهة المستخدم الاماميه.**

يتم نشر الإصدارات في التالى مع علامة `التالى` على npm. يتم إنشاء الإصدارات من علامة تجزئة لمحتويات البنية ، على سبيل المثال `0.0.0-1022ee0ec`.

#### استخدام القناة التالية فى اختبار التكامل {#using-the-next-channel-for-integration-testing}

تم تصميم القناة التالية لدعم اختبار التكامل بين React والمشاريع الأخرى.

تمر جميع التغييرات التي يتم إجراؤها على React باختبار داخلي شامل قبل إصدارها للجمهور. ومع ذلك ، هناك عدد لا يحصى من البيئات والتكوينات المستخدمة في نظام React البيئي ، وليس من الممكن أن نختبر كل واحد.

إذا كنت مؤلفًا لإطار React أو مكتبة أو أداة مطور أو أي مشروع مشابه من نوع البنية التحتية ، يمكنك مساعدتنا في الحفاظ على React مستقرًا لمستخدميك ومجتمع React بأكمله من خلال تشغيل مجموعة الاختبارات بشكل دوري ضد أحدث إصدار يتغير. إذا كنت مهتمًا ، فاتبع الخطوات التالية:

- قم بإعداد وظيفة [cron](https://ar.wikipedia.org/wiki/%D9%83%D8%B1%D9%88%D9%86_(%D9%8A%D9%88%D9%86%D9%83%D8%B3)) باستخدام نظام التكامل المستمر المفضل لديك. يتم دعم وظائف Cron بواسطة كل من [CircleCI](https://circleci.com/docs/2.0/triggers/#scheduled-builds) و [Travis CI](https://docs.travis-ci.com/user/cron-jobs/).
- في مهمة cron ، حدّث حزم React الخاصة بك إلى أحدث إصدار React في القناة التالية ، باستخدام علامة `next` في npm. باستخدام npm cli:

  ```
  npm update react@next react-dom@next
  ```

  أو yarn:

  ```
  yarn upgrade react@next react-dom@next
  ```
- قم بتشغيل مجموعة الاختبار الخاصة بك مقابل الحزم المحدثة.
- إذا مر كل شيء ، عظيم! يمكنك أن تتوقع أن مشروعك سيعمل مع الإصدار التفاعلي البسيط التالي.
- إذا حدث شيء ما بشكل غير متوقع ، فالرجاء إخبارنا عن طريق [تقديم مشكلة](https://github.com/facebook/react/issues).

المشروع الذي يستخدم سير العمل هذا هو Next.js. (لا يقصد التورية! على محمل الجد!) يمكنك الرجوع إلى [اعدادت CircleCI](https://github.com/zeit/next.js/blob/c0a1c0f93966fe33edd93fb53e5fafb0dcd80a9e/.circleci/config.yml) كمثال.

### قناة تجريبية {#experimental-channel}

مثل التالي ، القناة التجريبية هي قناة تجريبية تتعقب الفرع الرئيسي لمستودع React. بخلاف التالي ، تشتمل الإصدارات التجريبية على ميزات إضافية وواجهات برمجة تطبيقات غير جاهزة للإصدار الأوسع.

عادةً ما يكون التحديث إلى التالي مصحوبًا بتحديث مطابق لـ "تجريبي". تعتمد على مراجعة المصدر نفسها ، ولكنها مبنية باستخدام مجموعة مختلفة من إشارات المعالم.

قد تكون الإصدارات التجريبية مختلفة بشكل كبير عن الإصدارات التالية والأخيرة. **لا تستخدم الإصدارات التجريبية في تطبيقات واجهة المستخدم.** يجب أن تتوقع حدوث تغييرات متكررة بين الإصدارات في القناة التجريبية.

يتم نشر الإصدارات في التجريبية مع العلامة `التجريبية` على npm. يتم إنشاء الإصدارات من علامة تجزئة لمحتويات البنية ، على سبيل المثال `0.0.0-experimental-1022ee0ec`.

#### ما الذي يحدث في الإصدار التجريبي؟ {#what-goes-into-an-experimental-release}

الميزات التجريبية هي الميزات التي ليست جاهزة للإصدارعنها للجمهور الأوسع ، وقد تتغير بشكل كبير قبل الانتهاء منها. قد لا يتم وضع اللمسات الأخيرة على بعض التجارب - والسبب في أن لدينا تجارب هو اختبار صلاحية التغييرات المقترحة.

على سبيل المثال ، إذا كانت القناة التجريبية موجودة عندما أعلنا عن Hooks، فسنقوم بإصدار Hooks إلى القناة التجريبية قبل أسابيع من توفرها في الأحدث.

قد تجد أنه من المفيد إجراء اختبارات التكامل مقابل التجربة التجريبية. هذا متروك لكم. ومع ذلك ، يرجى العلم أن التجريبية أقل استقرارًا من التالي. **نحن لا نضمن أي استقرار بين الإصدارات التجريبية.**

#### كيف يمكنني معرفة المزيد عن الميزات التجريبية؟ {#how-can-i-learn-more-about-experimental-features}

الميزات التجريبية قد تكون أو لا تكون موثقة. عادة ، لا يتم توثيق التجارب حتى تكون قريبة من الشحن في التالي أو مستقر.

إذا لم يتم توثيق إحدى الميزات ، فقد تكون مصحوبة بـ [RFC](https://github.com/reactjs/rfcs).

سننشر على [React blog](/blog) عندما نكون مستعدين للإعلان عن تجارب جديدة ، لكن هذا لا يعني أننا سننشر كل تجربة.

يمكنك دائمًا الرجوع إلى مستودع GitHub العام الخاص بنا [التاريخ](https://github.com/facebook/react/commits/master) للحصول على قائمة شاملة بالتغييرات.