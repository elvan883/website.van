<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Website Elvan</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: linear-gradient(135deg, #667eea, #764ba2);
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
        }

        .container {
            text-align: center;
            background: rgba(0, 0, 0, 0.3);
            padding: 40px;
            border-radius: 15px;
            width: 300px;
        }

        h1 {
            margin-bottom: 30px;
        }

        button {
            padding: 10px 20px;
            margin: 10px;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            font-size: 16px;
            transition: 0.3s;
        }

        .klik {
            background-color: #ff6b81;
            color: white;
        }

        .cancel {
            background-color: #f1f2f6;
            color: #333;
        }

        button:hover {
            transform: scale(1.1);
        }

        .hidden {
            display: none;
        }

        .love {
            font-size: 40px;
            animation: pulse 1s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.2); }
            100% { transform: scale(1); }
        }
    </style>
</head>
<body>

    <!-- Layar Pertama -->
    <div class="container" id="home">
        <h1>Haiiiiiii kenalinnn gua elvann</h1>
        <button class="klik" onclick="showLove()">Klik</button>
        <button class="cancel" onclick="backHome()">Cancel</button>
    </div>

    <!-- Layar Kedua -->
    <div class="container hidden" id="love">
        <div class="love">Lovyuuu 💖</div>
        <br>
        <button class="cancel" onclick="backHome()">Kembali</button>
    </div>

    <script>
        function showLove() {
            document.getElementById("home").classList.add("hidden");
            document.getElementById("love").classList.remove("hidden");
        }

        function backHome() {
            document.getElementById("love").classList.add("hidden");
            document.getElementById("home").classList.remove("hidden");
        }
    </script>

</body>
</html>
