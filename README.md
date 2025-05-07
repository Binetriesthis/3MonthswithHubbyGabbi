<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Origami Heart Surprise</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: #fff0f0;
      font-family: 'Segoe UI', sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      height: 100vh;
    }

    .heart {
      width: 150px;
      height: 150px;
      background: red;
      position: relative;
      transform: rotate(-45deg);
      cursor: pointer;
      margin-bottom: 20px;
      transition: opacity 0.3s ease;
    }

    .heart:before,
    .heart:after {
      content: "";
      width: 150px;
      height: 150px;
      background: red;
      border-radius: 50%;
      position: absolute;
    }

    .heart:before {
      top: -75px;
      left: 0;
    }

    .heart:after {
      left: 75px;
      top: 0;
    }

    .hidden {
      display: none;
    }

    .video-container {
      margin-top: 20px;
      text-align: center;
    }

    iframe {
      width: 90vw;
      max-width: 560px;
      height: 315px;
      border: none;
    }

    .letter {
      max-width: 600px;
      margin-top: 20px;
      padding: 20px;
      background: white;
      border-radius: 12px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
      text-align: left;
      line-height: 1.6;
    }
  </style>
</head>
<body>

  <div id="heart" class="heart" title="Click me!"></div>

  <div id="content" class="hidden">
    <div class="video-container">
      <iframe 
        src="https://www.youtube.com/embed/kwxRqEjmfxM"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen>
      </iframe>
    </div>

    <div class="letter">
      <h2>Dear Gabbi,</h2>
      <p>
        Three months ago, everything changed for the better.<br>
        You bring light, laughter, and so much love into my life. This little surprise is just a small reflection of how much you mean to me.<br><br>
        I can't wait to make more memories with you.<br><br>
        With all my heart,<br>
        Your Hubby 💖
      </p>
    </div>
  </div>

  <script>
    const heart = document.getElementById('heart');
    const content = document.getElementById('content');

    heart.addEventListener('click', () => {
      heart.style.opacity = 0;
      setTimeout(() => {
        heart.style.display = 'none';
        content.classList.remove('hidden');
        document.body.style.justifyContent = 'flex-start';
        document.body.style.paddingTop = '40px';
      }, 300);
    });
  </script>

</body>
</html>
