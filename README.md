<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abdallah Masoud | Photographer</title>
    <!-- استدعاء خطوط جوجل (خط القاهرة) -->
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;800&display=swap" rel="stylesheet">
    <!-- استدعاء مكتبة الأيقونات -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --bg-color: #121212;
            --card-bg: #1e1e1e;
            --gold: #d4af37;
            --text-light: #f5f5f5;
            --text-muted: #aaaaaa;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Cairo', sans-serif;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-light);
            line-height: 1.6;
        }

        /* الهيدر وصورة الخلفية */
        header {
            background: linear-gradient(rgba(18, 18, 18, 0.8), rgba(18, 18, 18, 0.9)), url('https://images.unsplash.com/photo-1511285560929-80b456fea0bc?ixlib=rb-1.2.1&auto=format&fit=crop&w=1920&q=80') no-repeat center center/cover;
            padding: 6rem 1rem 4rem;
            text-align: center;
            border-bottom: 2px solid var(--gold);
        }

        header h1 {
            color: var(--gold);
            font-size: 3rem;
            margin-bottom: 0.5rem;
            letter-spacing: 2px;
        }

        .section-title {
            text-align: center;
            color: var(--gold);
            font-size: 2rem;
            margin: 3rem 0 2rem;
            position: relative;
        }
        
        .section-title::after {
            content: '';
            width: 50px;
            height: 3px;
            background: var(--gold);
            display: block;
            margin: 10px auto;
        }

        /* الباقات */
        .packages-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            padding: 0 5%;
            max-width: 1200px;
            margin: 0 auto;
        }

        .package-card {
            background-color: var(--card-bg);
            border: 1px solid #333;
            border-radius: 10px;
            padding: 2rem;
            text-align: center;
            transition: transform 0.3s ease, border-color 0.3s ease;
        }

        .package-card:hover {
            transform: translateY(-10px);
            border-color: var(--gold);
        }

        .package-title {
            font-size: 1.5rem;
            color: var(--gold);
            margin-bottom: 10px;
        }

        .package-price {
            font-size: 2rem;
            font-weight: bold;
            margin-bottom: 20px;
            color: #fff;
        }
        
        .package-price span {
            font-size: 1rem;
            color: var(--text-muted);
        }

        .package-features {
            list-style: none;
            margin-bottom: 25px;
            text-align: right;
        }

        .package-features li {
            padding: 8px 0;
            border-bottom: 1px solid #333;
            font-size: 0.95rem;
            color: var(--text-light);
        }

        .package-features li::before {
            content: '✪';
            color: var(--gold);
            margin-left: 8px;
        }

        .btn-book {
            background-color: var(--gold);
            color: #000;
            border: none;
            padding: 12px 30px;
            font-size: 1.1rem;
            font-weight: bold;
            border-radius: 5px;
            cursor: pointer;
            width: 100%;
            transition: 0.3s;
        }

        .btn-book:hover {
            background-color: #b8972e;
            color: #fff;
        }

        .extras-note {
            text-align: center;
            color: var(--text-muted);
            margin-top: 30px;
            font-size: 0.9rem;
        }

        /* آراء العملاء (الفيدباك) */
        .reviews-container {
            display: flex;
            overflow-x: auto;
            gap: 20px;
            padding: 20px 5%;
            scrollbar-width: thin;
            scrollbar-color: var(--gold) var(--bg-color);
        }
        
        .reviews-container::-webkit-scrollbar {
            height: 8px;
        }
        .reviews-container::-webkit-scrollbar-thumb {
            background-color: var(--gold);
            border-radius: 10px;
        }

        .review-card {
            min-width: 280px;
            background: var(--card-bg);
            padding: 20px;
            border-radius: 10px;
            border-right: 4px solid var(--gold);
        }

        .review-text {
            font-style: italic;
            font-size: 1rem;
            margin-bottom: 15px;
            color: #ddd;
        }

        .review-author {
            color: var(--gold);
            font-weight: bold;
            font-size: 0.9rem;
        }

        /* قسم التواصل السفلي */
        .contact-section {
            background-color: var(--card-bg);
            padding: 40px 20px;
            margin-top: 60px;
            border-top: 1px solid #333;
        }

        .contact-wrapper {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 30px;
            max-width: 500px;
            margin: 0 auto;
        }

        .social-list {
            display: flex;
            flex-direction: column;
            gap: 15px;
            width: 100%;
        }

        .social-link {
            display: flex;
            align-items: center;
            gap: 15px;
            text-decoration: none;
            color: var(--text-light);
            background: var(--bg-color);
            padding: 12px 20px;
            border-radius: 8px;
            border: 1px solid #333;
            transition: all 0.3s ease;
        }

        .social-link:hover {
            border-color: var(--gold);
            transform: translateX(-10px); /* حركة لليسار عند المرور */
            box-shadow: 0 4px 10px rgba(212, 175, 55, 0.1);
        }

        .social-icon {
            display: flex;
            justify-content: center;
            align-items: center;
            width: 35px; /* حجم صغير */
            height: 35px; /* حجم صغير */
            background-color: var(--bg-color);
            color: var(--gold);
            border: 1px solid var(--gold);
            border-radius: 50%;
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .social-link:hover .social-icon {
            background-color: var(--gold);
            color: #000;
        }

        .social-text {
            font-size: 1.1rem;
            font-weight: 600;
        }

        .contact-badges {
            display: flex;
            flex-direction: column;
            gap: 10px;
            width: 100%;
            direction: ltr; /* لضبط الأرقام والانجليزي */
        }

        .badge {
            background: rgba(255, 255, 255, 0.05);
            border: 1px dashed var(--gold);
            padding: 10px 15px;
            border-radius: 8px;
            font-size: 0.95rem;
            color: var(--gold);
            text-align: center;
            font-weight: bold;
        }

        /* الفوتر والمطور */
        footer {
            text-align: center;
            padding: 20px 10px;
            background-color: var(--card-bg);
        }
        
        .dev-credit {
            margin-top: 15px;
            font-size: 0.75rem;
            color: #666;
        }
        
        .dev-credit a {
            color: #888;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .dev-credit a:hover {
            color: var(--gold);
        }

        /* مودال الحجز (Pop-up) */
        .modal-overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.85);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }

        .modal-content {
            background: var(--card-bg);
            width: 90%;
            max-width: 500px;
            padding: 30px;
            border-radius: 10px;
            border: 1px solid var(--gold);
            position: relative;
            max-height: 90vh;
            overflow-y: auto;
        }

        .close-btn {
            position: absolute;
            top: 15px;
            left: 15px;
            background: none;
            border: none;
            color: var(--gold);
            font-size: 1.5rem;
            cursor: pointer;
        }

        .modal-content h3 {
            color: var(--gold);
            text-align: center;
            margin-bottom: 20px;
        }

        .form-group {
            margin-bottom: 15px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-size: 0.9rem;
            color: var(--text-light);
        }

        .form-group input, .form-group textarea {
            width: 100%;
            padding: 10px;
            background: #121212;
            border: 1px solid #444;
            color: #fff;
            border-radius: 5px;
            font-family: inherit;
        }
        
        .form-group input:focus, .form-group textarea:focus {
            outline: none;
            border-color: var(--gold);
        }

        .terms-box {
            background: rgba(212, 175, 55, 0.1);
            border-right: 3px solid var(--gold);
            padding: 15px;
            font-size: 0.85rem;
            margin-bottom: 20px;
            color: #ccc;
        }

        .checkbox-group {
            display: flex;
            align-items: flex-start;
            gap: 10px;
            margin-bottom: 20px;
            font-size: 0.85rem;
        }

    </style>
</head>
<body>

    <!-- الهيدر -->
    <header>
        <h1>ABDALLAH MASOUD</h1>
        <p style="color: var(--text-muted); font-size: 1.2rem; letter-spacing: 4px;">P H O T O G R A P H E R</p>
    </header>

    <!-- الباقات الرئيسية -->
    <h2 class="section-title">الباقات الرئيسية (Wedding & Engagement)</h2>
    <div class="packages-grid">
        
        <!-- باقة 1 -->
        <div class="package-card">
            <h3 class="package-title">Full Package</h3>
            <div class="package-price">8000 <span>LE</span></div>
            <ul class="package-features">
                <li>الميكب والتجهيزات</li>
                <li>فريست لوك</li>
                <li>تصوير الجروب</li>
                <li>السيشن (عدد الصور مفتوح ايديت)</li>
                <li>البارتي (القاعة)</li>
                <li>برومو & Rails</li>
                <li><strong>بكدج الطباعة:</strong> ألبوم (30x80)</li>
                <li>تابلو (50x70) + هدية تابلو (40x50)</li>
                <li>فلاشة هدية</li>
            </ul>
            <button class="btn-book" onclick="openModal('Full Package - 8000 LE')">احجز الآن</button>
        </div>

        <!-- باقة 2 -->
        <div class="package-card">
            <h3 class="package-title">Full Day</h3>
            <div class="package-price">6000 <span>LE</span></div>
            <ul class="package-features">
                <li>فريست لوك</li>
                <li>تصوير الجروب</li>
                <li>السيشن (عدد الصور مفتوح ايديت)</li>
                <li>البارتي (القاعة)</li>
                <li>Rails</li>
                <li><strong>إضافات:</strong> برومو + فلاشة</li>
                <li><strong>بكدج الطباعة:</strong> ألبوم (30x80)</li>
                <li>تابلو (50x60) + هدية تابلو (30x40)</li>
            </ul>
            <button class="btn-book" onclick="openModal('Full Day - 6000 LE')">احجز الآن</button>
        </div>

        <!-- باقة 3 -->
        <div class="package-card">
            <h3 class="package-title">Half Day</h3>
            <div class="package-price">4500 <span>LE</span></div>
            <ul class="package-features">
                <li>السيشن (عدد الصور مفتوح ايديت)</li>
                <li>تصوير الجروب</li>
                <li>Rails</li>
                <li><strong>بكدج الطباعة:</strong> سيراميك كبير</li>
                <li>تابلو (40x50)</li>
            </ul>
            <button class="btn-book" onclick="openModal('Half Day - 4500 LE')">احجز الآن</button>
        </div>

    </div>

    <!-- باقات السيشنز -->
    <h2 class="section-title">باقات السيشن (Sessions)</h2>
    <div class="packages-grid">
        <div class="package-card">
            <h3 class="package-title">سيشن زفاف / خطوبة</h3>
            <div class="package-price">3500 <span>LE</span></div>
            <ul class="package-features">
                <li>تصوير سيشن فقط</li>
                <li>عدد الصور مفتوح ايديت كل الصور</li>
            </ul>
            <button class="btn-book" onclick="openModal('سيشن فقط - 3500 LE')">احجز الآن</button>
        </div>
        
        <div class="package-card">
            <h3 class="package-title">سيشن كتب كتاب</h3>
            <div class="package-price">2000 <span>LE</span></div>
            <ul class="package-features">
                <li>تغطية كتب الكتاب فقط</li>
            </ul>
            <button class="btn-book" onclick="openModal('سيشن كتب كتاب - 2000 LE')">احجز الآن</button>
        </div>

        <div class="package-card">
            <h3 class="package-title">سيشن خطوبة فقط</h3>
            <div class="package-price">1700 <span>LE</span></div>
            <ul class="package-features">
                <li>تغطية الخطوبة فقط</li>
            </ul>
            <button class="btn-book" onclick="openModal('سيشن خطوبة فقط - 1700 LE')">احجز الآن</button>
        </div>
        
        <div class="package-card">
            <h3 class="package-title">سيشن عيد ميلاد</h3>
            <div class="package-price">1500 <span>LE</span></div>
            <ul class="package-features">
                <li>عدد الصور مفتوح ايديت</li>
                <li>Rails</li>
            </ul>
            <button class="btn-book" onclick="openModal('سيشن عيد ميلاد - 1500 LE')">احجز الآن</button>
        </div>
        
        <div class="package-card">
            <h3 class="package-title">سيشن كاجول</h3>
            <div class="package-price">1200 <span>LE</span></div>
            <ul class="package-features">
                <li>عدد الصور مفتوح ايديت</li>
                <li>Rails</li>
            </ul>
            <button class="btn-book" onclick="openModal('سيشن كاجول - 1200 LE')">احجز الآن</button>
        </div>
    </div>

    <div class="extras-note">
        <p>ملاحظة: تصوير داخل قصر أو فندق يضاف 500 ج.م | انتقالات خارج الجيزة أو سفر يضاف 1000 ج.م</p>
    </div>

    <!-- آراء العملاء -->
    <h2 class="section-title">قالوا عن شغلنا (Reviews)</h2>
    <div class="reviews-container">
        <div class="review-card">
            <p class="review-text">"تسلم إيدك يا فنان، الصور طلعت تحفة وعجبت كل الناس بجد، أنا وعريسي مبسوطين أوي بالنتيجة واليوم كان زي الفل."</p>
            <p class="review-author">- عروسة شهر 9</p>
        </div>
        <div class="review-card">
            <p class="review-text">"والله ما قصرت معانا، يوم متعب وزحمة بس طلعتنا قمرات وعرفت تطلع مننا أحسن حاجة، عاش يا عبد الله."</p>
            <p class="review-author">- محمود وندى</p>
        </div>
        <div class="review-card">
            <p class="review-text">"أحسن مصور في الدنيا، مريح جدا في التعامل والسيشن كان كله ضحك وهزار ومحسيناش بتوتر الكاميرا خالص."</p>
            <p class="review-author">- أحمد وسارة</p>
        </div>
        <div class="review-card">
            <p class="review-text">"الصور بتتكلم عن نفسها، الألبوم فخم جدا والتسليم في ميعاده بالظبط، تسلم يا محترم شغل يرفع الراس قدام أهلنا."</p>
            <p class="review-author">- مصطفى عريس</p>
        </div>
        <div class="review-card">
            <p class="review-text">"بجد شغل عالي أوي، البرومو كأنه فيلم سينما، شكرا ليك ولتيم العمل كله تعبكم واضح في جودة الصور."</p>
            <p class="review-author">- أسماء</p>
        </div>
        <div class="review-card">
            <p class="review-text">"يا فنان، بجد كل اللي شاف الصور سألني مين المصور، استلمنا الألبوم والتابلوهات حاجة تفرح بجد."</p>
            <p class="review-author">- محمد وحبيبة</p>
        </div>
    </div>

    <!-- قسم التواصل والروابط -->
    <div class="contact-section">
        <h2 class="section-title">تواصل معنا</h2>
        
        <div class="contact-wrapper">
            <!-- قائمة السوشيال ميديا بشكل عمودي ومنظم -->
            <div class="social-list">
                <a href="https://www.facebook.com/profile.php?id=100071408364892" target="_blank" class="social-link">
                    <span class="social-icon"><i class="fab fa-facebook-f"></i></span>
                    <span class="social-text">لمتابعة أعمالنا على فيسبوك</span>
                </a>
                
                <a href="https://www.instagram.com/abdullah_maseud?igsh=NXB6b3B6cjJhYmF2&utm_source=qr" target="_blank" class="social-link">
                    <span class="social-icon"><i class="fab fa-instagram"></i></span>
                    <span class="social-text">لمتابعة أعمالنا على إنستجرام</span>
                </a>

                <a href="https://www.tiktok.com/@abood_foto" target="_blank" class="social-link">
                    <span class="social-icon"><i class="fab fa-tiktok"></i></span>
                    <span class="social-text">لمتابعة فيديوهاتنا على تيك توك</span>
                </a>

                <a href="https://api.whatsapp.com/send/?phone=201010356451&text&type=phone_number&app_absent=0" target="_blank" class="social-link">
                    <span class="social-icon"><i class="fab fa-whatsapp"></i></span>
                    <span class="social-text">للحجز والاستفسار عبر واتساب</span>
                </a>
            </div>

            <!-- معلومات الدفع والتواصل كأرقام -->
            <div class="contact-badges">
                <div class="badge">WhatsApp: +20 10 10356451</div>
                <div class="badge">Vodafone Cash: +20 10 10356451</div>
                <div class="badge">InstaPay Accepted</div>
            </div>
        </div>
    </div>

    <!-- الفوتر -->
    <footer>
        <p>True Love Stories Never Have Endings.</p>
        <p style="color: var(--gold); font-weight: bold; margin-top: 5px;">Abdallah Masoud Photographer</p>
        
        <!-- حقوق المطور -->
        <div class="dev-credit">
            Developed by: <a href="https://wa.me/201109176051" target="_blank">Mahmoud Saeed ( BOPO ) - 01109176051</a>
        </div>
    </footer>

    <!-- نافذة الحجز (Modal) -->
    <div class="modal-overlay" id="bookingModal">
        <div class="modal-content">
            <button class="close-btn" onclick="closeModal()">×</button>
            <h3>تأكيد الحجز</h3>
            <form id="bookingForm">
                <input type="hidden" id="selectedPackage">
                
                <div class="form-group">
                    <label>اسم العريس (بالانجليزي):</label>
                    <input type="text" id="groomName" required placeholder="Groom Name">
                </div>
                
                <div class="form-group">
                    <label>اسم العروسة (بالانجليزي):</label>
                    <input type="text" id="brideName" required placeholder="Bride Name">
                </div>
                
                <div class="form-group">
                    <label>رقم الواتساب للتواصل:</label>
                    <input type="tel" id="whatsappNum" required placeholder="01xxxxxxxxx">
                </div>
                
                <div class="form-group">
                    <label>تاريخ المناسبة:</label>
                    <input type="date" id="eventDate" required>
                    <small style="color:var(--gold); display:block; margin-top:5px;">
                        * ملحوظة: في حال وجود حجز مسبق في نفس اليوم، سيتم إبلاغك للتنسيق لاختيار ميعاد مناسب أو تأكيد إمكانية التنفيذ.
                    </small>
                </div>
                
                <div class="form-group">
                    <label>مكان السيشن:</label>
                    <input type="text" id="sessionLocation" placeholder="اسم المكان / الفندق">
                </div>
                
                <div class="form-group">
                    <label>مكان القاعة:</label>
                    <input type="text" id="hallLocation" placeholder="اسم القاعة والمحافظة">
                </div>
                
                <div class="form-group">
                    <label>ملاحظات إضافية:</label>
                    <textarea id="notes" rows="2" placeholder="أي تفاصيل أو طلبات إضافية..."></textarea>
                </div>

                <div class="terms-box">
                    <strong>شروط الحجز:</strong><br>
                    1- الحساب بيكون خالص يوم المناسبة لسرعة الاستلام.<br>
                    2- في حالة إلغاء الحجز لا يتم استرداد العربون (الديپوزت) ومتاح التأجيل ليوم آخر.
                </div>

                <div class="checkbox-group">
                    <input type="checkbox" id="agreeTerms" required>
                    <label for="agreeTerms">أوافق على تفاصيل وشروط الحجز المذكورة أعلاه.</label>
                </div>

                <button type="button" class="btn-book" onclick="submitBooking()">إرسال الحجز عبر واتساب</button>
            </form>
        </div>
    </div>

    <script>
        // دوال التحكم في النافذة المنبثقة
        const modal = document.getElementById('bookingModal');
        const selectedPackageInput = document.getElementById('selectedPackage');

        function openModal(packageName) {
            selectedPackageInput.value = packageName;
            modal.style.display = 'flex';
        }

        function closeModal() {
            modal.style.display = 'none';
        }

        // إغلاق النافذة عند الضغط خارجها
        window.onclick = function(event) {
            if (event.target == modal) {
                closeModal();
            }
        }

        // دالة إرسال البيانات للواتساب
        function submitBooking() {
            const groomName = document.getElementById('groomName').value;
            const brideName = document.getElementById('brideName').value;
            const whatsappNum = document.getElementById('whatsappNum').value;
            const eventDate = document.getElementById('eventDate').value;
            const sessionLocation = document.getElementById('sessionLocation').value;
            const hallLocation = document.getElementById('hallLocation').value;
            const notes = document.getElementById('notes').value;
            const agree = document.getElementById('agreeTerms').checked;
            const package = selectedPackageInput.value;

            if(!groomName || !brideName || !whatsappNum || !eventDate || !agree) {
                alert("يرجى ملء جميع الحقول المطلوبة والموافقة على الشروط.");
                return;
            }

            // تجهيز الرسالة
            let message = `*طلب حجز جديد* 📸\n\n`;
            message += `*الباقة المطلوبة:* ${package}\n`;
            message += `*اسم العريس:* ${groomName}\n`;
            message += `*اسم العروسة:* ${brideName}\n`;
            message += `*رقم العميل:* ${whatsappNum}\n`;
            message += `*التاريخ:* ${eventDate}\n`;
            message += `*مكان السيشن:* ${sessionLocation || 'لم يحدد'}\n`;
            message += `*مكان القاعة:* ${hallLocation || 'لم يحدد'}\n\n`;
            message += `*ملاحظات:* ${notes || 'لا يوجد'}\n\n`;
            message += `✅ العميل موافق على شروط الحجز والدفع.`;

            // تحويل للواتساب الخاص بك
            const photographerWhatsapp = "201010356451"; 
            const whatsappUrl = `https://wa.me/${photographerWhatsapp}?text=${encodeURIComponent(message)}`;
            
            window.open(whatsappUrl, '_blank');
            closeModal();
        }
    </script>
</body>
</html>
