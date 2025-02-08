# ValentineDay
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>San Valentín</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&display=swap');
        body {
            text-align: center;
            font-family: 'Dancing Script', cursive;
            background: linear-gradient(to right, #ff9a9e, #fad0c4);
            color: #773f0a;
        }
        .container {
            margin-top: 20%;
        }
        .btn {
            margin-top: 20px;
            padding: 10px 20px;
            font-size: 18px;
            background-color: #ff4d4d;
            color: rgb(238, 231, 229);
            border: none;
            cursor: pointer;
            border-radius: 5px;
        }
        .btn:disabled {
            background-color: #6e470c;
            cursor: not-allowed;
        }
    </style>
</head>
<body>
    <div class="container" id="pregunta">
        <h2>Hola mi niña soy Bæ, hoy solo tengo una simple pregunta:</h2>
        <h1>Will you be my Valentine?</h1>
        <label>
            <input type="radio" name="respuesta" id="si"> Sí
        </label>
        <label>
            <input type="radio" name="respuesta" id="no" disabled> No
        </label>
        <br>
        <button class="btn" id="responder" disabled>Responder</button>
    </div>
    
    <div class="container" id="respuesta" style="display: none;">
        <h2>Sabías que aceptarías, te amo mi niña ❤️</h2>
        <h1>Aunque puede que estemos lejos, me las arreglaré para que todo sea mágico y feliz como tú me haces sentir.</h1>
    </div>
    
    <script>
        document.getElementById('si').addEventListener('change', function() {
            document.getElementById('responder').disabled = false;
        });
        
        document.getElementById('responder').addEventListener('click', function() {
            document.getElementById('pregunta').style.display = 'none';
            document.getElementById('respuesta').style.display = 'block';
        });
    </script>
</body>
</html>
