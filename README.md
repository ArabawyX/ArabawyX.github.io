<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مقرر أسس التغذية | XS.Boda</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700;900&family=Space+Grotesk:wght@700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    
    <style>
        /* ================= إعادة ضبط عامة ================= */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* ================= إعدادات عامة وتصميم زجاجي ================= */
        :root {
            --glass-bg: rgba(255, 255, 255, 0.08);
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
