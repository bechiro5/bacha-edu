# الدستور التربوي والتصميمي الشامل — المربي البشير السعيدي

هذه الوثيقة مرجع ملزم لجميع أدوات الذكاء الاصطناعي (Claude, Gemini, ChatGPT) عند إعداد المذكرات التربوية، الإنفوغرافيك التعليمي، أوراق العمل، والتقييمات وفق المنهج التونسي.

---

## أولاً: اتفاق الباشا الحديدي والأمانة للمحتوى
1. **الهوية التربوية الافتراضية:**
   - المؤسسة: المدرسة الابتدائية الشهبانية
   - إعداد: المربي البشير السعيدي
   - المستوى: السنة الأولى ابتدائي
2. **الأمانة الكاملة للمحتوى الأصلي:**
   - يُمنع منعاً باتاً حذف أي كلمة أو جملة أو سؤال أو نشاط أو مرحلة، أو إضافة أي معلومة غير موجودة في المصدر إلا بطلب صريح.
   - يُمنع إعادة صياغة النص أو تلخيصه أو اختصاره أو تغيير ترتيب الفقرات والأسئلة.
   - يُمنع إدراج الإجابات أو التلميحات التي تكشف الحل في ورقة التلميذ.
3. **سلامة اللغة العربية والتشكيل:**
   - لغة عربية سليمة مع التشكيل الكامل والصحيح (الفتحة، الضمة، الكسرة، السكون، الشدة، التنوين، وأواخر الكلمات).
   - احترام المنهج التونسي والتدرج البيداغوجي ومراحل الدرس دون دمج مرحلتين معاً.

---

## ثانياً: اتفاق RTL الصارم (من اليمين إلى اليسار)
1. جميع العناصر (العناوين، الفقرات، ترقيم التمارين، الجداول، الصناديق، المخططات، الأسهم، والخطوط الزمنية) تبدأ من أقصى اليمين إلى اليسار (`dir="rtl"`).
2. يوضع رقم كل تمرين ورمز المعيار (`معـ 1`، `معـ 2 أ`...) في **أقصى اليمين**، ويأتي نص التعليمات مباشرة إلى يسار الرقم.
3. يُمنع تصميم صفحة عربية بتسلسل بصري يبدأ من اليسار.

---

## ثالثاً: اتفاق التتابع العمودي الصارم (البنية الإلزامية للصفحة)
عند إعداد مذكرة أو إنفوغرافيك أو ورقة عمل أو تقييم، يكون ترتيب الصفحة عمودياً من الأعلى إلى الأسفل حصراً كما يلي:
1. **ترويسة مؤطّرة** أعلى الصفحة.
2. **عنوان المذكرة / الإنفوغرافيك** أسفل الترويسة مباشرة.
3. **التمرين الأول / المرحلة الأولى** بكامل عرض الصفحة.
4. **التمرين الثاني / المرحلة الثانية** تحته مباشرة.
5. **بقية التمارين أو المراحل بالتتابع العمودي** الواحد تلو الآخر.
6. **المساحات المخصصة للإجابة** عند الحاجة.
7. **جدول إسناد الأعداد** (في التقييمات) يوضع مجمّعاً في أسفل الصفحة الأخيرة بعد انتهاء جميع التمارين.

* **قاعدة صارمة (منع الأعمدة المتوازية):** يُمنع منعاً باتاً وضع تمرينين أو مرحلتين جنباً إلى جنب في عمودين متوازيين (`No Multi-Column Layout`).
* **الحد الأقصى:** 6 تمارين في الصفحة الواحدة كحد أقصى. إذا زاد العدد، يُوزع العمل على صفحات متتابعة دون تصغير الخط أو حشر المحتوى.

---

## رابعاً: القالب البرمجي القياسي (HTML/CSS A4) بالتتابع العمودي الإجباري

<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <title>مذكرة تربوية / إنفوغرافيك تعليمي</title>
  <style>
    @page { size: A4 portrait; margin: 10mm; }
    * { box-sizing: border-box; font-family: 'Traditional Arabic', 'Amiri', 'Cairo', sans-serif; }
    body { margin: 0; padding: 0; background: #fff; color: #1a1a1a; direction: rtl; text-align: right; }
    
    /* حاوية الصفحة بالتتابع العمودي الصارم */
    .a4-page { 
      width: 190mm; 
      min-height: 277mm; 
      margin: auto; 
      padding: 8mm; 
      border: 2px solid #1e3a8a; 
      border-radius: 8px;
      display: flex;
      flex-direction: column; /* إجبار التتابع العمودي ومنع التجاور الأفقي */
      gap: 12px;
    }
    
    /* 1. الترويسة الرسمية المؤطرة */
    .header-box { 
      width: 100%;
      display: flex; 
      justify-content: space-between; 
      align-items: center; 
      border: 2px solid #1e3a8a; 
      background: #f0f4ff; 
      padding: 10px 15px; 
      border-radius: 6px; 
      font-weight: bold; 
      font-size: 16px; 
    }
    
    /* 2. عنوان المذكرة أو الإنفوغرافيك */
    .main-title { 
      width: 100%;
      text-align: center; 
      background: #1e3a8a; 
      color: #fff; 
      padding: 8px; 
      border-radius: 6px; 
      font-size: 22px; 
      font-weight: bold; 
    }
    
    /* 3. بطاقات التمارين والمراحل (تأخذ 100% من العرض لمنع وضع تمرينين بجانب بعضهما) */
    .vertical-card { 
      width: 100%; 
      border: 1.5px solid #cbd5e1; 
      border-right: 6px solid #1e3a8a; 
      border-radius: 6px; 
      padding: 12px; 
      background: #ffffff; 
      page-break-inside: avoid; 
    }
    
    .card-header { 
      display: flex; 
      align-items: center; 
      gap: 10px; 
      font-weight: bold; 
      font-size: 18px; 
      color: #1e3a8a; 
      margin-bottom: 8px; 
      border-bottom: 1px dashed #cbd5e1; 
      padding-bottom: 4px; 
    }
    
    /* رمز المعيار أو رقم التمرين في أقصى اليمين */
    .right-badge { 
      background: #dbeafe; 
      color: #1e3a8a; 
      border: 1px solid #1e3a8a; 
      padding: 2px 10px; 
      border-radius: 4px; 
      font-size: 15px; 
      font-weight: bold; 
    }
    
    /* الجداول وجدول إسناد الأعداد أسفل الصفحة */
    table { width: 100%; border-collapse: collapse; margin-top: 8px; font-size: 16px; direction: rtl; }
    th, td { border: 1.5px solid #1e3a8a; padding: 8px; text-align: right; }
    th { background: #e0e7ff; color: #1e3a8a; text-align: center; }
  </style>
</head>
<body>
  <div class="a4-page">
    <!-- 1. الترويسة المؤطرة أعلى الصفحة -->
    <div class="header-box">
      <div>المدرسة الابتدائية الشهبانية<br>المستوى: السنة الأولى ابتدائي</div>
      <div style="text-align: center;">المادة: .........................<br>الموضوع: .........................</div>
      <div style="text-align: left;">إعداد المربي: البشير السعيدي<br>السنة الدراسية: 2026 / 2027</div>
    </div>

    <!-- 2. عنوان المذكرة / الإنفوغرافيك أسفل الترويسة -->
    <div class="main-title">عنوان المذكرة التربوية / الإنفوغرافيك التعليمي</div>

    <!-- 3. المرحلة الأولى / التمرين الأول -->
    <div class="vertical-card">
      <div class="card-header">
        <span class="right-badge">المرحلة 1 / معـ 1</span>
        <span>نص التعليمة أو المرحلة الأولى يوضع هنا إلى يسار الرقم...</span>
      </div>
      <div class="card-content">محتوى النشاط الأول...</div>
    </div>

    <!-- 4. المرحلة الثانية / التمرين الثاني تحته مباشرة بالتتابع العمودي -->
    <div class="vertical-card">
      <div class="card-header">
        <span class="right-badge">المرحلة 2 / معـ 2 أ</span>
        <span>نص التعليمة أو المرحلة الثانية يوضع هنا إلى يسار الرقم...</span>
      </div>
      <div class="card-content">محتوى النشاط الثاني...</div>
    </div>
  </div>
</body>
</html>
