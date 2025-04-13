<!DOCTYPE html>
<html lang="ml">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Vishu Surprise</title>
  <style>
    body {
      background-color: white;
      color: black;
      font-family: 'Segoe UI', sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      font-size: 1.5em;
      text-align: center;
      padding: 20px;
    }
    #text {
      transition: opacity 0.5s ease-in-out;
    }
  </style>
</head>
<body>
  <div id="text">പൂക്കളെ പോലും അഴക് പഠിപ്പിക്കുന്ന ആ ചിരിക്ക് വിഷുദിനാശംസകൾ!</div>

  <script>
    const messages = [
      { text: "പൂക്കളെ പോലും അഴക് പഠിപ്പിക്കുന്ന ആ ചിരിക്ക് വിഷുദിനാശംസകൾ!", duration: 5000 },
      { text: "🌸 Happy Vishu, my precious Ammukutty 🌸", duration: 6000 },
      { text: "ഈ വിഷുവിൽ ഞാൻ അപേക്ഷിക്കുന്ന ഒരേൊരു കാര്യമുണ്ട് – നീ എന്നോട് എന്നും കൂടെയിരിക്കണം.", duration: 8000 },
      { text: "😘💛", duration: 3000 }
    ];

    let index = 1;
    const textElement = document.getElementById("text");

    function showNextMessage() {
      if (index < messages.length) {
        textElement.style.opacity = 0;
        setTimeout(() => {
          textElement.textContent = messages[index].text;
          textElement.style.opacity = 1;
          setTimeout(showNextMessage, messages[index].duration);
          index++;
        }, 500);
      }
    }

    setTimeout(showNextMessage, messages[0].duration);
  </script>
</body>
</html>
# Ammukutty
