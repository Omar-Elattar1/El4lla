<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>اسألني</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            direction: rtl;
            text-align: center;
            background-color: #f5f5f5;
        }
        .container {
            width: 50%;
            margin: auto;
            background: white;
            padding: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
        }
        input, button {
            padding: 10px;
            margin: 10px 0;
            width: 80%;
        }
        button {
            background: #007bff;
            color: white;
            border: none;
            cursor: pointer;
            padding: 10px;
            border-radius: 5px;
        }
        button:hover {
            background: #0056b3;
        }
        ul {
            list-style: none;
            padding: 0;
        }
        li {
            background: #eee;
            margin: 5px;
            padding: 10px;
            border-radius: 5px;
        }
        .admin {
            margin-top: 30px;
            padding: 10px;
            background: #ddd;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>اسألني أي سؤال</h1>
        <form id="questionForm">
            <input type="text" id="questionInput" placeholder="اكتب سؤالك هنا..." required>
            <button type="submit">إرسال</button>
        </form>
        
        <div id="questionsContainer">
            <h2>الأسئلة والإجابات:</h2>
            <ul id="questionsList"></ul>
        </div>

        <div class="admin">
            <h2>لوحة التحكم (للإجابة على الأسئلة)</h2>
            <ul id="adminQuestionsList"></ul>
        </div>
    </div>

    <script>
        document.getElementById('questionForm').addEventListener('submit', function(event) {
            event.preventDefault();
            
            let questionInput = document.getElementById('questionInput');
            let questionText = questionInput.value.trim();
            
            if (questionText !== "") {
                let questions = JSON.parse(localStorage.getItem('questions')) || [];
                
                // حفظ السؤال بدون إجابة
                questions.push({ question: questionText, answer: "" });
                localStorage.setItem('questions', JSON.stringify(questions));
                
                questionInput.value = ""; // مسح الحقل بعد الإرسال
                displayQuestions();
            }
        });

        function displayQuestions() {
            let questionsList = document.getElementById('questionsList');
            let adminQuestionsList = document.getElementById('adminQuestionsList');
            
            questionsList.innerHTML = "";
            adminQuestionsList.innerHTML = "";
            
            let questions = JSON.parse(localStorage.getItem('questions')) || [];
            
            questions.forEach((q, index) => {
                let li = document.createElement('li');

                if (q.answer) {
                    li.innerHTML = `<strong>س: ${q.question}</strong><br>ج: ${q.answer}`;
                    questionsList.appendChild(li);
                } else {
                    let adminLi = document.createElement('li');
                    adminLi.innerHTML = `<strong>س: ${q.question}</strong> 
                        <button onclick="editAnswer(${index})">أضف إجابة</button>`;
                    adminQuestionsList.appendChild(adminLi);
                }
            });
        }

        function editAnswer(index) {
            let questions = JSON.parse(localStorage.getItem('questions')) || [];
            let newAnswer = prompt("اكتب الإجابة:");

            if (newAnswer) {
                questions[index].answer = newAnswer;
                localStorage.setItem('questions', JSON.stringify(questions));
                displayQuestions();
            }
        }

        displayQuestions();
    </script>
</body>
</html>
