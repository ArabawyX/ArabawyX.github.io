<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>XS.Boda | الموسوعة الغذائية الشاملة</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;600;900&family=Amiri:wght@700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    
    <style>
        :root {
            --primary: #d4a373;
            --dark: #121212;
            --glass: rgba(255, 255, 255, 0.1);
            --glass-border: rgba(255, 255, 255, 0.2);
            --card-white: #ffffff;
            --text-main: #333;
            --transition: all 0.3s ease;
        }

        * { box-sizing: border-box; margin: 0; padding: 0; }

        body {
            font-family: 'Cairo', sans-serif;
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), 
                        url('https://images.unsplash.com/photo-1490645935967-10de6ba17061?auto=format&fit=crop&q=80&w=2000') no-repeat center center fixed;
            background-size: cover;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
            direction: rtl;
            color: #fff;
        }

        .app-window {
            width: 100%;
            max-width: 1300px;
            background: var(--glass);
            backdrop-filter: blur(25px);
            border: 1px solid var(--glass-border);
            border-radius: 30px;
            display: flex;
            flex-direction: column;
            box-shadow: 0 40px 100px rgba(0,0,0,0.4);
            overflow: hidden;
        }

        header {
            padding: 20px 40px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid rgba(255,255,255,0.1);
        }

        .logo { font-family: 'Amiri', serif; font-size: 2.2rem; color: var(--primary); }

        .main-grid {
            display: grid;
            grid-template-columns: 320px 1fr;
            gap: 20px;
            padding: 25px;
        }

        /* الموبايل */
        @media (max-width: 992px) {
            .main-grid { grid-template-columns: 1fr; }
            body { padding: 10px; }
        }

        /* الجانب الأيمن (الطلاب والمعلومات السريعة) */
        .sidebar { display: flex; flex-direction: column; gap: 20px; }
        
        .card {
            background: var(--card-white);
            border-radius: 20px;
            padding: 20px;
            color: var(--text-main);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }

        .students-list { list-style: none; margin-top: 10px; font-size: 0.9rem; }
        .students-list li { padding: 5px 0; border-bottom: 1px solid #eee; }
        .students-list li:last-child { border: none; }

        /* منطقة المحتوى العلمي الرئيسي */
        .content-area {
            background: rgba(0,0,0,0.3);
            border-radius: 25px;
            padding: 30px;
            height: 70vh;
            overflow-y: auto;
            border: 1px solid rgba(255,255,255,0.05);
        }
        .content-area::-webkit-scrollbar { width: 6px; }
        .content-area::-webkit-scrollbar-thumb { background: var(--primary); border-radius: 10px; }

        .section-title {
            color: var(--primary);
            border-right: 5px solid var(--primary);
            padding-right: 15px;
            margin: 30px 0 15px;
            font-size: 1.5rem;
        }

        .info-block {
            background: rgba(255,255,255,0.05);
            padding: 20px;
            border-radius: 15px;
            margin-bottom: 20px;
            border: 1px solid rgba(255,255,255,0.1);
        }

        .info-block h4 { color: #fff; margin-bottom: 10px; font-weight: 900; }
        .info-block p, .info-block li { color: #ccc; font-size: 0.95rem; line-height: 1.8; }
        .highlight { color: var(--primary); font-weight: bold; }

        .formula {
            background: #222;
            padding: 10px;
            border-radius: 8px;
            text-align: center;
            font-family: monospace;
            color: var(--primary);
            margin: 10px 0;
        }

        footer {
            padding: 15px 40px;
            background: rgba(0,0,0,0.2);
            display: flex;
            justify-content: space-between;
            font-size: 0.8rem;
            opacity: 0.8;
        }
    </style>
</head>
<body>

    <div class="app-window">
        <header>
            <div class="logo">XS.Boda</div>
            <div style="font-size: 0.9rem; font-weight: 300;">مشروع مقرر أسس التغذية الشامل 2026</div>
        </header>

        <main class="main-grid">
            <aside class="sidebar">
                <div class="card">
                    <h3 style="font-size: 1.1rem; color: var(--primary);"><i class="fas fa-users"></i> فريق العمل</h3>
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
                <div class="card" style="background: var(--dark); color: white; border: 1px solid var(--primary);">
                    <h4>جامعة عين شمس</h4>
                    <p style="font-size: 0.8rem; opacity: 0.7;">كلية التربية النوعية<br>قسم الاقتصاد المنزلي</p>
                </div>
            </aside>

            <div class="content-area">
                
                <h2 class="section-title">📚 ملخص المنهج - النظري</h2>
                
                <div class="info-block">
                    <h4>المفاهيم الأساسية</h4>
                    <p><strong>الغذاء:</strong> المادة التي يتناولها الكائن الحي.<br>
                    <strong>التغذية:</strong> العمليات التي يحول بها الجسم الغذاء إلى طاقة وأنسجة.<br>
                    <strong>الحالة الغذائية:</strong> حالة الجسم نتيجة لما يتناوله ومدى استفادته منه.</p>
                </div>

                <div class="info-block">
                    <h4>العناصر الغذائية الكبرى والصغرى</h4>
                    <ul>
                        <li><span class="highlight">الكربوهيدرات:</span> المصدر الرئيسي للطاقة (سكريات، نشويات).</li>
                        <li><span class="highlight">البروتينات:</span> أحجار البناء لترميم الأنسجة.</li>
                        <li><span class="highlight">الفيتامينات:</span> ذائبة في الدهون (A, D, E, K) وذائبة في الماء (C, B).</li>
                    </ul>
                </div>

                <div class="info-block">
                    <h4>الطاقة والقيمة الحرارية</h4>
                    <div class="formula">
                        1g كربوهيدرات = 4 سعرات | 1g بروتين = 4 سعرات | 1g دهون = 9 سعرات
                    </div>
                </div>

                <h2 class="section-title">🍳 الجزء العملي - الأسس والتجهيز</h2>

                <div class="info-block">
                    <h4>قواعد تجهيز الوجبات المثالية</h4>
                    <p>يجب مراعاة ميزانية الأسرة، تنسيق الألوان لتكون جذابة، تنوع القوام بين اللين والصلب، وتجنب تكرار الصنف الواحد في الوجبة.</p>
                </div>

                <div class="info-block">
                    <h4>طرق الطهي (الحرارة الرطبة)</h4>
                    <ul>
                        <li><span class="highlight">السلق:</span> الطهي في ماء مغلي (100°م).</li>
                        <li><span class="highlight">التسبيك:</span> الطهي في سائل محدود (ني x ني، خفيف، ثقيل).</li>
                        <li><span class="highlight">البخار:</span> طهي صحي تصل حرارته لـ 120°م.</li>
                    </ul>
                </div>

                <h2 class="section-title">🍕 دليل البيتزا والخميرة</h2>

                <div class="info-block">
                    <h4>عالم الخميرة</h4>
                    <p>هي كائنات دقيقة غنية بـ <span class="highlight">فيتامين B المركب</span>. تساعد في عملية التخمير لإنتاج غاز ثاني أكسيد الكربون الذي يرفع العجين.</p>
                    <div style="margin-top:10px; display: flex; gap: 10px; flex-wrap: wrap;">
                        <span style="background:var(--primary); padding:2px 10px; border-radius:10px; font-size:0.8rem;">خميرة بيرة</span>
                        <span style="background:var(--primary); padding:2px 10px; border-radius:10px; font-size:0.8rem;">خميرة جافة</span>
                    </div>
                </div>

                <div class="info-block">
                    <h4>سر نجاح البيتزا</h4>
                    <p>الاعتماد على جودة الدقيق (الجلوتين)، تفعيل الخميرة بالماء الدافئ (ليس مغلياً)، وفترة التخمير الكافية للحصول على ملمس هش.</p>
                </div>

            </div>
        </main>

        <footer>
            <div>تصميم مطور لعام 2026 | XS.Studio</div>
            <div><i class="fab fa-github"></i> تم الحفظ في GitHub</div>
        </footer>
    </div>

</body>
</html>
