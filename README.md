<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abdallah Masoud | Photographer</title>
    <!-- خطوط جوجل -->
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;800&family=Montserrat:wght@700&display=swap" rel="stylesheet">
    <!-- مكتبة الأيقونات -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --gold: #d4af37;
            --gold-glow: rgba(212, 175, 55, 0.6);
            --text-light: #ffffff;
            --text-muted: #cccccc;
            --glass-bg: rgba(20, 20, 20, 0.45); 
            --glass-border: rgba(255, 255, 255, 0.1);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Cairo', sans-serif;
        }

        body {
            background: linear-gradient(-45deg, #0a0a0a, #1a1710, #05080f, #121212);
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

        header {
            padding: 4rem 1rem 2rem;
            text-align: center;
        }

        header h1 {
            color: var(--gold);
            font-family: 'Montserrat', sans-serif;
            font-size: 3rem;
            margin-bottom: 0.2rem;
            letter-spacing: 3px;
            text-shadow: 0 0 15px rgba(212, 175, 55, 0.3);
        }

        .section-title {
            color: var(--gold);
            font-size: 1.8rem;
            margin: 3rem 5% 1.5rem;
            border-right: 4px solid var(--gold);
            padding-right: 15px;
            text-shadow: 0 0 10px rgba(212, 175, 55, 0.2);
        }

        .packages-container {
            max-width: 900px;
            margin: 0 auto;
            padding: 0 20px;
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .package-card {
            background: var(--glass-bg);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid var(--glass-border);
            border-radius: 15px;
            padding: 25px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.4);
            position: relative;
            overflow: hidden;
        }

        .package-card:hover {
            border-color: var(--gold);
            transform: translateY(-8px);
            box-shadow: 0 15px 35px var(--gold-glow), inset 0 0 20px rgba(212, 175, 55, 0.1);
        }

        .package-card::before {
            content: '';
            position: absolute;
            top: 0; left: -100%;
            width: 50%; height: 100%;
            background: linear-gradient(to right, transparent, rgba(255,255,255,0.05), transparent);
            transform: skewX(-25deg);
            transition: all 0.7s ease;
        }
        .package-card:hover::before { left: 150%; }

        .package-content { flex: 1; padding-left: 20px; z-index: 1; }
        .package-title { font-size: 1.5rem; color: #fff; margin-bottom: 10px; display: flex; align-items: center; gap: 10px; }
        .package-title i { color: var(--gold); }
        .package-desc { color: var(--text-muted); font-size: 0.95rem; margin-bottom: 15px; }
        .package-features { list-style: none; }
        .package-features li { font-size: 0.95rem; color: #eee; margin-bottom: 8px; display: flex; align-items: center; gap: 8px; }
        .package-features li i { color: var(--gold); font-size: 0.8rem; }

        .package-action { display: flex; flex-direction: column; align-items: center; gap: 15px; min-width: 160px; z-index: 1; }
        .price-box { background: rgba(212, 175, 55, 0.9); color: #000; padding: 12px 20px; border-radius: 8px; font-weight: 800; font-size: 1.3rem; text-align: center; width: 100%; box-shadow: 0 4px 15px rgba(212, 175, 55, 0.4); }
        .btn-book { background: rgba(0, 0, 0, 0.5); color: var(--gold); border: 1px solid var(--gold); padding: 10px 20px; font-size: 1.1rem; font-weight: bold; border-radius: 8px; cursor: pointer; width: 100%; transition: 0.3s; }
        .btn-book:hover { background: var(--gold); color: #000; box-shadow: 0 0 15px var(--gold-glow); }

        .location-section { background: var(--glass-bg); backdrop-filter: blur(16px); border: 1px solid var(--glass-border); border-radius: 15px; padding: 30px; text-align: center; max-width: 900px; margin: 40px auto; }
        .btn-map { background-color: #a81c1c; color: #fff; text-decoration: none; padding: 12px 25px; border-radius: 8px; font-weight: bold; display: inline-flex; align-items: center; gap: 10px; transition: 0.3s; }
        .btn-map:hover { background-color: #c92a2a; box-shadow: 0 0 15px rgba(201, 42, 42, 0.5); }

        .reviews-wrapper { max-width: 900px; margin: 0 auto; background: var(--glass-bg); backdrop-filter: blur(16px); border: 1px solid var(--glass-border); border-radius: 15px; padding: 20px; overflow: hidden; position: relative; height: 350px; }
        .reviews-scroll-area { display: flex; flex-direction: column; gap: 15px; animation: scrollReviews 40s linear infinite; }
        .reviews-wrapper:hover .reviews-scroll-area { animation-play-state: paused; }
        @keyframes scrollReviews { 0% { transform: translateY(0); } 100% { transform: translateY(-50%); } }
        .review-card { background: rgba(255, 255, 255, 0.03); border-right: 3px solid var(--gold); padding: 15px 20px; border-radius: 8px; }
        .review-text { font-style: italic; font-size: 1rem; margin-bottom: 10px; color: #eee; }
        .review-author { color: var(--gold); font-weight: bold; font-size: 0.9rem; }

        .social-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; max-width: 900px; margin: 20px auto 40px; padding: 0 20px; }
        .social-btn { background: var(--glass-bg); backdrop-filter: blur(16px); border: 1px solid var(--glass-border); color: #fff; text-decoration: none; padding: 15px; border-radius: 10px; display: flex; justify-content: center; align-items: center; gap: 10px; font-weight: bold; transition: 0.3s; }
        .social-btn:hover { border-color: var(--gold); background: rgba(212, 175, 55, 0.1); box-shadow: 0 0 15px var(--gold-glow); transform: translateY(-3px); }
        .social-btn.whatsapp { border-color: #25D366; }
        .social-btn.whatsapp i { color: #25D366; font-size: 1.2rem; }

        .phones-box { background: var(--glass-bg); backdrop-filter: blur(16px); border: 1px solid var(--gold); border-radius: 10px; padding: 20px; max-width: 900px; margin: 0 auto 40px; text-align: center; box-shadow: 0 0 20px rgba(212, 175, 55, 0.15); }
        .phones-box h3 { color: var(--gold); margin-bottom: 10px; font-size: 1.3rem;}
        .phone-number { font-size: 1.5rem; font-weight: bold; letter-spacing: 2px; direction: ltr; }

        /* المودال الزجاجي وتفاصيل الفورم */
        .modal-overlay { display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0, 0, 0, 0.85); backdrop-filter: blur(8px); z-index: 1000; justify-content: center; align-items: center; }
        .modal-content { background: rgba(20, 20, 20, 0.9); backdrop-filter: blur(20px); width: 90%; max-width: 550px; padding: 30px; border-radius: 15px; border: 1px solid var(--gold); max-height: 90vh; overflow-y: auto; position: relative; box-shadow: 0 0 30px rgba(212,175,55,0.2); }
        .close-btn { position: absolute; top: 15px; left: 15px; background: none; border: none; color: var(--gold); font-size: 2rem; cursor: pointer; transition: 0.3s; }
        .close-btn:hover { transform: scale(1.2); }
        
        .total-price-display { background: rgba(212, 175, 55, 0.15); border: 1px dashed var(--gold); padding: 15px; text-align: center; border-radius: 8px; margin-bottom: 20px; }
        .total-price-display h2 { color: var(--gold); margin: 0; font-size: 1.5rem; }

        .form-group { margin-bottom: 15px; text-align: right; }
        .form-group label { display: block; margin-bottom: 5px; font-size: 0.95rem; color: #ddd; }
        .form-group input[type="text"], .form-group input[type="tel"], .form-group input[type="date"], .form-group textarea { width: 100%; padding: 12px; background: rgba(0,0,0,0.5); border: 1px solid #444; color: #fff; border-radius: 8px; transition: 0.3s; }
        .form-group input:focus, .form-group textarea:focus { outline: none; border-color: var(--gold); box-shadow: 0 0 10px rgba(212,175,55,0.3); }
        .form-group input[type="file"] { width: 100%; padding: 8px; background: rgba(0,0,0,0.3); border: 1px dashed var(--gold); color: #fff; border-radius: 8px; }

        .date-warning { display: none; background: rgba(212, 175, 55, 0.1); border-right: 4px solid var(--gold); padding: 15px; margin-top: 10px; font-size: 0.9rem; color: #eee; border-radius: 4px; animation: fadeIn 0.5s ease; text-align: right; line-height: 1.8;}
        @keyframes fadeIn { from { opacity: 0; transform: translateY(-5px); } to { opacity: 1; transform: translateY(0); } }

        .payment-info { background: rgba(0,0,0,0.4); border: 1px solid #333; padding: 20px; border-radius: 8px; margin-bottom: 20px; text-align: center; }
        
        .radio-group { background: rgba(0,0,0,0.3); border: 1px solid #333; padding: 15px; border-radius: 8px; margin-bottom: 15px; text-align: right; }
        .radio-option { display: flex; align-items: center; gap: 10px; margin-bottom: 10px; font-size: 0.9rem; cursor: pointer; color: #eee; }
        
        .custom-box { display: flex; align-items: center; gap: 10px; padding: 12px; border-radius: 8px; margin-bottom: 15px; cursor: pointer; font-size: 0.9rem; text-align: right; color: #eee; }
        .box-gold { border: 1px dashed var(--gold); background: rgba(212, 175, 55, 0.05); }
        .box-red { border: 1px dashed #ff4444; background: rgba(255, 68, 68, 0.05); }

        @media (max-width: 768px) {
            .package-card { flex-direction: column; text-align: center; }
            .package-content { padding-left: 0; margin-bottom: 20px; }
            .package-title { justify-content: center; }
            .package-features li { justify-content: center; }
            .package-action { width: 100%; }
            .social-grid { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>

    <header>
        <h1>ABDALLAH MASOUD</h1>
        <p style="color: var(--text-muted); font-size: 1.1rem; letter-spacing: 5px;">P H O T O G R A P H E R</p>
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
                <button class="btn-book" onclick="openModal('Full Package', 8000)">احجز الآن</button>
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
                <button class="btn-book" onclick="openModal('Full Day', 6000)">احجز الآن</button>
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
                <button class="btn-book" onclick="openModal('Half Day', 4500)">احجز الآن</button>
            </div>
        </div>
    </div>

    <!-- باقات السيشن (تصوير فردي) -->
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
                <button class="btn-book" onclick="openModal('سيشن زفاف / خطوبة', 3500)">احجز الآن</button>
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
                <button class="btn-book" onclick="openModal('كتب كتاب', 2000)">احجز الآن (كتب كتاب)</button>
                <button class="btn-book" style="margin-top:-5px;" onclick="openModal('خطوبة فقط', 1700)">احجز الآن (خطوبة)</button>
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
                <button class="btn-book" onclick="openModal('سيشن عيد ميلاد', 1500)">احجز الآن (عيد ميلاد)</button>
                <button class="btn-book" style="margin-top:-5px;" onclick="openModal('سيشن كاجول', 1200)">احجز الآن (كاجول)</button>
            </div>
        </div>
    </div>

    <!-- عنوان الاستوديو -->
    <h2 class="section-title">عنوان الاستوديو</h2>
    <div class="location-section">
        <p><i class="fas fa-map-marker-alt" style="color:var(--gold); font-size:1.5rem; margin-bottom:10px;"></i><br><strong>منشأة القناطر - خلف مغسلة ياسين</strong></p>
        <a href="https://maps.app.goo.gl/qENQy7LbUjVQZTk99" target="_blank" class="btn-map">
            <i class="fas fa-map"></i> افتح موقعنا على الخريطة
        </a>
    </div>

    <!-- الفيدباك -->
    <h2 class="section-title">Clients Feedback <i class="fas fa-heart" style="color:var(--gold);"></i></h2>
    <div class="reviews-wrapper">
        <div class="reviews-scroll-area" id="reviewsArea">
            <!-- سيتم توليد مئات التقييمات هنا برمجياً -->
        </div>
    </div>

    <!-- تابعنا على -->
    <h2 class="section-title">تابعنا على</h2>
    <div class="social-grid">
        <a href="https://api.whatsapp.com/send/?phone=201010356451&text&type=phone_number&app_absent=0" target="_blank" class="social-btn whatsapp">
            Abdallah Masoud <i class="fab fa-whatsapp"></i>
        </a>
        <a href="https://www.instagram.com/abdullah_maseud?igsh=NXB6b3B6cjJhYmF2&utm_source=qr" target="_blank" class="social-btn">
            إنستجرام <i class="fab fa-instagram"></i>
        </a>
        <a href="https://www.facebook.com/profile.php?id=100071408364892" target="_blank" class="social-btn">
            فيسبوك <i class="fab fa-facebook-f"></i>
        </a>
        <a href="https://www.tiktok.com/@abood_foto" target="_blank" class="social-btn">
            تيك توك <i class="fab fa-tiktok"></i>
        </a>
    </div>

    <div class="phones-box">
        <h3><i class="fas fa-phone-alt"></i> أرقام اتصالات المكتب للتواصل</h3>
        <div class="phone-number">010 10356451</div>
    </div>

    <!-- الفوتر -->
    <footer style="text-align: center; padding: 25px; background: rgba(0,0,0,0.8); border-top: 1px solid #333;">
        <div style="font-size: 0.85rem; color: #777;">
            Developed by: <a href="https://wa.me/201109176051" target="_blank" style="color: #999; text-decoration: none; transition: 0.3s;">Mahmoud Saeed ( BOPO ) - 01109176051</a>
        </div>
    </footer>

    <!-- فورم الحجز الزجاجي -->
    <div class="modal-overlay" id="bookingModal">
        <div class="modal-content">
            <button class="close-btn" onclick="closeModal()">×</button>
            <h3 style="color: var(--gold); text-align: center; margin-bottom: 15px; font-size:1.8rem;">تأكيد الحجز</h3>
            
            <div class="total-price-display">
                <p style="margin-bottom:5px; color:#ccc;">الباقة المختارة: <strong id="modalPackageName" style="color:#fff;"></strong></p>
                <h2>إجمالي حسابك: <span id="modalPriceVal"></span> ج.م</h2>
            </div>

            <form id="bookingForm">
                <input type="hidden" id="selectedPackage">
                <input type="hidden" id="selectedPrice">
                
                <div class="form-group">
                    <label>اسم العريس (بالانجليزي):</label>
                    <input type="text" id="groomName" required placeholder="Groom Name">
                </div>
                
                <div class="form-group">
                    <label>اسم العروسة (بالانجليزي):</label>
                    <input type="text" id="brideName" required placeholder="Bride Name">
                </div>
                
                <div class="form-group">
                    <label>رقم الواتساب:</label>
                    <input type="tel" id="whatsappNum" required placeholder="01xxxxxxxxx">
                </div>
                
                <div class="form-group">
                    <label>تاريخ المناسبة:</label>
                    <input type="date" id="eventDate" required onchange="showDateWarning()">
                    <!-- رسالة التنبيه الذكية للتاريخ -->
                    <div id="dateWarning" class="date-warning">
                        <strong><i class="fas fa-info-circle" style="color:var(--gold);"></i> تنبيه هام:</strong><br>
                        في حالة كان هذا اليوم محجوزاً مسبقاً، سيتم توفير مصور محترف جداً من تيم المكتب الخاص بنا ليكون معاك، وفي حال مقدرة وتوفر وقت لـ "عبدالله مسعود" هيكون معاك شخصياً أكيد!
                        <label style="display:flex; align-items:center; gap:8px; margin-top:15px; cursor:pointer; color:var(--gold); font-weight:bold;">
                            <input type="checkbox" id="agreeDoubleBooking" required>
                            موافق على هذا الترتيب لاستكمال الحجز
                        </label>
                    </div>
                </div>

                <div class="form-group">
                    <label>مكان السيشن:</label>
                    <input type="text" id="sessionLocation" placeholder="اكتب اسم المكان أو المحافظة">
                </div>

                <div class="form-group">
                    <label>مكان القاعة:</label>
                    <input type="text" id="hallLocation" placeholder="اكتب اسم القاعة">
                </div>

                <!-- معلومات وطرق الدفع -->
                <div class="payment-info">
                    <p style="color:var(--gold); font-weight:bold; margin-bottom:10px; font-size:1.1rem;">طرق الدفع (InstaPay & Vodafone Cash)</p>
                    <div style="display:flex; justify-content:center; align-items:center; gap:15px; margin-bottom:15px;">
                        <span style="font-size:1.6rem; font-weight:bold; letter-spacing:2px; direction:ltr;">01010356451</span>
                        <button type="button" onclick="copyNumber()" style="background:var(--gold); color:#000; border:none; padding:8px 12px; border-radius:5px; cursor:pointer; font-weight:bold; font-size:0.9rem;"><i class="fas fa-copy"></i> Copy</button>
                    </div>
                    
                    <div class="form-group" style="text-align:right; border-top:1px dashed #444; padding-top:15px;">
                        <label style="color:var(--gold);">إرفاق سكرين شوت التحويل:</label>
                        <input type="file" id="transferReceipt" accept="image/*" required>
                        <small style="color:#aaa; display:block; margin-top:5px; font-size:0.8rem;">* قم برفع صورة التحويل هنا، وسيتم إرسالها تلقائياً عند الضغط على تأكيد وإرسال.</small>
                    </div>
                </div>

                <!-- بنود الموافقة -->
                <div class="form-group">
                    <label style="color:var(--gold); font-weight:bold; font-size:1rem; margin-bottom:10px;">هل توافق على مشاركة تفاصيل اليوم والصور على مواقع التواصل؟</label>
                    <div class="radio-group">
                        <label class="radio-option">
                            <input type="radio" name="sharePhotos" value="موافق على النشر في Facebook, Instagram, TikTok" checked required>
                            موافق على النشر في Facebook, Instagram, TikTok
                        </label>
                        <label class="radio-option" style="margin-top:10px;">
                            <input type="radio" name="sharePhotos" value="لا مش حابب أشارك أي صور على مواقع التواصل">
                            لا مش حابب أشارك أي صور على مواقع التواصل
                        </label>
                    </div>
                </div>

                <label class="custom-box box-gold">
                    <input type="checkbox" id="agreePayment" required>
                    الحساب بيكون خالص يوم المناسبة لسرعة الاستلام.
                </label>
                
                <label class="custom-box box-red">
                    <input type="checkbox" id="agreeCancel" required>
                    في حالة إلغاء الحجز لا يتم استرداد العربون ومتاح التأجيل.
                </label>

                <!-- الملاحظات -->
                <div class="form-group" style="margin-top:20px;">
                    <label style="color:var(--gold);">الملاحظات:</label>
                    <textarea id="notes" rows="3" placeholder="لو في اي تفاصيل لليوم العميل يكتبه ف الملاحظات... اكتب ملاحظاتك أو أي إضافات تانية هنا..."></textarea>
                </div>

                <button type="button" onclick="submitBooking()" style="background: var(--gold); color: #000; border: none; padding: 15px; width: 100%; border-radius: 8px; font-weight: bold; font-size:1.1rem; cursor: pointer; transition:0.3s; margin-top:10px;" onmouseover="this.style.boxShadow='0 0 15px rgba(212,175,55,0.6)'" onmouseout="this.style.boxShadow='none'">تأكيد وإرسال الحجز عبر واتساب</button>
            </form>
        </div>
    </div>

    <script>
        // دالة نسخ الرقم
        function copyNumber() {
            navigator.clipboard.writeText("01010356451").then(() => {
                alert("تم نسخ الرقم بنجاح!");
            });
        }

        // توليد الفيدباك
        const egyptianPhrases = [
            "بجد تسلم إيدك يا فنان، الصور طلعت روعة وكل اللي شافها اتوهم بيها.",
            "اليوم كان متعب جدا بس انت ريحتنا خالص في التعامل، والصور طالعة قمر.",
            "ريلز الفرح مكسر الدنيا عندنا، بجد عظمة على عظمة يا عبدالله.",
            "أحسن قرار أخدناه في الفرح إننا حجزنا معاك، الصور بتتكلم عن نفسها.",
            "والله ما قصرت معانا، استلمنا الألبوم والتابلوهات حاجة تشرف بجد.",
            "عاش يا فنان، اللقطات كلها طبيعية ومفيهاش تصنع، بجد فنان.",
            "أعظم مصور في مصر بدون مبالغة، الكواليتي بتاعت الصور وهمية.",
            "تعبناك معانا في اليوم بس النتيجة طلعت فوق خيالنا، ربنا يوفقك دايما.",
            "الميكينج والبرومو طالعين كأنهم فيلم سينما، شكرا ليك وللتيم كله.",
            "السيشن طلع قمر بجد، مريح جدا في التعامل ومحسيناش بتوتر الكاميرا.",
            "شغل عالي ومحترم، التسليم كان في ميعاده والألبوم خامته تحفة.",
            "كل الناس بتسألني مين المصور من حلاوة الصور، تسلم إيدك يا محترم.",
            "بجد ونعم الأخلاق والشطارة، فنان بمعنى الكلمة وبتعرف تطلع أحسن زوايا.",
            "فرحتنا كملت بشغلك، الصور ألوانها مبهجة وتفاصيلها تخطف العين.",
            "من أحسن الناس اللي اتعاملت معاهم، ذوق جدا وشغلك يتوزن بالدهب."
        ];
        const randomNames = ["أحمد ومروة", "محمود وندى", "عروسة شهر 9", "مصطفى عريس", "محمد وحبيبة", "كابتن إسلام", "سارة وأحمد", "عمر وياسمين", "دكتور كريم", "شهد وعلي"];

        const reviewsArea = document.getElementById('reviewsArea');
        let reviewsHTML = "";
        for(let i=0; i<100; i++) {
            let randomPhrase = egyptianPhrases[Math.floor(Math.random() * egyptianPhrases.length)];
            let randomName = randomNames[Math.floor(Math.random() * randomNames.length)];
            if(i%3 === 0) randomPhrase = "✨ " + randomPhrase;
            if(i%4 === 0) randomName += " 📸";
            reviewsHTML += `<div class="review-card"><p class="review-text">"${randomPhrase}"</p><p class="review-author">- ${randomName}</p></div>`;
        }
        reviewsArea.innerHTML = reviewsHTML + reviewsHTML;

        // إدارة المودال
        const modal = document.getElementById('bookingModal');
        
        function openModal(packageName, price) {
            document.getElementById('selectedPackage').value = packageName;
            document.getElementById('selectedPrice').value = price;
            document.getElementById('modalPackageName').innerText = packageName;
            document.getElementById('modalPriceVal').innerText = price;
            document.getElementById('dateWarning').style.display = 'none';
            document.getElementById('agreeDoubleBooking').checked = false;
            modal.style.display = 'flex';
        }

        function closeModal() { modal.style.display = 'none'; }
        window.onclick = function(event) { if (event.target == modal) closeModal(); }

        function showDateWarning() {
            const dateInput = document.getElementById('eventDate').value;
            if(dateInput) { document.getElementById('dateWarning').style.display = 'block'; }
        }

        function submitBooking() {
            const groom = document.getElementById('groomName').value;
            const bride = document.getElementById('brideName').value;
            const phone = document.getElementById('whatsappNum').value;
            const date = document.getElementById('eventDate').value;
            const sessionLoc = document.getElementById('sessionLocation').value;
            const hallLoc = document.getElementById('hallLocation').value;
            const package = document.getElementById('selectedPackage').value;
            const price = document.getElementById('selectedPrice').value;
            const notes = document.getElementById('notes').value;
            
            const agreeDoubleBooking = document.getElementById('agreeDoubleBooking');
            const agreePayment = document.getElementById('agreePayment').checked;
            const agreeCancel = document.getElementById('agreeCancel').checked;
            const shareRadio = document.querySelector('input[name="sharePhotos"]:checked');
            const receiptFile = document.getElementById('transferReceipt').files.length > 0;

            if(!groom || !bride || !phone || !date || !agreePayment || !agreeCancel || !receiptFile) {
                alert("يرجى ملء جميع البيانات الأساسية، وإرفاق سكرين شوت التحويل، والموافقة على الشروط السفلية.");
                return;
            }

            if(document.getElementById('dateWarning').style.display === 'block' && !agreeDoubleBooking.checked) {
                alert("يرجى الموافقة على ترتيب تواجد المصور في حال كان اليوم محجوزاً مسبقاً.");
                return;
            }

            let message = `*طلب حجز جديد من الموقع* 📸\n\n`;
            message += `*الباقة:* ${package}\n`;
            message += `*إجمالي الحساب:* ${price} ج.م\n`;
            message += `-------------------\n`;
            message += `*اسم العريس:* ${groom}\n`;
            message += `*اسم العروسة:* ${bride}\n`;
            message += `*التاريخ:* ${date}\n`;
            message += `*رقم العميل:* ${phone}\n`;
            message += `*مكان السيشن:* ${sessionLoc || 'لم يُحدد'}\n`;
            message += `*مكان القاعة:* ${hallLoc || 'لم يُحدد'}\n\n`;
            message += `*مشاركة الصور:* ${shareRadio.value}\n`;
            message += `✅ العميل موافق على دفع الحساب يوم المناسبة.\n`;
            message += `✅ العميل موافق على شروط إلغاء الحجز وعدم استرداد العربون.\n`;
            if(agreeDoubleBooking.checked) message += `✅ العميل موافق على ترتيب تواجد تيم المكتب في حال كان اليوم محجوزاً.\n`;
            if(receiptFile) message += `\n📎 *ملاحظة هامة:* العميل قام برفع سكرين شوت التحويل، برجاء التأكيد عليه بإرسال الصورة في هذه المحادثة.\n`;
            if(notes) message += `\n*ملاحظات إضافية:* ${notes}`;

            const photographerWhatsapp = "201010356451"; 
            const whatsappUrl = `https://wa.me/${photographerWhatsapp}?text=${encodeURIComponent(message)}`;
            window.open(whatsappUrl, '_blank');
            closeModal();
        }
    </script>
</body>
</html>
