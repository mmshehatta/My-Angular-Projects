
# P3- 15 creating an ingredient model

#### Points:
   We're going to use ingredients a lot in our application,so having a model for it makes sense.
   Now where do we store this ingredient model? , We store it in the recipe model in the recipes folder because it belongs there . feature-wise but where does the ingredient model belong to?
   Well, I believe it belongs in a new folder, the shared folder which I'm going to create in the app folder.
   Shared is a fitting name for this folder because it will contain features or elements of our app which are shared across different features, like the ingredient which we're going to use both in the shopping list and the recipes section.
   ----------------------------------------
   1
00:00:02,520 --> 00:00:05,710
We're going to use ingredients a lot in our application,

2
00:00:05,760 --> 00:00:08,250
so having a model for it makes sense.

3
00:00:08,250 --> 00:00:10,980
Now where do we store this ingredient model?

4
00:00:11,130 --> 00:00:15,180
We store it in the recipe model in the recipes folder because it belongs there

5
00:00:15,180 --> 00:00:20,560
feature-wise but where does the ingredient model belong to?

6
00:00:21,210 --> 00:00:27,540
Well, I believe it belongs in a new folder, the shared folder which I'm going to create in the app folder.

7
00:00:28,050 --> 00:00:36,060
Shared is a fitting name for this folder because it will contain features or elements of our app which

8
00:00:36,060 --> 00:00:42,030
are shared across different features, like the ingredient which we're going to use both in the shopping

9
00:00:42,030 --> 00:00:44,580
list and the recipes section.

10
00:00:44,580 --> 00:00:53,530
So here I'll create a new file and this file will be named ingredient.model.ts. In there,

11
00:00:53,570 --> 00:01:01,940
I will export a class named ingredient and here, we will basically define how an ingredient should look like.

12
00:01:01,940 --> 00:01:09,980
Now how should it look like? It should have a name, so publicly available, which is a string and an

13
00:01:09,980 --> 00:01:10,470
amount,

14
00:01:10,470 --> 00:01:13,850
so how many items of that type should we have.

15
00:01:13,970 --> 00:01:14,660
So maybe

16
00:01:14,660 --> 00:01:17,880
amount here which would be of type number.

17
00:01:18,350 --> 00:01:24,950
Now in the constructor, we of course want to be able to receive that as arguments, name and amount

18
00:01:25,580 --> 00:01:32,420
and then assign it here as before, so this name here equals name and this amount equals amount.

19
00:01:32,420 --> 00:01:37,940
Now that is such a typical set up, that we receive the arguments we want to assign in the constructor

20
00:01:37,940 --> 00:01:42,630
and that instantly assign them, that TypeScript offers a shortcut.

21
00:01:42,890 --> 00:01:50,120
We can get rid of the declaration of our properties up here and get rid of the content in the body

22
00:01:50,120 --> 00:01:58,700
of this constructor and simply add an accessor in front of the property name here, so public in front

23
00:01:58,700 --> 00:02:00,770
of both arguments.

24
00:02:00,770 --> 00:02:06,600
What that will do is behind the scenes, it will create the same effect we had before,

25
00:02:06,620 --> 00:02:13,700
so it will automatically give us properties with the names we specify here as argument names, so name

26
00:02:13,700 --> 00:02:14,230
and amount

27
00:02:14,230 --> 00:02:21,470
in this case and it will automatically assign the values we receive in this constructor to these newly

28
00:02:21,470 --> 00:02:22,820
created properties.

29
00:02:22,940 --> 00:02:25,090
So nice and convenient shortcut.

30
00:02:25,730 --> 00:02:28,960
With that, we defined how ingredient should look like,

31
00:02:28,970 --> 00:02:31,210
now we can use it in the shopping list component.

32
00:02:31,340 --> 00:02:33,770
Let's do this in the next lecture.

### Translation
1
00: 00: 02520 -> 00: 00: 05710
سنستخدم المكونات كثيرًا في تطبيقنا ،

2
00: 00: 05760 -> 00: 00: 08250
لذا فإن وجود نموذج لها أمر منطقي.

3
00: 00: 08250 -> 00: 00: 10980
الآن أين نقوم بتخزين نموذج المكون هذا؟

4
00: 00: 11،130 -> 00: 00: 15180
نقوم بتخزينها في نموذج الوصفة في مجلد الوصفات لأنها تنتمي هناك

5
00: 00: 15180 -> 00: 00: 20560
من حيث الميزات ولكن إلى أين ينتمي نموذج المكوِّن؟

6
00: 00: 21210 -> 00: 00: 27540
حسنًا ، أعتقد أنه ينتمي إلى مجلد جديد ، المجلد المشترك الذي سأقوم بإنشائه في مجلد التطبيق.

7
00: 00: 28050 -> 00: 00: 36060
Shared هو اسم مناسب لهذا المجلد لأنه سيحتوي على ميزات أو عناصر من تطبيقنا

8
00: 00: 36،060 -> 00: 00: 42،030
يتم مشاركتها عبر ميزات مختلفة ، مثل المكون الذي سنستخدمه معًا في التسوق

9
00: 00: 42،030 -> 00: 00: 44580
قائمة وقسم الوصفات.

10
00: 00: 44580 -> 00: 00: 53530
لذا سأقوم هنا بإنشاء ملف جديد وسيسمى هذا الملف componentient.model.ts. هناك،

11
00: 00: 53570 -> 00: 01: 01940
سوف أقوم بتصدير فئة باسم المكون وهنا ، سنحدد بشكل أساسي كيف يجب أن يبدو أحد المكونات.

12
00: 01: 01940 -> 00: 01: 09980
الآن كيف يجب أن تبدو؟ يجب أن يكون لها اسم ، بحيث يكون متاحًا للجمهور ، وهو عبارة عن سلسلة و

13
00: 01: 09980 -> 00: 01: 10470
كمية،

14
00: 01: 10470 -> 00: 01: 13850
فكيف يجب أن يكون لدينا عدد العناصر من هذا النوع.

15
00: 01: 13970 -> 00: 01: 14660
لذا ربما

16
00: 01: 14660 -> 00: 01: 17880
المبلغ هنا والذي سيكون من نوع الرقم.

17
00: 01: 18350 -> 00: 01: 24950
الآن في المنشئ ، نريد بالطبع أن نكون قادرين على تلقي ذلك كحجج واسم ومبلغ

18
00: 01: 25580 -> 00: 01: 32420
ثم قم بتعيينه هنا كما كان من قبل ، لذا فإن هذا الاسم هنا يساوي الاسم وهذا المبلغ يساوي المبلغ.

19
00: 01: 32420 -> 00: 01: 37940
الآن هذا إعداد نموذجي ، حيث نتلقى الحجج التي نريد تعيينها في المنشئ

20
00: 01: 37940 -> 00: 01: 42630
والتي تقوم بتعيينها على الفور ، يقدم ذلك TypeScript اختصارًا.

21
00: 01: 42890 -> 00: 01: 50120
يمكننا التخلص من إعلان خصائصنا في الأعلى هنا والتخلص من المحتوى الموجود في الجسم

22
00: 01: 50120 -> 00: 01: 58700
من هذا المُنشئ وإضافة أداة وصول ببساطة أمام اسم الخاصية هنا ، لذا فهي عامة في المقدمة

23
00: 01: 58700 -> 00: 02: 00770
كلا الحجتين.

24
00: 02: 00770 -> 00: 02: 06600
ما سيفعله ذلك هو وراء الكواليس ، وسيخلق نفس التأثير الذي كان لدينا من قبل ،

25
00: 02: 06620 -> 00: 02: 13700
لذلك سيعطينا تلقائيًا خصائص بالأسماء التي نحددها هنا كأسماء وسيطات ، لذا اسم

26
00: 02: 13700 -> 00: 02: 14230
والمبلغ

27
00: 02: 14230 -> 00: 02: 21470
في هذه الحالة وسيقوم تلقائيًا بتعيين القيم التي نتلقاها في هذا المنشئ إلى هذه القيم الجديدة

28
00: 02: 21470 -> 00: 02: 22820
الخصائص التي تم إنشاؤها.

29
00: 02: 22940 -> 00: 02: 25090
اختصار لطيف جدا ومريح.

30
00: 02: 25730 -> 00: 02: 28960
من خلال ذلك ، حددنا كيف يجب أن يبدو المكون ،

31
00: 02: 28970 -> 00: 02: 31210
الآن يمكننا استخدامه في مكون قائمة التسوق.

32
00: 02: 31340 -> 00: 02: 33770
لنفعل هذا في المحاضرة القادمة.






##### Notes:
 * No notes for now!

