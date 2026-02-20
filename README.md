<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For Ali 🤍</title>

<style>
body {
    margin: 0;
    padding: 0;
    font-family: 'Segoe UI', sans-serif;
    background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    overflow: hidden;
    text-align: center;
}

.container {
    max-width: 700px;
    padding: 40px;
    background: rgba(255,255,255,0.07);
    border-radius: 25px;
    backdrop-filter: blur(15px);
    box-shadow: 0 0 50px rgba(255,255,255,0.15);
    transition: 0.6s;
}

h1 {
    font-weight: 300;
    letter-spacing: 3px;
}

input {
    padding: 10px;
    border-radius: 20px;
    border: none;
    outline: none;
    margin-top: 10px;
}

button {
    margin-top: 25px;
    padding: 10px 25px;
    border-radius: 20px;
    border: none;
    background: #ff9a9e;
    color: white;
    cursor: pointer;
    transition: 0.3s;
}

button:hover {
    background: #ff6a88;
}

.hidden {
    display: none;
}

.fade {
    animation: fadeIn 1.5s ease;
}

@keyframes fadeIn {
    from { opacity: 0; transform: translateY(15px); }
    to { opacity: 1; transform: translateY(0); }
}

.message {
    margin-top: 20px;
    line-height: 1.6;
    opacity: 0.95;
}

.question {
    margin-top: 20px;
    font-style: italic;
    opacity: 0.85;
}
</style>

</head>
<body>

<!-- PAGE 1: PASSWORD -->
<div class="container fade" id="page1">
    <h1>💐</h1>
    <p>Enter the password.</p>
    <input type="password" id="passwordInput" placeholder="Password">
    <br>
    <button onclick="checkPassword()">Unlock</button>
</div>

<!-- PAGE 2 -->
<div class="container hidden fade" id="page2">
    <h1>Hi Ali ✨</h1>
    <div class="message">
        Of course it's you.  
        It was always going to be you typing that.
    </div>
    <button onclick="nextPage(2)">Continue</button>
</div>

<!-- PAGE 3 -->
<div class="container hidden fade" id="page3">
    <h1>Our Thing 🤍</h1>
    <div class="message">
        I don't want to change anything.  
        I don't want to cross lines.  
        I just want you to know what we have is rare.
    </div>

    <div class="question">
        Do you ever notice how easy it is for us?
    </div>

    <div class="question">
        How calm it feels?
    </div>

    <button onclick="nextPage(3)">Next</button>
</div>

<!-- PAGE 4 -->
<div class="container hidden fade" id="page4">
    <h1>If Timing Was Different...</h1>
    <div class="message">
        Maybe things would look different.  
        Maybe not.
        <br><br>
        But what matters is this —
    </div>
    <button onclick="nextPage(4)">Tell Me</button>
</div>

<!-- PAGE 5 FINAL -->
<div class="container hidden fade" id="page5">
    <h1>Final Page 🤍</h1>
    <div class="message">
        I respect you.  
        I respect her.  
        And I respect us.
        <br><br>
        Whatever this spark is…  
        it doesn’t need a label to be meaningful.
        <br><br>
        I’m just grateful I get to have you in my life.
    </div>

    <div class="question">
        No matter what happens — promise we protect this?
    </div>
</div>

<script>
function checkPassword() {
    const password = document.getElementById("passwordInput").value;
    if (password === "ali") {
        document.getElementById("page1").classList.add("hidden");
        document.getElementById("page2").classList.remove("hidden");
    } else {
        alert("Not quite 🤍");
    }
}

function nextPage(current) {
    document.getElementById("page" + current).classList.add("hidden");
    document.getElementById("page" + (current + 1)).classList.remove("hidden");
}
</script>

</body>
</htm
