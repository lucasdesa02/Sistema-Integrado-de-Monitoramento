<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sistema Integrado de Monitoramento em Natividade/RJ</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-image: url('https://i.imgur.com/kxGJMBD.png');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            position: relative;
            color: #f1f1f1;
            user-select: none;
        }

        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.4);
            z-index: -1;
        }

        h1 {
            margin-top: 20px;
            text-align: center;
            text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.8);
        }

        .container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
            padding: 20px;
        }

        .camera-container {
            flex: 1;
            min-width: 300px;
            max-width: 500px;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 5px;
        }

        .title {
            background-color: rgba(0, 0, 0, 0.7);
            padding: 5px 10px;
            color: white;
            font-size: 18px;
            font-weight: bold;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.8);
            text-align: center;
            transition: transform 0.3s ease;
        }

        .title:hover {
            transform: scale(1.05);
        }

        .camera {
            width: 100%;
            aspect-ratio: 16/9;
            background-color: transparent;
            border: none;
            overflow: hidden;
            position: relative;
            box-shadow: 0px 4px 15px rgba(0, 0, 0, 0.8);
            transition: transform 0.3s ease;
        }

        .camera:hover {
            transform: scale(1.02);
        }

        iframe {
            width: 100%;
            height: 100%;
            border: none;
        }

        .emergency-numbers {
            position: fixed;
            bottom: 20px;
            left: 20px;
            background-color: rgba(0, 0, 0, 0.7);
            padding: 10px;
            color: white;
            font-size: 18px;
            border-radius: 5px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.8);
            z-index: 10;
        }

        .emergency-numbers p {
            margin: 5px 0;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .emergency-numbers i {
            color: #f1c40f;
        }

        footer {
            text-align: center;
            padding: 20px;
            background-color: rgba(0, 0, 0, 0.7);
            color: white;
            font-size: 16px;
            font-weight: bold;
            position: fixed;
            bottom: 0;
            width: 100%;
            box-shadow: 0 -2px 10px rgba(0, 0, 0, 0.8);
        }
    </style>
    <script>
        document.addEventListener('keydown', function (e) {
            const iframes = document.querySelectorAll('iframe');
            if (e.key === '1') iframes[0].focus();
            if (e.key === '2') iframes[1].focus();
            if (e.key === '3') iframes[2].focus();
            if (e.key === 'f') iframes[0].requestFullscreen();
        });
    </script>
</head>
<body>
    <h1>Sistema Integrado de Monitoramento em Natividade/RJ</h1>

    <div class="container">
        <div class="camera-container">
            <div class="title">CENTRO</div>
            <div class="camera">
                <iframe id="video1" src="https://www.youtube.com/embed/1LwyY82ydq0?autoplay=1&mute=1&controls=1&rel=0&modestbranding=1&showinfo=0&iv_load_policy=3" allowfullscreen></iframe>
            </div>
        </div>
        <div class="camera-container">
            <div class="title">TREVO NATIVIDADE X VARRE-SAI</div>
            <div class="camera">
                <iframe id="video2" src="https://www.youtube.com/embed/8GWx8VCVi2s?autoplay=1&mute=1&controls=1&rel=0&modestbranding=1&showinfo=0&iv_load_policy=3" allowfullscreen></iframe>
            </div>
        </div>
        <div class="camera-container">
            <div class="title">RIO CARANGOLA</div>
            <div class="camera">
                <iframe id="video3" src="https://www.youtube.com/embed/nhrIjPF_7go?autoplay=1&mute=1&controls=1&rel=0&modestbranding=1&showinfo=0&iv_load_policy=3" allowfullscreen></iframe>
            </div>
        </div>
    </div>

    <div class="emergency-numbers">
        <p><i class="fas fa-fire"></i> Bombeiro: <strong>193</strong></p>
        <p><i class="fas fa-shield-alt"></i> Polícia Militar: <strong>190</strong></p>
        <p><i class="fas fa-ambulance"></i> SAMU: <strong>192</strong></p>
    </div>

    <footer>
        Copyright © 2025 TV Natividade | Lucas de Sá. Todos os direitos reservados.
    </footer>
</body>
</html>
