<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>دليل أسس التغذية | Xs.boda</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;700;900&family=Amiri:wght@400;700&family=Great+Vibes&display=swap');

        :root {
            --primary: #1a365d;
            --accent: #fbbf24;
            --success: #059669;
            --bg: #f0f4f8;
            --glass: rgba(255, 255, 255, 0.9);
            --card-shadow: 0 8px 32px rgba(31, 38, 135, 0.1);
        }

        * { box-sizing: border-box; margin: 0; padding: 0; }

        body {
            font-family: 'Cairo', sans-serif;
            background-color: var(--bg);
            color: #2d3748;
            line-height: 1.7;
        }

        /* الهيدر العصري */
        .hero {
            background: linear-gradient(rgba(26, 54, 93, 0.8), rgba(26, 54, 93, 0.8)), 
                        url('https://images.unsplash.com/photo-1513104890138-7c749659a591?auto=format&fit=crop&q=80&w=1200');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 80px 20px;
            text-align: center;
            border-bottom: 6px solid var(--accent);
        }

        .brand {
            font-family: 'Great Vibes', cursive;
            font-size: 5rem;
            color: var(--accent);
            margin-bottom: 10px;
            text-shadow: 3px 3px 6px rgba(0,0,0,0.3);
        }

        .course-title { font-size: 1.8rem; font-weight: 300; opacity: 0.9; }

        .students-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 15px;
            max-width: 1000px;
            margin: 40px auto 0;
        }

        .student-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(5px);
            padding: 12px;
            border-radius: 12px;
            font-family: 'Amiri', serif;
            font-size: 1.1rem;
            border: 1px solid rgba(255, 255, 255, 0.2);
            transition: 0.3s;
        }

        .student-card:hover { background: var(--accent); color: var(--primary); transform: translateY(-5px); }

        /* الحاوية الرئيسية */
        .main-container { max-width: 1000px; margin: -40px auto 40px; padding: 0 20px; }

        .content-card {
            background: var(--glass);
            padding: 40px;
            border-radius: 24px;
            box-shadow: var(--card-shadow);
            margin-bottom: 30px;
        }

        h1, h2 { color: var(--primary); margin-bottom: 20px; }

        /* تنسيق الأكورديون (Details) */
        details {
            background: white;
            margin-bottom: 15px;
            border-radius: 15px;
            border: 1px solid #e2e8f0;
            overflow: hidden;
            transition: 0.3s;
        }

        summary {
            padding: 18px;
            font-weight: 700;
            cursor: pointer;
            list-style: none;
            display: flex;
            justify-content: space-between;
            align-items: center;
            color: var(--primary);
        }

        summary::after { content: '←'; transition: 0.3s; color: var(--accent); }
        details[open] summary::after { transform: rotate(-90deg); }
        details[open] { border-right: 6px solid var(--success); }

        .details-body { padding: 20px; border-top: 1px solid #f0f4f8; background: #fafafa; }

        /* أقسام الصور والنصوص */
        .info-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            align-items: center;
            margin-bottom: 40px;
            padding: 20px;
            border-bottom: 1px solid #eee;
        }

        .info-row:nth-child(even) { direction: ltr; }
        .info-row:nth-child(even) .text-side { direction: rtl; }

        .image-side img {
            width: 100%;
            border-radius: 20px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
            object-fit: cover;
            height: 250px;
        }

        .tag {
            background: var(--accent);
            color: var(--primary);
            padding: 4px 15px;
            border-radius: 50px;
            font-size: 0.8rem;
            font-weight: 900;
            text-transform: uppercase;
        }

        .formula {
            background: #2d3748;
            color: #a0aec0;
            padding: 15px;
            border-radius: 10px;
            font-family: monospace;
            text-align: center;
            margin: 15px 0;
            direction: ltr;
        }

        /* التوافق مع الجوال */
        @media (max-width: 768px) {
            .info-row { grid-template-columns: 1fr; text-align: center; }
            .info-row:nth-child(even) { direction: rtl; }
            .brand { font-size: 3rem; }
            .content-card { padding: 20px; }
            .students-grid { grid-template-columns: 1fr 1fr; }
        }
    </style>
</head>
<body>

    <header class="hero">
        <h1 class="brand">Xs.boda</h1>
        <h2 class="course-title">أسس التغذية / الاقتصاد المنزلي</h2>
        <div class="students-grid">
            <div class="student-card">عبدالرحمن مصطفى عويس</div>
            <div class="student-card">عمر محسن عبد العزيز</div>
            <div class="student-card">علي عباس علي</div>
            <div class="student-card">صبري حاتم صبري</div>
            <div class="student-card">هنا محمود مصطفي</div>
            <div class="student-card">منه رجب عبد التواب</div>
            <div class="student-card">هدير احمد مصطفي</div>
            <div class="student-card">ياسمين ابراهيم احمد</div>
            <div class="student-card">فاطمه فايز منصور</div>
            <div class="student-card">منه الله وليد فاروق</div>
        </div>
    </header>

    <div class="main-container">
        
        <section class="content-card">
            <h1 style="text-align: center;">📚 ملخص منهج أسس التغذية</h1>
            
            <details>
                <summary>1. مقدمة في علم التغذية</summary>
                <div class="details-body">
                    <p><strong>الغذاء:</strong> المادة التي يتناولها الكائن الحي.</p>
                    <p><strong>التغذية:</strong> العمليات الحيوية لتحويل الغذاء إلى طاقة.</p>
                </div>
            </details>

            <details>
                <summary>2. العناصر الغذائية الكبرى (Macronutrients)</summary>
                <div class="details-body">
                    <p>تشمل الكربوهيدرات (طاقة)، البروتينات (بناء)، والدهون (تخزين).</p>
                </div>
            </details>

            <details>
                <summary>3. الفيتامينات وأعراض النقص</summary>
                <div class="details-body">
                    <ul>
                        <li><span style="color: #e53e3e;">فيتامين A:</span> العشى الليلي.</li>
                        <li><span style="color: #3182ce;">فيتامين D:</span> لين العظام.</li>
                        <li><span style="color: #38a169;">فيتامين C:</span> الإسقربوط.</li>
                    </ul>
                </div>
            </details>
        </section>

        <section class="content-card">
            <h1 style="text-align: center; margin-bottom: 40px;">🍕 دليل الخميرة والبيتزا الشامل</h1>

            <div class="info-row">
                <div class="text-side">
                    <span class="tag">الأساسيات</span>
                    <h2>أنواع الخميرة</h2>
                    <p>الخميرة كائنات حية دقيقة غنية ببروتين وفيتامين B. تتوفر كخميرة بيرة طازجة أو خميرة جافة نشطة.</p>
                </div>
                <div class="image-side">
                    <img src="https://images.unsplash.com/photo-1589113243528-98e388fc40e0?auto=format&fit=crop&q=80&w=500" alt="Yeast">
                </div>
            </div>

            <div class="info-row">
                <div class="text-side">
                    <span class="tag">الكيمياء</span>
                    <h2>معادلة التخمير</h2>
                    <p>تحتاج الخميرة للدفء والغذاء (السكر) والرطوبة لتنتج غاز ثاني أكسيد الكربون الذي يرفع العجين.</p>
                    <div class="formula">Sucrose → Glucose → Alcohol + CO2</div>
                </div>
                <div class="image-side">
                    <img src="https://images.unsplash.com/photo-1555126634-323283e090fa?auto=format&fit=crop&q=80&w=500" alt="Fermentation">
                </div>
            </div>

            <div class="info-row">
                <div class="text-side">
                    <span class="tag">التحضير</span>
                    <h2>مراحل نمو العجين</h2>
                    <ol style="margin-right: 20px;">
                        <li>النشاط الأولي.</li>
                        <li>تضاعف الحجم (التخمير الأول).</li>
                        <li>التشكيل والراحة.</li>
                    </ol>
                </div>
                <div class="image-side">
                    <img src="https://images.unsplash.com/photo-1571407970349-bc81e7e96d47?auto=format&fit=crop&q=80&w=500" alt="Dough Growth">
                </div>
            </div>

            <div class="info-row">
                <div class="text-side">
                    <span class="tag">النتيجة النهائية</span>
                    <h2>الخبز والحشو</h2>
                    <p>يخبز في فرن حار جداً. يمكن استخدام حشوات متنوعة مثل الجبن الرومي، الأنشوجة، الزيتون، وزيت الزيتون البكر.</p>
                </div>
                <div class="image-side">
                    <img src="https://images.unsplash.com/photo-1565299624946-b28f40a0ae38?auto=format&fit=crop&q=80&w=500" alt="Final Pizza">
                </div>
            </div>
        </section>

    </div>

</body>
</html>
