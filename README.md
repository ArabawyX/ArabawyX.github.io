<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>XS.Boda | نظام إدارة التغذية الشامل</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;600;900&family=Amiri:wght@700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    
    <style>
        :root {
            --primary: #d4a373;
            --dark: #1a1c1d;
            --glass: rgba(255, 255, 255, 0.12);
            --glass-border: rgba(255, 255, 255, 0.3);
            --card-white: #ffffff;
            --text-dark: #2d2d2d;
            --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        /* أنيميشن الدخول */
        @keyframes slideUp {
            from { opacity: 0; transform: translateY(40px); }
            to { opacity: 1; transform: translateY(0); }
        }

        * { box-sizing: border-box; margin: 0; padding: 0; }

        body {
            font-family: 'Cairo', sans-serif;
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), 
                        url('https://images.unsplash.com/photo-1490818387583-1baba5e638af?auto=format&fit=crop&q=80&w=2000') no-repeat center center fixed;
            background-size: cover;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 20px;
            direction: rtl;
        }

        /* الحاوية المتجاوبة */
        .app-window {
            width: 100%;
            max-width: 1200px;
            height: auto;
            min-height: 80vh;
            background: var(--glass);
            backdrop-filter: blur(25px);
            -webkit-backdrop-filter: blur(25px);
            border: 1px solid var(--glass-border);
            border-radius: 30px;
            display: flex;
            flex-direction: column;
            overflow: hidden;
            box-shadow: 0 40px 100px rgba(0,0,0,0.3);
            animation: slideUp 0.8s ease-out forwards;
        }

        /* الهيدر المتجاوب */
        header {
            padding: 20px 40px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 15px;
            border-bottom: 1px solid rgba(255,255,255,0.1);
        }

        .logo { font-family: 'Amiri', serif; font-size: 2rem; color: white; font-weight: 900; }

        /* الشبكة الرئيسية: تتغير حسب حجم الشاشة */
        .content-grid {
            flex: 1;
            display: grid;
            grid-template-columns: 300px 1fr 250px; /* 3 أعمدة على الشاشات الكبيرة */
            gap: 20px;
            padding: 25px;
        }

        /* التحكم في الأعمدة للشاشات المتوسطة والصغيرة */
        @media (max-width: 1100px) {
            .content-grid { grid-template-columns: 1fr 1fr; } /* عمودين */
            .actions-sidebar { grid-column: span 2; display: flex; flex-direction: row !important; gap: 20px; }
        }

        @media (max-width: 768px) {
            .content-grid { grid-template-columns: 1fr; } /* عمود واحد للموبايل */
            .actions-sidebar { grid-column: span 1; flex-direction: column !important; }
            header { justify-content: center; text-align: center; }
            .app-window { border-radius: 20px; }
        }

        /* بطاقة قائمة الطلاب */
        .sidebar-card {
            background: var(--card-white);
            border-radius: 25px;
            padding: 25px;
            display: flex;
            flex-direction: column;
            transition: var(--transition);
        }

        .sidebar-card:hover { transform: translateY(-5px); box-shadow: 0 15px 30px rgba(0,0,0,0.1); }

        .sidebar-card h3 { font-size: 1.1rem; margin-bottom: 15px; border-right: 4px solid var(--primary); padding-right: 10px; }

        .scroll-list { 
            max-height: 300px; 
            overflow-y: auto; 
            margin-bottom: 15px;
            padding-left: 5px;
        }
        .scroll-list::-webkit-scrollbar { width: 4px; }
        .scroll-list::-webkit-scrollbar-thumb { background: #ddd; border-radius: 10px; }

        .list-item { padding: 10px 0; border-bottom: 1px solid #f0f0f0; font-size: 0.9rem; color: #444; list-style: none; }

        /* البطاقة الرئيسية (الهيرو) */
        .main-hero {
            background: var(--dark);
            border-radius: 25px;
            padding: 35px;
            color: white;
            position: relative;
            overflow: hidden;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .main-hero::before {
            content: "";
            position: absolute;
            top: 0; left: 0; right: 0; bottom: 0;
            background: url('https://images.unsplash.com/photo-1543353071-873f17a7a088?auto=format&fit=crop&q=80&w=800') center;
            background-size: cover;
            opacity: 0.2;
            z-index: 0;
        }

        .hero-content { z-index: 1; }
        .hero-content h1 { font-size: 2.2rem; margin-bottom: 20px; color: var(--primary); }

        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }

        .feature-box { background: rgba(255,255,255,0.05); padding: 15px; border-radius: 15px; border: 1px solid rgba(255,255,255,0.1); }
        .feature-box h4 { font-size: 0.9rem; color: var(--primary); margin-bottom: 5px; }
        .feature-box p { font-size: 0.75rem; opacity: 0.8; }

        /* الأكشنات الجانبية */
        .actions-sidebar { display: flex; flex-direction: column; gap: 20px; }
        
        .action-card {
            background: var(--glass-border);
            padding: 20px;
            border-radius: 20px;
            color: white;
            flex: 1;
            transition: var(--transition);
        }
        .action-card:hover { background: rgba(255,255,255,0.25); }

        .btn-main {
            background: var(--primary);
            color: white;
            border: none;
            padding: 12px;
            border-radius: 12px;
            width: 100%;
            font-weight: bold;
            cursor: pointer;
            margin-top: 10px;
            transition: var(--transition);
        }
        .btn-main:hover { background: white; color: var(--dark); transform: scale(1.05); }

        /* الفوتر المتجاوب */
        .footer-bar {
            width: 100%;
            background: rgba(255,255,255,0.1);
            padding: 15px 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-top: 1px solid rgba(255,255,255,0.1);
            flex-wrap: wrap;
            gap: 10px;
        }

        @media (max-width: 480px) {
            .footer-bar { justify-content: center; text-align: center; }
            .hero-content h1 { font-size: 1.5rem; }
        }
    </style>
</head>
<body>

    <div class="app-window">
        <header>
            <div class="logo">XS.Boda</div>
            <div style="display: flex; gap: 20px;">
                <i class="fas fa-search" style="color: white; cursor: pointer;"></i>
                <i class="fas fa-user-circle" style="color: white; cursor: pointer;"></i>
                <button style="padding: 5px 15px; border-radius: 20px; border: none; font-weight: bold;">Menu</button>
            </div>
        </header>

        <main class="content-grid">
            
            <aside class="sidebar-card">
                <h3>إعداد الطلاب</h3>
                <div class="scroll-list">
                    <ul>
                        <li class="list-item">عبدالرحمن مصطفى عويس</li>
                        <li class="list-item">عمر محسن عبد العزيز</li>
                        <li class="list-item">علي عباس علي</li>
                        <li class="list-item">صبري حاتم صبري</li>
                        <li class="list-item">هنا محمود مصطفي</li>
                        <li class="list-item">منه رجب عبد التواب</li>
                        <li class="list-item">هدير احمد مصطفي</li>
                        <li class="list-item">ياسمين ابراهيم احمد</li>
                        <li class="list-item">فاطمه فايز منصور</li>
                        <li class="list-item">منه الله وليد فاروق</li>
                    </ul>
                </div>
                <img src="https://images.unsplash.com/photo-1498837167922-ddd27525d352?auto=format&fit=crop&q=80&w=300" 
                     style="width: 100%; border-radius: 15px; height: 100px; object-fit: cover;" alt="Nutrition">
            </aside>

            <section class="main-hero">
                <div class="hero-content">
                    <span style="background: var(--primary); padding: 4px 12px; border-radius: 20px; font-size: 0.7rem; font-weight: bold;">PROJECT 2026</span>
                    <h1>أسس التغذية<br>والاقتصاد المنزلي</h1>
                    <p style="opacity: 0.7; font-size: 0.9rem;">دراسة تطبيقية شاملة حول العناصر الغذائية وطرق الطهي الحديثة بجامعة عين شمس.</p>
                    
                    <div class="features">
                        <div class="feature-box">
                            <h4>العملي</h4>
                            <p>طرق السلق، التسبيك، والطهي بالبخار.</p>
                        </div>
                        <div class="feature-box">
                            <h4>النظري</h4>
                            <p>دراسة الكربوهيدرات والفيتامينات والمعادن.</p>
                        </div>
                        <div class="feature-box">
                            <h4>الخميرة</h4>
                            <p>تفاعلات الكائنات الدقيقة في العجين.</p>
                        </div>
                    </div>
                </div>
            </section>

            <div class="actions-sidebar">
                <div class="action-card">
                    <i class="fas fa-flask-bubble" style="font-size: 1.5rem; margin-bottom: 10px;"></i>
                    <h4>قسم المختبر</h4>
                    <p style="font-size: 0.75rem; opacity: 0.8; margin: 10px 0;">اطلع على نتائج تجارب طهي البروتينات.</p>
                    <button class="btn-main">دخول</button>
                </div>
                <div class="action-card" style="background: var(--dark); border: 1px solid var(--primary);">
                    <h4>تحديثات 2026</h4>
                    <p style="font-size: 0.75rem; opacity: 0.8; margin: 10px 0;">تم دمج معايير الصحة العالمية الجديدة.</p>
                    <button class="btn-main" style="background: white; color: var(--dark);">تحديث</button>
                </div>
            </div>

        </main>

        <footer class="footer-bar">
            <div style="color: white; font-size: 0.8rem;">
                <strong>NEW COLLECTION</strong> | COSMIC SET 237
            </div>
            <div style="display: flex; gap: 15px;">
                <i class="fab fa-github" style="color: white;"></i>
                <i class="fas fa-share-alt" style="color: white;"></i>
            </div>
        </footer>
    </div>

</body>
</html>
