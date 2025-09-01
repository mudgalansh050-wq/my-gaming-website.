# my-gaming-website.function showLogin() {
    document.getElementById("loginForm").style.display = "block";
    document.getElementById("signupForm").style.display = "none";
}

function showSignup() {
    document.getElementById("signupForm").style.display = "block";
    document.getElementById("loginForm").style.display = "none";
}

// Simple front-end login/signup (no real backend)
function signupUser() {
    const username = document.getElementById("signupUsername").value;
    const password = document.getElementById("signupPassword").value;
    if (username && password) {
        localStorage.setItem("user_" + username, password);
        alert("Signup successful! Now login.");
        showLogin();
    } else {
        alert("Please enter username and password.");
    }
}

function loginUser() {
    const username = document.getElementById("loginUsername").value;
    const password = document.getElementById("loginPassword").value;
    const storedPassword = localStorage.getItem("user_" + username);
    if (storedPassword && storedPassword === password) {
        alert("Login successful!");
        document.getElementById("loginForm").style.display = "none";
    } else {
        alert("Invalid username or password.");
    }
}<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Gaming Website</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>My Gaming Website</h1>
        <nav>
            <button onclick="showLogin()">Login</button>
            <button onclick="showSignup()">Signup</button>
        </nav>
    </header>

    <main>
        <!-- Login Form -->
        <div id="loginForm" class="form-container">
            <h2>Login</h2>
            <input type="text" id="loginUsername" placeholder="Username">
            <input type="password" id="loginPassword" placeholder="Password">
            <button onclick="loginUser()">Login</button>
        </div>

        <!-- Signup Form -->
        <div id="signupForm" class="form-container">
            <h2>Signup</h2>
            <input type="text" id="signupUsername" placeholder="Username">
            <input type="password" id="signupPassword" placeholder="Password">
            <button onclick="signupUser()">Signup</button>
        </div>

        <!-- Games Section -->
        <section id="games">
            <h2>Available Games</h2>
            <div class="game-grid">
                <div class="game-card">
                    <img src="images/racing.png" alt="Racing Game">
                    <h3>Racing</h3>
                    <button>Play Now</button>
                </div>
                <div class="game-card">
                    <img src="images/ff.png" alt="Free Fire">
                    <h3>Free Fire</h3>
                    <button>Play Now</button>
                </div>
                <div class="game-card">
                    <img src="images/bgmi.png" alt="BGMI">
                    <h3>BGMI</h3>
                    <button>Play Now</button>
                </div>
                <div class="game-card">
                    <img src="images/coc.png" alt="Clash of Clans">
                    <h3>Clash of Clans</h3>
                    <button>Play Now</button>
                </div>
                <div class="game-card">
                    <img src="images/cod.png" alt="COD">
                    <h3>Call of Duty</h3>
                    <button>Play Now</button>
                </div>
            </div>
        </section>
    </main>

    <script src="script.js"></script>
</body>
</html>/* General styles */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background: #1e1e1e;
    color: #fff;
}

header {
    background: #111;
    padding: 10px 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

header h1 {
    margin: 0;
}

nav button {
    margin-left: 10px;
    padding: 5px 15px;
    cursor: pointer;
}

/* Forms */
.form-container {
    display: none;
    margin: 20px auto;
    max-width: 300px;
    padding: 20px;
    background: #222;
    border-radius: 10px;
}

.form-container input {
    width: 100%;
    padding: 10px;
    margin: 10px 0;
    border: none;
    border-radius: 5px;
}

.form-container button {
    width: 100%;
    padding: 10px;
    border: none;
    background: #ff4500;
    color: #fff;
    cursor: pointer;
    border-radius: 5px;
}

/* Games Section */
#games {
    padding: 20px;
    text-align: center;
}

.game-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 20px;
    margin-top: 20px;
}

.game-card {
    background: #222;
    padding: 10px;
    border-radius: 10px;
}

.game-card img {
    width: 100%;
    height: 120px;
    object-fit: cover;
    border-radius: 10px;
}

.game-card button {
    margin-top: 10px;
    padding: 5px 10px;
    border: none;
    background: #ff4500;
    color: #fff;
    cursor: pointer;
    border-radius: 5px;
}function showLogin() {
    document.getElementById("loginForm").style.display = "block";
    document.getElementById("signupForm").style.display = "none";
}

function showSignup() {
    document.getElementById("signupForm").style.display = "block";
    document.getElementById("loginForm").style.display = "none";
}

// Simple front-end login/signup (no real backend)
function signupUser() {
    const username = document.getElementById("signupUsername").value;
    const password = document.getElementById("signupPassword").value;
    if (username && password) {
        localStorage.setItem("user_" + username, password);
        alert("Signup successful! Now login.");
        showLogin();
    } else {
        alert("Please enter username and password.");
    }
}

function loginUser() {
    const username = document.getElementById("loginUsername").value;
    const password = document.getElementById("loginPassword").value;
    const storedPassword = localStorage.getItem("user_" + username);
    if (storedPassword && storedPassword === password) {
        alert("Login successful!");
        document.getElementById("loginForm").style.display = "none";
    } else {
        alert("Invalid username or password.");
    }
}function showLogin() {
    document.getElementById("loginForm").style.display = "block";
    document.getElementById("signupForm").style.display = "none";
}

function showSignup() {
    document.getElementById("signupForm").style.display = "block";
    document.getElementById("loginForm").style.display = "none";
}

// Simple front-end login/signup (no real backend)
function signupUser() {
    const username = document.getElementById("signupUsername").value;
    const password = document.getElementById("signupPassword").value;
    if (username && password) {
        localStorage.setItem("user_" + username, password);
        alert("Signup successful! Now login.");
        showLogin();
    } else {
        alert("Please enter username and password.");
    }
}

function loginUser() {
    const username = document.getElementById("loginUsername").value;
    const password = document.getElementById("loginPassword").value;
    const storedPassword = localStorage.getItem("user_" + username);
    if (storedPassword && storedPassword === password) {
        alert("Login successful!");
        document.getElementById("loginForm").style.display = "none";
    } else {
        alert("Invalid username or password.");
    }
}
