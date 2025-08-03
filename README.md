# Index.-Html
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>دليل شراء الشقق الذكي</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Cairo', sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            text-align: center;
            margin-bottom: 40px;
            color: white;
        }

        .main-title {
            font-size: 3rem;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            animation: fadeInDown 1s ease-out;
        }

        .subtitle {
            font-size: 1.2rem;
            opacity: 0.9;
            animation: fadeInUp 1s ease-out 0.3s both;
        }

        .section {
            background: white;
            margin-bottom: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            overflow: hidden;
            animation: slideInUp 0.6s ease-out;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        }

        .section-header {
            background: linear-gradient(45deg, #FF6B6B, #4ECDC4);
            color: white;
            padding: 20px;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: background 0.3s ease;
        }

        .section-header:hover {
            background: linear-gradient(45deg, #FF5252, #26C6DA);
        }

        .section-title {
            font-size: 1.5rem;
            font-weight: 600;
        }

        .toggle-icon {
            font-size: 1.5rem;
            transition: transform 0.3s ease;
        }

        .section-content {
            padding: 25px;
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.5s ease, padding 0.3s ease;
        }

        .section.active .section-content {
            max-height: 1000px;
            padding: 25px;
        }

        .section.active .toggle-icon {
            transform: rotate(180deg);
        }

        .tip-item {
            background: #f8f9fa;
            margin: 15px 0;
            padding: 15px;
            border-right: 4px solid #4ECDC4;
            border-radius: 8px;
            transition: all 0.3s ease;
        }

        .tip-item:hover {
            transform: translateX(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .important-tip {
            background: linear-gradient(45deg, #FFE0E0, #FFF0E0);
            border-right-color: #FF6B6B;
        }

        .warning-tip {
            background: linear-gradient(45deg, #FFF3CD, #F8F9FA);
            border-right-color: #FFC107;
        }

        .icon {
            display: inline-block;
            margin-left: 10px;
            font-size: 1.2rem;
        }

        .checklist {
            background: #E8F5E8;
            padding: 20px;
            border-radius: 10px;
            margin: 20px 0;
        }

        .checklist-item {
            margin: 10px 0;
            display: flex;
            align-items: center;
        }

        .checkbox {
            width: 20px;
            height: 20px;
            margin-left: 10px;
            cursor: pointer;
        }

        .progress-bar {
            background: #e0e0e0;
            height: 10px;
            border-radius: 5px;
            margin: 20px 0;
            overflow: hidden;
        }

        .progress-fill {
            background: linear-gradient(45deg, #4ECDC4, #44A08D);
            height: 100%;
            width: 0%;
            transition: width 0.5s ease;
        }

        .footer {
            text-align: center;
            color: white;
            margin-top: 40px;
            padding: 20px;
            opacity: 0.8;
        }

        @keyframes fadeInDown {
            from { opacity: 0; transform: translateY(-30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes slideInUp {
            from { opacity: 0; transform: translateY(50px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @media (max-width: 768px) {
            .main-title { font-size: 2rem; }
            .container { padding: 10px; }
            .section-content { padding: 15px; }
        }

        .floating-btn {
            position: fixed;
            bottom: 30px;
            left: 30px;
            background: linear-gradient(45deg, #FF6B6B, #4ECDC4);
            color: white;
            border: none;
            border-radius: 50%;
            width: 60px;
            height: 60px;
            font-size: 1.5rem;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            transition: all 0.3s ease;
            z-index: 1000;
        }

        .floating-btn:hover {
            transform: scale(1.1);
            box-shadow: 0 8px 25px rgba(0,0,0,0.3);
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1 class="main-title">🏠 دليل شراء الشقق الذكي</h1>
            <p class="subtitle">كل ما تحتاج معرفته قبل شراء شقتك الجديدة</p>
        </header>

        <div class="section active">
            <div class="section-header" onclick="toggleSection(this)">
                <h2 class="section-title">🔍 نصائح المعاينة والزيارة</h2>
                <span class="toggle-icon">▼</span>
            </div>
            <div class="section-content">
                <div class="tip-item">
                    <span class="icon">🌅</span>
                    <strong>زيارة متعددة:</strong> حاول تروح الشقة مرتين - مرة الصبح ومرة بالليل لتتعرف على البيئة في أوقات مختلفة
                </div>
                <div class="tip-item">
                    <span class="icon">⏰</span>
                    <strong>طول في المعاينة:</strong> خذ وقتك في المعاينة على قد ما تقدر وسيب الباب مفتوح (لو الشقة عليها مشاكل العصفورة هتبلغ انها اتفتحت)
                </div>
                <div class="tip-item important-tip">
                    <span class="icon">⚡</span>
                    <strong>العداد ضروري:</strong> الشقة اللي مافيش فيها عداد كهرباء.. ماتاخدهاش
                </div>
                <div class="tip-item">
                    <span class="icon">🏘️</span>
                    <strong>تعرف على البيئة:</strong> لازم تكون عارف ومتأكد انك انت واسرتك هتعرفوا تعيشوا في المكان ده ومع نفس الجيران دول
                </div>
            </div>
        </div>

        <div class="section">
            <div class="section-header" onclick="toggleSection(this)">
                <h2 class="section-title">📝 أهم نصائح التعاقد</h2>
                <span class="toggle-icon">▼</span>
            </div>
            <div class="section-content">
                <div class="checklist">
                    <h3>☆ المهم بقى - قائمة التحقق:</h3>
                    <div class="checklist-item">
                        <input type="checkbox" class="checkbox" onchange="updateProgress()">
                        <span>ماتشتريش من وكيل عن صاحب الشقة بتوكيل عام الا اذا كنت عارفهم كويس جدا</span>
                    </div>
                    <div class="checklist-item">
                        <input type="checkbox" class="checkbox" onchange="updateProgress()">
                        <span>صاحب الشقة يعملك توكيل خاص بالبيع حتى لو مسافر</span>
                    </div>
                    <div class="checklist-item">
                        <input type="checkbox" class="checkbox" onchange="updateProgress()">
                        <span>لو البائع فوق ٦٥ سنه ولاده يوقعوا شهود على العقد</span>
                    </div>
                    <div class="checklist-item">
                        <input type="checkbox" class="checkbox" onchange="updateProgress()">
                        <span>لو هتشترى من ورثة لازم كل الورثة يوقعوا على العقد</span>
                    </div>
                    <div class="checklist-item">
                        <input type="checkbox" class="checkbox" onchange="updateProgress()">
                        <span>لازم التوقيع على كل صفحات العقد</span>
                    </div>
                    <div class="checklist-item">
                        <input type="checkbox" class="checkbox" onchange="updateProgress()">
                        <span>لازم التوقيع يكون امامك مافيش توقيع مسبق</span>
                    </div>
                </div>
                <div class="progress-bar">
                    <div class="progress-fill" id="progressFill"></div>
                </div>
                <p style="text-align: center; color: #666;">التقدم: <span id="progressText">0%</span></p>
            </div>
        </div>

        <div class="section">
            <div class="section-header" onclick="toggleSection(this)">
                <h2 class="section-title">💰 الشراء بالقسط</h2>
                <span class="toggle-icon">▼</span>
            </div>
            <div class="section-content">
                <div class="tip-item warning-tip">
                    <span class="icon">⚠️</span>
                    <strong>تحذير مهم:</strong> اوعي تمضى على إيصالات امانه، أكتب الاقساط فى العقد [القيمة وميعاد القسط]
                </div>
                <div class="tip-item">
                    <span class="icon">📋</span>
                    <strong>تفاصيل الأقساط:</strong> لازم تكون كل تفاصيل الأقساط مكتوبة في العقد بوضوح
                </div>
            </div>
        </div>

        <div class="section">
            <div class="section-header" onclick="toggleSection(this)">
                <h2 class="section-title">👥 التحقق من حقوق الزوجة والجيران</h2>
                <span class="toggle-icon">▼</span>
            </div>
            <div class="section-content">
                <div class="tip-item important-tip">
                    <span class="icon">👩</span>
                    <strong>لااااااااازم:</strong> تشوف زوجة المالك حقك جداً.. احسن يكون مطلقها ومعاها قرار تمكين
                </div>
                <div class="tip-item">
                    <span class="icon">🏠</span>
                    <strong>حقك جداً:</strong> انك تدخل لجار واتنين فى العماره، وتسألهم عن الشقة
                </div>
                <div class="tip-item">
                    <span class="icon">🤝</span>
                    <strong>نصيحة:</strong> ديهم الأمان وفهمهم ان الكلام بينكم سر.. علشان يقولوا الصراحة
                </div>
            </div>
        </div>

        <div class="section">
            <div class="section-header" onclick="toggleSection(this)">
                <h2 class="section-title">📜 التحقق من سند الملكية</h2>
                <span class="toggle-icon">▼</span>
            </div>
            <div class="section-content">
                <div class="tip-item">
                    <span class="icon">📋</span>
                    <strong>التأكد من الملكية:</strong> لازم تتأكد من سند ملكية البائع وتسلسل الملكية حتى آخر مشتري
                </div>
                <div class="tip-item">
                    <span class="icon">🏗️</span>
                    <strong>عقد الأرض:</strong> وكمان عقد للأرض سواء عرفى أو مسجل وتتأكد من صحته
                </div>
                <div class="tip-item">
                    <span class="icon">⚖️</span>
                    <strong>التوكيل الشامل:</strong> تكتب عقد يضمن الثمن وبنود تضمن حقك وشرط جزائي وتوكيل في الشهر العقاري
                </div>
            </div>
        </div>

        <div class="section">
            <div class="section-header" onclick="toggleSection(this)">
                <h2 class="section-title">⚖️ أهمية المحامي</h2>
                <span class="toggle-icon">▼</span>
            </div>
            <div class="section-content">
                <div class="tip-item important-tip">
                    <span class="icon">👨‍💼</span>
                    <strong>ضرورى جداً:</strong> يكون معاك محامى ثقة بلاش تستخسر وتوفر اتعاب المحامى
                </div>
                <div class="tip-item">
                    <span class="icon">🛡️</span>
                    <strong>الحماية:</strong> وجود المحامى هيأمنك ويمنع عنك بلاوى كتير
                </div>
                <div class="tip-item">
                    <span class="icon">🔍</span>
                    <strong>دور المحامى:</strong> مهم علشان يتأكد من صحة مستندات الملكية وتسلسل العقود ويتأكد ان الشقة مفيش عليها اي مشاكل
                </div>
            </div>
        </div>

        <div class="footer">
            <p>والله الموفق 🤲</p>
            <p>مع تحياتي للجميع ❤️</p>
        </div>
    </div>

    <button class="floating-btn" onclick="scrollToTop()" title="العودة للأعلى">
        ⬆️
    </button>

    <script>
        function toggleSection(header) {
            const section = header.parentElement;
            section.classList.toggle('active');
        }

        function updateProgress() {
            const checkboxes = document.querySelectorAll('.checkbox');
            const checked = document.querySelectorAll('.checkbox:checked').length;
            const total = checkboxes.length;
            const percentage = Math.round((checked / total) * 100);
            
            document.getElementById('progressFill').style.width = percentage + '%';
            document.getElementById('progressText').textContent = percentage + '%';
        }

        function scrollToTop() {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        }

        // تأثير الظهور التدريجي للأقسام
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        });

        document.querySelectorAll('.section').forEach(section => {
            section.style.opacity = '0';
            section.style.transform = 'translateY(30px)';
            section.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(section);
        });

        // فتح القسم الأول تلقائياً
        document.addEventListener('DOMContentLoaded', function() {
            updateProgress();
        });
    </script>
</body>
</html>
