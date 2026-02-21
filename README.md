<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Birthday Surprise</title>

<style>
body {
    margin: 0;
    background: radial-gradient(circle, #8B0000, black);
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    flex-direction: column;
    font-family: Arial, sans-serif;
    overflow: hidden;
    color: white;
}

.door {
    width: 230px;
    height: 370px;
    border-radius: 12px;
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    font-size: 24px;
    font-weight: bold;
    letter-spacing: 2px;
    transition: transform 1s ease, box-shadow 0.5s;
}

#firstDoor {
    background: linear-gradient(45deg, #ff0000, #8B0000);
    box-shadow: 0 0 40px red;
}

#secondDoor {
    background: linear-gradient(45deg, darkred, black);
    box-shadow: 0 0 40px crimson;
    display: none;
}

.door:hover {
    box-shadow: 0 0 60px #ff4d4d;
}

.open {
    transform: rotateY(90deg);
}

.message {
    font-size: 26px;
    text-align: center;
    display: none;
    margin-top: 20px;
    max-width: 80%;
}
</style>
</head>

<body>

<div id="firstDoor" class="door">I'M SORRY</div>
<div id="secondDoor" class="door">I'M SORRY</div>

<div id="message1" class="message">
Happy Birthday to the girl who makes my heart race faster than my morning coffee. You’re my sweetest addiction! ☕💖
</div>

<div id="message2" class="message">
HAPPY BIRTHDAY BOXY DE LUFFY AND MY SWEET CUPCAKE
</div>

<script>
const firstDoor = document.getElementById("firstDoor");
const secondDoor = document.getElementById("secondDoor");
const message1 = document.getElementById("message1");
const message2 = document.getElementById("message2");

firstDoor.onclick = function() {
    firstDoor.classList.add("open");
    setTimeout(() => {
        firstDoor.style.display = "none";
        message1.style.display = "block";
        secondDoor.style.display = "flex";
    }, 1000);
};

secondDoor.onclick = function() {
    secondDoor.classList.add("open");
    setTimeout(() => {
        secondDoor.style.display = "none";
        message2.style.display = "block";
    }, 1000);
};
</script>

</body>
</html>
