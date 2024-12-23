<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>te amo.</title>
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
      
