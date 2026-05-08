<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>منهج أسس التغذية والاقتصاد المنزلي | Xs.boda</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Amiri:ital,wght@0,400;0,700;1,400&family=Cairo:wght@300;600;900&family=Great+Vibes&display=swap" rel="stylesheet">
    
    <style>
        /* المتغيرات العامة للألوان */
        :root {
            --dark-header: #0f172a;
            --dark-header-grad: #1e293b;
            --gold: #fbbf24;
            --nutrition-color: #27ae60;
            --pizza-primary: #2c5f78;
            --pizza-accent: #e67e22;
            --bg-color: #f4f7f6;
            --text-color: #333;
        }

        /* التنسيقات الأساسية */
        body {
            font-family: 'Cairo', 'Segoe UI', Tahoma, sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
            margin: 0;
            padding: 0;
        }

        /* تنسيقات الترويسة (Header) */
        .main-header {
            background: linear-gradient(135deg, var(--dark-header-grad) 0%, var(--dark-header) 100%);
            color: white;
            padding: 60px 20px;
            text-align: center;
            border-bottom: 5px solid var(--gold);
        }

        .brand-name {
            font-family: 'Great Vibes', cursive;
            font-size: 4rem;
            color: var(--gold);
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            direction: ltr;
        }

        .course-name {
            font-family: 'Cairo', sans-serif;
            font-weight: 600;
            font-size: 1.8rem;
            letter-spacing: 1px;
            opacity: 0.9;
            margin-top: 0;
        }

        .separator {
            width: 80px;
            border: 1px solid var(--gold);
            margin: 30px auto;
        }

        .students-section h3 {
            font-family: 'Cairo', sans-serif;
            font-weight: 900;
            font-size: 1.5rem;
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
            transition: transform 0.3s ease, background 0.3s ease;
        }

        .students-list li:hover {
            transform: translateY(-5px);
            background: rgba(251, 191, 36, 0.15);
            color: var(--gold);
        }

        /* حاوية المحتوى الرئيسي */
        .container {
            max-width: 900px;
            margin: 40px auto;
            padding: 0 20px;
        }

        .main-title {
            text-align: center;
            color: #2c3e50;
            border-bottom: 3px solid var(--gold);
            padding-bottom: 15px;
            margin-bottom: 40px;
            font-weight: 900;
        }

        /* تنسيقات قسم التغذية */
        .nutrition-section-title {
            background-color: var(--nutrition-color);
            color: white;
            padding: 12px 20px;
            border-radius: 8px;
            margin-top: 40px;
            font-size: 1.4rem;
        }

        details {
            background: #fff;
            margin-bottom: 15px;
            padding: 15px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
            border-right: 5px solid transparent;
        }

        details[open] {
            border-right: 5px solid var(--nutrition-color);
        }

        summary {
            font-weight: bold;
            font-size: 1.1rem;
            cursor: pointer;
            outline: none;
            list-style: none;
            color: #2e86de;
            display: flex;
            align-items: center;
        }

        summary::before {
            content: "➕ ";
            margin-left: 10px;
            font-size: 0.9em;
        }

        details[open] summary::before {
            content: "➖ ";
        }

        .details-content {
            padding: 15px 10px 0;
            border-top: 1px solid #eee;
            margin-top: 15px;
            font-family: 'Amiri', serif;
            font-size: 1.1rem;
        }

        .highlight { color: #d35400; font-weight: bold; }

        /* تنسيقات قسم الخميرة والبيتزا */
        .pizza-wrapper {
            background: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.08);
            margin-top: 50px;
        }

        .pizza-header {
            text-align: center;
            background-color: var(--pizza-primary);
            color: white;
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 30px;
        }

        .topic-card {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 30px;
            padding: 20px;
            border-bottom: 2px solid #d9e8ef;
            align-items: center;
        }

        .topic-card:last-child { border-bottom: none; margin-bottom: 0; }

        .topic-content {
            flex: 1;
            min-width: 300px;
        }

        .topic-content h2 {
            color: var(--pizza-primary);
            border-right: 5px solid var(--pizza-accent);
            padding-right: 10px;
            margin-top: 0;
        }

        .image-placeholder {
            flex: 0 0 250px;
            height: 200px;
            background-color: #d9e8ef;
            border: 2px dashed var(--pizza-primary);
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 10px;
            color: var(--pizza-primary);
            font-weight: bold;
            text-align: center;
            font-size: 0.9rem;
        }

        .formula {
            background: #f8fafc;
            padding: 15px;
            border-radius: 5px;
            font-family: 'Courier New', Courier, monospace;
            direction: ltr;
            text-align: center;
            border: 1px solid #cbd5e1;
            font-weight: bold;
            color: #b91c1c;
        }

        .tag {
            display: inline-block;
            background: var(--pizza-accent);
            color: white;
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 0.85em;
            margin-bottom: 10px;
            font-weight: bold;
        }

        /* تجاوب الشاشات */
        @media (max-width: 768px) {
            .brand-name { font-size: 3rem; }
            .students-list { grid-template-columns: 1fr 1fr; }
            .topic-card { flex-direction: column; text-align: center; }
            .topic-content h2 { border-right: none; border-bottom: 3px solid var(--pizza-accent); padding-bottom: 10px; padding-right: 0; display: inline-block;}
            .image-placeholder { width: 100%; flex-basis: auto; }
        }
        @media (max-width: 480px) {
            .brand-name { font-size: 2.5rem; }
            .students-list { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>

    <header class="main-header">
        <div class="overlay">
            <h1 class="brand-name">Xs.boda</h1>
            <h2 class="course-name">أسس التغذية / الاقتصاد المنزلي</h2>
            <hr class="separator">
            <div class="students-section">
                <h3>فريق إعداد الطلاب</h3>
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

    <main class="container">
        
        <h1 class="main-title">📚 الدليل الشامل للمنهج الدراسي</h1>

        <section>
            <h2 class="nutrition-section-title">الجزء الأول: المفاهيم الأساسية في التغذية</h2>

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
                <summary>4. الماء وتفاعلات الأيض</summary>
                <div class="details-content">
                    <p><strong>أهمية الماء:</strong></p>
                    <ul>
                        <li>تنظيم درجة حرارة الجسم.</li>
                        <li>نقل العناصر الغذائية والتخلص من الفضلات.</li>
                        <li>وسط للتفاعلات الكيميائية داخل الخلايا.</li>
                    </ul>
                    <p><strong>عمليات التمثيل الغذائي (Metabolism):</strong></p>
                    <ul>
                        <li><strong>الهضم:</strong> تحويل الطعام من صورة معقدة إلى بسيطة.</li>
                        <li><strong>الامتصاص:</strong> انتقال الغذاء من الأمعاء إلى الدم.</li>
                        <li><strong>التمثيل (الأيض):</strong> استغلال العناصر في الطاقة أو البناء.</li>
                    </ul>
                </div>
            </details>

            <h2 class="nutrition-section-title">الجزء الثاني: التعمق الفني والتطبيقي</h2>

            <details>
                <summary>1. تفاصيل الكربوهيدرات والبروتينات</summary>
                <div class="details-content">
                    <p><strong>الكربوهيدرات (الوقود الحيوي):</strong></p>
                    <ul>
                        <li>سكريات أحادية: جلوكوز (سكر الدم)، فركتوز (سكر الفاكهة).</li>
                        <li>سكريات ثنائية: سكروز (سكر المائدة)، لاكتوز (سكر الحليب).</li>
                        <li>سكريات معقدة: النشا، الجليكوجين، والألياف الضرورية للأمعاء.</li>
                    </ul>
                    <p><strong>البروتينات (المعمار الهيكلي):</strong> تتكون من <strong>أحماض أمينية</strong>:</p>
                    <ul>
                        <li>أحماض أساسية: لا يصنعها الجسم (مثل المصادر الحيوانية).</li>
                        <li>أحماض غير أساسية: يستطيع الجسم تصنيعها.</li>
                    </ul>
                    <p class="highlight">💡 نصيحة: فكرة "التكامل الغذائي" (مثل الفول مع الخبز).</p>
                </div>
            </details>

            <details>
                <summary>2. الطاقة والفيتامينات (نصائح للامتحان)</summary>
                <div class="details-content">
                    <p><strong>القيمة الحرارية (السعرات):</strong></p>
                    <ul>
                        <li>1 جرام كربوهيدرات = 4 سعرات | 1 جرام بروتين = 4 سعرات | 1 جرام دهون = 9 سعرات.</li>
                    </ul>
                    <p><strong>أعراض نقص الفيتامينات:</strong></p>
                    <ul>
                        <li><strong>فيتامين A:</strong> العشى الليلي | <strong>فيتامين D:</strong> الكساح ولين العظام | <strong>فيتامين C:</strong> الإسقربوط | <strong>B12:</strong> الأنيميا ومشاكل الأعصاب.</li>
                    </ul>
                    <p class="highlight">كيف تضمن الدرجة النهائية؟</p>
                    <ul>
                        <li>استخدام الرسوم التخطيطية لمسار الهضم وعمل جداول مقارنة بين الدهون المشبعة وغير المشبعة.</li>
                    </ul>
                </div>
            </details>
        </section>

        <section class="pizza-wrapper">
            <div class="pizza-header">
                <h2 style="margin:0; font-size: 2rem;">دليل المذاكرة: الخميرة والبيتزا</h2>
                <p style="margin-top: 5px; opacity: 0.9;">خطة تعليمية تفصيلية لمكونات وعمليات العجين</p>
            </div>

            <div class="topic-card">
                <div class="topic-content">
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
                    [صورة أنواع الخميرة <br> وشكل الخلايا]
                </div>
            </div>

            <div class="topic-card">
                <div class="image-placeholder">
                    [صورة مخطط <br> الدفء/الغذاء/الرطوبة]
                </div>
                <div class="topic-content">
                    <span class="tag">القسم الثاني</span>
                    <h2>الظروف المناسبة والكيمياء</h2>
                    <p>تحتاج الخميرة للنمو: <strong>الغذاء، الرطوبة، والدفء.</strong></p>
                    <p>المعادلة الكيميائية للتخمير:</p>
                    <div class="formula">
                        Sucrose &rarr; Glucose &rarr; Fructose &rarr; Alcohol + CO2
                    </div>
                    <p>ينتج غاز CO2 وهو المسؤول عن رفع العجين وتمدده.</p>
                </div>
            </div>

            <div class="topic-card">
                <div class="topic-content">
                    <span class="tag">القسم الثالث</span>
                    <h2>صنع البيتزا والطرق</h2>
                    <ul>
                        <li><strong>الطريقة البطيئة:</strong> تخمير متعدد، أفضل قوام.</li>
                        <li><strong>الطريقة المعتدلة:</strong> توقيت متوسط.</li>
                        <li><strong>الخلط العنيف:</strong> سريعة، خلط أولي أقل.</li>
                    </ul>
                    <p><strong>المقادير الأساسية:</strong> دقيق، ملح، زيت، خميرة، سكر، حليب، بيضة.</p>
                </div>
                <div class="image-placeholder">
                    [صورة أيقونات المقادير <br> دقيق/زيت/بيض]
                </div>
            </div>

            <div class="topic-card">
                <div class="image-placeholder">
                    [صورة مراحل <br> تضاعف حجم العجين]
                </div>
                <div class="topic-content">
                    <span class="tag">القسم الرابع</span>
                    <h2>مراحل التخمير والخبز</h2>
                    <ol>
                        <li><strong>مرحلة النشاط:</strong> بداية التفاعل.</li>
                        <li><strong>التخمير الأول:</strong> تضاعف الحجم (Double Volume).</li>
                        <li><strong>التخمير الثاني:</strong> (نصف ساعة).</li>
                        <li><strong>التشكيل:</strong> (45 دقيقة) مع تجنب زيادة التخمير.</li>
                    </ol>
                    <p>يتم الخبز في <strong>فرن حار</strong> لإيقاف فعل الخميرة وتمدد الغاز. ويمكن إضافة حشوات مثل الجبن الرومي، الزعتر، والزيتون.</p>
                </div>
            </div>
        </section>

    </main>

</body>
</html>

