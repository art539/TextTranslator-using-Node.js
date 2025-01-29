# Text Translator using Google Translation 
مترجم نصوص يترجم أي نص من أي لغة إلى أي لغة أخرى يدعمها جوجل مجانًا.
تم تطوير هذا التطبيق باستخدام Nodejs Express، ويعرض واجهة برمجة تطبيقات REST بعد الترجمة لترجمة النص. 
يتم تعريف تنسيق البيانات التي سيتم إرسالها عبر واجهة برمجة التطبيقات.
فقط قم الاتصال بواجهة برمجة التطبيقات وستعطيك واجهة برمجة التطبيقات النتائج المطلوبة

يستخدم هذا التطبيق MongoDB كقاعدة بيانات للتخزين المؤقت، لذلك إذا استفسرت عن ترجمة تم طلبها منك من قبل، فسيستخدم ذاكرة التخزين المؤقت للإجابة على استعلامك وبالتالي تقليل وقت الاستجابة.

---
## المتطلبات

من أجل التطوير، ستحتاج إلى Node.js.

- #### تثبيت Node

يمكنك تثبيت nodejs وnpm بسهولة باستخدام apt install، فقط قم بتشغيل الأوامر التالية.

      $ sudo apt install nodejs
      $ sudo apt install npm

- #### قم بتشغيل الأمر التالي.

    $ node --version
    v8.11.3

    $ npm --version
    6.1.0


---



#### تثبيت الاعتماديات 

```
npm install
```

## تكوين التطبيق

- يجب إنشاء ملف باسم .env يحتوي على رابط قاعدة البيانات للاتصال بـ mongoose و قم بحفظه.

## تنفيذ المشروع

```
npm start
```

---

## هيكل التطبيق

```
/app.js - This is the main of the app having code of all the API's and app formation and listening and DB connection
/Language DB/ languages.js - This file contains all the languages support by the app and their manipulations.
/Models/ model.js - This contains the schema of cache object 
/Assets - Contains image assets for Readme
```
---

## تنسيق Api

```
نقطة نهاية واجهة برمجة التطبيقات REST هي '/api/translate/'

وتنسيق البيانات التي إرسالها عبر واجهة برمجة التطبيقات في نص واجهة برمجة التطبيقات.

{
    "to" : "chinese simplified",
    "from" : "English",
    "text" : "That person is calling you"
}

where 'to' is the target language
      'from' is language of given text
      'text' is the data to be translated. 

```
