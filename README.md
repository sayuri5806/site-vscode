<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Catálogo de Vídeos</title>
    <link rel="stylesheet" href="styles.css">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.4.0/p5.js"></script>
</head>
<body>
    <div class="container">
        <h1>Catálogo de Vídeos</h1>
        
        <!-- Galeria de Vídeos -->
        <div id="catalogo" class="catalogo">
            <div class="video-item" onclick="playVideo(0)">
                <img src="thumb1.jpg" alt="Vídeo 1">
                <h3>Vídeo 1</h3>
            </div>
            <div class="video-item" onclick="playVideo(1)">
                <img src="thumb2.jpg" alt="Vídeo 2">
                <h3>Vídeo 2</h3>
            </div>
            <div class="video-item" onclick="playVideo(2)">
                <img src="thumb3.jpg" alt="Vídeo 3">
                <h3>Vídeo 3</h3>
            </div>
        </div>
        
        <!-- Player de Vídeo -->
        <div id="player" class="player">
            <video id="video-player" width="640" controls>
                <source id="video-source" src="" type="video/mp4">
            </video>
        </div>
    </div>

    <script src="sketch.js"></script>
</body>
</html>
/* styles.css */

/* Resetando margens e paddings */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f9;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
}

h1 {
    text-align: center;
    margin-bottom: 30px;
}

.catalogo {
    display: flex;
    justify-content: space-between;
    gap: 20px;
    flex-wrap: wrap;
    margin-bottom: 50px;
}

.video-item {
    width: 30%;
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    overflow: hidden;
    cursor: pointer;
    transition: transform 0.3s ease;
}

.video-item:hover {
    transform: scale(1.05);
}

.video-item img {
    width: 100%;
    height: 180px;
    object-fit: cover;
}

.video-item h3 {
    padding: 15px;
    text-align: center;
    background-color: #f1f1f1;
    margin: 0;
}

.player {
    text-align: center;
}

video {
    max-width: 100%;
    border: 2px solid #ccc;
    border-radius: 8px;
}
