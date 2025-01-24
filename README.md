<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Telegram Mini App</title>
</head>
<body>
    <h1>Welcome to My Mini App</h1>
    <p id="user-info"></p>
    <button onclick="Telegram.WebApp.close()">Close App</button>

    <script>
        Telegram.WebApp.ready(); // Initializes the Mini App
        
        // Display user information
        const user = Telegram.WebApp.initDataUnsafe?.user;
        document.getElementById('user-info').textContent = `Hello, ${user?.first_name || 'User'}!`;
    </script>
</body>
</html>
