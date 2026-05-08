<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مشروع مقرر أسس التغذية الشامل</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Amiri:ital,wght@0,400;0,700;1,400&family=Cairo:wght@300;400;600;700;900&family=Great+Vibes&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    
    <style>
        /* ================= المتغيرات العامة للألوان ================= */
        :root {
            /* ألوان الجزء العملي (الغذاء) */
            --food-gold: #d4a373;
            --food-dark: #1a1c1d;
            --food-bg: #fefae0;
            --food-accent: #bc6c25;
            
            /* ألوان الجزء النظري (الأسس) */
            --theory-primary: #27ae60;
            --theory-dark: #2c3e50;
            --theory-light: #e8f8f5;
            --theory-accent: #d35400;

            /* ألوان قسم البيتزا والخميرة */
            --pizza-primary: #2c5f78;
            --pizza-secondary: #d9e8ef;
            --pizza-accent: #e67e22;

            /* عام */
            --bg-color: #f4f7f6;
            --text-color: #333;
        }

        body {
            font-family: 'Cairo', sans-serif;
            background-color: var(--bg-color);
            margin: 0;
            padding: 0;
            color: var(--text-color);
            line-height: 1.7;
        }

        .container {
            max-width: 950px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* ================= 1. تنسيقات الغلاف (الهيدر) ================= */
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
            font-weight: 300;
            font-size: 1.5rem;
            letter-spacing: 1px;
            opacity: 0.9;
            margin-top: 0;
        }

        .separator {
            width: 80px;
            border: 1px solid #fbbf24;
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

        /* ================= التنسيق العام للقوائم المنسدلة (Details) ================= */
        details {
            background: #fff;
            margin-bottom: 15px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
        }

        details[open] {
            box-shadow: 0 8px 15px rgba(0,0,0,0.1);
            transform: translateY(-2px);
        }

        summary {
            padding: 18px 20px;
            font-size: 1.2rem;
            font-weight: 700;
            cursor: pointer;
            list-style: none;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-radius: 10px;
        }

        summary::after {
            font-family: "Font Awesome 5 Free";
            font-weight: 900;
            transition: transform 0.3s ease;
        }

        details[open] summary::after {
            transform: rotate(180deg);
        }

        .content-box {
            padding: 0 20px 20px;
            color: #444;
            padding-top: 15px;
        }

        ul, ol { padding-right: 25px; }
        li { margin-bottom: 8px; }

        /* ================= 2. تنسيقات الجزء النظري ================= */
        .theory-section {
            background-color: white;
            padding: 40px;
            border-radius: 15px;
            margin-bottom: 40px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }

        .theory-header {
            text-align: center;
            color: var(--theory-dark);
            border-bottom: 3px solid var(--theory-primary);
            padding-bottom: 15px;
            margin-bottom: 30px;
        }

        .theory-subtitle {
            background-color: var(--theory-primary);
            color: white;
            padding: 12px 20px;
            border-radius: 8px;
            margin-top: 35px;
            margin-bottom: 20px;
            font-size: 1.3rem;
        }

        .theory-section details { border: 1px solid rgba(39, 174, 96, 0.2); }
        .theory-section details[open] { border-right: 5px solid var(--theory-primary); }
        .theory-section summary { color: var(--theory-dark); }
        .theory-section summary::after { content: '\f067'; color: var(--theory-primary); } /* علامة زائد */
        .theory-section details[open] summary::after { content: '\f068'; } /* علامة ناقص */
        .theory-section .content-box { border-top: 1px solid #eee; }
        .theory-section .highlight { color: var(--theory-accent); font-weight: bold; }

        /* ================= 3. تنسيقات الجزء العملي (الغذاء) ================= */
        .food-section {
            background-color: var(--food-bg);
            padding: 40px;
            border-radius: 15px;
            margin-bottom: 40px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }

        .food-header {
            text-align: center;
            padding: 30px 20px;
            background: var(--food-dark);
            color: var(--food-gold);
            border-radius: 15px;
            margin-bottom: 30px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }

        .food-section details { border: 1px solid rgba(212, 163, 115, 0.3); }
        .food-section summary { color: var(--food-accent); }
        .food-section summary::after { content: '\f0fe'; color: var(--food-gold); } /* أيقونة إضافة */
        .food-section details[open] summary::after { content: '\f146'; }
        .food-section .content-box { border-top: 1px dashed var(--food-gold); }
        .food-section .highlight { color: var(--food-accent); font-weight: bold; }

        /* ================= 4. تنسيقات قسم البيتزا والخميرة ================= */
        .pizza-section {
            background: white;
            padding: 40px;
            border-radius: 15px;
            margin-bottom: 50px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }

        .pizza-header {
            text-align: center;
            background-color: var(--pizza-primary);
            color: white;
            padding: 25px;
            border-radius: 10px;
            margin-bottom: 30px;
        }

        .section-row {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 30px;
            padding: 20px;
            border-bottom: 2px solid var(--pizza-secondary);
            align-items: center;
        }

        .section-row:last-child { border-bottom: none; margin-bottom: 0; }

        .pizza-content { flex: 1; min-width: 300px; }

        .image-placeholder {
            flex: 0 0 250px;
            height: 180px;
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

        .pizza-content h3 { 
            color: var(--pizza-primary); 
            border-right: 5px solid var(--pizza-accent); 
            padding-right: 10px; 
            margin-top: 0;
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
            margin: 15px 0;
        }

        .tag {
            display: inline-block;
            background: var(--pizza-accent);
            color: white;
            padding: 3px 12px;
            border-radius: 5px;
            font-size: 0.85em;
            margin-bottom: 10px;
        }

        /* ================= 5. الفوتر ================= */
        footer {
            text-align: center;
            padding: 30px;
            font-size: 0.95rem;
            color: #666;
            background: #e9ecef;
            border-top: 3px solid #ddd;
        }

        /* شاشات الجوال */
        @media (max-width: 768px) {
            .brand-name { font-size: 3rem; }
            .theory-section, .food-section, .pizza-section { padding: 20px; }
            .section-row { flex-direction: column; }
            .image-placeholder { width: 100%; flex: auto; height: 120px; }
        }
    </style>
</head>
<body>

    <header class="main-header">
        <div class="container">
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

    <div class="container">
        
        <section class="theory-section">
            <div class="theory-header">
                <h2>📚 ملخص منهج أسس التغذية - النظري</h2>
            </div>

            <h3 class="theory-subtitle">الجزء الأول: المفاهيم الأساسية</h3>

            <details>
                <summary>1. مقدمة في علم التغذية</summary>
                <div class="content-box">
                    <p><strong>الغذاء:</strong> المادة التي يتناولها الكائن الحي.</p>
                    <p><strong>التغذية:</strong> العمليات التي يحول بها الجسم الغذاء إلى طاقة وأنسجة.</p>
                    <p><strong>العناصر الغذائية:</strong> المواد الكيميائية في الطعام (كربوهيدرات، بروتينات، إلخ).</p>
                    <p><strong>الحالة الغذائية:</strong> حالة الجسم نتيجة لما يتناوله ومدى استفادته منه.</p>
                </div>
            </details>

            <details>
                <summary>2. العناصر الغذائية الكبرى (Macronutrients)</summary>
                <div class="content-box">
                    <p><strong>الكربوهيدرات:</strong> المصدر الرئيسي للطاقة (سكريات، نشويات، ألياف).</p>
                    <p><strong>البروتينات:</strong> أحجار البناء، بناء العضلات وترميم الأنسجة.</p>
                    <p><strong>الدهون:</strong> مصدر مركز للطاقة، وامتصاص الفيتامينات وحماية الأعضاء.</p>
                </div>
            </details>

            <details>
                <summary>3. العناصر الغذائية الصغرى (Micronutrients)</summary>
                <div class="content-box">
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
                <div class="content-box">
                    <ul>
                        <li>تنظيم درجة حرارة الجسم.</li>
                        <li>نقل العناصر الغذائية والتخلص من الفضلات.</li>
                        <li>وسط للتفاعلات الكيميائية داخل الخلايا.</li>
                    </ul>
                </div>
            </details>

            <details>
                <summary>5. عمليات التمثيل الغذائي (Metabolism)</summary>
                <div class="content-box">
                    <p><strong>الهضم:</strong> تحويل الطعام من صورة معقدة إلى بسيطة.</p>
                    <p><strong>الامتصاص:</strong> انتقال الغذاء من الأمعاء إلى الدم.</p>
                    <p><strong>التمثيل (الأيض):</strong> استغلال العناصر في الطاقة أو البناء.</p>
                </div>
            </details>

            <h3 class="theory-subtitle">الجزء الثاني: التعمق الفني</h3>

            <details>
                <summary>1. الكربوهيدرات (الوقود الحيوي)</summary>
                <div class="content-box">
                    <p><strong>سكريات أحادية:</strong> جلوكوز (سكر الدم)، فركتوز (سكر الفاكهة).</p>
                    <p><strong>سكريات ثنائية:</strong> سكروز (سكر المائدة)، لاكتوز (سكر الحليب).</p>
                    <p><strong>سكريات معقدة:</strong> النشا، الجليكوجين، والألياف الضرورية للأمعاء.</p>
                </div>
            </details>

            <details>
                <summary>2. البروتينات (المعمار الهيكلي)</summary>
                <div class="content-box">
                    <p>تتكون من <strong>أحماض أمينية</strong>:</p>
                    <ul>
                        <li>أحماض أساسية: لا يصنعها الجسم (مثل المصادر الحيوانية).</li>
                        <li>أحماض غير أساسية: يستطيع الجسم تصنيعها.</li>
                    </ul>
                    <p><span class="highlight"><i class="fas fa-lightbulb"></i> نصيحة:</span> فكرة "التكامل الغذائي" (مثل الفول مع الخبز).</p>
                </div>
            </details>

            <details>
                <summary>3. الطاقة والقيمة الحرارية (السعرات)</summary>
                <div class="content-box">
                    <ul>
                        <li>1 جرام كربوهيدرات = 4 سعرات.</li>
                        <li>1 جرام بروتين = 4 سعرات.</li>
                        <li>1 جرام دهون = 9 سعرات.</li>
                    </ul>
                </div>
            </details>

            <details>
                <summary>4. الفيتامينات وأعراض النقص</summary>
                <div class="content-box">
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
                <div class="content-box">
                    <ul>
                        <li>استخدام الرسوم التخطيطية لمسار الهضم.</li>
                        <li>عمل جداول مقارنة بين الدهون المشبعة وغير المشبعة.</li>
                        <li>التدرب على معادلات حساب السعرات.</li>
                    </ul>
                </div>
            </details>
        </section>

        <section class="food-section">
            <div class="food-header">
                <i class="fas fa-utensils fa-2x"></i>
                <h2>مقرر أسس الغذاء والتغذية (العملي)</h2>
                <p>كلية التربية النوعية - جامعة عين شمس</p>
            </div>

            <details>
                <summary>١. مكونات الغذاء الأساسية</summary>
                <div class="content-box">
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
                <div class="content-box">
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
                <div class="content-box">
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
                <div class="content-box">
                    <ul>
                        <li><span class="highlight">السلق:</span> الطهي في ماء مغلي (100°م). يستخدم كمية ماء كبيرة للبقول وقليلة للخضر.</li>
                        <li><span class="highlight">التسبيك:</span> الطهي في سائل محدود في إناء محكم الغطاء تحت درجة الغليان. له ثلاث طرق: (ني x ني)، التسبيك الخفيف، والتسبيك الثقيل.</li>
                        <li><span class="highlight">التشريب:</span> طهي الطعام في كمية قليلة جداً من السائل حتى يتشربه (مثل الأرز).</li>
                        <li><span class="highlight">البخار:</span> طهي الطعام بواسطة بخار الماء الذي تصل حرارته لـ 120°م.</li>
                    </ul>
                </div>
            </details>
        </section>

        <section class="pizza-section">
            <div class="pizza-header">
                <h2>🍕 دليل المذاكرة الشامل: الخميرة والبيتزا</h2>
                <p>خطة تعليمية تفصيلية لمكونات وعمليات العجين</p>
            </div>

            <div class="section-row">
                <div class="pizza-content">
                    <span class="tag">القسم الأول</span>
                    <h3>أساسيات الخميرة</h3>
                    <p><strong>التعريف:</strong> كائنات دقيقة غنية بفيتامين B المركب والبروتينات.</p>
                    <p><strong>الأنواع:</strong></p>
                    <ul>
                  --bg-color: #f1f5f9;      /* خلفية رمادية فاتحة جداً مريحة للعين */
            --card-bg: #ffffff;
            --text-main: #1e293b;
            --text-muted: #64748b;
            --border-color: #e2e8f0;
            --radius: 16px;
            --shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
            --shadow-hover: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
        }

        /* ================= إعدادات عامة ================= */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html { scroll-behavior: smooth; }

        body {
            font-family: 'Cairo', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-main);
            line-height: 1.6;
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* ================= الشريط العلوي (Navbar) ================= */
        .navbar {
            background-color: var(--card-bg);
            box-shadow: 0 1px 3px rgba(0,0,0,0.05);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .nav-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 70px;
        }

        .logo {
            font-family: 'Outfit', 'Cairo', sans-serif;
            font-size: 1.5rem;
            font-weight: 800;
            color: var(--primary);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo span { color: var(--secondary); }

        .nav-links {
            display: flex;
            gap: 25px;
            font-weight: 600;
            color: var(--text-muted);
        }

        /* ================= الهيدر (البانر الرئيسي) ================= */
        .hero {
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-dark) 100%);
            color: white;
            padding: 60px 20px;
            border-radius: 0 0 30px 30px;
            text-align: center;
            margin-bottom: -40px; /* لدمج قسم الطلاب مع الهيدر */
            padding-bottom: 80px;
        }

        .hero h1 { font-size: 2.5rem; margin-bottom: 15px; font-weight: 800; }
        .hero p { font-size: 1.1rem; color: #e2e8f0; max-width: 600px; margin: 0 auto; }
        .hero .badge {
            background: rgba(255, 255, 255, 0.2);
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            display: inline-block;
            margin-bottom: 15px;
        }

        /* ================= قسم الطلاب ================= */
        .team-section {
            background: var(--card-bg);
            border-radius: var(--radius);
            padding: 30px;
            box-shadow: var(--shadow);
            margin-bottom: 50px;
            position: relative;
            z-index: 10;
        }

        .team-header {
            text-align: center;
            margin-bottom: 20px;
            color: var(--primary);
            font-weight: 700;
        }

        .team-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            justify-content: center;
        }

        .team-member {
            background: var(--bg-color);
            color: var(--text-main);
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.95rem;
            font-weight: 600;
            border: 1px solid var(--border-color);
            transition: 0.3s;
        }

        .team-member:hover { background: var(--primary); color: white; border-color: var(--primary); }

        /* ================= البطاقات التعليمية (الأقسام) ================= */
        .section-title {
            text-align: center;
            font-size: 2rem;
            margin-bottom: 40px;
            color: var(--text-main);
            font-weight: 800;
        }

        .course-card {
            background: var(--card-bg);
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            margin-bottom: 40px;
            overflow: hidden;
            display: flex;
            flex-direction: column;
            border: 1px solid var(--border-color);
        }

        .card-header {
            padding: 25px 30px;
            color: white;
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .card-header h2 { font-size: 1.5rem; margin: 0; }

        /* ألوان مختلفة لكل بطاقة */
        .theory-bg { background: linear-gradient(to left, var(--primary), #3b82f6); }
        .practical-bg { background: linear-gradient(to left, var(--success), #34d399); }
        .pizza-bg { background: linear-gradient(to left, var(--secondary), #fbbf24); }

        .card-body { padding: 30px; }

        /* ================= القوائم المنسدلة (Details / Accordion) ================= */
        details {
            background: var(--bg-color);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            margin-bottom: 15px;
            overflow: hidden;
        }

        summary {
            padding: 15px 20px;
            font-weight: 700;
            font-size: 1.1rem;
            cursor: pointer;
            list-style: none;
            display: flex;
            justify-content: space-between;
            align-items: center;
            color: var(--text-main);
            background: var(--card-bg);
            transition: 0.3s;
        }

        summary:hover { background: #f8fafc; }

        summary::-webkit-details-marker { display: none; } /* إخفاء السهم الافتراضي */

        summary::after {
            content: '\f078'; /* أيقونة سهم للأسفل */
            font-family: "Font Awesome 6 Free";
            font-weight: 900;
            color: var(--text-muted);
            transition: transform 0.3s ease;
        }

        details[open] summary { border-bottom: 1px solid var(--border-color); }
        details[open] summary::after { transform: rotate(180deg); color: var(--primary); }

        .accordion-content {
            padding: 20px;
            color: var(--text-muted);
            font-size: 1rem;
        }

        .accordion-content ul, .accordion-content ol { padding-right: 25px; margin-top: 10px; }
        .accordion-content li { margin-bottom: 8px; }

        /* تمييز النصوص */
        .badge-text {
            background: #e0e7ff;
            color: var(--primary-dark);
            padding: 2px 8px;
            border-radius: 4px;
            font-weight: 700;
        }

        .pizza-bg-text { background: #fef3c7; color: #b45309; }
        .practical-bg-text { background: #d1fae5; color: #047857; }

        /* ================= الفوتر ================= */
        footer {
            background: var(--text-main);
            color: #cbd5e1;
            text-align: center;
            padding: 40px 20px;
            margin-top: 50px;
        }

        footer p { margin-bottom: 10px; }
        footer .credits { font-size: 0.9rem; color: #94a3b8; }
        
        .footer-logo {
            font-family: 'Outfit', sans-serif;
            font-size: 1.5rem;
            font-weight: 800;
            color: white;
            margin-bottom: 15px;
        }

        /* ================= التجاوب (Responsive) ================= */
        @media (max-width: 768px) {
            .nav-links { display: none; }
            .hero h1 { font-size: 2rem; }
            .card-header { padding: 20px; }
            .card-body { padding: 20px; }
            summary { font-size: 1rem; }
        }
    </style>
</head>
<body>

    <nav class="navbar">
        <div class="container nav-content">
            <a href="#" class="logo">
                <i class="fa-solid fa-graduation-cap"></i> XS.<span>BODA</span>
            </a>
            <div class="nav-links">
                <span>أسس التغذية</span>
                <span>العملي</span>
                <span>الفرقة الأولى</span>
            </div>
        </div>
    </nav>

    <header class="hero">
        <div class="container">
            <span class="badge">جامعة عين شمس - كلية التربية النوعية</span>
            <h1>مقرر أسس التغذية والاقتصاد المنزلي</h1>
            <p>منصة تعليمية شاملة تضم الملخصات النظرية، التطبيقات العملية، ودليل المخبوزات والبيتزا.</p>
        </div>
    </header>

    <div class="container">
        
        <section class="team-section">
            <h3 class="team-header"><i class="fa-solid fa-users"></i> إعداد فريق العمل</h3>
            <div class="team-grid">
                <span class="team-member">عبدالرحمن مصطفى عويس</span>
                <span class="team-member">عمر محسن عبد العزيز</span>
                <span class="team-member">علي عباس علي</span>
                <span class="team-member">صبري حاتم صبري محمد</span>
                <span class="team-member">هنا محمود مصطفي محمد</span>
                <span class="team-member">منه رجب عبد التواب</span>
                <span class="team-member">هدير احمد مصطفي</span>
                <span class="team-member">ياسمين ابراهيم احمد</span>
                <span class="team-member">فاطمه فايز منصور</span>
                <span class="team-member">منه الله وليد فاروق</span>
            </div>
        </section>

        <article class="course-card">
            <div class="card-header theory-bg">
                <i class="fa-solid fa-book-open-reader fa-2x"></i>
                <h2>الجزء الأول: المفاهيم النظرية</h2>
            </div>
            <div class="card-body">
                <details open>
                    <summary>1. مقدمة في علم التغذية</summary>
                    <div class="accordion-content">
                        <p><span class="badge-text">الغذاء:</span> المادة التي يتناولها الكائن الحي.</p>
                        <p><span class="badge-text">التغذية:</span> العمليات التي يحول بها الجسم الغذاء إلى طاقة وأنسجة.</p>
                        <p><span class="badge-text">العناصر الغذائية:</span> المواد الكيميائية في الطعام (كربوهيدرات، بروتينات، إلخ).</p>
                    </div>
                </details>

                <details>
                    <summary>2. العناصر الغذائية (الكبرى والصغرى)</summary>
                    <div class="accordion-content">
                        <ul>
                            <li><span class="badge-text">الكربوهيدرات:</span> المصدر الرئيسي للطاقة (سكريات، نشويات، ألياف).</li>
                            <li><span class="badge-text">البروتينات:</span> أحجار البناء، بناء العضلات وترميم الأنسجة.</li>
                            <li><span class="badge-text">الدهون:</span> مصدر مركز للطاقة، وامتصاص الفيتامينات.</li>
                            <li><span class="badge-text">الفيتامينات:</span> ذائبة في الدهون (A, D, E, K) وذائبة في الماء (B, C).</li>
                        </ul>
                    </div>
                </details>

                <details>
                    <summary>3. عمليات التمثيل الغذائي</summary>
                    <div class="accordion-content">
                        <p><span class="badge-text">الهضم:</span> تحويل الطعام من صورة معقدة إلى بسيطة.</p>
                        <p><span class="badge-text">الامتصاص:</span> انتقال الغذاء من الأمعاء إلى الدم.</p>
                        <p><span class="badge-text">التمثيل (الأيض):</span> استغلال العناصر في الطاقة أو البناء.</p>
                    </div>
                </details>
            </div>
        </article>

        <article class="course-card">
            <div class="card-header practical-bg">
                <i class="fa-solid fa-utensils fa-2x"></i>
                <h2>الجزء الثاني: التغذية العملي والطهي</h2>
            </div>
            <div class="card-body">
                <details open>
                    <summary>١. قواعد تجهيز الوجبات المثالية</summary>
                    <div class="accordion-content">
                        <ul>
                            <li>مراعاة ميزانية الأسرة وتقديم بدائل اقتصادية.</li>
                            <li>تنسيق الألوان في الوجبة لتكون جذابة وغير مملة.</li>
                            <li>تنوع القوام بين اللين (كالبوريه) والصلب (كالمحمرات) والطازج (كالسلطة).</li>
                        </ul>
                    </div>
                </details>

                <details>
                    <summary>٢. أهمية وأثر الطهي على الغذاء</summary>
                    <div class="accordion-content">
                        <p>يساعد على تكسير ألياف الخضر وتليين نسيج اللحوم لسهولة الهضم، وقتل الميكروبات.</p>
                        <ul>
                            <li><span class="badge-text practical-bg-text">البروتين:</span> يتجمد بالحرارة وينكمش بسبب انفصال العصارات.</li>
                            <li><span class="badge-text practical-bg-text">النشويات:</span> تتحول بالحرارة الجافة إلى "دكسترين" سهل الهضم.</li>
                        </ul>
                    </div>
                </details>
                
                <details>
                    <summary>٣. طرق الطهي (الحرارة الرطبة)</summary>
                    <div class="accordion-content">
                        <ul>
                            <li><span class="badge-text practical-bg-text">السلق:</span> الطهي في ماء مغلي (100°م).</li>
                            <li><span class="badge-text practical-bg-text">التسبيك:</span> الطهي في سائل محدود في إناء محكم الغطاء.</li>
                            <li><span class="badge-text practical-bg-text">التشريب:</span> طهي الطعام في كمية قليلة جداً من السائل حتى يتشربه.</li>
                        </ul>
                    </div>
                </details>
            </div>
        </article>

        <article class="course-card">
            <div class="card-header pizza-bg">
                <i class="fa-solid fa-pizza-slice fa-2x"></i>
                <h2>الجزء الثالث: دليل الخميرة والبيتزا</h2>
            </div>
            <div class="card-body">
                <details open>
                    <summary>1. أساسيات وكيمياء الخميرة</summary>
                    <div class="accordion-content">
                        <p>كائنات دقيقة غنية بفيتامين B المركب. تحتاج للنمو إلى: <strong style="color:var(--secondary)">الغذاء، الرطوبة، والدفء.</strong></p>
                        <div style="background: #f8fafc; padding: 15px; border-radius: 8px; text-align: center; margin: 15px 0; font-family: monospace; border: 1px dashed #cbd5e1; direction: ltr;">
                            Sucrose &rarr; Glucose &rarr; Fructose &rarr; Alcohol + CO₂
                        </div>
                    </div>
                </details>

                <details>
                    <summary>2. مراحل نمو وتكاثر الخميرة</summary>
                    <div class="accordion-content">
                        <ol>
                            <li><span class="badge-text pizza-bg-text">مرحلة النشاط:</span> بداية التفاعل.</li>
                            <li><span class="badge-text pizza-bg-text">التخمير الأول:</span> تضاعف الحجم.</li>
                            <li><span class="badge-text pizza-bg-text">التخمير الثاني:</span> نصف ساعة راحة.</li>
                            <li><span class="badge-text pizza-bg-text">التشكيل والخبز:</span> الخبز في فرن حار لإيقاف التفاعل وتمدد الغاز.</li>
                        </ol>
                    </div>
                </details>

                <details>
                    <summary>3. صنع البيتزا والطرق</summary>
                    <div class="accordion-content">
                        <ul>
                            <li><strong>الطريقة البطيئة:</strong> تخمير متعدد، تعطي أفضل قوام.</li>
                            <li><strong>الطريقة المعتدلة:</strong> توقيت متوسط.</li>
                            <li><strong>الخلط العنيف:</strong> سريعة، خلط أولي أقل.</li>
                        </ul>
                    </div>
                </details>
            </div>
        </article>

    </div>

    <footer>
        <div class="footer-logo">XS.BODA</div>
        <p>&copy; 2026 جميع الحقوق محفوظة - حقيبة التغذية التعليمية</p>
        <p class="credits">تصميم وبرمجة: عبدالرحمن مصطفي | الناشر: إلــعــربــآوي</p>
    </footer>

</body>
</html>
            --glass-border: rgba(255, 255, 255, 0.15);
            --glass-blur: blur(25px);
            --text-main: #ffffff;
            --text-muted: rgba(255, 255, 255, 0.85);
            --accent-color: #00e5ff; 
        }

        body {
            font-family: 'Cairo', sans-serif;
            color: var(--text-main);
            background-image: url('https://images.unsplash.com/photo-1545562083-948f9439164a?q=80&w=2070&auto=format&fit=crop');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            min-height: 100vh;
            line-height: 1.7;
            overflow-x: hidden; 
        }

        .overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.3); 
            z-index: -1;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* ================= الأنيميشن (Animations) ================= */
        @keyframes fadeInUp {
            0% { opacity: 0; transform: translateY(40px); }
            100% { opacity: 1; transform: translateY(0); }
        }

        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-12px); }
            100% { transform: translateY(0px); }
        }

        @keyframes pulseGlow {
            0% { box-shadow: 0 0 0 0 rgba(0, 229, 255, 0.4); }
            70% { box-shadow: 0 0 0 10px rgba(0, 229, 255, 0); }
            100% { box-shadow: 0 0 0 0 rgba(0, 229, 255, 0); }
        }

        /* ================= الشريط العلوي ================= */
        .top-nav {
            background: var(--glass-bg);
            backdrop-filter: var(--glass-blur);
            -webkit-backdrop-filter: var(--glass-blur);
            border: 1px solid var(--glass-border);
            border-radius: 50px;
            padding: 15px 40px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 10px;
            margin-bottom: 40px;
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.2);
            /* حركة الظهور */
            animation: fadeInUp 0.8s ease-out forwards;
        }

        .logo {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 1.5rem;
            font-weight: 700;
            letter-spacing: 2px;
            display: flex;
            align-items: center;
            gap: 10px;
            color: var(--accent-color);
        }

        .nav-links {
            display: flex;
            gap: 20px;
            font-size: 0.95rem;
            color: var(--text-main);
            font-weight: 600;
        }

        .login-btn {
            background: #fff;
            color: #000;
            border: none;
            padding: 8px 25px;
            border-radius: 30px;
            font-weight: bold;
            font-family: 'Cairo', sans-serif;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .login-btn:hover { 
            background: var(--accent-color); 
            color: #000;
            transform: translateY(-2px); 
            box-shadow: 0 5px 15px rgba(0, 229, 255, 0.4);
        }

        /* ================= البطاقات الزجاجية ================= */
        .glass-panel {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: var(--glass-blur);
            -webkit-backdrop-filter: var(--glass-blur);
            border: 1px solid var(--glass-border);
            border-radius: 30px;
            padding: 40px;
            margin-bottom: 40px;
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.2);
            position: relative;
            overflow: hidden;
            /* حركة الظهور المتدرج للأقسام */
            opacity: 0;
            animation: fadeInUp 0.8s ease-out forwards;
        }

        /* تأخير حركة ظهور الأقسام بالترتيب */
        .glass-panel:nth-child(2) { animation-delay: 0.2s; }
        .glass-panel:nth-child(3) { animation-delay: 0.4s; }
        .glass-panel:nth-child(4) { animation-delay: 0.6s; }

        .glass-panel::before {
            content: attr(data-number);
            position: absolute;
            top: -20px;
            left: 30px;
            font-family: 'Space Grotesk', sans-serif;
            font-size: 10rem;
            font-weight: 700;
            color: rgba(255, 255, 255, 0.03);
            z-index: 0;
            line-height: 1;
            pointer-events: none;
        }

        .panel-layout {
            display: flex;
            gap: 40px;
            position: relative;
            z-index: 1;
            align-items: flex-start;
        }

        .panel-text {
            flex: 1;
            width: 100%;
        }

        /* ================= بطاقات الصور (Image Cards) ================= */
        .panel-image-card {
            flex: 0 0 320px;
            background: rgba(255, 255, 255, 0.03);
            padding: 15px;
            border-radius: 25px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 15px 35px rgba(0,0,0,0.3);
            display: flex;
            flex-direction: column;
            gap: 15px;
            /* تأثير الطفو المستمر */
            animation: float 6s ease-in-out infinite;
            overflow: hidden;
        }

        .image-wrapper {
            width: 100%;
            height: 350px;
            border-radius: 15px;
            overflow: hidden;
        }

        .panel-image-card img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.6s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }

        /* تأثير التكبير عند تمرير الماوس */
        .panel-image-card:hover img {
            transform: scale(1.08);
        }

        .image-caption {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 10px;
            font-size: 0.85rem;
            color: rgba(255,255,255,0.6);
            font-family: 'Space Grotesk', 'Cairo', sans-serif;
        }

        .image-caption i {
            background: rgba(255,255,255,0.08);
            padding: 8px;
            border-radius: 50%;
            cursor: pointer;
            color: var(--accent-color);
            transition: all 0.3s ease;
        }

        .panel-image-card:hover .image-caption i {
            background: var(--accent-color);
            color: #000;
            animation: pulseGlow 1.5s infinite;
        }

        /* ================= العناوين والقوائم المنسدلة ================= */
        .panel-header {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 30px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.08);
            padding-bottom: 20px;
        }

        .panel-header i { color: var(--accent-color); }
        .panel-header h2 { margin: 0; font-weight: 400; font-size: 1.8rem; }

        details {
            background: rgba(0, 0, 0, 0.15);
            margin-bottom: 15px;
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.03);
            transition: all 0.4s cubic-bezier(0.25, 0.8, 0.25, 1);
        }

        details:hover {
            background: rgba(0, 0, 0, 0.25);
            border-color: rgba(255, 255, 255, 0.1);
        }

        details[open] {
            background: rgba(0, 0, 0, 0.3);
            border-color: var(--glass-border);
        }

        summary {
            padding: 18px 20px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            list-style: none;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: color 0.3s ease;
        }

        summary::after {
            content: '\f107';
            font-family: "Font Awesome 6 Free";
            font-weight: 900;
            transition: transform 0.4s ease;
            color: var(--accent-color);
        }

        details[open] summary::after { transform: rotate(180deg); }

        .content-box {
            padding: 0 20px 20px;
            color: var(--text-muted);
            border-top: 1px solid rgba(255, 255, 255, 0.05);
            padding-top: 15px;
            font-size: 0.95rem;
            animation: fadeInUp 0.4s ease-out forwards; /* أنيميشن لفتح القائمة */
        }

        .content-box ul, .content-box ol { padding-right: 25px; margin: 10px 0; }
        .content-box li { margin-bottom: 10px; }

        .highlight {
            color: #fff;
            font-weight: bold;
            background: rgba(0, 229, 255, 0.15);
            padding: 2px 8px;
            border-radius: 5px;
        }

        /* ================= قسم الطلاب ================= */
        .students-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
            gap: 15px;
            width: 100%;
        }

        .student-card {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.08);
            padding: 12px;
            border-radius: 12px;
            text-align: center;
            font-size: 0.9rem;
            transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
        }

        .student-card:hover { 
            background: rgba(255, 255, 255, 0.15); 
            transform: translateY(-5px); 
            border-color: var(--accent-color);
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
            color: #fff;
        }

        /* ================= الشريط السفلي ================= */
        .bottom-bar {
            background: var(--glass-bg);
            backdrop-filter: var(--glass-blur);
            border: 1px solid var(--glass-border);
            border-radius: 50px;
            padding: 15px 40px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            font-size: 0.85rem;
            color: var(--text-muted);
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.2);
            flex-wrap: wrap;
            gap: 10px;
            opacity: 0;
            animation: fadeInUp 0.8s ease-out 0.8s forwards; /* يظهر أخيراً */
        }

        .bottom-bar i { color: var(--accent-color); transition: transform 0.3s; }
        .bottom-bar .up-btn:hover i { transform: translateY(-3px); }

        /* ================= التجاوب مع جميع الشاشات (Responsive) ================= */
        @media (max-width: 992px) {
            .panel-layout { flex-direction: column; }
            .panel-image-card { width: 100%; max-width: 100%; flex: auto; }
            .image-wrapper { height: 300px; }
            .glass-panel::before { font-size: 7rem; left: 15px; top: -10px; }
        }

        @media (max-width: 768px) {
            .nav-links { display: none; }
            .top-nav { padding: 15px 25px; }
            .glass-panel { padding: 25px; border-radius: 20px; }
            .panel-header h2 { font-size: 1.4rem; }
            .bottom-bar { flex-direction: column; text-align: center; border-radius: 20px; padding: 20px;}
        }

        @media (max-width: 480px) {
            .students-grid { grid-template-columns: repeat(auto-fill, minmax(140px, 1fr)); }
            .image-wrapper { height: 200px; }
            summary { font-size: 1rem; padding: 15px; }
            .logo { font-size: 1.2rem; }
            .glass-panel::before { font-size: 5rem; left: 10px; top: -5px; }
        }
    </style>
</head>
<body>

    <div class="overlay"></div>

    <div class="container">
        
        <nav class="top-nav">
            <div class="logo">
                <i class="fa-solid fa-water"></i> XS.BODA
            </div>
            <div class="nav-links">
                <span>أسس التغذية</span>
                <span>الاقتصاد المنزلي</span>
                <span>الفرقة الأولى</span>
            </div>
            <button class="login-btn">تسجيل الدخول</button>
        </nav>

        <section class="glass-panel" data-number="00">
            <div class="panel-layout">
                <div class="panel-text">
                    <div class="panel-header">
                        <i class="fas fa-users fa-2x"></i>
                        <h2>فريق العمل - إعداد الطلاب</h2>
                    </div>
                    <div class="students-grid">
                        <div class="student-card">عبدالرحمن مصطفى عويس</div>
                        <div class="student-card">عمر محسن عبد العزيز</div>
                        <div class="student-card">علي عباس علي</div>
                        <div class="student-card">صبري حاتم صبري محمد</div>
                        <div class="student-card">هنا محمود مصطفي محمد</div>
                        <div class="student-card">منه رجب عبد التواب</div>
                        <div class="student-card">هدير احمد مصطفي</div>
                        <div class="student-card">ياسمين ابراهيم احمد</div>
                        <div class="student-card">فاطمه فايز منصور</div>
                        <div class="student-card">منه الله وليد فاروق</div>
                    </div>
                </div>
            </div>
        </section>

        <section class="glass-panel" data-number="01">
            <div class="panel-layout">
                <div class="panel-text">
                    <div class="panel-header">
                        <i class="fas fa-book-open fa-2x"></i>
                        <h2>ملخص منهج أسس التغذية (النظري)</h2>
                    </div>

                    <details open>
                        <summary>1. مقدمة في علم التغذية</summary>
                        <div class="content-box">
                            <p><span class="highlight">الغذاء:</span> المادة التي يتناولها الكائن الحي.</p>
                            <p><span class="highlight">التغذية:</span> العمليات التي يحول بها الجسم الغذاء إلى طاقة وأنسجة.</p>
                            <p><span class="highlight">العناصر الغذائية:</span> المواد الكيميائية في الطعام (كربوهيدرات، بروتينات، إلخ).</p>
                        </div>
                    </details>

                    <details>
                        <summary>2. العناصر الغذائية (الكبرى والصغرى)</summary>
                        <div class="content-box">
                            <ul>
                                <li><span class="highlight">الكربوهيدرات:</span> المصدر الرئيسي للطاقة (سكريات، نشويات، ألياف).</li>
                                <li><span class="highlight">البروتينات:</span> أحجار البناء، بناء العضلات وترميم الأنسجة.</li>
                                <li><span class="highlight">الدهون:</span> مصدر مركز للطاقة، وامتصاص الفيتامينات.</li>
                                <li><span class="highlight">الفيتامينات:</span> ذائبة في الدهون (A, D, E, K) وذائبة في الماء (B, C).</li>
                            </ul>
                        </div>
                    </details>

                    <details>
                        <summary>3. عمليات التمثيل الغذائي</summary>
                        <div class="content-box">
                            <p><span class="highlight">الهضم:</span> تحويل الطعام من صورة معقدة إلى بسيطة.</p>
                            <p><span class="highlight">الامتصاص:</span> انتقال الغذاء من الأمعاء إلى الدم.</p>
                            <p><span class="highlight">التمثيل (الأيض):</span> استغلال العناصر في الطاقة أو البناء.</p>
                        </div>
                    </details>
                </div>
                
                <div class="panel-image-card">
                    <div class="image-wrapper">
                        <img src="https://images.unsplash.com/photo-1490645935967-10de6ba17061?q=80&w=800&auto=format&fit=crop" alt="أكل صحي وتغذية">
                    </div>
                    <div class="image-caption">
                        <span>NUTRITION BASICS</span>
                        <i class="fas fa-search-plus"></i>
                    </div>
                </div>
            </div>
        </section>

        <section class="glass-panel" data-number="02">
            <div class="panel-layout">
                <div class="panel-text">
                    <div class="panel-header">
                        <i class="fas fa-utensils fa-2x"></i>
                        <h2>مقرر الغذاء والتغذية (العملي)</h2>
                    </div>

                    <details open>
                        <summary>١. قواعد تجهيز الوجبات المثالية</summary>
                        <div class="content-box">
                            <ul>
                                <li>مراعاة ميزانية الأسرة وتقديم بدائل اقتصادية.</li>
                                <li>تنسيق الألوان في الوجبة لتكون جذابة وغير مملة.</li>
                                <li>تنوع القوام بين اللين (كالبوريه) والصلب (كالمحمرات) والطازج (كالسلطة).</li>
                            </ul>
                        </div>
                    </details>

                    <details>
                        <summary>٢. أهمية وأثر الطهي على الغذاء</summary>
                        <div class="content-box">
                            <p>يساعد على تكسير ألياف الخضر وتليين نسيج اللحوم لسهولة الهضم، وقتل الميكروبات.</p>
                            <ul>
                                <li><span class="highlight">البروتين:</span> يتجمد بالحرارة وينكمش بسبب انفصال العصارات.</li>
                                <li><span class="highlight">النشويات:</span> تتحول بالحرارة الجافة إلى "دكسترين" سهل الهضم.</li>
                            </ul>
                        </div>
                    </details>
                    
                    <details>
                        <summary>٣. طرق الطهي (الحرارة الرطبة)</summary>
                        <div class="content-box">
                            <ul>
                                <li><span class="highlight">السلق:</span> الطهي في ماء مغلي (100°م).</li>
                                <li><span class="highlight">التسبيك:</span> الطهي في سائل محدود في إناء محكم الغطاء.</li>
                                <li><span class="highlight">التشريب:</span> طهي الطعام في كمية قليلة جداً من السائل حتى يتشربه.</li>
                            </ul>
                        </div>
                    </details>
                </div>

                <div class="panel-image-card" style="animation-delay: 0.5s;"> <div class="image-wrapper">
                        <img src="https://images.unsplash.com/photo-1556910103-1c02745a872f?q=80&w=800&auto=format&fit=crop" alt="أدوات الطهي والتحضير">
                    </div>
                    <div class="image-caption">
                        <span>PRACTICAL COOKING</span>
                        <i class="fas fa-search-plus"></i>
                    </div>
                </div>
            </div>
        </section>

        <section class="glass-panel" data-number="03">
            <div class="panel-layout">
                ard">هدير احمد مصطفي</div>
                        <div class="student-card">ياسمين ابراهيم احمد</div>
                        <div class="student-card">فاطمه فايز منصور</div>
                        <div class="student-card">منه الله وليد فاروق</div>
                    </div>
                </div>
            </div>
        </section>

        <section class="glass-panel" data-number="01">
            <div class="panel-layout">
                <div class="panel-text">
                    <div class="panel-header">
                        <i class="fas fa-book-open fa-2x"></i>
                        <h2>ملخص منهج أسس التغذية (النظري)</h2>
                    </div>

                    <details open>
                        <summary>1. مقدمة في علم التغذية</summary>
                        <div class="content-box">
                            <p><span class="highlight">الغذاء:</span> المادة التي يتناولها الكائن الحي.</p>
                            <p><span class="highlight">التغذية:</span> العمليات التي يحول بها الجسم الغذاء إلى طاقة وأنسجة.</p>
                            <p><span class="highlight">العناصر الغذائية:</span> المواد الكيميائية في الطعام (كربوهيدرات، بروتينات، إلخ).</p>
                        </div>
                    </details>

                    <details>
                        <summary>2. العناصر الغذائية (الكبرى والصغرى)</summary>
                        <div class="content-box">
                            <ul>
                                <li><span class="highlight">الكربوهيدرات:</span> المصدر الرئيسي للطاقة (سكريات، نشويات، ألياف).</li>
                                <li><span class="highlight">البروتينات:</span> أحجار البناء، بناء العضلات وترميم الأنسجة.</li>
                                <li><span class="highlight">الدهون:</span> مصدر مركز للطاقة، وامتصاص الفيتامينات.</li>
                                <li><span class="highlight">الفيتامينات:</span> ذائبة في الدهون (A, D, E, K) وذائبة في الماء (B, C).</li>
                            </ul>
                        </div>
                    </details>

                    <details>
                        <summary>3. عمليات التمثيل الغذائي</summary>
                        <div class="content-box">
                            <p><span class="highlight">الهضم:</span> تحويل الطعام من صورة معقدة إلى بسيطة.</p>
                            <p><span class="highlight">الامتصاص:</span> انتقال الغذاء من الأمعاء إلى الدم.</p>
                            <p><span class="highlight">التمثيل (الأيض):</span> استغلال العناصر في الطاقة أو البناء.</p>
                        </div>
                    </details>
                </div>
                
                <div class="panel-image-card">
                    <img src="https://images.unsplash.com/photo-1490645935967-10de6ba17061?q=80&w=800&auto=format&fit=crop" alt="أكل صحي وتغذية">
                    <div class="image-caption">
                        <span>NUTRITION BASICS</span>
                        <i class="fas fa-search-plus"></i>
                    </div>
                </div>
            </div>
        </section>

        <section class="glass-panel" data-number="02">
            <div class="panel-layout">
                <div class="panel-text">
                    <div class="panel-header">
                        <i class="fas fa-utensils fa-2x"></i>
                        <h2>مقرر الغذاء والتغذية (العملي)</h2>
                    </div>

                    <details open>
                        <summary>١. قواعد تجهيز الوجبات المثالية</summary>
                        <div class="content-box">
                            <ul>
                                <li>مراعاة ميزانية الأسرة وتقديم بدائل اقتصادية.</li>
                                <li>تنسيق الألوان في الوجبة لتكون جذابة وغير مملة.</li>
                                <li>تنوع القوام بين اللين (كالبوريه) والصلب (كالمحمرات) والطازج (كالسلطة).</li>
                            </ul>
                        </div>
                    </details>

                    <details>
                        <summary>٢. أهمية وأثر الطهي على الغذاء</summary>
                        <div class="content-box">
                            <p>يساعد على تكسير ألياف الخضر وتليين نسيج اللحوم لسهولة الهضم، وقتل الميكروبات.</p>
                            <ul>
                                <li><span class="highlight">البروتين:</span> يتجمد بالحرارة وينكمش بسبب انفصال العصارات.</li>
                                <li><span class="highlight">النشويات:</span> تتحول بالحرارة الجافة إلى "دكسترين" سهل الهضم.</li>
                            </ul>
                        </div>
                    </details>
                    
                    <details>
                        <summary>٣. طرق الطهي (الحرارة الرطبة)</summary>
                        <div class="content-box">
                            <ul>
                                <li><span class="highlight">السلق:</span> الطهي في ماء مغلي (100°م).</li>
                                <li><span class="highlight">التسبيك:</span> الطهي في سائل محدود في إناء محكم الغطاء.</li>
                                <li><span class="highlight">التشريب:</span> طهي الطعام في كمية قليلة جداً من السائل حتى يتشربه.</li>
                            </ul>
                        </div>
                    </details>
                </div>

                <div class="panel-image-card">
                    <img src="https://images.unsplash.com/photo-1556910103-1c02745a872f?q=80&w=800&auto=format&fit=crop" alt="أدوات الطهي والتحضير">
                    <div class="image-caption">
                        <span>PRACTICAL COOKING</span>
                        <i class="fas fa-search-plus"></i>
                    </div>
                </div>
            </div>
        </section>

        <section class="glass-panel" data-number="03">
            <div class="panel-layout">
                <div class="panel-text">
                    <div class="panel-header">
                        <i class="fas fa-pizza-slice fa-2x"></i>
                        <h2>دليل المذاكرة: الخميرة والبيتزا</h2>
                    </div>

                    <details open>
                        <summary>1. أساسيات وكيمياء الخميرة</summary>
                        <div class="content-box">
                            <p>كائنات دقيقة غنية بفيتامين B المركب. تحتاج للنمو إلى: <span class="highlight">الغذاء، الرطوبة، والدفء.</span></p>
                            <div style="background: rgba(0,0,0,0.3); padding: 10px; border-radius: 8px; text-align: center; margin: 10px 0; font-family: monospace; letter-spacing: 1px;">
                                Sucrose &rarr; Glucose &rarr; Fructose &rarr; Alcohol + CO₂
                            </div>
                        </div>
                    </details>

                    <details>
                        <summary>2. مراحل نمو وتكاثر الخميرة</summary>
                        <div class="content-box">
                            <ol>
                                <li><span class="highlight">مرحلة النشاط:</span> بداية التفاعل.</li>
                                <li><span class="highlight">التخمير الأول:</span> تضاعف الحجم.</li>
                                <li><span class="highlight">التخمير الثاني:</span> نصف ساعة راحة.</li>
                                <li><span class="highlight">التشكيل والخبز:</span> الخبز في فرن حار لإيقاف التفاعل.</li>
                            </ol>
                        </div>
                    </details>
                </div>

                <div class="panel-image-card">
                    <img src="https://images.unsplash.com/photo-1513104890138-7c749659a591?q=80&w=800&auto=format&fit=crop" alt="بيتزا طازجة">
                    <div class="image-caption">
                        <span>YEAST & PIZZA</span>
                        <i class="fas fa-search-plus"></i>
                    </div>
                </div>
            </div>
        </section>

        <footer class="bottom-bar">
            <div><i class="fa-regular fa-copyright"></i> 2026 حقيبة التغذية التعليمية</div>
            <div>مصمم الصفحة: عبدالرحمن مصطفي | الناشر: إلــعــربــآوي</div>
            <div style="font-family: 'Space Grotesk', sans-serif;"><i class="fa-solid fa-arrow-up"></i></div>
        </footer>

    </div>

</body>
</html>
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
