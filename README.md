<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<title>RB Platform</title>

<style>
  * {
    box-sizing: border-box;
  }

  body {
    margin: 0;
    font-family: "Segoe UI", Arial, sans-serif;
    background-color: #121215;
    color: #ffffff;
  }

  /* ===== HEADER (как у Roblox) ===== */
  header {
    height: 56px;
    background-color: #1f2023;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 24px;
    border-bottom: 1px solid #2c2d30;
  }

  .logo {
    font-size: 20px;
    font-weight: 700;
    letter-spacing: 1px;
  }

  .header-buttons button {
    background: #ffffff;
    color: #000;
    border: none;
    padding: 8px 16px;
    border-radius: 6px;
    font-weight: 600;
    cursor: pointer;
  }

  /* ===== MAIN ===== */
  .main {
    max-width: 1100px;
    margin: 40px auto;
    padding: 0 20px;
  }

  .welcome {
    font-size: 28px;
    font-weight: 700;
    margin-bottom: 8px;
  }

  .subtitle {
    color: #b0b0b0;
    margin-bottom: 32px;
  }

  /* ===== GAME CARDS (как Roblox плитки) ===== */
  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
    gap: 20px;
  }

  .card {
    background: #1f2023;
    border-radius: 10px;
    overflow: hidden;
    cursor: pointer;
    transition: transform 0.2s;
  }

  .card:hover {
    transform: translateY(-4px);
  }

  .thumbnail {
    height: 120px;
    background: linear-gradient(135deg, #3a3aff, #7d7dff);
  }

  .card-info {
    padding: 10px;
  }

  .game-title {
    font-weight: 600;
    font-size: 14px;
  }

  .players {
    font-size: 12px;
    color: #9e9e9e;
    margin-top: 4px;
  }

  /* ===== LOGIN MODAL ===== */
  .overlay {
    display: none;
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,0.7);
    justify-content: center;
    align-items: center;
  }

  .login-box {
    background: #1f2023;
    width: 320px;
    padding: 24px;
    border-radius: 10px;
  }

  .login-box h2 {
    margin-top: 0;
    margin-bottom: 16px;
    font-size: 20px;
  }

  .login-box input {
    width: 100%;
    padding: 10px;
    margin-bottom: 12px;
    border-radius: 6px;
    border: none;
    background: #2b2c30;
    color: white;
  }

  .login-box button {
    width: 100%;
    background: #ffffff;
    color: #000;
    border: none;
    padding: 10px;
    border-radius: 6px;
    font-weight: 600;
    cursor: pointer;
  }

  .demo-text {
    text-align: center;
    font-size: 11px;
    color: #8a8a8a;
    margin-top: 10px;
  }
</style>
</head>

<body>

<header>
  <div class="logo">RB</div>
  <div class="header-buttons">
    <button onclick="openLogin()">Log In</button>
  </div>
</header>

<div class="main">
  <div class="welcome">Discover Experiences</div>
  <div class="subtitle">Play, create, and explore</div>

  <div class="grid">
    <div class="card">
      <div class="thumbnail"></div>
      <div class="card-info">
        <div class="game-title">Adventure World</div>
        <div class="players">👤 3.2K playing</div>
      </div>
    </div>

    <div class="card">
      <div class="thumbnail"></div>
      <div class="card-info">
        <div class="game-title">Obby Challenge</div>
        <div class="players">👤 5.8K playing</div>
      </div>
    </div>

    <div class="card">
      <div class="thumbnail"></div>
      <div class="card-info">
        <div class="game-title">RP City</div>
        <div class="players">👤 1.1K playing</div>
      </div>
    </div>
  </div>
</div>

<!-- LOGIN -->
<div class="overlay" id="overlay">
  <div class="login-box">
    <h2>Log In</h2>
    <input type="text" placeholder="Username">
    <input type="password" placeholder="Password">
    <button onclick="demo()">Log In</button>
    <div class="demo-text">Demo only • Not Roblox</div>
  </div>
</div>

<script>
  function openLogin() {
    document.getElementById("overlay").style.display = "flex";
  }

  function demo() {
    alert("Это демо-сайт. Данные никуда не отправляются 😊");
  }
</script>

</body>
</html>
