<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>منهج التغذية | Xs.boda</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;700;900&family=Amiri:wght@400;700&display=swap" rel="stylesheet">
    
    <style>
        :root {
            /* لوحة ألوان حديثة */
            --glass-bg: rgba(255, 255, 255, 0.15);
            --glass-border: rgba(255, 255, 255, 0.2);
            --accent-gold: #ffcc33;
            --accent-cyan: #00f2fe;
            --text-main: #ffffff;
            --bg-gradient: linear-gradient(135deg, #0f172a 0%, #1e293b 50%, #334155 100%);
        }

        * {
            box-sizing: border-box;
            transition: all 0.3s ease;
        }

        body {
            font-family: 'Cairo', sans-serif;
            background: var(--bg-gradient);
            background-attachment: fixed;
            color: var(--text-main);
            margin: 0;
            padding: 0;
            overflow-x: hidden;
        }

        /* الخلفية المتحركة لإبراز تأثير الزجاج */
        body::before {
            content: "";
            position: fixed;
            top: -10%;
            left: -10%;
            width: 400px;
            height: 400px;
            background: radial-gradient(circle, rgba(0, 242, 254, 0.15) 0%, transparent 70%);
            z-index: -1;
            filter: blur(50px);
            animation: move 20s infinite alternate;
        }

        @keyframes move {
            from { transform: translate(0, 0); }
            to { transform: translate(100vw, 100vh); }
        }

        /* تأثير الزجاج العام */
        .glass-card {
            background: var(--glass-bg);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid var(--glass-border);
            border-radius: 20px;
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.3);
        }

        /* الترويسة */
        .main-header {
            padding: 80px 20px;
            text-align: center;
            margin-bottom: 40px;
        }

        .brand-name {
            font-size: 5rem;
            font-weight: 900;
            background: linear-gradient(to right, #fff, var(--accent-gold));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin: 0;
            letter-spacing: 2px;
        }

        .course-name {
            font-size: 1.5rem;
            opacity: 0.8;
            margin-top: 10px;
        }

        /* قائمة الطلاب */
        .students-container {
            margin-top: 40px;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
            max-width: 1000px;
            margin-left: auto;
            margin-right: auto;
        }

        .student-chip {
            background: rgba(255, 255, 255, 0.1);
            padding: 8px 20px;
            border-radius: 50px;
            font-size: 0.9rem;
            border: 1px solid var(--glass-border);
        }

        .student-chip:hover {
            background: var(--accent-gold);
            color: #000;
            transform: scale(1.05);
        }

        /* المحتوى الرئيسي */
        .container {
            max-width: 900px;
            margin: 0 auto 100px;
            padding: 0 20px;
        }

        .section-title {
            font-size: 2rem;
            margin: 50px 0 30px;
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .section-title::after {
            content: "";
            flex: 1;
            height: 2px;
            background: linear-gradient(to left, var(--glass-border), transparent);
        }

        /* الانهيارات (Details) بتصميم زجاجي */
        details {
            margin-bottom: 15px;
            overflow: hidden;
        }

        summary {
            padding: 20px;
            cursor: pointer;
            list-style: none;
            font-weight: bold;
            font-size: 1.2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        summary::after {
            content: "✦";
            color: var(--accent-gold);
        }

        .details-content {
            padding: 20px;
            background: rgba(0, 0, 0, 0.2);
            font-family: 'Amiri', serif;
            font-size: 1.2rem;
            line-height: 1.8;
        }

        /* قسم البيتزا والخميرة */
        .pizza-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-top: 30px;
        }

        .pizza-card {
            padding: 25px;
            position: relative;
        }

        .pizza-card h3 {
            color: var(--accent-gold);
            margin-top: 0;
        }

        .formula {
            background: #000;
            color: var(--accent-cyan);
            padding: 15px;
            border-radius: 10px;
            font-family: monospace;
            text-align: center;
            margin: 15px 0;
            border: 1px solid var(--accent-cyan);
        }

        /* تحسينات الشاشات الصغيرة */
        @media (max-width: 768px) {
            .brand-name { font-size: 3rem; }
            .pizza-grid { grid-template-columns: 1fr; }
            .container { padding: 0 15px; }
        }
    </style>
</head>
<body>

    <header class="main-header">
        <h1 class="brand-name">Xs.boda</h1>
        <p class="course-name">أسس التغذية والاقتصاد المنزلي</p>
        
        <div class="students-container">
            <span class="student-chip">عبدالرحمن مصطفى</span>
            <span class="student-chip">عمر محسن</span>
            <span class="student-chip">علي عباس</span>
            <span class="student-chip">صبري حاتم</span>
            <span class="student-chip">هنا محمود</span>
            <span class="student-chip">منه رجب</span>
            <span class="student-chip">هدير احمد</span>
            <span class="student-chip">ياسمين ابراهيم</span>
            <span class="student-chip">فاطمه فايز</span>
            <span class="student-chip">منه الله وليد</span>
        </div>
    </header>

    <main class="container">
        
        <h2 class="section-title">🧪 أساسيات التغذية</h2>

        <details class="glass-card">
            <summary>المفاهيم الكبرى (Macronutrients)</summary>
            <div class="details-content">
                <p>• <b>الكربوهيدرات:</b> وقود الجسم السريع (4 سعرات/جرام).</p>
                <p>• <b>البروتينات:</b> لترميم الأنسجة وبناء العضلات.</p>
                <p>• <b>الدهون:</b> مخزن الطاقة والفيتامينات (9 سعرات/جرام).</p>
            </div>
        </details>

        <details class="glass-card">
            <summary>الفيتامينات والأملاح</summary>
            <div class="details-content">
                <p>تنقسم الفيتامينات إلى: <br>
                1. <b>ذائبة في الدهون:</b> (A, D, E, K) <br>
                2. <b>ذائبة في الماء:</b> (C, B Complex)</p>
                <p><i>نقص فيتامين C يؤدي للإسقربوط، ونقص D يؤدي للكساح.</i></p>
            </div>
        </details>

        <h2 class="section-title">🍕 فنون العجين والخميرة</h2>

        <div class="pizza-grid">
            <div class="glass-card pizza-card">
                <h3>كيمياء التخمير</h3>
                <p>الخميرة كائن حي يحول السكر إلى غاز CO2 وكحول لرفع العجين.</p>
                <div class="formula">
                    Sucrose → Glucose → CO2 ↑
                </div>
            </div>

            <div class="glass-card pizza-card">
                <h3>عناصر النجاح</h3>
                <p>للحصول على أفضل تفاعل للخميرة، يجب توفير الثلاثي الذهبي:</p>
                <ul>
                    <li>الغذاء (السكر/النشا)</li>
                    <li>الرطوبة (الماء/الحليب)</li>
                    <li>الدفء (الحرارة المناسبة)</li>
                </ul>
            </div>
        </div>

        <div class="glass-card" style="margin-top: 20px; padding: 30px;">
            <h3 style="color:var(--accent-gold)">مراحل تصنيع البيتزا</h3>
            <p>تبدأ بـ <b>النشاط</b> ثم <b>التخمير الأول</b> (تضاعف الحجم)، يليه <b>التشكيل</b>، وأخيراً <b>الخبز</b> في فرن ساخن جداً لضمان نضج العجين وتوقف نشاط الخميرة في الوقت المثالي.</p>
        </div>

    </main>

</body>
</html>
