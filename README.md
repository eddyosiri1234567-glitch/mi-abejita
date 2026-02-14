[index.html.txt](https://github.com/user-attachments/files/25310853/index.html.txt)
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para mi flor favorita 🌸</title>
    <style>
        body { background: #fff9c4; font-family: sans-serif; height: 100vh; margin: 0; display: flex; justify-content: center; align-items: center; overflow: hidden; text-align: center; }
        #btn-rebelde { background: #f44336; color: white; border: none; padding: 20px 40px; font-size: 24px; border-radius: 50px; position: absolute; cursor: pointer; transition: all 0.2s; box-shadow: 0 8px 15px rgba(0,0,0,0.3); font-weight: bold; }
        #carta { display: none; background: white; width: 85%; max-width: 400px; padding: 30px; border-radius: 30px; border: 4px solid #ffeb3b; box-shadow: 0 15px 40px rgba(0,0,0,0.2); }
        h1 { color: #e91e63; }
        .poema { font-style: italic; color: #444; line-height: 1.6; font-size: 19px; }
    </style>
</head>
<body>
    <div id="juego">
        <h2 style="color: #5d4037;">¿Podrás atrapar mi mensaje? 🐝</h2>
        <button id="btn-rebelde" onmouseover="mover()" ontouchstart="mover()" onclick="mostrar()">📩 ÁBREME</button>
    </div>
    <div id="carta">
        <h1>Para mi flor favorita 🌸</h1>
        <p class="poema">
            Tú eres la flor de pétalos bellos,<br>yo la abeja loca en tus cabellos.<br><br>
            A veces eres cactus con tus espinas,<br>pero igual me encantas cuando caminas.
        </p>
        <p style="color:#fbc02d; font-weight:bold; font-size: 22px;">Tu abejita fiel ❤️</p>
    </div>
    <script>
        let intentos = 0;
        function mover() {
            if (intentos < 6) {
                const btn = document.getElementById('btn-rebelde');
                btn.style.left = Math.random() * (window.innerWidth - btn.clientWidth) + 'px';
                btn.style.top = Math.random() * (window.innerHeight - btn.clientHeight) + 'px';
                intentos++;
            }
        }
        function mostrar() {
            document.getElementById('juego').style.display = 'none';
            document.getElementById('carta').style.display = 'block';
        }
    </script>
</body>
</html>
