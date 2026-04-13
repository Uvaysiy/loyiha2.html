<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Minecraft World | Ortiqjon Xasanov</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', 'Minecraft', 'Courier New', monospace;
            background: #0d1f0a;
            background-image: 
                linear-gradient(45deg, #1a3a12 1px, transparent 1px),
                linear-gradient(-45deg, #1a3a12 1px, transparent 1px);
            background-size: 40px 40px;
            color: #e8f0e0;
            line-height: 1.5;
        }

        /* Blokli Minecraft uslubi */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 15px 20px;
        }

        /* Sarlavha qismi - blokli dizayn */
        header {
            background: #2b2b2b;
            border-bottom: 6px solid #6b8c42;
            box-shadow: 0 8px 0 #1a2a0f;
            margin-bottom: 20px;
        }

        .header-flex {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 15px;
        }

        .logo h1 {
            font-size: 2rem;
            color: #a0e060;
            text-shadow: 3px 3px 0 #2d5a1a;
            letter-spacing: 2px;
        }

        .logo p {
            color: #b8d9a6;
            font-size: 0.85rem;
        }

        .user-card {
            background: #1f2a1a;
            padding: 10px 25px;
            border-radius: 0;
            border-left: 5px solid #f5b042;
            border-right: 5px solid #f5b042;
            border-top: 2px solid #8aac6b;
            border-bottom: 2px solid #8aac6b;
            font-weight: bold;
            font-size: 1.2rem;
            font-family: monospace;
            box-shadow: 0 3px 0 #3a4a2a;
        }

        .user-card span {
            color: #ffcc66;
        }

        /* Navigatsiya - Minecraft tugmalari */
        nav {
            background: #1f2a18;
            margin-top: 15px;
            padding: 10px 0;
            border-top: 3px solid #6b8c42;
            border-bottom: 3px solid #6b8c42;
        }

        nav ul {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            list-style: none;
            gap: 8px;
        }

        nav ul li a {
            display: inline-block;
            background: #2c3e23;
            color: #f0f0d0;
            text-decoration: none;
            padding: 8px 20px;
            font-weight: bold;
            font-family: monospace;
            border: 2px solid #6e944d;
            transition: 0.1s linear;
            box-shadow: 0 3px 0 #1a2a0f;
        }

        nav ul li a:hover {
            background: #4a7040;
            transform: translateY(-2px);
            box-shadow: 0 5px 0 #1a2a0f;
        }

        /* Bo'limlar */
        .section {
            background: #1f2a1aa0;
            backdrop-filter: blur(2px);
            margin: 40px 0;
            padding: 10px 0;
        }

        .section-title {
            font-size: 1.8rem;
            background: #2a3a20;
            display: inline-block;
            padding: 8px 25px;
            margin-bottom: 25px;
            border-left: 12px solid #f5b042;
            border-right: 4px solid #6b8c42;
            font-family: monospace;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Grid kartochkalar */
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 25px;
        }

        .minecraft-card {
            background: #262f1f;
            border: 3px solid #5f7e42;
            box-shadow: 5px 5px 0 #0f1a0a;
            transition: all 0.2s;
        }

        .minecraft-card:hover {
            transform: translate(-2px, -2px);
            box-shadow: 8px 8px 0 #0f1a0a;
            border-color: #e5b83c;
        }

        .card-img {
            height: 140px;
            background-color: #3a552a;
            background-size: cover;
            background-position: center;
            border-bottom: 3px solid #7faa5a;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
        }

        .card-content {
            padding: 18px;
        }

        .card-content h3 {
            color: #ffdd99;
            margin-bottom: 8px;
            font-size: 1.3rem;
        }

        .card-content p {
            color: #cce0bb;
            font-size: 0.9rem;
        }

        .tag {
            display: inline-block;
            background: #4a3920;
            padding: 3px 10px;
            margin-top: 12px;
            font-size: 0.7rem;
            font-family: monospace;
            border-left: 3px solid #ffaa33;
        }

        /* Seed ro'yxati maxsus */
        .seed-box {
            background: #1e2a16;
            border: 3px solid #5a7940;
            padding: 20px;
        }

        .seed-list {
            list-style: none;
        }

        .seed-list li {
            background: #2c3b22;
            margin: 12px 0;
            padding: 12px 15px;
            font-family: 'Courier New', monospace;
            border-left: 8px solid #ffaa44;
            word-break: break-all;
        }

        .seed-code {
            font-weight: bold;
            color: #ffcc88;
            background: #0f1a0c;
            padding: 3px 8px;
            display: inline-block;
        }

        footer {
            background: #111d0e;
            text-align: center;
            padding: 20px;
            margin-top: 50px;
            border-top: 6px solid #5f7e42;
            font-size: 0.8rem;
        }

        button, .mc-button {
            background: #4a6e32;
            border: none;
            color: white;
            padding: 5px 12px;
            font-family: monospace;
        }

        @media (max-width: 650px) {
            .header-flex {
                flex-direction: column;
                text-align: center;
            }
            .section-title {
                font-size: 1.4rem;
            }
            .card-img {
                height: 100px;
            }
        }
    </style>
</head>
<body>

<header>
    <div class="container header-flex">
        <div class="logo">
            <h1>⛏️ MC.UZ | CRAFT WORLD</h1>
            <p>Bloklar saltanati — o‘zbek tilidagi eng to‘liq portal</p>
        </div>
        <div class="user-card">
            🧑‍💻 <span>Ortiqjon Xasanov</span>
        </div>
    </div>
    <div class="container">
        <nav>
            <ul>
                <li><a href="#">🏠 BOSH</a></li>
                <li><a href="#">🎨 SKINLAR</a></li>
                <li><a href="#">🧩 MODLAR</a></li>
                <li><a href="#">🌾 SEEDLAR</a></li>
                <li><a href="#">📘 MASLAHATLAR</a></li>
                <li><a href="#">🆕 1.21 YANGILIK</a></li>
            </ul>
        </nav>
    </div>
</header>

<main class="container">
    
    <!-- SKINLAR bo'limi -->
    <div class="section">
        <h2 class="section-title">🎨 MASHHUR SKINLAR</h2>
        <div class="grid">
            <div class="minecraft-card">
                <div class="card-img">⚔️🧑</div>
                <div class="card-content">
                    <h3>Qora qilichboz</h3>
                    <p>Qora zirh + qip-qizil ko'zlar. PvP serverlar uchun ajoyib tanlov.</p>
                    <span class="tag">📥 15k+ yuklangan</span>
                </div>
            </div>
            <div class="minecraft-card">
                <div class="card-img">🧝‍♀️🍃</div>
                <div class="card-content">
                    <h3>O‘rmon elfi</h3>
                    <p>Yashil va oltin tuslardagi nozik skin. Builderlar orasida mashhur.</p>
                    <span class="tag">✨ Yangi</span>
                </div>
            </div>
            <div class="minecraft-card">
                <div class="card-img">🐉🔥</div>
                <div class="card-content">
                    <h3>Ajdar qo'riqchisi</h3>
                    <p>Qanotli dubulg'a, olmos naqshlari. Epic skin!</p>
                    <span class="tag">Legendary</span>
                </div>
            </div>
            <div class="minecraft-card">
                <div class="card-img">🤖⚡</div>
                <div class="card-content">
                    <h3>Kiber-2025</h3>
                    <p>Futuristik neon skin, tungi serverlarda porlaydi.</p>
                    <span class="tag">Premium</span>
                </div>
            </div>
        </div>
    </div>

    <!-- MODLAR bo'limi -->
    <div class="section">
        <h2 class="section-title">🧩 ENG YAXSHI MODLAR</h2>
        <div class="grid">
            <div class="minecraft-card">
                <div class="card-content">
                    <h3>🔧 Create Mod</h3>
                    <p>Mexanizmlar, konveyerlar, aylanuvchi qismlar — avtomatika olami.</p>
                    <span class="tag">Forge 1.20.1</span>
                </div>
            </div>
            <div class="minecraft-card">
                <div class="card-content">
                    <h3>🧙 Ars Nouveau</h3>
                    <p>Sehrgarlik, o'z sehrlaringizni yozish va murakkab spellar.</p>
                    <span class="tag">Mana tizimi</span>
                </div>
            </div>
            <div class="minecraft-card">
                <div class="card-content">
                    <h3>🗺️ JourneyMap</h3>
                    <p>Real vaqtda xarita, bo'limlarni belgilash va kuzatish.</p>
                    <span class="tag">Majburiy</span>
                </div>
            </div>
            <div class="minecraft-card">
                <div class="card-content">
                    <h3>🐉 Ice and Fire</h3>
                    <p>Haqiqiy ajdarlar, gifonlar va mifologik maxluqlar.</p>
                    <span class="tag">Epik janglar</span>
                </div>
            </div>
        </div>
    </div>

    <!-- SEEDLAR bo'limi -->
    <div class="section">
        <h2 class="section-title">🌱 NOYOB SEEDLAR (Java 1.20+ / 1.21)</h2>
        <div class="seed-box">
            <ul class="seed-list">
                <li><span class="seed-code">🌲 -8400280189225650786</span> — Keng qayin o'rmoni, yonida katta qishloq va omborxona.</li>
                <li><span class="seed-code">🏰 808080808</span> — Spawn nuqtasidan 150 blok uzoqlikda qal'a (stronghold) va portal.</li>
                <li><span class="seed-code">💎 9876543210</span> — Y=-54 da katta olmas tomirlari, ulanishli g'orlar tarmog'i.</li>
                <li><span class="seed-code">🏝️ -672410349</span> — 8 ta orol, markazda mangrov biomi va yashirin sandiqlar.</li>
                <li><span class="seed-code">❄️ 1.21_trial</span> — Trial Chambers spawn ostida, Breeze mavjudoti yaqin.</li>
            </ul>
        </div>
    </div>

    <!-- FOYDALI MASLAHATLAR bo'limi -->
    <div class="section">
        <h2 class="section-title">📘 MINECRAFT FOYDALI MASLAHATLAR</h2>
        <div class="grid">
            <div class="minecraft-card">
                <div class="card-content">
                    <h3>💎 Olmos qazish sirlari</h3>
                    <p>Y=-59 eng optimal qavat. Strip mining (2x1 yo'lak) usuli eng samarali. Fortune 3 bilan 2-3 barobar ko'p olmos olasiz.</p>
                </div>
            </div>
            <div class="minecraft-card">
                <div class="card-content">
                    <h3>⚡ Nether transport</h3>
                    <p>Netherda 1 blok = Overworldda 8 blok. Portallarni to'g'ri hisoblab, tez sayohat qiling.</p>
                </div>
            </div>
            <div class="minecraft-card">
                <div class="card-content">
                    <h3>🛡️ Villager savdolari</h3>
                    <p>Zombie - villagerni davolab, 1 zumradga mending kitob olish mumkin. Eng kuchli buyumlar shunday olinadi.</p>
                </div>
            </div>
            <div class="minecraft-card">
                <div class="card-content">
                    <h3>🐉 Ender Dragon uchun tayyorgarlik</h3>
                    <p>Olmos zirh + Feather Falling etik, slow falling iksiri, o'q va qum bloklari (kristallarni buzish uchun).</p>
                </div>
            </div>
            <div class="minecraft-card">
                <div class="card-content">
                    <h3>🔮 Enchanting maksimal</h3>
                    <p>15 ta kitob javonini 2 blok masofada joylashtiring. Eng yaxshi sehrlar 30 lvl ochiladi.</p>
                </div>
            </div>
        </div>
    </div>

    <!-- YANGILANISHLAR 1.21 (TRIAL & TALES) -->
    <div class="section">
        <h2 class="section-title">🆕 MINECRAFT 1.21 YANGILIKLARI</h2>
        <div class="grid">
            <div class="minecraft-card">
                <div class="card-content">
                    <h3>🏛️ Trial Chambers</h3>
                    <p>Yangi yer osti inshootlari. Trial Spawner orqali to'lqinli janglar. Mukofot: mace quroli va breeze tuxumlari.</p>
                    <span class="tag">Yangi struktura</span>
                </div>
            </div>
            <div class="minecraft-card">
                <div class="card-content">
                    <h3>💨 Breeze mavjudoti</h3>
                    <p>Uchuvchi, shamol hujumlari bilan otadi. Undan breeze rod tushadi — mace yasash uchun kerak.</p>
                    <span class="tag">Hostile mob</span>
                </div>
            </div>
            <div class="minecraft-card">
                <div class="card-content">
                    <h3>🔨 Mace quroli</h3>
                    <p>Balandlikdan tushganda qancha baland bo'lsa, shuncha katta zarar. Yiqilishdan o'zingiz himoyalanmagan bo'lsangiz ishlaydi.</p>
                    <span class="tag">Yangi qurol</span>
                </div>
            </div>
            <div class="minecraft-card">
                <div class="card-content">
                    <h3>🎨 Armor trim + yangi naqshlar</h3>
                    <p>7 xil yangi bezak (Flow, Bolt, Guster). Netherite yangilash crafting stolida o'zgartirildi.</p>
                    <span class="tag">1.21</span>
                </div>
            </div>
        </div>
        <div style="background: #1e2e16; padding: 15px; margin-top: 20px; border-left: 6px solid gold;">
            <p>⭐ <strong>Eslatma:</strong> 1.21 versiyasida "Trial Chambers" Y= -40 dan -20 gacha paydo bo'ladi. Yangi "crafter" bloki sizga avtomatik craft qilish imkonini beradi.</p>
        </div>
    </div>

    <!-- Qo'shimcha foydali havolalar -->
    <div style="background: #1b2815; padding: 20px; margin: 30px 0; border: 2px solid #708a4a;">
        <h3 style="color: #ffcc77; margin-bottom: 10px;">🔗 Foydali manbalar (O'zbekiston o'yinchilari uchun)</h3>
        <p>📌 <strong>Skinlar yuklash:</strong> NameMC, Planet Minecraft <br>
        📌 <strong>Modlar:</strong> CurseForge, Modrinth <br>
        📌 <strong>Seed tekshirish:</strong> Chunkbase (App) <br>
        📌 <strong>O‘zbekcha Discord server:</strong> Minecraft.uz community</p>
        <p style="margin-top: 12px;">✨ Barcha ma'lumotlar siz uchun, <strong>Ortiqjon Xasanov</strong> — dunyongiz keng bo'lsin!</p>
    </div>
</main>

<footer>
    <p>© 2025 Minecraft World | Ortiqjon Xasanov tomonidan yaratilgan. Minecraft rasmiy Mojang brendi.</p>
    <p>Sayt faqat ma'lumot olish uchun. Barcha skinlar, modlar mualliflik huquqiga ega.</p>
</footer>

</body>
</html>
