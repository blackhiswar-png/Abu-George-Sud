<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <title>سود محمد عارف حربه - برنامج الأسئلة عن المشاركات</title>
  <style>
    body {
      background: #222;
      color: #eee;
      font-family: 'Cairo', Arial, sans-serif;
      text-align: center;
      margin: 0;
      padding: 0;
    }
    .container {
      max-width: 400px;
      margin: 60px auto;
      background: #333;
      border-radius: 12px;
      padding: 32px 16px;
      box-shadow: 0 2px 12px #0006;
    }
    input, button {
      padding: 12px;
      border-radius: 6px;
      border: none;
      margin: 8px 0;
      font-size: 1.1em;
      width: 80%;
    }
    button {
      background: #444;
      color: #fff;
      cursor: pointer;
      transition: background 0.2s;
    }
    button:hover {
      background: #555;
    }
    .answer {
      margin-top: 24px;
      background: #222;
      padding: 14px;
      border-radius: 8px;
      min-height: 40px;
      color: #f8ea9e;
      font-weight: bold;
    }
    h1 {
      margin-bottom: 12px;
      color: #ffd700;
    }
    .sub {
      color: #aaa;
      font-size: 1em;
      margin-bottom: 20px;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>سود محمد عارف حربه</h1>
    <div class="sub">برنامج الأسئلة حول المشاركات</div>
    <form id="askForm" onsubmit="return false;">
      <input type="text" id="question" placeholder="اكتب سؤالك حول المشاركات هنا..." required>
      <br>
      <button onclick="answerQuestion()">اسأل</button>
    </form>
    <div class="answer" id="answer"></div>
  </div>
  <script>
    function answerQuestion() {
      var q = document.getElementById('question').value.trim();
      var answerDiv = document.getElementById('answer');
      if (!q) {
        answerDiv.textContent = "يرجى كتابة سؤال.";
        return;
      }
      // نموذج إجابة تلقائية (يمكن تعديلها لاحقاً)
      var answers = [
        "المشاركة الأخيرة كانت مميزة جداً!",
        "عدد المشاركات حتى الآن: 15 مشاركة.",
        "يمكنك إضافة مشاركة جديدة في أي وقت.",
        "جميع المشاركات متاحة للعرض.",
        "لم يتم العثور على مشاركات متعلقة بهذا السؤال."
      ];
      // إخراج إجابة عشوائية
      var ans = answers[Math.floor(Math.random() * answers.length)];
      answerDiv.textContent = ans;
    }
  </script>
</body>
</html>
