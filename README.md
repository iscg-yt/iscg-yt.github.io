<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>戰場地圖代碼</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
        }
        .hamburger {
            position: fixed;
            top: 20px;
            right: 20px;
            width: 50px;
            height: 50px;
            cursor: pointer;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }
        .hamburger div {
            height: 6px;
            width: 100%;
            background-color: black;
            border-radius: 3px;
        }
        .menu {
            display: none;
            position: fixed;
            top: 80px;
            right: 20px;
            background-color: white;
            border: 2px solid #ccc;
            border-radius: 12px;
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);
            padding: 20px;
            width: 250px;
        }
        .menu a {
            text-decoration: none;
            color: black;
            font-size: 18px;
            display: block;
            padding: 12px 15px;
            border-bottom: 1px solid #ccc;
        }
        .menu a:last-child {
            border-bottom: none;
        }
        .search-bar {
            display: flex;
            justify-content: center;
            margin: 20px 0;
        }
        .search-bar input {
            width: 300px;
            padding: 10px;
            font-size: 16px;
            border: 1px solid #ccc;
            border-radius: 8px;
            margin-right: 10px;
        }
        .search-bar button {
            padding: 10px 20px;
            font-size: 16px;
            background-color: #007BFF;
            color: white;
            border: none;
            border-radius: 8px;
            cursor: pointer;
        }
        .search-bar button:hover {
            background-color: #0056b3;
        }
        .container {
            max-width: 800px;
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            margin: 20px auto;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        .section {
            text-align: center;
            margin-bottom: 30px;
        }
        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <div class="hamburger" onclick="toggleMenu()">
        <div></div>
        <div></div>
        <div></div>
    </div>
    <div class="menu" id="menu">
        <a href="https://iscg-yt.github.io"><p style="font-size: 30px;">1.Map code</p></a>
        <a href="https://linktr.ee/ff.cg"><p style="font-size: 30px;">2. All social medias</p></a>
        <a href="https://forms.zohopublic.com/sobrickffgm1/form/Playersmaprecommend/formperma/lsD3viLptVn5sEEwdmRBHRpsjEWC7ZF-q0gihbwDW7k"><p style="font-size: 30px;">3. Players map recommend（問卷）</p></a>
        <a href="https://linktr.ee/ff.cg"><p style="font-size: 30px;">4. Players map recommend（地圖）</p></a>
    </div>
    <div class="search-bar">
        <input type="text" id="searchInput" placeholder="搜尋關鍵字...">
        <button onclick="filterSections()">搜尋</button>
    </div>
    <div class="container">
        <h1>[b]我的戰場地圖代碼</h1>
        <!-- Section 1 -->
        <div class="section" data-keywords="進化槍 進化武器 進化 衣服 體驗 塗裝 #FREEFIREC55A6330CE58EB61C8E3C975B8E90D8F9815">
            <h1>所有進化武器體驗</h1>
            <img src="Screenshot_20241225-220715328.jpg" alt="進化武器">
            <p id="text1">#FREEFIREC55A6330CE58EB61C8E3C975B8E90D8F9815</p>
            <button class="copy-btn" onclick="copyText('text1')">複製代碼</button>
        </div>
        <!-- Section 2 -->
        <div class="section" data-keywords="外掛 體驗 外掛體驗 #FREEFIRED796B3438F1B31DDE1814CA8A851491A9815">
            <h1>外掛體驗！</h1>
            <img src="Screenshot_20241226-191506882.jpg" alt="外掛">
            <p id="text2">#FREEFIRED796B3438F1B31DDE1814CA8A851491A9815</p>
            <button class="copy-btn" onclick="copyText('text2')">複製代碼</button>
        </div>
        <!-- Section 3 -->
        <div class="section" data-keywords="單人 進化槍 進化武器 進化 衣服 塗裝 體驗 #FREEFIRECC6698AD72FE062B3D8E4D9463D61CDD9815">
            <h1>單人-全進化槍+衣服</h1>
            <img src="Screenshot_20241226-201708674_2.jpg" alt="單人">
            <p id="text3">#FREEFIRECC6698AD72FE062B3D8E4D9463D61CDD9815</p>
            <button class="copy-btn" onclick="copyText('text3')">複製代碼</button>
        </div>
        <!-- Section 4 -->
        <div class="section" data-keywords="雙人 進化槍 進化武器 進化 衣服 塗裝 體驗 #FREEFIREDF3E35BEF841A8858646FC70F227CC6F9815">
            <h1>雙人-全進化槍+衣服</h1>
            <img src="Screenshot_20241226-201708674_1.jpg" alt="雙人">
            <p id="text4">#FREEFIREDF3E35BEF841A8858646FC70F227CC6F9815</p>
            <button class="copy-btn" onclick="copyText('text4')">複製代碼</button>
        </div>
        <!-- Section 5 -->
        <div class="section" data-keywords="塗裝 裕隆歸 裕隆 #FREEFIRE64F58476D76F49441A1B9FA0600547229815">
            <h1>自動去塗裝地圖（裕隆規用）</h1>
            <img src="Screenshot_20241230-211928416.jpg" alt="裕隆">
            <p id="text5">#FREEFIRE64F58476D76F49441A1B9FA0600547229815</p>
            <button class="copy-btn" onclick="copyText('text5')">複製代碼</button>
        </div>
        <!-- Section 6 -->
        <div class="section" data-keywords="取得服裝 取得服裝id #FREEFIREC77E5B663EBB33602FD4C8074A86A8B79815">
            <h1>取得服裝ID</h1>
            <img src="Screenshot_20241230-212331781.jpg" alt="服裝">
            <p id="text6">#FREEFIREC77E5B663EBB33602FD4C8074A86A8B79815</p>
            <button class="copy-btn" onclick="copyText('text6')">複製代碼</button>
        </div>
        <!-- Section 7 -->
        <div class="section" data-keywords="狙擊 訓練場 狙擊訓練場 單人 #FREEFIRE99929B54F0C8CDABAD54FF2157E51FC49815">
            <h1>單人-狙擊訓練場</h1>
            <img src="Screenshot_20241230-212242413.jpg" alt="狙擊訓練場">
            <p id="text7">#FREEFIRE99929B54F0C8CDABAD54FF2157E51FC49815</p>
            <button class="copy-btn" onclick="copyText('text7')">複製代碼</button>
        </div>
        <!-- Section 8 -->
        <div class="section" data-keywords="雙人 跑酷 合作 雙人合作 雙人跑酷 雙人合作跑酷 #FREEFIREBDDA32692D1DFB97BF2CD77842895A4B9815">
            <h1>雙人合作跑酷</h1>
            <img src="FreeFire_01_01_2025 14_05_16.png" alt="雙人跑酷">
            <p id="text8">#FREEFIREBDDA32692D1DFB97BF2CD77842895A4B9815</p>
            <button class="copy-btn" onclick="copyText('text8')">複製代碼</button>
        </div>
        <!-- Section 9 -->
        <div class="section" data-keywords="凝膠 體驗 凝膠塗裝 塗裝體驗 塗裝 凝膠塗裝體驗 #FREEFIREA56D6F07C155F825F63CCD7BA50871219815">
            <h1>凝膠塗裝體驗</h1>
            <img src="Screenshot_20250101-140333230.jpg" alt="凝膠塗裝體驗">
            <p id="text9">#FREEFIREA56D6F07C155F825F63CCD7BA50871219815</p>
            <button class="copy-btn" onclick="copyText('text9')">複製代碼</button>
        </div>
    <script>
        // 切換漢堡菜單顯示
        function toggleMenu() {
            const menu = document.getElementById('menu');
            menu.style.display = menu.style.display === 'block' ? 'none' : 'block';
        }
        // 複製文字功能
        function copyText(elementId) {
            const text = document.getElementById(elementId).innerText;
            navigator.clipboard.writeText(text).then(() => {
                alert("已複製！快去玩玩看地圖吧！");
            }).catch(err => {
                alert("複製失敗，請重試！");
            });
        }
        // 搜尋功能
        function filterSections() {
            const query = document.getElementById('searchInput').value.toLowerCase();
            const sections = document.querySelectorAll('.section');
            sections.forEach(section => {
                const keywords = section.getAttribute('data-keywords').toLowerCase();
                if (keywords.includes(query)) {
                    section.style.display = "block";
                } else {
                    section.style.display = "none";
                }
            });
        }
    </script>
</body>
</html>
