<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quiz Dễ Thương</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #ffecf0;
            padding: 20px;
        }
        .quiz-container {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            max-width: 400px;
            margin: auto;
        }
        button {
            margin-top: 10px;
            padding: 10px;
            border: none;
            background-color: #ff66b2;
            color: white;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #ff3385;
        }
    </style>
</head>
<body>
    <div class="quiz-container" id="quiz">
        <h2 id="question">Em có người yêu chưa?</h2>
        <div id="answers">
            <button onclick="nextQuestion(1)">Rồi</button>
            <button onclick="nextQuestion(0)">Chưa</button>
        </div>
    </div>
    <script>
        let step = 0;
        function nextQuestion(answer) {
            const quiz = document.getElementById("quiz");
            if (step === 0 && answer === 1) {
                quiz.innerHTML = '<h2>Người yêu em tên gì?</h2><input type="text" id="nameInput"><button onclick="checkName()">Tiếp tục</button>';
            } else if (step === 0 && answer === 0) {
                quiz.innerHTML = '<h2>Huhu, vậy khi nào có nhớ báo anh nhé!</h2>';
            }
        }

        function checkName() {
            const name = document.getElementById("nameInput").value;
            if (name.trim().toLowerCase() === "đặng nhã quỳnh") {
                document.getElementById("quiz").innerHTML = '<h2>Em có yêu người yêu của em không?</h2><button onclick="loveMessage()">Có</button><button onclick="loveMessage()">Rất có</button>';
            } else {
                alert("Sai rồi! Hãy nhập lại tên người yêu em nhé!");
            }
        }
        
        function loveMessage() {
            document.getElementById("quiz").innerHTML = '<h2>Em yêu người yêu của em thì hãy nhắn gửi đến người đó gì đi</h2><input type="text" id="message"><button onclick="finalMessage()">Gửi</button>';
        }
        
        function finalMessage() {
            document.getElementById("quiz").innerHTML = '<h2>NQ yêu em</h2>';
        }
    </script>
</body>
</html>![483107603_122129740448415214_1343454979986706313_n](https://github.com/user-attachments/assets/b4d5e380-10f7-4375-a97c-ae1c685c7e66)
