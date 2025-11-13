<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Hello World</title>
    <style>
        body { font-family: Arial, sans-serif; padding: 20px; }
        h1, h2 { margin: 10px 0; }
    </style>
</head>
<body>

<h1>Hello World</h1>

<h2>Current Time:</h2>
<p id="clock">Loading...</p>

<h2>Navigator Info:</h2>
<p id="navigatorInfo"></p>

<button id="btn">Click to show Alert Msg</button>

<script>
    // تحديث الوقت كل ثانية
    function updateClock() {
        document.getElementById('clock').textContent = new Date().toLocaleTimeString();
    }
    setInterval(updateClock, 1000);
    updateClock(); // لتظهر الساعة مباشرة عند تحميل الصفحة

    // عرض معلومات المتصفح
    const navInfo = `
        <strong>Navigator.userAgent:</strong> ${navigator.userAgent}<br>
        <strong>Navigator.appName:</strong> ${navigator.appName}<br>
        <strong>Navigator.appCodeName:</strong> ${navigator.appCodeName}<br>
        <strong>Navigator.appVersion:</strong> ${navigator.appVersion}
    `;
    document.getElementById('navigatorInfo').innerHTML = navInfo;

    // زر التنبيه
    document.getElementById('btn').addEventListener('click', function() {
        alert('JS alert test');
        console.log("JS alert test");
    });
</script>

</body>
</html>
