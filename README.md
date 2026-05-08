<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>XS.Boda | مشروع أسس التغذية</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;600;900&family=Amiri:wght@700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    
    <style>
        :root {
            --primary-accent: #d4a373;
            --glass: rgba(255, 255, 255, 0.15);
            --glass-heavy: rgba(255, 255, 255, 0.25);
            --dark-card: rgba(30, 30, 30, 0.85);
            --text-main: #2d2d2d;
            --transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
        }

        /* أنيميشن الظهور */
        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        * { box-sizing: border-box; margin: 0; padding: 0; }

        body {
            font-family: 'Cairo', sans-serif;
            background: url('https://images.unsplash.com/photo-1473580044384-7ba9967e16a0?auto=format&fit=crop&q=80&w=2000') no-repeat center center fixed;
            background-size: cover;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            direction: rtl;
        }

        /* الحاوية الرئيسية الزجاجية */
        .app-container {
            width: 92%;
            max-width: 1200px;
            height: 85vh;
            background: var(--glass);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255,255,255,0.3);
            border-radius: 40px;
            display: flex;
            flex-direction: column;
            box-shadow: 0 25px 50px rgba(0,0,0,0.2);
            animation: fadeInUp 1s ease-out;
        }

        /* الهيدر العلوي */
        .nav-bar {
            padding: 25px 50px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid rgba(255,255,255,0.1);
        }

        .logo { font-family: 'Amiri', serif; font-size: 2.5rem; color: var(--text-main); font-weight: 900; }

        .nav-items { display: flex; gap: 30px; list-style: none; }
        .nav-items a { text-decoration: none; color: var(--text-main); font-weight: 600; font-size: 0.9rem; opacity: 0.7; transition: var(--transition); }
        .nav-items a:hover { opacity: 1; color: var(--primary-accent); }

        /* منطقة المحتوى */
        .main-grid {
            flex: 1;
            display: grid;
            grid-template-columns: 300px 1fr 280px;
            gap: 25px;
            padding: 30px;
            overflow: hidden;
        }

        /* بطاقة الطلاب (اليسار) */
        .students-card {
            background: white;
            border-radius: 30px;
            padding: 30px;
            display: flex;
            flex-direction: column;
            animation: fadeInUp 1.2s ease-out;
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
        }

        .students-card h3 { font-weight: 900; margin-bottom: 20px; font-size: 1.2rem; color: #1a1a1a; }
        
        .list-container { flex: 1; overflow-y: auto; padding-right: 5px; }
        .list-container::-webkit-scrollbar { width: 4px; }
        .list-container::-webkit-scrollbar-thumb { background: #eee; border-radius: 10px; }
        
        .students-list { list-style: none; }
        .students-list li { padding: 8px 0; border-bottom: 1px solid #f5f5f5; font-size: 0.9rem; color: #555; transition: var(--transition); }
        .students-list li:hover { padding-right: 10px; color: var(--primary-accent); }

        .img-box {
            height: 150px;
            background: url('https://images.unsplash.com/photo-1542291026-7eec264c27ff?auto=format&fit=crop&q=80&w=500') center;
            background-size: cover;
            border-radius: 20px;
            margin-top: 20px;
            filter: grayscale(0.5);
            transition: var(--transition);
        }
        .students-card:hover .img-box { filter: grayscale(0); transform: scale(1.02); }

        /* البطاقة المركزية (العملي) */
        .hero-card {
            background: var(--dark-card);
            border-radius: 35px;
            padding: 40px;
            color: white;
            position: relative;
            overflow: hidden;
            display: flex;
            flex-direction: column;
            animation: fadeInUp 1.4s ease-out;
        }

        .hero-card::after {
            content: "";
            position: absolute;
            top: 0; left: 0; right: 0; bottom: 0;
            background: url('https://images.unsplash.com/photo-1552346154-21d32810aba3?auto=format&fit=crop&q=80&w=800') no-repeat center;
            background-size: 70%;
            opacity: 0.15;
            z-index: 0;
            pointer-events: none;
        }

        .tag { background: rgba(255,255,255,0.1); padding: 6px 15px; border-radius: 20px; font-size: 0.7rem; letter-spacing: 2px; width: fit-content; }
        
        .hero-content { z-index: 1; margin-top: 20px; }
        .hero-content h2 { font-size: 2.8rem; font-weight: 900; line-height: 1.2; }
        .hero-content p { color: #aaa; margin: 15px 0 25px; font-size: 1rem; }

        .info-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; z-index: 1; }
        .info-item h4 { color: var(--primary-accent); font-size: 0.9rem; margin-bottom: 5px; }
        .info-item p { font-size: 0.85rem; color: #ddd; }

        /* الأكشن (اليمين) */
        .actions-col { display: flex; flex-direction: column; gap: 20px; animation: fadeInUp 1.6s ease-out; }
        .mini-card { background: var(--glass-heavy); border-radius: 25px; padding: 25px; border: 1px solid rgba(255,255,255,0.1); }
        .mini-card h4 { font-size: 1rem; margin-bottom: 10px; }
        .mini-card p { font-size: 0.8rem; opacity: 0.7; margin-bottom: 15px; }
        
        .btn {
            background: white;
            color: black;
            border: none;
            padding: 12px;
            border-radius: 15px;
            width: 100%;
            font-weight: 700;
            cursor: pointer;
            transition: var(--transition);
        }
        .btn:hover { background: var(--primary-accent); color: white; transform: translateY(-3px); }

        /* الفوتر العائم */
        .floating-footer {
            width: 80%;
            background: var(--glass-heavy);
            backdrop-filter: blur(10px);
            margin: -35px auto 20px;
            border-radius: 30px;
            padding: 15px 40px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border: 1px solid rgba(255,255,255,0.2);
            animation: fadeInUp 1.8s ease-out;
        }

        .footer-left { display: flex; align-items: center; gap: 15px; }
        .circle-btn { width: 45px; height: 45px; border-radius: 50%; background: var(--text-main); color: white; border: none; cursor: pointer; display: flex; align-items: center; justify-content: center; transition: var(--transition); }
        .circle-btn:hover { background: var(--primary-accent); transform: rotate(-45deg); }

        @media (max-width: 900px) {
            .main-grid { grid-template-columns: 1fr; overflow-y: auto; }
            .app-container { height: auto; }
            body { overflow-y: auto; padding: 20px 0; }
        }
    </style>
</head>
<body>

    <div class="app-container">
        <nav class="nav-bar">
            <div class="logo">XS.Boda</div>
            <ul class="nav-items">
                <li><a href="#">الرئيسية</a></li>
                <li><a href="#">المشاريع</a></li>
                <li><a href="#">الفريق</a></li>
            </ul>
            <div style="display: flex; gap: 20px; align-items: center;">
                <i class="fa-solid fa-earth-americas"></i>
                <button style="background: white; border:none; padding: 8px 20px; border-radius: 20px; font-weight:700; cursor:pointer;">دخول</button>
            </div>
        </nav>

        <main class="main-grid">
            
            <aside class="students-card">
                <h3>إعداد الطلاب</h3>
                <div class="list-container">
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
                <div class="img-box"></div>
            </aside>

            <section class="hero-card">
                <div class="tag">PRO PROJECT 2026</div>
                <div class="hero-content">
                    <h2>مقرر أسس الغذاء<br>والتغذية (العملي)</h2>
                    <p>كلية التربية النوعية - جامعة عين شمس</p>
                    
                    <div class="info-grid">
                        <div class="info-item">
                            <h4>01 المكونات الأساسية</h4>
                            <p>البروتينات، الكربوهيدرات، الدهون، الأملاح، والفيتامينات.</p>
                        </div>
                        <div class="info-item">
                            <h4>02 القواعد الذهبية</h4>
                            <p>تنسيق الألوان، تنوع القوام، وتجنب التكرار في الأصناف.</p>
                        </div>
                        <div class="info-item">
                            <h4>03 أثر الحرارة</h4>
                            <p>تكسير ألياف الخضر وتليين اللحوم وقتل الميكروبات الضارة.</p>
                        </div>
                        <div class="info-item">
                            <h4>04 طرق الطهي</h4>
                            <p>السلق، التسبيك، التشريب، والطهي بالبخار الصحي.</p>
                        </div>
                    </div>
                </div>
            </section>

            <div class="actions-col">
                <div class="mini-card">
                    <h4>أساسيات الخميرة</h4>
                    <p>كائنات دقيقة غنية بفيتامين B المركب والبروتينات الضرورية لبناء الجسم.</p>
                    <button class="btn">اكتشف المزيد</button>
                </div>
                <div class="mini-card" style="margin-top: auto; background: var(--text-main); color: white;">
                    <h4>حالة المشروع</h4>
                    <p>تم تحديث البيانات لعام 2026 بنجاح.</p>
                    <button class="btn" style="background: var(--primary-accent); color: white;">تحديث <i class="fa-solid fa-rotate"></i></button>
                </div>
            </div>
        </main>
    </div>

    <footer class="floating-footer">
        <div class="footer-left">
            <div style="width: 40px; height: 40px; background: #eee; border-radius: 10px; display: flex; align-items: center; justify-content: center; font-weight: 900;">XS</div>
            <div>
                <p style="font-size: 0.9rem; font-weight: 900;">NEW • COSMIC SET 237</p>
                <p style="font-size: 0.7rem; opacity: 0.6;">Designed by XS.Studio | 2026 Collection</p>
            </div>
        </div>
        <button class="circle-btn">
            <i class="fa-solid fa-arrow-up-right-from-square"></i>
        </button>
    </footer>

</body>
</html>
