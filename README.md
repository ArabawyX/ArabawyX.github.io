<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Xs.boda Dashboard</title>
    <link href="https://fonts.googleapis.com/css2?family=Amiri&family=Cairo:wght@300;600;900&display=swap" rel="stylesheet">
    <style>
        :root {
            --glass-bg: rgba(255, 255, 255, 0.07);
            --glass-border: rgba(255, 255, 255, 0.12);
            --text-main: #ffffff;
            --gold: #fbbf24;
            --accent-blue: #38bdf8;
        }

        * { box-sizing: border-box; }

        body, html {
            margin: 0; padding: 0; height: 100vh; width: 100vw;
            font-family: 'Cairo', sans-serif; color: var(--text-main);
            overflow: hidden; /* لمنع سكرول المتصفح الخارجي */
            background-image: url('https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?q=80&w=2070');
            background-size: cover; background-position: center;
        }

        /* الطبقة الضبابية الخلفية */
        .glass-overlay {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0, 0, 0, 0.35); backdrop-filter: blur(8px);
            z-index: -1;
        }

        /* الحاوية الكبرى المرتبة */
        .main-app {
            display: flex; flex-direction: column;
            height: 100vh; padding: 20px; gap: 15px;
            max-width: 1400px; margin: 0 auto;
        }

        /* 1. الناف بار العلوي */
        .top-nav {
            flex: 0 0 60px;
            background: var(--glass-bg);
            backdrop-filter: blur(15px);
            border: 1px solid var(--glass-border);
            border-radius: 50px;
            display: flex; align-items: center; justify-content: space-between;
            padding: 0 30px;
        }

        .logo { font-weight: 900; font-size: 1.5rem; letter-spacing: 1px; direction: ltr; }
        .nav-items { display: flex; gap: 20px; font-size: 0.9rem; opacity: 0.8; }

        /* 2. منطقة المحتوى الوسطى (البطاقة الكبيرة) */
        .dashboard-card {
            flex: 1;
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(20px);
            border: 1px solid var(--glass-border);
            border-radius: 40px;
            display: flex; overflow: hidden; /* مهم جداً */
            position: relative;
        }

        /* الجزء الأيمن (القائمة الجانبية داخل الكارت) */
        .side-info {
            width: 320px;
            background: rgba(255, 255, 255, 0.03);
            border-left: 1px solid var(--glass-border);
            padding: 30px;
            display: flex; flex-direction: column; gap: 20px;
        }

        .team-box {
            background: var(--glass-bg);
            padding: 20px; border-radius: 25px;
            border: 1px solid var(--glass-border);
            text-align: center;
        }

        .team-img {
            width: 70px; height: 70px; border-radius: 50%;
            border: 2px solid var(--gold); margin-bottom: 10px;
            object-fit: cover;
        }

        /* الجزء الأيسر (المحتوى القابل للتمرير) */
        .scrollable-content {
            flex: 1;
            padding: 40px;
            overflow-y: auto; /* هنا يحدث السكرول */
            scrollbar-width: thin;
            scrollbar-color: var(--gold) transparent;
        }

        /* ستايل الأكورديون (Details) */
        details {
            background: rgba(255, 255, 255, 0.04);
            margin-bottom: 10px; border-radius: 15px;
            border: 1px solid var(--glass-border);
        }
        summary {
            padding: 15px; cursor: pointer; font-weight: 600;
            display: flex; justify-content: space-between; align-items: center;
        }
        .inner-text { padding: 15px; border-top: 1px solid var(--glass-border); font-family: 'Amiri'; font-size: 1.1rem; color: #ddd; }

        /* كروت البيتزا المختصرة */
        .pizza-grid {
            display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 15px; margin-top: 20px;
        }
        .mini-card {
            background: var(--glass-bg); padding: 15px; border-radius: 20px; border: 1px solid var(--glass-border);
        }
        .mini-card img { width: 100%; height: 120px; object-fit: cover; border-radius: 15px; margin-bottom: 10px; }

        /* 3. الفوتر السفلي */
        .bottom-bar {
            flex: 0 0 80px;
            background: var(--glass-bg);
            backdrop-filter: blur(15px);
            border: 1px solid var(--glass-border);
            border-radius: 40px;
            display: flex; align-items: center; justify-content: space-between; padding: 0 30px;
        }

        .teacher-info { display: flex; align-items: center; gap: 12px; }
        .teacher-info img { width: 45px; height: 45px; border-radius: 50%; border: 2px solid var(--gold); }

        .big-number {
            position: absolute; top: 10px; left: 40px;
            font-size: 7rem; font-weight: 900; opacity: 0.05; pointer-events: none;
        }

        /* سكرول بار مخصص */
        .scrollable-content::-webkit-scrollbar { width: 6px; }
        .scrollable-content::-webkit-scrollbar-thumb { background: var(--gold); border-radius: 10px; }

        @media (max-width: 900px) {
            .side-info { display: none; }
            body { overflow-y: auto; height: auto; }
            .dashboard-card { height: 800px; }
        }
    </style>
</head>
<body>

    <div class="glass-overlay"></div>

    <div class="main-app">
        <nav class="top-nav">
            <div class="logo">Xs.boda</div>
            <div class="nav-items">
                <span>الرئيسية</span>
                <span>المناهج</span>
                <span>الاختبارات</span>
            </div>
            <div style="font-size: 1.2rem;">🌐</div>
        </nav>

        <div class="dashboard-card">
            <div class="big-number">01</div>
            
            <div class="scrollable-content">
                <h1 style="color: var(--gold); margin-top: 0;">منهج أسس التغذية</h1>
                <p style="opacity: 0.7;">استعرض محتوى الدليل الدراسي بشكل منظم وسريع.</p>
                
                <details open>
                    <summary>1. مفاهيم علم التغذية الأساسية <span>+</span></summary>
                    <div class="inner-text">
                        تتضمن دراسة الغذاء، التغذية، العناصر الغذائية، والحالة الصحية للجسم.
                    </div>
                </details>

                <details>
                    <summary>2. العناصر الكبرى والصغرى <span>+</span></summary>
                    <div class="inner-text">
                        الكربوهيدرات والبروتينات (طاقة وبناء) والفيتامينات والأملاح (وقاية).
                    </div>
                </details>

                <h3 style="margin-top: 30px; border-right: 3px solid var(--accent-blue); padding-right: 10px;">قسم المخبوزات والخميرة</h3>
                <div class="pizza-grid">
                    <div class="mini-card">
                        <img src="https://images.unsplash.com/photo-1594910609351-8636b13e029c?q=80&w=400" alt="خميرة">
                        <h4 style="margin: 5px 0;">أنواع الخميرة</h4>
                        <p style="font-size: 0.8rem; opacity: 0.6;">طبيعية، جافة، وبيرة طازجة.</p>
                    </div>
                    <div class="mini-card">
                        <img src="https://images.unsplash.com/photo-1513104890138-7c749659a591?q=80&w=400" alt="بيتزا">
                        <h4 style="margin: 5px 0;">سر نجاح العجين</h4>
                        <p style="font-size: 0.8rem; opacity: 0.6;">التخمير المضاعف والحرارة.</p>
                    </div>
                </div>
            </div>

            <div class="side-info">
                <button style="background: var(--gold); border: none; padding: 12px; border-radius: 15px; font-weight: 900; cursor: pointer;">دخول المنصة</button>
                
                <div class="team-box">
                    <img src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?q=80&w=200" class="team-img" alt="team">
                    <h4 style="margin: 5px 0;">فريق الإعداد</h4>
                    <ul style="list-style: none; padding: 0; font-size: 0.8rem; opacity: 0.8; line-height: 1.8;">
                        <li>عبدالرحمن مصطفى</li>
                        <li>عمر محسن</li>
                        <li>هنا محمود</li>
                        <li>فاطمة فايز</li>
                    </ul>
                </div>
            </div>
        </div>

        <footer class="bottom-bar">
            <div class="teacher-info">
                <img src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?q=80&w=100" alt="teacher">
                <div>
                    <div style="font-size: 0.9rem; font-weight: 600;">إشراف: أ. محمد عباس</div>
                    <div style="font-size: 0.7rem; opacity: 0.6;">خبير الاقتصاد المنزلي</div>
                </div>
            </div>
            <div style="text-align: center;">
                <div style="font-size: 0.8rem; letter-spacing: 2px;">2024 - 2025</div>
                <div style="font-size: 0.6rem; opacity: 0.5;">جميع الحقوق محفوظة</div>
            </div>
            <div style="background: rgba(255,255,255,0.1); width: 40px; height: 40px; border-radius: 50%; display: flex; align-items: center; justify-content: center; cursor: pointer;">
                ↑
            </div>
        </footer>
    </div>

</body>
</html>
