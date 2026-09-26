<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abdallah Masoud | Photographer</title>
    <!-- خطوط جوجل -->
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;800&display=swap" rel="stylesheet">
    <!-- مكتبة الأيقونات -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --gold: #d4af37;
            --gold-dark: #b8972e;
            --text-light: #f5f5f5;
            --text-muted: #aaaaaa;
            --glass-bg: rgba(30, 30, 30, 0.55);
            --glass-border: rgba(212, 175, 55, 0.3);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Cairo', sans-serif;
        }

        /* خلفية متحركة لإبراز شكل الزجاج */
        body {
            background: linear-gradient(-45deg, #0d0d0d, #1a1813, #0a1118, #121212);
            background-size: 400% 400%;
            animation: gradientBG 15s ease infinite;
            color: var(--text-light);
            line-height: 1.6;
            min-height: 100vh;
        }

        @keyframes gradientBG {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* هيدر بسيط */
        header {
            padding: 3rem 1rem 1rem;
            text-align: center;
        }

        header h1 {
            color: var(--gold);
            font-size: 2.5rem;
            margin-bottom: 0.2rem;
            letter-spacing: 2px;
        }

        .section-title {
            color: var(--gold);
            font-size: 1.8rem;
            margin: 2rem 5% 1.5rem;
            border-right: 4px solid var(--gold);
            padding-right: 15px;
        }

        /* حاوية الباقات */
        .packages-container {
            max-width: 900px;
            margin: 0 auto;
            padding: 0 20px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        /* تصميم الكارت الزجاجي (Glassmorphism) */
        .package-card {
            background: var(--glass-bg);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid var(--glass-border);
            border-radius: 15px;
            padding: 25px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: all 0.3s ease;
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.3);
        }

        .package-card:hover {
            border-color: var(--gold);
            transform: translateY(-5px);
            box-shadow: 0 12px 40px 0 rgba(212, 175, 55, 0.15);
        }

        /* محتوى الباقة (اليمين) */
        .package-content {
            flex: 1;
            padding-left: 20px;
        }

        .package-title {
            font-size: 1.4rem;
            color: var(--text-light);
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .package-title i {
            color: var(--gold);
            font-size: 1.1rem;
        }

        .package-desc {
            color: var(--text-muted);
            font-size: 0.95rem;
            margin-bottom: 15px;
        }

        /* تفاصيل الباقة مع أيقونة النجمة */
        .package-features {
            list-style: none;
        }

        .package-features li {
            font-size: 0.9rem;
            color: #ddd;
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .package-features li i {
            color: var(--gold);
            font-size: 0.8rem;
        }

        /* السعر والزر (اليسار) */
        .package-action {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 15px;
            min-width: 150px;
        }

        .price-box {
            background-color: var(--gold);
            color: #000;
            padding: 10px 20px;
            border-radius: 8px;
            font-weight: 800;
            font-size: 1.2rem;
            text-align: center;
            width: 100%;
            box-shadow: 0 4px 15px rgba(212, 175, 55, 0.3);
        }

        .btn-book {
            background: transparent;
            color: var(--gold);
            border: 1px solid var(--gold);
            padding: 10px 20px;
            font-size: 1rem;
            font-weight: bold;
            border-radius: 8px;
            cursor: pointer;
            width: 100%;
            transition: 0.3s;
        }

        .btn-book:hover {
            background-color: var(--gold);
            color: #000;
        }

        /* قسم العنوان والخريطة زجاجي */
        .location-section {
            background: var(--glass-bg);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid var(--glass-border);
            border-radius: 15px;
            padding: 30px;
            text-align: center;
            max-width: 900px;
            margin: 40px auto;
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.3);
        }
        
        .location-section p {
            font-size: 1.1rem;
            margin-bottom: 20px;
        }

        .btn-map {
            background-color: #a81c1c;
            color: #fff;
            text-decoration: none;
            padding: 12px 25px;
            border-radius: 8px;
            font-weight: bold;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            transition: 0.3s;
        }

        .btn-map:hover {
            background-color: #c92a2a;
        }

        /* الفيدباك (قالوا عن عدستنا) */
        .reviews-container {
            max-width: 900px;
            margin: 0 auto;
            background: var(--glass-bg);
            backdrop-filter: blur(12px);
            border: 1px solid var(--glass-border);
            border-radius: 15px;
            padding: 30px;
            text-align: center;
        }
        
        .review-text {
            font-style: italic;
            font-size: 1.1rem;
            margin-bottom: 15px;
            color: #eee;
        }
        
        .review-author {
            color: var(--gold);
            font-weight: bold;
        }

        /* السوشيال ميديا شبكة زجاجية */
        .social-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            max-width: 900px;
            margin: 40px auto;
            padding: 0 20px;
        }

        .social-btn {
            background: var(--glass-bg);
            backdrop-filter: blur(12px);
            border: 1px solid #444;
            color: #fff;
            text-decoration: none;
            padding: 15px;
            border-radius: 10px;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 10px;
            font-weight: bold;
            transition: 0.3s;
        }

        .social-btn:hover {
            border-color: var(--gold);
            background: rgba(212, 175, 55, 0.1);
        }

        .social-btn.whatsapp { border-color: #25D366; }
        .social-btn.whatsapp i { color: #25D366; }

        .phones-box {
            background: var(--glass-bg);
            backdrop-filter: blur(12px);
            border: 1px solid #444;
            border-radius: 10px;
            padding: 20px;
            max-width: 900px;
            margin: 0 auto 40px;
            text-align: center;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
        }

        .phone-item {
            background: rgba(0,0,0,0.3);
            padding: 10px;
            border-radius: 5px;
            border: 1px dashed #555;
            direction: ltr;
        }

        /* المودال الزجاجي */
        .modal-overlay {
            display: none;
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0, 0, 0, 0.8);
            backdrop-filter: blur(5px);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }

        .modal-content {
            background: rgba(20, 20, 20, 0.85);
            backdrop-filter: blur(15px);
            width: 90%;
            max-width: 500px;
            padding: 30px;
            border-radius: 15px;
            border: 1px solid var(--gold);
            max-height: 90vh;
            overflow-y: auto;
            position: relative;
        }

        /* الموبايل ريسبونسيف */
        @media (max-width: 768px) {
            .package-card {
                flex-direction: column;
                text-align: center;
            }
            .package-content {
                padding-left: 0;
                margin-bottom: 20px;
            }
            .package-title { justify-content: center; }
            .package-features li { justify-content: center; }
            .package-action { width: 100%; }
        }

        /* تنسيقات فورم الحجز (البنود الجديدة) */
        .form-group { margin-bottom: 15px; }
        .form-group label { display: block; margin-bottom: 5px; font-size: 0.9rem; color: var(--gold); }
        .form-group input[type="text"], .form-group input[type="tel"], .form-group input[type="date"], .form-group textarea {
            width: 100%; padding: 10px; background: rgba(0,0,0,0.5); border: 1px solid #444; color: #fff; border-radius: 8px;
        }
        
        .custom-box {
            border-radius: 8px;
            padding: 12px;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 0.9rem;
        }
        .box-gold { border: 1px dashed var(--gold); background: rgba(212, 175, 55, 0.05); }
        .box-red { border: 1px dashed #ff4444; background: rgba(255, 68, 68, 0.05); }
        .radio-group { background: rgba(0,0,0,0.3); border: 1px solid #333; padding: 15px; border-radius: 8px; margin-bottom: 15px; }
        .radio-option { display: flex; align-items: center; gap: 10px; margin-bottom: 10px; font-size: 0.9rem; }
        .radio-option:last-child { margin-bottom: 0; }
    </style>
</head>
<body>

    <header>
        <h1>ABDALLAH MASOUD</h1>
        <p style="color: var(--text-muted); font-size: 1rem; letter-spacing: 4px;">P H O T O G R A P H E R</p>
    </header>

    <!-- الباقات الرئيسية -->
    <h2 class="section-title">الباقات الرئيسية (Wedding & Engagement)</h2>
    <div class="packages-container">
        
        <div class="package-card">
            <div class="package-content">
                <h3 class="package-title"><i class="fas fa-star"></i> باكدج كاملة (Full Package)</h3>
                <p class="package-desc">تغطية شاملة ليومك المميز بأعلى جودة وتفاصيل.</p>
                <ul class="package-features">
                    <li><i class="fas fa-star"></i> الميكب والتجهيزات + فريست لوك</li>
                    <li><i class="fas fa-star"></i> تصوير الجروب + البارتي (القاعة)</li>
                    <li><i class="fas fa-star"></i> السيشن (عدد الصور مفتوح ايديت)</li>
                    <li><i class="fas fa-star"></i> برومو & Rails</li>
                    <li><i class="fas fa-star"></i> ألبوم (30x80) + تابلو (50x70) + هدية تابلو (40x50) + فلاشة</li>
                </ul>
            </div>
            <div class="package-action">
                <div class="price-box">EGP 8000</div>
                <button class="btn-book" onclick="openModal('Full Package - 8000 EGP')">احجز الآن</button>
            </div>
        </div>

        <div class="package-card">
            <div class="package-content">
                <h3 class="package-title"><i class="fas fa-star"></i> باكدج (Full Day)</h3>
                <p class="package-desc">تغطية يوم الفرح من البداية للنهاية.</p>
                <ul class="package-features">
                    <li><i class="fas fa-star"></i> فريست لوك + تصوير الجروب</li>
                    <li><i class="fas fa-star"></i> السيشن (عدد الصور مفتوح ايديت) + البارتي</li>
                    <li><i class="fas fa-star"></i> Rails + برومو + فلاشة</li>
                    <li><i class="fas fa-star"></i> ألبوم (30x80) + تابلو (50x60) + هدية تابلو (30x40)</li>
                </ul>
            </div>
            <div class="package-action">
                <div class="price-box">EGP 6000</div>
                <button class="btn-book" onclick="openModal('Full Day - 6000 EGP')">احجز الآن</button>
            </div>
        </div>

        <div class="package-card">
            <div class="package-content">
                <h3 class="package-title"><i class="fas fa-star"></i> باكدج (Half Day)</h3>
                <p class="package-desc">باقة مناسبة للسيشن والجروب وتفاصيل سريعة.</p>
                <ul class="package-features">
                    <li><i class="fas fa-star"></i> السيشن (عدد الصور مفتوح ايديت)</li>
                    <li><i class="fas fa-star"></i> تصوير الجروب + Rails</li>
                    <li><i class="fas fa-star"></i> سيراميك كبير + تابلو (40x50)</li>
                </ul>
            </div>
            <div class="package-action">
                <div class="price-box">EGP 4500</div>
                <button class="btn-book" onclick="openModal('Half Day - 4500 EGP')">احجز الآن</button>
            </div>
        </div>
    </div>

    <!-- باقات السيشن (تصوير فردي) بنفس شكل الباقات الرئيسية -->
    <h2 class="section-title">تصوير فردي (Sessions)</h2>
    <div class="packages-container">
        
        <div class="package-card">
            <div class="package-content">
                <h3 class="package-title"><i class="fas fa-star"></i> سيشن زفاف / خطوبة</h3>
                <p class="package-desc">تصوير سيشن فقط الخارجي للعروسين.</p>
                <ul class="package-features">
                    <li><i class="fas fa-star"></i> تصوير سيشن فقط</li>
                    <li><i class="fas fa-star"></i> عدد الصور مفتوح ايديت كل الصور</li>
                </ul>
            </div>
            <div class="package-action">
                <div class="price-box">EGP 3500</div>
                <button class="btn-book" onclick="openModal('سيشن زفاف / خطوبة - 3500 EGP')">احجز الآن</button>
            </div>
        </div>
        
        <div class="package-card">
            <div class="package-content">
                <h3 class="package-title"><i class="fas fa-star"></i> خطوبة أو كتب كتاب</h3>
                <p class="package-desc">تصوير خطوبة أو كتب كتاب.</p>
                <ul class="package-features">
                    <li><i class="fas fa-star"></i> تغطية كتب الكتاب فقط 2000 ج.م</li>
                    <li><i class="fas fa-star"></i> تغطية الخطوبة فقط 1700 ج.م</li>
                </ul>
            </div>
            <div class="package-action">
                <div class="price-box">EGP 2000</div>
                <button class="btn-book" onclick="openModal('خطوبة أو كتب كتاب')">احجز الآن</button>
            </div>
        </div>

        <div class="package-card">
            <div class="package-content">
                <h3 class="package-title"><i class="fas fa-star"></i> سيشن كاجول / عيد ميلاد</h3>
                <p class="package-desc">سيشن خفيف للذكريات الجميلة.</p>
                <ul class="package-features">
                    <li><i class="fas fa-star"></i> سيشن عيد ميلاد (1500 ج.م)</li>
                    <li><i class="fas fa-star"></i> سيشن كاجول (1200 ج.م)</li>
                    <li><i class="fas fa-star"></i> عدد الصور مفتوح ايديت + Rails</li>
                </ul>
            </div>
            <div class="package-action">
                <div class="price-box">EGP 1500</div>
                <button class="btn-book" onclick="openModal('سيشن كاجول / عيد ميلاد')">احجز الآن</button>
            </div>
        </div>
    </div>

    <!-- عنوان الاستوديو -->
    <h2 class="section-title">عنوان الاستوديو</h2>
    <div class="location-section">
        <p><i class="fas fa-map-marker-alt" style="color:var(--gold)"></i> <strong>منشأة القناطر - خلف مغسلة ياسين</strong></p>
        <a href="https://maps.app.goo.gl/qENQy7LbUjVQZTk99" target="_blank" class="btn-map">
            <i class="fas fa-map"></i> افتح موقعنا على الخريطة
        </a>
    </div>

    <!-- قالوا عن عدستنا -->
    <h2 class="section-title">قالوا عن عدستنا <i class="fas fa-comment-dots" style="color:var(--gold); font-size: 1.2rem;"></i></h2>
    <div class="reviews-container">
        <p class="review-text">"الألبوم طالع تحفة والألوان بجد سينمائية وريلز الفرح مكسر الدنيا عندنا تسلم إيدك"</p>
        <p class="review-author"><i class="fas fa-star" style="font-size: 0.8rem;"></i> كابتن محمد & آية</p>
    </div>

    <!-- تابعنا على -->
    <h2 class="section-title">تابعنا على</h2>
    <div class="social-grid">
        <a href="https://api.whatsapp.com/send/?phone=201010356451&text&type=phone_number&app_absent=0" target="_blank" class="social-btn whatsapp">
            Ali WhatsApp <i class="fab fa-whatsapp"></i>
        </a>
        <a href="#" class="social-btn">
            رقم المكتب <i class="fas fa-circle" style="color:#25D366; font-size: 0.6rem;"></i>
        </a>
        <a href="https://www.instagram.com/abdullah_maseud?igsh=NXB6b3B6cjJhYmF2&utm_source=qr" target="_blank" class="social-btn">
            إنستجرام
        </a>
        <a href="https://www.facebook.com/profile.php?id=100071408364892" target="_blank" class="social-btn">
            فيسبوك
        </a>
        <a href="https://www.tiktok.com/@abood_foto" target="_blank" class="social-btn" style="grid-column: span 2;">
            تيك توك
        </a>
    </div>

    <div class="phones-box">
        <div style="grid-column: span 2; color: var(--gold); font-weight: bold; margin-bottom: 10px;">
            <i class="fas fa-phone-alt"></i> أرقام اتصالات المكتب:
        </div>
        <div class="phone-item">01122382861</div>
        <div class="phone-item">01505827390</div>
        <div class="phone-item">01009292635</div>
        <div class="phone-item">01094019014</div>
    </div>

    <!-- الفوتر -->
    <footer style="text-align: center; padding: 20px; background: rgba(0,0,0,0.5); border-top: 1px solid #333;">
        <div style="font-size: 0.8rem; color: #666;">
            Developed by: <a href="https://wa.me/201109176051" target="_blank" style="color: #888; text-decoration: none;">Mahmoud Saeed ( BOPO ) - 01109176051</a>
        </div>
    </footer>

    <!-- فورم الحجز الزجاجي -->
    <div class="modal-overlay" id="bookingModal">
        <div class="modal-content">
            <button onclick="closeModal()" style="position: absolute; top: 15px; left: 15px; background: none; border: none; color: var(--gold); font-size: 1.5rem; cursor: pointer;">×</button>
            <h3 style="color: var(--gold); text-align: center; margin-bottom: 20px;">تأكيد الحجز</h3>
            <form id="bookingForm">
                <input type="hidden" id="selectedPackage">
                
                <div class="form-group">
                    <label>اسم العريس (بالانجليزي):</label>
                    <input type="text" id="groomName" required>
                </div>
                
                <div class="form-group">
                    <label>اسم العروسة (بالانجليزي):</label>
                    <input type="text" id="brideName" required>
                </div>
                
                <div class="form-group">
                    <label>رقم الواتساب:</label>
                    <input type="tel" id="whatsappNum" required>
                </div>
                
                <div class="form-group">
                    <label>تاريخ المناسبة:</label>
                    <input type="date" id="eventDate" required>
                </div>

                <!-- سؤال مشاركة الصور -->
                <div class="form-group">
                    <label>هل توافق على مشاركة تفاصيل اليوم والصور على مواقع التواصل؟</label>
                    <div class="radio-group">
                        <label class="radio-option">
                            <input type="radio" name="sharePhotos" value="موافق" required> موافق على النشر في Facebook, Instagram, TikTok
                        </label>
                        <label class="radio-option">
                            <input type="radio" name="sharePhotos" value="غير موافق"> لا مش حابب أشارك أي صور على مواقع التواصل
                        </label>
                    </div>
                </div>

                <!-- بنود الموافقة بالشكل المطلوب -->
                <label class="custom-box box-gold">
                    <input type="checkbox" id="agreePayment" required>
                    الحساب بيكون خالص يوم المناسبة لسرعة الاستلام.
                </label>
                
                <label class="custom-box box-red">
                    <input type="checkbox" id="agreeCancel" required>
                    في حالة إلغاء الحجز لا يتم استرداد العربون ومتاح التأجيل.
                </label>

                <div class="form-group">
                    <label>لو في أي ملاحظات ممكن تكتبها هنا:</label>
                    <textarea id="notes" rows="2" placeholder="اكتب ملاحظاتك أو أي إضافات تانية هنا..."></textarea>
                </div>

                <button type="button" onclick="submitBooking()" style="background: var(--gold); color: #000; border: none; padding: 12px; width: 100%; border-radius: 8px; font-weight: bold; cursor: pointer; margin-top: 10px;">إرسال الحجز عبر واتساب</button>
            </form>
        </div>
    </div>

    <script>
        const modal = document.getElementById('bookingModal');
        const selectedPackageInput = document.getElementById('selectedPackage');

        function openModal(packageName) {
            selectedPackageInput.value = packageName;
            modal.style.display = 'flex';
        }

        function closeModal() {
            modal.style.display = 'none';
        }

        window.onclick = function(event) {
            if (event.target == modal) closeModal();
        }

        function submitBooking() {
            const groom = document.getElementById('groomName').value;
            const bride = document.getElementById('brideName').value;
            const phone = document.getElementById('whatsappNum').value;
            const date = document.getElementById('eventDate').value;
            const notes = document.getElementById('notes').value;
            const package = selectedPackageInput.value;
            
            const agreePayment = document.getElementById('agreePayment').checked;
            const agreeCancel = document.getElementById('agreeCancel').checked;
            
            const shareRadio = document.querySelector('input[name="sharePhotos"]:checked');

            if(!groom || !bride || !phone || !date || !shareRadio || !agreePayment || !agreeCancel) {
                alert("يرجى ملء جميع البيانات واختيار الموافقة على الشروط.");
                return;
            }

            let message = `*طلب حجز جديد* 📸\n\n`;
            message += `*الباقة:* ${package}\n`;
            message += `*العريس:* ${groom}\n`;
            message += `*العروسة:* ${bride}\n`;
            message += `*التاريخ:* ${date}\n`;
            message += `*الرقم:* ${phone}\n\n`;
            message += `*مشاركة الصور:* ${shareRadio.value}\n`;
            message += `✅ موافق على دفع الحساب يوم المناسبة\n`;
            message += `✅ موافق على شرط إلغاء الحجز\n\n`;
            if(notes) message += `*ملاحظات:* ${notes}`;

            const photographerWhatsapp = "201010356451"; 
            const whatsappUrl = `https://wa.me/${photographerWhatsapp}?text=${encodeURIComponent(message)}`;
            window.open(whatsappUrl, '_blank');
            closeModal();
        }
    </script>
</body>
</html>
