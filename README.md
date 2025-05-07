
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
      <h2>Hi Hubs!</h2>
      <p>
        Happy 3rd Monthsary!<br>
        As the days go by, you make me realize how much I have always wished to have you. How my heart longs to find its other half and discover a deeper meaning to this life.<br><br>
        You make me feel happy, excited, curious, worried at times, sad because I miss you, and yes, even a little angry because, why are you so 
        pogi and yet you're not here? But above all, you make me feel loved.<br><br>
        My love, never forget that you are precious.<br><br>
        You are, have always been, and will always be-- especially for me.<br><br>
        Thank you for existing my love. Thank you for bringing me laughter and giggles, and all sorts of emotions. <br><br>
        Thank you for trying. Thank you for not giving up on moments you and I havent crossed paths yet.<br><br>
        And now that we found each other, be assured that I will always be here.<br><br>
        For whatever comes in life, you're the person I'll always ask:<br><br>

        Wanna come along with me? <br><br>
        
        With all my heart,<br>
        Your Bine 💖
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
