<!DOCTYPE html>
<html>
<head>
  <title>siteTest</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-image: url("11.png");
      background-size: cover;
      background-position: center;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .container {
      background-color: rgba(186, 59, 59, 0.9);
      border-radius: 8px;
      padding: 20px;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
      width: 300px;
      text-align: center;
    }

    .container h1 {
      margin-top: 0;
      color: white;
    }

    .logo {
      width: 100px;
      height: 100px;
      margin: 0 auto 20px;
      background-image: url("11.png");
      background-size: contain;
      background-repeat: no-repeat;
    }

    .form-group {
      margin-bottom: 10px;
    }

    .form-group label {
      display: block;
      font-weight: bold;
      margin-bottom: 5px;
      color: white;
    }

    .form-group input[type="text"],
    .form-group input[type="password"] {
      width: 100%;
      padding: 8px;
      border-radius: 4px;
      border: 1px solid #ccc;
    }

    .form-group button {
      width: 100%;
      padding: 10px;
      background-color: #1877f2;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }

    .form-group button:hover {
      background-color: #1559a5;
    }

    .toggle-link {
      margin-top: 10px;
    }

    .site-like {
      color: white;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="logo"></div>
    <h1>Formulário</h1>
    <div id="loginForm">
      <form>
        <div class="form-group">
          <label for="username">Usuário:</label>
          <input type="text" id="username" placeholder="Digite seu usuário" required>
        </div>
        <div class="form-group">
          <label for="password">Senha:</label>
          <input type="password" id="password" placeholder="Digite sua senha" required>
        </div>
        <div class="form-group">
          <button type="submit">Entrar</button>
        </div>
        <div class="toggle-link">
          <a href="#" onclick="toggleForm('registerForm')">Criar uma conta</a>
        </div>
      </form>
    </div>
    <div id="registerForm" style="display: none;">
      <form>
        <div class="form-group">
          <label for="newUsername">Novo Usuário:</label>
          <input type="text" id="newUsername" placeholder="Digite seu novo usuário" required>
        </div>
        <div class="form-group">
          <label for="newPassword">Nova Senha:</label>
          <input type="password" id="newPassword" placeholder="Digite sua nova senha" required>
        </div>
        <div class="form-group">
          <button type="submit">Cadastrar</button>
        </div>
        <div class="toggle-link">
          <a href="#" onclick="toggleForm('loginForm')">Voltar para o login</a>
        </div>
      </form>
    </div>
    <h1 class="site-like">Gostou do site??</h1>
    <button class="button" id="simButton">Sim</button>
    <button class="button button-no" id="naoButton">Não</button>

    <script>
      var simButton = document.getElementById("simButton");
      var naoButton = document.getElementById("naoButton");
    
      simButton.addEventListener("click", function() {
        alert("Entra nesse site: https://www.youtube.com/watch?v=I7R-aemDDiA&ab_channel=CostaRF");
      });
    
      naoButton.addEventListener("click", function() {
        alert("Você clicou no botão errado. Sugiro que tente mais uma vez.");
      });
    </script>
  </div>
</body>
<script>
  function toggleForm(formId) {
    var loginForm = document.getElementById('loginForm');
    var registerForm = document.getElementById('registerForm');

    if (formId === 'loginForm') {
      loginForm.style.display = 'block';
      registerForm.style.display = 'none';
    } else {
      loginForm.style.display = 'none';
      registerForm.style.display = 'block';
    }
  }
</script>
</html>
