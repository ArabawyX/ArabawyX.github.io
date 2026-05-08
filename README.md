<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>أسس التغذية والاقتصاد المنزلي | Xs.boda</title>
    
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Amiri:ital,wght@0,400;0,700;1,400&family=Cairo:wght@300;400;600;900&family=Great+Vibes&display=swap');

        /* المتغيرات اللونية لتسهيل التحكم بالتصميم */
        :root {
            --primary-dark: #0f172a;
            --primary-light: #1e293b;
            --gold-accent: #fbbf24;
            --green-accent: #27ae60;
            --blue-accent: #2c5f78;
            --blue-light: #d9e8ef;
            --orange-accent: #e67e22;
            --bg-color: #f8fafc;
            --text-main: #333;
        }

        /* الإعدادات العامة */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Cairo', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-main);
            line-height: 1.6;
        }

        /* =============================
           1. تصميم الترويسة (الهيدر)
        ============================= */
        .main-header {
            background: linear-gradient(135deg, var(--primary-light) 0%, var(--primary-dark) 100%);
            color: white;
            padding: 60px 20px;
            text-align: center;
            border-bottom: 5px solid var(--gold-accent);
        }

        .brand-name {
            font-family: 'Great Vibes', cursive;
            font-size: clamp(3rem, 8vw, 4.5rem);
            color: var(--gold-accent);
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            direction: ltr;
        }

        .course-name {
            font-weight: 300;
            font-size: clamp(1.2rem, 4vw, 1.8rem);
            letter-spacing: 1px;
            opacity: 0.9;
        }

        .separator {
            width: 80px;
            border: 1px solid var(--gold-accent);
            margin: 30px auto;
        }

        .students-section h3 {
            font-weight: 900;
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: #f8fafc;
        }

        .students-list {
            list-style: none;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            max-width: 900px;
            margin: 0 auto;
        }

        .students-list li {
            font-family: 'Amiri', serif;
            font-size: 1.2rem;
            background: rgba(255, 255, 255, 0.05);
            padding: 10px;
            border-radius: 8px;
            transition: transform 0.3s ease, background 0.3s;
        }

        .students-list li:hover {
            transform: translateY(-5px);
            background: rgba(251, 191, 36, 0.15);
            color: var(--gold-accent);
        }

        /* =============================
           2. الحاوية المشتركة للمحتوى
        ============================= */
        .container {
            max-width: 900px;
            margin: 40px auto;
            background: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.05);
            width: 90%;
        }

        /* =============================
           3. قسم أسس التغذية
        ============================= */
        .section-title-nutrition {
            text-align: center;
            color: var(--primary-dark);
            border-bottom: 3px solid var(--green-accent);
            padding-bottom: 10px;
            margin-bottom: 30px;
        }

        .sub-title {
            background-color: var(--green-accent);
            color: white;
            padding: 10px 15px;
            border-radius: 5px;
            margin: 30px 0 15px;
            font-weight: 600;
        }

        details {
            background: #fff;
            margin-bottom: 10px;
            padding: 12px;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
            border: 1px solid #eee;
            transition: all 0.3s ease;
        }

        summary {
            font-weight: bold;
            cursor: pointer;
            outline: none;
            list-style: none;
            color: var(--blue-accent);
            display: flex;
            align-items: center;
        }

        summary::-webkit-details-marker { display: none; }
        summary::before {
            content: "➕";
            margin-left: 10px;
            font-size: 0.9em;
        }
        details[open] summary::before { content: "➖"; }
        
        details[open] { border-right: 5px solid var(--green-accent); }

        .details-content {
            padding: 15px 15px 0 15px;
            border-top: 1px solid #eee;
            margin-top: 10px;
        }

        .highlight { color: #d35400; font-weight: bold; }
        ul { padding-right: 20px; list-style-type: square; }
        li { margin-bottom: 8px; }

        /* =============================
           4. قسم الخميرة والبيتزا
        ============================= */
        .yeast-header {
            text-align: center;
            background-color: var(--blue-accent);
            color: white;
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 30px;
        }

        .yeast-section {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 30px;
            padding: 20px;
            border-bottom: 2px solid var(--blue-light);
            align-items: center;
        }

        .yeast-section:last-child { border-bottom: none; }

        .yeast-content {
            flex: 1;
            min-width: 250px;
        }

        .image-card {
            flex: 1;
            min-width: 250px;
            min-height: 200px;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .image-card .content-image {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .yeast-content h2 { 
            color: var(--blue-accent); 
            border-right: 5px solid var(--orange-accent); 
            padding-right: 10px; 
            margin-bottom: 15px;
        }
        
        .formula {
            background: #eee;
            padding: 10px;
            border-radius: 5px;
            font-family: 'Courier New', Courier, monospace;
            direction: ltr;
            text-align: center;
            font-weight: bold;
            margin: 10px 0;
            overflow-x: auto;
        }

        .tag {
            display: inline-block;
            background: var(--orange-accent);
            color: white;
            padding: 4px 12px;
            border-radius: 5px;
            font-size: 0.85em;
            margin-bottom: 10px;
            font-weight: bold;
        }

        /* =============================
           5. التوافق مع الهواتف المحمولة
        ============================= */
        @media (max-width: 768px) {
            .container { padding: 15px; margin: 20px auto; width: 95%; }
            .yeast-section { flex-direction: column; text-align: center; }
            .yeast-content h2 { border-right: none; border-bottom: 3px solid var(--orange-accent); padding-bottom: 10px; display: inline-block;}
            ul, ol { text-align: right; }
            .image-card { width: 100%; }
        }
    </style>
</head>
<body>

    <header class="main-header">
        <h1 class="brand-name">Xs.boda</h1>
        <h2 class="course-name">أسس التغذية / الاقتصاد المنزلي</h2>
        <hr class="separator">
        <div class="students-section">
            <h3>إعداد الطلاب</h3>
            <ul class="students-list">
                <li>عبدالرحمن مصطفى عويس</li>
                <li>عمر محسن عبد العزيز</li>
                <li>علي عباس علي</li>
                <li>صبري حاتم صبري محمد</li>
                <li>هنا محمود مصطفي محمد</li>
                <li>منه رجب عبد التواب</li>
                <li>هدير احمد مصطفي</li>
                <li>ياسمين ابراهيم احمد</li>
                <li>فاطمه فايز منصور</li>
                <li>منه الله وليد فاروق</li>
            </ul>
        </div>
    </header>

    <main class="container">
        <h1 class="section-title-nutrition">📚 ملخص منهج أسس التغذية - الفرقة الأولى</h1>

        <h2 class="sub-title">الجزء الأول: المفاهيم الأساسية</h2>

        <details>
            <summary>1. مقدمة في علم التغذية</summary>
            <div class="details-content">
                <p><strong>الغذاء:</strong> المادة التي يتناولها الكائن الحي.</p>
                <p><strong>التغذية:</strong> العمليات التي يحول بها الجسم الغذاء إلى طاقة وأنسجة.</p>
                <p><strong>العناصر الغذائية:</strong> المواد الكيميائية في الطعام (كربوهيدرات، بروتينات، إلخ).</p>
                <p><strong>الحالة الغذائية:</strong> حالة الجسم نتيجة لما يتناوله ومدى استفادته منه.</p>
            </div>
        </details>

        <details>
            <summary>2. العناصر الغذائية الكبرى (Macronutrients)</summary>
            <div class="details-content">
                <p><strong>الكربوهيدرات:</strong> المصدر الرئيسي للطاقة (سكريات، نشويات، ألياف).</p>
                <p><strong>البروتينات:</strong> أحجار البناء، بناء العضلات وترميم الأنسجة.</p>
                <p><strong>الدهون:</strong> مصدر مركز للطاقة، وامتصاص الفيتامينات وحماية الأعضاء.</p>
            </div>
        </details>

        <details>
            <summary>3. العناصر الغذائية الصغرى (Micronutrients)</summary>
            <div class="details-content">
                <p><span class="highlight">الفيتامينات:</span></p>
                <ul>
                    <li>ذائبة في الدهون: (A, D, E, K).</li>
                    <li>ذائبة في الماء: (مجموعة B، وفيتامين C).</li>
                </ul>
                <p><strong>الأملاح المعدنية:</strong> الكالسيوم، الحديد، الفسفور، واليود.</p>
            </div>
        </details>

        <details>
            <summary>4. الماء</summary>
            <div class="details-content">
                <ul>
                    <li>تنظيم درجة حرارة الجسم.</li>
                    <li>نقل العناصر الغذائية والتخلص من الفضلات.</li>
                    <li>وسط للتفاعلات الكيميائية داخل الخلايا.</li>
                </ul>
            </div>
        </details>

        <details>
            <summary>5. عمليات التمثيل الغذائي (Metabolism)</summary>
            <div class="details-content">
                <p><strong>الهضم:</strong> تحويل الطعام من صورة معقدة إلى بسيطة.</p>
                <p><strong>الامتصاص:</strong> انتقال الغذاء من الأمعاء إلى الدم.</p>
                <p><strong>التمثيل (الأيض):</strong> استغلال العناصر في الطاقة أو البناء.</p>
            </div>
        </details>

        <h2 class="sub-title">الجزء الثاني: التعمق الفني</h2>

        <details>
            <summary>1. الكربوهيدرات (الوقود الحيوي)</summary>
            <div class="details-content">
                <p><strong>سكريات أحادية:</strong> جلوكوز (سكر الدم)، فركتوز (سكر الفاكهة).</p>
                <p><strong>سكريات ثنائية:</strong> سكروز (سكر المائدة)، لاكتوز (سكر الحليب).</p>
                <p><strong>سكريات معقدة:</strong> النشا، الجليكوجين، والألياف الضرورية للأمعاء.</p>
            </div>
        </details>

        <details>
            <summary>2. البروتينات (المعمار الهيكلي)</summary>
            <div class="details-content">
                <p>تتكون من <strong>أحماض أمينية</strong>:</p>
                <ul>
                    <li>أحماض أساسية: لا يصنعها الجسم (مثل المصادر الحيوانية).</li>
                    <li>أحماض غير أساسية: يستطيع الجسم تصنيعها.</li>
                </ul>
                <p class="highlight">💡 نصيحة: فكرة "التكامل الغذائي" (مثل الفول مع الخبز).</p>
            </div>
        </details>

        <details>
            <summary>3. الطاقة والقيمة الحرارية (السعرات)</summary>
            <div class="details-content">
                <ul>
                    <li>1 جرام كربوهيدرات = 4 سعرات.</li>
                    <li>1 جرام بروتين = 4 سعرات.</li>
                    <li>1 جرام دهون = 9 سعرات.</li>
                </ul>
            </div>
        </details>

        <details>
            <summary>4. الفيتامينات وأعراض النقص</summary>
            <div class="details-content">
                <ul>
                    <li><strong>فيتامين A:</strong> نقصه يسبب العشى الليلي.</li>
                    <li><strong>فيتامين D:</strong> نقصه يسبب الكساح ولين العظام.</li>
                    <li><strong>فيتامين C:</strong> نقصه يسبب الإسقربوط.</li>
                    <li><strong>B12:</strong> ضروري للأعصاب والأنيميا.</li>
                </ul>
            </div>
        </details>

        <details>
            <summary>كيف تضمن الدرجة النهائية؟</summary>
            <div class="details-content">
                <ul>
                    <li>استخدام الرسوم التخطيطية لمسار الهضم.</li>
                    <li>عمل جداول مقارنة بين الدهون المشبعة وغير المشبعة.</li>
                    <li>التدرب على معادلات حساب السعرات.</li>
                </ul>
            </div>
        </details>
    </main>

    <main class="container">
        <div class="yeast-header">
            <h1>دليل المذاكرة الشامل: الخميرة والبيتزا</h1>
            <p>خطة تعليمية تفصيلية لمكونات وعمليات العجين</p>
        </div>

        <div class="yeast-section">
            <div class="yeast-content">
                <span class="tag">القسم الأول</span>
                <h2>أساسيات الخميرة</h2>
                <p><strong>التعريف:</strong> كائنات دقيقة غنية بفيتامين B المركب والبروتينات.</p>
                <p><strong>الأنواع:</strong></p>
                <ul>
                    <li><strong>خميرة بيرة طازجة:</strong> سريعة المفعول، رطوبة عالية، تحتاج اختبار فوران.</li>
                    <li><strong>خميرة بيرة جافة:</strong> حبيبات، صلاحية أطول، تفعيل مختلف.</li>
                </ul>
            </div>
            <div class="image-card">
                <img src="https://image_generation_service.com/p/yeast_baker_photo.jpg" alt="Types of Yeast and Baker Kneading" class="content-image">
            </div>
        </div>

        <div class="yeast-section">
            <div class="image-card">
                [صورة مخطط <br> الدفء/الغذاء/الرطوبة]
            </div>
            <div class="yeast-content">
                <span class="tag">القسم الثاني</span>
                <h2>الظروف المناسبة والكيمياء</h2>
                <p>تحتاج الخميرة للنمو: <strong>الغذاء، الرطوبة، والدفء.</strong></p>
                <p>المعادلة الكيميائية للتخمير:</p>
                <div class="formula">
                    Sucrose -> Glucose -> Fructose -> Alcohol + CO2
                </div>
                <p>ينتج غاز CO2 وهو المسؤول عن رفع العجين.</p>
            </div>
        </div>

        <div class="yeast-section">
            <div class="yeast-content">
                <span class="tag">القسم الثالث</span>
                <h2>صنع البيتزا والطرق</h2>
                <ul>
                    <li><strong>الطريقة البطيئة:</strong> تخمير متعدد، أفضل قوام.</li>
                    <li><strong>الطريقة المعتدلة:</strong> توقيت متوسط.</li>
                    <li><strong>الخلط العنيف:</strong> سريعة، خلط أولي أقل.</li>
                </ul>
                <p><strong>المقادير:</strong> دقيق، ملح، زيت، خميرة، سكر، حليب، بيضة.</p>
            </div>
            <div class="image-card">
                [صورة أيقونات المقادير <br> دقيق/زيت/بيض]
            </div>
        </div>

        <div class="yeast-section">
            <div class="image-card">
                [صورة مراحل <br> تضاعف حجم العجين]
            </div>
            <div class="yeast-content">
                <span class="tag">القسم الرابع</span>
                <h2>مراحل نمو وتكاثر الخميرة</h2>
                <ol>
                    <li><strong>مرحلة النشاط:</strong> بداية التفاعل.</li>
                    <li><strong>التخمير الأول:</strong> تضاعف الحجم (Double Volume).</li>
                    <li><strong>التخمير الثاني:</strong> (نصف ساعة).</li>
                    <li><strong>التشكيل:</strong> (3/4 ساعة) مع تجنب زيادة التخمير.</li>
                </ol>
            </div>
        </div>

        <div class="yeast-section">
            <div class="yeast-content">
                <span class="tag">القسم الخامس</span>
                <h2>الخبز والحشو</h2>
                <p>يتم الخبز في <strong>فرن حار</strong> لإيقاف فعل الخميرة وتمدد الغاز.</p>
                <p><strong>التطبيقات:</strong> حشو بالجبن الرومي أو الأنشوجة.</p>
                <p><strong>المكونات الإضافية:</strong> زعتر، زيتون أسود، فلفل، زيت زيتون.</p>
            </div>
            <div class="image-card">
                [صورة الفرن <br> وصورة البيتزا النهائية]
            </div>
        </div>
    </main>

</body>
</html>
