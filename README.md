# 人工智慧期中報告

## 👤 基本資料
班級：___  
學號：___  
姓名：___  

---

## 🎮 遊戲畫面
（之後放截圖）

---

## 🎨 Logo
![logo](logo.png)

---

## 💻 程式碼
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>可愛點擊遊戲</title>
    <style>
        body {
            text-align: center;
            font-family: Arial;
            background-color: #ffe4f2;
        }

        h1 {
            color: #ff66a3;
        }

        button {
            font-size: 30px;
            padding: 20px;
            border-radius: 15px;
            background-color: #ff99cc;
            border: none;
            cursor: pointer;
        }

        button:hover {
            background-color: #ff66a3;
        }
    </style>
</head>

<body>

<h1>🎮 可愛點擊遊戲 🎮</h1>

<p>分數：<span id="score">0</span></p>
<p>時間：<span id="time">10</span> 秒</p>

<button onclick="addScore()">點我！</button>

<h2 id="result"></h2>

<script>
let score = 0;
let time = 10;

function addScore() {
    if (time > 0) {
        score++;
        document.getElementById("score").innerText = score;
    }
}

let timer = setInterval(function () {
    time--;
    document.getElementById("time").innerText = time;

    if (time <= 0) {
        clearInterval(timer);
        document.getElementById("result").innerText = "遊戲結束！你的分數：" + score;
    }
}, 1000);
</script>

</body>
</html>
