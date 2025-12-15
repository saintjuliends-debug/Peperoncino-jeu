<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Cadeau Mystère - Peperoncino</title>

  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #1c1c1c, #3a3a3a);
      color: white;
      text-align: center;
      padding: 30px;
    }

    .box {
      max-width: 420px;
      margin: auto;
      background: #111;
      border-radius: 15px;
      padding: 25px;
      box-shadow: 0 0 20px rgba(0,0,0,0.6);
    }

    button, a.button-link {
      background: #e63946;
      color: white;
      border: none;
      padding: 15px 25px;
      font-size: 18px;
      border-radius: 10px;
      cursor: pointer;
      margin-top: 20px;
      text-decoration: none;
      display: inline-block;
    }

    button:hover, a.button-link:hover {
      background: #ff4d5a;
    }

    button:disabled {
      background: #555;
      cursor: not-allowed;
    }

    #resultat {
      margin-top: 25px;
      font-size: 20px;
      font-weight: bold;
    }

    .code {
      margin-top: 15px;
      font-size: 18px;
      background: #222;
      padding: 10px;
      border-radius: 8px;
      letter-spacing: 2px;
    }

    .serveur {
      margin-top: 15px;
      font-size: 14px;
      opacity: 0.85;
      color: #ffd166;
    }

    .conditions {
      font-size: 12px;
      opacity: 0.6;
      margin-top: 20px;
    }
  </style>
</head>

<body>

<div class="box">
  <h1>🎁 Cadeau Mystère</h1>
  <p>
    Laissez un avis Google<br>
    et découvrez votre cadeau
  </p>

  <a href="https://www.google.com/maps/search/Peperoncino/" 
     target="_blank"
     class="button-link"
     id="avisButton">
     Laisser un avis
  </a>

  <button id="decouvrir" style="display:none;" onclick="tirage()">
    Découvrir mon cadeau
  </button>

  <div id="resultat"></div>
  <div id="code" class="code"></div>
  <div id="serveur" class="serveur"></div>

  <div class="conditions">
    Offre valable 1 fois par appareil / 24h.<br>
    Le code doit être validé par le serveur.
  </div>
</div>

<script>
  const cadeaux = [
    "🎉 10% de réduction sur la note",
    "🍰 Dessert maison offert",
    "🍹 Cocktail sans alcool offert"
  ];

  const STORAGE_KEY = "cadeauPeperoncino";
  const DUREE = 24 * 60 * 60 * 1000; // 24h

  function genererCode() {
    return "PP-" + Math.random().toString(36).substring(2, 6).toUpperCase();
  }

  function afficherCadeau(data) {
    document.getElementById("resultat").innerText = data.cadeau;
    document.getElementById("code").innerText = "Code : " + data.code;
    document.getElementById("serveur").innerText =
      "À faire valider par le serveur aujourd’hui.";
    document.getElementById("decouvrir").disabled = true;
    document.getElementById("decouvrir").style.display = "inline-block";
  }

  window.onload = function () {
    const saved = localStorage.getItem(STORAGE_KEY);
    if (saved) {
      const data = JSON.parse(saved);
      if (Date.now() - data.date < DUREE) {
        afficherCadeau(data);
      } else {
        localStorage.removeItem(STORAGE_KEY);
      }
    }
  };

  function tirage() {
    if (localStorage.getItem(STORAGE_KEY)) {
      alert("Cadeau déjà récupéré aujourd’hui 🎁");
      return;
    }

    const cadeau = cadeaux[Math.floor(Math.random() * cadeaux.length)];
    const data = {
      cadeau: cadeau,
      code: genererCode(),
      date: Date.now()
    };

    localStorage.setItem(STORAGE_KEY, JSON.stringify(data));
    afficherCadeau(data);
  }

  document.getElementById("avisButton").addEventListener("click", function () {
    document.getElementById("decouvrir").style.display = "inline-block";
  });
</script>

</body>
</html>
