<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>منهج أسس التغذية والاقتصاد المنزلي | Xs.boda</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&family=Cairo:wght@300;600;900&display=swap" rel="stylesheet">
    
    <style>
        /* ==============================
           1. المتغيرات والأساسيات (Reset & Variables)
           ============================== */
        :root {
            /* ألوان متلائمة مع التصميم الزجاجي */
            --glass-bg: rgba(255, 255, 255, 0.08); /* خلفية بيضاء شفافة جداً */
            --glass-border: rgba(255, 255, 255, 0.15); /* حدود بيضاء خفيفة */
            --blur-strength: 15px; /* قوة التأثير البلوري */
            
            /* ألوان النص */
            --text-main: #f8fafc; /* أبيض مائل للزرقة */
            --text-sub: #cbd5e1; /* رمادي فاتح */
            
            /* ألوان مميزة (Accents) */
            --gold: #fbbf24;
            --pizza-primary: #38bdf8; /* أزرق فاتح */
            --pizza-accent: #f97316; /* برتقالي */
            
            /* ألوان لأقسام التفاصيل (Accordions) */
            --acc-nutrition: #34d399; /* أخضر */
            --acc-blue: #38bdf8; /* أزرق */
            --acc-pizza: #f87171; /* أحمر */
            --acc-gold: #fbbf24; /* ذهبي */
        }

        body, html {
            height: 100%;
            margin: 0;
            padding: 0;
            font-family: 'Cairo', sans-serif;
            color: var(--text-main);
            overflow-x: hidden;
        }

        /* صورة خلفية كاملة وبلورية */
        body {
            /* ملاحظة: يمكنك استبدال الرابط أدناه بصورتك الخاصة */
            background-image: url('https://images.unsplash.com/photo-1518770660439-4636190af475?q=80&w=2070');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
        }

        /* طبقة بلورية فوق الخلفية */
        .glass-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.4); /* تظليل داكن */
            backdrop-filter: blur(10px); /* تأثير بلوري */
            -webkit-backdrop-filter: blur(10px); /* للتوافق مع Safari */
            z-index: -1;
        }

        a { text-decoration: none; color: inherit; }
        ul { list-style: none; padding: 0; margin: 0; }
        
        /* ==============================
           2. شريط التنقل العلوي (Top Nav)
           ============================== */
        .top-nav {
            position: fixed;
            top: 20px;
            left: 50%;
            transform: translateX(-50%);
            width: 90%;
            max-width: 1200px;
            height: 60px;
            background: var(--glass-bg);
            backdrop-filter: blur(var(--blur-strength));
            -webkit-backdrop-filter: blur(var(--blur-strength));
            border: 1px solid var(--glass-border);
            border-radius: 30px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 30px;
            z-index: 1000;
        }

        .brand-logo-top {
            font-size: 1.8rem;
            font-weight: 900;
            letter-spacing: 2px;
            color: var(--text-main);
            direction: ltr; /* لضمان قراءة Xs.boda بشكل صحيح */
        }

        .nav-links {
            display: flex;
            gap: 25px;
        }

        .nav-link {
            font-size: 1.1rem;
            color: var(--text-sub);
            transition: color 0.3s ease;
        }

        .nav-link:hover { color: var(--gold); }

        .nav-icons {
            display: flex;
            gap: 15px;
            font-size: 1.2rem;
            color: var(--text-sub);
        }

        /* ==============================
           3. المحتوى الرئيسي (Main Container)
           ============================== */
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 120px auto 40px; /* تباعد من الأعلى للـ Nav */
            display: flex;
            flex-direction: column;
            gap: 40px;
        }

        /* ==============================
           4. قسم الهيدر الأساسي (Hero Header)
           ============================== */
        .main-header {
            background: var(--glass-bg);
            backdrop-filter: blur(var(--blur-strength));
            -webkit-backdrop-filter: blur(var(--blur-strength));
            border: 1px solid var(--glass-border);
            border-radius: 20px;
            padding: 60px;
            display: flex;
            flex-wrap: wrap;
            gap: 40px;
            position: relative;
        }

        .header-content-left {
            flex: 1;
            min-width: 300px;
        }

        .brand-name {
            font-weight: 900;
            font-size: 3.5rem;
            margin: 0;
            color: var(--gold);
            direction: ltr;
        }

        .course-name {
            font-weight: 600;
            font-size: 1.8rem;
            margin: 10px 0 30px;
            color: var(--text-main);
        }

        .students-section {
            display: flex;
            gap: 20px;
            align-items: flex-start;
        }

        .team-image-container {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            border: 3px solid var(--glass-border);
            overflow: hidden;
        }

        /* ملاحظة: يمكنك استبدال الرابط أدناه بصورتك الخاصة */
        .team-image {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .students-list-wrapper {
            flex: 1;
        }

        .students-title {
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: 10px;
            color: var(--text-sub);
        }

        .students-list {
            font-family: 'Amiri', serif;
            font-size: 1rem;
            color: var(--text-sub);
            display: flex;
            flex-direction: column;
            gap: 3px;
        }

        .students-list li:hover { color: var(--gold); cursor: default; }

        .header-content-right {
            width: 30%;
            min-width: 250px;
            display: flex;
            flex-direction: column;
            gap: 20px;
            align-items: flex-end;
            justify-content: flex-start;
        }

        .header-btn {
            background: rgba(251, 191, 36, 0.1);
            color: var(--gold);
            border: 1px solid var(--gold);
            padding: 10px 25px;
            border-radius: 20px;
            font-weight: 600;
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .header-btn:hover {
            background: var(--gold);
            color: rgba(0,0,0,0.8);
        }

        /* رقم 01 المزخرف */
        .decorative-number {
            font-size: 8rem;
            font-weight: 900;
            color: rgba(251, 191, 36, 0.05); /* ذهبي خافت جداً */
            position: absolute;
            bottom: -20px;
            right: 40px;
            pointer-events: none;
        }

        /* ==============================
           5. قسم الدليل والتفاصيل (Accordions)
           ============================== */
        .curriculum-section {
            background: var(--glass-bg);
            backdrop-filter: blur(var(--blur-strength));
            -webkit-backdrop-filter: blur(var(--blur-strength));
            border: 1px solid var(--glass-border);
            border-radius: 20px;
            padding: 40px;
        }

        .main-title {
            text-align: center;
            font-size: 2.2rem;
            font-weight: 900;
            color: var(--text-main);
            margin-bottom: 40px;
        }

        .nutrition-section-title {
            background-color: var(--acc-nutrition);
            color: rgba(0,0,0,0.8);
            padding: 12px 20px;
            border-radius: 10px;
            margin-top: 30px;
            margin-bottom: 15px;
            font-size: 1.3rem;
            font-weight: 600;
        }

        /* تنسيقات الأكورديون البلوري */
        details {
            background: rgba(255, 255, 255, 0.02);
            margin-bottom: 15px;
            padding: 18px;
            border-radius: 15px;
            border: 1px solid var(--glass-border);
            transition: background 0.3s ease;
        }

        details:hover { background: rgba(255, 255, 255, 0.05); }

        summary {
            font-weight: bold;
            font-size: 1.1rem;
            cursor: pointer;
            outline: none;
            list-style: none;
            color: var(--text-main);
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        summary::after {
            content: "➕";
            font-size: 0.9em;
            color: var(--text-sub);
        }

        details[open] summary::after { content: "➖"; }

        .details-content {
            padding: 15px 10px 0;
            border-top: 1px solid var(--glass-border);
            margin-top: 15px;
            font-family: 'Amiri', serif;
            font-size: 1.1rem;
            color: var(--text-sub);
        }

        .details-content li { list-style-type: disc; margin-right: 20px; }

        .highlight { color: var(--pizza-accent); font-weight: bold; }

        /* تغيير ألوان كل تفصيل */
        .det-nutrition summary { color: var(--acc-nutrition); }
        .det-blue summary { color: var(--acc-blue); }
        .det-pizza summary { color: var(--acc-pizza); }
        .det-gold summary { color: var(--acc-gold); }

        /* ==============================
           6. قسم البيتزا والخميرة (Pizza Section)
           ============================== */
        .pizza-section {
            background: var(--glass-bg);
            backdrop-filter: blur(var(--blur-strength));
            -webkit-backdrop-filter: blur(var(--blur-strength));
            border: 1px solid var(--glass-border);
            border-radius: 20px;
            padding: 40px;
        }

        .pizza-header {
            text-align: center;
            padding: 20px;
            border-bottom: 1px solid var(--glass-border);
            margin-bottom: 40px;
        }

        .pizza-header h2 { font-size: 2rem; color: var(--pizza-primary); margin: 0; }
        .pizza-header p { color: var(--text-sub); opacity: 0.8; margin-top: 5px; }

        /* كروت الأجزاء (Part Cards) */
        .topic-card {
            background: rgba(255, 255, 255, 0.01);
            border: 1px solid var(--glass-border);
            border-radius: 15px;
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 30px;
            padding: 20px;
            align-items: center;
            transition: all 0.3s ease;
        }

        .topic-card:hover { transform: translateY(-3px); background: rgba(255, 255, 255, 0.03); }
        .topic-card:last-child { margin-bottom: 0; }

        .topic-content {
            flex: 1;
            min-width: 300px;
        }

        .topic-content h2 {
            color: var(--pizza-primary);
            padding-right: 10px;
            margin-top: 0;
            font-size: 1.5rem;
            position: relative;
        }

        .topic-content h2::after {
            content: "";
            position: absolute;
            top: 50%;
            right: 0;
            transform: translateY(-50%);
            width: 4px;
            height: 100%;
            background-color: var(--pizza-accent);
            border-radius: 2px;
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

        .topic-content p, .topic-content li { color: var(--text-sub); }
        .topic-content li { list-style-type: circle; margin-right: 15px; }

        /* حاوية الصورة المتجاوبة */
        .image-placeholder {
            flex: 0 0 250px;
            height: 200px;
            border: 2px dashed var(--pizza-primary);
            border-radius: 10px;
            overflow: hidden;
            background-color: rgba(0,0,0,0.2);
        }

        .content-image {
            width: 100%;
            height: 100%;
            object-fit: cover; /* لضمان ملء الصورة للحاوية */
        }

        .formula {
            background: rgba(0, 0, 0, 0.3);
            padding: 15px;
            border-radius: 5px;
            font-family: 'Courier New', Courier, monospace;
            direction: ltr;
            text-align: center;
            border: 1px solid var(--glass-border);
            font-weight: bold;
            color: #f87171; /* أحمر ناعم */
            margin-top: 15px;
        }

        /* ==============================
           7. شريط التذييل (Footer Strip)
           ============================== */
        .footer-strip {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto 20px;
            height: 80px;
            background: var(--glass-bg);
            backdrop-filter: blur(var(--blur-strength));
            -webkit-backdrop-filter: blur(var(--blur-strength));
            border: 1px solid var(--glass-border);
            border-radius: 40px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 40px;
        }

        .footer-left {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .teacher-image-container {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            border: 2px solid var(--gold);
            overflow: hidden;
        }

        /* ملاحظة: يمكنك استبدال الرابط أدناه بصورتك الخاصة */
        .teacher-image {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .footer-mid {
            flex: 1;
            text-align: right;
            margin-right: 20px;
        }

        .semester-title { font-size: 1.1rem; color: var(--text-main); font-weight: 600; margin: 0; }
        .semester-date { font-size: 0.9rem; color: var(--text-sub); margin: 0; }

        .footer-arrow {
            width: 40px;
            height: 40px;
            border: 1px solid var(--glass-border);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            color: var(--text-sub);
            transition: all 0.3s ease;
        }

        .footer-arrow:hover { border-color: var(--gold); color: var(--gold); }

        /* ==============================
           8. تجاوب الشاشات (Responsive)
           ============================== */
        @media (max-width: 1024px) {
            .container, .top-nav, .footer-strip { width: 95%; }
            .header-content-right { width: auto; align-items: flex-start; justify-content: flex-end; }
        }

        @media (max-width: 768px) {
            .brand-name { font-size: 2.8rem; }
            .nav-links { display: none; } /* إخفاء القائمة في الموبايل */
            .top-nav { height: 50px; }
            .students-section { flex-direction: column; align-items: center; text-align: center; }
            .topic-card { flex-direction: column; text-align: center; }
            .topic-content h2::after { right: 50%; transform: translateX(50%) translateY(-50%); width: 100%; height: 3px; top: 100%; }
            .image-placeholder { width: 100%; flex-basis: auto; height: 180px; }
            .main-header { padding: 30px; }
            .footer-strip { height: auto; flex-direction: column; gap: 15px; padding: 20px; border-radius: 20px; }
            .footer-left { flex-direction: column; text-align: center; }
            .footer-mid { margin-right: 0; text-align: center; }
        }

        @media (max-width: 480px) {
            .brand-name { font-size: 2.2rem; }
            .students-list { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>
    
    <div class="glass-overlay"></div>

    <nav class="top-nav">
        <div class="brand-logo-top">Xs.boda</div>
        <div class="nav-links">
            <a href="#" class="nav-link">الرئيسية</a>
            <a href="#دليل-المنهج" class="nav-link">الدليل الشامل</a>
            <a href="#قسم-البيتزا" class="nav-link">الخميرة والبيتزا</a>
            <a href="#" class="nav-link">تواصل معنا</a>
        </div>
        <div class="nav-icons">
            <a href="#" target="_blank">&#127760;</a> <a href="#" target="_blank">&#9426;</a> </div>
    </nav>

    <main class="container">
        
        <header class="main-header">
            <div class="header-content-left">
                <h1 class="brand-name">Xs.boda</h1>
                <h2 class="course-name">أسس التغذية / الاقتصاد المنزلي</h2>
                
                <div class="students-section">
                    <div class="team-image-container">
                        <img src="https://images.unsplash.com/photo-1519389950473-47ba0277781c?q=80&w=200" alt="فريق الطلاب" class="team-image">
                    </div>
                    <div class="students-list-wrapper">
                        <h3 class="students-title">فريق إعداد الطلاب</h3>
                        <ul class="students-list">
                            <li>عبدالرحمن مصطفى عويس</li>
                            <li>عمر محسن عبد العزيز</li>
                            <li>علي عباس علي</li>
                            <li>صبري حاتم صبري محمد</li>
                            <li>منه رجب عبد التواب</li>
                            <li>ياسمين ابراهيم احمد</li>
                        </ul>
                    </div>
                </div>
            </div>
            
            <div class="header-content-right">
                <a href="#" class="header-btn">دخول / سلة الشراء</a>
            </div>
            
            <div class="decorative-number">01</div>
        </header>

        <section id="دليل-المنهج" class="curriculum-section">
            <h1 class="main-title">📚 الدليل الشامل للمنهج الدراسي</h1>

            <h2 class="nutrition-section-title">الجزء الأول: المفاهيم الأساسية في التغذية</h2>

            <details class="det-nutrition">
                <summary>1. مقدمة في علم التغذية</summary>
                <div class="details-content">
                    <p><strong>الغذاء:</strong> المادة التي يتناولها الكائن الحي.</p>
                    <p><strong>التغذية:</strong> العمليات التي يحول بها الجسم الغذاء إلى طاقة وأنسجة.</p>
                    <p><strong>العناصر الغذائية:</strong> المواد الكيميائية في الطعام.</p>
                    <p><strong>الحالة الغذائية:</strong> حالة الجسم نتيجة لما يتناوله.</p>
                </div>
            </details>

            <details class="det-blue">
                <summary>2. العناصر الغذائية الكبرى (Macronutrients)</summary>
                <div class="details-content">
                    <p><strong>الكربوهيدرات:</strong> المصدر الرئيسي للطاقة (سكريات، نشويات).</p>
                    <p><strong>البروتينات:</strong> أحجار البناء، بناء العضلات.</p>
                    <p><strong>الدهون:</strong> مصدر مركز للطاقة.</p>
                </div>
            </details>

            <details class="det-gold">
                <summary>3. العناصر الغذائية الصغرى (Micronutrients)</summary>
                <div class="details-content">
                    <p><span class="highlight">الفيتامينات:</span> ذائبة في الدهون/الماء.</p>
                    <p><strong>الأملاح المعدنية:</strong> 
