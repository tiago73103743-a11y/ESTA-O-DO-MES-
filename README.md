<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Estação do Ano</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #f2f2f2, #e6e6e6);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .container {
      background: white;
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
      text-align: center;
      width: 300px;
    }

    h2 {
      margin-bottom: 15px;
    }

    input, button {
      padding: 10px;
      margin: 10px 0;
      border-radius: 8px;
      border: 1px solid #ccc;
      font-size: 16px;
      width: 100%;
    }

    button {
      background: #4CAF50;
      color: white;
      cursor: pointer;
      transition: 0.3s;
    }

    button:hover {
      background: #45a049;
    }

    #resultado {
      font-weight: bold;
      margin-top: 20px;
      font-size: 18px;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>Descubra a Estação do Ano</h2>
    <label for="mes">Digite o mês (1 a 12):</label>
    <input type="number" id="mes" min="1" max="12" placeholder="Ex: 3 para Março">
    <button onclick="verEstacao()">Ver Estação</button>
    <p id="resultado"></p>
  </div>

  <script>
    function verEstacao() {
      let mes = parseInt(document.getElementById("mes").value);
      let estacao = "";

      switch(mes) {
        case 12: case 1: case 2:
          estacao = "Verão 🌞";
          break;
        case 3: case 4: case 5:
          estacao = "Outono 🍂";
          break;
        case 6: case 7: case 8:
          estacao = "Inverno ❄️";
          break;
        case 9: case 10: case 11:
          estacao = "Primavera 🌸";
          break;
        default:
          estacao = "Mês inválido!";
      }

      document.getElementById("resultado").innerText = "Estação: " + estacao;
    }
  </script>
</body>
</html>
