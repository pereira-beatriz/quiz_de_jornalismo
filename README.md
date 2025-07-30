# quiz_de_jornalismo
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Quiz de Jornalismo</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f2f2f2;
      padding: 20px;
      max-width: 600px;
      margin: auto;
    }
    h1 {
      color: #2c3e50;
    }
    .question {
      margin-bottom: 20px;
      padding: 15px;
      background: #fff;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
    .options label {
      display: block;
      margin-bottom: 8px;
      cursor: pointer;
    }
    .btn {
      padding: 10px 20px;
      background: #3498db;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      margin-top: 10px;
    }
    .result {
      margin-top: 20px;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1>📰 Quiz sobre Jornalismo</h1>
  <form id="quizForm">
    <div class="question">
      <p>1️⃣ Qual é a principal função do jornalismo?</p>
      <div class="options">
        <label><input type="radio" name="q1" value="0"> Entreter o público</label>
        <label><input type="radio" name="q1" value="1"> Informar e educar a sociedade</label>
        <label><input type="radio" name="q1" value="2"> Promover produtos e serviços</label>
        <label><input type="radio" name="q1" value="3"> Criar histórias fictícias</label>
      </div>
    </div>
    <div class="question">
      <p>2️⃣ O que é considerado um princípio ético fundamental no jornalismo?</p>
      <div class="options">
        <label><input type="radio" name="q2" value="0"> Sensacionalismo</label>
        <label><input type="radio" name="q2" value="1"> Imparcialidade</label>
        <label><input type="radio" name="q2" value="2"> Publicidade paga</label>
        <label><input type="radio" name="q2" value="3"> Exagero nas manchetes</label>
      </div>
    </div>
    <button type="button" class="btn" onclick="checkAnswers()">Verificar respostas</button>
    <div class="result" id="result"></div>
  </form>

  <script>
    function checkAnswers() {
      const resultEl = document.getElementById('result');
      const answers = [1, 1];
      let score = 0;

      const q1 = document.querySelector('input[name="q1"]:checked');
      const q2 = document.querySelector('input[name="q2"]:checked');

      if (q1 && parseInt(q1.value) === answers[0]) score++;
      if (q2 && parseInt(q2.value) === answers[1]) score++;

      resultEl.textContent = `Você acertou ${score} de 2 questões.`;
    }
  </script>
</body>
</html>
