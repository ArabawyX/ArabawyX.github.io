<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>منهج أسس التغذية والاقتصاد المنزلي | Xs.boda</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&family=Cairo:wght@300;600;900&family=Great+Vibes&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --glass-bg: rgba(255, 255, 255, 0.12);
            --glass-border: rgba(255, 255, 255, 0.25);
            --blur: blur(15px);
            --gold: #fbbf24;
            --accent-blue: #7dd3fc;
        }

        body {
            margin: 0;
            padding: 0;
            font-family: 'Cairo', sans-serif;
            background: url('https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?q=80&w=2070&auto=format&fit=crop') no-repeat center center fixed;
            background-size: cover;
            color: white;
            line-height: 1.6;
        }

        /* الطبقة الزجاجية الرئيسية */
        .main-wrapper {
            background: rgba(0, 0, 0, 0.4);
            min-height: 100vh;
            padding: 40px 20px;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
        }

        /* الهيدر الزجاجي */
        header {
            background: var(--glass-bg);
            backdrop-filter: var(--blur);
            -webkit-backdrop-filter: var(--blur);
            border: 1px solid var(--glass-border);
            border-radius: 40px;
            padding: 50px 20px;
            text-align: center;
            margin-bottom: 40px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }

        .brand-name {
            font-family: 'Great Vibes', cursive;
            font-size: 5rem;
            color: var(--gold);
            margin: 0;
            direction: ltr;
        }

        .course-name {
            font-size: 2rem;
            font-weight: 900;
            margin-top: 10px;
            letter-spacing: 2px;
        }

        /* شبكة الطلاب */
        .students-section {
            margin-top: 30px;
            border-top: 1px solid var(--glass-border);
            padding-top: 20px;
        }

        .students-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 15px;
            list-style: none;
            padding: 0;
        }

        .students-list li {
            background: rgba(255, 255, 255, 0.05);
            padding: 10px;
            border-radius: 15px;
            font-family: 'Amiri', serif;
            font-size: 1.2rem;
            border: 1px solid transparent;
            transition: 0.3s;
        }

        .students-list li:hover {
            background: var(--glass-bg);
            border-color: var(--gold);
            transform: scale(1.05);
        }

        /* العناوين والأقسام */
        .section-glass {
            background: var(--glass-bg);
            backdrop-filter: var(--blur);
            -webkit-backdrop-filter: var(--blur);
            border: 1px solid var(--glass-border);
            border-radius: 30px;
            padding: 30px;
            margin-bottom: 30px;
        }

        h2.title-glow {
            color: var(--gold);
            border-right: 5px solid var(--gold);
            padding-right: 15px;
            margin-bottom: 25px;
            font-weight: 900;
        }

        /* تفاصيل المنهج (Details) */
        details {
            background: rgba(255, 255, 255, 0.05);
            margin-bottom: 10px;
            border-radius: 15px;
            overflow: hidden;
            border: 1px solid var(--glass-border);
        }

        summary {
            padding: 15px;
            cursor: pointer;
            font-weight: bold;
            color: var(--accent-blue);
            list-style: none;
        }

        .details-content {
            padding: 20px;
            background: rgba(0, 0, 0, 0.2);
            font-family: 'Amiri', serif;
            font-size: 1.2rem;
        }

        /* قسم البيتزا والكيمياء */
        .pizza-card {
            display: flex;
            gap: 20px;
            align-items: center;
            margin-bottom: 25px;
            background: rgba(255, 255, 255, 0.03);
            padding: 20px;
            border-radius: 20px;
        }

        .formula {
            background: rgba(0, 0, 0, 0.5);
            padding: 15px;
            border-radius: 10px;
            font-family: monospace;
            color: #4ade80;
            text-align: center;
            margin: 15px 0;
            border: 1px solid #4ade80;
            direction: ltr;
        }

        .tag {
            background: var(--gold);
            color: black;
            padding: 2px 12px;
            border-radius: 10px;
            font-size: 0.8rem;
            font-weight: bold;
            display: inline-block;
            margin-bottom: 10px;
        }

        .img-box {
            min-width: 150px;
            height: 150px;
            background: rgba(255,255,255,0.1);
            border: 2px dashed var(--glass-border);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.8rem;
            text-align: center;
        }

        @media (max-width: 768px) {
            .pizza-card { flex-direction: column; text-align: center; }
            .brand-name { font-size: 3rem; }
        }
    </style>
</head>
<body>

<div class="main-wrapper">
    <div class="container">
        
        <header>
            <h1 class="brand-name">Xs.boda</h1>
            <h2 class="course-name">أسس التغذية / الاقتصاد المنزلي</h2>
            <div class="students-section">
                <p style="font-weight: 900; color: var(--gold);">فريق إعداد الطلاب</p>
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

        <main>
            <div class="section-glass">
                <h2 class="title-glow">📚 المفاهيم الأساسية في التغذية</h2>
                
                <details>
                    <summary>1. مقدمة في علم التغذية</summary>
                    <div class="details-content">
                        <p><strong>الغذاء:</strong> المادة التي يتناولها الكائن الحي.</p>
                        <p><strong>التغذية:</strong> العمليات التي يحول بها الجسم الغذاء إلى طاقة وأنسجة.</p>
                    </div>
                </details>

                <details>
                    <summary>2. العناصر الغذائية الكبرى والصغرى</summary>
                    <div class="details-content">
                        <p><strong>الكربوهيدرات:</strong> المصدر الرئيسي للطاقة.</p>
                        <p><strong>البروتينات:</strong> بناء العضلات وترميم الأنسجة.</p>
                        <hr style="opacity: 0.1;">
                        <p><span style="color:var(--gold)">الفيتامينات:</span> ذائبة في الدهون (A, D, E, K) وذائبة في الماء (B, C).</p>
                    </div>
                </details>
            </div>

            <div class="section-glass">
                <h2 class="title-glow">🍕 دليل الخميرة والبيتزا</h2>
                
                <div class="pizza-card">
                    <div style="flex: 1;">
                        <span class="tag">العملية الكيميائية</span>
                        <h3>كيمياء التخمير</h3>
                        <p>ينتج غاز CO2 وهو المسؤول عن رفع العجين وتمدده.</p>
                        <div class="formula">
                            Sucrose &rarr; Glucose &rarr; Fructose &rarr; Alcohol + CO2
                        </div>
                    </div>
                    <div class="img-box">[ صورة التفاعل الكيميائي ]</div>
                </div>

                <div class="pizza-card">
                    <div class="img-box">[ مراحل التخمير ]</div>
                    <div style="flex: 1;">
                        <span class="tag">خطوات العمل</span>
                        <h3>مراحل الخبز</h3>
                        <ul>
                            <li>التخمير الأول: تضاعف الحجم.</li>
                            <li>التخمير الثاني: نصف ساعة.</li>
                            <li>الخبز: فرن حار لإيقاف الخميرة.</li>
                        </ul>
                    </div>
                </div>
            </div>
        </main>

    </div>
</div>

</body>
</html>
