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
        /* 漢堡菜單樣式 */
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
        .menu a:hover {
            background-color: #f0f0f0;
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
    <!-- 漢堡菜單 -->
    <div class="hamburger" onclick="toggleMenu()">
        <div></div>
        <div></div>
        <div></div>
    </div>
    <div class="menu" id="menu">
        <a href="https://iscg-yt.github.io">1. Map code</a>
        <a href="https://linktr.ee/ff.cg">2. All social medias</a>
    </div>
    <!-- 搜尋框 -->
    <div class="search-bar">
        <input type="text" id="searchInput" placeholder="搜尋關鍵字...">
        <button onclick="searchContent()">搜尋</button>
    </div>
    <!-- 主頁內容 -->
    <div class="container">
        <!-- Section 1 -->
        <h1>所有進化武器體驗</h1>
        <div class="section">
            <img src="Screenshot_20241225-220715328.jpg" alt="1">
            <p id="text1">#FREEFIREC55A6330CE58EB61C8E3C975B8E90D8F9815</p>
            <button class="copy-btn" onclick="copyText('text1')">複製代碼</button>
        </div>
        <div class="divider"></div>
        <!-- Section 2 -->
        <h1>外掛體驗</h1>
        <div class="section">
            <img src="Screenshot_20241226-191506882.jpg" alt="2">
            <p id="text2">#FREEFIRED796B3438F1B31DDE1814CA8A851491A9815</p>
            <button class="copy-btn" onclick="copyText('text2')">複製代碼</button>
        </div>
        <div class="divider"></div>
        <!-- Section 3 -->
        <h1>單人-全進化槍+衣服</h1>
        <div class="section">
            <img src="Screenshot_20241226-201708674_2.jpg" alt="3">
            <p id="text3">#FREEFIRECC6698AD72FE062B3D8E4D9463D61CDD9815</p>
            <button class="copy-btn" onclick="copyText('text3')">複製代碼</button>
        </div>
        <div class="divider"></div>
        <!-- Section 4 -->
        <h1>雙人-全進化槍+衣服</h1>
        <div class="section">
            <img src="Screenshot_20241226-201708674_1.jpg" alt="4">
            <p id="text4">#FREEFIREDF3E35BEF841A8858646FC70F227CC6F9815</p>
            <button class="copy-btn" onclick="copyText('text4')">複製代碼</button>
        </div>
        <div class="divider"></div>
        <!-- Section 5 -->
        <h1>雙人合作跑酷</h1>
        <div class="section">
            <img src="Screenshot_20241226-201708674_1.jpg" alt="4">
            <p id="text4">#FREEFIREDF3E35BEF841A8858646FC70F227CC6F9815</p>
            <button class="copy-btn" onclick="copyText('text4')">複製代碼</button>
        </div>
        <div class="divider"></div>
    </div>
    <script>
        // 切換漢堡菜單顯示
        function toggleMenu() {
            const menu = document.getElementById('menu');
            menu.style.display = menu.style.display === 'block' ? 'none' : 'block';
        }
        // 搜尋功能
        function searchContent() {
            const input = document.getElementById('searchInput').value.toLowerCase();
            const sections = document.querySelectorAll('.section');
            sections.forEach(section => {
                const keywords = section.getAttribute('data-keywords').toLowerCase();
                if (keywords.includes(input)) {
                    section.classList.remove('hidden');
                } else {
                    section.classList.add('hidden');
                }
            });
        }
    </script>
</body>
</html>
