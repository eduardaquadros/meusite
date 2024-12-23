<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TE AMO.</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background: linear-gradient(45deg, #ffb6c1, #f8a5c2); /* Gradiente suave */
      color: #333;
      padding: 20px;
      overflow: hidden;
      position: relative;
      animation: backgroundChange 10s infinite alternate; /* Mudança de fundo suave */
    }

    @keyframes backgroundChange {
      0% {
        background: linear-gradient(45deg, #ffb6c1, #f8a5c2);
      }
      100% {
        background: linear-gradient(45deg, #f8a5c2, #ffb6c1);
      }
    }

    h1 {
      color: #d32f2f;
      transition: color 0.3s ease;
      font-size: 3em;
    }

    h1:hover {
      color: #ff4081; /* Mudança de cor suave */
      text-shadow: 0 0 10px rgba(255, 105, 180, 0.8); /* Efeito de brilho suave no título */
    }

    .message {
      margin-top: 20px;
      font-size: 1.5em;
      color: #d32f2f;
      transition: color 0.3s ease;
      opacity: 0;
      animation: fadeIn 2s forwards;
    }

    @keyframes fadeIn {
      0% {
        opacity: 0;
      }
      100% {
        opacity: 1;
      }
    }

    .message:hover {
      color: #ff4081; /* Efeito de brilho suave no texto */
    }

    .hearts {
      margin-top: 20px;
      font-size: 24px;
      color: red;
    }

  

    /* Neve */
    .snowflake {
      position: fixed;
      top: -10px;
      color: white;
      font-size: 1em;
      user-select: none;
      z-index: 1000;
      animation-name: fall;
      animation-timing-function: linear;
      animation-iteration-count: infinite;
    }

    @keyframes fall {
      0% {
        transform: translateY(0);
      }
      100% {
        transform: translateY(100vh);
      }
    }

    /* Efeito de brilho e cor suavizada na imagem */
    img {
      transition: transform 0.3s ease, box-shadow 0.5s ease, filter 0.3s ease;
    }

    img:hover {
      transform: scale(1.1); /* Aumenta a imagem em 10% */
      box-shadow: 0px 0px 20px rgba(255, 105, 180, 0.8); /* Brilho suave */
      filter: brightness(1.2); /* Aumenta o brilho */
    }



    /* Efeito de corações animados */
    .heart {
      position: absolute;
      font-size: 24px;
      color: red;
      animation: heart-animation 1s ease-in-out infinite;
      z-index: 100;
    }

    @keyframes heart-animation {
      0% {
        transform: scale(0);
        opacity: 1;
      }
      100% {
        transform: scale(1.5);
        opacity: 0;
        transform: translateY(-100px);
      }
    }

    .heart:nth-child(even) {
      animation-duration: 1.5s;
    }

    /* Efeito de rosas animadas */
    .rose {
      position: absolute;
      font-size: 30px;
      color: pink;
      animation: rose-animation 2s ease-out infinite;
      z-index: 100;
    }

    @keyframes rose-animation {
      0% {
        transform: scale(0);
        opacity: 1;
      }
      100% {
        transform: scale(1.2);
        opacity: 0;
        transform: translateY(-150px);
      }
    }

    /* Corações flutuando pelo fundo */
    .floating-heart {
      position: absolute;
      font-size: 30px;
      color: red;
      animation: float-heart 5s infinite ease-in-out;
    }

    @keyframes float-heart {
      0% {
        transform: translateY(0) scale(1);
      }
      50% {
        transform: translateY(-100px) scale(1.2);
      }
      100% {
        transform: translateY(0) scale(1);
      }
    }

  </style>
</head>
<body>
  <h1>Feliz Natal, meu amor! ❤️</h1>
  <img src="eueisa.jpeg" alt="Descrição da imagem" width="250" id="image">
  
  <div class="message">
    <p>[Falei que sou técnica em info (mas também não lembro de muitas coisas por isso é simples)!!] </p>
     Eu te amo muito, obrigada por tanto.  🎄🎅
    <br>Esse ano pedi pro Papai Noel me dar a vida inteira com você.  💖
  </div>



  <!-- Script para Neve -->
  <script>
    function createSnowflake() {
      const snowflake = document.createElement('div');
      snowflake.classList.add('snowflake');
      snowflake.innerHTML = '❄';
      snowflake.style.left = Math.random() * 100 + 'vw';
      snowflake.style.animationDuration = Math.random() * 3 + 2 + 's';
      snowflake.style.fontSize = Math.random() * 20 + 10 + 'px';

      document.body.appendChild(snowflake);

      setTimeout(() => {
        snowflake.remove();
      }, 5000);
    }

    setInterval(createSnowflake, 200);

    // Efeito de corações
    const image = document.getElementById('image');
    image.addEventListener('mouseenter', function(event) {
      createHearts(event);
      createRoses(event);
    });

    function createHearts(event) {
      const heart = document.createElement('div');
      heart.classList.add('heart');
      heart.innerHTML = '❤️';
      heart.style.left = (event.pageX - 25) + 'px';  // Posição do mouse
      heart.style.top = (event.pageY - 25) + 'px';   // Posição do mouse
      document.body.appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 1000); // Remove os corações depois de 1 segundo
    }

    // Efeito de rosas
    function createRoses(event) {
      const rose = document.createElement('div');
      rose.classList.add('rose');
      rose.innerHTML = '🌹';
      rose.style.left = (event.pageX - 30) + 'px';  // Posição do mouse
      rose.style.top = (event.pageY - 30) + 'px';   // Posição do mouse
      document.body.appendChild(rose);

      setTimeout(() => {
        rose.remove();
      }, 2000); // Remove as rosas depois de 2 segundos
    }

    // Corações flutuando pelo fundo
    function createFloatingHearts() {
      const floatingHeart = document.createElement('div');
      floatingHeart.classList.add('floating-heart');
      floatingHeart.innerHTML = '❤️';
      floatingHeart.style.left = Math.random() * 100 + 'vw';
      floatingHeart.style.top = Math.random() * 100 + 'vh';
      document.body.appendChild(floatingHeart);

      setTimeout(() => {
        floatingHeart.remove();
      }, 5000);
    }

    setInterval(createFloatingHearts, 1000); // Cria corações flutuantes a cada segundo

  


  </script>

</body>
</html>
