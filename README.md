<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Nosso Amor 💖</title>
  <style>
    body {
      background: #ffd6e9 url('https://i.imgur.com/xaZZa1g.png') repeat;
      font-family: 'Arial', sans-serif;
      text-align: center;
      color: #000;
    }

    h1 {
      margin-top: 20px;
      font-size: 2em;
      color: #000;
    }

    .fotos {
      display: flex;
      justify-content: center;
      gap: 20px;
      flex-wrap: wrap;
      margin: 20px 0;
    }

    .fotos img {
      max-width: 220px;
      width: 100%;
      height: auto;
      border-radius: 20px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.3);
    }

    .contador {
      font-size: 1.5em;
      margin-top: 20px;
      color: #000;
    }

    iframe {
      margin-top: 20px;
      border: none;
    }

    audio {
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <audio controls autoplay loop style="display: block; margin: 20px auto;">
    <source src="a-thousand-years.mp3" type="audio/mpeg">
    Seu navegador não suporta áudio HTML5.
  </audio>

  <h1>💘 Feliz Dia dos Namorados 💘</h1>
  
  <div class="fotos">
    <img src="foto1.jpg" alt="Foto 1" />
    <img src="foto2.jpg" alt="Foto 2" />
    <img src="foto3.jpg" alt="Foto 3" />
  </div>

  <div class="contador">
    <p>Estamos juntos há:</p>
    <div id="tempo"></div>
  </div>

  <script>
    const inicio = new Date("2022-04-22T19:00:00");
    function atualizarContador() {
      const agora = new Date();
      const diff = agora - inicio;

      const anos = Math.floor(diff / (1000 * 60 * 60 * 24 * 365));
      const dias = Math.floor((diff / (1000 * 60 * 60 * 24)) % 365);
      const horas = Math.floor((diff / (1000 * 60 * 60)) % 24);
      const minutos = Math.floor((diff / (1000 * 60)) % 60);
      const segundos = Math.floor((diff / 1000) % 60);

      document.getElementById("tempo").innerText =
        `${anos} anos, ${dias} dias, ${horas}h ${minutos}m ${segundos}s`;
    }
    setInterval(atualizarContador, 1000);
    atualizarContador();
  </script>
</body>
</html>
