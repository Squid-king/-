<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>親愛的鼻 ❤️</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background: linear-gradient(to right, #ffb6c1, #ff6a9d); /* 粉紅色漸層背景 */
            padding: 20px;
            margin: 0;
            height: 100vh;
            overflow: hidden;
        }
        h1 {
            color: white; /* 字體顏色改為白色 */
            font-size: 2.5em;
            margin-bottom: 20px;
        }
        .dialog-box {
            margin-top: 50px;
            padding: 20px;
            border: 2px solid #f54b8d;
            background-color: #fff;
            border-radius: 15px;
            display: inline-block;
            width: 100%;
            max-width: 90%;
            text-align: center;
            font-size: 1.2em; /* 字體縮小 */
            line-height: 1.5;
        }
        .button-container {
            display: flex;
            justify-content: space-between;
            margin-top: 20px;
        }
        button {
            color: white;
            border: none;
            padding: 10px;
            border-radius: 10px;
            cursor: pointer;
            font-size: 1em;
            width: 45%;
        }
        .love-btn {
            background-color: #f54b8d;
        }
        .love-btn:hover {
            background-color: #d43d6a;
        }
        .not-love-btn {
            background-color: #8c8c8c;
        }
        .not-love-btn:hover {
            background-color: #707070;
        }
        .response {
            margin-top: 20px;
            font-size: 1.4em; /* 字體縮小 */
            color: #d43d6a;
            font-weight: bold;
            white-space: normal; /* 文字換行 */
            overflow: hidden;
            text-overflow: ellipsis; /* 文字溢出時顯示省略號 */
        }

        /* 手機版適配 */
        @media (max-width: 600px) {
            h1 {
                font-size: 2em;
            }
            .dialog-box {
                width: 100%;
                padding: 15px;
                font-size: 1.1em;
            }
            .button-container {
                flex-direction: column;
                justify-content: center;
                align-items: center;
            }
            button {
                width: 80%;
                font-size: 1.1em;
                margin-bottom: 10px;
            }
            .response {
                font-size: 1.2em;
            }
        }
    </style>
</head>
<body>
    <h1>親愛的鼻 ❤️</h1>
    <div class="dialog-box" id="dialogBox">
        <p id="question">愛不愛我?</p>
        <div class="response" id="response"></div> <!-- 跳出的文字會顯示在這裡 -->
        <div class="button-container">
            <button class="love-btn" onclick="chooseLove()">愛你</button>
            <button class="not-love-btn" onclick="chooseNotLove()">不愛你</button>
        </div>
    </div>

    <script>
        function chooseLove() {
            document.getElementById('question').style.display = 'none'; // 隱藏問題文字
            const responses = [
                "我也愛你",
                "我愛你也想跟你抱抱",
                "寶貝真的嗎？我也好愛你喔"
            ];
            const randomResponse = responses[Math.floor(Math.random() * responses.length)];
            document.getElementById('response').innerText = randomResponse;
        }

        function chooseNotLove() {
            document.getElementById('question').style.display = 'none'; // 隱藏問題文字
            const responses = [
                "好啊？不愛我是不是！我就知道你4給！！",
                "你不是背著我搞什麼了？",
                "嗚嗚嗚！渣男！"
            ];
            const randomResponse = responses[Math.floor(Math.random() * responses.length)];
            document.getElementById('response').innerText = randomResponse;
        }
    </script>
</body>
</html>
