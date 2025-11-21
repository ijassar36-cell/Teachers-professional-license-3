# Teachers-professional-license-3
Compiled by Teacher Fahad Alkhaldi


<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>اختبار الرخصة المهنية للمعلمين</title>
    <style>
        :root {
            --primary-color: #1a1a2e;
            --secondary-color: #16213e;
            --accent-color: #0f3460;
            --correct-color: #2ecc71;
            --incorrect-color: #e74c3c;
            --text-color: #ecf0f1;
            --border-radius: 10px;
            --transition: all 0.3s ease;
            --card-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: linear-gradient(135deg, var(--primary-color), #0c0c1a);
            color: var(--text-color);
            line-height: 1.6;
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            margin-bottom: 30px;
            padding: 25px;
            background-color: var(--secondary-color);
            border-radius: var(--border-radius);
            box-shadow: var(--card-shadow);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        h1 {
            font-size: 2.5rem;
            margin-bottom: 15px;
            color: #4cc9f0;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
        }

        .subtitle {
            font-size: 1.2rem;
            color: #b0b0b0;
            margin-bottom: 10px;
        }

        .exam-info {
            display: flex;
            justify-content: space-between;
            background-color: var(--secondary-color);
            padding: 20px;
            border-radius: var(--border-radius);
            margin-bottom: 25px;
            box-shadow: var(--card-shadow);
            flex-wrap: wrap;
            gap: 15px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .info-item {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .info-item i {
            color: #4cc9f0;
            font-size: 1.2rem;
        }

        .progress-container {
            margin-bottom: 25px;
            background-color: var(--secondary-color);
            padding: 15px;
            border-radius: var(--border-radius);
            box-shadow: var(--card-shadow);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .progress-bar {
            height: 12px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 6px;
            overflow: hidden;
        }

        .progress {
            height: 100%;
            background: linear-gradient(90deg, #4cc9f0, #4361ee);
            border-radius: 6px;
            transition: width 0.5s ease;
            width: 0%;
        }

        .progress-text {
            display: flex;
            justify-content: space-between;
            margin-top: 8px;
            font-size: 0.9rem;
            color: #b0b0b0;
        }

        .question-container {
            background-color: var(--secondary-color);
            border-radius: var(--border-radius);
            padding: 25px;
            margin-bottom: 25px;
            box-shadow: var(--card-shadow);
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .question-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .question-number {
            font-weight: bold;
            color: #4cc9f0;
            font-size: 1.2rem;
        }

        .question-text {
            font-size: 1.15rem;
            margin-bottom: 25px;
            line-height: 1.8;
            background-color: rgba(0, 0, 0, 0.2);
            padding: 15px;
            border-radius: var(--border-radius);
            border-right: 3px solid #4cc9f0;
        }

        .options-container {
            display: grid;
            grid-template-columns: 1fr;
            gap: 15px;
            margin-bottom: 20px;
        }

        .option {
            padding: 18px;
            background-color: rgba(255, 255, 255, 0.05);
            border-radius: var(--border-radius);
            cursor: pointer;
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.1);
            display: flex;
            align-items: center;
        }

        .option:hover {
            background-color: rgba(255, 255, 255, 0.1);
            transform: translateY(-3px);
            box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
        }

        .option-label {
            font-weight: bold;
            margin-left: 15px;
            width: 35px;
            height: 35px;
            display: flex;
            align-items: center;
            justify-content: center;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            transition: var(--transition);
        }

        .option-text {
            flex: 1;
        }

        .correct {
            background-color: rgba(46, 204, 113, 0.2);
            border-color: var(--correct-color);
        }

        .correct .option-label {
            background-color: var(--correct-color);
        }

        .incorrect {
            background-color: rgba(231, 76, 60, 0.2);
            border-color: var(--incorrect-color);
        }

        .incorrect .option-label {
            background-color: var(--incorrect-color);
        }

        .result-popup {
            background-color: rgba(0, 0, 0, 0.8);
            padding: 20px;
            border-radius: var(--border-radius);
            margin-top: 20px;
            border-left: 4px solid #4cc9f0;
            display: none;
        }

        .result-popup.show {
            display: block;
            animation: fadeIn 0.5s ease;
        }

        .result-title {
            font-weight: bold;
            margin-bottom: 10px;
            color: #4cc9f0;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .result-content {
            line-height: 1.7;
        }

        .correct-answer {
            color: var(--correct-color);
            font-weight: bold;
            margin-top: 10px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .navigation {
            display: flex;
            justify-content: space-between;
            margin-top: 30px;
        }

        .btn {
            padding: 12px 25px;
            background: linear-gradient(135deg, #4cc9f0, #4361ee);
            color: white;
            border: none;
            border-radius: var(--border-radius);
            cursor: pointer;
            font-size: 1rem;
            font-weight: bold;
            transition: var(--transition);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(76, 201, 240, 0.4);
        }

        .btn:disabled {
            background: #555;
            cursor: not-allowed;
            transform: none;
            box-shadow: none;
        }

        .btn-prev {
            background: linear-gradient(135deg, #f0a04b, #e67e22);
        }

        .btn-finish {
            background: linear-gradient(135deg, #2ecc71, #27ae60);
        }

        .footer {
            text-align: center;
            margin-top: 40px;
            padding: 20px;
            color: #b0b0b0;
            font-size: 0.9rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* تصميم متجاوب */
        @media (max-width: 768px) {
            .exam-info {
                flex-direction: column;
            }
            
            .question-container {
                padding: 15px;
            }
            
            .navigation {
                flex-direction: column;
                gap: 15px;
            }
            
            .btn {
                width: 100%;
                justify-content: center;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>اختبار الرخصة المهنية للمعلمين</h1>
            <p class="subtitle">اختبار شامل ومتكامل لتقييم الكفايات المهنية للمعلمين</p>
        </header>

        <div class="exam-info">
            <div class="info-item">
                <i>⏱️</i>
                <span>الوقت المتبقي: <span id="timer">02:00:00</span></span>
            </div>
            <div class="info-item">
                <i>❓</i>
                <span>عدد الأسئلة: 68 سؤال</span>
            </div>
            <div class="info-item">
                <i>📊</i>
                <span>المستوى: متقدم</span>
            </div>
        </div>

        <div class="progress-container">
            <div class="progress-bar">
                <div class="progress" id="progress-bar"></div>
            </div>
            <div class="progress-text">
                <span>التقدم: <span id="progress-text">0%</span></span>
                <span>سؤال <span id="current-question">1</span> من 68</span>
            </div>
        </div>

        <div class="question-container">
            <div class="question-header">
                <div class="question-number">سؤال رقم <span id="question-number">1</span></div>
                <div class="question-category" id="question-category">القيم والمسؤوليات المهنية</div>
            </div>

            <div class="question-text" id="question-text">
                <!-- سيتم تعبئة نص السؤال هنا -->
            </div>

            <div class="options-container" id="options-container">
                <!-- سيتم تعبئة الخيارات هنا -->
            </div>

            <div class="result-popup" id="result-popup">
                <div class="result-title">
                    <span>شرح الإجابة</span>
                </div>
                <div class="result-content" id="result-content">
                    <!-- سيتم تعبئة شرح الإجابة هنا -->
                </div>
                <div class="correct-answer" id="correct-answer">
                    <!-- سيتم عرض الإجابة الصحيحة هنا -->
                </div>
            </div>

            <div class="navigation">
                <button class="btn btn-prev" id="prev-btn" disabled>
                    <span>السابق</span>
                </button>
                <button class="btn btn-next" id="next-btn">
                    <span>التالي</span>
                </button>
                <button class="btn btn-finish" id="finish-btn" style="display: none;">
                    <span>إنهاء الاختبار</span>
                </button>
            </div>
        </div>

        <div class="footer">
            <p>جميع الحقوق محفوظة © 2023 - هيئة تقويم التعليم والتدريب</p>
        </div>
    </div>

    <script>
        // بيانات الأسئلة مع خيارات متشابهة في المعنى مع اختلافات دقيقة في القوة والارتباط
        const questions = [
            {
                id: 1,
                category: "القيم والمسؤوليات المهنية",
                text: "يعتبر الالتزام بالقيم الإسلامية الوسطية من أهم أسس الممارسة المهنية للمعلم. في هذا السياق، أي من الممارسات التالية تعكس بشكل أفضل الالتزام بهذه القيم في البيئة التعليمية؟",
                options: [
                    "التركيز على بناء الشخصية المتكاملة للطالب من خلال تعزيز القيم الأخلاقية والروح النقدية البناءة في إطار الاعتدال والتسامح",
                    "العمل على تنمية الجوانب القيمية لدى الطلاب مع الاهتمام بتحقيق التوازن بين متطلبات التنشئة الإسلامية والانفتاح على الثقافات الأخرى",
                    "الاهتمام بتعزيز القيم الإسلامية في سلوك الطلاب مع مراعاة الفروق الفردية وتنمية المهارات الحياتية المختلفة",
                    "تطوير بيئة تعليمية تركز على القيم الإسلامية مع تشجيع الطلاب على المشاركة المجتمعية والتفاعل الإيجابي مع الآخرين"
                ],
                correctAnswer: 0,
                explanation: "التركيز على بناء الشخصية المتكاملة للطالب من خلال تعزيز القيم الأخلاقية والروح النقدية البناءة في إطار الاعتدال والتسامح يعكس الالتزام الكامل بالقيم الإسلامية الوسطية التي تجمع بين الأصالة والمعاصرة، وتوازن بين الثوابت والمتغيرات في إطار من الاعتدال والتسامح."
            },
            {
                id: 2,
                category: "المعرفة المهنية",
                text: "يعد استيعاب النص المسموع والمقروء من المهارات الأساسية للمعلم. أي من الاستراتيجيات التالية تكون الأكثر فعالية في تحسين هذه المهارة لدى الطلاب؟",
                options: [
                    "استخدام منهجية متكاملة تعتمد على الربط بين النصوص والخبرات الحياتية مع تدريب الطلاب على التحليل النقدي والتلخيص الفعال",
                    "تنويع أساليب تقديم النصوص وربطها بالمواقف التعليمية المختلفة مع تشجيع الطلاب على المشاركة الفعالة في المناقشات",
                    "تطوير أنشطة قرائية متدرجة الصعوبة تراعي الفروق الفردية مع توفير فرص للممارسة والتطبيق في سياقات متنوعة",
                    "اعتماد استراتيجيات تعلم تعاوني تعزز التفاعل مع النصوص مع تقديم تغذية راجعة مستمرة حول أداء الطلاب"
                ],
                correctAnswer: 0,
                explanation: "استخدام منهجية متكاملة تعتمد على الربط بين النصوص والخبرات الحياتية مع تدريب الطلاب على التحليل النقدي والتلخيص الفعال تمثل الاستراتيجية الأكثر شمولية وفعالية، حيث تربط بين الجانب النظري والتطبيقي وتنمي مهارات التفكير العليا لدى الطلاب."
            },
            {
                id: 3,
                category: "الممارسات المهنية",
                text: "يعتبر التخطيط للتدريس وتنفيذه من الممارسات المهنية الأساسية. أي من الخيارات التالية يمثل أفضل ممارسة في تصميم خطة التدريس؟",
                options: [
                    "بناء خطة تدريسية تراعي الاحتياجات المتنوعة للطلاب مع تحديد مؤشرات أداء واضحة وآليات تقويم متنوعة ترتبط مباشرة بالأهداف التعليمية",
                    "تصميم خطط تدريسية مرنة تستجيب للفروق الفردية مع توفير أنشطة تعليمية متنوعة وموارد تعلم إضافية للطلاب",
                    "وضع خطط تدريسية تركز على تحقيق الأهداف التعليمية مع مراعاة الأساليب الحديثة في التدريس وتقنيات التعليم الفعال",
                    "إعداد خطط تدريسية تشمل أنشطة تعلم تفاعلية مع تخصيص وقت كافٍ للممارسة والتطبيق وتقديم الدعم اللازم للطلاب"
                ],
                correctAnswer: 0,
                explanation: "بناء خطة تدريسية تراعي الاحتياجات المتنوعة للطلاب مع تحديد مؤشرات أداء واضحة وآليات تقويم متنوعة ترتبط مباشرة بالأهداف التعليمية تمثل أفضل الممارسات، حيث تجمع بين التخطيط الاستراتيجي والمرونة والتركيز على نتائج التعلم مع آليات تقويم فعالة."
            },
            {
                id: 4,
                category: "التفاعل المهني",
                text: "يعد التفاعل مع مجتمعات التعلم المهني من الممارسات المهمة لتطوير الأداء التعليمي. أي من الممارسات التالية تعزز هذا التفاعل بشكل أفضل؟",
                options: [
                    "المشاركة الفاعلة في بحوث العمل التربوي المشتركة وتطبيق نتائجها مع تقييم أثرها على تحسين ممارسات التعليم والتعلم",
                    "الانخراط في حلقات النقاش المهنية وتبادل الخبرات مع الزملاء حول استراتيجيات التدريس الفعالة وتجاربهم الصفية",
                    "التواصل المستمر مع المعلمين في التخصصات المختلفة وتبادل الأفكار حول أساليب تحسين البيئة التعليمية وتطوير المناهج",
                    "المساهمة في برامج التطوير المهني وتنظيم ورش العمل التربوية التي تستهدف تحسين المخرجات التعليمية"
                ],
                correctAnswer: 0,
                explanation: "المشاركة الفاعلة في بحوث العمل التربوي المشتركة وتطبيق نتائجها مع تقييم أثرها على تحسين ممارسات التعليم والتعلم تمثل أعلى مستويات التفاعل المهني، حيث تربط بين النظرية والتطبيق وتؤدي إلى تحسين ملموس في الممارسات التعليمية."
            },
            {
                id: 5,
                category: "التطوير المهني المستمر",
                text: "يعد التطوير المهني المستمر ضرورة للمعلم لمواكبة المستجدات التربوية. أي من الخيارات التالية يمثل أفضل وسيلة للتطوير المهني المستمر؟",
                options: [
                    "اعتماد منهجية التطوير القائمة على البحث الإجرائي والتأمل في الممارسة مع متابعة المستجدات البحثية وتطبيقها في سياقات حقيقية",
                    "الالتحاق ببرامج التدريب المستمر والمشاركة في المؤتمرات التربوية مع الاطلاع على الأدبيات الحديثة في مجال التخصص",
                    "تطوير خطة شخصية للتطوير المهني تشمل تحديد الاحتياجات التدريبية ومتابعة آخر المستجدات في طرق التدريس والتقويم",
                    "المشاركة في مجتمعات التعلم المهنية وتبادل الخبرات مع الزملاء مع توثيق الممارسات الناجحة ونشرها بين المعلمين"
                ],
                correctAnswer: 0,
                explanation: "اعتماد منهجية التطوير القائمة على البحث الإجرائي والتأمل في الممارسة مع متابعة المستجدات البحثية وتطبيقها في سياقات حقيقية تمثل النهج الأكثر شمولية وفعالية، حيث تجمع بين التعلم النظري والتطبيق العملي والتأمل في الممارسة."
            },
            {
                id: 6,
                category: "تهيئة بيئات التعلم",
                text: "أي من الممارسات التالية تعتبر الأكثر فعالية في تهيئة بيئة تعلم تفاعلية وداعمة للمتعلم؟",
                options: [
                    "تأسيس بيئة تعلم قائمة على الثقة المتبادلة والدعم النفسي مع توفير فرص حقيقية للتعلم النشط والتعبير عن الرأي في إطار من الاحترام",
                    "توفير مساحات تعلم مفتوحة ومرنة تشجع على العمل الجماعي مع استخدام تقنيات تعليمية متنوعة تناسب أنماط التعلم المختلفة",
                    "بناء أنظمة دعم متعددة المستويات للطلاب مع توفير موارد تعلم غنية ومتنوعة تلبي الاحتياجات التعليمية المتباينة",
                    "تهيئة أجواء صفية إيجابية تعزز المشاركة الطوعية مع تصميم أنشطة تعلم تثير الفضول وتشجع على الاستقصاء والبحث"
                ],
                correctAnswer: 0,
                explanation: "تأسيس بيئة تعلم قائمة على الثقة المتبادلة والدعم النفسي مع توفير فرص حقيقية للتعلم النشط والتعبير عن الرأي في إطار من الاحترام تمثل الممارسة الأكثر شمولية، حيث تجمع بين الجوانب النفسية والاجتماعية والأكاديمية لخلق بيئة تعلم مثالية."
            }
        ];

        // متغيرات التطبيق
        let currentQuestionIndex = 0;
        let userAnswers = new Array(questions.length).fill(null);
        let timerInterval;

        // عناصر DOM
        const questionNumberElement = document.getElementById('question-number');
        const questionCategoryElement = document.getElementById('question-category');
        const questionTextElement = document.getElementById('question-text');
        const optionsContainer = document.getElementById('options-container');
        const resultPopup = document.getElementById('result-popup');
        const resultContent = document.getElementById('result-content');
        const correctAnswerElement = document.getElementById('correct-answer');
        const prevBtn = document.getElementById('prev-btn');
        const nextBtn = document.getElementById('next-btn');
        const finishBtn = document.getElementById('finish-btn');
        const progressBar = document.getElementById('progress-bar');
        const progressText = document.getElementById('progress-text');
        const currentQuestionElement = document.getElementById('current-question');
        const timerElement = document.getElementById('timer');

        // تهيئة المؤقت
        function initializeTimer() {
            let timeLeft = 2 * 60 * 60; // ساعتان بالثواني
            updateTimerDisplay(timeLeft);
            
            timerInterval = setInterval(() => {
                timeLeft--;
                updateTimerDisplay(timeLeft);
                
                if (timeLeft <= 0) {
                    clearInterval(timerInterval);
                    finishExam();
                }
            }, 1000);
        }
        
        function updateTimerDisplay(seconds) {
            const hours = Math.floor(seconds / 3600);
            const minutes = Math.floor((seconds % 3600) / 60);
            const secs = seconds % 60;
            
            timerElement.textContent = `${hours.toString().padStart(2, '0')}:${minutes.toString().padStart(2, '0')}:${secs.toString().padStart(2, '0')}`;
        }

        // عرض السؤال الحالي
        function displayCurrentQuestion() {
            const question = questions[currentQuestionIndex];
            
            questionNumberElement.textContent = question.id;
            questionCategoryElement.textContent = question.category;
            questionTextElement.textContent = question.text;
            
            // تحديث شريط التقدم
            const progress = ((currentQuestionIndex + 1) / questions.length) * 100;
            progressBar.style.width = `${progress}%`;
            progressText.textContent = `${Math.round(progress)}%`;
            currentQuestionElement.textContent = currentQuestionIndex + 1;
            
            // إعادة تعيين النافذة المنبثقة
            resultPopup.classList.remove('show');
            
            // تعبئة الخيارات
            optionsContainer.innerHTML = '';
            const optionLabels = ['أ', 'ب', 'ج', 'د'];
            
            question.options.forEach((option, index) => {
                const optionElement = document.createElement('div');
                optionElement.className = 'option';
                if (userAnswers[currentQuestionIndex] === index) {
                    optionElement.classList.add(userAnswers[currentQuestionIndex] === question.correctAnswer ? 'correct' : 'incorrect');
                }
                
                optionElement.innerHTML = `
                    <div class="option-label">${optionLabels[index]}</div>
                    <div class="option-text">${option}</div>
                `;
                
                optionElement.addEventListener('click', () => selectOption(index));
                optionsContainer.appendChild(optionElement);
            });
            
            // تحديث أزرار التنقل
            prevBtn.disabled = currentQuestionIndex === 0;
            
            if (currentQuestionIndex === questions.length - 1) {
                nextBtn.style.display = 'none';
                finishBtn.style.display = 'flex';
            } else {
                nextBtn.style.display = 'flex';
                finishBtn.style.display = 'none';
            }
            
            // إذا كان المستخدم قد أجاب على السؤال، عرض النتيجة
            if (userAnswers[currentQuestionIndex] !== null) {
                showResult();
            }
        }

        // اختيار خيار
        function selectOption(optionIndex) {
            userAnswers[currentQuestionIndex] = optionIndex;
            displayCurrentQuestion();
            showResult();
        }

        // عرض نتيجة السؤال
        function showResult() {
            const question = questions[currentQuestionIndex];
            const userAnswer = userAnswers[currentQuestionIndex];
            
            if (userAnswer === null) return;
            
            resultContent.textContent = question.explanation;
            
            if (userAnswer === question.correctAnswer) {
                correctAnswerElement.innerHTML = `<span>✅ الإجابة صحيحة</span>`;
            } else {
                correctAnswerElement.innerHTML = `<span>❌ الإجابة الصحيحة: ${question.options[question.correctAnswer]}</span>`;
            }
            
            resultPopup.classList.add('show');
        }

        // التنقل بين الأسئلة
        nextBtn.addEventListener('click', () => {
            if (currentQuestionIndex < questions.length - 1) {
                currentQuestionIndex++;
                displayCurrentQuestion();
            }
        });

        prevBtn.addEventListener('click', () => {
            if (currentQuestionIndex > 0) {
                currentQuestionIndex--;
                displayCurrentQuestion();
            }
        });

        // إنهاء الاختبار
        finishBtn.addEventListener('click', finishExam);

        function finishExam() {
            clearInterval(timerInterval);
            
            // حساب النتيجة
            let score = 0;
            userAnswers.forEach((answer, index) => {
                if (answer === questions[index].correctAnswer) {
                    score++;
                }
            });
            
            const percentage = (score / questions.length) * 100;
            
            // عرض النتيجة النهائية
            alert(`تم إنهاء الاختبار!\n\nنتيجتك: ${score} من ${questions.length}\nالنسبة المئوية: ${percentage.toFixed(2)}%`);
        }

        // بدء التطبيق
        initializeTimer();
        displayCurrentQuestion();
    </script>
</body>
</html>
