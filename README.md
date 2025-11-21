<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Auto Login</title>
<script>
window.onload = function () {

    // === BURAYA KENDİN YAZACAKSIN ===
    var myEmail = "mandarineczgumbet";  
    var myPass  = "mandarinecz929g";           
    // ================================

    // login sayfasını iframe içinde yüklüyoruz
    var iframe = document.getElementById("loginframe");

    iframe.onload = function () {
        var doc = iframe.contentDocument || iframe.contentWindow.document;

        // form alanlarına eriş
        doc.querySelector('input[name="email"]').value = myEmail;
        doc.querySelector('input[name="password"]').value = myPass;

        // 1 saniye bekle → login tıkla
        setTimeout(function () {
            var btn = doc.querySelector('button[type="submit"]');
            if (btn) btn.click();
        }, 1000);
    };
};
</script>

<style>
body, html { margin:0; padding:0; height:100%; }
iframe { width:100%; height:100%; border:0; }
</style>
</head>
<body>
<iframe id="loginframe" src="https://tr.eczanesistemi.net/login"></iframe>
</body>
</html>
