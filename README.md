<!DOCTYPE html><html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>KiritoVortex - MLBB Gaming</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #1a1a1a;
            color: white;
            margin: 0;
            padding: 0;
        }
        .logo {
            margin-top: 20px;
            width: 150px;
        }
        .container {
            padding: 20px;
        }
        .content {
            margin-top: 20px;
            padding: 20px;
            background-color: #333;
            border-radius: 10px;
            display: inline-block;
            width: 80%;
        }
        .nav {
            margin-top: 20px;
        }
        .nav button {
            background-color: #ff5733;
            color: white;
            border: none;
            padding: 10px 20px;
            margin: 5px;
            cursor: pointer;
            border-radius: 5px;
        }
        .nav button:hover {
            background-color: #e04d2c;
        }
        .signup-btn {
            background-color: #28a745;
        }
        .signup-btn:hover {
            background-color: #218838;
        }
    </style>
</head>
<body>
    <header>
        <img src="https://drive.google.com/uc?export=view&id=102zVzRY2j_-HbFfz0XOlmqKJQdNuLIUr" alt="KiritoVortex Logo" class="logo">
        <h1>Welcome to KiritoVortex</h1>
        <p>Your ultimate MLBB gaming hub!</p>
        <div class="nav">
            <button onclick="navigate('dashboard')">Dashboard</button>
            <button onclick="navigate('news')">News</button>
            <button onclick="navigate('videos')">Videos</button>
            <button onclick="navigate('photos')">Photos</button>
            <button class="signup-btn" onclick="signup()">Sign Up</button>
        </div>
    </header>
    <div class="container">
        <div class="content" id="content">
            <h2>About Us</h2>
            <p>We are passionate about Mobile Legends: Bang Bang, bringing you the latest news, strategies, and community events.</p>
        </div>
    </div>
    <script>
        function navigate(section) {
            document.getElementById('content').innerHTML = `<h2>${section.charAt(0).toUpperCase() + section.slice(1)}</h2><p>Content for ${section} will be added soon.</p>`;
        }
        function signup() {
            alert('Signup functionality coming soon!');
        }
    </script>
</body>
</html>