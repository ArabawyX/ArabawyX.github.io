<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>XS.Boda | المرجع الشامل لعلوم التغذية</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;600;900&family=Amiri:wght@700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    
    <style>
        :root {
            --primary: #d4a373;
            --accent: #e67e22;
            --dark-bg: #0f172a;
            --glass: rgba(255, 255, 255, 0.08);
            --glass-border: rgba(255, 255, 255, 0.15);
            --card-white: #ffffff;
            --text-main: #334155;
            --transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        * { box-sizing: border-box; margin: 0; padding: 0; scroll-behavior: smooth; }

        body {
            font-family: 'Cairo', sans-serif;
            background: linear-gradient(135deg, rgba(15, 23, 42, 0.9), rgba(30, 41, 59, 0.8)), 
                        url('https://images.unsplash.com/photo-1505935428862-770b6f24f629?auto=format&fit=crop&q=80&w=2000') no-repeat center center fixed;
            background-size: cover;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
            direction: rtl;
            color: #f8fafc;
        }

        .app-window {
            width: 100%;
            max-width: 1400px;
            background: var(--glass);
            backdrop-filter: blur(30px);
            -webkit-backdrop-filter: blur(30px);
            border: 1px solid var(--glass-border);
            border-radius: 35px;
            display: flex;
            flex-direction: column;
            box-shadow: 0 50px 100px rgba(0,0,0,0.5);
            overflow: hidden;
            animation: fadeIn 1s ease-out;
        }

        @keyframes fadeIn { from { opacity: 0; transform: scale(0.95); } to { opacity: 1; transform: scale(1); } }

        header {
            padding: 25px 50px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid rgba(255,255,255,0.1);
            background: rgba(0,0,0,0.2);
        }

        .logo { font-family: 'Amiri', serif; font-size: 2.5rem; color: var(--primary); text-shadow: 0 0 20px rgba(212, 163, 115, 0.3); }

        .main-grid {
            display: grid;
            grid-template-columns: 340px 1fr;
            gap: 25px;
            padding: 30px;
        }

        @media (max-width: 1100px) { .main-grid { grid-template-columns: 1fr; } .sidebar { order: 2; } .content-area { order: 1; height: auto !important; } }

        /* الجانب الأيمن */
        .sidebar { display: flex; flex-direction: column; gap: 20px; }
        
        .card {
            background: var(--card-white);
            border-radius: 25px;
            padding: 25px;
            color: var(--text-main);
            box-shadow: 0 15px 35px rgba(0,0,0,0.2);
            transition: var(--transition);
        }
        .card:hover { transform: translateY(-10px); }

        .students-list { list-style: none; margin-top: 15px; }
        .students-list li { 
            padding: 10px 15px; 
            margin-bottom: 8px; 
            background: #f1f5f9; 
            border-radius: 12px; 
            font-size: 0.9rem; 
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        .students-list li::before { content: "\f501"; font-family: "Font Awesome 5 Free"; font-weight: 900; color: var(--primary); }

        /* منطقة المحتوى المعرفي */
        .content-area {
            background: rgba(0,0,0,0.25);
            border-radius: 30px;
            padding: 40px;
            height: 75vh;
            overflow-y: auto;
            border: 1px solid rgba(255,255,255,0.05);
        }
        .content-area::-webkit-scrollbar { width: 8px; }
        .content-area::-webkit-scrollbar-thumb { background: var(--primary); border-radius: 10px; }

        .section-header {
            display: flex;
            align-items: center;
            gap: 15px;
            margin: 40px 0 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--primary);
        }
        .section-header i { font-size: 1.8rem; color: var(--primary); }
        .section-header h2 { font-size: 1.8rem; font-weight: 900; }

        .info-card {
            background: rgba(255,255,255,0.03);
            border: 1px solid rgba(255,255,255,0.08);
            border-radius: 20px;
            padding: 25px;
            margin-bottom: 25px;
            transition: var(--transition);
        }
        .info-card:hover { background: rgba(255,255,255,0.06); border-color: var(--primary); }

        .info-card h4 { color: var(--primary); margin-bottom: 15px; font-size: 1.2rem; display: flex; align-items: center; gap: 10px; }
        .info-card p, .info-card li { font-size: 1rem; line-height: 1.8; color: #cbd5e1; margin-bottom: 10px; }
        
        .badge { background: var(--accent); color: white; padding: 2px 12px; border-radius: 8px; font-size: 0.8rem; margin-right: 5px; }
        .highlight { color: #fff; font-weight: 700; border-bottom: 1px dashed var(--primary); }

        .formula-box {
            background: #000;
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            border: 1px solid var(--primary);
            margin: 20px 0;
        }
        .formula-box code { font-size: 1.2rem; color: var(--primary); font-family: 'Courier New', Courier, monospace; }

        footer {
            padding: 20px 50px;
            background: rgba(0,0,0,0.4);
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 0.85rem;
            color: #94a3b8;
        }

        .tag-cloud { display: flex; gap: 10px; flex-wrap: wrap; margin-top: 10px; }
        .tag-cloud span { background: rgba(212, 163, 115, 0.2); border: 1px solid var(--primary); padding: 4px 12px; border-radius: 20px; font-size: 0.75rem; color: var(--primary); }

    </style>
</head>
<body>

    <div class="app-window">
        <header>
            <div class="logo">XS.Boda</div>
            <div style="text-align: left;">
                <p style="font-weight: 900; letter-spacing: 1px;">أسس التغذية الشاملة</p>
                <p style="font-size: 0.7rem; opacity: 0.6;">إصدار التحديث الأكاديمي 2026</p>
            </div>
        </header>

        <main class="main-grid">
            <aside class="sidebar">
                <div class="card">
                    <h3 style="color: var(--dark-bg); font-weight: 900;"><i class="fas fa-graduation-cap"></i> فريق الباحثين</h3>
                    <ul class="students-list">
                        <li>عبدالرحمن مصطفى عويس</li>
                        <li>عمر محسن عبد العزيز</li>
                        <li>علي عباس علي</li>
                        <li>صبري حاتم صبري</li>
                        <li>هنا محمود مصطفي</li>
                        <li>منه رجب عبد التواب</li>
                        <li>هدير احمد مصطفي</li>
                        <li>ياسمين ابراهيم احمد</li>
                        <li>فاطمه فايز منصور</li>
                        <li>منه الله وليد فاروق</li>
                    </ul>
                </div>
                
                <div class="card" style="background: var(--dark-bg); color: white;">
                    <h4 style="color: var(--primary); margin-bottom: 10px;">إحصائيات المنهج</h4>
                    <p style="font-size: 0.8rem; line-height: 1.6; opacity: 0.8;">تم دمج 12 وحدة تعليمية، 45 عنصر غذائي، و 18 طريقة طهي فنية ضمن هذا النظام.</p>
                </div>
            </aside>

            <div class="content-area">
                
                <div class="section-header">
                    <i class="fas fa-book-open"></i>
                    <h2>المفاهيم النظرية المتقدمة</h2>
                </div>

                <div class="info-card">
                    <h4>١. التمثيل الغذائي (Metabolism) <span class="badge">مفهوم حيوي</span></h4>
                    <p>ينقسم إلى عمليتين متكاملتين:</p>
                    <ul>
                        <li><span class="highlight">عملية البناء (Anabolism):</span> استخدام الطاقة لبناء أنسجة جديدة وترميم التالف.</li>
                        <li><span class="highlight">عملية الهدم (Catabolism):</span> تكسير الروابط الكيميائية في الغذاء لتحرير الطاقة.</li>
                    </ul>
                </div>

                <div class="info-card">
                    <h4>٢. تفاصيل الألياف الغذائية</h4>
                    <p>ليست مجرد فضلات، بل هي ضرورية لصحة الجهاز الهضمي:</p>
                    <ul>
                        <li><span class="highlight">ألياف ذائبة:</span> تساعد في خفض مستوى الكوليسترول وتنظيم السكر.</li>
                        <li><span class="highlight">ألياف غير ذائبة:</span> تزيد من حركة الأمعاء وتقي من الإمساك.</li>
                    </ul>
                </div>

                <div class="info-card">
                    <h4>٣. الأملاح المعدنية الدقيقة</h4>
                    <p>يحتاجها الجسم بكميات ضئيلة لكن تأثيرها حاسم:</p>
                    <ul>
                        <li><span class="highlight">اليود:</span> ضروري لعمل الغدة الدرقية.</li>
                        <li><span class="highlight">الزنك:</span> يدعم جهاز المناعة وسرعة التئام الجروح.</li>
                        <li><span class="highlight">البوتاسيوم:</span> توازن السوائل ونبضات القلب.</li>
                    </ul>
                </div>

                <div class="section-header">
                    <i class="fas fa-blender"></i>
                    <h2>التقنيات العملية والطهي الفني</h2>
                </div>

                <div class="info-card">
                    <h4>١. كيمياء الحرارة في الغذاء</h4>
                    <p>ماذا يحدث فعلياً عند الطهي؟</p>
                    <ul>
                        <li><span class="highlight">تجلط البروتين:</span> تحول البروتين من الحالة السائلة للصلبة (مثل البيض).</li>
                        <li><span class="highlight">كرملة السكر:</span> تغير لون السكر للنبي عند التعرض للحرارة الجافة.</li>
                        <li><span class="highlight">تجلتن النشا:</span> انتفاخ حبيبات النشا بامتصاص الماء الساخن لتكوين قوام غليظ.</li>
                    </ul>
                </div>

                <div class="info-card">
                    <h4>٢. معايير سلامة الغذاء (HACCP)</h4>
                    <p>تجهيز الوجبة يتطلب مراقبة "نقاط التحكم الحرجة":</p>
                    <ul>
                        <li><span class="highlight">منطقة الخطر:</span> هي الحرارة بين (٥ - ٦٠ درجة مئوية) حيث تنشط البكتيريا.</li>
                        <li><span class="highlight">التبريد السريع:</span> ضروري لمنع نمو السموم في الوجبات المطهية.</li>
                    </ul>
                </div>

                <div class="section-header">
                    <i class="fas fa-pizza-slice"></i>
                    <h2>تكنولوجيا المخبوزات والخمائر</h2>
                </div>

                <div class="info-card">
                    <h4>١. دور الجلوتين (Gluten)</h4>
                    <p>هو البروتين الناتج عن اتحاد "الجليادين" و "الجلوتينين" في الدقيق عند إضافة الماء. هو الذي يعطي العجين <span class="highlight">المرونة والقدرة على حبس الغازات</span>.</p>
                </div>

                <div class="info-card">
                    <h4>٢. التخمر الحيوي</h4>
                    <p>تقوم الخميرة بتحويل السكريات البسيطة إلى:</p>
                    <div class="formula-box">
                        <code>C₆H₁₂O₆ (سكر) → 2C₂H₅OH (كحول) + 2CO₂ (ثاني أكسيد كربون)</code>
                    </div>
                    <p>غاز CO₂ هو المسؤول عن نفش العجين وجعله خفيفاً ومسامياً.</p>
                </div>

                <div class="tag-cloud">
                    <span>حموضة العجين</span>
                    <span>درجة الحرارة المثالية (٣٥°م)</span>
                    <span>النشاط الإنزيمي</span>
                    <span>الأميلوز</span>
                    <span>تفاعلات مايارد</span>
                </div>

            </div>
        </main>

        <footer>
            <div>تم تطويره بواسطة فريق XS.Boda | حقوق المحتوى محفوظة لجامعة عين شمس</div>
            <div>
                <i class="fab fa-github" style="margin-left: 15px;"></i>
                <i class="fas fa-shield-alt"></i> مؤمن بنظام التشفير 2026
            </div>
        </footer>
    </div>

</body>
</html>
