<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مقرر الغذاء والتغذية - مشروع شامل</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Amiri:ital,wght@0,400;0,700;1,400&family=Cairo:wght@300;400;600;700;900&family=Great+Vibes&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    
    <style>
        /* المتغيرات العامة للألوان */
        :root {
            /* ألوان قسم الغذاء */
            --main-gold: #d4a373;
            --main-dark: #1a1c1d;
            --soft-bg: #fefae0;
            --accent: #bc6c25;
            
            /* ألوان قسم البيتزا والخميرة */
            --pizza-primary: #2c5f78;
            --pizza-secondary: #d9e8ef;
            --pizza-accent: #e67e22;
        }

        body {
            font-family: 'Cairo', sans-serif;
            background-color: #f4f7f6; /* لون خلفية محايد */
            margin: 0;
            padding: 0;
            color: var(--main-dark);
            line-height: 1.6;
        }

        /* ================= تنسيقات الغلاف (الهيدر) ================= */
        .main-header {
            background: linear-gradient(135deg, #1e293b 0%, #0f172a 100%);
            color: white;
            padding: 60px 20px;
            text-align: center;
            border-bottom: 5px solid #fbbf24;
            margin-bottom: 40px;
        }

        .brand-name {
            font-family: 'Great Vibes', cursive;
            font-size: 4rem;
            color: #fbbf24;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .course-name {
            font-family: 'Cairo', sans-serif;
            font-weight: 300;
            font-size: 1.5rem;
            letter-spacing: 1px;
            opacity: 0.9;
        }

        .separator {
            width: 80px;
            border: 1px solid #fbbf24;
            margin: 30px auto;
        }

        .students-section h3 {
            font-family: 'Cairo', sans-serif;
            font-weight: 900;
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: #f8fafc;
        }

        .students-list {
            list-style: none;
            padding: 0;
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
            transition: transform 0.3s ease;
        }

        .students-list li:hover {
            transform: translateY(-5px);
            background: rgba(251, 191, 36, 0.1);
            color: #fbbf24;
        }

        /* ================= تنسيقات قسم مقرر الغذاء ================= */
        .food-section {
            background-color: var(--soft-bg);
            padding: 40px 20px;
            margin-bottom: 40px;
            border-radius: 15px;
            max-width: 900px;
            margin-left: auto;
            margin-right: auto;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }

        .food-header {
            text-align: center;
            padding: 30px 20px;
            background: var(--main-dark);
            color: var(--main-gold);
            border-radius: 15px;
            margin-bottom: 30px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }

        details {
            background: #fff;
            margin-bottom: 15px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
            border: 1px solid rgba(212, 163, 115, 0.2);
        }

        details[open] {
            box-shadow: 0 8px 15px rgba(0,0,0,0.1);
            transform: translateY(-2px);
        }

        summary {
            padding: 20px;
            font-size: 1.2rem;
            font-weight: 700;
            cursor: pointer;
            list-style: none;
            display: flex;
            justify-content: space-between;
            align-items: center;
            color: var(--accent);
        }

        summary::after {
            content: '\f0fe';
            font-family: "Font Awesome 5 Free";
            font-weight: 900;
            transition: 0.3s;
        }

        details[open] summary::after {
            content: '\f146';
            transform: rotate(180deg);
        }

        .content {
            padding: 0 20px 20px;
            color: #444;
            border-top: 1px dashed var(--main-gold);
            padding-top: 15px;
        }

        .highlight {
            color: var(--accent);
            font-weight: bold;
        }

        /* ================= تنسيقات قسم البيتزا والخميرة ================= */
        .pizza-section {
            background: white;
            padding: 40px;
            border-radius: 15px;
            max-width: 900px;
            margin: 0 auto 50px auto;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }

        .pizza-header {
            text-align: center;
            background-color: var(--pizza-primary);
            color: white;
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 30px;
        }

        .section-row {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 40px;
            padding: 20px;
            border-bottom: 2px solid var(--pizza-secondary);
            align-items: center;
        }

        .section-row:last-child { 
            border-bottom: none; 
        }

        .pizza-content {
            flex: 1;
            min-width: 300px;
        }

        .image-placeholder {
            flex: 0 0 250px;
            height: 200px;
            background-color: var(--pizza-secondary);
            border: 2px dashed var(--pizza-primary);
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 10px;
            color: var(--pizza-primary);
            font-weight: bold;
            text-align: center;
            padding: 10px;
        }

        .pizza-content h2 { 
            color: var(--pizza-primary); 
            border-right: 5px solid var(--pizza-accent); 
            padding-right: 10px; 
        }
        
        .formula {
            background: #eee;
            padding: 10px;
            border-radius: 5px;
            font-family: 'Courier New', Courier, monospace;
            direction: ltr;
            text-align: center;
            font-weight: bold;
            color: #333;
        }

        .tag {
            display: inline-block;
            background: var(--pizza-accent);
            color: white;
            padding: 2px 10px;
            border-radius: 5px;
            font-size: 0.9em;
            margin-bottom: 10px;
        }

        /* تنسيقات عامة للقوائم والفوتر */
        ul, ol { padding-right: 20px; }
        li { margin-bottom: 10px; }

        footer {
            text-align: center;
            padding: 30px;
            font-size: 0.9rem;
            color: #888;
            background: #e9ecef;
        }

        /* شاشات الجوال */
        @media (max-width: 600px) {
            .brand-name { font-size: 2.5rem; }
            .students-list { grid-template-columns: 1fr 1fr; }
            .section-row { flex-direction: column; }
            .image-placeholder { width: 100%; flex: auto; }
        }
    </style>
</head>
<body>

    <header class="main-header">
        <div class="overlay">
            <h1 class="brand-name">XS.Boda</h1>
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
        </div>
    </header>

    <div class="food-section">
        <div class="food-header">
            <i class="fas fa-book-open fa-2x"></i>
            <h2>مقرر اسس الغذاء والتغذية (عملي)</h2>
            <p>كلية التربية النوعية - جامعة عين شمس</p>
        </div>

        <details>
            <summary>١. مكونات الغذاء الأساسية</summary>
            <div class="content">
                يحتاج الجسم لحوالي 45 مادة لبنائه، تتوفر في:
                <ul>
                    <li><span class="highlight">البروتينات:</span> اللبن، البيض، اللحوم، الأسماك، البقول.</li>
                    <li><span class="highlight">الكربوهيدرات:</span> الحبوب، الخبز، البطاطس، السكريات.</li>
                    <li><span class="highlight">الدهون:</span> الزيوت النباتية، الزبد، السمن.</li>
                    <li><span class="highlight">الأملاح والفيتامينات:</span> كالكالسيوم والحديد وفيتامينات (أ، ب، ج، د).</li>
                </ul>
            </div>
        </details>

        <details>
            <summary>٢. قواعد تجهيز الوجبات المثالية</summary>
            <div class="content">
                <ul>
                    <li>مراعاة ميزانية الأسرة وتقديم بدائل اقتصادية.</li>
                    <li>تنسيق الألوان في الوجبة لتكون جذابة وغير مملة.</li>
                    <li>تنوع القوام بين اللين (كالبوريه) والصلب (كالمحمرات) والطازج (كالسلطة).</li>
                    <li>تجنب تكرار الصنف الواحد في الوجبة (مثل تقديم عدة أصناف كلها تحتوي طماطم).</li>
                </ul>
            </div>
        </details>

        <details>
            <summary>٣. أهمية وأثر الطهي على الغذاء</summary>
            <div class="content">
                <p><strong>أهمية الطهي:</strong> يساعد على تكسير ألياف الخضر وتليين نسيج اللحوم لسهولة الهضم، وقتل الميكروبات.</p>
                <p><strong>الأثر على العناصر:</strong></p>
                <ul>
                    <li><span class="highlight">البروتين:</span> يتجمد بالحرارة وينكمش بسبب انفصال العصارات.</li>
                    <li><span class="highlight">النشويات:</span> تتحول بالحرارة الجافة إلى "دكسترين" سهل الهضم وبالرطبة إلى مادة جيلاتينية.</li>
                    <li><span class="highlight">الفيتامينات:</span> فيتامين (ج) هو الأكثر تأثراً بالحرارة وقد يفقد بنسبة 98%.</li>
                </ul>
            </div>
        </details>

        <details>
            <summary>٤. طرق الطهي (الحرارة الرطبة)</summary>
            <div class="content">
                <ul>
                    <li><span class="highlight">السلق:</span> الطهي في ماء مغلي (100°م). يستخدم كمية ماء كبيرة للبقول وقليلة للخضر.</li>
                    <li><span class="highlight">التسبيك:</span> الطهي في سائل محدود في إناء محكم الغطاء تحت درجة الغليان. له ثلاث طرق: (ني x ني)، التسبيك الخفيف، والتسبيك الثقيل.</li>
                    <li><span class="highlight">التشريب:</span> طهي الطعام في كمية قليلة جداً من السائل حتى يتشربه (مثل الأرز).</li>
                    <li><span class="highlight">البخار:</span> طهي الطعام بواسطة بخار الماء الذي تصل حرارته لـ 120°م.</li>
                </ul>
            </div>
        </details>
    </div>

    <div class="pizza-section">
        <div class="pizza-header">
            <h2>دليل المذاكرة الشامل: الخميرة والبيتزا</h2>
            <p>خطة تعليمية تفصيلية لمكونات وعمليات العجين</p>
        </div>

        <div class="section-row">
            <div class="pizza-content">
                <span class="tag">القسم الأول</span>
                <h2>أساسيات الخميرة</h2>
                <p><strong>التعريف:</strong> كائنات دقيقة غنية بفيتامين B المركب والبروتينات.</p>
                <p><strong>الأنواع:</strong></p>
                <ul>
                    <li><strong>خميرة بيرة طازجة:</strong> سريعة المفعول، رطوبة عالية، تحتاج اختبار فوران.</li>
                    <li><strong>خميرة بيرة جافة:</strong> حبيبات، صلاحية أطول، تفعيل مختلف.</li>
                </ul>
            </div>
            <div class="image-placeholder">
                [مكان لصورة: أنواع الخميرة وشكل الخلايا]
            </div>
        </div>

        <div class="section-row">
            <div class="image-placeholder">
                [مكان لصورة: مخطط الدفء/الغذاء/الرطوبة]
            </div>
            <div class="pizza-content">
                <span class="tag">القسم الثاني</span>
                <h2>الظروف المناسبة والكيمياء</h2>
                <p>تحتاج الخميرة للنمو: <strong>الغذاء، الرطوبة، والدفء.</strong></p>
                <p>المعادلة الكيميائية للتخمير:</p>
                <div class="formula">
                    Sucrose &rarr; Glucose &rarr; Fructose &rarr; Alcohol + CO<sub>2</sub>
                </div>
                <p>ينتج غاز ثاني أكسيد الكربون (CO<sub>2</sub>) وهو المسؤول عن رفع العجين.</p>
            </div>
        </div>

        <div class="section-row">
            <div class="pizza-content">
                <span class="tag">القسم الثالث</span>
                <h2>صنع البيتزا والطرق</h2>
                <ul>
                    <li><strong>الطريقة البطيئة:</strong> تخمير متعدد، أفضل قوام.</li>
                    <li><strong>الطريقة المعتدلة:</strong> توقيت متوسط.</li>
                    <li><strong>الخلط العنيف:</strong> سريعة، خلط أولي أقل.</li>
                </ul>
                <p><strong>المقادير:</strong> دقيق، ملح، زيت، خميرة، سكر، حليب، بيضة.</p>
            </div>
            <div class="image-placeholder">
                [مكان لصورة: أيقونات المقادير (دقيق/زيت/بيض)]
            </div>
        </div>

        <div class="section-row">
            <div class="image-placeholder">
                [مكان لصورة: مراحل تضاعف حجم العجين]
            </div>
            <div class="pizza-content">
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

        <div class="section-row">
            <div class="pizza-content">
                <span class="tag">القسم الخامس</span>
                <h2>الخبز والحشو</h2>
                <p>يتم الخبز في <strong>فرن حار</strong> لإيقاف فعل الخميرة وتمدد الغاز.</p>
                <p><strong>التطبيقات:</strong> حشو بالجبن الرومي أو الأنشوجة.</p>
                <p><strong>المكونات الإضافية:</strong> زعتر، زيتون أسود، فلفل، زيت زيتون.</p>
            </div>
            <div class="image-placeholder">
                [مكان لصورة: الفرن وصورة البيتزا النهائية]
            </div>
        </div>
    </div>

    <footer>
        <p>مصمم الصفحة : عبدالرحمن مصطفي ، الناشر : إلــعــربــآوي</p>
    </footer>

</body>
</html>
