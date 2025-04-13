<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ABCESS GRUMEC - Login</title>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Roboto', sans-serif;
    }

    body {
      background: linear-gradient(135deg, #8b0000, #ff4d4d);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .login-wrapper {
      background-color: white;
      padding: 3rem 2rem;
      border-radius: 16px;
      box-shadow: 0 15px 25px rgba(0, 0, 0, 0.3);
      width: 100%;
      max-width: 400px;
      text-align: center;
    }

    .login-wrapper h1 {
      color: #8b0000;
      margin-bottom: 0.5rem;
      font-size: 1.8rem;
    }

    .login-wrapper h2 {
      text-align: center;
      margin-bottom: 1.5rem;
      color: #333;
    }

    .form-group {
      margin-bottom: 1.2rem;
      text-align: left;
    }

    .form-group label {
      display: block;
      margin-bottom: 0.5rem;
      color: #555;
      font-weight: 500;
    }

    .form-group input {
      width: 100%;
      padding: 10px 14px;
      border: 1px solid #ccc;
      border-radius: 8px;
      font-size: 1rem;
    }

    .btn-login {
      width: 100%;
      padding: 12px;
      background-color: #8b0000;
      color: white;
      border: none;
      border-radius: 8px;
      font-size: 1.1rem;
      cursor: pointer;
      transition: background 0.3s;
    }

    .btn-login:hover {
      background-color: #b30000;
    }

    .alert {
      margin-top: 1rem;
      padding: 0.8rem;
      background-color: #f8d7da;
      color: #721c24;
      border: 1px solid #f5c6cb;
      border-radius: 8px;
      display: none;
    }

    .footer {
      margin-top: 2rem;
      font-size: 0.85rem;
      color: #999;
    }
  </style>
</head>
<body>
  <div class="login-wrapper">
    <h1>ABCESS GRUMEC</h1>
    <h2>Acesso ao Painel</h2>
    <div class="form-group">
      <label for="email">E-mail</label>
      <input type="email" id="email" placeholder="Digite seu e-mail" required />
    </div>
    <div class="form-group">
      <label for="senha">Senha</label>
      <input type="password" id="senha" placeholder="Digite sua senha" required />
    </div>
    <button class="btn-login" onclick="fazerLogin()">Entrar</button>
    <div class="alert" id="mensagemErro">E-mail ou senha incorretos.</div>
    <div class="footer">BY SOUZAHZZ & Stop</div>
  </div>

  <script>
    function fazerLogin() {
      const email = document.getElementById('email').value;
      const senha = document.getElementById('senha').value;
      const alerta = document.getElementById('mensagemErro');

      if (email === 'admin@empresa.com' && senha === 'admin123') {
        alerta.style.display = 'none';
        alert('Login bem-sucedido! Redirecionando para o painel...');
        // window.location.href = '/painel.html';
      } else {
        alerta.style.display = 'block';
      }
    }
  </script>
</body>
</html>
