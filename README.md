# Babyroleta
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Roleta CMQ</title>
<style>
    body {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        height: 100vh;
        background-color: white;
        font-family: Arial, sans-serif;
    }
    canvas {
        border: 2px solid black;
        border-radius: 50%;
    }
    #pointer {
        position: absolute;
        top: 45px;
        width: 0;
        height: 0;
        border-left: 25px solid transparent;
        border-right: 25px solid transparent;
        border-top: 40px solid red;
    }
    button {
        margin-top: 20px;
        padding: 10px 20px;
        font-size: 18px;
        cursor: pointer;
    }
</style>
</head>
<body>
<div id="pointer"></div>
<canvas id="wheel" width="500" height="500"></canvas>
<button onclick="spinWheel()">Girar</button>
<script>
const canvas = document.getElementById('wheel');
const ctx = canvas.getContext('2d');
const slices = 5;
const sliceDeg = 360 / slices;
const colors = ["green", "red", "blue", "yellow", "pink"];
const numbers = [1, 2, 3, 4, 5];
let startAngle = 0;
let spinAngle = 0;
let spinTime = 0;
let spinTimeTotal = 0;

function drawWheel() {
    for (let i = 0; i < slices; i++) {
        const angle = startAngle + i * sliceDeg * Math.PI / 180;
        ctx.beginPath();
        ctx.moveTo(canvas.width / 2, canvas.height / 2);
        ctx.arc(canvas.width / 2, canvas.height / 2, 200, angle, angle + sliceDeg * Math.PI / 180);
        ctx.closePath();
        ctx.fillStyle = colors[i];
        ctx.fill();
        ctx.save();
        ctx.translate(canvas.width / 2, canvas.height / 2);
        ctx.rotate(angle + sliceDeg * Math.PI / 360);
        ctx.fillStyle = "black";
        ctx.font = "bold 40px Arial";
        ctx.fillText(numbers[i], 150, 10);
        ctx.restore();
    }
}

function spinWheel() {
    spinAngle = Math.random() * 10 + 10;
    spinTime = 0;
    spinTimeTotal = Math.random() * 3000 + 4000;
    rotateWheel();
}

function rotateWheel() {
    spinTime += 30;
    if (spinTime >= spinTimeTotal) {
        stopRotateWheel();
        return;
    }
    const spinAngleIncrement = spinAngle - (spinTime / spinTimeTotal) * spinAngle;
    startAngle += spinAngleIncrement * Math.PI / 180;
    draw();
    requestAnimationFrame(rotateWheel);
}

function stopRotateWheel() {
    const degrees = startAngle * 180 / Math.PI + 90;
    const arcd = sliceDeg;
    const index = Math.floor((360 - degrees % 360) / arcd) % slices;
    draw();
    console.log("Número sorteado:", numbers[index]);
}

function draw() {
    ctx.clearRect(0, 0, canvas.width, canvas.height);
    drawWheel();
}

draw();
</script>
</body>
</html>
