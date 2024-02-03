<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Örnek</title>
</head>
<body>
    <!-- Kullanıcı Adı: Text Box -->
    <input type="text" id="username" placeholder="Kullanıcı Adı" onchange="saveCredentials()">

    <!-- Şifre: Text Box -->
    <input type="password" id="password" placeholder="Şifre" onchange="saveCredentials()">

    <!-- Kayıt Ol Buton -->
    <button id="registerButton">Kayıt Ol</button>

    <!-- A Buton -->
    <a href="#" id="link">Giriş Yap</a>

    <!-- ९ -->
    <div id="devideSymbol">९</div>

    <!-- Giriş Text Box -->
    <input type="text" id="loginBox" placeholder="Giriş Yap">

    <script>
        // Kullanıcı sayfasının yüklenmesi sırasında çalışacak kod
        window.onload = function() {
            loadCredentials();
        }

        function saveCredentials() {
            localStorage.setItem('username', document.getElementById('username').value);
            localStorage.setItem('password', document.getElementById('password').value);
        }

        function loadCredentials() {
            document.getElementById('username').value = localStorage.getItem('username');
            document.getElementById('password').value = localStorage.getItem('password');
        }
    </script>
</body>
</html>
