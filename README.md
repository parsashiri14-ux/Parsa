<!DOCTYPE html>
<html lang="fa">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>سایت پارسا</title>
  <style>
    :root {
      --main-bg: #000;
      --main-color: #0ff;
      --text-color: #fff;
    }
    body {
      margin: 0; font-family: sans-serif;
      background: var(--main-bg); color: var(--text-color);
    }
    header, footer {
      background: var(--main-color); color: #000;
      text-align: center; padding: 15px;
    }
    nav {
      display: flex; justify-content: center;
      background: #111;
    }
    nav a {
      color: var(--main-color); padding: 10px;
      text-decoration: none;
    }
    nav a:hover {
      background: #222;
    }
    section {
      padding: 20px;
    }
    .gallery img {
      width: 100px; margin: 5px; border-radius: 8px;
    }
    form input, form textarea {
      width: 100%; margin: 5px 0; padding: 10px;
      border: none; border-radius: 5px;
    }
    form button {
      background: var(--main-color); color: #000;
      padding: 10px; border: none; border-radius: 5px;
    }
    #adminPanel {
      display: none;
    }
  </style>
</head>
<body>
  <header><h1>سایت پارسا</h1></header>
  <nav>
    <a href="#home">خانه</a>
    <a href="#about">درباره</a>
    <a href="#gallery">گالری</a>
    <a href="#contact">تماس</a>
    <a href="#admin">مدیریت</a>
  </nav>

  <section id="home">
    <h2>خوش آمدید</h2>
    <p>سایتی کامل برای معرفی، ارتباط و نمایش آثار.</p>
  </section>

  <section id="about">
    <h2>درباره ما</h2>
    <p>ما با موبایل سایت می‌سازیم، طراحی می‌کنیم و برند می‌سازیم!</p>
  </section>

  <section id="gallery" class="gallery">
    <h2>گالری</h2>
    <img src="https://via.placeholder.com/100" alt="نمونه 1">
    <img src="https://via.placeholder.com/100" alt="نمونه 2">
    <img src="https://via.placeholder.com/100" alt="نمونه 3">
  </section>

  <section id="contact">
    <h2>تماس با ما</h2>
    <form>
      <input type="text" placeholder="نام شما">
      <input type="email" placeholder="ایمیل">
      <textarea placeholder="پیام شما"></textarea>
      <button type="submit">ارسال</button>
    </form>
  </section>

  <section id="admin">
    <h2>ورود مدیریت</h2>
    <input type="password" id="adminPass" placeholder="رمز عبور">
    <button onclick="checkAdmin()">ورود</button>
    <div id="adminPanel">
      <h3>پنل مدیریت</h3>
      <p>اینجا می‌تونی مطالب، تصاویر و تنظیمات رو مدیریت کنی.</p>
    </div>
  </section>

  <footer>
    <p>© 2025 ساخته شده توسط پارسا</p>
  </footer>

  <script>
    function checkAdmin() {
      const pass = document.getElementById("adminPass").value;
      if (pass === "1234") {
        document.getElementById("adminPanel").style.display = "block";
      } else {
        alert("رمز اشتباه است!");
      }
    }
  </script>
</body>
</html>
