<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>COSMOS</title>

<style>
* {
    box-sizing: border-box;
    scroll-behavior: smooth;
}

body {
    margin: 0;
    font-family: Tahoma, Arial, sans-serif;
    background: #050817;
    color: white;
    line-height: 1.9;
}

header {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 25px;
    background:
        radial-gradient(circle at 20% 20%, #51408f, transparent 30%),
        radial-gradient(circle at 80% 70%, #075078, transparent 35%),
        linear-gradient(135deg, #050817, #101538, #071b36);
}

header h1 {
    font-size: clamp(60px, 12vw, 110px);
    margin: 10px 0;
    letter-spacing: 8px;
    text-shadow: 0 0 30px #528dff;
}

header p {
    max-width: 650px;
    color: #d4e8ff;
    font-size: 19px;
}

.button {
    display: inline-block;
    margin-top: 20px;
    padding: 12px 30px;
    border-radius: 30px;
    background: #70e7ff;
    color: #061124;
    text-decoration: none;
    font-weight: bold;
}

section {
    padding: 60px 7%;
}

h2 {
    text-align: center;
    color: #83eaff;
    font-size: 32px;
}

.description {
    text-align: center;
    color: #c2cde4;
    max-width: 750px;
    margin: 0 auto 35px;
}

.about {
    background: #0a1025;
}

.info-box {
    max-width: 900px;
    margin: auto;
    padding: 25px;
    background: #101a35;
    border: 1px solid #263d69;
    border-radius: 20px;
}

.planets {
    background: #070b1c;
}

.planet-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(210px, 1fr));
    gap: 22px;
}

.planet-card {
    background: linear-gradient(145deg, #131e3c, #090f22);
    border: 1px solid #293e68;
    border-radius: 20px;
    padding: 25px 20px;
    text-align: center;
    transition: 0.3s;
}

.planet-card:hover {
    transform: translateY(-5px);
    border-color: #70e7ff;
}

.planet {
    width: 105px;
    height: 105px;
    border-radius: 50%;
    margin: 0 auto 15px;
    box-shadow: inset -15px -10px 20px #0008;
}

.mercury {
    background: radial-gradient(circle at 30% 25%, #bcb8b3, #686875 65%, #33364b);
}

.venus {
    background: radial-gradient(circle at 30% 25%, #fff0b7, #d79a55 60%, #764a3a);
}

.earth {
    background:
        radial-gradient(circle at 35% 35%, #6de2ff 0 10%, transparent 11%),
        radial-gradient(circle at 65% 65%, #61d58a 0 14%, transparent 15%),
        radial-gradient(circle at 35% 35%, #3e94ff, #1740a3 65%, #07153e);
}

.mars {
    background: radial-gradient(circle at 30% 25%, #ffb18c, #d34d35 60%, #6b2028);
}

.jupiter {
    background: repeating-linear-gradient(
        0deg, #d9b68d 0 10px, #a96f54 10px 18px,
        #f2d7b0 18px 27px, #9c674f 27px 35px
    );
}

.saturn {
    background: radial-gradient(circle at 30% 25%, #f4e2ae, #c7a56b 65%, #765e47);
    position: relative;
}

.saturn::after {
    content: "";
    position: absolute;
    width: 140px;
    height: 35px;
    border: 6px solid #ddc89a;
    border-radius: 50%;
    top: 32px;
    left: -20px;
    transform: rotate(-20deg);
}

.uranus {
    background: radial-gradient(circle at 30% 25%, #c8ffff, #69d5e2 65%, #347b9d);
}

.neptune {
    background: radial-gradient(circle at 30% 25%, #75baff, #2855d8 60%, #101d78);
}

.planet-card h3 {
    color: #8beaff;
    font-size: 22px;
}

.planet-card p {
    color: #d1d9ed;
    font-size: 15px;
}

.facts {
    background: #0b1329;
}

.facts-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 20px;
}

.fact {
    padding: 22px;
    background: #131e3a;
    border-radius: 16px;
    border-right: 4px solid #70e7ff;
}

.fact h3 {
    color: #8beaff;
}

.sultan {
    background: linear-gradient(140deg, #080d20, #111b36);
    text-align: center;
}

.sultan-card {
    max-width: 850px;
    margin: 30px auto 0;
    padding: 25px;
    background: #101a32;
    border: 1px solid #314b79;
    border-radius: 24px;
}

.sultan-photo {
    display: block;
    width: 100%;
    max-width: 560px;
    height: auto;
    margin: 0 auto 25px;
    border-radius: 18px;
    border: 2px solid #70e7ff;
    box-shadow: 0 0 30px #397cff35;
}

.sultan-card h3 {
    color: #83eaff;
    font-size: 27px;
}

.sultan-card p {
    color: #d8e3f7;
    font-size: 17px;
    text-align: right;
}

.stars {
    background:
        radial-gradient(circle at 20% 20%, #172c5a, transparent 35%),
        #060a19;
}

.star-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 20px;
}

.star-card {
    padding: 23px;
    border-radius: 18px;
    background: #111a33;
    border: 1px solid #293e68;
}

.star-card h3 {
    color: #8beaff;
}

.star-icon {
    font-size: 42px;
    color: #b9eaff;
    text-shadow: 0 0 20px #70cfff;
}

@media (max-width: 600px) {
    section {
        padding: 45px 6%;
    }

    h2 {
        font-size: 27px;
    }

    .info-box, .sultan-card {
        padding: 18px;
    }
}
</style>
</head>

<body>

<!-- الصفحة الرئيسية -->
<header>
    <h1>COSMOS</h1>
    <p>
        اكتشفي أسرار الكون، وتعرّفي على الكواكب والنجوم،
        واستكشفي عظمة الفضاء الواسع.
    </p>
    <a href="#about" class="button">ابدئي الاستكشاف ✦</a>
</header>

<!-- مقدمة عن الفضاء -->
<section class="about" id="about">
    <h2>ما هو الفضاء؟</h2>
    <p class="description">عالم واسع مليء بالأسرار والاكتشافات.</p>

    <div class="info-box">
        <p>
            الفضاء هو الامتداد الواسع الذي توجد فيه النجوم والكواكب
            والمجرات والأجرام السماوية. ويستكشف العلماء الكون باستخدام
            التلسكوبات والأقمار الصناعية والمركبات الفضائية.
        </p>
        <p>
            تقع الأرض في المجموعة الشمسية، وهي جزء من مجرة درب التبانة،
            التي تحتوي على أعداد هائلة من النجوم.
        </p>
    </div>
</section>

<!-- الكواكب -->
<section class="planets" id="planets">
    <h2>كواكب المجموعة الشمسية</h2>
    <p class="description">
        ثمانية كواكب تدور حول الشمس، ولكل كوكب خصائصه المميزة.
    </p>

    <div class="planet-grid">

        <div class="planet-card">
            <div class="planet mercury"></div>
            <h3>عطارد</h3>
            <p>أقرب الكواكب إلى الشمس، وهو أصغر كواكب المجموعة الشمسية.</p>
        </div>

        <div class="planet-card">
            <div class="planet venus"></div>
            <h3>الزهرة</h3>
            <p>أشد الكواكب حرارة بسبب غلافه الجوي الكثيف.</p>
        </div>

        <div class="planet-card">
            <div class="planet earth"></div>
            <h3>الأرض</h3>
            <p>موطننا، وتتميز بوجود الماء السائل والحياة المعروفة.</p>
        </div>

        <div class="planet-card">
            <div class="planet mars"></div>
            <h3>المريخ</h3>
            <p>الكوكب الأحمر، ويبحث العلماء عن آثار الماء القديم على سطحه.</p>
        </div>

        <div class="planet-card">
            <div class="planet jupiter"></div>
            <h3>المشتري</h3>
            <p>أكبر كواكب المجموعة الشمسية، ويشتهر بعواصفه الضخمة.</p>
        </div>

        <div class="planet-card">
            <div class="planet saturn"></div>
            <h3>زحل</h3>
            <p>يشتهر بحلقاته الواسعة المكوّنة من الجليد والصخور والغبار.</p>
        </div>

        <div class="planet-card">
            <div class="planet uranus"></div>
            <h3>أورانوس</h3>
            <p>عملاق جليدي أزرق مخضر، ويدور حول الشمس بطريقة مائلة جدًا.</p>
        </div>

        <div class="planet-card">
            <div class="planet neptune"></div>
            <h3>نبتون</h3>
            <p>أبعد كواكب المجموعة الشمسية عن الشمس، ويتميز بلونه الأزرق.</p>
        </div>

    </div>
</section>

<!-- حقائق عن الفضاء -->
<section class="facts">
    <h2>حقائق مدهشة عن الفضاء</h2>
    <p class="description">معلومات ممتعة عن الكون من حولنا.</p>

    <div class="facts-grid">
        <div class="fact">
            <h3>☀️ الشمس</h3>
            <p>نجم يقع في مركز المجموعة الشمسية، وتدور الكواكب حوله.</p>
        </div>

        <div class="fact">
            <h3>🌌 المجرات</h3>
            <p>درب التبانة هي المجرة التي توجد فيها مجموعتنا الشمسية.</p>
        </div>

        <div class="fact">
            <h3>🌙 القمر</h3>
            <p>القمر هو التابع الطبيعي للأرض، ونرى أطواره المختلفة خلال الشهر.</p>
        </div>

        <div class="fact">
            <h3>🛰️ الأقمار الصناعية</h3>
            <p>تساعد الأقمار الصناعية في الاتصالات ومراقبة الطقس ودراسة الأرض.</p>
        </div>

        <div class="fact">
            <h3>🚀 استكشاف الفضاء</h3>
            <p>تتيح المركبات الفضائية لرواد الفضاء إجراء التجارب خارج الأرض.</p>
        </div>

        <div class="fact">
            <h3>🔭 التلسكوبات</h3>
            <p>تساعد العلماء على رصد الأجرام البعيدة ودراسة المجرات.</p>
        </div>
    </div>
</section>

<!-- الأمير سلطان بن سلمان -->
<section class="sultan" id="sultan">
    <h2>أول رائد فضاء سعودي</h2>
    <p class="description">
        إنجاز سعودي بارز في تاريخ استكشاف الفضاء.
    </p>

    <div class="sultan-card">

        <img
            class="sultan-photo"
            src="https://images-assets.nasa.gov/image/51g-04-010/51g-04-010~orig.jpg"
            alt="الأمير سلطان بن سلمان خلال رحلته الفضائية"
            onerror="this.onerror=null;this.src='https://images-assets.nasa.gov/image/51g-21-011/51g-21-011~orig.jpg';"
        >

        <h3>الأمير سلطان بن سلمان بن عبدالعزيز آل سعود</h3>

        <p>
            يُعد الأمير سلطان بن سلمان أول رائد فضاء سعودي،
            وأول عربي ومسلم يصل إلى الفضاء.
        </p>

        <p>
            شارك في رحلة مكوك الفضاء الأمريكي ديسكفري
            ضمن مهمة STS-51-G عام 1985م بصفته أخصائي حمولة.
        </p>

        <p>
            مثّل المملكة العربية السعودية في هذه الرحلة التاريخية،
            وأصبح إنجازه مصدر إلهام للمهتمين بالعلوم والفضاء.
        </p>

    </div>
</section>

<!-- معلومات عن النجوم تحت قسم سلطان -->
<section class="stars" id="stars">
    <h2>أسرار النجوم ✨</h2>
    <p class="description">
        النجوم ليست مجرد نقاط مضيئة في السماء؛ إنها عوالم هائلة تحمل الكثير من الأسرار.
    </p>

    <div class="star-grid">

        <div class="star-card">
            <div class="star-icon">✦</div>
            <h3>ما النجوم؟</h3>
            <p>
                النجوم كرات ضخمة من الغاز الساخن، تتكون أساسًا من الهيدروجين
                والهيليوم، وتنتج الطاقة والضوء من خلال الاندماج النووي في داخلها.
            </p>
        </div>

        <div class="star-card">
            <div class="star-icon">☀</div>
            <h3>الشمس نجم</h3>
            <p>
                الشمس أقرب نجم إلى الأرض، وهي مصدر الضوء والحرارة الأساسي
                لكوكبنا، وتساعد طاقتها على استمرار الحياة.
            </p>
        </div>

        <div class="star-card">
            <div class="star-icon">✧</div>
            <h3>ألوان النجوم</h3>
            <p>
                قد تبدو النجوم حمراء أو برتقالية أو صفراء أو بيضاء أو زرقاء.
                ويعطي لون النجم العلماء معلومات عن درجة حرارة سطحه.
            </p>
        </div>

        <div class="star-card">
            <div class="star-icon">✴</div>
            <h3>ولادة النجوم</h3>
            <p>
                تتكوّن النجوم داخل سحب ضخمة من الغاز والغبار تُسمى السدم،
                عندما تتجمع المادة بفعل الجاذبية وتزداد حرارتها.
            </p>
        </div>

        <div class="star-card">
            <div class="star-icon">🌌</div>
            <h3>مجموعات النجوم</h3>
            <p>
                تربط الثقافات بين بعض النجوم في السماء لتكوين أشكال تُعرف
                بالكوكبات، وتُستخدم للتعرّف على مناطق السماء.
            </p>
        </div>

        <div class="star-card">
            <div class="star-icon">💫</div>
            <h3>نهاية حياة النجوم</h3>
            <p>
                تختلف نهاية النجم حسب كتلته؛ فقد يتحول إلى قزم أبيض،
                أو ينفجر في مستعر أعظم، وقد يترك وراءه نجمًا نيوترونيًا
                أو ثقبًا أسود.
            </p>
        </div>

    </div>
</section>

</body>
</html>
<!-- قسم فيديو COSMOS -->
<section id="cosmos-video" dir="rtl">
  <style>
    #cosmos-video {
      padding: 45px 20px;
      margin: 30px auto;
      max-width: 1000px;
      text-align: center;
      color: white;
      font-family: Tahoma, Arial, sans-serif;
      background: linear-gradient(145deg, #080e27, #111c3d);
      border: 1px solid #315a83;
      border-radius: 24px;
      box-shadow: 0 0 35px #00d9ff12;
    }

    #cosmos-video .video-label {
      color: #59eaff;
      letter-spacing: 3px;
      font-size: 12px;
    }

    #cosmos-video h2 {
      font-size: clamp(25px, 4vw, 38px);
      margin: 18px 0 12px;
    }

    #cosmos-video p {
      color: #bac9e7;
      line-height: 1.9;
      margin-bottom: 25px;
    }

    #cosmos-video .video-frame {
      position: relative;
      width: 100%;
      aspect-ratio: 16 / 9;
      overflow: hidden;
      border-radius: 18px;
      border: 1px solid #5cecff66;
      box-shadow: 0 0 28px #24dfff18;
    }

    #cosmos-video iframe {
      position: absolute;
      inset: 0;
      width: 100%;
      height: 100%;
      border: 0;
    }

    #cosmos-video .video-link {
      display: inline-block;
      margin-top: 22px;
      padding: 13px 24px;
      color: #061322;
      background: #59eaff;
      border-radius: 12px;
      text-decoration: none;
      font-weight: bold;
    }
  </style>

  <div class="video-label">COSMOS • SPACE VIDEO</div>

  <h2>🎬 نافذتك إلى الفضاء</h2>

  <p>
    شاهدي هذا المقطع وتعرّفي على عالم الكواكب القزمة
    وأسرار الفضاء.
  </p>

  <div class="video-frame">
    <iframe
      src="https://www.youtube-nocookie.com/embed/Er5L6cxnRTc"
      title="مقطع فضائي من يوتيوب"
      loading="lazy"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      referrerpolicy="strict-origin-when-cross-origin"
      allowfullscreen>
    </iframe>
  </div>

  <a
    class="video-link"
    href="https://youtu.be/Er5L6cxnRTc"
    target="_blank"
    rel="noopener noreferrer">
    ▶ مشاهدة على يوتيوب
  </a>
</section>
<!-- ===== COSMOS: المسابقة الفضائية ===== -->
<section id="cosmos-contest" dir="rtl">
<style>
#cosmos-contest {
  font-family: Tahoma, Arial, sans-serif;
  color: #fff;
  max-width: 1000px;
  margin: 35px auto;
  padding: 35px 18px;
  border: 1px solid #315a83;
  border-radius: 25px;
  background:
    radial-gradient(ellipse at top left,#203b73,transparent 50%),
    linear-gradient(145deg,#060b1b,#101a36,#160f2c);
  box-shadow: 0 0 40px #24dfff12;
}
#cosmos-contest * { box-sizing: border-box; }
#cosmos-contest .cc-heading { text-align:center; margin-bottom:28px; }
#cosmos-contest .cc-label {
  color:#59eaff; font-size:12px; letter-spacing:3px;
}
#cosmos-contest h2 {
  font-size:clamp(27px,5vw,42px); margin:17px 0 12px;
}
#cosmos-contest .cc-muted { color:#bac8e4; line-height:2; }
#cosmos-contest .cc-card {
  max-width:650px; margin:auto; padding:24px;
  border:1px solid #7be9ff35; border-radius:19px;
  background:#ffffff08;
}
#cosmos-contest .cc-field { margin:18px 0; text-align:right; }
#cosmos-contest .cc-field label {
  display:block; margin-bottom:9px; font-size:14px;
}
#cosmos-contest input, #cosmos-contest select {
  width:100%; padding:14px; border-radius:11px;
  background:#0c1730; border:1px solid #42577e;
  color:#fff; font-family:inherit; font-size:15px;
}
#cosmos-contest input::placeholder { color:#8497b8; }
#cosmos-contest input:focus, #cosmos-contest select:focus {
  outline:2px solid #59eaff; outline-offset:2px;
}
#cosmos-contest .cc-btn {
  width:100%; padding:15px; margin-top:12px;
  border:0; border-radius:11px;
  background:linear-gradient(100deg,#59eaff,#a99aff);
  color:#071222; font-family:inherit;
  font-size:16px; font-weight:bold; cursor:pointer;
}
#cosmos-contest .cc-btn:hover { filter:brightness(1.08); }
#cosmos-contest .cc-error {
  color:#ffb5c2; font-size:13px; line-height:1.8;
}
#cosmos-contest .cc-hidden { display:none !important; }
#cosmos-contest .cc-top {
  display:flex; justify-content:space-between;
  gap:12px; color:#b9c9e8; font-size:13px;
  margin-bottom:15px;
}
#cosmos-contest .cc-progress {
  height:6px; background:#24304d; border-radius:20px;
  overflow:hidden; margin-bottom:25px;
}
#cosmos-contest .cc-fill {
  height:100%; width:0;
  background:linear-gradient(90deg,#59eaff,#a99aff);
  transition:width .3s;
}
#cosmos-contest .cc-question {
  font-size:21px; line-height:1.8; margin:0 0 20px;
}
#cosmos-contest .cc-answers { display:grid; gap:11px; }
#cosmos-contest .cc-answer {
  width:100%; text-align:right; padding:14px;
  border:1px solid #42557c; border-radius:11px;
  background:#101d39; color:#e7efff;
  font-family:inherit; font-size:15px; cursor:pointer;
}
#cosmos-contest .cc-answer:hover:not(:disabled) {
  border-color:#59eaff; background:#17314b;
}
#cosmos-contest .cc-answer:disabled { cursor:default; }
#cosmos-contest .cc-answer.cc-correct {
  border-color:#53f2b0; background:#123b38; color:#8affcb;
}
#cosmos-contest .cc-answer.cc-wrong {
  border-color:#ff8199; background:#421d35; color:#ffb0bd;
}
#cosmos-contest .cc-feedback {
  min-height:28px; line-height:1.9; color:#c3d1ed;
  font-size:14px; margin:16px 0 5px;
}
#cosmos-contest .cc-result { text-align:center; }
#cosmos-contest .cc-score {
  color:#59eaff; font-size:44px; font-weight:bold; margin:18px;
}
#cosmos-contest .cc-result p { color:#c3d1ed; line-height:2; }
#cosmos-contest .cc-small {
  color:#8498bb; font-size:12px; line-height:1.9;
  text-align:center; margin-top:20px;
}
@media(max-width:500px) {
  #cosmos-contest { padding:28px 13px; }
  #cosmos-contest .cc-card { padding:17px; }
  #cosmos-contest .cc-question { font-size:18px; }
}
</style>

<div class="cc-heading">
  <div class="cc-label">C O S M O S · SPACE CHALLENGE</div>
  <h2>🚀 تحدّي COSMOS الفضائي</h2>
  <p class="cc-muted">
    أهلًا بكِ في تحدّي الكون!<br>
    سجّلي بياناتك وجرّبي معلوماتك عن الفضاء.
    خمس أسئلة، ومهمة جديدة تنتظركِ ✨
  </p>
</div>

<!-- التسجيل -->
<div class="cc-card" id="cc-register">
  <h3>👩‍🚀 قبل الانطلاق...</h3>
  <p class="cc-muted">
    خلينا نتعرّف عليكِ أولًا.
    اكتبي اسمك واختاري صفك، وإذا كنتِ معلمة اختاري «معلمة».
  </p>

  <form id="cc-form">
    <div class="cc-field">
      <label for="cc-name">الاسم</label>
      <input id="cc-name" type="text" maxlength="50"
        placeholder="اكتبي اسمك هنا" autocomplete="name" required>
    </div>

    <div class="cc-field">
      <label for="cc-class">الصف أو الفئة</label>
      <select id="cc-class" required>
        <option value="">اختاري صفك</option>
        <option>أول متوسط 1</option>
        <option>أول متوسط 2</option>
        <option>ثاني متوسط 1</option>
        <option>ثاني متوسط 2</option>
        <option>ثالث متوسط 1</option>
        <option>ثالث متوسط 2</option>
        <option>أول ثانوي 1</option>
        <option>أول ثانوي 2</option>
        <option>ثاني ثانوي 1</option>
        <option>ثاني ثانوي 2</option>
        <option>ثالث ثانوي 1</option>
        <option>ثالث ثانوي 2</option>
        <option value="معلمة">معلمة 👩‍🏫</option>
      </select>
    </div>

    <p id="cc-error" class="cc-error" aria-live="polite"></p>
    <button class="cc-btn" type="submit">ابدئي التحدّي ✦</button>
  </form>
</div>

<!-- الأسئلة -->
<div class="cc-card cc-hidden" id="cc-game">
  <div class="cc-top">
    <span id="cc-progress-text">السؤال 1 من 5</span>
    <span>⭐ النقاط: <b id="cc-score">0</b></span>
  </div>

  <div class="cc-progress">
    <div class="cc-fill" id="cc-fill"></div>
  </div>

  <h3 class="cc-question" id="cc-question"></h3>
  <div class="cc-answers" id="cc-answers"></div>
  <p class="cc-feedback" id="cc-feedback" aria-live="polite"></p>

  <button class="cc-btn cc-hidden" id="cc-next" type="button">
    السؤال التالي ←
  </button>
</div>

<!-- النتيجة -->
<div class="cc-card cc-result cc-hidden" id="cc-result" aria-live="polite">
  <div style="font-size:60px" id="cc-trophy">🏆</div>
  <h3 id="cc-result-title">انتهت المهمة!</h3>
  <p id="cc-greeting"></p>
  <div class="cc-score" id="cc-final-score">0 / 5</div>
  <p id="cc-result-message"></p>
  <button class="cc-btn" id="cc-retry" type="button">
    ↻ أعيدي المسابقة
  </button>
  <button class="cc-btn" id="cc-new-person" type="button"
    style="background:#182746;color:#dcecff;border:1px solid #42577e">
    مشاركة جديدة
  </button>
</div>

<p class="cc-small">
  COSMOS · لكل سؤال معلومة جديدة، ولكل محاولة فرصة للتعلّم 🪐
</p>

<script>
(() => {
  const root = document.getElementById("cosmos-contest");
  if (!root || root.dataset.ready === "yes") return;
  root.dataset.ready = "yes";

  const $ = id => root.querySelector("#" + id);

  const questions = [
    {
      q: "ما أقرب نجم إلى الأرض؟",
      a: ["الشمس", "الشعرى اليمانية", "نجم القطب"],
      correct: 0,
      info: "الشمس أقرب نجم إلى الأرض، وهي مصدر الضوء والحرارة لكوكبنا."
    },
    {
      q: "ما أكبر كوكب في مجموعتنا الشمسية؟",
      a: ["الأرض", "المشتري", "المريخ"],
      correct: 1,
      info: "المشتري هو أكبر كواكب مجموعتنا الشمسية."
    },
    {
      q: "ما اسم المجرة التي نعيش فيها؟",
      a: ["درب التبانة", "المرأة المسلسلة", "مجرة سومبريرو"],
      correct: 0,
      info: "تقع مجموعتنا الشمسية في مجرة درب التبانة."
    },
    {
      q: "من أول رائد فضاء عربي ومسلم؟",
      a: ["الأمير سلطان بن سلمان", "يوري غاغارين", "نيل أرمسترونغ"],
      correct: 0,
      info: "شارك الأمير سلطان بن سلمان في رحلة مكوك الفضاء ديسكفري عام 1985."
    },
    {
      q: "أي كوكب يُعرف بالكوكب الأحمر؟",
      a: ["الزهرة", "أورانوس", "المريخ"],
      correct: 2,
      info: "يعود اللون الأحمر للمريخ إلى أكاسيد الحديد الموجودة في غباره وسطحه."
    }
  ];

  let name = "";
  let category = "";
  let index = 0;
  let score = 0;
  let locked = false;

  $("cc-form").addEventListener("submit", event => {
    event.preventDefault();

    const enteredName = $("cc-name").value.trim();
    const selectedClass = $("cc-class").value;

    if (!enteredName || !selectedClass) {
      $("cc-error").textContent = "تأكدي من كتابة اسمك واختيار صفك أو فئتك.";
      return;
    }

    name = enteredName;
    category = selectedClass;
    index = 0;
    score = 0;

    $("cc-error").textContent = "";
    $("cc-register").classList.add("cc-hidden");
    $("cc-result").classList.add("cc-hidden");
    $("cc-game").classList.remove("cc-hidden");

    showQuestion();
  });

  function showQuestion() {
    locked = false;
    const item = questions[index];

    $("cc-progress-text").textContent =
      "السؤال " + (index + 1) + " من " + questions.length;
    $("cc-score").textContent = score;
    $("cc-question").textContent = item.q;
    $("cc-feedback").textContent = "";
    $("cc-feedback").style.color = "#c3d1ed";
    $("cc-fill").style.width =
      (index / questions.length * 100) + "%";
    $("cc-next").classList.add("cc-hidden");

    const answers = $("cc-answers");
    answers.replaceChildren();

    item.a.forEach((answer, i) => {
      const button = document.createElement("button");
      button.type = "button";
      button.className = "cc-answer";
      button.textContent = answer;

      button.addEventListener("click", () => {
        if (locked) return;
        locked = true;

        const allButtons = answers.querySelectorAll("button");
        allButtons.forEach((b, j) => {
          b.disabled = true;
          if (j === item.correct) b.classList.add("cc-correct");
        });

        if (i === item.correct) {
          score++;
          $("cc-score").textContent = score;
          $("cc-feedback").textContent = "إجابة صحيحة! ✨ " + item.info;
          $("cc-feedback").style.color = "#7dffd0";
        } else {
          button.classList.add("cc-wrong");
          $("cc-feedback").textContent =
            "مو مشكلة، نتعلم مع كل محاولة! " +
            "الإجابة الصحيحة: " + item.a[item.correct] + ". " + item.info;
          $("cc-feedback").style.color = "#ffb5c2";
        }

        $("cc-fill").style.width =
          ((index + 1) / questions.length * 100) + "%";

        $("cc-next").textContent =
          index === questions.length - 1
            ? "شوفي نتيجتك ✦"
            : "السؤال التالي ←";

        $("cc-next").classList.remove("cc-hidden");
      });

      answers.appendChild(button);
    });
  }

  $("cc-next").addEventListener("click", () => {
    if (!locked) return;

    index++;
    if (index < questions.length) {
      showQuestion();
    } else {
      showResult();
    }
  });

  function showResult() {
    $("cc-game").classList.add("cc-hidden");
    $("cc-result").classList.remove("cc-hidden");

    $("cc-greeting").textContent =
      "أحسنتِ يا " + name + "! · " + category;

    $("cc-final-score").textContent = score + " / " + questions.length;

    if (score === 5) {
      $("cc-trophy").textContent = "🏆";
      $("cc-result-title").textContent = "يا سلام! مستكشفة متميزة";
      $("cc-result-message").textContent =
        "ما شاء الله، كل إجاباتك صحيحة! عندك معلومات رائعة عن الفضاء.";
    } else if (score >= 3) {
      $("cc-trophy").textContent = "🚀";
      $("cc-result-title").textContent = "إنجاز جميل!";
      $("cc-result-message").textContent =
        "أبدعتِ! جاوبتِ عن أغلب الأسئلة صح، وباقي لك معلومات بسيطة تكتشفينها.";
    } else {
      $("cc-trophy").textContent = "🌟";
      $("cc-result-title").textContent = "بداية موفقة!";
      $("cc-result-message").textContent =
        "شكرًا لمشاركتك! كل سؤال فرصة للتعلّم، جرّبي مرة ثانية وشوفي كيف تتطور نتيجتك.";
    }
  }

  $("cc-retry").addEventListener("click", () => {
    index = 0;
    score = 0;
    $("cc-result").classList.add("cc-hidden");
    $("cc-game").classList.remove("cc-hidden");
    showQuestion();
  });

  $("cc-new-person").addEventListener("click", () => {
    $("cc-result").classList.add("cc-hidden");
    $("cc-register").classList.remove("cc-hidden");
    $("cc-name").value = "";
    $("cc-class").value = "";
    $("cc-error").textContent = "";
  });
})();
</script>
</section>
<!-- ===== نهاية مسابقة COSMOS ===== --><section style="background:#080e24;color:white;padding:25px;text-align:center;border-radius:18px;font-family:Tahoma">
<h2 style="color:#54efad">🚀 تحدي عباقرة COSMOS</h2>
<h3>48 ساعة تفصل بينك وبين لقب العبقرية! 🪐</h3>
<p>مو كل شخص يقدر يحل اللغز.. هل أنتِ منهم؟</p>
<h3 style="color:#54efad">🧠 السؤال الفضائي</h3>
<p>لماذا لا تتمدد الذرات مع تمدد الكون، بينما تزداد المسافات بين المجرات البعيدة؟</p>
<select id="c">
<option>أول متوسط 1</option><option>أول متوسط 2</option>
<option>ثاني متوسط 1</option><option>ثاني متوسط 2</option>
<option>ثالث متوسط 1</option><option>ثالث متوسط 2</option>
<option>أول ثانوي 1</option><option>أول ثانوي 2</option>
<option>ثاني ثانوي 1</option><option>ثاني ثانوي 2</option>
<option>ثالث ثانوي 1</option><option>ثالث ثانوي 2</option>
</select><br><br>
<input id="n" placeholder="اسم الطالبة"><br><br>
<textarea id="a" placeholder="اكتبي إجابتك بثقة"></textarea><br><br>
<button onclick="send()">أثبت أنني أستطيع! ✨</button>
<p id="m"></p>
<hr>
<h3 style="color:#54efad">✨ تذكري دائمًا</h3>
<p>كل اكتشاف عظيم بدأ بسؤال!</p>
<p>لا تبحثي عن الإجابة فقط، بل افهمي السبب وراءها.</p>
<p>قد تكون فكرتك اليوم بداية اكتشاف يغيّر المستقبل. 🚀</p>
<h2 style="color:#54efad">هل أنتِ مستعدة لصناعة الفرق؟</h2>
</section>
<script>
function send(){
let n=document.getElementById('n').value.trim();
let a=document.getElementById('a').value.trim();
if(!n||!a)return alert("اكتبي اسمك وإجابتك أولًا!");
document.getElementById('m').innerHTML=
"🌟 أحسنتِ يا "+n+"! تم تسجيل إجابتك في هذه الصفحة.";
}
</script>
<section id="cosmos-message" dir="rtl">
  <style>
    #cosmos-message {
      background: linear-gradient(135deg, #050b20, #101d3d, #071426);
      color: #f0f6ff;
      text-align: center;
      padding: 65px 20px;
      font-family: Tahoma, Arial, sans-serif;
      border-radius: 22px;
      margin: 25px 0;
      overflow: hidden;
    }

    #cosmos-message .space-icon {
      font-size: 55px;
      margin-bottom: 15px;
      animation: floatCosmos 3s ease-in-out infinite;
    }

    #cosmos-message h2 {
      color: #65e8ff;
      font-size: 30px;
      margin-bottom: 25px;
    }

    #cosmos-message .message-text {
      max-width: 720px;
      margin: auto;
      font-size: 17px;
      line-height: 2.2;
      color: #e0eaff;
    }

    #cosmos-message .quote {
      color: #8fffe0;
      font-size: 19px;
      margin: 28px auto;
      font-weight: bold;
    }

    #cosmos-message .credits {
      border-top: 1px solid #385477;
      margin: 35px auto 0;
      padding-top: 25px;
      max-width: 450px;
      line-height: 2.2;
      color: #c7d9f5;
    }

    #cosmos-message .credits strong {
      color: #65e8ff;
    }

    #cosmos-message .stars {
      letter-spacing: 12px;
      color: #8fffe0;
      margin-top: 25px;
    }

    @keyframes floatCosmos {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }
  </style>

  <div class="space-icon">🌌</div>

  <h2>رسالة أخيرة من COSMOS</h2>

  <div class="message-text">
    <p>
      وصلنا إلى نهاية رحلتنا في عالم الفضاء،
      لكن حكاية هذا الكون ما تنتهي هنا!
    </p>

    <p>
      من النجوم اللي تضيء السماء، إلى الكواكب
      والمجرات البعيدة، ما زال الفضاء مليئًا
      بأسرار تنتظر من يكتشفها.
    </p>

    <p>
      أتمنى أن تكون رحلتكم مع COSMOS ممتعة،
      وأنكم تعلمتم معلومات جديدة خلتكم تنظرون
      للسماء بفضول أكبر، وتفكرون في الأشياء
      المذهلة الموجودة خارج عالمنا.
    </p>

    <p>
      يمكن سؤال صغير اليوم يكون بداية اكتشاف
      كبير في المستقبل؛ لذلك استمروا في التعلم
      والبحث، ولا تتوقفون عن طرح الأسئلة. 🚀
    </p>
  </div>

  <div class="quote">
    «انتهت رحلتنا هنا، لكن اكتشافاتكم تبدأ الآن.»
  </div>

  <div class="credits">
    <p>إعداد الطالبة: <strong>إيلان الظاهري</strong></p>
    <p>المعلمة: <strong>عائشة المطيري</strong></p>
    <p>شكرًا لكم على رحلتكم مع COSMOS 💙</p>
  </div>

  <div class="stars">✦ ✧ ★ ✧ ✦</div>
</section>
