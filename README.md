<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Merry Christmas</title>
    <style>
        body {
            background-color: #2b2b2b;
            font-family: Arial, sans-serif;
            text-align: center;
            color: white;
        }
        .gift-box {
            position: relative;
            margin: 50px auto;
            width: 200px;
            height: 200px;
            background-color: #ff0000;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
            cursor: pointer;
        }
        .gift-box:before {
            content: "";
            position: absolute;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 40px;
            height: 200px;
            background-color: gold;
            z-index: 1;
        }
        .gift-box:after {
            content: "";
            position: absolute;
            left: 0;
            top: 50%;
            transform: translateY(-50%);
            width: 200px;
            height: 40px;
            background-color: gold;
            z-index: 1;
        }
        .tree {
            display: none;
            margin-top: -100px;
            animation: appear 2s ease forwards;
        }
        .tree .branches {
            background-color: green;
            width: 0;
            height: 0;
            border-left: 50px solid transparent;
            border-right: 50px solid transparent;
            border-bottom: 80px solid green;
            margin: 0 auto;
        }
        .tree .branches:not(:last-child) {
            margin-bottom: -30px;
        }
        .tree .lights {
            width: 6px;
            height: 6px;
            background-color: gold;
            border-radius: 50%;
            position: absolute;
            animation: blink 1.5s infinite;
        }
        .tree .star {
            font-size: 24px;
            color: gold;
            position: relative;
            margin-bottom: -15px;
        }
        @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.3; }
        }
        @keyframes appear {
            from { opacity: 0; transform: translateY(50px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>
    <h1>Merry Christmas!</h1>
    <div class="gift-box" onclick="openGift()">
        <div class="ribbon"></div>
    </div>
    <div class="tree" id="tree">
        <div class="star">★</div>
        <div class="branches"></div>
        <div class="branches"></div>
        <div class="branches"></div>
        <div class="branches"></div>
        <div class="branches"></div>
        <div class="lights" style="top: 20px; left: 90px;"></div>
        <div class="lights" style="top: 50px; left: 110px;"></div>
        <div class="lights" style="top: 80px; left: 70px;"></div>
        <div class="lights" style="top: 110px; left: 90px;"></div>
    </div>
    <script>
        function openGift() {
            document.querySelector(".gift-box").style.display = "none";
            document.getElementById("tree").style.display = "block";
        }
    </script>
</body>
</html>
