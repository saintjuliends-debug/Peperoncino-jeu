# Peperoncino-jeu
Jeu cadeau interactif pour le restaurant Peperoncino

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
      max-width: 400px;
      margin: auto;
      background: #111;
      border-radius: 15px;
      padding: 25px;
      box-shadow: 0 0 20px rgba(0,0,0,0.6);
    }

    h1 {
      margin-bottom: 10px;
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

    #resultat {
      margin-top: 25px;
      font-size: 20px;
      font-weight: bold;
    }

    .conditions {
      font-size: 12px;
      opacity: 0.7;
      margin-top: 20px;
    }
  </style>
</head>

<body>

  <div class="box">
    <h1>🎁 Cadeau Mystère</h1>
    <p>Bienvenue chez <strong>Peperoncino</strong><br>
    Laissez un avis sur Google Maps pour découvrir votre cadeau !</p>

    <a href="https://www.google.com/maps/search/Peperoncino/?utm_campaign=ml-sul" 
       target="_blank" class="button-link" id="avisButton">Laisser un avis</a>

    <button id="decouvrir" style="display:none;" onclick="tirage()">Découvrir mon cadeau</button>

    <div id="resultat"></div>

    <div class="conditions">
      Offre valable une seule fois par table.<br>
      Présenter ce cadeau au serveur.
    </div>
  </div>

  <script>
    const cadeaux = [
      "🎉 10% de réduction sur la note",
      "🍰 1 dessert maison offert",
      "🍹 1 cocktail sans alcool offert"
    ];

    function tirage() {
      const hasard = Math.floor(Math.random() * cadeaux.length);
      document.getElementById("resultat").innerText = cadeaux[hasard];
    }

    // Affiche le bouton "Découvrir mon cadeau" après clic sur le lien Google Maps
    document.getElementById("avisButton").addEventListener("click", function(){
      document.getElementById("decouvrir").style.display = "inline-block";
    });
  </script>

</body>
</html>
